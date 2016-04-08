---
date: "2016-04-08 10:48 -0400"
published: false
title: "Maybe Harder is Better?"
Category: "embedded-systems"
Tags: 
  - Tessel
  - PIC
  - Microchip
  - IoT
---

The Internet of Things. It is all around you. It is there when you pay your taxes. It is there when you take out your neighbour's trash. It is made up of cloud-based web apps and Node.js powered interfaces.

I have a few colleagues that are honest-to-goodness embedded systems developers, and they all without fail absolutely hate these newer embedded toolchains. Most embedded developers I've known over the years may have played with IDEs over the years, but eventually go back to plain old POSIX command line development. _Maybe_ they choose fancy text editor that can run Make or Bitbake for them, but that's about it.

But for weekend warriors and hobbyists, setting up various toolchains for cross-compiling can be a real problem. To be fair, it's a problem that's often measured in hours as you sort out all the steps and read blog postings (yay for the internet, because in the old days you had to figure this stuff out seriously out-of-band), as long as you are reasonably good at hacking away on computers and figuring problems out in a step-wise manner.

The problem I have is keeping these toolchains up-to-date and working over time. I'll get things working so I can hack on my EZ430 Chronos, and then put that down for a few months. When I come back to it, some unrelated system change has broken some key step, or I need to update part of the toolchain which causes a ripple effect of failure. So, we are back to a few hours of busy work putting things back together, which often burns up the time I've blocked out for the project, or my interest (or both.)

To be fair, this isn't limited to embedded toolchains. It's just more obvious, in my experience. As a counter-example, recently my entire Ruby and RoR development environment on the Mac was completely hosed by an OS update. (Apple has done this to me a few times, actually: more than once an innocent update has actually had subtle effects that broke some development environment I depended on.)

Anyway, I get why all these vendors want to get hardware into your hands with the thinnest possible cloud-based toolchain. They know as well as anyone that the barrier to entry is often the toolchain itself, and the faster you get a USB cable hooked up to some Node.js or cloud IDE, the faster you are going to blink that LED, and keep it blinking over successive weekends.

However, I've noticed a down-side that isn't necessarily related to what the pros complain about when discussing these tools. 