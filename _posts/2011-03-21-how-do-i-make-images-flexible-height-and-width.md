---
id: 23
title: How do I make images flexible height and width?
date: 2011-03-21T18:00:20+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=23
permalink: /20110321/how-do-i-make-images-flexible-height-and-width/
categories:
  - 'HTML &amp; CSS'
---
This is easy stuff.

    img { max-width:100%; }

This idea was originally experimented on by [Richard Rutter](http://clagnut.com/sandbox/imagetest3/) has proven to be very helpful, well for me at least. Basically, an image will load in at 100% of the browser width, unless the browser width is smaller than the image, in which case it loads in at the max-width of the browser. Fluid images!

Unfortunately not supported in IE but I believe appending targeted IE code will work out fine.

    img {
        max-width:100%;
        *width: 100%; 
    }

I&#8217;ve used this code on my home page light box to view large images of my work [here](http://iamchristinabot.com) &#8211; try resizing your browser.