---
title: "Designing a Configurable List View for Recruiting"
date: 2021-03-09T12:00:00+00:00
author: admin
layout: post
permalink: /blog/20210309/designing-a-configurable-list-view-for-recruiting/
categories:
  - Web Development
---

I've been working on a [recruiting application](/projects/recruiting-app)
that helps companies find and recruit talent. Most of my work has focused on
one deceptively hard piece of it: a configurable list view that lets clients
compare candidates.

List views are one of those problems that look simple until you build one for
real users with real data. Every client cares about different attributes, so
the columns have to be configurable. Comparison only works if the data stays
scannable, so density, alignment, and hierarchy carry more weight than any
flashy visual choice. And the moment you let people configure something, you
take on the responsibility of making the default configuration good enough
that most people never need to.

It's the kind of work I find quietly satisfying: no hero moments, just a
hundred small decisions that add up to a tool people can rely on every day.

A few (confidentiality-friendly) screens are on the
[project page](/projects/recruiting-app).
