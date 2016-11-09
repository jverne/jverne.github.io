---
date: '2016-11-07 23:32 -0500'
published: true
title: Windows OS X 10 Ubuntu Edition
category: daily
tags:
  - os x
  - windows
  - laptop
  - lenovo
  - posix
---
Well, I finally bought [a new laptop](http://www3.lenovo.com/ca/en/laptops/thinkpad/thinkpad-t-series/T460s/p/22TP2TT460S). The T460s seems to be the hacker weapon of choice these days, so after a little research I decided to go for it. So, I'm going to eventually be the owner of an "ultrabook", and the first laptop that I've ever purchased with my own money that isn't an Apple product.

According to UPS it's on its way from China, so I don't have it in my grubby paws yet. I suspect I'll miss the giant screen on the old Macbook Pro I'm currently using. I won't miss the tiny battery life or the way it acts like a little space heater.

I _probably_ won't miss OS X, at least too much.

The idea was to get a smaller upgradeable laptop with decent Linux support and run [Arch](https://www.archlinux.org/) or [Gentoo](https://www.gentoo.org/), blowing away the Windows 10 install it comes with.

<a name="more"></a>

OS X works fine as a development workstation, of course. The reasons I switched to OS X early on was because both Linux and Windows were such a hot mess for something that, really, ought to be pretty easy. But I've made a career out of not really caring that much what platform I code on. I've been a paid cross-platform developer for many years now so I really don't have a dog in this fight. I do like my POSIX shell tweaked  just right, but I also like pointy clicky GUIs for browsing and IDEs and what-not. Think of it as "laziness as a virtue".

This hybrid approach fit nicely with OS X, and I've banged out a lot of releases using a Mac.

But I've banged out a lot more using Windows. Even the shitty releases of Windows (I'm looking at you, NT 3.51).

I was lucky, in that early on I also worked for a company that made POSIX tools and APIs for Windows, which made things much easier for me. I cut my teeth on pre-POSIX command-line-only environments, and old habits die hard.

So, once I'd placed the order for this new laptop I started thinking ahead to how I was going to configure it for maximum coffee-shop hackery. And I came to a surprising (for me) conclusion.

I'm probably __not__ going to install Linux on it, at least for now. I actually have very few bad things to say about Windows 10 as a development OS at work. And installing Linux on a laptop, configuring it just right, and all that nonsense is just _boring_. Quite frankly, most of what I need an OS to give me is a decent POSIX command-line, and it just so happens that [Windows 10 now offers a fairly useful Linux style command line environment](https://msdn.microsoft.com/en-us/commandline/wsl/about).

That's right. I'm a [switcher](https://www.apple.com/pr/library/2002/06/10Apple-Launches-Real-People-Ad-Campaign.html) again, just like back in '02. Or maybe I only like to use releases that have the number 10 in them?

It isn't tightly integrated like that other toolkit I mentioned from TLA, Inc., but it works fine for doing Gradle builds and doing unnatural things to pipes with `find`, which is sort of my life right now. And it is certainly the path of least resistance for a lot of those little apps that let me manage my ebook collection and so on that I always forget about, and then have to spend a few days figuring out on Linux.

So I figured, why not just turn on all the developer settings in Windows 10 and see if it works out?
