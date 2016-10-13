---
id: 15
title: Can a span have a width?
date: 2011-03-18T03:52:53+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=15
permalink: /20110318/can-a-span-have-a-width/
categories:
  - 'HTML &amp; CSS'
---
**Yes.** Since a span tag is an inline element and it has &#8220;display:inline&#8221; as default, it doesn&#8217;t naturally have a width.

If you want to apply a width to a span you&#8217;ll have to change the display property to either inline-block & inline (for ie) and then add a width.

    
    span { display:inline-block; width:200px; }
    *html span { display:inline; }
    
    

Adding a float to the span also changes the display property so you can set a width that way too.

    
    span { float:left; width:200px; }