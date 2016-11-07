---
id: 111
title: How do I delete a MySQL database?
date: 2011-07-24T14:32:13+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=111
permalink: /blog/20110724/how-do-i-delete-a-mysql-database/
categories:
  - MySQL
  - 'Web Development'
---
To delete a database, open terminal and login to your MySQL, if you don&#8217;t have a password leave it blank. If your default user isn&#8217;t ROOT you&#8217;ll want to change that to your id =]


    mysql -u root -p YOURPASSWORD
    drop database DATABASENAME;



Note: don&#8217;t forget your semicolon and be careful!
