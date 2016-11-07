---
id: 215
title: 'WordPress Plugin: Nivo Slider Loading Slow'
date: 2012-12-07T23:46:38+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=215
permalink: /blog/20121207/wordpress-plugin-nivo-slider-loading-slow/
categories:
  - WordPress
  - 'Web Development'
---
Nivo Slider is one of the best slider tools available for WordPress &#8230; until you&#8217;ve had too much fun and suddenly have too many images in it. So what do you do when Nivo Slider takes too long to load? Add a single line of CSS, hide any image that doesn&#8217;t need to be displayed initially.


    .nivoSlider img:not(:first-child) {display:none;}



Now, as you may know the [:not](http://www.w3schools.com/cssref/sel_not.asp) and [:first-child](http://www.w3schools.com/cssref/sel_firstchild.asp) selectors are CSS3 so anything before IE8 will still see long loading times.
