---
title: How to make a blog with R blogdown and GitHub Pages
date: 2021-04-01
cover: "how-to-make-a blog-with-r-blogdown-and-github-pages.jpg"
caption: "Photo by Jess Bailey on <a target='_blank' href='https://unsplash.com/photos/q10VITrVYUM'>Unsplash</a>"
author: "annav"
category: "tutorials"
tags:
    - post
    - guest-post
layout: article
preview: "Code is one of those things in life, where you don't know how useful it is until you get really proficient at it."
featured: false
excludeFromSitemap: true
---

Have you ever thought about making your own website or personal blog easily and for free? <!-- excerpt --> Or maybe you want to learn some web development basics? Then this tutorial might be interesting for you.

Below we will create a static website in [markdown](https://www.markdownguide.org/basic-syntax/) with [R programming language](https://www.r-project.org/) and deploy it to [Github Pages](https://pages.github.com/). **Don’t be afraid if you are not familiar with R or markdown.** The instructions are simple and anyone, even with limited experience in programming, can follow them. You should also be familiar with the use of the terminal because site building and page editing can’t be accessed through a graphical interface as in a Content Management System (e.g.: WordPress, Drupal, etc ). Nevertheless, RStudio IDE makes the development much more user friendly and straightforward than just in a terminal and text editor.

Above all, you can also use this tutorial to get some practice with markdown and R programming language or [R markdown](https://rmarkdown.rstudio.com/authoring_basics.html). Data scientists and analysts often use R markdown to combine R or Python code and visualizations of their data in reports, dashboards or presentations. For example, [AirBnb uses R markdown for the documentation of their research in R](https://www.tandfonline.com/doi/full/10.1080/00031305.2017.1392362).

The website in R is created with the `blogdown` package. [Blogdown](https://bookdown.org/yihui/blogdown/) is based on the popular static site generator [Hugo](https://gohugo.io/) that renders your markdown content into HTML files. In other words, Hugo will transform your content so that any web browser can read it. You don’t need to know much about Hugo at this stage since everything is done by blogdown package.

**This tutorial will approximately take 1-2 hours of your time depending on your experience.** Be aware that further styling (e.g. themes, css) and creating content are not explained in this post. I leave this part to you or maybe I will cover it in the future. Together we will run through all the steps to build our R markdown-powered blog in Rstudio IDE.

## Step 0. Prerequisites

You need to have this software installed on your PC:

- [R](https://www.r-project.org/)
- [RStudio](https://rstudio.com/)
- [Git](https://git-scm.com/)

This [link](https://rstudio-education.github.io/hopr/starting.html) should help you to set up the R environment. First, you need to install R. Second, install RStudio. Here is another [link](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) that tells you how to install git in case if you don’t have it yet. Also you will need to have an account on [GitHub](https://github.com/).

## Step 1. Install blogdown and Hugo

First, let’s run these two commands in the R console to install `blogdown` and `hugo`.

```r
install.packages("blogdown")
blogdown::install_hugo()
```

This will install all packages needed for `blogdown` and `hugo` to work. In case you already have them; please check the latest updates and update these packages if needed.

## Step 2. Create Rstudio project

After that, let’s create a new project in `"File"` -> `"New Project..."` menu. Select `"New Directory"`:

![snapshot of the new project wizard to create a project](../images/step2_1.png)

Then select `"Website using blogdown"`:

![snapshot of the project type options view](../images/step2_2.png)

Now fill in a directory and project name as shown in figure below:

![snapshot of the new project wizard step 3](../images/step2_3.png)

## Step 3. Create GitHub repository

In addition, publishing our website via Github Pages requires some additional customization. We will need to create a new repository on [Github](https://github.com/). For example, let’s call it “rblogexample”. In step 6, we’ll take a look at how to deploy a website to Github more closely.

## Step 4. Customize ‘config.yaml’

Now we need to modify our `config.yaml` that is located in the main folder of your project. Open `config.yaml` and change the fields as follows:

- First, set up the base URL to the “root” of the web page: `https://<user_name>.github.io/<repo_name>`. For example, in my case it is https://annavarzina.github.io/rblogexample/).

```yml
baseurl: https://annavarzina.github.io/rblogexample/
```

- Second, change the default `/public` folder to a custom folder of the repository outside of the project. In this example I named the folder `/myblog` which I put one level up. This is needed because your website should be kept in the separate repository. Therefore, every time you make changes in the project and make a build, the website folder will be automatically updated. So there is no need to copy a new website version manually. Moreover, you will need to initiate git in the website folder while your project sources can have a separate version control.

```yml
publishdir: ../myblog
```

- [Optional] Add title:

```yml
title: R blog example
```

- [Optional] Finally, update `menu` and add or change the links (e.g. Github, Twitter or other):

```yml
menu:
  main:
    - name: About
      url: /about/
    - name: GitHub
      url: https://github.com/rstudio/blogdown
    - name: Twitter
      url: https://twitter.com/rstudio
```

## Step 5. Build website

Now we can build our blog by running these commands:

```r
blogdown::build_site()
blogdown::serve_site()
```

In addition, you can also run `library(blogdown)` in the console. This will allow you to run your commands without having to write the `blogdown::` prefix. In this tutorial we use the first method in order to show explicitly that these commands belong to the `blogdown` library.

Now we are ready to view our website in the Rstudio viewer or browser!

```r
http://localhost:4321/rblogexample
```

![snapshot of the website working on localhost](../images/step5_1.png)

After it has been built, the components are placed in the folder `/myblog` which we defined in the configurations earlier.

In order to stop running site, use the following command:

```r
blogdown::stop_site()
```

**TIP!**

If you want to personalize your blog there is a variety of options available that will let you adjust the styling with existing Hugo-themes, custom CSS or JavaScript. This is not really a part of this tutorial’s scope, but this might help you get started:

- Hugo themes: Update `theme` in `config.yaml` with themes from https://themes.gohugo.io/.
- Replace logo: Just use your own file and place it to `/static/images/logo.png` path. In `config.yaml` it should look as:

```yml
logo:
    alt: Logo
    height: 50
    url: logo.png
    width: 50
```

- CSS: For example, add `/static/css/custom.css` and update `config.yaml` with `customCSS: ["css/custom.css"]` in `params`.
- JavaScript: For example, add `/static/js/custom.js` and update `config.yaml` with `customJS: ["js/custom.js"]` in `params`.

## Step 6. Deploy to Github

First, let’s [create a version control in the project folder](https://docs.github.com/en/github/importing-your-projects-to-github/adding-an-existing-project-to-github-using-the-command-line) so we can track changes. Secondly, we’ll initialize git in the rendered blog folder (`/myblog`). You can use Rstudio Terminal to create a git repository (Click `"View"` -> `"Move focus to Terminal"` if the terminal window is not open). Write the following commands in the terminal:

```bash
cd ../myblog
git init
git add .
git commit -m "Init blogdown site"
git branch -M main
```

Add the remote repository (it is always a good practice to make a connection with [SSH key](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)):

```bash
git remote add origin git@github.com:annavarzina/rblogexample.git
```

Now we can upload changes to remote repository:

```bash
git push -u origin main
```

After the deployment, go to repository settings and scroll down to **Github Pages**. Choose branch `main`, directory `/root` and click on `Save`. Your webpage styles will be updated in a while and you can enjoy it via link
`https://<user_name>.github.io/<repo_name>`.

## Step 7. Create post

Go back to the Console and make a new post with the `new_post()` function similarly to:

```r
blogdown::new_post(title = "My first blog post", 
                   author = "annav", ext = ".Rmd")
```

By default, it will be created with the extension `.md`. Personally, I prefer R Markdown instead and thus explicitly define the extension as `.Rmd`. The file will be generated in folder `/content/post/yyyy-mm-dd-my-first-blog-post` where `yyyy-mm-dd` is the date. Now we will fill it with the content (according to markdown rules) and push the button `Knit`. The `.html` file will be rendered and saved in the same folder.

## Step 8. Publish changes

Rebuild the website for publishing with `blogdown::build_site()`.
The website will look like this now:

![final snapshot of the website](../images/step8_1.png)

Now all we need to do is commit the changes (in both project and output directories) and deploy them (in `/myblog` repository):

```text
git add .
git commit -m "Create new post"
git push origin main
```

## Step 9. [Optional] Customize domain name

If you are interested you can go one step further and use your own domain name instead of `<user_name>.github.io`. Github will only serve as a hosting then.

To do that we should change a `baseurl` in config file to the domain (`www.example.com`). In the repository settings on the Github pages section we’ll add the same domain name (`www.example.com`). Github will automatically generate a CNAME file and commit it. !Do not forget to fetch this commit! And we will also have to link the domain with Github which is done with the DNS provider of our website. There you will have to link the CNAME `*` and `www` with `<user_name>.github.io`. You might have to wait up to 24 hours until these changes take place. Once it is done, the new blog should work on your own domain name. If you want to learn more about this, check out this link on [how to manage a custom domain in Github](https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site).

## Congratulations!

Let me welcome you to the world of blogging! Now you can enjoy your new blog and create your own content. For example, my blog is also made in this manner and I am pretty happy with it especially because I write mostly about programming topics, mathematics and data science with R markdown.

## References

Here are a few additional links for more information and extra reading:

1. [R Markdown](https://rmarkdown.rstudio.com/)
2. [R Markdown book](https://bookdown.org/yihui/rmarkdown/)
3. [Blogdown](https://github.com/rstudio/blogdown/)
4. [Blogdown book](https://bookdown.org/yihui/blogdown/)
5. [Github Pages](https://guides.github.com/features/pages/)
6. [Hugo](https://gohugo.io/)
7. [R blogdown setup in github](https://aurora-mareviv.github.io/talesofr/2018/02/r-blogdown-setup-in-github-2/)
8. [Up & running with blogdown in 2021](https://alison.rbind.io/post/new-year-new-blogdown/)
9. [How I Used Hugo and blogdown to Set Up My Own Website](https://medium.com/@diegousaiuk/how-i-used-hugo-and-blogdown-to-set-up-my-own-website-e32e2eddbf81)