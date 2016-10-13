---
id: 16
title: How do I define multiple CSS attribues in JQuery?
date: 2011-03-18T20:57:51+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=16
permalink: /20110318/how-do-i-define-multiple-css-attribues-in-jquery/
categories:
  - 'HTML &amp; CSS'
  - Javascript
---
You can string up your classes this way.

    
    $("#message").css("width", "450px").css("height", "100px");
    
    

&#8230; this gets old real fast, this way is more effective.

    
    $("#message").css( {width : '450px', height : '100px'} );