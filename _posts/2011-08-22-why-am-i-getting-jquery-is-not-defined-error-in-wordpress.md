---
id: 140
title: 'Why am I getting &#8220;jQuery is not defined&#8221; Error in WordPress?'
date: 2011-08-22T22:59:38+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=140
permalink: /blog/20110822/why-am-i-getting-jquery-is-not-defined-error-in-wordpress/
categories:
  - Web Development
tags:
  - Bugs, Ew!
  - WordPress
  - jQuery
  - JavaScript
---
It sounds like your script is being loaded before jQuery, a couple of things will help you fix this:

First, you&#8217;ll want jQuery to recognize the $ shortcut so open up your .js file. I&#8217;m naming mine main.js and this bit of code:


    jQuery(document).ready(function($){
       $('#hover-bullet1').mouseover(function() {
         $('#bullet-details1').removeClass('pretty-hide');
         $('#bullet-details1').addClass('pretty-hover');
       });
    });



**Note:** Look at the first line closely, you want the to include the $ in the function.

* * *

Next, load in your file AFTER jQuery has finished loading, here&#8217;s how:

**Open header.php** from your theme folder.

**Search for wp_head();**

**Add your script tag** _AFTER_ the php close tag that looks like this: ?>


    ...
       wp_head();
    ?>
    &#60;script type="text/javascript" src="&#60;?php bloginfo("template_url"); ?>/js/main.js">&#60;/script>



Hope that helps!
