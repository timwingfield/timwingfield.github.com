---
layout: post
title: Is Code Coverage Worth Bragging About?
categories: development testing
---
## Is Code Coverage Worth Bragging About?

I'm a hockey fan, have been for a while. In being a hockey fan, I've had a number of statistical discussions around the sport. Second only to baseball fans in statsville, hockey fans love their numbers. One major discussion took place around shots on goal. That semi-subjective stat that tells a team how many times the goalie got between them and a goal. I've seen teams put 40 shots on net and lose to a team that got 18 because 3 of the 18 went in and only 1 of the 40. After the game, you lost, but hey...you put 40 shots on that guy! You certainly didn't lose for a lack of trying.

So, over in the software world, I'm now wondering if Code Coverage is our shots on goal stat. You get over beers and start talking with peers and hear...

Bob: "I've got 40% code coverage!"

Terry: "Bah, that's nothing, we hit 55% this afternoon!"

James: "You both suck, we've got 70% coverage and are almost through UAT!"

Here's what's missing in that discussion...Bob is 60% uncovered, Terry is 45% uncovered, and James has 30% of his code waiting to spring something on him in the next few days of UAT. In essence, they've each got a number of shots on goal, but how many are in the net? Are we focused on the wrong side of the equation?

The goal of 100% code coverage is a tough one, unless you're [Joe O'Brien](http://objo.com). (See: Testing Mandatory, CodeMash 08) In my life in ASP.Net, getting 1% coverage on a code behind file would be worth a round of beers.

But, are we focused on the wrong goal? Clearly, increasing your code coverage is decreasing uncovered code. But, if your goal is 75% coverage and you reach that goal, do you stop? Maybe shifting our focus to code uncoverage will close that gap.

Don't be happy with those 40 shots on goal...
