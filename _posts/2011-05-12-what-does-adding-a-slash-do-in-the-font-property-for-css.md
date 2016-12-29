---
id: 67
title: What does adding a slash do in the font property for CSS?
date: 2011-05-12T19:49:52+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=67
permalink: /blog/20110512/what-does-adding-a-slash-do-in-the-font-property-for-css/
categories:
  - Web Development
tags:
  - 'HTML &amp; CSS'
---
This is actually a shorthand for font size (first metric) and line-height (second metric) and font-family.


    font: 12px/16px "Times", serif;



&#8230; is the same as&#8230;


    font-size: 12px;
    line-height: 16px;
    font-family: "Times", serif;



**Notes**

&#8211; In order to use this shortcut you **must have the size, line height AND font-family specified** or it will not work.

&#8211; This shorthand works in all modern browsers, but not in emails.
