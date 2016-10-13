---
id: 164
title: How do I block Google Analytics on my local machine/testing environment?
date: 2012-01-16T21:31:28+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=164
permalink: /20120116/how-do-i-block-google-analytics-on-my-local-machinetesting-environment/
categories:
  - Mac OS X
  - Web Development
---
You&#8217;ll need to add the google servers to your host file.

For Mac:
  
I manage mine with Gas Mask for Mac ([download](http://www.macupdate.com/app/mac/29949/gas-mask)):

You&#8217;ll need to add these two lines:
  
127.0.0.1 www.google-analytics.com
  
127.0.0.1 google-analytics.com
  
127.0.0.1 ssl.google-analytics.com

&nbsp;

If you&#8217;re on a PC:
  
Open your hosts file with a text editor to windows/system32/drivers/etc/hosts

You&#8217;ll need to add these two lines:
  
127.0.0.1 www.google-analytics.com
  
127.0.0.1 google-analytics.com
  
127.0.0.1 ssl.google-analytics.com

Restart your browser, especially if you&#8217;re using IE.