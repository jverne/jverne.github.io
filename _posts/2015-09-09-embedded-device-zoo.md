---
date: "2015-09-09 14:50 -0400"
published: true
title: Embedded Device Zoo
category: "embedded-systems"
tags: 
  - arduino
  - TI
  - STM
  - BeagleBone Black
  - embedded
---


While cleaning up my work area today I moved a bunch of electronics stuff around into different storage boxes. Since I had _most_ of the turnkey embedded hobby systems out as part of that reorganization, I decided to take a photo of them.

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/clvrmnky/21285543061/in/datetaken-public/" title="Embedded Device Zoo"><img src="https://farm6.staticflickr.com/5685/21285543061_bd6884476c.jpg" width="372" height="500" alt="Embedded Device Zoo"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

<a name="more"></a>

Clockwise from lower-left:

1. Texas Instruments [MSP-eZ430U-based Chronos](http://www.ti.com/tool/ez430-chronos) programmable digital watch (with wireless and direct-connection programming dongles)
2. STMicroelectronics [STM32F0DISCOVERY STM32F0 Cortex-M0 kit](http://www.st.com/web/catalog/tools/FM116/CL1620/SC959/SS1532/LN1848/PF253215) (I think I got this one for free just by asking for it)
3. [Arduino Duemilanove](https://www.arduino.cc/en/Main/ArduinoBoardDuemilanove) ATmega328p (with a well-hacked Adafruit bootloader)
4. Texas Instruments [eZ430-F2013](http://www.ti.com/tool/EZ430-F2013) USB development system (which I got for free when I went to a TI event)
5. [BeagleBone Black](http://beagleboard.org/black) revision B, currently running either Debian or Arch ARM (which I received in trade for a guitar amp)

Not shown:

1. An Arduino-based [Triggertrap](http://www.triggertrap.com/) photography tool (a Kickstarter reward which doesn't even seem to be a product anymore)
2. A [LEGO MINDSTORMS RCX](https://en.wikipedia.org/wiki/Lego_Mindstorms#RCX) brick that I usually hack on with [my own fork of NQC](https://github.com/jverne/nqc)

I was originally going to turn the BeagleBone into a low-power edge box running Arch Linux, but that project was easier with some donated hardware and [DD-WRT](http://www.dd-wrt.com/site/index). I think the plan is to turn it into a [BitScope](http://www.bitscope.com/) device once that is officially supported.

The Chronos watch I've tweaked heavily, but the irony is I never wear a watch, so it sits in a box. It does occur to me now that the watch guts could easily be turned into a remote weather datalogger. So let's put a pin in that idea.

The Arduino is currently a KIM UNO KIM-1 (incomplete) software-only emulator [as discussed earlier]({% post_url 2015-08-27-thoughts-on-a-kim-1-emulator %}). I'd like to get back to getting the KIM-1 RRIOT emulation more complete.

The other two I've run the equivalent of "Hello World" on (_i.e._, made an LED flash). I've had idle thoughts about turning one or the other into a little bike computer of some sort.

So, not exactly bursting with embedded activity over here, but a respectible collection that I've actually spent some time with. I might even have working toolchains for the majority of these devices.
