---
Title: Estimation Rant Part Two
Author: Tim Wingfield
layout: post
categories: agile lean estimation sizing
---
## Estimation Rant Part Two

The [Estimation Rant](/2011/05/12/estimation-rant.html) opened the can of worms on estimation. This topic is always a good one on software teams and is sure to drive opinions and discussions around those opinions. Some of those opinions were surfacing in the comments of that post when Blogger decided to flake out. A whole conversation disappearing for a few days is a sure fire way to end said conversation. So why not pick it back up here.

I have estimated and sized work for both the purpose of sales and  for delivery - they are different exercises. The conversations take place with a different group of people, and the level of detail needed between a sales estimate and a delivery estimate are much different. A sales estimate should not be concerned with scope. Your client has a business problem that needs solved **AND** they need your help in solving it. Scope at a story point level - or worse, at an hours level - in a sales meeting is doing a disservice to the client and to the delivery team.

I’m sure a few people are chomping at the bit at that one, that sales shouldn’t be concerned with the scope of a project. That is until you realize the scope of a project will change. Repeat: The scope of a project **WILL** change. The delivery team is going to tear into the project and they’re going to learn more and more about it. They are going to learn that some concepts are smaller than they initially thought, just as they will learn that some concepts will be more complex than they thought. The scope is definitely going to change, and it will change constantly. When is the last time you built the project you started? Change happens all the time. [Embrace or get ulcers.](http://twitter.com/#!/aJimHolmes/status/80576009975496704) (That awesome one-liner courtesy of [Jared Richardson](http://twitter.com/#!/jaredrichardson).)

We have a number of tools available to us as agilists that should also help drive the sales process. The concept of a [minimal marketable feature](http://www.upstarthq.com/2010/04/introduction-to-minimum-marketable-features-mmf/) (or minimal viable product or minimal value feature, pick your phrase) which is the minimal amount of work that needs to be done to deliver value to your customer. Or the [value story](http://napkin.highgroove.com/articles/2011/01/20/a-day-in-the-life-of-agile-hands-on-workshop), where the business decides the value of a story in dollars prior to making it a project, then prioritizes the work to satisfy the value story. Both those concepts are going to support an iterative development process.

### Building Software

A couple of comments to the prior estimation rant brought up finishing a basement. This steps into one of my biggest pet peeves about our industry: We build software, we’re not basement finishers. We don’t build houses. We don’t build bridges. We don’t build skyscrapers. We create software. Software is soft, it is mutable, and built correctly it can be changed at a low cost. The SOLID principles are solid as an acronym only because each and every principle is concerned with lowering the cost of change. They are about **KEEPING** software soft. The practice of building software is a knowledge creating process. It’s not a repetition of the same process with the same materials on a different job site.

In the context of my estimation rant, the number of unknowns in building a software application compared to the unknowns in framing out a basement wall are what leads to the waste of estimations. Take a small feature and develop it. Don’t estimate it, code it. At the end of that feature you’ll have learned more about the system, you’ll have created some value by delivering the feature, and you’ll have an actual time it took to build the feature.

The size of the East River didn’t change while they were building the Brooklyn Bridge. The size and shape of my basement didn’t change as we finished it. But the scope and size of my project changed **TODAY** as we found a better way to display data to our users. And it will likely change again tomorrow.

### Are we agile or not?

The traditional way to start bidding was with,  “I have this idea and this much money; I want it done by Tuesday? Can you do that?” Teams would clamor for the business, put a bid in to win the project, get the business, then spend weeks in a detailed contract negotiation detailing what the deliverables would be. When development started and the actual scope got out of hand, they would change control the hell out of it to keep it profitable.

But if we move to an agile bidding process, we can start the conversation with, “I have this idea and this much money, how much of my idea can I get?” Then we can prioritize some features, possibly very large features, and get to work on it. Line three of the [agile manifesto](http://agilemanifesto.org/): Customer collaboration over contract negotiation. Which is not to say we don’t enter into a contract, we most certainly will. However the conversation in determining what can be delivered to satisfy the customer's business need should lead to that contract, not be hindered by the contract. Your contract is there to protect both parties, but it should not be written down to the detail level that allows one or both parties to hide behind it in order to “win” the engagement.

Obviously trust is going to be a big factor here, as you just can’t say, “We’ll do it all agile like! Trust me!” Trust will need to be built, and the easiest way to build it is to be open and honest with all your communication. Be professional. Start small and build it from there. If there is no trust between you and your client there is no contract out there that will force it to happen.

A friend and colleague was working on a project recently where they are doing that incremental trust building, introducing agile, and having their ups and downs. In one case they proposed an approach to solving one of the client’s problems, and client replied with: _“Your competitors have proposed a solution, and they already know and have priced out what they will need to build, whereas you just proposed an approach.”_

That is a pretty straightforward response, and one that fits directly into traditional project bidding. So my friend’s reply was definitely not traditional: _“Nobody knows exactly what you need built; not you, not them, not us. The difference here isn’t that they have a solution, it’s that we are not lying to you to try to win your business.”_ Open and honest communication.

### Last Word on Estimation

I was in attendance at Agile Dev Practices West recently and got to see [Linda Rising’s](http://lindarising.org/) [keynote address “Deceptions and Estimating: How We Fool Ourselves.”](http://www.sqe.com/AgileDevPracticesWest/Keynotes/Default.aspx#tk1) Linda had many studies and examples of how we as humans are overly optimistic at most things in life: How we drive, what we eat, and how we estimate software. We have learned that we are so bad at estimating software that we will spend extra time on the estimation in order to get it as accurate as possible, only to fail at it again. 

Why do we keep spending money on an estimation that is wrong? Sometimes wildly wrong? Doesn’t it make more sense to spend money on building it?
