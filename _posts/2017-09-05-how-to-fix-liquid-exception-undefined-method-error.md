---
id: 000
title: "How do I fix Liquid Exception undefined method error?"
date: 2017-09-05T01:16:42+00:00
author: admin
layout: post
permalink: /blog/20170905/how-to-fix-liquid-exception-undefined-method-error/
categories:
  - Web Development
tags:
  - Jekyll
---

Went to start up my Jekyll server and got roadblocked by a little red error in my console. "Liquid Exception: undefined method 'has_key?'..." ...and then remembered I recently ran gem update that gave me a newer version of Jekyll that wasn't compatible with the code on my site. Rather than update my site, I decided to go get the last compatible version of Jekyll.

This command will show you all the gems you have with their versions, if you have too many you might want to grep for just the jekyll gems.

<pre>
$ gem list jekyll
</pre>

In my particular case, I had upgraded to 3.5.2 but needed 2.5.3, so I uninstalled the new one and reinstalled the old.

<pre>
$ gem uninstall jekyll --version 3.5.2
$ gem install jekyll --version 2.5.3
</pre>

All was well after that, however, I recommend using bundler to manage ruby Gems. You will need to create a Gemfile in your project where you can specify version numbers for each Gem.

For more information on using bundler visit their website:
[http://bundler.io/](http://bundler.io/)
