---
date: '2016-06-14 15:38 -0400'
published: true
title: Rexx Fortis Vocat
tags:
  - DOS
  - PC-DOS
  - Rexx
  - VirtualBox
category: retro-computing
---
So, I'm home sick from work today and, as one does, I'm idly playing around with some emulation stuff. Earlier I was researching my KIM-1 emulation project (which is turning out to be a bit harder than I thought).

Then, for some reason, I decided to get [IBM PC-DOS](https://en.wikipedia.org/wiki/IBM_PC_DOS) 7.x/2000 working on [VirtualBox](https://www.virtualbox.org/). This is not for any particular reason, though I've occasionally needed a real DOS environment to mess about with [abandonware](https://en.wikipedia.org/wiki/Abandonware). So, this image may be put to good use one day.

But for now, an almost-complete PC-DOS system. I haven't figured out the networking stuff yet, but it has CD-ROM support, loads [DOSidle](http://maribu.home.xs4all.nl/zeurkous/download/mirror/dosidle.html) so it doesn't burn up my Mac, the usual assortment of high/upper/confusing/WTF memory settings that DOS requires, and so on. I don't think networking will be that hard, but my Google-Fu is not finding the PCNet ethernet drivers that VirtualBox is emulating. So, for now I'm using sneaker-net.

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/clvrmnky/27674314215/in/datetaken-public/" title="PC-DOS 2000 on VirtualBox running Rexx"><img src="https://c8.staticflickr.com/8/7117/27674314215_fc8807cc6d.jpg" width="500" height="307" alt="PC-DOS 2000 on VirtualBox running Rexx"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

Yeah. So, that's a [Rexx](https://en.wikipedia.org/wiki/Rexx) script being called via the command interpreter via a pseudo [hash-bang](https://en.wikipedia.org/wiki/Shebang_%28Unix%29) mechanism (think of `/* ... */` as the shebang line). There's a reason I liked to run _PC_-DOS instead of that other one.

What's going to bend your noodle is that I actually _paid_ for a copy of PC-DOS, lo, those many years ago. So, I'm _technically_ not pirating anything, matey.

------
Well, that was easy. Started the PCNet packet driver and ran `DHCP` from the [mTCP](http://www.brutman.com/mTCP/) project. I was even able to annoy some people on IRC.
