---
date: "2016-04-08 10:48 -0400"
published: true
title: "Maybe Harder is Better?"
Category: "embedded-systems"
Tags: 
  - Tessel
  - PIC
  - Microchip
  - IoT
---


The Internet of Things. It is all around you. It is there when you pay your taxes. It is there when you take out your neighbour's trash. It is made up of cloud-based web apps and Node.js powered interfaces.

I have a few colleagues that are honest-to-goodness embedded systems developers, and they all without fail absolutely hate these newer embedded toolchains. Most embedded developers I've known may have played with IDEs over the years, but eventually go back to plain old POSIX command line development. _Maybe_ they choose fancy text editor that can run Make or Bitbake for them, but that's about it.

But for weekend warriors and hobbyists, setting up various toolchains for cross-compiling can be a real problem. To be fair, it's a problem that's often measured in hours as you sort out all the steps and read blog postings (yay for the internet, because in the old days you had to figure this stuff out seriously out-of-band) as long as you are reasonably good at hacking away on computers and figuring problems out in a step-wise manner.

The problem I have is keeping these toolchains up-to-date and working over time. I'll get things working so I can, for example,  hack on my [EZ430 Chronos](http://processors.wiki.ti.com/index.php/EZ430-Chronos), and then put that down for a few months. When I come back to it often some unrelated system change has broken some key step, or I need to update part of the toolchain which causes a ripple effect of connected failures. So, we are back to a few hours of busy work putting things back together, which often burns up the time I've blocked out for the project, or my interest (or both.)

<a name="more"></a>

To be fair, this isn't limited to embedded toolchains. It's just more obvious and commonplace, in my experience. As a counter-example, recently my entire Ruby and [RoR](http://rubyonrails.org/) development environment on the Mac was completely hosed by an OS update. (Apple has done this to me a few times, actually: more than once an innocent update has actually had subtle effects that broke some development environment I depended on.)

Anyway, I get why all these vendors want to get hardware into your hands with the thinnest possible cloud-based toolchain. They know as well as anyone that the barrier to entry is often the toolchain itself, and the faster you get a USB cable hooked up to some Node.js interface or cloud IDE, the faster you are going to blink that LED, and keep it blinking over successive weekends.

However, I've noticed a down-side that isn't necessarily related to what the pros complain about when discussing these tools. I suspect that a great majority of hobbyists happily hacking away at Tessel devices or getting into PIC via MPLAB Xpress see few problems. Their tools work, and continue to work. What could go wrong? Well, if something _does_ go wrong (and it will) much of the debugging and problem solving skills one has learned over the years has little value when trying to get things to work. You are sort of at the mercy of the cloud, or some library, or some driver. In some ways, we just move the problem around.

Here are two examples:

1. For fun, I requested a free Xpress Board from Microchip, and dutifully signed up for access to their shiny new [MPLAB Xpress
Cloud-based IDE](http://hackaday.com/2016/02/15/microchip-unveils-online-mplab-ide-and-10-board/). I plugged in the board and... nothing. For some reason, on my Mac, the board is being mounted as a read-only device, so I am unable to drop hex files onto it (which is the programming interface) and neither is the IDE able to install and run compiled apps. No amount of system tweaking and hacking showed any promise, and the Microchip forums were less than helpful. I recognize this is probably something specific to my environment, but after a few hours of messing about I gave up. I was able to determine that it worked on Windows 10 at work, and that's as far as that went. Microchip has [open-sourced their USB mass-storage loader](http://hackaday.com/2016/03/11/microchips-publishes-usb-mass-storage-loader/) that is at fault here, so _maybe_ I can figure it out. That isn't really an itch I want to scratch, though.
2. Even more recently, my [Tessel2](http://tessel.io/) arrived, which is a platform driven by a more familiar (to me) command line interface. This interface is deployed by Node.js, so the first step is to install Node. And then everything fell apart in a variety of unhelpful ways. On Windows, the USB-device programming drivers are supposed to be provided when the device boots, but for Windows 10 this doesn't work. The slightly more helpful Tessel forums actually showed they are trying to push a change out to fix this shortly. Ok, no problem. I plan to use my Mac with this anyway, so I take it home and do the same setup and... it completely fails, and looks like no one has even tried the steps they show on their start page. In this case Node is unable to install the Tessel tools globally (probably because of how OS X is so locked down now) and unable to run properly when installed locally. I'm sure this is all very solvable, but at this point I declined to spend the time digging into it. Perhaps someone else will figure it out later and I'll pick up the thread then.

My point isn't that everything sucks (though it does, sort of) but rather that if this was a traditional toolchain I might have had a fighting chance. But, because these new models are based on stuff that is at a higher level of abstraction (i.e., the web, or USB mounts, or monolithic Javascript engines) my usual ways of solving these problems are not as useful.

And the end result is the same: as a weekend warrior, the thought of wrestling the interface or toolchain often makes me want to choose a different hobby.
