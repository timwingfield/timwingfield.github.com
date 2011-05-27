---
layout: post
title: I forgot what the M in MVC was for
categories: ASP.Net-MVC MVC development Rails Ruby
---
## I forgot what the M in MVC was for

What brought me to this conclusion was my reading up on a little Rails. I finally took the dive. I’ve been avoiding Rails for a while in favor of just learning Ruby. [Steve](http://twitter.com/stevehorn) loaned me [“Rails for .Net Developers,”](http://www.pragprog.com/titles/cerailn/rails-for-net-developers) and the research was underway in earnest.

On page 89, the light bulb went off. But not for Rails so much as for how I’m writing my ASP.Net MVC apps. Here’s the bit that got me:

* Models are the classes that represent your business domain and that are responsible for communicating with your data. In Rails, this means the tables in your database. 
* Views represent your presentation layer, for example, HTML and JavaScript. 
* Controllers are responsible for connecting the models and views and managing the flow of the application. 
![I'm doing it completely wrong](/images/posts/mvc-wrong.png "I'm doing it completely wrong")

That reads pretty straightforward to me. Hell, I’ve stood in front of groups of devs on more than one occasion and said, “Views are what gets rendered, controllers marry up the views with anything they need from the model, and **the model is everything that’s not a view or a controller.**”

So, what’s been going wrong? I’ve been putting way too much business logic in my controllers.

The structure of most of the MVC apps I’ve worked with is a typical .Net program structure. We’ve got a core where our business domain lives, and some type of ORM set up to talk to the database. From there, we expose that domain up to the UI through some simple domain services.

The issue comes when I consume those services. I’m using my controller actions to marry all that up and present it to the UI. I think my “excuse” to this point has been that I have two models: My domain model, which I’m accessing through my domain services, and my presentation model, which lives in the Models directory in the ASP.Net MVC structure. My controllers have to care about two places to get their information to provide to the views. At the least I’m violating the pattern and at worst I’m likely repeating myself somewhere and creating a future maintenance issue.

I think I can see where this happened, too. Think back to the Bad Old Days of dealing with Web Forms, and the cubby code behinds that came with it. In order to avoid the 197 line PageLoad method, I would have a lot of little one-off methods scattered about the code behind file. Switch over to MVC, and it seemed perfectly normal to have a similar structure. Alarms should have gone off when I had 5 classes in the Models directory but 18 methods in one controller class.

But wait, there’s more!

While perusing some code on my current project, I came across the [NonAction] attribute decorating a couple of controller actions. Re-reading that…I had NonAction decorating Actions. That has a certain “Jumbo-Shrimp” feel to it, doesn’t it? I suppose the non-action could fall under “managing the flow of the application” from above, but I’m thinking any non-actions might need to be refactored into the model.

Moving forward on my MVC apps – of any flavor, Ruby or .Net – I think I’ll move to a much thinner controller model in favor of loading up the model with business logic. Though I thought I knew the pattern fairly well, I didn’t practice what I preached.
