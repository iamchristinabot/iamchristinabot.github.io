---
id: 209
title: 'What is the Error: Cannot modify header information&#8230; in WordPress?'
date: 2012-10-07T22:28:32+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=209
permalink: /blog/20121007/what-is-the-error-cannot-modify-header-information-in-wordpress/
categories:
  - Web Development
---
**Warning**: Cannot modify header information &#8211; headers already sent by (output started at {PATH TO FUNCTIONS}:92) in **/home/content/17/9436817/html/wp-includes/pluggable.php** on line **881**

If you&#8217;re seeing this error when publishing your post on WordPress it is probably because you&#8217;ve got some whitespace before or after your PHP tags.  Check before and after to be sure there are no extra lines or spaces and re-upload your files.
