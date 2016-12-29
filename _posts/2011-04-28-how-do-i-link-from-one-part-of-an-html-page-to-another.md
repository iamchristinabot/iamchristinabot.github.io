---
id: 61
title: How do I link to from one part of an HTML page to another?
date: 2011-04-28T03:37:15+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=61
permalink: /blog/20110428/how-do-i-link-from-one-part-of-an-html-page-to-another/
categories:
  - Web Development
tags:
  - 'HTML &amp; CSS'
---
This would be called using an HTML anchor tag and there are two parts to doing this.

1. **Label your container with the &#8220;name&#8221; attribut**e, I&#8217;m going to call my section jump to, because I want to jump to it. :]


    <a name="jumpto">Jump to this line of text.</a>



2. Add a plain &#8216;ol HTML **link to your container**, using the # symbol + the name you gave in step 1.


    <a href="#jumpto">Click here to jump to your anchor.</a>



Now that you&#8217;ve created your first anchor tag, you can also link to your information from other pages like so.


    <a href="http://iamchristinabot.com/#jumpto">
         View your container through a link from another page, click here!
    </a>



You can even get fancy by wrapping images with your a tags.
