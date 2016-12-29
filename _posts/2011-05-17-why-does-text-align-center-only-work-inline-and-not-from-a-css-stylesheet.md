---
id: 70
title: Why does text-align center only work inline and not from a css stylesheet?
date: 2011-05-17T17:26:52+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=70
permalink: /blog/20110517/why-does-text-align-center-only-work-inline-and-not-from-a-css-stylesheet/
categories:
  - Web Development
tags:
  - 'HTML &amp; CSS'
---
I started thinking I was crazy when my text-align center worked inline but not when I added it to the stylesheet, this was due to the order in which the CSS loaded. The center property was being over-written by a left property somewhere else so adding !important fixed it right up.


    .center{text-align:center !important;}
