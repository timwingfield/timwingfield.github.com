---
layout: post
title: TDD Growing Pains
categories: development testing TDD
---
## TDD Growing Pains

I've understood and attempted to follow TDD practices for a while. The initial understanding of it was pretty tough, and very, VERY sporadically put into practice. After all, it's a pretty big shift in thinking when you first encounter it. "Write tests? For code that's not there?? Wow, that's fantastic!!"

So, over time I've gotten much better at the whole TDD thing. Or so I had thought.

Wednesday, mid-presentation, my lack of patience with the system outed me. I had written my tests, passed my tests, changed my code, changed it a little more, and then went to present it. Wow did I get smacked in the head by not running the tests after each change. (Continuous integration for a small demo app didn't really enter my mind. I have a hard time firing up CI at home since there's not much to I, but maybe I should join Mr. Donaldson in doing so.) So, big time lesson learned there.

The flip side to that bit of a stumble was the amount of time TDD saved me on my current project at work. I had written a number of unit tests to cover some business logic, and a few integration tests. A couple of defects came in showing that I needed to change a number of my dates to nullable objects. Not a difficult change, but not totally trivial, either. Made the changes, ran the tests. Oops...more changes, ran the tests. The whole change over was done, tested, and passing within 15 minutes.

A few pitfalls I've fallen into while traveling down the path towards TDD enlightenment:

1. I tend to wrestle a lot with when to layout some of the framework and when to just breakdown and write the tests. The main reason I wrestle with this one is that the good ol' crutch of intellisense sure comes in handy for test writing if you've framed your code out some. (When writing Ruby code in e, this doesn't seem to be as much of an issue for me.)

2. A recent project found our team working with a pile of generated tests. With the ever present deadline looming larger and larger, we decided to go with the generated tests as they appeared to be "good enough." They were good at the start, but as the code base grew, and our tests with it, we started looking at our CI build taking up to an hour. There's a big red flag. Dug into the code, very few unit tests were generated, but a pile of integration tests were. Takes a while for nHibernate to do its thing 4,316 times. (We've since started cleaning that up, build is back to a more reasonable, but still outrageous half-an-hour now...)

3. When to mock? I'm hip to the whole mocking thing, but identifying the right time to do so is still giving me troubles. I'm sure I'll get there with practice, just need some more practice.

4. Is this test trivial, or needed? In a [previous post](/2008/03/12/is-code-coverage-worth-bragging-about.html) I mentioned viewing code coverage the other way around, seeing what's uncovered rather than covered. I don't see 100% coverage, er I mean, 0% uncovered as attainable in the web projects I usually work on, but where do you draw the line? If you end up falling over on a piece of untested code, I guess it wasn't trivial.

5. I still have large holes in what I test. Just about all of my javascript code is completely untested. I know there are frameworks available to help me with that, but I haven't gotten down and dug into them.

So, short term I'm going to keep the ears pinned back and keep moving forward with the testing first. May as well get a home build server set up, and keep digging on mocking as much as I can. Gonna have to investigate [Moq](http://code.google.com/p/moq/), as well. Also, time to get that javascript tested. With as much AJAX as we're cranking out, this is quickly becoming a priority.

