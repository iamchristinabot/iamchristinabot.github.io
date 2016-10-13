---
id: 167
title: How do I remove dotted lines around links in FireFox?
date: 2012-01-18T22:03:08+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=167
permalink: /20120118/how-do-i-remove-dotted-lines-around-links-in-firefox/
categories:
  - Bugs, Ew!
  - 'HTML &amp; CSS'
---
This can be done with CSS, you&#8217;ll need to change button to whatever class, tag or id you need to remove those dotted lines from.

    button:focus {outline: none;}
    button:focus {outline: none;}
    button::-moz-focus-inner {boder:0;}