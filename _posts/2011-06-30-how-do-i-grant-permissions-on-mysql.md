---
id: 90
title: How Do I Grant Permissions on MySQL?
date: 2011-06-30T22:56:48+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=90
permalink: /20110630/how-do-i-grant-permissions-on-mysql/
categories:
  - MySQL
---
Open Terminal

    
    mysql -u root {PRESS ENTER}
    
    

Login to MySQL with your username, in my case it&#8217;s root.

    
    mysql> show grants for 'root'@'localhost'; 
    
    +--------------------------------------------------------------+
    | Grants for root@localhost                                                                           |
    +--------------------------------------------------------------+
    | GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost' WITH GRANT OPTION   |
    | GRANT ALL PRIVILEGES ON `database1`.* TO 'root'@'localhost'                  |
    | GRANT ALL PRIVILEGES ON `database2`.* TO 'root'@'localhost'                  |
    +--------------------------------------------------------------+
    3 rows in set (0.00 sec)
    
    
    

View current privileges of my user (root) to databases installed in MySQL.

    
    mysql> grant all on database1.* to 'root'@'localhost';
    mysql> use database1;
    
    

Grant permissions to my user for a specific database (database1).

    
    mysql> -u root -e"flush privileges";
    
    

Reset privileges. Done.