---
id: 144
title: How do I create a 301 redirect with PHP?
date: 2011-09-02T21:02:36+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=144
permalink: /blog/20110902/how-do-i-create-a-301-redirect-with-php/
categories:
  - Web Development
tags:
  - 'HTML &amp; CSS'
  - PHP
---
For old HTML files I&#8217;d typically create a 301 permanent redirect with apache by editing the .htaccess however when that isn&#8217;t an option, I use a meta redirect in the head tag like so:


    &#60;head>
        &#60;meta http-equiv="refresh" content="3; URL=http://iamchristinabot.com">
    &#60;/head>



If your old files are PHP extensions, you&#8217;re in luck, because the following method is better since it notifies search engines of a permanent redirect and moves your user to the new page. Editing the .htaccess file sometimes gives me the heebie jeebies and so this is my preferred method.


    &#60;?php
      header ('HTTP/1.1 301 Moved Permanently');
      header ('Location: http://www.newurl.com');
    ?>
