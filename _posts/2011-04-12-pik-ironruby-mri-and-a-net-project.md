---
layout: post
title: pik, IronRuby, MRI, and a .Net Project
categories: ASP.Net-MVC Cucumber IronRuby Ruby
---
## pik, IronRuby, MRI, and a .Net Project

On a recent ASP.Net MVC project I was leveraging IronRuby and Cucumber to get some BDD specs in place to drive development. Though this post isn't about the benefits of BDD, it was very easy to get the specs worked out with my Product Owner, and the demos went really quickly. For the most part, I was using IronRuby to run functional tests at the controller level.

Then we decided to add on some GUI tests. With Ruby and Cucumber already in place, we decided to give watir a try. Except once we went on to using watir, IronRuby was no longer needed to test the website. We could instead use MRI 1.9.2 as our interpreter and get a little more speed out of our watir tests, and leverage the latest version Cucumber.

Since we're doing our development in Windows we don't have the luxury of RVM, but pik is a great solution to switching Ruby interpreters on Windows. During development, a few pik switch statements keeps all our cucumber tests in sync with either our IronRuby testing or our watir testing. However, if we wanted to run them all at once I had to write a little batch file to handle it. (I'm a dev, I'm lazy, I just want to type one line in the command prompt and have it all kick off...)

After knocking the rust off my batch file fu, here is the contents of that batch file...

    @echo off
    @call pik sw 100
    @call rake
    @call pik sw 192
    @call rake watir

Here's what's happening in our little five line helper file. First line just doesn't echo your commands back out to the command prompt. After that we call pik sw 100, which is pik switch to IronRuby 1.0.0. Then our default rake task is called, which builds the project, runs the unit test suite (in nUnit in this case), then run the IronRuby cucumber tests. pik sw 192 is switching to Ruby 1.9.2, then calling rake watir just runs our watir tests against the already built website. Pretty straightforward.

Now that was only for our dev machines in order to do one line build test, test, test during development. Our CI server was much easier to configure.

We were using TeamCity as our CI environment when we added watir to the mix, but the batch file wasn't needed as TC allows for different build tasks to use rake and specify which interpreter to use. So it was as easy as add an IronRuby build task call the default rake task, then create another rake build task and call the watir task in the rake file. We have since switched from TeamCity to Jenkins, but the set up with a build task per interpreter is identical.

(Don't have pik installed and you're a Windows using, Ruby loving programmer? [Ben Hall's post](http://bit.ly/gHB7d0) on getting pik installed and running is the best reference I've found.)
