---
id: 59
title: How do I make my first git commit?
date: 2011-04-29T16:29:14+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=59
permalink: /blog/20110429/how-do-i-make-my-first-git-commit/
categories:
  - Web Development
tags:
  - Git
---
Started using git to backup for the code on my website, here&#8217;s how I made my first commit =]

In Terminal, navigate to your website directory.


    cd /your/directory/here



Once you&#8217;re there&#8230;


    git init
    git add .



Make your first commit and label it with a note on what you&#8217;re committing.


    git commit -m "My First Commit"



The -m is for message, make sure there is no space between the dash and the letter &#8220;m&#8221;.

If you botch it up, go to your web directory and delete the .git folder &#8211; if you don&#8217;t see one it&#8217;s because it&#8217;s hidden you&#8217;ll have to [turn on hidden folders, like this.](http://www.iamchristinabot.com/blog/20110427/how-do-i-display-hidden-files-in-mac-finder/)
