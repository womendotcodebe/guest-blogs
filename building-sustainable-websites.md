---
title: "Building Sustainable Websites"
date: 2023-12-20
cover: "sustainable-websites.png"
author: "claudiar"
category: "tips"
tags:
  - article
  - guest-post
layout: article
featured: true
source: "https://tech.reyndeer.com/articles/building-sustainable-websites/"
sourceName: "tech.reyndeer.com"
---

Have you ever took a moment to stand still and think about the impact you're making with the websites you're building?

For the last 5 years or so I have been working on becoming more conscious about the impact I'm making, more in particular the negative impact.<br><br><strong>Btw, did you know that tech is responsible for 4% of the global energy consumption???</strong>

<!-- excerpt -->

In this article I will share some of the things I have learned along the way, partially thanks to a lot of great people and also by taking an interest in how to design and build more sustainable websites. I am not a specialist in this, so I learn by doing and reading up on facts, talking and meeting with likeminded peers and by frequently questioning things and not just ignorantly accepting information.

## Some facts & numbers
*The following data is collected from multiple resources such as articles and people's keynotes.*

IT produces approximately 4% of global carbon emissions and is responsible for 10% of global power consumption!!!

**Besides power consumption and carbon emissions, there is also a percentage of natural resources being depleted.**

<figure class="quote">
  <blockquote>
  <p>Research estimates that by 2025, the IT industry could use 20% of all electricity produced and emit up to 5.5% of the world’s carbon emissions.</p>
  </blockquote>

  <figcaption>⎯  Source: <a href="https://theconversation.com/the-internet-consumes-extraordinary-amounts-of-energy-heres-how-we-can-make-it-more-sustainable-160639" target="_blank" rel="noopener noreferrer">theconversation.com</a>
  </figcaption>
</figure><br>


Global trends such as (addictive) social media, AI, cryptocurrency, automation, smart devices, internet of things and others definitely play a big part in this. 

A more detailed impactful example was brought to my attention by my former colleague [Kjelle V](https://be.linkedin.com/in/kjelle) during his excellent keynote titled: *"Designing for Sustainable Digital Experiences"*, where he spoke a lot about the current usage of data. More specifcally, streaming online video.

<figure class="quote">
  <blockquote>
    <p>We live in a world where only one form of digital use, online video, generates 60% of the world data flows and thus over 300 million tons of CO2 per year.</p>
  </blockquote>

  <figcaption>⎯  Source: <a href="https://theshiftproject.org/en/article/unsustainable-use-online-video/" target="_blank" rel="noopener noreferrer">The Shift Project</a>
  </figcaption>
</figure><br>

All we do can be traced back to data, so we can expect that data usage and storage will grow exponentially. Now that it feels like everyone is experimenting with AI and trying to come up with as much use cases as possible, we should also realise that we already waste most of our data. Another fact from Kjelle's keynote:
<figure class="quote">
  <blockquote>
    <p>90% of content indexed by Google has 0 visitors (ever).</p>
  </blockquote>

  <figcaption>⎯  Source: <a href="https://ahrefs.com/blog/search-traffic-study/" target="_blank" rel="noopener noreferrer">ahref blog</a>
  </figcaption>
</figure><br>


The way I see it is that almost everything we do nowadays is either consuming power,  producing higher CO2 emissions and continues to deplete earth's natural resources. At the same time forests are getting cut down to make room and/or produce the resources we need, CO2 levels keep on rising. As with everything, there is need for balance.

## What can we do about it?
Everything we build adds onto the total of power consumption, CO2 emissions and in some cases also further depletion of precious resources. So it’s natural to assume that we should take some responsibility for it as well.

### Things you can do: 
I personally believe we should all try to be more conscious about what we are putting out there. Whether it’s online and open for all or going to be used in a museum as an interactive guide. We have an impact on energy consumption and co2 emissions through our creations.

So be intentional about whether a project really needs to be built, how it’s built and if it really needs to stay online or active way past its use.

Who knows how many old websites are floating around the internet?

So something you can ask yourself:  **Does this project fill an actual need or is pure for entertainment?**
Because whether we like it or not at some point we might need to put a stop to giving into building every idea we have and putting it out there. (this is not limited to tech of course)

And since we were talking about data before, also think about data usage as well as data collection.

### Practical tips 

**If you are a developer start with looking up the carbon score of your website.**

If you haven’t already:
- Look for ways you can reduce your website in size and amount of requests
  - Always optimise images, audio & video and choose the right format.
    To help you get started check out the following sources:
    - [Modern Image Formats: AVIF & WebP](https://www.smashingmagazine.com/2021/09/modern-image-formats-avif-webp/)
    - [How To Optimize Images for Web and Performance](https://kinsta.com/blog/optimize-images-for-web/)
    - [Optimizing Video For Size And Quality](https://www.smashingmagazine.com/2021/02/optimizing-video-size-quality/)
  - Ideally, don't use video unless it's really necessary
    A big one if you do work with video: [lazy load](https://developer.mozilla.org/en-US/docs/Web/Performance/Lazy_loading) scripts or load on click  - especially third party ones like Youtube or Vimeo.
  - Use SVG for visuals where possible (SVG's have better compression and better scalability)
  - Use web caching & GZIP compression for your website 
  - Preload external resources with [preconnect](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/rel/preconnect)
  - Use [system fonts](https://css-tricks.com/snippets/css/system-font-stack/), custom web fonts such as google fonts can have a huge impact on your site.
- CSS > JS; If you can use CSS instead of JS to get something done, do it.
  CSS has progressed remarkably over the last decade and more is to come. To get an idea of what's already available and what is still in the works, [check out my friend Bramus his blog](https://www.bram.us/2023/10/13/whats-new-in-css-2022-10-12-frontmania/#the-talk)
- Make sure your website is accessible ([see info from Sophie’s techtalk](https://womendotcode.be/blog/recap-of-techtalks-autumn-edition-2021/#sophie-ragas---practical-accessibility-tips) or [Rune's techtalk](https://womendotcode.be/blog/recap-of-techtalks-spring-edition-2023/#see-me%2C-hear-me%2C-include-me%3A-a-journey-through-disabilityand-web-accessibility-by-rune-devuyst))
- Improve your SEO with this [SEO Starter Guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide)
- Generally: be very aware of what third parties are adding to your website, this includes analytics, anything you get from Google (yes also Google Fonts! Host fonts on your server if you can), Facebook and other big platforms.
- Anything that improves privacy also improves load times: the more data you gather the more bandwidth you need, so focus on the analytics that really matter (and that are anonymized as much as possible). So stop collecting unnecessary data!
- Another thing is cloud storage: the less we need of it the better as servers need a ton of energy to run. This is both a thing to keep in mind for applications we build but also for how we run our businesses and for our own personal use.
- Use CDN’s instead of cloud hosting
  A CDN caches your website in the data center(s) closest to your visitors, which in turn shortens the distance the data has to travel. A CDN can also add an extra layer of security


### Tools for testing

- Measuring your website's carbon score
  - [websitecarbon](https://www.websitecarbon.com/) (Seems less accurate after latest update)
  - [Ecograder](https://ecograder.com)
  - [greenpixie](https://greenpixie.com/sites/tech-reyndeer-com)
  - [carbonanalyser for Firefox](https://addons.mozilla.org/fr/firefox/addon/carbonalyser/)
  - [globemallow for Chrome & Edge](https://globemallow.io/)
- Overall testing
  - [Lighthouse on Chrome](https://chromewebstore.google.com/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk)

- Accessibility testing
  - [Deque AXE](https://www.deque.com/axe/) (extensive accessibility testing)

- Optimisation
  - [TinyPNG](https://tinypng.com/) (shrinking / optimizing images)
  - [Kraken.io](https://kraken.io/) (shrinking / optimizing images)

### Other resources  worth checking out
- [Web Sustainability Guidelines (WSG) 1.0](https://w3c.github.io/sustyweb/)
- [Sustainable Web Design](https://sustainablewebdesign.org/)
- [Green Software Practicioner](https://learn.greensoftware.foundation/)
- [Embrace the Platform](https://www.bram.us/2023/12/12/embrace-the-platform-article/) by Bramus


