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

Contrast that with other conversations with management and leadership types who don't
know what cucumber is, but as you explain it you can see the words scrolling across
their foreheads, "If we use this, I can lay off half my QA people! Cost savings!!"

Now, I can't totally discount both points, there is a little merit of truth to each one
of them. In the first case, a QA group that knows and understands Cucumber can be a
great asset to the long term future of your product. Additionally, once Cucumber is in
place it will free up some QA departments from doing repetitive manual tests and allow
them to focus on more exploratory testing. 

However, if you consider Cucumber to be only a QA tool, you are missing a good portion
of what this and other ATDD/BDD frameworks, can provide.

###Collaboration

The biggest benefit to employing Cucumber, or any BDD framework, is that it tears down a
lot of the communication walls to which we have become accustomed. Specifically the
Gherkin syntax of `Given/When/Then` helps bring down those walls by writing acceptance
criteria in a plain text format that everybody can agree on.

From the business's standpoint, finally being able to communicate to the development and
QA teams in a clear manner has to be beyond welcome. Being able to send something to the
dev team that says:

    Given the customer has an item in their shopping cart
    When the click the checkout button
    Then I will have more money in my bank account

No more reams of documentation around a simple feature with wireframes, UML diagrams,
feature documents, and other items buried in a wiki somewhere that gets ignored. Plain
text is easy, and in my experience the easier something is to use, the better you chance
you have of it getting used.
