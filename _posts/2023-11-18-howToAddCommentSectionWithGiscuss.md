---
title:  Build and host portfolio site with jekyll chirpy - Part 3
date: 2023-11-18 12:34:27 -500
categories: [portfolio]
tags: [portfolio,personal site,cv,giscus,comment]
---

## Objective
We are going to understand how to 
<br>
- Use [Giscus](https://giscus.app/) to add comment section to our blog

## What is Giscus
Giscus is  comments system powered by [GitHub Discussions](https://docs.github.com/en/discussions). Our website visitors can leave comments and reactions on our blog post via GitHub.


## How to use Giscus

### Setup in the Giscus site
First we need to go to the official giscus site : https://giscus.app/

Before putting our repository details in the giscus site , we find need to check some points
1. Our blog repository should be public
2. Giscus is installed as an app for our GitHub profile. we can install giscus from [HERE](https://github.com/apps/giscus)
3. Discussion is enabled for our blog repository. we can find how to enable discussion feature from [HERE](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/enabling-or-disabling-github-discussions-for-a-repository)

### Setup in our blog
we need to put our blog address in the repository field in the giscus website. And after putting our repo link if we see the message like : `Success! This repository meets all of the above criteria.` Then we are good to go.
![1](/../assets/img/3/1.png)

For now the section `Page ↔️ Discussions Mapping` we are keeping the setting as it is.
![2](/../assets/img/3/2.png)

The section `Discussion Category` we are keeping the setting as it is.
![3](/../assets/img/3/3.png)

and the section `Features` we are keeping the setting as : `Enable reactions for the main post`.
![4](/../assets/img/3/4.png)

The section `Enable giscus` is our section of interest.
![5](/../assets/img/3/5.png)
we want the comment section per each blog post, and we can do it by creating an `comment.html` page and then paste everything in between the `<scirpt>` tag in the html file. 

Finally, include the `.html` file in each and every blog post by adding this at the last of your `.md` file

```bash
{% include comment.html %}
```

And for the final step we need to update the giscus section data in the `_config.yml` file. Which we can find in the root directory of our blog repo.
For my blog it looks something like this 

```bash
  giscus:
    repo: ronokdev/ronokdev.github.io 
    repo_id: R_kgDOJ-5M8Q
    category: General
    category_id: DIC_kwDOJ-5M8c4CZbjA
    mapping: pathname 
    input_position: bottom  
    reactions_enabled: 1 
```
You must change `repo, repo_id, category, category_id` as per your need and configuration.

If everything is set up correctly then we should see something like below.
![6](/../assets/img/3/6.png)

Aaaand, we are done !!

{% include comment.html %}
