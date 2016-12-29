---
id: 117
title: How do I create a new database and import .SQL file?
date: 2011-07-24T14:58:55+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=117
permalink: /blog/20110724/how-do-i-create-a-new-database-and-import-sql-file/
categories:
  - Web Development
tags:
  - MySQL
---
Open Terminal & Login.

If you don&#8217;t have a password, leave it off like I did.


    mysql -u root {PRESS ENTER}
    mysql> create database iamchristinabot; {PRESS ENTER}
    Query OK, 1 row affected (0.00 sec)



Now I&#8217;ve got a spot to drop in a new database, exit out of mySQL and back to your command prompt.


    mysql -u root iamchristinabot < Downloads/iamchristinabot.sql



MYSQL LOGIN DATABASENAME < LOCATION/OF/DATABASE.sql If nothing happens after that, you did it right! That's it!
