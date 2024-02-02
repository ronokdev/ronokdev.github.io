---
title:  Build and host portfolio site with jekyll chirpy - Part 4 | Set Custom Domain
date: 2024-01-20 12:34:27 -500
categories: [portfolio]
tags: [portfolio,personal site,cv,domain,hosting,custom]
---

## Objective
We are going to learn how can we host this portfolio site to a custom domain.

I have my domain bought from [Namecheap](https://www.namecheap.com/) and I will show you what to set up in the namecheap site and what to do in our GitHub repository. 


## Setup In Namecheap
My domain `www.ronokdev.com` is bought from Namecheap and in this post I will actually show you, what settings need to change so that when we go to our domain(`www.ronokdev.com`) then it will actually redirect to `ronokdev.github.io` ,where our portfolio site is hosted .
<br>
First we need to log in to the namecheap account and then go the ADVANCED DNS settings for the domain. And we need to change the setting like the table below. In the place of YOUR_GITREPO_NAME, for my case it will be `ronokdev.github.io`. But you need to fill up according to your GitHub repository name.

| Type      | Host | Value             | TTL    |
|-----------|------|-------------------|--------|
| A Record  | @    | 185.199.108.153   | 30 min |
| a record  | @    | 185.199.109.153   | 30 min  |
| A Record  | @    | 185.199.110.153   | Automatic |
| A Record  | @    | 185.199.111.153   | Automatic|
| CNAME Record | www  | YOUR_GITREPO_NAME |Automatic|

![1](/../assets/img/4/1.png)

<br>
And these are all the changes that need to be done from the namecheap end.


## Setup In GitHub Repository

Go to the `settings` option on the GitHub repository.
![1](/../assets/img/4/2.png)

Then select the `Pages` option and in the `Custom domain` section we need to set our domain name and then press save. In my case it is `www.ronokdev.com`
![1](/../assets/img/4/3.png)

If the domain name is correct, we should see a message saying `DNS check successful`.  

After doing all the changes we need to wait for 24 to 72 hour, and then we should be able to see our portfolio site hosted at our custom domain.

Aand, we are done !! ✅

{% include comment.html %}
