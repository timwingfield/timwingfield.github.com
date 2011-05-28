---
layout: post
title: ASP.Net MVC - A Step in the Right Direction
categories: ASP.Net-MVC MVC development
---
## ASP.Net MVC: A Step in the Right Direction

A link to Doug Copestake’s article [“ASP.Net MVP: A Step Backwards?”](http://www.thecurlybracket.com/?p=164) was forwarded to me, and it made some short rounds on twitter. I read it and had a comment underway and thought, “This is WAY to big for a comment, let’s blog it!” So here we are.

Off the top, I’d like to give a tip of the hat to Doug for stepping outside his day to day and taking a look at ASP.Net MVC. It’s very easy to hide behind FUD and just blow off something different. Additionally, his initial findings are pretty much on par with most other folks happy with WebForms who take their first look at MVC.

The MVC framework definitely provides simplicity and separation of concerns to web development. It allows you to only write the code you need to write to get the job done, and it allows you to work with the framework. Views become very small and very specialized, controller actions mature to be very thin, and it’s all easily testable.

This has made my work with the MVC framework extremely successful. Since everything is easily testable, as we refactor the code to clean it up or add new functionality, it all flows very easily.

Control reuse comes from veteran WebForms developers quite often. But if we again point at simplicity, how many of those drag and drop controls were written to cover more functionality than you need? You drag a grid control out and use 15% of it’s power because its made for everyone. Yes, you can write your own application controls to do exactly what you want, but you can do that in MVC, too.

Another point to control reuse is the leveraging of more javascript frameworks to do many of the things that the WebForm control suites do. In jQuery UI alone, you’ll get tabs, accordion panels, sliders and other UI elements, all with out that “server side” part that is so prevalent in WebForms. The win there is in more than just lighter weight controls, you gain a much better user experience. (And who doesn’t like happy users?)

The spaghetti code point Doug makes is quite valid, though I think that’s not a factor of one framework or the other as much as it is the person writing the code. The [Glen Vanderburg](http://www.vanderburg.org/Blog) quote, “A bad developer will move heaven and Earth to do the wrong thing,” applies to all languages and frameworks. The person with the keyboard under their fingers is responsible for keeping their code clean, not the framework developers, but I digress.

Spaghetti code in the views is a big sign that you’ve done something wrong. Even before moving to [Spark](http://www.sparkviewengine.com/), if you see lots of server instructions in your views, it’s time to stop and think, “What can I do differently here?” Same can be said of your controllers. If you’re used to writing a 50 line page load method in WebForms, turning similar code into 50 line controller actions is a step in the wrong direction. I guess the main point here is instead of relying/hoping for the framework to do the work for you, the onus is now squarely on the shoulders of the developer to keep his or her code concise.

Doug’s last point is very true, though: if you have a lot invested in WebForms in your current situation, there’s no real reason to switch away from it. Switching for the sake of switching to anything usually isn’t a good move.

That said, you can easily run WebForms and MVC in the same web application. If you have a little something to add to the project that can stand on its own, I’d say a look at MVC is in order.

This definitely would have been too long of a comment… :)
