---
layout: post
title: IronRuby - Rake, Albacore, and you
categories: IronRuby Albacore Cucumber nUnit RSpec
---
## IronRuby: Rake, Albacore, and you

In my post about setting up to run [Cucumber with IronRuby](/2010/07/16/ironruby-0-to-cucumber-in-15-minutes.html), I included steps to install [Rake](http://rake.rubyforge.org/) and [Albacore](http://albacorebuild.net/), but didn’t use them. In this post, we’ll put them to use.

<img src="/images/posts/rake.jpg" align="right" alt="rake" />
Using Rake in .Net isn’t really a new idea, and a [number](http://codebetter.com/blogs/david_laribee/archive/2008/08/25/omg-rake.aspx) of [people](http://stevenharman.net/blog/archive/2009/05/29/being-lazy-with-rake.aspx) have been [using](http://www.codethinked.com/post/2010/04/26/Say-Goodbye-to-NAnt-and-MSBuild-With-IronRuby.aspx) it for a while. I’ve used rake to compile and run the tests on all my .Net projects for at least the last year. Before Albacore came along to make my Rake tasks easier, I was copying the set-up from the folks at [Fluent nHibernate](http://github.com/jagregory/fluent-nhibernate/blob/master/RakeFile). (FNH has used rake to build as far back as I can remember it existing and is now utilizing Albacore as well.) Now with IronRuby in the mix, rake is going to take on even more fun in your .Net projects.

For my example I’m again going to use my [TestingSeaPound](http://github.com/timwingfield/TestingSeaPound) project, and specifically the rake file I’m using in that project. [Pop it open](http://github.com/timwingfield/TestingSeaPound/blob/master/rakefile) real quick, and we’ll look through it.

At the top, you’ll see the standard Ruby require statements. In this file we’re including rake, the task library for RSpec, Cucumber, the task library for Cucumber, and Albacore.

Following the required libraries are a number of tasks that are combining the tasks that are defined later in the file. This is a way keep your rake file nice and dry. Define each task as needed, combine them in a call such as `task :spec => [:msbuild, :rspec]` to reuse them in different situations. From the command line in the directory where this rake file lives, if I enter `rake spec` it’s going to build the code then run RSpec

The only task in this list to take note of is the `:default` task. That’s the task that will run if you’re at the command prompt and just enter the command `rake`.

### MSBuild

Skip down to the line that includes msbuild do |msb|. That’s our first task definition, and in this case we’re using the Albacore library. The top line of that task that includes the path_to_command is needed to build a .Net 4.0 project. I believe a fix is in the works, and may already be in place, but when I set up this file this was the way to call the .Net 4.0 compiler.

The next two lines, properties and targets, should look pretty familiar to anybody who has set up a .Net build in the past using MSBuild or Nant. Here we’re just saying what configuration we want to compile in, and what our target build is. Following that I’m setting the verbosity to quiet to keep the command line output fairly small.

The last line should be fairly obvious, it’s the path the solution file. Since MSBuild is very good at picking up a solution file and building it, why fight it? Pass the solution to MSBuild and let it do its thing.

### nUnit

The next task down is our nUnit test runner. This is again an Albacore task, and it’s just pointing the test assemblies at the nUnit console app.

These two tasks are the only Albacore tasks in the file, so here’s as good a place as any to let you know the magic going on under the covers with Albacore. It is in essence building the correct command line arguments for MSBuild and nUnit and then shelling out to run them. Now, there’s more work going on than just that, but that’s the bulk of if. Albacore is giving us a nice DSL to write .Net build tasks. I’m only using two, there are a lot more available.

One important note: to this point our rake file hasn’t _required_ IronRuby. You can use Albacore to build your project and run .Net based testing suites with MRI, IronRuby isn’t a requirement. I know as a .Netter that may seem odd, but we’re really not leveraging the Iron part of IronRuby.

Yet…

### RSpec

The next two tasks are both RSpec tasks, and they’re running rspec against our .Net app. The first task is the default runner where it outputs a period for each passing test, the second will output the describe blocks and spec names.

**_NOW_** we need IronRuby. Not so much for the rake task, but because RSpec isn’t going to be able to test our dlls without the Iron added to our Ruby.

### Cucumber

The final two tasks are Cucumber tasks. The first outputs the standard cucumber output, with each feature and specification output in their full glory – minus line numbers because I turned those off with the –-no-source option. The second task outputs the cucumber specs very much like nUnit and RSpec do, with a period for each passing test.

Once again we need IronRuby. Since I’m using the Ruby version of Cucumber in this case, we need to add the Iron to get it to reach into our dlls and do its magic.

That’s all for the tasks required to build and run the tests for this sample application. If you pull down the code and go to the root of the project and enter `rake all` at a command prompt, you’ll build it and run each suite of tests in order. Give it a try.
