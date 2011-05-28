---
layout: post
title: Beware Your Buffering
categories: development kanban
---
## Beware Your Buffering

In a twitter discussion that was centering around some Kanban joy, the point of buffering came up. I offered [a bit of twitter-esque advice](http://twitter.com/timwingfield/status/6944584935), meaning it was short, could be interpreted as terse, and lacked the detail it needed. As any good friend would do, [Jim](http://twitter.com/ajimholmes) called me out for my 140 character bit of guidance.

So, in more than 140 characters…

Be careful with your queues on your Kanban board. (I say queue here, because a buffer is just the queue for the next step.) By definition, any queue is waste. It’s a step in the process where something is waiting, therefore value isn’t being provided to your customer.

Can queues be used effectively? Yes. Quite effectively, but you have to stay on top of them. In reality, there has to be some queuing going on to give a pull system something to pull. In practice, those queues need to be as small as you can keep them to keep things flowing.

My tweet that started this mess was that I’d been burned by buffers on more than one occasion. Here’s one nasty one where the queue wasn’t a help, it was hiding the real problem.

We had a project where our developers far outnumbered our testers. This isn’t an unheard of scenario in the world of software development, but we handled it badly on our Kanban board. We ended up with not one, but two buffers between the dev team and the QA folks. The true, root cause problem was we had a resource problem because we needed more testers. Instead, we masked it with some queuing.

The biggest problem was that we lost our short feedback loop from development to demo. Early in the process, we’d complete a feature and it would demo within a day or two. As the project progressed and the developers’ momentum took off, the testing team was backed up and the feedback loop grew. Bugs were sitting open longer, code complete features waited to be tested, and the churn began.

Our solution was to swarm the test queue to get it lowered. Having a dev or two help get some testing done got our backed up test queue fixed, but it put devs in a testing role which I’m not a big fan of doing. (Devs are notorious for making sure something works rather than looking for ways something could break.) Also, this solution was very temporary as the queue naturally filled back up once the dev team was back in high gear. The actual solution: add a testing resource. Our full queues told us that, but we didn’t listen too closely for a while.

In the end, some buffers and queues are inevitable in many situations. However, make sure to do the following:

1. Make them as small as you can, maybe half the size of the queue limit of the step that the buffer is feeding. Adjust as necessary, but don’t keep increasing it as it fills up.

2. If you need to increase its size, ask why a couple times to clear it up. If the answer is, “Because we need more room!” then look at the next step and see why it’s backing up your process.

So, back to what started all this…buffers can bite you in the butt as they tend to mask the issue rather than solving it. Make sure your buffers aren’t hiding a bigger problem.
