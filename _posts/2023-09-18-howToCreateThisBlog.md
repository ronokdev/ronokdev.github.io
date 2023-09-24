---
title:  Build and host portfolio site with jekyll chirpy under 1 hour
date: 2023-09-18 12:34:27 -500
categories: [portfolio]
tags: [portfolio,personal site,cv]
---

### Objective of this article
we are going to understand how to build and host portfolio site with jekyll-chirpy under 1 hour. We will use chirpy as a theme and we will host this static site to GitHub.


### Why we are using jekyll
Because jekyll is open-source static site generator and it also has a very good integration with GitHub Pages. If you already have a ruby development setup installed in your local machine then it is very easy and much fast to run anything with jekyll locally


### How to Prepare our local development environment to get started
In this article we will only discuss how to set up in the MAC environment

First , we need to check if we already have ruby installed
```bash
which -a ruby
```
if we see something like this as output 
```text
/usr/bin/ruby
```
that means we already have ruby installed in our machine.

As the system Ruby is old, and it can’t be updated we will not use the ruby that is already installed , instead we will set up latest version of ruby and then work with it.


we can set up ruby in a lot of different ways but my recommendation is to use a ruby version manager tool like [rbenv](https://github.com/rbenv/rbenv). Also with `rbenv` we can switch between multiple Ruby versions on the same machine if needed.



{% include comment.html %}
