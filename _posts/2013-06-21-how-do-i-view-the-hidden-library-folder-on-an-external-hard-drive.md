---
id: 221
title: How do I view the hidden Library folder on an external hard drive?
date: 2013-06-21T05:08:53+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=221
permalink: /blog/20130621/how-do-i-view-the-hidden-library-folder-on-an-external-hard-drive/
categories:
  - Web Development
tags:
  - Mac OS X
---
I couldn&#8217;t figure out how to view the hidden user library folder on Mountain Lion, part of the reason why is because there is a space in the name of my external hard drive. Having a space in the name is ok, here&#8217;s how I finally got it to work.

1. Open Terminal.

2. Type chflags nohidden

3. (Leave a space after nohidden)

4. Drag the user directory from Finder to your terminal window.

5. Add /Library to the end of the folder structure.

6. Hit Enter.

Result:

chflags nohidden /Volumes/DRIVENAME/Users/YOURNAME/Library

Ah! Success!
