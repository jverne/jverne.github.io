---
date: "2016-02-17 20:09 -0500"
published: true
title: "Learning Astable Multivibrators Like a 5-year Old"
category: electronics
tags: [kids, '555', circuits]
---



My daughter finds my basement shack fascinating, mostly because it's full of interesting junk she can wade through. The other day she saw my collection of electronics parts and couldn't get them out of her mind. Which is to be expected. I mean, [have you seen electronics parts](https://duckduckgo.com/?q=electronics+parts&t=ffab&iax=1&ia=images)? They look like robot jewelry, which (now that I think about it) is like catnip to a 5-year old.

So, I promised I'd show her a few things that you can do with the parts. I _know_ she had visions of robots wandering around answering to her commands. But, I figured it would be an education in bottom-up design to just, you know, flash an LED. So, I collected a [555 timer](https://en.wikipedia.org/wiki/555_timer_IC), an LED, and a solderless bread-board and showed her how _boring_ it is to debug a circuit. It had been awhile since I made a multivibrator circuit, so I grabbed the first 555 datasheet I found on the internet and went for it (thanks, TI!)

What I've learned is that I have a terrible collection of capacitors. Really. My RC circuits are pretty limited, so we only had limited success getting a reasonable duty cycle going.

Also, the tweaky wires and boring schematics quickly illustrated what [littleBits](http://littlebits.cc/) is doing right. I mean, even when I was twice her age I was more interesting in slamming things together to make lights flash, speakers squeal, and motors turn.

But! Even thought she got bored and walked away to watch mom play video games, I decided to pull out the brand-new [BitScope](http://www.bitscope.com/) and see if my oscillator was actually oscillating.

I should have taken a screenshot, but I was right chuffed to see a perfectly nice square wave coming out of pin 3. Now, because of aformentioned capacitor issues, the duty cycle was a little tight which meant the whole "flashing" aspect was missing. But still: a great way to determine my BitScope works, as this is the first signal it has displayed that has not been self-generated.

So, overall, a win. As for budding hobbyist electronics and robotics enthusiasts in the house, not so much. Perhaps I should take advantage of the littleBits evenings at the local library for that.
