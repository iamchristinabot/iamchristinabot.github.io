---
id: 89
title: How do I list databases in MySQL?
date: 2011-05-30T02:18:21+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=89
permalink: /blog/20110530/how-do-i-list-databases-in-mysql/
categories:
  - Web Development
tags:
  - MySQL
---
To list database type the following command

Open Terminal


    mysql {PRESS ENTER}
    mysql> show databases;



This is the output of my command, it only listed the mysql default database, not quite what I wanted to see.


    +--------------------+
    | Database           |
    +--------------------+
    | information_schema |
    | test               |
    +--------------------+



The reason my databases weren&#8217;t listed is because I wasn&#8217;t logged in as root so when logging in I typed -u root and if you have a password you&#8217;ll have to do that by adding -p yourpassword


    quit {PRESS ENTER}
    mysql -u root {PRESS ENTER}
    mysql> show databases; {PRESS ENTER}

    +--------------------------+
    | Database                 |
    +--------------------------+
    | information_schema       |
    | headliner            |
    | mysql                    |
    | test                     |
    +--------------------------+



Now I&#8217;m able to see all databases that I&#8217;ve installed.
