---
id: 22
title: How do I include one HTML file in a another with HTML includes.
date: 2011-03-22T19:10:47+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=22
permalink: /20110322/how-do-i-include-one-html-file-in-a-another-html-includes/
categories:
  - 'HTML &amp; CSS'
---
I recently used HTML (Server Side) Includes to convert an old iFrame site into a table-less iframe-less site. Here&#8217;s a quick bit on how to do this.

You can place the following code where you&#8217;d like the file to appear.
  
If the file you want to include is in the same directory, include with &#8220;file&#8221; parameter.

    
    <!--#include file="header.htm" -->
    
    

When the file you want to include is in a different directory, you can include with &#8220;virtual&#8221;.

    
    <!--#include virtual="includes/header.htm" -->
    
    

**Note:** Make sure there is a single space after the quoted file name, there is no equivalent space in the beginning of the line.

* * *

**Why didn&#8217;t that work?**
  
If the site does not render for you in your working/production environment you&#8217;ll need to check a few things. Here are two things you can test.</p> 

**Is Apache running on your server?**
  
Try uploading an html file to your hosting space with the following code.

    
    <!--#config timefmt="%A" --> <!--#echo var="DATE_LOCAL" -->
    
    

Load the page in your browser, if you see the date & time, you are running apache.

**Do you have Apache running on your local machine?**
  
You should install something like [MAMP](http://www.mamp.info/en/index.html).

**Does your server require .shtml files?**
  
Try renaming the included file extension to .shtml and change the include code to .shtml

**Is your Apache configured to parse for Server Side Includes?**
  
You may have to manually configure Apache to look for SSI, you can do this by editing/adding a .htaccess file.

If your root folder doesn&#8217;t have a .htaccess file, you&#8217;ll need to create one with a blank text file. Here&#8217;s what I did:

    
    AddType text/html .html .htm
    AddHandler server-parsed .html .htm
    
    DirectoryIndex index.htm
    
    

First two lines configures .htaccess to parse .html and .htm for SSI &#8211; if you&#8217;re using .shtml files you&#8217;ll want to change the code to reflect that. The third line sets my website default page to be index.htm &#8211; you may have to do the same.

Just a warning that changing Apache to parse all of your html files will have some effect on your site performance. In addition, editing the .htaccess can do some funny things to your server if not configured properly, so be sure to test in a sub-directory and be ready to remove the file right away since it might cause a server error. Good Luck!