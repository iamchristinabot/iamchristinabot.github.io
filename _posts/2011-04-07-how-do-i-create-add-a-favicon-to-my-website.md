---
id: 26
title: 'How do I create &#038; add a favicon to my website?'
date: 2011-04-07T19:46:11+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=26
permalink: /blog/20110407/how-do-i-create-add-a-favicon-to-my-website/
categories:
  - Web Development
tags:
  - 'HTML &amp; CSS'
---
There are two ways to do this.

**My Preferred Method**

1. Create an image with the same width & height, resize image to 16&#215;16 pixels.

2. In Photoshop, File-> Save for Web as a PNG-24, check Transparent if you want to.

3. Add this bit to your **<head>** tag.


    <link rel="icon" href="favicon.png" type="image/png" />



**The Other Way**

I usually create a .ico as a backup anyway, but the previous method works just fine. I like to use <a href="http://tools.dynamicdrive.com/favicon/" target="_blank"><em>Dynamic Drive Favicon Generator</em></a>. If you take this route you&#8217;ll want to use this code in your **<head>** tag instead.


    <link rel="icon" href="favicon.ico" type="image/x-icon" />
    <link rel="shortcut icon" href="favicon.ico" type="image/x-icon" />



For examples of favicon design, <a href="http://www.smashingmagazine.com/2007/01/31/inspire-yourself-50-remarkable-favicons/" target="_blank">check out <em>Smashing Magazine</em></a>.

If my code helped you out, I&#8217;d like to know, please leave comments below (no registration needed).
