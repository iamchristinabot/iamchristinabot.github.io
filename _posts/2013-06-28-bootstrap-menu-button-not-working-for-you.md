---
id: 223
title: Bootstrap menu button not working for you?
date: 2013-06-28T16:10:33+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=223
permalink: /blog/20130628/bootstrap-menu-button-not-working-for-you/
categories:
  - Web Development
tags:
  - Bootstrap
---
There&#8217;s a couple things you should know about the bootstrap menu icon, if it&#8217;s not working for you chances are one of these things is off.

In order to get it to show up, you will need to have it set in the appropriate tags. It needs to be sitting in a &#8220;navbar&#8221; class, followed by a &#8220;btn-navbar&#8221; class. In my example below, I&#8217;ve got a div called &#8220;navbar&#8221; and a button tag called &#8220;btn-navbar&#8221;. Once you have your structure nested properly, you&#8217;ll notice the css triggering from your bootstrap.css file.


    <div class="navbar navbar-inverse">
      <div class="navbar-inner">
        <button type="button" class="btn btn-navbar">
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </button>
      </div>
    </div>


If your menu button isn&#8217;t showing up at all, chances are because bootstrap is hiding it. I think the original purpose of this button was to display a condensed navigation menu on smaller screens and mobile devices&#8230; so it only shows when the viewing area is small, other times, it is hidden. Now that people want to use this menu on their full-size websites, we have to fight with bootstrap, just a little bit.

Add this to your CSS overrides:


    .navbar .btn-navbar {
         display: inline-block;
    }


If this blog was helpful, let me know on [Twitter](https://twitter.com/iamchristinabot).
