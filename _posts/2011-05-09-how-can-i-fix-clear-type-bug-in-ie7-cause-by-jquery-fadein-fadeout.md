---
id: 65
title: 'How can I fix clear type bug in IE7 cause by JQuery fadeIn &#038; fadeOut?'
date: 2011-05-09T18:29:18+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=65
permalink: /20110509/how-can-i-fix-clear-type-bug-in-ie7-cause-by-jquery-fadein-fadeout/
categories:
  - Bugs, Ew!
---
Before fading completing fadeIn, remove the filter attribute but I can&#8217;t fix the filter on fadeOut. I&#8217;ve tried everything, I&#8217;m just not sure how to do it&#8230;

    
    fadeIn(function(){
         this.style.removeAttribute("filter");
    });