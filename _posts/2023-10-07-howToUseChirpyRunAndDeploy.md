---
title:  Build and host portfolio site with jekyll chirpy - Part 2
date: 2023-10-07 12:34:27 -500
categories: [portfolio]
tags: [portfolio,personal site,cv]
---

## Objective
we are going to understand how to 
<br>
- Use Chirpy theme 
- Run in local environment
- create first Blog post
- Deploy using GitHub pages


## How to use Chirpy theme
First step is to fork the chirpy project from [CHIRPY-GITHUB](https://github.com/cotes2020/chirpy-starter)
<br>
<br>
![](/../assets/img/article_2/1.png)

<br>
then, give the repository name. The repository name must align with your GitHub username. 

For Example, 
if my GitHub username is `ronokdev` then the repository name must be `ronokdev.github.io`

![](/../assets/img/article_2/2.png)

After creating fork of the chirpy starter project we need to pull or clone the project into our local machine.  

![](/../assets/img/article_2/3.png)

We can use any IDE as of our choice.I am using webstorm from JetBrains.

If the pulling from GitHub happened correctly, and we open the project with our IDE. We should see the project folder structure something like below 

![](/../assets/img/article_2/4.png)


## Run in local environment
Now it's time to run the project locally.

we need to go to the project folder in our local machine and run 

```bash
bundle
```
This `bundle` command will download and install all the dependency for this project.
For actually run the project in our local machine, we need to execute

```bash
bundle exec jekyll s
```

Then we should see the project run in our local machine on this address  `http://127.0.0.1:4000/`

![](/../assets/img/article_2/5.png)

And that's it , so now we have all the component we need to continue building our static site.

## Create first Blog post
For creating a blog we need to add file with a specific format under the `_post` folder.

File name should be in this format

```bash
DATE-FILENAME.md

# Example
2023-10-07-FILENAME.md

```
The format is very important.
**_Also if we put future date, then the post will not come up in our site_**.


Let's create a file named `2022-10-08-BlogFirst.md` into out `_posts` folder and as a content put these

```text
---
title: Blog First
date: 2022-10-08 12:34:27 -500
categories: [cat1]
tags: [tag1,tag2]
---

## Heading
This is a content
```
and if our local server is running, and we open our browser and hit this address `http://127.0.0.1:4000/`. We should see our first created blog post. 

![](/../assets/img/article_2/6.png)

we can click on it, and it will show us the details

![](/../assets/img/article_2/7.png)

And this is how we can create a blog post.

Now it's time for deploy.


## Deploy using GitHub pages
Assuming that we are at `main` git branch and if we add all the changes to a commit and push the commit to gitHub then automatically it will trigger a deployment and our site will be deployed to `YOUR-GIVEN-NAME.github.io` and in my case it will be `ronokdev.github.io`  

Before pushing our changes we need to check what is our default branch in our git repository. And we can do that by going to `settings` and check the `Default Branch` name.

![](/../assets/img/article_2/8.png)

After we push our commit to the `main` branch, we should see a deployment running. 

![](/../assets/img/article_2/9.png)

And when the deployment is successfully done then we should see our site running at `YOUR-GIVEN-NAME.github.io` and in my case `ronokdev.github.io`




{% include comment.html %}