---
id: 91
title: How do I export a database using phpMyAdmin?
date: 2011-05-30T03:11:40+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=91
permalink: /20110530/how-do-i-export-a-database-using-phpmyadmin/
categories:
  - MySQL
---
Everyone&#8217;s setup is different so first you&#8217;ll have to get to the phpMyAdmin section on your web hosting server. With Dreamhost it was easy, under &#8220;Goodies&#8221; click &#8220;MySQL Databases&#8221; and then in the right column you&#8217;ll see a link for PHPMyAdmin, click that and login.

When you&#8217;re there, you&#8217;ll see an &#8220;Export&#8221; tab at the top.
  
<img src="http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.28.03-PM.png" alt="" title="Screen shot 2011-05-29 at 10.28.03 PM" width="328" height="62" class="aligncenter size-full wp-image-92" srcset="http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.28.03-PM.png 328w, http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.28.03-PM-300x56.png 300w" sizes="(max-width: 328px) 100vw, 328px" />

* * *

Click the database you want to export, **do not select information_schema** unless you want to overrite your default MySQL database, which isn&#8217;t recommended.
  
<img src="http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.33.41-PM.png" alt="" title="Screen shot 2011-05-29 at 10.33.41 PM" width="251" height="118" class="aligncenter size-full wp-image-93" />

* * *

**Check off the box for Structure** and the following:
    
Add DROP TABLE / VIEW / PROCEDURE / FUNCTION / EVENT
    
Add IF NOT EXISTS
    
Add AUTO_INCREMENT value
    
Enclose table and field names with backquotes

**Check the box for data** and the following:
    
Complete inserts
    
Extended inserts
    
Maximal length of created query
    
Use hexadecimal for BLOB

Select &#8220;Insert&#8221; from drop box.

<img src="http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.37.11-PM.png" alt="" title="Screen shot 2011-05-29 at 10.37.11 PM" width="583" height="403" class="aligncenter size-full wp-image-94" srcset="http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.37.11-PM.png 583w, http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.37.11-PM-300x207.png 300w" sizes="(max-width: 583px) 100vw, 583px" />

* * *

**Check off the box &#8220;Save As File&#8221;** and give your file a name, I like to use an uncompressed version of my database so I&#8217;m going to select &#8220;none&#8221; for that.
  
<img src="http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.44.12-PM.png" alt="" title="Screen shot 2011-05-29 at 10.44.12 PM" width="487" height="93" class="aligncenter size-full wp-image-95" srcset="http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.44.12-PM.png 487w, http://www.iamchristinabot.com/blog/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.44.12-PM-300x57.png 300w" sizes="(max-width: 487px) 100vw, 487px" />

Press &#8220;Go&#8221; and you&#8217;ll see the SQL file start to download.