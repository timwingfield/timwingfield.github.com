---
Title: Kanban on the Factory Floor
Author: Tim Wingfield
layout: post
categories: kanban agile lean
---
##Kanban on the Factory Floor

Over the last few years I have done a fair amount of work with Kanban on software teams,
but recently I got to see Kanban in action in a factory. Knowing that the Lean software
movement was born in manufacturing, it was very interesting to see Lean and Kanban in
action on a factory floor.

Some quick background details before we get too much further. At the request of my
client, I can not share what was being manufactured (or who my client is). What I can
say is the items they build are large. Large enough that they need to be separated into
pieces to be loaded on to a semi trailer to be shipped. Sometimes multiple semi trailers
are needed to ship one item. Steel is the principle material used in the manufacturing,
so there is also plenty of cutting, welding, pressing, and painting going on to go from
raw steel to completed product being shipped to the customer.

The building itself sits north to south, with the north end being shipping of the
finished product. The south end of the building is where the raw materials are
received, so the product moves south to north through the building to become a shippable
product.

###Factory Floor as a Kanban Board

The first thing that jumped out at me upon touring our factory was that the entire
building was the kanban board for this particular product. On a software project we will determine our value stream and write it on a whiteboard. These are the steps our features will work through from concept to cash. In a factory, there is no whiteboard with columns on it. Instead there is the factory floor with overhead cranes, welders, and paint booths.

This idea of the factory as a Kanban board is pretty easy to see when you are looking at
it. In an attempt to explain it, the south end of the building has stacks of steel with
other supplies nearby in a storage area. The factory is run pretty lean, but they still
need a supply of welding materials, nuts, and bolts. 

The steel begins its journey north through the building by first being cut and shaped.
It makes a stop at a plasma cutter, then some of it will move into a huge hydraulic press to be bent into the correct shape. From there it moves into the welding booth where robotic welders make the standard welds. Any custom welding will be done by hand at the next station. Following welding, the product is essentially put together and the finishing touches start by going through a cleaning process then into the paint booth. Once it is painted the only thing left to do is get it loaded on a truck to get shipped to the customer.

That is a pretty abbreviated version of the process. But from a Kanban standpoint once
the table under the welding robots is available, a sheet of steel slides in there. Same
with the multi-ton hydraulic press. If it has capacity, it has steel being pressed. The steps of the process are not arbitrary, they are physically located to the north of the step that precedes it.

###Lean and We Mean It

On the Lean side of things, there is no inventory. Once an item starts getting produced,
it has already been sold. There really is no room to keep one or more of these products
just sitting around waiting to be sold. It is not a practical solution for this
particular factory.

On the other end of the spectrum, there really is not any room for a large amount of
surplus steel to be stored, either. If the steel shows up at the south end of the
factory, it will go into production pretty quickly in an effort to get it into its
customer's hands.

Once again, there physically is no room in the factory to hold excess steel for that
"just in case" order that comes in from the field. Nor is there room to hold any extra
finished product at the north end of the factory for that "emergency" client.

###Work In Progress Limit? Um, Yeah...

On the software side of things we struggle many times trying to enforce our Work In
Progress Limits, or our WIP Limits. Many times if we need one more thing put into
development or testing, it is just a post-it note...put it in there! Stick it on top of
that lesser post-it note if you need the capacity.

Let's take a look at that same situation in our factory. We have a new order that just
came in, and it is an urgent one. Yeah, I know we already have 8 tons of steel being
welded by the robots, go ahead and put another 8 tons of steel on top of that and
get it done first.

Seems a bit silly, doesn't it?

Once again, the physical limitations involved with moving, shaping, and welding tons of
steel comes into play. It makes enforcing WIP Limits pretty easy. Only one thing can be
cut, welded, or painted at a time. If an "emergency" comes into the queue, it has to
wait its turn, there really is no room for it.

On a software team, that limited capacity is just as real, but it is much harder to
visualize. It is very easy to see a paint booth full to capacity, not quite as easy to
look at two developers and two testers and see that those four people are already
running at capacity with the work they have been given.

###What We Learned

I have enjoyed working with Kanban in the software industry, but it was definitely worth
seeing it working in manufacturing to see the differences. For software teams the
idea of limiting work in progress is a great goal, but clearly much more difficult to
visualize than it is in manufacturing. My biggest takeaway from seeing Kanban in action
in a manufacturing setting was that WIP Limits are easy where there is physically no more space for more work. 

The discipline needed in the software implementation of Kanban to enforce WIP Limits and keep queues from building up is more than a number on a white board.
