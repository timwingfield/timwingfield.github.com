---
Title: Coacing in India
Author: Tim Wingfield
layout: post
categories: agile lean coaching
---
##Coaching in India

My client has an offshore team in Coimbatore, India and I recently spent three weeks there working with them. This group of people is about to become the other part of our development team on our current project. They are joining us, merging their code with ours, all working towards completing the project -- we need to become a team and getting the 8,000 mile wall out of the way was step one.

###The People

<img src="/images/posts/coimbatore_team.png" alt="The People" align="left" />

There is no process, no technology, no framework that can lead your project to success without the right people. I had no expectations, good or bad, for this group prior to leaving. I had met the team lead as he had traveled to the US for a week, but I knew very little about the others. ([Todd has a great post](http://toddkaufman.blogspot.com/2011/07/thank-you-coimbatore.html) summing up his thoughts from the trip. I highly recommend reading it.)

What we soon discovered was this group was very excited to learn what we were doing. And not only what we were doing, but why we made the decisions we had made. We had already done four months of development so a lot of the groundwork was laid before they saw the code the first time. Unlike standard Ego Driven Developer who would take one look at the code and respond with, “This sucks, I can do this better,” these guys had already dropped that attitude (or never had it) and were ready to learn what was going into the project.

###The First Few Days

The first 2 or 3 days were spent having conversations and finding where everyone was comfortable. Many conversations took place about application structure, domain knowledge, and general practices of the team. It as almost a mini two-day conference that was just focused around our application.

Also in the first few days the team was very excited to show us the features they had completed prior to our arrival. The code looked fairly clean, but there were a few changes to be made, so they excused themselves to make the changes. Later we figured out why they wanted to leave the room: There had been a large amount of copy/paste development done, and they were still struggling to figure out what this copy/pasted code was doing.

One thing to note here, they had created cucumber features, and those cucumber features were green. Before we think they had just copied, pasted, and said “We’re done!” they did have acceptance criteria, and they had put those acceptance criteria to work in the form of automated cucumber tests. So even though the code needed some refactoring, and it needed some better unit test coverage, if we would have had to ship the application the next day, their features were functional and developed to our agreed upon acceptance criteria. 

###The Task

With the initial conversations out of the way, the task at hand became much more clear. We had a team of talented problem solvers who thought well in C# and general patterns  who needed to be brought up to speed on the practices and tools of our team. Essentially we were down to 12 business days to teach TDD, give a clearer understanding of BDD, get them up to speed on mocking, and get them more comfortable with the ins and outs of git and github. 

If this was an infomercial, I believe this is where I would say, “What would you pay now?!?”

Don’t answer yet!

###The Tools

Step one was to get some in depth TDD going. The best tool here is the daily code Kata, so we started with the Roman Numeral Kata and Todd and I took a ping-pong pairing approach through the first day as a demonstration. (Ping-pong pairing: one of wrote a test, the other made it pass then wrote the next test. Wash. Rinse. Repeat.) The next day, they did the ping-pong approach through the same problem. Everyday for the rest of our time the team paired on a Kata, switching pairs daily, with step one being to create a new dev branch in their local git repository. (We were using [this empty C# project](https://github.com/PillarTechnology/dot-net-kata) for our katas every day.)

The Katas did a good job laying the groundwork for doing TDD on the features that the team was going to work on while we were there. We did a lot of team coding with the projector so we could collectively work our way through the features. As coaches we were guiding rather than ordering which allowed the team to make and correct mistakes.

The second exercise we used almost daily was plenty of refactoring. Todd found a sample of some horrid code online that he converted to C# to use as an [example for practice](https://github.com/PillarTechnology/RefactoringExercise). Todd lead the exercise using some simple refactoring rules such as watching out for duplication, nested if statements, large methods, and multiple parameter methods.

After the introductory refactoring exercise we opened up the features the team had already written and started refactoring. Following the simple refactoring rules Todd had used previously the team went about refactoring their own code. In the first session one of the guys on the team got to delete about 40 lines of code and insert 2, and there were smiles all around the team room as he was doing it. One of the tallest hurdles as a developer is deleting code you have crafted, but this team was deleting it and enjoying it. 

By the time we left the team had refactored all four of the features they had been assigned. Most of the refactoring was done as a group, with a different person at the keyboard each day, to help teach what it means to refactor code. Our last week there the team had taken the initiative on refactoring and I returned from lunch one day with a request to do a code review of their most recent refactoring work. Once again, lots of smiles in the room.

###The Results

I was surprised how much we got taught in such a short amount of time. By leveraging as many exercises as we could, and doing as much hands on as possible, the team picked up the basics of TDD, BDD, and refactoring. We left a wiki full of cheat sheets (or “bits” as such documents are known to our Indian friends) as reminders for all the exercises we had done, and for some other concepts such as our git workflow and some nHibernate tips. 

However, without a group willing to learn and do the work of learning we would have never gotten so far. So a huge credit needs to go to the team for the work they put in to the crash course we were teaching.

Will they stick with it hard core? I doubt it, most teams will revert to “what they know” when the heat gets turned up. But I think this group will be pretty easy to influence back to their new practices...even from 8000 miles away.
