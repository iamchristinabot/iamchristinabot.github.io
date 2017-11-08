---
id: 000
title: "Why aren't my environment variables working in React?"
date: 2017-11-02T01:16:42+00:00
author: admin
layout: post
permalink: /blog/20171102/why-arent-environment-variables-working/
categories:
  - Web Development
tags:
  - React
---

Spent too much time trying to figure out why environment variables weren't showing in my React app, so I thought I would document the solution for other developers to find. I had added some new parameters to my environment variables so that they could be used by my app. I made sure they were loaded up by the terminal that runs my development server, everything looked good.

<pre>
export EXAMPLE_SITE_URL='https://example.com/'
</pre>

I tried to access the variables through the client, but kept seeing logs of undefined.
<pre>
window.open(`${process.env.EXAMPLE_SITE_URL}`, '_blank')
console.log(process.env.EXAMPLE_SITE_URL)
</pre>

Since some of my variables were visible to the app, I assumed they were somehow being cached, so I started looking up "environment variables not updating" or "environment variables cached". Finally I came across a solution to my issue in the Facebook Incubator github:

<blockquote>
Note: You must create custom environment variables beginning with REACT_APP_. Any other variables except NODE_ENV will be ignored to avoid accidentally exposing a private key on the machine that could have the same name. Changing any environment variables will require you to restart the development server if it is running.
</blockquote>

So what I actually needed was to preface my export and then everything worked as expected.
<pre>
export REACT_APP_EXAMPLE_SITE_URL='https://example.com/'
</pre>

For more information visit Facebook Incubator github:
[https://github.com/facebookincubator/create-react-app/tree/master/packages/react-scripts/template#adding-custom-environment-variables](https://github.com/facebookincubator/create-react-app/tree/master/packages/react-scripts/template#adding-custom-environment-variables)
