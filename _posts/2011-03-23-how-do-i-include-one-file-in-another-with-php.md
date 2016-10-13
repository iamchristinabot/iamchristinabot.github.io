---
id: 25
title: How do I include one file in another with PHP?
date: 2011-03-23T23:00:18+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=25
permalink: /20110323/how-do-i-include-one-file-in-another-with-php/
categories:
  - PHP
---
This is my favorite approach to including one file in another, but it means your server has to be running PHP and all of your file names need to be named .php instead of .html. If you&#8217;re not sure if your web hosting runs PHP you&#8217;ll have to check with them otherwise you can follow these instructions to see if it works.

    
    <?php 
         include("includes/header.php"); 
    ?>
    
    

Create a directory called includes and put all the files you would want to include in there. Make sure the file calling the include is a .php extension. In order to see php on your local machine you&#8217;ll have to have PHP running on your web server, you can use [MAMP](http://www.mamp.info/en/index.html) for this.