---
layout: post
title: Kanban-o-rama - Part 1
categories: development kanban
---
## Kanban-o-rama - Part 1

Our current project is much more of the maintenance variety than of the new development type. Originally we tried to apply our standard scrum-ish approach to it - feature cards, load sheets, 2 week iterations, etc. However, it became clear that working maintenance tickets wasn't going to fit that model. Our load sheets meant nothing after a while because they were just getting overloaded with work items that were un-estimated, but needed assigned to get worked. It also became increasingly difficult to track the status of an item. Due to the lack of information about some tickets, any developer would show multiple tickets being "worked" at any given time. Keeping track of that on prod push day wasn't very easy, either.

Enter the Kanban idea.

The idea was brought up after a Friday retrospective by fellow QSI guy, [Alexei](http://govorin.blogspot.com/). Comrade, myself, and our PM had about an hour discussion around the idea, and the following Monday put it into action. I did some information gathering over the weekend, hit up a couple other Quick guys for some more information, "borrowed" a white board from an office in the building, and away we went.

### Our setup

Our setup is pretty simple. You can have 1 item as "Work in Progress" at any one time. You can't work more than one item at a time. Focus on that item until complete, then pull an item from your backlog.

We set up the backlog not as a community backlog, but each developer has his own backlog. I know this isn't ideal, but it gives us one extra layer of control on the flow of which tickets go to which guy to fix them. (The system we're working on is pretty broad, and though I'd love to practice collective ownership of the whole thing across the whole team, that's just not practical.) The backlog can max out at 3 items, and the item you choose is your choice, unless there's a high priority item in your backlog. (Denoted by a purple ticket rather than the normal yellow.)

If your item becomes blocked, we have two blocked areas available to move the ticket into. The first is "Blocked, need more information." Tickets moved here are assigned back to the PM who will follow up with the user to get the information needed to complete the ticket.

The second blocked area is "Blocked, Internal" which is a horrible name...the creative juices just weren't flowing that day. Typically tickets get moved here when they're dependant on another work item to be completed prior to them being worked.

Our max tickets allowable in the Need More Info slot is 8, and the internal is 2. If we go over those counts, we stop and figure out what we need to do to move those tickets along.

Once a ticket is no longer blocked, it goes back into the developer's backlog that originally had it. If there's not room in the backlog when it comes unblocked, it will wait in the "Ready for Dev" queue that is maintained in SharePoint. All the tickets are tracked through SharePoint as well as on the board, but prior to hitting the board they're managed only in SharePoint.

Once a work item is completed, it moves to "Ready to Test." The rules of testing are you test a ticket you didn't complete, as we don't have dedicated QA resources available. When you complete an item and there's one available for test, take the time to test it before starting your next item. So far, using the honor system has worked well, though we do still have some testing to catch up on before we do our weekly prod push. (We've picked Tuesday, so there's some testing going on Monday afternoon.)

Following testing, the ticket moves to "Tested." There it sits until it's rolled out to production.

That's the standard flow we've been using, but we did open up an "Emergency" option. So far, we've only had three emergency items drop into that slot. When that happens, the developer chosen to work it stops the item he's currently working and switches gears to the emergency until it's complete.

I'll end part 1 here. Up next I'll show off some photos of our board and add some more details as to how its been working out for us.
