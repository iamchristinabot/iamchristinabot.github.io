---
id: 63
title: How do I remove the bullet in list items with CSS?
date: 2011-05-05T20:13:18+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=63
permalink: /blog/20110505/how-do-i-remove-the-bullet-in-list-items-with-css/
categories:
  - Web Development
tags:
  - 'HTML &amp; CSS'
---
Just when I thought I had removed the bullet&#8230; I found it still there in IE7. Best way to remove the stupid thing once and for all is to add list style type to both the UL and LI items.

I needed the list items to remain as block elements so here&#8217;s what I did for CSS.


      .press_wrap ul, .press_wrap li {
        list-style-type: none;
        margin-left: 0px;
        padding-left: 0px;
      }
