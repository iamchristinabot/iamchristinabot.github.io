---
id: 68
title: 'Why isn&#8217;t my CSS class working in hover or active state of a link?'
date: 2011-05-14T03:18:10+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=68
permalink: /blog/20110514/why-isnt-my-css-class-working-in-hover-or-active-state-of-a-link/
categories:
  - Bugs, Ew!
  - 'HTML &amp; CSS'
  - 'Web Development'
---
One of the reasons your active or hover state isn&#8217;t working is because there is actually a particular order for pseudo-classes (link, visited, hover, active) in CSS. If they aren&#8217;t in the proper order, they won&#8217;t work.

This seems to be the shortest way to put it:


    .footer a:link { text-decoration:none; color:#737373;}
    .footer a:visited{ text-decoration:none; color:#737373;}
    .footer a:hover{ text-decoration:underline; color:#0095e0;}
    .footer a:active{ text-decoration:none; color:#FFFFFF;}



**Note:** a:hover MUST come after a:link & a:visited.

**Note:** a:active MUST come after a:hover.

It&#8217;s kind of a bummer for pseudo-classes to work this way because it seems like more code than it needs to be. I typically only use the link and the hover, so even though I define active link it doesn&#8217;t do anything and I only have two lines of CSS.


    .footer a:link, .footer a:active, .footer a:visited {text-decoration:none; color:#737373;}
    .footer a:hover{ text-decoration:underline; color:#0095e0;}



Feel free to comment if you have a better method.
