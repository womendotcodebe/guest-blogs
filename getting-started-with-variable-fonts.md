---
title: "Getting started with variable fonts"
date: 2022-04-06
cover: "getting-started-with-variable-fonts.jpg"
caption: "Photo by Markus Spiske on <a target='_blank' href='https://unsplash.com/photos/f81ym3dE5N4' rel='noreferrer'>Unsplash</a>"
author: "federicab"
category: "tips"
tags:
    - post
    - guest-post
layout: article
preview: "Are you already using variable fonts? No? Find out why and how you should start using variable fonts."
---

You might not be a web typography freak, but no developer likes a FOUT (Flash Of Unstyled Text) welcoming users on their pages. Variable fonts are here to help. And if you really are kind of a web typography freak, you will be even more enticed to hear about variable fonts. So let’s get started!

## Web fonts

If you have been working with custom web fonts you are accustomed to having a good ol’ folder with several single files, one for each width, weight, slant of the font. For each font variation you want to use on the web page a bit of data that must be downloaded, processed, and rendered by the browser, which can end up causing performance issues. To avoid these issues developers have been trying to to cut on the number of loaded files by using less fonts variations. This might do the job in terms of performance but it’s not a great practice in typography: graphic designers will tell you that it’s normal to use a up to 8-10 different weights and variants of a typeface to create a balanced and readable layout.

### Variable fonts

With variable fonts all the font’s permutations are contained in a single file. The regular shape of the character and the deltas of where the points move along to make the variations are stored in one single file. Instead of having the single variations' files ready to go, variable fonts are storing the code instructions to make each of these variations - smart, right? The difference in weight is remarkable: a variable font can be like 230KB, much smaller than loading multiple variants of a classic web font (each of them being around 200KB)!

Each variant of a font is bound to an axis, which is a specific setting that can change how the font looks. The variants of a font are defined by the type designer. There are five registered axes, which correspond to the classic font variations (width, weight, italic, slant, optical size). If you want to see a font morphing on its registered axis, [take a look at this article](https://variablefonts.io/about-variable-fonts/). In addition to those custom axes can also be defined and they can be anything and everything, such as gravity spread, drippiness and other cool effects.


## How to use variable fonts

Variable fonts can be controlled through CSS with high-level and low-level properties.

High-level properties:  font-weight, font-stretch, font-style, font-optical-sizing. Each of them interacting with a registered axis is labelled with 4 letters: 

- wght for font-weight
- wdth for font-stretch
- ital and slnt for font-style
- opsz for font-optical-sizing

As a convention registered axes are represented with lowercase letters while custom axes are represented with uppercase letters. 

Here is how you set variable font properies with high-level properties 

```css 
    .style {
    font-weight: 300; 
    font-stretch: 100; 
    } 
```

Low-level: font-variation-settings you can use the 4-letter label to specify the settings in here. 
 
And here is the same code with low-level properties 

```css 
    .style {
    font-variation-settings: 'wght' 300, 'wdth' 100;  
    } 
```

[This free one-hour-long course](https://www.youtube.com/watch?v=9IFqv5uVP_c&t=2728s&ab_channel=EnvatoTuts%2B) is going to walk you though the basic steps of setting up and using variable fonts on your project.

### Browser and software support 

Developers of Edge, Chrome and Safari are part of the open type variable fonts projects, so it no surprise that Chrome and Edge have the best support. Safari has also good support provided that you have MacOS10.13 or higher. Firefox does not have full support yet.

If you decide to use variable fonts in your next designs you can use Photoshop or Illustrator, or try the [samsa.js plugin](https://www.figma.com/community/plugin/966184368629063440/Variable-Fonts) on Figma. Photoshop can also be used as a preview tool for variable fonts. 


## Where to find variable fonts

[Axispraxis](https://www.axis-praxis.org) and [V-fonts](https://v-fonts.com/) are two great resources for discovering variable fonts. On both sites you can play around with sliders to see the fonts’ variations on the various axes - very satisfying. [Google Fonts](https://fonts.google.com/variablefonts) also provides loads of variable fonts, without the fun sliders tho. To delve deeper in the topic highly recommend to listen to the [Smashing Podcast episode](https://www.smashingmagazine.com/2019/12/smashing-podcast-episode-5/) on variable fonts with Jason Pamental, the ultimate web typography connoisseur. And if you want to venture even further take a look at this valuable list of resources compiled by [A Variable Fonts Primer](https://variablefonts.io/variable-font-resources/)

### Conclusions

Variable fonts can be super useful and a lot of fun. On the merely technical side, they are a clear win in terms of performance. They are a blessing for designers who can use an almost infinite variants spectrum towards a more nuanced approach to typography on the web, which ultimately leads to a better UX. Finally, they allow for mad typographic experiments to come to life. No matters what sort of pixel pusher you are, variable fonts are exciting stuff!


---

For more about variable fonts and how to use them, you could also check out this article: <a href="https://evilmartians.com/chronicles/variable-fonts-in-real-life-how-to-use-and-love-them" rel="noreferrer">Variable fonts in real life: how to use and love them</a>