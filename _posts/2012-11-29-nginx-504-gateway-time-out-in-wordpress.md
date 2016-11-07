---
id: 213
title: Nginx 504 Gateway Time-out in WordPress
date: 2012-11-29T06:06:08+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=213
permalink: /blog/20121129/nginx-504-gateway-time-out-in-wordpress/
categories:
  - Errors
  - PHP
  - WordPress
  - 'Web Development'
---
I got this error after changing a template on one of the pages on my local machine, but as it turns out, the template had nothing to do with the time-out. It was just a delayed reaction. Some things I immediately tried was restarting nginx and also increasing the PHP memory cache to 64MB but neither thing worked.

The reason I received the error was because I duplicated the theme folder to have a backup and it was clogging up my WordPress setup. After I removed the duplicate theme, everything went back to normal. I&#8217;m glad that turned out to be an easy fix.
