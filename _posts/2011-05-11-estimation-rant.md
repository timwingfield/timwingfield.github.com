---
layout: post
title: Estimation Rant
categories: agile lean estimation sizing
uuid: http://blog.timwingfield.com/2011/05/estimation-rant.html
---
## Estimation Rant

<img src="/images/posts/estimation_rant.png" alt="I feel an estimation rant coming on" align="right" />
Estimation is a bad word on dev teams. We have learned from many painful estimation debacles to the point we cringe when we hear the word, "Estimate." In many software endeavors estimating is a necessary practice, at least on some levels, to get the thumbs up to start writing software in the first place. But just because we have done estimating activities often, does not mean we are good at it.

_Disclaimer: I am discussing estimation in the context of delivery, not sales. Clients everywhere want to know when something will be done before they commit money to it, which is why many talented sales people drive fancy cars._

### Failing Into the Hours Trap

The very first failure of many estimating exercises is estimating your tasks, stories, and features in hours - or days or weeks or years. Any unit of time measurement is likely going to get you in trouble, but we will stick with hours for our example. Yes, hours fit neatly into a column in Microsoft project, but for estimating a development effort your setting yourself up for failure as soon as you choose hours as your unit of measure.

<img src="/images/posts/dages_estimation.jpg" alt="Ready! Aim! Estimate!" align="left" />

The first trap in using hours is we are all going to base that guesstimate on the 8 hour work day. If you commit to 8 hours, you are essentially saying that you will have that feature done in a day. Your manager is definitely hearing "one day" when you say 8 hours. If you could sit and code for 8 hours straight, maybe that estimate would be worthwhile. But how often do you get to code 8 straight hours? All kinds of things happen that derail that 8 hour day of uninterrupted coding. The stand up, other meetings, lunch, nature will inevitably call, and there's a better than average chance a Nerf war will break out in many team rooms.

The second trap of hours is they really only get used as a measurement when you go over your estimate. For example...

Let's take a developer on our team, we'll call him Jeff. In our estimation meeting, the team has determined that feature #1337 will take 16 hours to complete. Based on our previous trap we all just heard, "Two days." Jeff pulls feature #1337 off the board Monday morning and gets to work. Wednesday afternoon, he moves it to dev complete. Whoa, that feature just took 24 hours to complete! Come on, Jeff, you're 8 hours over the estimate? How will we ever make that time up?? We're on a deadline here!!

Sorry...all accusations are purely hypothetical.

The next Monday morning we're back at work, and our trusty developer Jeff looks on the board and sees feature #1355 on the board estimated at 16 hours. He pulls the card into the development queue and gets to work on it. At the end of the day he's done. 8 hours into his 16 hour feature he moves it to dev complete. Way to go Jeff!! You rock! Best developer ever!!

But hold on a second. Our rock star dev has missed his estimate by 50% in both cases. In one he's the villain and the other the hero? He goofed by 50% but thanks to "beating the hours" on the second feature that gets lost. In reality we should be asking Jeff why he missed each estimate. That will help us learn where we as a team missed and how we can apply that to future guesstimation exercises.

### The Cost of Estimation

During a lunch conversation at a past conference I listened to a gentleman tell us how he was contracted to do a 6 month estimation on what it would cost to build a certain piece of software. Two weeks into the contract, one that was paying him quite well, he went to his stakeholders and said, "The amount of money you are sinking into the estimation contract will never be returned to you. You will never get $1 back from it, how about I just start building the software and we'll see where we are in 5 and a half months?" They went for it, and he won the development contract 5 and a half months later.

The estimate means nothing to the actual delivery of the software. One of my former managers used to say, "The effort is the effort is the effort." The iron triangle of software is scope, timeline, and quality. We're allowed to fix any two of them, but the third has to be flexible. (It's scary how many times quality is the one that gets forced to flex.) Our estimate won't change any of the three points on the iron triangle.

### All Is Not Lost

Fear not, there are ways to get your software written without falling into estimation traps, and giving those outside the team a reasonable idea of when something will be delivered.

First up is story points. Story points are a representation of the [level of effort](http://blog.mountaingoatsoftware.com/its-effort-not-complexity) the team thinks it will take to complete a story. Story points can be anything. I have seen teams use numbers such as 1, 3, 5, and 8 as their points, and other teams will use t-shirt sizes such as S, M, L as points. One team I saw **REALLY** wanted to drive home the fact that story points are relative, so they went with duck, unicorn, and elephant as their sizes. Using any of those units of measurement illustrates that story points are used relative to each other rather than to a fixed value such as hours. Humans are very good at doing comparisons, so we don't know exactly how big a unicorn story is, but we know an elephant story is bigger.

Another way to step away from estimations is to move to a continuous flow system. Get yourself a Kanban board, get rid of iterations and iteration commitments, and start tracking the cycle time on the completed side of things. There are a few challenges with going this way, the first being that you will not have a reasonable idea of your cycle time until you have pulled a few stories through the system. Additionally sizing may still come into play because stories have this habit of never being exactly the same size. But, get through a few cycles, get some actual times on features from concept to completion, and you'll be handing your managers actual times from which they can plan future work. It may take a little time to get the data, but there isn't a manager in an IT department anywhere that wouldn't love to hear, "This story is sized as a small for our team and small features take us about 2 days to complete. Come back Wednesday, we should have it for you."

The last way to get rid of estimation is just to get rid of estimation. Like the story where the gentleman stopped researching on the estimation contract and just started writing code, just write the freakin' code! That could make for some difficult conversations at some point, but if your 4 person dev team is in a 2 hour estimation meeting every iteration, that's 8 hours you could have spent writing code towards a deliverable.

    </rant>
