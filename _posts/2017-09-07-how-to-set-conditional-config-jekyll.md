---
id: 000
title: "How do I set up a conditional config with Jekyll?"
date: 2017-09-07T01:16:42+00:00
author: admin
layout: post
permalink: /blog/20170907/how-to-set-conditional-config-jekyll/
categories:
  - Web Development
tags:
  - Jekyll
---
I found that there are a few ways of getting your Jekyll environment to behave differently for development purposes. I would use the first method if I'm going to conditionally change a thing or two in my templates but if I needed to change any of the variables in my config file, I would say the second one has much more functionality.
<hr>

#### Method 1
This first example utilizes the Environment setting from the Jekyll documentation.

When you start your local server you can specify your JEKYLL_ENV as development and serve your site as usual.
<pre>
  JEKYLL_ENV=development jekyll serve
</pre>

Github pages will automatically set the production environment for you, but if you need to start your local dev in production after you've set development, you can then overwrite the environment variable.
<pre>
  JEKYLL_ENV=development jekyll serve
</pre>

You can use environment variables to do some convenient things like, conditionally load Google Analytics.
<pre>
&#123;% if jekyll.environment == "production" %}
&#60;script>
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','https://www.google-analytics.com/analytics.js','ga');

  ga('create', '{{ site.ga_track_id }}', 'auto');
  ga('send', 'pageview');

&#60;/script>
&#123;% endif %}
</pre>

<br>
<hr>
<br>

#### Method 2
This method uses the Configuration setting from the Jekyll documentation. It gives you the ability to customize a whole config file as opposed to just using conditionals in liquid templates.

You probably already have a _config.yml, if not, go ahead and create one with a param called environment and set it to production.

<pre>
environment: production
</pre>

Create another configuration and name it whatever you like, for this example I'll call it _config_dev.yml.

<pre>
environment: development
</pre>

When you fire up your server, overwrite your prod env with the dev one, so you'll want to run a command that looks like this:

<pre>
jekyll serve --config _config.yml,_config_dev.yml
</pre>

This method is useful if you want to change site variables that are specified in your config (like a test account number or paths to your assets). You can also use your new config variables to conditionally include code:

<pre>
&#123;% if site.environment == "dev" %}
  &#60;script>console.log("hey yah")</script>
&#123;% endif %}
&#123;% if site.environment == "production" %}
  &#60;script>console.log("hey nah")</script>
&#123;% endif %}
</pre>

<br>
For more information take a look at the Jekyll documentation:
[https://jekyllrb.com/docs/configuration/](https://jekyllrb.com/docs/configuration/)
