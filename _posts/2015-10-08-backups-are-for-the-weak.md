---
date: "2015-10-08 13:20 -0400"
published: true
title: Backups are for the Weak
category: "site-info"
tags: 
  - blog
  - linux
  - data
---


Well, I just went through **all** my old PATA drives looking for the MySQL dump from an earlier incarnation of this blog, and it appears that the data is well and truly gone forever. I made a backup image of a candidate drive, which was very lucky: the heads crashed hard whilst I was running [TestDisk](http://www.cgsecurity.org/wiki/TestDisk) on it.

But I'm not really able to make sense of the image anyway. It looks like this IBM drive is from my _original_ OS X/Mac OS box that I bought nearly 15 years ago. At some point I put it in a FireWire (remember that?) enclosure as a bootable Mac OS drive (when Apple still supported that) so I could play Alpha Centauri, and from there it ended up as an OpenBSD backup drive. So, most partition-level tools see a complete mess of HFS and DOS partitions containing a hodge-podge of duplicate HFS+, NTFS, and FFS filesystems.

It's an intractible mess, or at least enough of a mess the rewards are not worth the effort.  Just use the Internet Wayback Machine if you want to see how much I used to swear on my blog. (Hint: a lot.)

I suppose I did become an instant expert in Linux partition and filesystem tools. I still think the best solution to data loss is to not make data you are afraid to lose.