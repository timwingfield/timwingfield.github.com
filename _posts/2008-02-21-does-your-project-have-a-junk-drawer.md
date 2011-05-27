---
layout: post
title: Does Your Project Have a Junk Drawer
category: development
---
## Does Your Project Have a Junk Drawer

Everybody's kitchen has a junk drawer. You know, the drawer where the tape, scissors, small jar of screws, various measuring items, and those clacker balls on a string that your mom is hiding from you. (Well, the ones my mom was hiding from me.) If you've got something in the house, and you're not sure where it goes, you fire it into the junk drawer. Oddly enough, you also find many useful items by looking in the junk drawer first when tackling something around the house.

However, I've found on a few recent projects that we're falling into the Junk Drawer model a bit. Look around your project, do you have file named "Utilities?" Maybe one called "GlobalMethods?" Or the very popular "ProjectHelper?" If so, there's a good chance you're throwing all kinds of things into the junk drawer. Could be a static class library, a little something in the App_Code directory in an ASP.Net project, or even a javascript file. Or, better yet, all three!

Now, don't misunderstand me, utility classes can be helpful. If you've got a series of string manipulations you need for a project, then a static stringUtils file makes perfect sense. Maybe a constants file for things that don't fit in an enum. As long as they are well defined and don't creep outside the scope of what you're trying to accomplish, I think they can be very helpful.

But, the junk drawer file that contains string manipulations, constants, get user name methods, some validation methods, a few odd conversion methods, a couple more string methods, and a few methods only called from your test project is not much of an asset to your project.

From a usage aspect, how do you tell other team members where your constants live? If they're scattered about your utility file, suddenly you're going to the same file for some string methods and your constants representing a product group. Or worse, your team gets so used to hitting your helper file that everything starts collecting there. Before you know it, you're looking at a maintenance nightmare with a couple thousand lines of code that should live in a number of more logical places.

Look around your projects, if you find a junk drawer take the time to refactor that thing out of there. Get all the files where they belong. You could end up with a utility file or two, but most likely you'll find you can move a number of methods right to the class that's using them because it's the only class that's using them. Turns out our friend YAGNI contributes many "global utility" functions to our projects.

Keep the junk drawer in your kitchen, though. Where else are you going to keep your SpongeBob commemorative Krusty Krab stamp?
