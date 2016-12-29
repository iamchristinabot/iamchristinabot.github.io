---
id: 96
title: How can I make textarea grow without breaking the horizontal layout?
date: 2011-05-30T19:58:41+00:00
author: admin
layout: post
guid: http://www.iamchristinabot.com/blog/?p=96
permalink: /blog/20110530/how-can-i-make-textarea-grow-without-breaking-the-horizontal-layout/
categories:
  - Web Development
tags:
  - Javascript
---
Depending on the audience, letting users resize an input box isn&#8217;t always the best option, in addition, resizing in any direction can break a layout. That&#8217;s why I prefer [this auto-resizing jQuery plugin](http://plugins.jquery.com/project/autogrowtextarea)

Call the function at the bottom of your page.


    $(document).ready(function(){
      $("#message").autoGrow();
    });




    /*!
     * Autogrow Textarea Plugin Version v2.0
     * http://www.technoreply.com/autogrow-textarea-plugin-version-2-0
     *
     * Copyright 2011, Jevin O. Sewaruth
     *
     * Date: March 13, 2011
     */
    jQuery.fn.autoGrow = function(){
    	return this.each(function(){
    		// Variables
    		var colsDefault = this.cols;
    		var rowsDefault = this.rows;

    		//Functions
    		var grow = function() {
    			growByRef(this);
    		}

    		var growByRef = function(obj) {
    			var linesCount = 0;
    			var lines = obj.value.split('\n');

    			for (var i=lines.length-1; i>=0; --i)
    			{
    				linesCount += Math.floor((lines[i].length / colsDefault) + 1);
    			}

    			if (linesCount >= rowsDefault)
    				obj.rows = linesCount + 1;
    			else
    				obj.rows = rowsDefault;
    		}

    		var characterWidth = function (obj){
    			var characterWidth = 0;
    			var temp1 = 0;
    			var temp2 = 0;
    			var tempCols = obj.cols;

    			obj.cols = 1;
    			temp1 = obj.offsetWidth;
    			obj.cols = 2;
    			temp2 = obj.offsetWidth;
    			characterWidth = temp2 - temp1;
    			obj.cols = tempCols;

    			return characterWidth;
    		}

    		// Manipulations
    		this.style.width = "auto";
    		this.style.height = "auto";
    		this.style.overflow = "hidden";
    		this.style.width = ((characterWidth(this) * this.cols) + 6) + "px";
    		this.onkeyup = grow;
    		this.onfocus = grow;
    		this.onblur = grow;
    		growByRef(this);
    	});
    };



Let the above jQuery code do the rest of the work.

[Source](http://plugins.jquery.com/project/autogrowtextarea)
