# Post format and author profile guide

This guide covers the following content:
- [Author profile](#author-profile)
- [Post formatting](#post-formatting)
    - [Yaml Front Matter](#yaml-front-matter)
    - [Custom Markdown Formatting](#custom-markdown-formatting)
        - [Exerpts / preview text](#excerpt--preview)
        - [Code blocks](#code-blocks)
        - [Images and image layout options](#images-and-image-layout-options)

## Author profile
If it's your first time posting add or link the following information to your pull request:
- name (firstname + first letter of your last name)
- role (job or student specialisation)
- bio (short)
- twitter (handle only)
- avatar (if possible in 2 formats, square and portrait in jpg format)

## Post formatting
We use traditional markdown with a couple of extras. If you're not familiar with Markdown yet, it's best to start here: [Markdown Cheat sheet](https://www.markdownguide.org/cheat-sheet/)

### YAML Front Matter
Every blogpost has to start with a section of front matter in order to be parsed properly.
In this section of front matter you fill in a set of variables such as the title, date and so on...

**Your author ID** is always your firstname + the first letter of your last name (unless we have naming conflict)

Each blogpost can contain only one category, if it fits under one of the existing categories please opt to use that one. Otherwise we'll be happy to create a new category after considering what the best name could be.

**Categories for guest posts:**
- learn to code
- tips
- tutorials
- techtalks (reserved for the recaps of our TechTalks events)


**Tags should always be post and guest-post**, the use of tags is not keyword or SEO related in this case, but rather a way to sort blog collections.

**preview**, this can be used to add a preview of your blogpost. There is another option to do this, but this falls under our custom Markdown formatting.

Make sure you don't forget to add `layout: article` so that the page will be rendered correctly.


Front matter example:

```yaml
---
title: "The next steps in Android Development"
date: 2021-05-03
cover: "android2.jpg"
author: "oyac"
category: "learn to code"
tags:
  - post
  - guest-post
layout: article
preview: "We are back for another part to get into Android development"
---
```


### Custom Markdown Formatting

#### Excerpt / preview
Instead of adding a preview in the front matter, you can also opt to use an `excerpt`-marker directly in your content. The downside is that it cannot wrap text, so everything before that marker will be considered as excerpt text. So ideally you only use this somewhere in the very beginning of your blogpost, otherwise we recommend adding a preview text instead.

```markdown
Have you ever thought about making your own website or personal blog easily and for free? <!-- excerpt --> Or maybe you want to learn some web development basics? Then this tutorial might be interesting for you.
```

As you can see in the example above, the `<!--excerpt -->` has been put between two sentences. But only the first sentence will be marked as part of the excerpt text for that blogpost.

#### Code blocks
If you are writing a blogpost that contain showing pieces of code, you can make use of code highlighting.

Inline code:
`\`let item = "potion;"``

Code block:
\```js
const toCelsius = (fahrenheit) => {
    return (5/9) * (fahrenheit-32);
}
\```


#### Images and image layout options

To add images, you need to use a piece of custom shortcode that we have created to optimize all images for web.


Example of the image shortcode:
```liquid
{% image {src: "./blog/guest-blogs/images/learntocode-frontend-example-1.jpg", alt: "Aesop aromatique candles - product website"} %}
```

As usual you add an image src and the alt text. The image path should always start with: `./blog/guest-blogs/images/` and then the image itself.

##### Image Layout options

You can wrap text around image or display a few images in a row (this works best with images in portrait-mode)

You can wrap text around an image as follows:
```markdown
::: text--float-right
{% image {src: "./blog/guest-blogs/images/learntocode-frontend-example-1.jpg", alt: "Aesop aromatique candles - product website"} %}
Learning front-end development has become a lot easier of the years. With so many different online courses, books, courses and stuff out there, it's just a matter of choosing what works best for you.
:::
```
A few images displayed inline:
```markdown
::: image-block
{% image {src: "./blog/guest-blogs/images/learntocode-frontend-example-1.jpg", alt: "Aesop aromatique candles - product website"} %}
{% image {src: "./blog/guest-blogs/images/learntocode-frontend-example-2.jpg", alt: "product website"} %}
:::
```



If something in this guide is unclear or you want to add something new, feel free to reach out to Claudia.