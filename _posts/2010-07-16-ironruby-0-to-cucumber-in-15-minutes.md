---
layout: post
title: IronRuby - 0 to Cucumber in 15 minutes
categories: Cucumber IronRuby Ruby
---
## IronRuby: 0 to Cucumber in 15 minutes

Once again, a 140 character (or less) “outburst” gets me in trouble with a follower and I end up with a blog post. This one is one I probably should  have written a while back. I’ve enjoyed working with IronRuby the last few months, so this little intro is long overdue.
[<img src="/images/posts/tw-ir-cuke-tweet.png" alt="Tim: From 0 to IronRuby all set up in less than 15 minutes. Preparing to cuke me some .Net. woot!" align="right" />](http://twitter.com/timwingfield/status/18517846272)


First things first, you’ll need to install [IronRuby](http://ironruby.net/). Head off to the [download](http://ironruby.codeplex.com/releases/view/25901) page, and click on your msi of choice and let the installer do its thing.

Since my goal here was to get cucumber ready to roll against some .Net assemblies, you’ll need to install a few gems. IronRuby comes with Ruby Gems already installed, so thankfully to install the ones you need you just need to type `igem install` a few times.

[<img alt="Jared: Sounds like someone needs to blog the steps needed to setup." src="/images/posts/jr-ir-cuke-tweet.png" align="left" />](http://twitter.com/jaredrichardson/status/18517907299)
“Wait, what? igem? WTF?” Yeah, that’s one of the IronRuby-isms, putting an i on the front of a couple of commands. If you’ve done a bit of Ruby, you’ll have a little muscle memory to retrain, but it’s a small hurdle. (You’ll also type `ir` instead of `ruby` to run a script and `iirb` instead of `irb` to get to irb.)

So, on with our gem installing…

    igem install rake

First install is rake. I’m not going to use it right away on the cucumber running, but I’ll use it at some point, I always do.

    igem install albacore

Like rake, I’m not going to use this one right away, but I’ve found it to be the one must have gem if you’re using rake with your .Net builds and test runners. It just makes you life that much easier.

    igem install rspec

I’m not starting out writing rspec in this example, but cucumber is going to use its matchers.

    igem install cucumber –-version “=0.6.4”

This is the one we’re after for this example. Be sure to add that version command on there because IronRuby isn’t quite ready for the latest version of Cucumber. But, 0.6.4 is going to get the job done for us.

    igem install iron-term-ansicolor

The first time you run cucumber, it’s going to advise you to install this gem to get color coding in the terminal window. Go ahead and do it now, and you skip that warning. (Or don’t, and check the message for yourself. ;) )

Now all you need is some features, some step definitions, and a dll to write it all against. As luck would have it, I have just that written up in a code sample that I just used at Codestock a couple weeks ago. (And also coming soon to an Ohio user group meeting near you…) Here’s the root of that project: [http://github.com/timwingfield/TestingSeaPound](http://github.com/timwingfield/TestingSeaPound)

The features directory there is where you’ll find my cucumber samples and the dll they are running against. Download it and give it a shot. Once you get it downloaded, open the command prompt in whatever directory contains the features directory (not the actual features directory) and type:

    cucumber features

Happy IronRubying!
