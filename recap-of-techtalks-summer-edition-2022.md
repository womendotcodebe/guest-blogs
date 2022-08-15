---
title: Recap of our TechTalks summer edition 2022
date: 2022-07-23
author: "federicab"
category: "techtalks"
tags:
    - post
    - guest-post
layout: article
metaIMG: "womendotcodebe-techtalks-recap-sept2021.jpg"
featured: true
---

Buckle up for the recap of another eclectic edition of our TechTalks!
Lisa Trapletti shared some tips on how to eco-design our system, Asma Oualmakran demystified cybersecurity buzzwords, and Liza Morrison walked us through a brand-new framework, Qwik.

<!-- excerpt -->

## A path to sustainable IT. Eco-designing its digital services by Lisa Trapletti

{% image {src: "./blog/guest-blogs/images/techtalks-lisa-trapletti.jpg", alt: "Lisa Trapletti", widths: [300]} %}

Lisa is a senior software developer working for iCure. She is certified in eco-design of digital services and passionate about the environmental transition and digital transformation.

### The impact of IT

Let’s kick off with some shocking numbers on the IT industry.

With 34 billions of connected devices, computing technologies are part of 5 billions of users's daily life. And it’s estimated that these numbers will double by 2025! 😱

The environmental costs of IT’s ever-expanding presence are skyrocketing too. Here are some figures:

- The IT industry produces 4% of the greenhouse gas (GHG) emissions in the world (more than the aviation sector, which is responsible for 2% of GHG emissions)
- It takes 10% of the world-wide electricity consumption
- It is responsible for abiotic resources depletion
- It perpetrates inhumane working conditions. In the Democratic Republic of Congo 6 million of workers died in coltan mines, a material used to produce electronics.

Let’s break the IT industry into smaller components to understand why it has such a big ecological impact. There are three main actors in IT:

1. The end user device
2. The network infrastructure
3. The data centres

We can identify two sources of impact:

1. The manufacture of equipment
2. The manufacture of electricity

Even if data centres conjure the image of the most energy-consuming part of IT industry, it's the end user devices that are responsible for most of the environmental impact - and especially their manufacture!

{% image {src: "./blog/guest-blogs/images/techtalks-summer-2022-img1.jpg", alt: "a table showing that end user devices have by far the highest ecological impact (67,2%, compared to 12,3% of networks and 20,6% of data centres)", widths: [300,600,1000]} %}

Of all end user devices the top 3 with the biggest environmental impact are:

1. TV (14%)
2. Desktop (7,5%)
3. Laptop (7%)

Maybe you too were expecting to see the smartphone showing up as number one? With 4,5% the smartphone only comes sixth in the list but here’s the caveat: this ranking takes into account impact due to both manufacturing and use. While the smartphone has a negligible impact in terms of usage (it doesn’t need to be plugged in to function) it has the highest impact for manufacturing only.

### What can we do as citizens?

As citizens we can adopt a digital sobriety approach: try to buy less equipment, and when we do, go for something useful and long-lasting.
We should always ask ourself the question “Do I really need this equipment?” before buying another tech gadget.
If the answer is yes, we can still choose a product with an eco-certification which takes into account both its ecological and social costs. The most commons eco-certifications for tech products are:

- **TCO** Smartphones, tablets, computers, monitors, headphones, projectors
- **EPEAT** Same as TCO + tv, printers, servers
- **Blue Angel** Printers, Bureaucratic paper
- **FSC** Recycled paper, coming from sustainable forests

The main reason why we buy new electronics is that, as software and applications are becoming heavier and heavier, our devices become too slow. As consumers we don’t have much agency on that, but as tech professionals we do. Which brings us to the next question.

### What can we do as IT professionals?

We can choose to eco-design a digital service, which means trying to decrease its environmental impact by improving its concept and production. Eco-design is a twofold operation: on one hand trying to increase the lifetime of end user devices, on the other trying to decrease the physical resources needed to run our software.

The equivalent of the “Do I really need this equipment?” question for tech professionals is “Do I really need this functionality/feature?”. To keep in line with the digital sobriety approach we should focus on the users’ needs instead of their wishes.

### Eco-designing your service

The good practices discussed here are based on the book [Éco-conception web: Les 115 bonnes pratiques](https://www.eyrolles.com/Informatique/Livre/ecoconception-web-les-115-bonnes-pratiques-9782416006272/) (FR only)

- Assess the current situation by measuring your website’s environmental footprint (a couple oh handy plugins are [GreenIT Analysis Plugin](https://chrome.google.com/webstore/detail/greenit-analysis/mofbfhffeklkbebfclfaiifefjflcpad?hl=en) or [Google LightHouse](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk?hl=en))
- Remove non-essential functionalities
- Favour a simple design and optimise UX (good practices can be found on [this guide](https://eco-conception.designersethiques.org/guide/en/) )
- Optimise images by compressing them (with online tools such as [Kraken](https://kraken.io/) or [Compressor](https://compressor.io/)), resizing them, choosing the appropriate format, or using CSS over images
- Use a green web hosting solution (you can fins a list in the [Green Hosting Directory](https://www.thegreenwebfoundation.org/directory/))
- Limit the number of HTTP requests
- Offer asynchronous treatment where possible
- Optimise requests to the database by using index and cache
- Implement a modular architecture
- Include a circuit-breaker in your solution

As developers we can implement only 20% of the eco-design practices discussed in the book - the remaining 80% concerns the before and after of writing code. This calls for a holistic approach to eco-design.

#### Some tips & tools

* [To calculate accessibility score of your website](https://wave.webaim.org/)
* [To share files](https://filevert.fr/)
* [For secured visio-conferences](https://www.infomaniak.com/fr/kmeet)
* [To avoid WordPress to create a simple website](https://gohugo.io/)
* To repair your devices : [Repaircafe](https://repaircafe.org/fr/) & [Fixware](https://www.fixware.be/)
* [To buy reconditioned devices](https://www.asmartworld.be/)

## Application security: Finding your way through buzzwords by Asma Oualmakran

{% image {src: "./blog/guest-blogs/images/techtalks-asma-oualmakran.jpg", alt: "Asma OUalmakran", widths: [300]} %}

Asma is a Software Security Consultant at Software Improvement Group. She started as a general software person and then decided to specialise in security. Outside of her consultant role she is also a security officer, part of the research and development team (R&D) and a technical consultant.

### Some vocabulary

Cyber crime has been making the headlines, especially after covid. According to the European Union Agency for Cybersecurity (ENISA) the top 15 cyber threats emerged from the pandemic are the ones illustrated in this image:

{% image {src: "./blog/guest-blogs/images/techtalks-summer-2022-img2.png", alt: "1 Malware, 2 Web-based attacks, 3 Phishing, 4 Web application attacks, 5 Spam, 6 DDos, 7 Identity theft, 8 Data breach, 9 Insider threat, 10 Botnets, 11 Physical manipulation, damage, theft and loss, 12 Information leakage, 13 Ransomware, 14 Cyberespionage, 15 Cryptojacking", widths: [300,600,1000]} %}

Let’s define some fundamental cybersecurity concepts:

- **Threat** An attacker or situation that might cause a weakness to become a security incident
- **Risk** An assessment of an unwanted event based on a threat, considering chance and impact
- **Weakness** A shortcoming that might lead to a security incident. All known software and hardware weaknesses are listed in the format of Common Weakness Enumeration (CWE) in the reference library MITRE
- **Vulnerability** A weakness that is exploitable. Known vulnerabilities are listed in a reference library called NVD, in the format of Common Vulnerability Enumeration (CVE)

Let’s look at these concepts in practice in a case study:

- **Situation** A company stores user passwords unencrypted in an unprotected database
- **Threat** An attacker might be able to abuse user credentials
- **Risk** It is highly probable that user credentials can be abused as the database is not protected. A breach causes high reputation damage
- **Weakness** Listed on the CWE as CWE-256: Plaintext Storage of a PasswordStoring a password in plaintext may result in a system compromise
- **Vulnerability** An attacker can abuse user credentials. Listed on the CVE as CVE-2020-17511: a vulnerability occurred in Airflow versions prior to 1.10.13, when creating a user using Airflow CLI, the password gets logged in plain text in the Log table in Airflow Metadatase

### Best practices and good practices that backfire

There are two ways to uncover weaknesses and vulnerabilities:

- **Penetration testing** (from outside in) A testing strategy to find vulnerabilities in a running application. It can be done manually or using Dynamic Application Security Tools (DAST)
- **Code Inspection** (from inside out) Scanning the code for vulnerabilities and requirements compliance

Both are necessary because a code inspection spots issues that are unacknowledged by a penetration test.

Here are some catchphrases often heard in the tech industry. The person who pronounces them probably thinks their company is handling security pretty well, but these partial implementation of security good practices can actually make it worse:

- **“We’re doing our yearly pentest (penetration testing) so our code is secure!”**
  We already know that a penetration test cannot catch all the vulnerabilities in an application. In addition to that, the penetration test happens late in the process, when fixing issues can be 10-100 times more expensive. In terms of workflow is not ideal, because it separates security issues from “regular” development work, allowing fixing issues to be postponed. This late rework can cause rushed fixes, with no compliance to industry standards and regulations.

- **“We are fixing security by buying code inspection tools!”**
  The issue with this approach is that tools cannot find every vulnerability. Without an appropriate training or guidance the high complexity and the large output of these tools can be overwhelming for the team.

### Software Development Life Cycle and DevSecOps

If you look at a classic Software Development Life Cycle (SDLC) you will notice that security practices are implemented very late in the cycle.

{% image {src: "./blog/guest-blogs/images/techtalks-summer-2022-img3.jpg", alt: "there are 6 phasse in the cycle (visualization of a software development cycle in six phases: Analysis, Design, Development, Testing, Deployment and Maintenance. Security practices come into play only in the penultimate step, between deployment and maintenance", widths: [300,600,1000]} %}

A better way to integrate security in a SDLC could be DevSecOps, where each phase has a security test associated to it. The idea is to treat security as a feature, not only as a requirement.

{% image {src: "./blog/guest-blogs/images/techtalks-summer-2022-img3.jpg", alt: "there are 6 phase in the cycle (visualization of a DevSecOps approach where security practices are integrated in each step of the cycle: analysis is paired with security requirement, design with threat modelling and security by design, development with vulnerability scanning and opensource health, testing with security testing, deployment with security configuration, maintenance with vulnerability scanning and opensource health.", widths: [300,600,1000]} %}

If you work in an Agile team you are probably not so sure about how to integrate security practices: tracking and dealing with security is one of Agile Development’s blind spots. In [Agile Application Security](https://www.oreilly.com/library/view/agile-application-security/9781491938836/) you will find more information on how to integrate security in your workflow.

### Main takeaways

- Security is not a one-time thing
- Tooling alone is not enough
- Security practices need to be more integrated in the SDLC
- Proper package management is needed to keep software secure
- Training and awareness are needed

### The developer's security toolkit

- **Security code scanning tools** Checkmarx, Veracode, Fortify, Coverity, Sigrid
- **Opensource health** Snyk, Blackduck, Whitesource, Sigrid
- **Maintainability measurement** SonarQube, Sigrid
- **Process maturity guidelines and testing** OWASP SAMM , BSIMM, CIP
- **Training tools** Secure code warrior, Secure Flag, Codebashing
- **Security references** NVD, MITRE, ASVS, OWASP Top 10

## Be Qwik, don’t ship JavaScript by Liza Morrison

{% image {src: "./blog/guest-blogs/images/techtalks-liza-morisson.jpg", alt: "Liza Morisson, widths: [300]} %}

Liza Morrison is a software engineer from the United States, who specialises in front-end development. She moved to Belgium a year ago and has recently joined as a developer at Rosa.

### Performance and speed on the web

The harsh truth is that 40% of visitors are going to leave your page if it doesn’t display correctly within the first 3 seconds.

Today speed is everything, especially on the web. Not only for user experience and for those who are constantly in a hurry: having a top performance score is also going to improve the SEO (Search Engine Optimisation) of your page.

Time To Interactive (TTI), that is how long it takes your page to become fully interactive, is also an important metric for performance.

### Ship less JavaScript

When a website scores poorly on performance the blame falls on the the developer, but what if it was the framework’s fault instead?

A common problem in software design is that as more features are added to the application, performance decays. One solution to keep performance rating stable in an increasingly complex application is to ship less JavaScript.

[Qwik](https://qwik.builder.io/) is a new open source framework designed for the fastest possible page load time. It focuses on HTML : before it displays the component then it makes it interactive. Qwik skips the TTI phase: it starts on the server side and downloading the Qwikloader, a tiny piece of JavaScript (less than 1KB) that knows how to download the rest of the application on an as-needed basis.

### Qwik's architecture

Frameworks divide in mainly 2 types of architecture:

- **Monolith** (eg Angular, React, Vue etc) the website is one large application. The browser downloads the application’s JavaScript, executes it and starts hydration process, using client-side JavaScript to add application state and interactivity to server-rendered HTML. Since these frameworks have a lazy loading approach, they only load components as they become visible on the page.

- **Island aka Microservices** (eg Astro) The application is made out of single business units, each of them responsible for a feature. The downside is that each of them has to be bootstrapped individually and there is no easy way for them to interact with each other.

Qwik sits between the two because it breaks the application in many little JavaScript bundles. When the user interacts with the UI only that component is rendered are only its JavaScript is executed.

## Final thoughts

It's exciting to see how vast and uncharted the industry is: working in IT can mean being one of the few women in cybersecurity (currently the percentage is roughly 24%), caring about technology and the environment, using the latest framework to build light-speed pages, and many more! We loved the women-only vibe of the event - everyone was super attentive during the presentations and up for a chat during the breaks. It was a good one, until the next edition of TechTalks!
