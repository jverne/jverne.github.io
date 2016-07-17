---
date: '2016-07-17 17:24 -0400'
published: false
title: Groovy Android Rocks the Gradle
category: work
tags:
  - groovy
  - gradle
  - android-studio
  - android
---
Embedded Android development continues apace, and I'm currently head's down on an App Widget that needs an XML parser and some sort of datastore, which is a pretty good learning experience. We also ended up swtiching to a full-on Android Studio, Gradle, and jCenter environment, which has side-stepped a fair amount of Eclipse cruft. It has also introduced some infrastructure churn which I'm hoping settles down shortly. So, I am most definitely an Android developer now.

This has given me the excuse I need to think about using [Groovy](http://www.groovy-lang.org/index.html) at work, though, which is a bit if a win. We need a fair number of custom Gradle tasks, and I think the best way to do this is direct functional Groovy. If this morphs into a full-on [Spock](https://code.google.com/archive/p/spock/) unit-test environment I will call the whole thing a gigantic, play-off, Premier League level win.

The challenge is that I sort of promised a working demo of the app this coming week. So, I have my work cut out for me, I think. I was sure of this schedule on Friday, but then all weekend I've been remembering little things that need to be sorted before we really ship, so now I'm hoping I haven't over-promised.

So, the Groovy Spock will have to wait until I bang out a few hundred lines of Android Java, including a semaphore controlled background executor.

Good thing I'm a senior developer. It says so right on my job description!
