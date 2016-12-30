---
id: 112
title: 'Fix for ERROR 1049 (42000): Unknown database&#8230;'
date: 2011-07-24T14:51:43+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=112
permalink: /blog/20110724/fix-for-error-1049-42000-unknown-database/
categories:
  - Web Development
tags:
  - MySQL
---
I was trying to import a new database but kept getting this error ERROR 1049 (42000): Unknown database &#8216;MYDATABASE&#8217;, finally got it fixed&#8230; the error wasn&#8217;t with the syntax it was how I exported my database.

When I exported my database from phpmyadmin, I selected the main database rather than the individual tables. So in phpMyAdmin you&#8217;ll want to click on your database in the left column first.

<img src="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/07/Screen-shot-2011-07-24-at-10.38.05-AM.png" alt="" title="Screen shot 2011-07-24 at 10.38.05 AM" width="202" height="175" class="aligncenter size-full wp-image-113" />

Then click **Export** along the top tabs.

[<img src="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/07/Screen-shot-2011-07-24-at-10.44.07-AM.png" alt="" title="Export MySQL" width="629" height="254" class="aligncenter size-full wp-image-115" srcset="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/07/Screen-shot-2011-07-24-at-10.44.07-AM.png 629w, {{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/07/Screen-shot-2011-07-24-at-10.44.07-AM-300x121.png 300w" sizes="(max-width: 629px) 100vw, 629px" />]({{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/07/Screen-shot-2011-07-24-at-10.44.07-AM.png)

**Select All** tables in the database.

<img src="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/07/Screen-shot-2011-07-24-at-10.48.15-AM.png" alt="" title="Select all Databases in phpMyAdmin" width="287" height="200" class="aligncenter size-full wp-image-116" />

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

<img src="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.37.11-PM.png" alt="" title="Screen shot 2011-05-29 at 10.37.11 PM" width="583" height="403" class="aligncenter size-full wp-image-94" srcset="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.37.11-PM.png 583w, {{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.37.11-PM-300x207.png 300w" sizes="(max-width: 583px) 100vw, 583px" />

* * *

**Check off the box &#8220;Save As File&#8221;** and give your file a name, I like to use an uncompressed version of my database so I&#8217;m going to select &#8220;none&#8221; for that.

<img src="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.44.12-PM.png" alt="" title="Screen shot 2011-05-29 at 10.44.12 PM" width="487" height="93" class="aligncenter size-full wp-image-95" srcset="{{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.44.12-PM.png 487w, {{ site.url | prepend: site.baseurl }}/wp-content/uploads/2011/05/Screen-shot-2011-05-29-at-10.44.12-PM-300x57.png 300w" sizes="(max-width: 487px) 100vw, 487px" />

Press &#8220;Go&#8221; and you&#8217;ll see the SQL file start to download.
