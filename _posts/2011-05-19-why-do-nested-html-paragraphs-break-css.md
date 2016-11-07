---
id: 75
title: Why do nested html paragraphs break CSS?
date: 2011-05-19T22:45:23+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=75
permalink: /blog/20110519/why-do-nested-html-paragraphs-break-css/
categories:
  - 'HTML &amp; CSS'
  - 'Web Development'
---
I tried something silly today&#8230; to find that it didn&#8217;t work, here&#8217;s what:


    <p>
         <p>Title</p>
         <p>Description</p>
    </p>



I thought that by nesting p-tags I would have text that was indented much like a blockquote but with my p-tag CSS attributes. It didn&#8217;t work because before CSS styles can be applied, the HTML has to be valid and as it turns out, nested paragraphs are not possible because when an HMTL parser sees two p-tags it interprets them as 2 paragraphs following each other, extra closed p-tags are ignored as errors. **Do not do this.**
