---
date: '2017-05-16 14:34 -0400'
published: true
title: Dance Like Nobody's Debugging
tags:
  - robots
  - robotics
  - electronics
category: electronics
---
So, A. and I completed the [Wigl dancing robot]({{ site.baseurl }}{% post_url 2017-01-08-wigl-it-just-a-little-bit %}), but the results were not that exciting. It appears to move, and the LEDs are lighting in a somewhat appropriate manner. But, after some experimentation with various instruments, it appears it is about a half-step off from the expected. I should report that A. successfully soldered the motors to the motor wires, and only once found out that you shouldn't hold the iron like a pencil, near the hot end. (Don't worry: no one was _seriously_ harmed.)

The idea is that certain notes with cause the robot to turn, move forward, etc. And certain combination of notes will cause mode changes. However, after some head-scratching it looked like it was sampling such that a B&#x266D; would turn left, instead of a natural B. Not only that, but the movements seemed, well, really jerky and weird. Almost like the sample rate was a little too fast. It wouldn't respond at all, and then it would take off in some random manner. Something was not right.

This was, of course, a little disappointing.

Anyway, since we have some of the tools to figure this out, the first step was to confirm through the  [Crowd Supply page](https://www.crowdsupply.com/vivek-mano/wigl) that the code published in the [GitHub project](https://github.com/vivekmano/wigl) repository is actually on the ATmega328P shipped with the kit. I also made sure the pin header pads on the board were typical sizes so I could order a 90-degree 6-pin header so I can start poking at the chip via a serial port.

<a name="more"></a>

It turns out that we can't be sure that what Crowd Supply shipped was within spec, so Vivek said he'd order a project for himself and make sure what was shipped was what he designed. Meanwhile, I could experiment a bit with the software, which required reprogramming the ATmega chip. Since I didn't have any programming headers around, I put the board down for a bit.

Fast-forward a few weeks and through the magic of global manufacturing and supply I have more 0.100&#x02033; (2.54 mm) Breakaway Male Headers than I will be able to use in my lifetime shipped right to my door for a few bucks.

Last night I soldered the header in and hooked up an FTDI USB-to-TTL-Serial cable to the board and started down the rabbit hole of talking to an ATmega chip via various AVR/Arduino tools. After talking with Vivek, the chip is _supposed_ to be Arduino Uno-compatible with an on-chip bootloader but it sure isn't behaving like it. It looks like the serial port circuit is sensing the DTR and invoking the auto-reset (or at least we see some LEDs flashing, which is the universal indicator for Arduino auto-reset) but otherwise I get the dreaded "avrdude:stk500_recv(): programmer is not responding" message.

Well, by then it's 1:30AM and I actually have to work in the morning, so here we are.

The next step is to pull the ATmega chip and put it in the Arduino that I know works, and poke at that with the built-in FTDI and possibly the ISP. Luckily I am the proud owner of an [AdaFruit USBtinyISP](https://learn.adafruit.com/usbtinyisp) so I have the tools necessary if I need to burn a new bootloader on the chip. I should also check that my el cheapo FTDI cable is actually doing the right thing using my 'scope. For all I know, the DTS is not being strobed and the Arduino bootloader on the chip has no clue I'm desperately trying to upload a new program image.

Hopefully by this evening I'll have a better idea if we assembled this thing right, or if maybe the kit has some odd or out of spec parts. Perhaps the next Wigl update will be a video of actual robotic things.
