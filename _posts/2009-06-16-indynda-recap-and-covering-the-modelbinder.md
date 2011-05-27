---
layout: post
title: IndyNDA Recap and Covering the ModelBinder
categories: speaking ASP.Net-MVC
---
## IndyNDA Recap and Covering the ModelBinder

I want to thank all that attended my MVC presentation in Indy last week. I had a great time speaking, and even though I left a portion of my code sample out (model binders, which I’ll cover below), I thought it went well and I got some good questions during and after. I apologize for leaving it out of the talk, but I get to write a little blog post about it.

A couple housekeeping things before I cover the ModelBinder part I missed.

During the post talk talking, [Dave](http://twitter.com/daveleininger) asked me about a grid option in MVC. One we’ve been using is [Flexigrid](http://flexigrid.info/). It will do paging and sorting on its own, and will call back to your controller on its own for a little JSON. The big gotcha here is it runs on an older version of jQuery, which bit us in the butt on Friday on our project.

The blog post that contains the code and explanation…well better explanation than, “I copied and pasted and it worked,” on the partial views is on [Steve Sanderson’s blog](http://blog.codeville.net/2008/10/14/partial-requests-in-aspnet-mvc/).

Now on to the part I forgot…

###ModelBinder

I’m still feeling bad for not sharing this part. I got a question about it after the presentation, and that’s when I realized I totally forgot the edit page, which was going to demonstrate the ModelBinder. (Among other things, like the FluentHTML controls.)

If you have the code form above, the files in play here are InventoryController.cs and Edit.aspx. AssaultItemEditModel.cs is the object passed, but it’s just a property bag.

For the Reader’s Digest version: the ModelBinder works on the premise of convention over configuration, so the naming of your fields matter in that they have to match the property names of the object you want to bind to.

For the example I missed, we had the edit model that we wanted to bind to:

    public class AssaultItemEditModel 
    { 
        public virtual int Id { get; set; } 
        public virtual string Type { get; set; } 
        public virtual string Description { get; set; } 
        public virtual int LoadValue { get; set; }
    }

The view had the form fields hooked to that edit model through the Fluent HTML controls from MVC Contrib.

    <% Html.BeginForm("Save", "Inventory");%>
        <h2>Edit <%=Html.Encode(Model.Type) %></h2> 
        <%=this.Hidden(x => x.Id) %> 
        <ul class="details"> 
            <li><span>Type: </span><%=this.TextBox(x => x.Type) %></li> 
            <li><span>Description: </span><%=this.TextBox(x => x.Description) %></li> 
            <li><span>Load Value: </span><%=this.TextBox(x => x.LoadValue) %></li> 
            <li><%=this.SubmitButton("Save") %></li> 
        </ul> 
    <% Html.EndForm();%>`

And finally, the controller method that’s going to process it all. Rather than taking in the standard id, it takes in a model object to which it will do all the Request.Form for you and hook the form values up to the object properties.

    [AcceptVerbs(HttpVerbs.Post)] 
    public ActionResult Save(AssaultItemEditModel item) 
    { 
         //do save 
         var assaultItem = new AssaultItem(item.Id) 
             { 
                 Description = item.Description,
                 Type = item.Type,
                 LoadValue = item.LoadValue 
             };

         Service.SaveAssaultItem(assaultItem);

         var message = "Item saved successfully.";

         return this.RedirectToAction(x =&gt; x.Index(message)); 
    }

Don’t mind my extra step on newing up an object with the id as a parameter, that’s due to the way I hooked up [Fluent nHibernate](http://fluentnhibernate.org/) at the start. Basically, to generate my maps from my domain objects, the id gets a private setter as convention. So, to get the right object to save, I had to set up the constructor to take an id argument. I cut some corners to get the demo app out the door. (John, you may hit me with, “Quicker does not equal better,” as soon as you read this.)

The other way around that is to not use my domain objects in my views, but that’s another discussion.

Under the hood where the magic happens, I haven’t dug too deep. But, I use this daily and it works swimmingly. You don’t even have to take in the model the view is bound to, just have the form fields match the model you’re taking in. I don’t recommend doing ad hoc model binding, in practice we set our edit model as a child of the view model.

I feel bad that I didn’t get this up on the screen, because it’s some fun stuff to show off.
