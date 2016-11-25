---
date: '2016-11-24 22:08 -0500'
published: false
title: WTF WSL LOL NV JK
category: daily
tags:
  - Windows 10
  - windows
  - laptop
  - Ruby
  - WSL
---
As [discussed earlier]({{ site.baseurl }}{% post_url 2016-11-07-windows-os-x-10-ubuntu-edition %}), I have indeed purchased a Windows 10 based _ultrabook_ and I'm _not_ immediately installing Linux on it. I cannot tell a lie: I have kept Windows 10 on it, along with the [Windows Subsystem for Linux](https://blogs.msdn.microsoft.com/wsl/2016/04/22/windows-subsystem-for-linux-overview/) (WSL) to scratch that Ubuntu itch.

And it's just fine.

Even though WSL is in beta (and I'm compounding that by installing bleeding edge "Windows Insider" builds) it's actually pretty solid. I might be losing all my hipster geek street-cred by saying it, but Windows 10 is just as good for me as OS X. Since I'm no avid fan of **any** X.org environment, this means I think it's better than any Linux UI. So that's a win.

WSL seems to be a pretty complete command-line Ubuntu install, with all the trappings of a Debian-flavoured console. I haven't _really_ pushed it hard, of course, but as a sort of acid-test I moved my Ruby-Jekyll-GitHub blog stuff over to the new lappy and made the right `gem` and `apt-get` incantations until I was able to successfully run `bundle exec jekyll serve`. I also updated Ubuntu to Xenial last night with little trouble.

I didn't think I'd care that much about the mechanisms by which Microsoft has done all of this, but I've been skimming the technical notes with some interest. They've really done a decent job of implementing the user and kernel spaces.