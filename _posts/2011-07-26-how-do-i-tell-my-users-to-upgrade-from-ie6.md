---
id: 130
title: How do I kindly tell my users to upgrade from IE6?
date: 2011-07-26T20:17:50+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=130
permalink: /blog/20110726/how-do-i-tell-my-users-to-upgrade-from-ie6/
categories:
  - Web Development
tags:
  - 'HTML &amp; CSS'
---
It&#8217;s almost impossible to get every site working properly on IE6 and with the way it renders HTML & CSS what developer in their right mind would even want to try? I wrote a little HTML & CSS to target users on IE6, in hopes that some of them will upgrade to something a bit more current.

**HTML**


    &#60;div id="ie6_user">
      &#60;!--[if IE 6]>
      Looks like you're using Internet Explorer 6 but Headliner.fm does not support it.  For the best experience use &#60;a href="http://www.mozilla.com" target="_blank">FireFox&#60;/a> or &#60;a href="http://www.google.com/chrome" target="_blank">Chrome&#60;/a>.
      &#60;![endif]-->
    &#60;/div>



**CSS**


    #ie6_user{
      background-color:#f6f37d;
      color:black;
      border:1px solid #edc748;
      padding:10px 0px;
      text-align:center;
      font-size:14px;
    }



Here&#8217;s what it ends up looking like:

[<img src="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/07/Screen-shot-2011-07-26-at-4.11.36-PM-300x26.png" alt="" title="Target IE6" width="300" height="26" class="aligncenter size-medium wp-image-131" srcset="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/07/Screen-shot-2011-07-26-at-4.11.36-PM-300x26.png 300w, {{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/07/Screen-shot-2011-07-26-at-4.11.36-PM.png 948w" sizes="(max-width: 300px) 100vw, 300px" />]({{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/07/Screen-shot-2011-07-26-at-4.11.36-PM.png)
