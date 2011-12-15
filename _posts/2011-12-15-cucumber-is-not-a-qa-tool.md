---
Title: Cucumber Is Not a QA Tool
Author: Tim Wingfield
layout: post
categories: agile lean cucumber testing
---
##Cucumber Is Not a QA Tool

In my recent travels, and they have been plenty, I have come across some interesting
views about Cucumber.

In one conversation someone was looking for "QA people with Cucumber experience." I
thought that was pretty cool, they want some testing folks familiar with a rather
popular test framework. Then came the second sentence, "I really don't know what
cucumber does, but I know that QA people need to do it." (Yes, this person was a
recruiter, if you couldn't tell by now.)

Contrast that with conversations with management and leadership types who don't
know what cucumber is, but as you explain it you can see the words scrolling across
their foreheads, "If we use this, I can lay off half my QA people! Cost savings!!"

Now, I can not totally discount both points, there is a little merit of truth in each one
of them. In the first case, a QA group that knows and understands Cucumber can be a
great asset to your product team and the long term quality of your product. Additionally, once Cucumber is in place it will free up some QA departments from doing repetitive manual tests and allow them to focus on more exploratory testing. 

However, if you consider Cucumber to be only a QA tool, you are missing a good portion
of what this and other Acceptance Test Driven Development (ATDD) or Behavior Driven
Development (BDD) frameworks can provide.

_Note: From this point forward I will use BDD in the discussion. BDD and ATDD are very
closely related, almost indistinguishable in practice. I learned the phrase BDD first,
so I tend to stick with that. And for writing purposes, it is one character shorter,
thus promoting my natural laziness._

###Collaboration

The biggest benefit to employing Cucumber, or any BDD framework, is that it tears down a
lot of the communication walls to which we have become accustomed. Specifically the
Gherkin syntax of `Given/When/Then` helps bring down those walls by writing acceptance
criteria in a plain text format that everybody can agree on.

From the business's standpoint, finally being able to communicate to the development and
QA teams in a clear manner has to be beyond welcome. Being able to work with multiple
team members and arrive at something for the delivery team that says:

    Given the customer has an item in their shopping cart
    When the click the checkout button
    Then I will have more money in my bank account

No more reams of documentation around a simple feature with wire frames, UML diagrams,
feature documents, and other items buried in a wiki somewhere that gets ignored. Plain
text is easy, and in my experience the easier something is to use, the better chance
you have of it getting used.

Now from the QA person's standpoint, we have actual acceptance criteria that let us know
if a feature is complete or not. No more vague language that allows room for
interpretation where I can inadvertently add more functionality to a feature because
it is what I think the user might want someday. Maybe.

Finally from the developer's standpoint we have features with an end point and a better
description than, "Customer checkout feature." And not only do we have more clear,
concise feature descriptions, when we are done writing code for the features we have a set of
tests that will execute against the plain text features.

###Build What We Want

Cucumber benefits all aspects of the business, but possibly its greatest benefit is that
it allows us to easily agree to what "done" means for any given feature. The definition
of done for a feature won't change over the life of the project, or if it does change we
will have a broken Cucumber spec to alert us that we have changed our mind somewhere.
But by having that agreement of "done" in place up front it frees up the developers and
testers to focus on specifics of implementation and verification of the feature without
ambiguity.

Developers of many languages keep a set of unit tests handy that will break if they
make an unexpected change to some existing code. It may or may not be an intentional break, but the point is they have a safety net to catch a logic change. A suite of Cucumber tests has that same watchful eye over your application as a whole, rather than just at the class or method level. If the business changes how a feature operates and a cucumber test goes red, then the collaboration can kick back in across the whole team and the team can decide how to handle the original intent of the feature with this new feature request.

In short, we have a living record of what "done" has meant to every feature we have
developed over the life of the project. By executing tests against those acceptance
criteria, we also have a constant check that "done" for existing features remains done.

###Cucumber Helps With Quality

So while I don't think Cucumber is a QA specific tool, it helps with overall product
quality. By providing a good place for collaboration and by helping the team define
"done" early in the feature life cycle, then quality has become a first class citizen to
your team. Quality is a whole team goal, not just members of the QA team. (By
definition, people on the QA team *assure* quality, they don't build it.) 

If you are not using Cucumber or another BDD framework, I would highly recommend
looking into using one. However, look into those tools for the benefits they can bring
your whole team not simply as a QA tool. And while they will help alleviate some manual
work for the QA folks on your team, Cucumber is no replacement for a human being who can
dive into the application in ways you never thought of when laying out the acceptance
criteria.

After all who would you rather have poking around your app looking for things to go
wrong?

Your QA people?

Or your users?
