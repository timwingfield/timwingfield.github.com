---
Title: Katas for Teaching
Author: Tim Wingfield
layout: post
categories: agile lean coaching
---
##Katas for Teaching

While recently bringing a team up to speed on Test Driven Development (TDD) in a very short time frame we leveraged code Katas as a teaching tool. The Kata approach is to use a simple code exercise and repeat it a number of times to practice the act of writing code rather than the act of solving the problem. In fact, “getting done” is not usually a requirement as Katas are typically time boxed activities. By repeating the problem you spend less time on the solution and more time on your craft.

We got to spend two weeks going through two different Katas with the team. At the end of those two weeks they had definitely learned some new things and had strengthened their approach to TDD. The team also struggled in some areas at the end of our practice time, some of which was attributable to their teachers. We had more things to work on during these exercises, so we did not get to be full time proctor every day.

**Day 0** - Roman Numerals: The other coach and myself did the kata using ping-pong pairing, where one of us would write a test and the other the implementation. We did this on the projector to demonstrate TDD. We stressed doing the simplest possible thing to solve the problem, and that changing code that has already been written is part of the practice.

**Day 1** - Roman Numerals: Today the team got to dive into their first kata, and they
did group pairing on the projector. Again we stressed the “simplest possible thing”
which was illustrated pretty well with a line of `return 1` to solve the first step of the Roman Numeral kata where “I” is the input.

**Day 2** - Roman Numerals: Again the team did the Roman Numeral kata where they were
taking in a string of Roman numerals and returning the correct integer value. Today we
switched up the focus a bit and looked much closer at refactoring code rather than getting closer to a solution. We spent enough time on refactoring that we did not solve the first subtraction case of “IV.” The team got a pretty good look at refactoring this way and it also helped us stress that the Katas were not about solving the problem.

**Day 3** - Roman Numerals: The third day was essentially a repeat of days one and two. The two of us coaching the team stayed out of the way on this one and let the team direct themselves. They combined the first two days by getting further with the solution, but also doing a couple of refactoring steps to keep the code clean. The biggest change today was we stopped using the projector and group coding, and instead had them split into pairs.

**Day 4** - Roman Numerals: Day four saw us throw monkey wrench number one into the works: Flip the Roman Numeral problem and take in an integer and return the correct Roman Numeral string. I had forgotten how much more difficult this approach to the problem can be, and it slowed our teachings quite a bit as we collectively became focused on the problem and not on the practice.

One good thing did come from switching the problem up to something more difficult, it got the team lead to ask the age old question: “But TDD takes longer, why do we do it?” After the team lead got a straight answer of, “Yes it does,” he seemed to really tune in. After explaining that we will happily trade a little time in initial development for a lot of time during product maintenance, the entire team was nodding in agreement.

**Day 5** - Roman Numerals: Our last day of doing the Roman numeral kata and we went back to the regular way of doing the kata from days one, two, and three by taking in  a string and returning an integer. For today’s fun at the halfway point of the kata we had everybody get up and switch pairing stations. This was a way to show that you will inherit somebody else’s code as a project goes along, and with the team all taking the same TDD approach it will be easy to see where the previous pair had left off and what move your pair could make next.

**Day 6** - Game of Life: For our next kata we switched to Conway’s Game of Life (GOL). This is a tried and true kata, and though I thought it was quite a jump in complexity for a simple kata, I was sure we could carve out just enough of it to continue on the path of Red, Green, Refactor that we had started with the Roman numerals in the previous sessions. 

The first day of the GOL was definitely focused on solving the problem, but that was understandable as it was a new problem and it needed to be solved once before you could delete it and practice solving it again. The team regressed a little from their solid TDD approach from the previous week. Again, not surprising as teams will fall back to “what they know” when things get a bit more difficult, which in this case was trial and error implementations. It was not a total regression as there were a few unit tests written by each pair.

**Day 7** - Game of Life: Day two with the GOL went much better. The problem solving was basically over, so focus went back to TDD and refactoring much more. We had to have a few reminders for “simplest possible thing” again as a couple of pairs were implementing nested loops to simulate the game’s canvas when the instructions were to ignore the canvas and focus on the rules for the cells to be living or dead. Once brought back on task they got back to good TDD practice and implemented the four rules for the cells.

**Day 8** - Game of Life: Day three with the GOL and we added the canvas concept to the list of rules and how many cells should be alive on that canvas to start and that the group would progress at least one generation. They were to do the practice from the previous days with the cell rules and expand on them with all the new rules. Yes, we took them from 0 to 60 took quickly...and the exercise showed it.

We had one pair not even implement the rules for a cell, instead just started hammering out loops to build a canvas. Another pair focused completely on getting the output of `0` or `1` correct. A third pair did not throw away the code from the prior day, so they already had the four cell rules implemented. Though that was “cheating” just a little, the bigger issue was that they were not even going to use the already written code.

As the third day of GOL shook out, we got most of the pairs back on track, but it took the white board, some coaches jumping in to pair for a bit, and a lot of “Do you have a test for that?” questions. It was definitely a big jump, but in the end things were again progressing in the right direction.

Some lessons learned from this particular day:
1. We added too many rules too quickly.
2. When you are new to something, and in novice mode in the Dryfuss Learning Model, then you want specific rules to implement. By giving the team new specific rules, they hedged directly towards implementing them and ignored building on the prior days’ code.
3. On the coaching side, we totally missed on building on the previous days’ exercises. 
4. Like our change in the Roman Numeral kata on day four, adding these rules changed the exercise once again to a problem solving exercise.

**Day 9** - Game of Life: For our last day with this team we lowered the rules back to a more sane level which again allowed them to focus more on the practice and less on the problem. This helped as we saw unit test counts rise with each pair and better focus at completing smaller steps rather than trying to solve the whole thing from the start.

###Lessons Learned

Katas are a great way to teach, and the changing pairing stations exercise was a lot of fun. But you have to keep the focus on the practice not on the solution. Keeping the problem simple early will allow more focus on the practice. When switching problems, be sure to take the solution in small steps so the focus can remain on the practice. 

Be clear in the rules: Deleting the code before you start. Red, Green, Refactor. Solving the problem is not the main goal. If you have the time and availability, be a full time proctor. Watch for pairs having issues, or the whole group struggling, and try to get them back on task sooner. If a team is new to TDD that will usually mean stressing the simplest possible thing and asking, “Do you have a test for that?” often.

I have been through a couple of code camps where we practiced for a few hours and have done Katas myself at Code and Coffee a number of times. But this was the first time I put them to work as a teaching tool over the span of days and can say I was really happy with the results. Even with the goofs we made, we still got the team a long way with TDD in a very short time.
