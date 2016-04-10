---
date: "2016-04-09 09:43 -0400"
published: true
title: Paranoid Android
category: work
tags: 
  - Android
  - coding
  - work
---



The only constant is change.

So, the wheels have turned ever so slowly, and now it looks like I am to be an Android application developer, at least for the next few months.

This new position I took recently has, so far, been the usual tour through Java and C++ with the expected diversions into Ant and Jenkins. However, I've found out this week that I'll have to get up to speed fast on Android on a set of embedded devices (_i.e._, not strictly a phone of some type). So, not only will I have to sort out Android app development using the Android APIs, but also how that fits into a highly custom runtime we're targeting.

<a name="more"></a>

As a result, this has been a tricky week for me. I spent a few days reading the API docs (ours and theirs) and figuring out what API level we are supporting, and figuring out how to make Eclipse do Android things. This last part is a challenge because it looks like The Google have deprecated their Eclipse ADT plug-in in favour of their own IntelliJ Idea Android Studio. However, all my examples and demos are Eclipse-ADT-based. It still works for the time being, but there is a decision to be made there. I also took a few online courses related to Android and Android development, if only because I've never really used _or_ coded an Android device.

(Truth be told, I'm still not a huge fan of Android as a mobile UI. It works fine enough for what I'm doing, but I cannot imagine replacing my BlackBerry with any Android device. I find the user experience just so odd and clunky. But I digress.)

I'm still a bit at sea with all this, and the requirements are _very_ mushy at the moment.  But I've been down this road before. All those tendrils I'm growing toward each other will meet over the next week and I'll have put together the story I need to feel a lot more confident in where this is all going. It looks like this is going to be a bit of nice green-field development; our small team is going to put together and maintain a few key apps, along with the libraries necessary for those apps. Libraries that will be useful if we need to push out a custom app at the last minute, which is part of the business aim here.

So, exciting times.
