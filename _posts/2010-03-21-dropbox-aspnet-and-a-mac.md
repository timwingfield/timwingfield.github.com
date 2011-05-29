---
layout: post
title: Dropbox, ASP.Net, and a Mac
categories: ASP.Net-MVC development Mac Windows
---
## Dropbox, ASP.Net, and a Mac

I recently [switched to a Mac](/2010/01/03/five-days-with-my-macbook-pro.html) for my development platform, and have enjoyed the experience so far. Working with zsh and ruby and rails and all kinds of things have been much easier in OSX. Getting down with .Net is still done in Win7 for me, usually on my VM. (I haven’t booted into Windows for .Net development, yet, VMWare has done great.)

I set up my environment so that most everything is saved on the OSX partition, which isn’t a big deal because VMWare just shares folders over to Windows. So, all my files reside in one place. Nice and tidy. I have a Code directory set up to keep my code on one spot (genius on the naming of that directory, I thought). It’s shared over to Windows, and I can get to everything in either OS.

The downside to this plan is that to Windows it’s a network share. If you’ve ever fired up Visual Studio to do some ASP.Net development over a network share, you know it’s not a happy camper. But, I don’t want to duplicate everything for the sake of keeping Studio happy. If I do that for Visual Studio, then I’ll have to do it for everybody, and that’s a slippery slope I don’t want to go down.

A little Googling later, and I find somebody using [Dropbox](http://www.dropbox.com) to keep it all synced up. I’m already a happy Dropbox customer, and had the, “Well, duh!” moment as soon as I read it. (If you’d like to become a happy Dropbox customer, [get an extra 250 MB when you sign up with my invitation](https://www.dropbox.com/referrals/NTIyNzAyMDE5). They give me an extra 250 MB, too.)

Pretty easy to set up at that point. I installed Dropbox on the VM, created a folder in it for .Net development, and I was all ready to go. ASP.Net was happy because it was now on a local drive, I was happy because I could still move things in and out of git on the Mac side of things.

I can already hear some howling, “You’re duplicating your code! It’s stored twice on the same machine!” True…but I Dropbox does all the syncing for me, so it’s mostly an afterthought. The upside is that I can get to it with the tools I want in the OS I want whenever I want. Code it up in Studio, grep the VSS files out of it in zsh, commit branch and merge with git on the Mac, and debug away in Windows.

Even though the code files exist twice, the tools don’t. I don’t have git or a text editor installed on Windows because I can use the Mac ones.

Another big downside would be coding sans Internet connection. For the most part Dropbox syncs everything up so quickly I rarely notice it. But, if I’m away from an Internet connection, that’s not going to happen at all, and even though both copies are on the same machine, they’d be out of sync until I get hooked back up. For all practical purposes, this hasn’t been an issue, yet.

Overall, for having a little duplication on the hard drive and an extra layer of something-that-could-go-wrong in there, the experience has been, well, not noticeable. Everything just works, I haven’t had to wait on Dropbox to finish syncing files yet, and I get to use the right tool for the right job.
