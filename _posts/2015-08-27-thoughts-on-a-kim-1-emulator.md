---
published: true
title: "Thoughts on a KIM-1 Emulator"
tags: 
  - "retro-computing"
  - "kim-1"
  - emulators
date: "2015-08-27 10:02 -0400"
category: "retro-computing"
---



So, nobody has _really_ made a fully binary compatible [KIM-1](http://www.oldcomputers.net/kim1.html) software emulator.

[KIM Uno](http://obsolescence.wix.com/obsolescence#!kim-uno-summary/c1uuh) KIM-on-an-[Arduino](http://arduino.cc) project is really cool, and highly accessible. It does 96% of what needs to be done, even without hardware. The [MAME/MESS](http://www.mess.org/) mess is an approximation, but it doesn't do single-stepping, which is pretty much the best thing about the KIM-1. And it really doesn't behave like a KIM-1. I even found an old Palm III emulator that is actually pretty close, but it does not pass the acid test.

<!--more-->

Where by "acid test" I mean "does it play [WUMPUS](https://en.wikipedia.org/wiki/Hunt_the_Wumpus)?"

Because of how the KIM-1 was designed, the intention was to give the engineer a pretty complete turnkey solution that would highlight the features of the [MOS](https://en.wikipedia.org/wiki/MOS_Technology) [65xx](https://en.wikipedia.org/wiki/MOS_Technology_65xx) family of [CMOS](https://en.wikipedia.org/wiki/CMOS) processors. And it does this admirably. So well, in fact, that people just bought them to do the work the MOS expected them to design new boards for.

So a full emulation requires emulating not just the CPU and registers and ROM, all of which appears to be pretty straightforward. It also requires emulating the two 6530 [RRIOTs](https://en.wikipedia.org/wiki/MOS_Technology_RRIOT) that provided the IO and timer capabilities they were demonstrating. And WUMPUS needs a working timer. (Perhaps for its sucker feet?)

So, as a very novice hardware hacker, have been thinking long and hard about how to emulate this rather strange memory map, where a single block of memory can contain ROM, RAM, IO, and timer interfaces across two different discrete devices. I'm going to go ahead and assume this is a **hard** problem, because so many folks have just ignored it. Or returned a random value for the timer (because some games just used the current timer value as a random seed [yes, I know... it was the mid 70s; cut us some slack]).

But WUMPUS actually needs a working timer. And while I'm not sure I'm the person to provide that timer, my mind keeps turning on how one might emulate this in software. Does it need to be a separate task? Probably. And the "ticks" it makes need to match the 1Mhz speed that 6502 implementations ran at, at least as a master clock, which can then be divided down based on what is stored in specific RAM locations within the RIOT. How to handle the second timer that raises an interrupt?

These are actually _very_ foreign notions to a high-level maintenance coder like myself, though they touch on concurrency and interruptibility in ways very similar to how the latest concurrent tools work.

I suppose it is because I recognize this problem as solvable that it interests me. It is a hard problem, but not intractible.

And it gives me hope for running WUMPUS on my Arduino.
