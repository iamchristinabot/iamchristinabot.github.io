---
id: 163
title: Count Number of List Items with jQuery
date: 2012-01-17T21:20:01+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=163
permalink: /20120117/count-number-of-list-items-with-jquery/
categories:
  - Javascript
---
So you want to know how many items are in that list:

<pre>&lt;ul id="imagelist"&gt;
	&lt;li&gt;Image 1&lt;/li&gt;
	&lt;li&gt;Image 2&lt;/li&gt;
&lt;/ul&gt;</pre>

&nbsp;

Make sure you&#8217;ve got the jQuery libaray running and run the following lines after page load.

    $(document).ready(function(){
    alert($("#imagelist li").size());
    });