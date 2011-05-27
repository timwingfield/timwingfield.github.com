---
layout: post
title: But WebForms did that FOR me.
categories: development ASP.Net-MVC
---
## "But WebForms did that FOR me."

While working with the model binder the other day, the statement in the title was made by one of the guys on my team. It’s not an unreasonable statement, but I think it spells out an important distinction between traditional ASP.Net WebForm development and using the new, shiny ASP.Net MVC framework.

The point in question was in posting an object after edit, the id didn’t automatically come through. The model binders do some magic under the hood, and it’s welcome magic in my opinion as I’ll gladly leave Request.Form back with Classic ASP. However, you still have to tell the model binder the whole story, it’s not done for you anymore. (Nor was it done for you before WebForms.)

Solution to our little problem: Stash the object id in a hidden form field. (Yes, I know, right click and view source and there’s my object id.) Once looked down upon in WebForms development…well, other than that one GIANT hidden form field called “ViewState”…the hidden field looks to be making a quiet comeback.

Basically, if you want the model binder to find all the bits to your object, you have to make it available when the page posts. So, it needs to be in the form somewhere.

Personally, I don’t see this as a step backwards, but I grew up in the salad days of request/response. Having to provide that info so you can get it back seems normal. The flip side is also true: if you don’t need it, you don’t have to add it.

The more I work with ASP.Net MVC, the more I fall in love with it.
