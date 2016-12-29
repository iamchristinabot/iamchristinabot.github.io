---
id: 24
title: How do I style a horizontal rule HR tag with CSS?
date: 2011-07-19T18:52:27+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=24
permalink: /blog/20110719/how-do-i-style-a-horizontal-rule-tag-with-css/
categories:
  - Web Development
tags:
  - 'HTML &amp; CSS'
---
Here&#8217;s how you can style the Horizontal Rule tag with CSS. Just a note, the default of an HR tag is 100% wide, 2px high (1px for line the and 1px for a border to give the line a 3D effect).


    hr{
      width: 100%;
      height: 1px;
      background: #DFDFDF;
      margin: 30px 0;
      display: block;
      border: none;
    }



I prefer to add borders to divs to create horizontal lines but there are situations where an HR tag is useful.
