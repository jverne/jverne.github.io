---
date: "2015-09-08 22:02 -0400"
published: false
title: How to not Repair a Dinosaur
category: "retro-computing"
tags: 
  - "trs-80"
  - model 100
  - electronics
  - hacking
---


As I mentioned in [a previous post]({% post_url 2015-09-02-retro-computing-the-last-refuge-of-the-scoundrel %}) I have a dinosaur of a [TRS-80 Model 100](http://www.oldcomputers.net/trs100.html) that I'm trying to bring back to life.

The symptoms:

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/clvrmnky/21233283076/in/datetaken-public/" title="Slightly Dead Model 100"><img src="https://farm6.staticflickr.com/5725/21233283076_24791a5140_n.jpg" width="320" height="180" alt="Slightly Dead Model 100"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

It responds to power by setting all the LCD pixels on except for that weird half column. Reset doesn't do anything.

Armed with nothing more than a copy of the original Tandy service manual I found on the internet, a cheap DMM, and three semesters of high school electronics shop education, I started troubleshooting today.

And I'm pretty sure I'm going to need a 'scope. All the easy voltage references check out, and the reset circuitry is setting things high and low when it ought to, and the CPU appears to be agreeing with these levels. And there isn't any obvious physical signs of failure. Which leaves seeing if I can get a picture of things like clock cycles going into (and out) of the CPU, and LCD driver pulses.

I'm almost positive that I'm going to eventually spring for a [BitScope Micro](http://bitscope.com/product/BS05/). This is a nice cheap-and-cheerful solution that I can run on the Macbook, or the Arch Linux box in my \[Radio|Electronics|Computer\] Shack, or even standalone via a [Raspberry Pi](http://bitscope.com/pi/) (or, eventually, my BeagleBone). And, if my memory of how analog 'scopes work, it has a sample rate and probes options necessary to get a decent picture of what this nearly dead computer is doing.

I mean, the Model 100 runs at a max clock speed of 4.9152 MHz (or some division thereof) so it's not like I have to freeze picosecond moments like a Time Lord here. And, well, the price is right, that's for sure. For a weekend warrior like myself, it's just right.

But, for now, I think I'm stuck. I probably ought to spend some time collecting all these pieces into one handy box. And maybe try to find the missing hardware from the first time I took it apart.

Which also makes it easy to ship as-is to an eBay victim if I decide to give up on all this nonsense.
