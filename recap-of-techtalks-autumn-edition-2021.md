---
title: Recap of our TechTalks autumn edition 2021
date: 2021-11-23
author: "federicab"
category: "techtalks"
tags:
    - post
    - guest-post
    - accessibility
layout: article
metaIMG: "womendotcodebe-techtalks-recap-sept2021.jpg"
featured: true
---

It’s the last day of September and we’re in for a journey from pixels to space narrated by the voice of a screen reader! The two speakers Sophie Ragas and Marta Luffarelli talked about all things web accessibility and remote Earth Observation - here are the main takeaways from their presentations. 
<!-- excerpt -->

## Sophie Ragas - Practical Accessibility Tips

{% image {src: "./blog/guest-blogs/images/techtalks-sophie.png", alt: "Sophie Ragas", widths: [300]} %}

Sophie is a sustainability consultant at [Eleven Ways](https://www.elevenways.be/) an accessibility company based in Gent. Developers tend to struggle with accessibility, especially testing, so she’s gifting us some practical advice to make it less difficult and intimidating. 

### Access to information as a basic human right
Nowadays services and information are getting more and more digital. Making the web accessible for everyone is fundamental because through that one can exercise other human rights such as privacy or education. “The power of the Web is in its universality. Access by everyone regardless of disability is an essential aspect” and I’m quoting Tim Berners-Lee, the inventor of the World Wide Web himself.

### Common perception of disability
Most people have a set idea of how disability looks like: it often conveys the mental image of a lonely person in a wheelchair. But disability is much more diverse than that, it is a broad spectrum encompassing: 

- permanent disabilities (such as blindness and impaired mobility)
- disabilities due to ageing 
- temporary disabilities (such as a broken arm) 
- situational disabilities (for instance carrying a baby in your arm or not being able to use sound in a public space) dyslexia, ADHD and autism

{% image {src: "./blog/guest-blogs/images/techtalks-autumn-2021-img1.png", alt: "a visual overview of formentioned disabilities", widths: [300,600,1000]} %}


Because of how broad this spectrum is, it is for sure that disability will affect all of us at some point in our lives. Knowing that should encourage us to figure out tailored solutions for a diverse set of issues and build more empathy towards disabled users. 

### Developers’ perception of disability
When most developers think about disability they have a similarly narrow mental image of it: they think exclusively of visual disability, screen readers and braille devices. So they tend to focus solely on that issue, while the spectrum, also for what concerns apps and website users, is much broader.

The outcome of a research on the use of disability settings by the dutch company [Q42](https://werkenbij.q42.nl/) shows it well. The most used disability feature is reciting tex (33%), which makes sense in relation to the visually impaired or the elderly. But the second most used feature is an interesting reveal: dark mode (27%) used to prevent tired eyes and increase contrast, which illustrates the aforementioned broad spectrum of disabilities and how accessibility can also benefit people without disabilities. 

### WCAG (Web Content Accessibility Guidelines)

The W3C (Word Wide Web Consortium), an international community that develops standards for the Web, elaborated a set of strategies, standards and resources to make the Web accessible to people with disabilities: the WCAG (Web Content Accessibility Guidelines).

{% image {src: "./blog/guest-blogs/images/techtalks-autumn-2021-img2.png", alt: "visual representation of POUR, which stands for perceivable, operable, understandable, robust", widths: [300,600,1000]} %}

The 4 core principles of the WCAG are:

- The information on the website should be **perceivable**
- The website should be **operable**
- The content should be **understandable**
- The code should be **robust** so that it can be interpreted by a wide range of technologies

The quick reference is a good resource to start out with [WCAG](https://www.w3.org/WAI/WCAG21/quickref/): levels A and AA are the most relevant for testing. 

### Practical tips for testing according to WCAG principles
There are 3 types of testing: 
Manual testing Automated testing User testing 

We are going to focus on manual (keyboard, images) and automated testing. 

#### Keyboard testing
Click through the website to check if you can reach all links, buttons and controls and activate them. Check if these elements have a focus outline and if their order is logical. You can read more about [the #NoMouse Challenge on this website](https://nomouse.org/). 

#### Images
Images should always have an “alt” attribute: if the image is informative the “alt” should contain a text while if the image is decorative it should be empty. But how to tell if an image is informative or decorative? Pretty arbitrary right? The [Alt Decision Tree](https://www.w3.org/WAI/tutorials/images/decision-tree/) has you covered. To check a posteriori if you’ve done it right you can use the [Web Developer toolbar](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm ), a Chrome extension that helps you notice missing and empty “alt” attributes. 

#### Responsive design
You can test responsive design with the browser’s tools or use [Polypane](https://polypane.app/), a browser that uses Chrome under the hood and has a lot of tools and simulators to test your projects. 

#### Resizing text
Check if the text can be zoomed by using the shortcut CMD (or CTRL) and + or - . Text should not overlap with other elements nor disappear. 

#### Contrast 
You can check contrast ratio with Polypane or with the inspect element in Chrome’s DevTools (and even get suggestions on how to fix that!). Different elements require different contrast ratios:

- For user interface components at least 3:1
- For normal text 4.5:1
- For larger text (>18px and bold) at least 3:1

[Stark](https://www.figma.com/community/plugin/732603254453395948/Stark) a plugin for all major design tools and 
[Contrast](https://www.figma.com/community/plugin/748533339900865323/Contrast), a Figma plugin, can help you bear in mind contrast during the design phase.

{% image {src: "./blog/guest-blogs/images/techtalks-autumn-2021-img3.png", alt: "where to find the contract check in chrome", widths: [300,600,1000]} %}

Remember to check if your website makes sense for colour-blind people!

#### Test your code
[Axe DevTools](https://chrome.google.com/webstore/detail/axe-devtools-web-accessib/lhdoppojpmngadmnindnejefpokejbdd/related) is a Chrome extension that you can use to run automated tests. And don’t forget to check the markup of Web Documents with [Validator](https://validator.w3.org/) and missing labels with Chrome’s DevTools and the Web Developer toolbar extension.

#### Testing with screen readers

The bogeyman! Definitely the most dreaded one: try to disable the sound and show the screen reader’s output on screen to be less overwhelmed at first. Don’t worry if you can’t spot all issues because if you manage to fix the most high-level ones that’s already gonna have a big impact on users. 

Some useful resources:

- [How to turn VoiceOver on ](https://support.apple.com/en-gb/guide/iphone/iph3e2e415f/ios) 
- Screen Reader Basics: VoiceOverAccessibility Testing with the NVDA [Non Visual Desktop Access]https://dequeuniversity.com/ 
- Tip: to save you time while testing with screen reader you should set up the shortcuts first 
    - Enable [shortcut on iOS](https://support.apple.com/en-us/HT210628)
    - Enable [shortcut TalkBack](https://support.google.com/accessibility/android/answer/6007100?hl=en)



## Marta Luffarelli - Earth Observation from Satellite
{% image {src: "./blog/guest-blogs/images/techtalks-marta.png", alt: "Marta Luffarelli", widths: [300]} %}

Marta studied electronic engineering in Italy. She moved to Brussels in 2016 to join Reference, a private R&D company focusing on radiation transfer and she is now doing a PhD at the Faculty of Science at the Université Libre de Bruxelles (ULB). She is passionate about Earth Observation and she is going to shed light on what that is and what it is used for. 

### What is earth observation

Earth observation (EO) is the process of measuring the Earth’s surface and atmosphere via remote sensing instruments. The data collected through EO has applications in many different fields such as forest and water management, monitoring damages after natural disasters, air pollution, climate change, weather forecasts and air quality.

The date of birth of earth observation is considered to be 1858, when the first photo of history from an air balloon was taken. This development of these technologies accelerated during the two World Wars, since they were heavily employed for military purposes, and even more so during the Cold War when Sputnik, the first artificial satellite, was sent to orbit by the Soviet Union.


{% image {src: "./blog/guest-blogs/images/techtalks-autumn-2021-img4.png", alt: "A visual historical timeline representation of aerial photography from Marta's slides", widths: [300,600,1000]} %}

### Coding for Earth Observation
Since then we’ve come a long way and today we have more than 700 Earth Observation Satellites flying around the planet! All these satellites collect an incredible amount of data (the so-called Big Earth Data), which also comes in very different formats: all this information needs to be processed (sometimes for days and months) and very robust software needs to be developed for that. 

The programming languages used to write this software are often quite old-fashioned. Fortran is still very popular and this is not only because of historical reasons (Fortran was all the rage when the field of EO emerged), but also for its efficient array handling and easy core-level parallelisation which makes it very suitable for math-heavy software. 

For everything that is not mathematics the most commonly used languages are Python and C++. Different layers of the software are coded in different languages (with the higher-level is in Python and the core in Fortran) and communicate through interfaces. 

### The radiation transfer theory

{% image {src: "./blog/guest-blogs/images/techtalks-autumn-2021-img5.png", alt: "a visual representation of how a satellite measures the fraction of reflected solar radiation", widths: [300,600,1000]} %}

But what do satellites actually measure? Well, they measure the fraction of solar radiation reflected by the atmosphere. Radiation transfer theory is the model of how sun radiations that hit the atmosphere interact with Earth are absorbed and transmitted. A scientific model seeks to represent empirical objects, phenomena and physical processes in a logical and objective way. The Earth is a very complex system, therefore it is difficult to represent it faithfully in a model and that’s why radiation transfer theory models are still rather sketchy and oversimplified. 

{% image {src: "./blog/guest-blogs/images/techtalks-autumn-2021-img6.png", alt: "Today's oversimplified model", widths: [300, 600, 1000]} %}

### Real applications
*“Watch it Grow”* is a Belgian application for agriculture and especially potato cultivation. The application monitors when the potatoes are ready for harvest, if the soil needs more water or if there is any change in the growth of the potatoes.

Another application of EO is for dust storm prediction: satellite data can detect dust from its formation and release an early warning to minimise the damages associated with it.

Earth Observation data is also used to monitor climate change: due to greenhouse gases incoming solar radiations are not outgoing, and this contributes to the increase of temperature on Earth.

{% image {src: "./blog/guest-blogs/images/techtalks-autumn-2021-img7.png", alt: "a more realistic representation of how solar radiation hits the earth", widths: [300,600,1000]} %}