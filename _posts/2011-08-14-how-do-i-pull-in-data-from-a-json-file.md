---
id: 136
title: How do I pull in data from a JSON file?
date: 2011-08-14T16:28:25+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=136
permalink: /20110814/how-do-i-pull-in-data-from-a-json-file/
categories:
  - Javascript
---
Now that you&#8217;ve [created a JSON file](http://www.iamchristinabot.com/blog/category/web-development/javascript/), you&#8217;ll want to use that data somewhere.

Using JavaScript JQuery, pull in data using the getJSON function. In the parenthesis put the location of your file and a variable where you&#8217;ll store the contents of the JSON, I called mine &#8220;data&#8221;.

In this example I&#8217;m pulling in a specific object from the file, data[0] which is the first object on the list and filling an given div (with the ID &#8220;container&#8221;) with some HTML.

    
    &#60;script>
    $.getJSON('json/myjsonfile.json',function(data){
    	$('#container').html([
    	  '&#60;div class="heading">'+data[0].title+'&#60;/div>',
    	  '&#60;div>',
    	    '&#60;img src="'+data[0].image+'" style="width:150px; height:100px;"/>',
    	  '&#60;/div>'
    	].join(''));
    });
    &#60;/script>
    
    

**Note:** The last line of your javascript containing HTML should not have a comma.
  
**Note:** Make sure your HTML has a container to receive the JSON data.

For more detailed documentation, [head over to the jQuery API](http://api.jquery.com/jQuery.getJSON/).