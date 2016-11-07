---
id: 17
title: How do I create a global variable with Javascript?
date: 2011-04-08T20:09:54+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=17
permalink: /blog/20110408/how-do-i-create-a-global-variable-with-javascript/
categories:
  - Javascript
  - 'Web Development'
---
**Global Variable vs. Local Variable**

Global variable means the data it holds can be referenced from anywhere in the document, whereas local means the variable data can only be referenced from inside the function it was created in.

**The Short Answer**

Move the variable declaration outside of your function and add the word &#8220;var&#8221; in front of it.


    var a = "Global Variable";
    displayVariable();
    function displayVariable()
       {
       var a = "Local Variable";
       alert(a);
       }
    alert(a);



In executing this code you&#8217;ll see that the variable &#8220;a&#8221; contains two separate values &#8220;Global Variable&#8221; and &#8220;Local Variable&#8221;. The alert function in displayVariable will display the local variable first, if it doesn&#8217;t find it then it will check for the global variable.

So if your code is written properly but Javascript still won&#8217;t recognize your variable it&#8217;s possible that you need a global declaration, happy coding!
