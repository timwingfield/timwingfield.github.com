---
layout: post
title: Why Not Add Some Ruby?
categories: IronRuby Ruby
---
## Why Not Add Some Ruby?

If twitter is good for one thing it’s starting debates amongst your friends. Today didn’t disappoint as [Mike](http://twitter.com/mikelikesbikes) [started us off with](http://twitter.com/mikelikesbikes/status/20327495866): “things i miss from rails while i'm doing java: rails.”

It started in the productivity trap, which is going to be subjective to the developer doing the work, so it’s a tough one to measure. Can I do some things faster in Ruby than I can C#? Yes, but the inverse is still true.

One point I need to make is I’ve seen a few of these discussions and often they become Rails v. C#/.Net, which isn’t really a fair comparison because Rails is a web framework. To go apples to  apples, you need to compare Rails to ASP.Net MVC, not .Net in general. You wouldn’t compare WebForms or WPF to Ruby or Python, would you? (You shouldn’t compare WebForms to much of anything…but I digress.)

So, Jon asked a pretty valid question: Why don’t more people switch? Since I come from a .Net background, I’ve really only seen this debated as it pertains to .Net.

For a number of the arguments around the IDE, Intellisense, Static v. Dynamic typing, there are plenty of other blogs that have covered this, here’s a recent one I really liked: [Ruby is Scary](http://devlicio.us/blogs/casey/archive/2010/07/31/ruby-is-scary.aspx).

For my quick entry here, I’ll say this…I can have VIM or TextMate open and have a couple tests written before the VisualStudio splash screen has closed. Also, those two tools have yet to throw an “Out of Memory” exception on me, can’t say the same for Studio.

And I don’t really miss intellisense.

On with the show…

On the heels of Jon’s question [Bill Sempf](http://twitter.com/sempf) jumped in. As a bystander, Bill was very much representing the average .Net dude, and the arguments I’ve heard from the average .Net dude. (Bill has looked into Ruby, we’ve paired writing Ruby. That’s not really the point here, though.)

### Ruby, the Average Dev, and the Complex System

> @JonKruger: That's not my problem. I just don't think that 80% of the dev teams out there can handle coding in Ruby. ([link](http://twitter.com/sempf/status/20329674218))

That was Bill’s entry to the discussion, and I’m not sure I can disagree with him. However, I’m going to be snobbish and self centered and say I want to work with the 20%. If you’re in the 80% and can’t code Ruby…or Python, or F#, or any other language you have to learn…I don’t want to work with you. You can stay in “The Enterprise.”

> @JonKruger: My point is those stories are told by top-tier devs, and not everyone is one of those. ([link](http://twitter.com/sempf/status/20335437396))

Again, tough to disagree with Bill’s assertion here. Not everybody is a rock star, and that’s cool. If you’re a budding rock star, you’ll be able to write some effective Ruby code.

In between those tweets were a few others, mainly around supporting complex systems using Ruby. Personally, I haven’t written a large scale application in Ruby, so I can’t lean on any experience here in writing the typical central Ohio “claims app” in Ruby.

What I have done with it has worked well. So my first counter to Bill’s argument on the complex systems: Use it where it fits. Ruby brings a great set of DSLs to the table for testing, web frameworks, and testing. Yeah, said it twice. Year one of [Codemash](http://codemash.org/) (Jan of ‘07) I listened to Neal Ford talk about DSLs to help write your applications and Polyglot programming. Using Ruby to support your app – to write build scripts, tests, POC web sites – falls right in on the polyglot thing.

On the testing side, I’d much rather read a batch of RSpec tests than a batch of nUnit tests. Cucumber is already helping my current team get through some testing issues. Let me repeat that: I’m using Cucumber in a .Net environment **RIGHT NOW** to help the team get better test coverage on their application.

### Learning a New Language

> @JonKruger: There is a difference between learning the language, and being productive in it. ([link](http://twitter.com/sempf/status/20335549836))

I’m in total agreement with Bill here. Which is why I’m such a big fan of the incremental approach to using Ruby on your projects.

Great place to start: use Rake as your build script. I’ve done this for a couple years now, it’s a great way to dip your toe into Ruby, get comfortable with the language and a few of its concepts without really getting in on your production code. On the .Net side, use Albacore with Rake and you’ll have a build script in no time.

Next up you can start writing some tests in it. That’s a pretty good way to pick up a new language, anyway. And with the nice testing tools with Ruby, you can learn a new language and ease some testing pain.

But, the main point here, don’t be afraid of picking up a new language. How many do you know already? If you’re a web developer, you probably already know Javascript, CSS, HTML, C# (or some back end language), a little SQL, and a healthy dash of XML. Picking up another one isn’t going to be too difficult.

### Essence v. Ceremony

I first heard this from Neal Ford, possibly at eRubyCon a couple years back. But, Stuart Holloway [had a great blog post about it](http://thinkrelevance.com/blog/2008/04/01/ending-legacy-code-in-our-lifetime.html) prior to when I heard Neal speak.

To me (and many others), Ruby gets to the essence of what you’re after quickly. I find myself working within it’s idioms easily, not fighting them constantly with adapter patterns, dependency injection, and ORMs. I find that my tests flow naturally from the various testing tools I use in Ruby, and the code that makes those tests pass benefits from that.

So, to Bill’s point, maybe Ruby isn’t ready to have average devs write big, complex, “enterprise” systems in it. But, it is ready to support what you’re writing today. Right now. Why not give it a try?

Unless you’re afraid of learning…
