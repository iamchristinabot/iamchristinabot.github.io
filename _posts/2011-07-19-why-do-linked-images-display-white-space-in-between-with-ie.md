---
id: 45
title: Why do linked images display white space in between with IE7?
date: 2011-07-19T18:47:46+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=45
permalink: /blog/20110719/why-do-linked-images-display-white-space-in-between-with-ie/
categories:
  - Web Development
tags:
  - Bugs, Ew!
  - 'HTML &amp; CSS'
---
If you ever tried to display a row of linked images in a row, you may notice some white space in between them when viewing in Internet Explorer 7, this is because IE7 adds a default line-height of 16px which, in the case of seeing whitespace isn&#8217;t what you need.

**To fix this change the parent container&#8217;s line-height property to something like 1em.**
