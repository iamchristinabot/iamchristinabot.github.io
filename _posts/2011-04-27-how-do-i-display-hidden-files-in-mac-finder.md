---
id: 60
title: 'How do I display hidden files in Mac &#8211; Finder?'
date: 2011-04-27T18:42:54+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=60
permalink: /blog/20110427/how-do-i-display-hidden-files-in-mac-finder/
categories:
  - Mac OS X
  - Work Life
---
To turn on hidden files in finder, open Terminal and paste the following:


    defaults write com.apple.finder AppleShowAllFiles -bool true



To restart Finder from command line, type:


    killall Finder



When it restarts you&#8217;ll see all your hidden files with a prefix of &#8220;.&#8221;

To turn hidden files off, open terminal and paste this:


    defaults write com.apple.finder AppleShowAllFiles -bool false
