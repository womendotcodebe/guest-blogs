---
title: Recap of our TechTalks summer edition 2021
date: 2021-11-23
author: "federicab"
category: "techtalks"
tags:
  - post
  - guest-post
layout: article
metaIMG: "womendotcodebe-techtalks-recap-june2021.jpg"
featured: true
---

Buckle up for the recap of another eclectic Techtalk.
Lisa Tarpletti shared some tip on how to eco-design our system, Asma Oualmakran shed light on cybersecurity buzzwords, and Liza Morrison is walked us through a brand-new framework, Qwick.

<!-- excerpt -->

## Lisa Trapletti - Eco-designing its digital services. A path to sustainable IT

{% image {src: "./blog/guest-blogs/images/techtalks-sophie.png", alt: "Sophie Ragas", widths: [300]} %}

Lisa is a senior software developer working for iCure. She is certified in eco-design of digital services and passionate about the environmental transition and digital transformation.

### The impact of IT

Let’s kick off with some shocking numbers on the IT industry.

Computing technologies are part of the daily life of 5 billions of users with 34 billions of connected devices, and it’s estimated that these numbers will double by 2025! 😱

Also the environmental costs of IT’s ever-expanding presence are skyrocketing. Here are some figures:

- The IT industry produces 4% of the greenhouse gas emissions in the world (more than the aviation sector which is responsible only for 2% of emissions)
- It takes 10% of the world-wide electricity consumption
- It is responsible for abiotic resources depletion
- It perpetrates inhumane working conditions. In the Democratic Republic of Congo 6 million of workers died in coltan mines, a material used to produce electronics.

Let’s break the IT industry into its component to understand why it has such a big ecological impact.There are three main actors in IT:

1. The end user device
2. The network infrastructure
3. The data centres

We can identify two sources of impact:

1. The manufacture of equipments
2. The manufacture of electricity

Even if data centres conjure the image of the most energy-consuming part of IT industry, it is the end user devices that are responsible for most of the environmental impact - and especially their manufacture!

{% image {src: "./blog/guest-blogs/images/techtalks-summer-2021-img1.pdf", alt: "a table showing that end user devices have by far the highest ecological impact (67,2%, compared to 12,3% of networks and 20,6% of data centres)", widths: [300,600,1000]} %}

Of all end user devices the top 3 with the biggest environmental impact are the

1. TV (14%)
2. Desktop (7,5%)
3. Laptop (7%)

Maybe you too were expecting to see the smartphone showing up as number one? The reason why it doesn’t is that this ranking takes into account impact due to both manufacturing and use. With 4,5% the smartphone only comes sixth in the list but here’s the caveat: while it has a negligible impact in terms of usage (it doesn’t need to be plugged to energy to function) the smartphone has the highest impact for manufacturing only.

### What can we do as citizen?

As citizens we can strive towards a digital sobriety approach: try to buy less equipment which lasts longer and is really useful.
We should always ask ourself the question “Do I really need this equipment?” before buying another tech gadget.
If the answer is yes, well, one can still decide to choose a product with an eco-certification which takes into account both its ecological and the social costs. The most commons eco-certifications for tech products are:

- **TCO** Smartphones, tablets, computers, monitors, headphones, projectors
- **EPEAT** Same as TCO + tv, printers, servers
- **Blue Angel** Printers, Bureaucratic paper
- **FSC** Recycled paper, coming from sustainable forests

The main reason of changing our devices is that they become too slow, because software and applications are becoming heavier and heavier. As consumers we don’t have much agency on that, but as tech professionals we do. Which brings us to the next question.

### What can we do as IT professionals?

When most developers think about disability they have a similarly narrow mental image of it: they think exclusively of visual disability, screen readers and braille devices. So they tend to focus solely on that issue, while the spectrum, also for what concerns apps and website users, is much broader.

The outcome of a research on the use of disability settings by the dutch company [Q42](https://werkenbij.q42.nl/) shows it well. The most used disability feature is reciting tex (33%), which makes sense in relation to the visually impaired or the elderly. But the second most used feature is an interesting reveal: dark mode (27%) used to prevent tired eyes and increase contrast, which illustrates the aforementioned broad spectrum of disabilities and how accessibility can also benefit people without disabilities.

### WCAG (Web Content Accessibility Guidelines)

We could choose to eco-design a digital service, which means trying to decrease its environmental impact by improving its conception and realisation. Which is basically a twofold operation: on one hand trying to increase the lifetime of end user devices, on the other trying to decrease the physical resources needed to run our software.

The equivalent of the “Do I really need this equipment?” question for tech professionals is “Do I really need this functionality/feature?”. To keep in line with the digital sobriety approach we should focus on the users’ needs instead of their wishes.

### Eco-designing your service

The good practices discussed here are based on the book [Éco-conception web: Les 115 bonnes pratiques](https://www.eyrolles.com/Informatique/Livre/ecoconception-web-les-115-bonnes-pratiques-9782416006272/) (FR only)

- Assess the current situation by measuring your website’s environmental footprint (a couple oh handy plugins are [GreenIT Analysis Plugin](https://chrome.google.com/webstore/detail/greenit-analysis/mofbfhffeklkbebfclfaiifefjflcpad?hl=en) or [Google LightHouse](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk?hl=en))
- Remove the non-essential functionalities
- Favour a simple design and optimise UX (good practices can be found on [this guide](https://eco-conception.designersethiques.org/guide/en/) )
- Optimise your images by compressing them (with online tools such as [Kraken](https://kraken.io/) or [Compressor](https://compressor.io/)), resizing them, choosing the appropriate format, or using CSS over images.
- Use a green web hosting solution (you can fins a list in the [Green Hosting Directory](https://www.thegreenwebfoundation.org/directory/))
- Limit the number of HTTP requests
- Offer asynchronous treatment where possible
- Optimise requests to the database by using index and cache
- Implement a modular architecture
- Include a circuit-breaker in your solution

As developers we can implement only 20% of these eco-design practices - the remaining 80% concerns the before and after of writing code, which calls for a holistic approach to eco-design.

#### Some tips & tools

[To calculate accessibility score of your website](https://wave.webaim.org/)
[To share files](https://filevert.fr/)
[For secured visio-conferences](https://www.infomaniak.com/fr/kmeet)
[To avoid WordPress to create a simple website](https://gohugo.io/)
To repair your devices : [Repaircafe](https://repaircafe.org/fr/) & [Fixware](https://www.fixware.be/)
[To buy reconditioned devices](https://www.asmartworld.be/)

#### Asma Oualmakran - Application security: Finding your way through buzzwords

{% image {src: "./blog/guest-blogs/images/techtalks-autumn-2021-img5.png", alt: "a visual representation of how a satellite measures the fraction of reflected solar radiation", widths: [300,600,1000]} %}

Asma is a Software Security Consultant at Software Improvement Group. She started as a general software person and then decided to specialise in security. Outside of her consultant role she is also a security officer, part of the research and development team (R&D) and a technical consultant.

#### Some vocabulary

Cybercrime has been making the headlines, especially after covid. According to the European Union Agency for Cybersecurity (ENISA) the top 15 cyber threats cyber threats emerged from the pandemic are the ones illustrated in this image:

{% image {src: "./blog/guest-blogs/images/techtalks-summer-2021-img2.png", alt: "1 Malware, 2 Web-based attacks, 3 Phishing, 4 Web application attacks, 5 Spam, 6 DDos, 7 Identity theft, 8 Data breach, 9 Insider threat, 10 Botnets, 11 Physical manipulation, damage, theft and loss, 12 Information leakage, 13 Ransomware, 14 Cyberespionage, 15 Cryptojacking", widths: [300,600,1000]} %}

First of all let’s define some fundamental cybersecurity concepts:

- **Threat** An attacker or situation that might cause a weakness to become a security incident
- **Risk** An assessment of an unwanted event based on a threat, considering chance and impact
- **Weakness** A shortcoming that might lead to a security incident. All known software and hardware weaknesses are listed in the format of Common Weakness Enumeration (CWE) in the reference library MITRE
- **Vulnerability** A weakness that is exploitable. Known vulnerabilities are also listed in a reference library called NVD, in the format of Common Vulnerability Enumeration (CVE). Each CVE has a common vulnerability scoring system rating (CVSS).

Let’s look at these concepts in practice in a case study.

- **Situation Company** stores user passwords unencrypted in an unprotected database
- **Threat** An attacker might be able to abuse user credentials.
- **Risk** It is highly probable that user credentials can be abused as the database is not protected. A breach causes high reputation damage.
- **Weakness** Listed on the CWE as CWE-256: Plaintext Storage of a Password Storing a password in plaintext may result in a system compromise.
- **Vulnerability** An attacker can abuse user credentials. Listed on the CVE as CVE-2020-17511: a vulnerability occurred in Airflow versions prior to 1.10.13, when creating a user using Airflow CLI, the password gets logged in plain text in the Log table in Airflow Metadatase. Same happened when creating a Connection with a password field.

#### Best practices and good practices that backfire

There are two ways to uncover weaknesses and vulnerability:

- **Penetration testing** (from outside in) Is a testing strategy to find vulnerabilities in a running application. This can be done manually or using Dynamic Application Security Tools (DAST)
- **Code Inspection** (from inside out) Scanning the code for vulnerabilities and requirements compliance.

Both are necessary because a code inspection spots issues that are unacknowledged by a penetration test.
That’s why some catchphrases often heard in the tech industry, meaning to show how they comply with good practices, can actually backfire:

- **“We’re doing our yearly pentest (penetration testing) so our code is secure!”**
  We already know that penetration test cannot catch the entirety of an application’s vulnerabilities. In addition to that, penetration test happens late in the process, when fixing issues can be 10-100 times more expensive. This late rework can cause rushed fixes, with no compliance to industry standards and regulations. In terms of workflow, separating security issues from “regular” development work, fixing issues might be postponed.

- **“We are fixing security by buying code inspection tools!”**
  The issue with this approach is that tools cannot find every vulnerability. The high complexity and the large output of the tools can be overwhelming for the team, without an appropriate training or guidance.

#### Software Development Life Cycle and DevSecOps

If you look at a classic Software Development Life Cycle (SDLC) you will notice that security practices are implemented very late in the cycle.

{% image {src: "./blog/guest-blogs/images/techtalks-summer-2021-img3.pdf", alt: "there are 6 phasse in the cycle (visualization of a software development cycle in six phases: Analysis, Design, Development, Testing, Deployment and Maintenance. Security practices come into play only in the penultimate step, between deployment and maintenance", widths: [300,600,1000]} %}

A better way to integrate security in a SDLC could be DevSecOps, where each phase has a security test associated to it. The idea is to treat security as a feature, not only as a requirement.

{% image {src: "./blog/guest-blogs/images/techtalks-summer-2021-img3.pdf", alt: "there are 6 phase in the cycle (visualization of a DevSecOps approach where security practices are integrated in each step of the cycle: analysis is paired with security requirement, design with threat modelling and security by design, development with vulnerability scanning and opensource health, testing with security testing, deployment with security configuration, maintenance with vulnerability scanning and opensource health.", widths: [300,600,1000]} %}

If you are following an Agile workflow you are probably not so sure where and how to integrate security: tracking and dealing with security is one of Agile Development’s blind spots, as articulated in [Agile Application Security](https://www.oreilly.com/library/view/agile-application-security/9781491938836/)

#### Summing up

Here are main takeaways on security:

- Security is not a one-time thing
- Tooling alone is not enough
- Security practices need to be more integrated in the SDLC
- Proper package management is needed to keep software secure
- Training and awareness are needed

#### The developer's security toolkit

- **Security code scanning tools** Checkmarx, Veracode, Fortify, Coverity, Sigrid
- **Opensource health** Snyk, Blackduck, Whitesource, Sigrid
- **Maintainability measurement** SonarQube, Sigrid
- **Process maturity guidelines and testing** OWASP SAMM , BSIMM, CIP
- **Training tools** Secure code warrior, Secure Flag, Codebashing
- **Security references** NVD, MITRE, ASVS, OWASP Top 10

## Liza Morrison - Be Qwick, don’t ship JavaScript

{% image {src: "./blog/guest-blogs/images/techtalks-marta.png", alt: "Marta Luffarelli", widths: [300]} %}

Liza Morrison is a software engineer from the United States, who specializes in front-end development. She moved to Belgium a year ago and has recently joined as a developer at Rosa.

### Performance and speed

The harsh truth is that 40% of visitors are going to leave your page if that doesn’t display correctly within the first 3 seconds.

Today speed is everything, especially on the web. Not only for user experience and for those who are constantly in a hurry: having a top performance score is also going to improve the SEO (Search Engine Optimisation) of your page.

Time To Interactive (TTI), that is how long it takes your page to become fully interactive, is also an important metric for performance.

### Ship less JavaScript

When a website scores poorly on performance the blame will fall on the the developers, but what is it was the framework’s fault instead?

A common problem in software design is that as the application becomes more features are added, performance decays. One solution to have an increasingly complex application whose performance rating stays the same is to ship less JavaScript.

[Qwick](https://qwik.builder.io/) is a new opensource framework designed for the fastest possible page load time. It focuses on HTML : before it displays the component then it makes it interactive. Qwick skips the TTO phase: it starts on the server side and downloading the Qwickloader, a tiny piece of JavaScript (less than 1KB) that knows how to download the rest of the application on an as-needed basis.

### Qwick's architecture

Frameworks divide in mainly 2 types of architecture:

- **Monolith** (eg Angular, React, Vue etc) the website is one large application. The browser downloads the application’s JavaScript, executes it and starts hydration process, using client-side JavaScript to add application state and interactivity to server-rendered HTML. Since these frameworks have a lazy loading approach, they load components that are visible in the page.

- **Island aka Microservices** (eg Astro)The application is made out of single business units, each of them responsible for a feature. The downside is that each of them has to be bootstrapped individually and there is no easy way for them to interact with each other.

Qwick sits between the two because it breaks the application in many little JavaScript bundles. When the user interacts with the UI only that component is rendered are only its JavaScript is executed.
