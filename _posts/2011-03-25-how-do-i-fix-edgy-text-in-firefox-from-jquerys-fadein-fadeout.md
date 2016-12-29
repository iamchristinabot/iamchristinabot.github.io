---
id: 28
title: 'How do I fix edgy text in FireFox from JQuery&#8217;s fadeIn() &#038; fadeOut?'
date: 2011-03-25T03:44:20+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=28
permalink: /blog/20110325/how-do-i-fix-edgy-text-in-firefox-from-jquerys-fadein-fadeout/
categories:
  - Web Development
tags:
  - Bugs, Ew!
  - Javascript
---
If you are noticing a problem with text appearing light, crunchy or edgy in FireFox while fading in and out, you&#8217;ve found the cleartype bug! You&#8217;ll have to remove the filter property from the DOM. Try this:


    document.getElementById("#container").style.removeAttribute("filter");



You&#8217;ll have to use after the fadeIn function is complete or in the function callback as follows:


    $("#container").fadeIn(  function() {
        this.style.removeAttribute( "filter" );
    });
