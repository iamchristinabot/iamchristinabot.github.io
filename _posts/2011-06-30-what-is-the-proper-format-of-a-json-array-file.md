---
id: 18
title: What is the proper format of a JSON Array file?
date: 2011-06-30T23:28:37+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=18
permalink: /blog/20110630/what-is-the-proper-format-of-a-json-array-file/
categories:
  - Web Development
tags:
  - Javascript
---
Well let&#8217;s start off by understanding what JSON is, JavaScript Object Notation. It&#8217;s a derivative of JavaScript that allows data to be passed between a server & a website in the form of objects. It&#8217;s similar to XML, except the JSON syntax is less invasive than XML and so it ends up having a bit of a smaller file size.

Below you&#8217;ll find a basic sample of a JSON array that has two objects.


    [
      {
        "title":"Name of Article 1",
        "image":"/images/press_article1.png",
        "timestamp":"March 2011"
      },
      {
        "title":"Name of Article 4",
        "image":"/images/press_article2.png",
        "timestamp":"March 2011"
      }
    ]



**Note:** There are no commas on the last line of each array.

There are many other structures of JSON files, I highly suggest checking out the <a href="http://en.wikipedia.org/wiki/JSON" target="_blank">wiki page</a> for other uses.
