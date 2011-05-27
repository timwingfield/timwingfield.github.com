---
layout: post
title: Tech Night - Getting Started with MVC
categories: development speaking MVC ASP.Net-MVC
---
## Tech Night - Getting Started with MVC

First of all, thanks to all those who attended TechNight this past week at QSI HQ. That was by far the largest crowd I'd seen gather for TechNight, much bigger than the 10 people that came in September when I presented on ASP.Net AJAX. With Quick having the much larger training center now, I hope this trend continues.

### The Snag

During post-presentation discussions, I finally arrived at why the test failed. Short version: I'm an idiot.

Long version: I went with the whole TDD approach to the presentation to show how MVC was more testable. It is a great way to show some of the advantages of MVC. It is if you continue to run those tests as you refactor your code.

What I did was stop at red, green, refactor. I didn't try for more green following an additional refactoring. I had written and passed my product controller tests, where the big test failure happened in the presentation, before I had added my model code to the product controller. That's a pretty big change, and clearly the tests caught that change...in front of an audience, rather than in the comfort of my own home.

So, my protests of, "These passed at home!" were correct, because I only ran them once. Like I said, idiocy.

In the end we got it working for purposes of the demo, and I owe Mel, Steve, Steve, Kris and many others who shouted advice a big thanks for helping me over the hurdle. However, the demo ended up testing what I didn't need or want to test: That LINQ was doing what it said. I had wanted to add one more test prior to the demo that hit an in memory collection of products, that would have solved my problem with the connection string and been a much better test of the controller code.
