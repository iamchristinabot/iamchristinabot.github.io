---
id: 76
title: Why do resized images in IE7 look pixelated?
date: 2011-05-20T18:54:30+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=76
permalink: /blog/20110520/why-do-resized-images-in-ie7-look-pixelated/
categories:
  - Bugs, Ew!
  - 'Web Development'
---
When using width or height properties to resize images, IE will render a dirty pixelated image unless you correct the rendering type with CSS.


    img{-ms-interpolation-mode: bicubic;}



**Note:** Works for IE7 +

* * *

Before:

<img src="http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-20-at-2.51.34-PM.png" alt="" title="Screen shot 2011-05-20 at 2.51.34 PM" width="595" height="303" class="aligncenter size-full wp-image-77" srcset="http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-20-at-2.51.34-PM.png 595w, http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-20-at-2.51.34-PM-300x152.png 300w" sizes="(max-width: 595px) 100vw, 595px" />

After:

<img src="http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-20-at-2.51.54-PM.png" alt="" title="Screen shot 2011-05-20 at 2.51.54 PM" width="598" height="305" class="aligncenter size-full wp-image-78" srcset="http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-20-at-2.51.54-PM.png 598w, http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-20-at-2.51.54-PM-300x153.png 300w" sizes="(max-width: 598px) 100vw, 598px" />
