---
layout: post
title: TDD Starting to Sink In
categories: development TDD
---
## TDD Starting to Sink In

Back in late March, I [blogged about my issues getting going with TDD](/2008/03/30/tdd-growing-pains.html). At the time I was nearing the end of a project where I had attempted some unit testing, but had not done it up front. I was looking forward to a clean slate to get some more work on TDDing up my code.

That opportunity somewhat presented itself, though I was moving on to an established team, which presents its own challenges. However, this team, or a good portion of it, was practicing TDD. So, plenty of example code out there. Not only that, I ended up sitting about 3 feet from world renowned TDD zealot, Steve Harman. Steve is a great teacher, and only yelled at me a few times. (And I only cried the one time...)

That helped on the professional side of things, but even in my own hobby coding I started writing more and more tests before the code. I've been presenting on ASP.Net MVC at a few places recently, and the sample code I use there was written all TDD style. (And is presented test first.) Well, almost all of it...somebody wrote his repository wrong, and the updates didn't work so well. I have some refactoring to do.

So, here I am 3 months later, where do I stand on the points I brought up back in March?

1. I tend to wrestle a lot with when to layout some of the framework and when to just breakdown and write the tests.

This one became pretty easy when Steve introduced some BDD ([Behavior Driven Design/Development](http://en.wikipedia.org/wiki/Behavior_driven_development)) style grammar to our testing. This one shift in thinking opened up my ability to get the requirements into unit tests, and get them green quicker. In a nutshell, thinking along the lines of, "When X condition is present, then Y should happen," and naming the classes and test methods with that type of grammar took me well beyond wondering when to write the tests.

2. A recent project found our team working with a pile of generated tests.

Generated tests are a thing of the past. This is a non-issue at this point.

3. When to mock?

Again, a healthy dose of Steve helped here a lot. Also, [Rhino Mocks](http://www.ayende.com/projects/rhino-mocks/downloads.aspx) 3.5 was released with the [Arrange, Act, Assert syntax](http://ayende.com/Blog/archive/2008/05/16/Rhino-Mocks--Arrange-Act-Assert-Syntax.aspx), and that cleared up a lot in the mocking area. No more record and playback blocks, and lots of lambdas to stub out that which you want doing the dirty work.

The answer to the original question finally became clear: Get the hard stuff out of the way with mocks. Beyond that, get the stuff that you're not testing out of the way with mocks. The AAA syntax made that pretty easy.

4. Is this test trivial, or needed?

OK, I still have a bit of trouble here. Not as much as before, but occasionally I find myself writing a test, looking at it, and going, "Gee, I'm testing the setter of that property...that had BETTER work!"

5. I still have large holes in what I test.

Again, still having trouble here. Even with the good TDD practices in place at the most recent project, I found myself frustrated and writing the code and screen testing it rather than writing my unit tests up front. I did have a deadline that I was up against, but cutting the unit tests is never the right solution. I fell back to an old habit, one I've been working pretty diligently on breaking.

In the March blog entry, this referred to unit testing my javascript. Well, ending up on a Webforms project pretty much ended my worries about getting my javascript tested.

So, with those steps behind me, what do I want to focus on now? Well, I can still improve on numbers 4 and 5 above, but I think those two will be continuous improvements. I'm going to continue down the BDD-ish path. It's not pure BDD, but it got me over the hump, and I like the syntax. But overall, I'm just going to keep going at getting the tests written up front. Focus more on the red, green, refactor as much as I can. I'm seeing the benefits, just need to get those old habits kicked.

