---
layout: post
title: ASP.Net MVC v. WebForms
categories: ASP.Net-MVC MVC development development-practices
---
## ASP.Net MVC v. WebForms

This question seems to come up a lot in discussions around these two ASP.Net frameworks. Just this past weekend in Cincy at the MVC Firestarter, it came up a number of times.

So, on the way to work this morning, I was listening to [Hanselminutes 184](http://www.hanselminutes.com/default.aspx?showID=202), and the question was FINALLY given an answer by Scott Hunter.

> _If you care about separation of concerns, testability and tight control of your markup you should go with MVC. If you’re an enterprise developer and just want to get something out there quickly then use WebForms._

That’s paraphrased, I may have gotten the MVC reasons in a different order, but that was the point made.

Scary that “Just get it done,” is the main reason to use WebForms. I’ll stick with my “slow” TDD and long term maintainability in MVC and steer clear of WebForms where DDD apparently stands for Drag, Drop, Deploy.
