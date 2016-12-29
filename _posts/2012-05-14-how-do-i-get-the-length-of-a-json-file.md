---
id: 189
title: How do I get the length of a JSON file?
date: 2012-05-14T18:37:55+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=189
permalink: /blog/20120514/how-do-i-get-the-length-of-a-json-file/
categories:
  - Web Development
tags:
  - Javascript
---
First, you&#8217;ll have to [create a properly formatted JSON file](http://www.iamchristinabot.com/blog/category/web-development/javascript/). Once you&#8217;re done with that, getting the current number of objects from that list is a piece of cake.

    <script>
    $.getJSON('json/myjsonfile.json',function(data){
    var json = data;
    alert(json.length);
    });
    </script>


Pull in the feed via getJSON function, toss it into a variable (I called mine json) and grab the length with .length. My example alerts the number of entries but you can do what ever you&#8217;d like.
