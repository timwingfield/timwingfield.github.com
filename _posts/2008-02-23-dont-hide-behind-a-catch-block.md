---
layout: post
title: Don't Hide Behind a Catch Block
category: development
---
## Don't Hide Behind a Catch Block

"Pragmatic Programmer tip #32: Crash Early."

I've been recently tasked with some refactoring items. Like any project that's longer than 8 weeks, you'll dig into some code and find yourself going, "What was I thinking with THIS?" Or, if the project's a bit longer, you wonder if you came up with this gem (and no, not a Ruby gem) or if somebody else on the team left this odor in the code.

The code smell of this particular blog post is the abuse of the try/catch block. I've stumbled across a few uses of the try/catch programatically, or worse, using an empty catch block to hide an issue you're not sure how to deal with.

Right off the top will go with the empty catch block. I encountered a few of these while refactoring, and had to wonder why we were hiding behind the empty catch block. Crash early, but when you crash sweep that under the rug and move on? That's not good. If you need a catch block, then isn't there something you should be catching? Take the following for an example:

[Image lost to time and the Internet...]

That's a pretty simple little conversion function, with the dreaded empty catch block in there. It's there not because of the TryParse, which is going to give you a false if it fails its own try, but because applying ToString to a null object is going to throw an object error. Rather than the empty catch, why not a null check on o? Then you know what you're dealing with rather than not caring and returning 0 for anything you're not expecting. To me, this is a classic garbage in, garbage out scenario. You pass in a null or an object that can't be converted to a an int and you get a 0.

Next up was a bit of sheer genius, and throwing my hands up when dealing with nHibernate. Rather than find out what was going on, I resorted to using a try/catch procedurally to handle the issue. Here's a bit of code that shows my brilliant solution:

[Image lost to time and the Internet...]

The issue there turned out to be that we were [using the load method from nHibernate rather than the get](http://toddkaufman.blogspot.com/2008/02/failing-to-fail-early.html), so I didn't have null object to check. I had an actual proxy object full of null properties. My solution, duck behind the catch block and make it bend to my will. If the load found something, the id check would pass and I'm doing an update. If the resulting object error from the property check threw, then I'm dealing with a new object, time for an insert.

In this case my ignorance of nHibernate's dealing with objects was the problem, but ignorance is no excuse. Using the try/catch in this manner was a hack with Paul Bunyan's ax. It got me moving foward, but was a bad solution.

The final empty catch falls in the same lines, where ignorance of what was available to us wasn't found until much later. This empty catch block example was saving us from a null reference error in a nullable data type in a data bind method.

[Image lost to time and the Internet...]

Getting rid of this empty catch may have been the easiest of the three, because nullable data types carry a "HasValue" property that tells you, well, if they have a value. The refactored code looked like:

[Image lost to time and the Internet...]

Using the HasValue property, we can refactor this one down to the always elegant ternary operator. We know what value we have or don't have and can cleanly bind our data to what's in this case a grid column.

If you're going to fail early, don't hide the failure. Figure out what it is and write the correct code for it. The try/catch is there to help you handle exceptions, not to hide them and move on.

