---
id: 169
title: How do I get an image to float on my website even when scrolling?
date: 2012-01-19T03:10:37+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=169
permalink: /blog/20120119/how-do-i-get-an-image-to-float-on-my-website-even-when-scrolling/
categories:
  - Web Development
tags:
  - 'HTML &amp; CSS'
---
First you&#8217;ll want to put a DIV somewhere on your page and give it a class, for my example I&#8217;m going to call it floatingbanner.

So, our HTML will look like this:

     <div class="floatingbanner"> <!-- Banner Appears Here --> </div>

Then we drop in some CSS, setting the image as a centered background and give the div positioning properties so that it&#8217;s fixed at 0px from the bottom of the browser window:

    .floatingbanner{
     background:transparent url(../images/floatingimage.png) no-repeat scroll top center;
     bottom:0;
     left:0px;
     position:fixed;
     width:100%;
     z-index:9999;
     height:80px;
    }

Here&#8217;s what it looks like:

<img src="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2012/01/image-floating-in-browser-window.png" alt="" title="image floating in browser window" width="645" height="268" class="aligncenter size-full wp-image-171" srcset="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2012/01/image-floating-in-browser-window.png 645w, {{ site.url | prepend: site.baseurl }}/wp-content/uploads/2012/01/image-floating-in-browser-window-300x124.png 300w" sizes="(max-width: 645px) 100vw, 645px" />
