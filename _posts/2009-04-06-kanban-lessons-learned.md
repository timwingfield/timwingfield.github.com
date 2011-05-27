---
layout: post
title: Kanban Lessons Learned
categories: development development-practices kanban
---
## Kanban Lessons Learned

After seeing success with Kanban in a production support environment ([part 1](/2008/11/16/kanban-o-rama-part-1.html), [part 2](/2008/11/19/kanban-o-rama-part-2.html)), we decided to give it a try in a new development situation. This project was a mix of new development and working with an inherited code base to implement some existing features differently.

Because of this situation, we ended up with a mixed bag of features. At the onset, we decided to break these features out into tasks, and we would track both across our Kanban board, as shown here with a snapshot of our Work In Progress section.
![Project Kanban Board](/images/posts/tl-kanban-board.jpg)

Features were broken into tasks and grouped together in the backlog. Once a feature went into WIP, it's tasks moved below into the Task Breakout section and were worked there. Once all tasks were completed, they were once again compiled back into a feature and went into test as a whole.

What we tried to accomplish here was to keep the concept of a MMF while still breaking the work into smaller, more manageable units. What ended up happening was that features themselves became secondary to almost full task development, however we were tracking features through the system for our cycle time. Early, heavy task features that focused more on the business model skewed the cycle time higher, and later UI tweaking features sent it lower. As such, our cycle time diminished quickly as the deadline drew near...a good thing, but I don't think it was totally attributable to the team's momentum.

I think we failed here in poor estimation of what lie in front of us when we started. A good bit of this is the situation we were in at the onset where we were under pressure to start getting things moving right away, and we didn't give much credence to estimating later features very well. That wasn't really a Kanban issue, and we should have known better. The excuse is we had very little time to ramp up on the discovery side of things when we got the project, but it would just be an excuse...we should have known better.

One final area where we had some issues was in reporting where exactly we stood in features completed. We were fairly visible on this project, and had a lot of interest in our success by the due date. (OK, what project doesn't?) While you could look at the board and see what was being worked at any given point, due to the lack of good feature estimation up front, it was hard to see where we were in the big picture. In the latter half of the project we stole ourselves a project manager, and she did a bang up job of getting that information worked out, but she did struggle in figuring it out. Again, I think she had trouble due to the lack of good estimation up front.

It wasn't all pain and suffering as we moved our cards across the board.

One good thing we got out of the board was it was easily changed to fit our constantly changing team size and make up. We started out as three developers, and ended as four developers - two different than the original three, one PM, and one QA person. Being able to walk up to the board and change the queue limits on feature WIP, task development, and features in test made things flow quite smoothly as the project moved along. It did a good job of identifying a few roadblocks and getting them out of the way, as well.

As noted earlier, our cycle time did drop as we neared the due date. Part of that was due to the smaller features coming through later, but there was a good bit of momentum on the dev team, too. Morale stayed fairly good as we kept moving things into the done envelope at the right side of the board.

I still think we were successful with Kanban in this situation, but clearly I think we need some refinements around how we did it on this project. I'll save those ideas for my next post.
