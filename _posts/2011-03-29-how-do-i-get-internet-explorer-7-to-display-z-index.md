---
id: 38
title: How do I get Internet Explorer 7 to display z-index ?
date: 2011-03-29T18:55:06+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=38
permalink: /blog/20110329/how-do-i-get-internet-explorer-7-to-display-z-index/
categories:
  - Web Development
tags:
  - Bugs, Ew!
  - 'HTML &amp; CSS'
---
The ticker bar lower shadow displayed perfectly in Safari, Chrome & Firefox, but IE didn&#8217;t show it.

[<img src="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/03/Screen-shot-2011-03-29-at-2.47.55-PM-1024x309.png" alt="" title="Screen shot 2011-03-29 at 2.47.55 PM" width="480" height="144" class="aligncenter size-large wp-image-40" srcset="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/03/Screen-shot-2011-03-29-at-2.47.55-PM-1024x309.png 1024w, {{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/03/Screen-shot-2011-03-29-at-2.47.55-PM-300x90.png 300w, {{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/03/Screen-shot-2011-03-29-at-2.47.55-PM.png 1108w" sizes="(max-width: 480px) 100vw, 480px" />]({{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/03/Screen-shot-2011-03-29-at-2.47.55-PM.png)

It looked cut off like this:

[<img src="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/03/Screen-shot-2011-03-29-at-2.41.09-PM-1024x377.png" alt="" title="Screen shot 2011-03-29 at 2.41.09 PM" width="480" height="176" class="aligncenter size-large wp-image-39" srcset="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/03/Screen-shot-2011-03-29-at-2.41.09-PM-1024x377.png 1024w, {{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/03/Screen-shot-2011-03-29-at-2.41.09-PM-300x110.png 300w, {{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/03/Screen-shot-2011-03-29-at-2.41.09-PM.png 1050w" sizes="(max-width: 480px) 100vw, 480px" />]({{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/03/Screen-shot-2011-03-29-at-2.41.09-PM.png)

To get IE to display z-index, **you have add positioning and z-index to the parent container**. I added a lower and higher z-index and both seemed to display just fine in IE7.


    #jumpinconsole{
      width:100%;
      position:relative;
      height: 115px;
      overflow:visible;
      <span class="green">z-index:2000;</span>
    }

    #jumpinconsole .console_counter{
        padding:25px 0px 0px 0px;
        background-image:url(/images/background_fancalculator2.png);
        background-repeat:repeat-x;
        position:absolute;
        width:100%;
        top:-20px;
        left:0px;
        z-index:1000;
        height:145px;
      }
