---
id: 162
title: IE Displays White Space Above and Below A-Tag and Linked Images
date: 2012-01-15T21:18:31+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=162
permalink: /blog/20120115/ie-displays-white-space-above-and-below-a-tag-and-linked-images/
categories:
  - Web Development
tags:
  - Bugs, Ew!
---
I recently made a gallery with a bunch of image thumbnails laid out in multiple rows, each one linked to the larger image but when I tested in IE7 I noticed some white space in between the rows.  The reason for this is that IE adds a default line-height of 16px, so if the images or navigation items or horizontal rules (whatever it may be) is smaller than that, you&#8217;ll have to manually set the css for this object like so:


    .thumbnail {line-height:1px; font-size:1px;}
