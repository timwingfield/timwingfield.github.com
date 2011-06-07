---
Base Header Level: 1
Title: Moving The Blog 
Author: Tim Wingfield
layout: post
categories: Jekyll Ruby development
---
## Moving The Blog

With the [Estimation Rant](/2011/05/12/estimation-rant.html) quickly becoming my most popular blog post and generating a good discussion in the comments, Blogger decided that was the day to start doing random deletions of comments and later posts. I have been leaning towards moving off the Blogger platform for a while, but being lazy and it mostly working, I didn’t move anything around. Since “mostly working” went out the window, it was time to move the blog.

But where to? I’ve always wanted to have a bit more control over where my content lived. I used the FTP upload option on blogger which kept the content on my own hosted server, but they discontinued that a couple years ago. I thought about moving to an installed WordPress blog, but that whole lazy thing kept me from pursuing that one too far. What about the blog hosted on WordPress? Why leave Blogger if that’s the choice.

Then I stumbled upon [Jekyll](https://github.com/mojombo/jekyll). Followed a [few links](https://github.com/mojombo/mojombo.github.com) to some other [Jekyll sites](https://github.com/joefiorini/userobsessed) then to how [github pages](http://pages.github.com/) works and made my decision. My content lives on github rather than in some database somewhere, and it exists as plain html files. The power and storage of github behind a blog being served up as plain HTML files? Awesome! Publishing by typing `git push origin master`? Geek points out the wazoo!

### Setting Up The Jekyll Site

Step 1 was to toy around with Jekyll some and see what was involved. Essentially do a quick spike of Jekyll and see if it was going to work. About an 3 hours into my spike, I had an html template in place, four of five test blog posts, and an about page. Decision solidified. I laid out the steps between where I was and where I wanted to be to get it launched and went to work. If you're the kind that flips to the back of the book to see how it ends, it took me roughly two weekends to complete the move and get it published.

The first hurdle I ran into was running Jekyll plugins on github. I had added a plugin to generate category links for me based on the categories in my blog posts. Pretty straightforward, but not handled by base Jekyll functionality. Everything worked fine locally, push to github and no categories. Looked around some, find the right page of the manual to complete my RTFM, and found that github doesn't run any code in the \_plugins directory as it is untrusted code. Seemed a good enough reason to me, and the fix was pretty simple. Generate the site locally, add the categories directory that gets generated to the root directory of the project, then `git push origin master` and the categories are there. _(I’m not sure this is the best solution, but it is a solution.)_

### Migrating From Blogger

This was the real PITA for the whole move. There were a couple suggestions on how to automate the move, but I had no luck with either of them. In the end I settled on doing it all by hand, which really wasn't that hard. Copying from the blogger dashboard into markdown required very few edits. If I was moving more than the 60 or so posts I had, I would have probably found a way to script an import or something. I figured I could copy/paste my way through it quicker than scripting it out, so brute force won the day.

The smallish edits I had to make were what you would expect. Recreate some formatting - bold, italics, headings, etc - add the images back in, and add the links back to the posts. My earlier blog posts were easy as I was really lazy back then with few headings, links, and images. My more recent ones where I have decided to add a few more pieces of flair took a little longer to recreate in copy/paste mode.

That said, if I had it to do over, I would probably brute force it again. If I had closer to 100 posts to migrate, I would probably opt for creating some kind of migration script.

### Migrating the Comments

The few comments I had on the blog I didn't really want to lose. What seemed to be the obvious choice here was to migrate to Disqus. They are everywhere, manage threads, help keep down spam, and hit right at my price point of free. The migration was a little trial and error for me, though.

My first try was to just import them from Blogger. Disqus has an automated way to do that, it took all of 4 minutes to complete the process. However, I had no good way to link my newly imported comments back to they’re original blog posts. Disqus will relate comments to posts in one of two ways, a unique identifier you provide them or the blog post url. I had no way to give them a unique identifier, and the url for each post was about to change.

After a little more research, I found that Disqus provides some tools for more complex blog migrations to keep your posts and comments linked up. (I'm telling you, the people at Disqus have thought of EVERYTHING!) So I redid the import to blogger, but instead of just importing the comments I installed Disqus as the commenting system on the existing blog. Then I had to do a quick CSV file to map the old url to the new url and upload that to Disqus. About an hour later, the comments appeared on the new blog. (The new blog was still not "live." It was running on local host and at timwingfield.github.com, but the comments were there.)

### Still On the Todo List

Sunday I "pushed the button" and swapped the DNS around to point at github rather than at blogger, and about an hour after that switch the DNS had refreshed to the point that I was seeing the new blog. But now that I have the level of control over my blog that most geeks like to have, I’ve got plenty on the todo list.

I still want to add some more features to the index page, starting with getting a comment count and link under each post to go directly to the post. I would also like to revisit that publishing the categories thing from above. Initial thoughts are I will end up with some little rake script or something to handle it, but may do some more looking. A dedicated mobile interface would be nice. Jekyll has the ability to publish at a given time, so I will need to spike that one out to see what I need to do. 

One week into this little experiment and I am liking it. I feel like I'm more in control of my content, I have a better comment system than before, and publishing is git push. Big fun!
