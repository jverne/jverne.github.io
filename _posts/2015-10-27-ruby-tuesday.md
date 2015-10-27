---
date: "2015-10-27 14:35 -0400"
published: true
title: Ruby Tuesday
category: coding
tags: 
  - ruby
  - RoR
  - Rails
  - OS X
---



On Monday I had a meeting, and today (Tuesday) I blew the space-dust off of my copy off of the [Pick-axe Book](https://pragprog.com/book/ruby/programming-ruby) and, Crom save me, re-re-reinstalled [Ruby On Rails](http://rubyonrails.org/) on my lappy.

These two things are tangentially related, of course, and this will be discussed in a follow-up. But, since I'm in a mood to Learn All The Languages, I may as well refresh my L33t Ruby Skillz while I'm at it.

<a name="more"></a>

But (as [Eloise](http://www.eloisewebsite.com/) would say), _oh, my Lord_, did the OS X 10.11 upgrade totally **wreck** everything to do with my RoR and Jekyll development setup! What a total and complete mess. This is even better than that time they updated the C++ compiler to Clang without warning in a point release. After an hour or so I have managed to successfully invoke `rails new ...` and get a working demo, and the Jekyll bundle that drives the local version of this blog is, once again, working. I'm sure I'll find more as I go along.

I don't even remember exactly what I did, but it involved much custom tweaking based on experimentation and reading StackOverflow articles. Be wary of anyone who says "all you have to do is ..." regarding this! I might still have a weird problem where some of the "shimmed" rbenv executables overlap with the local copy of the Ruby Gem executables I have in `~/bin`. It's still very much a disaster, but a very slow-moving one.

I'll have to sit down and sort out how to rationalize the stuff in `.rbenv`, `.gemrc`, and `.gem` at some point, I'm _rawther_ sure.
