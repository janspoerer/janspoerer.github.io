---
layout: post
title: "2022-07-24: Project Portfolio"
date: 2022-07-24
categories: post
tags: spoerico
is_series: true
series_title: "Spoerico"
---
<sub>This article is updated on an ongoing basis. Latest change: 2022-11-10. See the [version history of this repository](https://github.com/janspoerer/janspoerer.github.io/blob/main/_posts/2022-07-24-project-portfolio.markdown) for exact versioning.</sub>

## CV
My first freelance project started in August 2017, right after my undergrad in International Management from WHU. Back then, I helped a startup to raise money and professionalize their accounting and controlling. The full-time project lasted for about four months.

From early 2018, a year of working on a software startup followed. We developed a tool to improve banks' Know Your Customer (KYC) processes.

In the summer of 2018, I did a web development bootcamp at Le Wagon in Berlin to deepen my coding skills. Shortly after that, a year after undergrad, I enrolled in the first intake of the newly-created Applied Data Science program at Frankfurt School of Finance & Management.

In 2019, I got excited about crypto while attending a blockchain elective at Frankfurt School, held by [Prof. Dr. Philipp Sandner](https://www.linkedin.com/in/philippsandner/) and [Christoph Kreiterling](https://www.linkedin.com/in/christoph-kreiterling/). I freelanced for multiple companies and implemented backtesting solutions for them, and these were my first highly technical freelancing projects.

In 2020, I graduated from [Frankfurt School](https://www.frankfurt-school.de/en/home/programmes/master/data-science) and started to work at Commerzbank AG as a software engineer. Today, I am working as a software engineer in Commerzbank's DLT/Blockchain Lab.

In the same year, I enrolled in a Ph.D. program in computer science at the [University of St. Gallen](https://ics.unisg.ch/chair-ds-nlp-handschuh/). Find more about it [here](/phdstudies).

Furthermore, I co-founded [21e6 Capital AG](https://assets.21e6.io/), a startup that provides investment advice to professional investors seeking to invest in crypto markets. I am still involved here, and the business is developing beyond my expectations. We have a first-class team of quant portfolio analysts and crypto experts. We have three business areas: 1) consulting, 2) fund of funds, and 3) other financial products; 2) is our primary business.

## Projects

### 2022

* DLT Lab Commerzbank
    * Worked on a self-sovereign identity application based on Java Spring Boot and Angular.
    * Organized monthly "DLT Affiliate Call" to align interested employees on DLT-related activities within the bank.
    * Held numerous knowledge sharing presentations for colleagues interested in crypto/DLT.
    * Supervised junior software development colleagues.
* University of St. Gallen
    * Completed the proposal for my dissertation.
    * Outlined a software infrastructure for processing financial texts.
    * [Please refer to my Ph.D. blog posts to see the most recent progress.](https://janspoerer.github.io/post/2022/08/20/nlpjourney-1-of-75.html)
* 21e6 Capital AG
    * Launched the fund of funds, our flagship product, in April 2022.
    * We achieved exceptional performance of the fund of funds throughout the Q2 crypto meltdown.

### 2021

* DLT Lab Commerzbank
    * Assisted in a request for proposal (RfP): created proposal documents, managed bidder workshops, evaluated proposals, managed internal stakeholders from different divisions, ensured compliance with internal guidelines.
    * Created a full-stack application (based on React.js, Python Flask, Java Spring Boot, and enterprise-internal services) that allows clients to have decentralized identity information signed by Commerzbank.
* Trading Infrastructure Commerzbank
    * Developed a FIX converter in Java for new FIX connections. FIX converters are used to translate financial messages from other financial companies into one's own data infrastructure.
    * Smaller data wrangling in a Front Arena trading application.
* 21e6 Capital AG
    * Set up a data infrastructure for 21e6 with data of about 1000 crypto funds. Created a data pipeline for monthly performance data for crypto funds.
    * High-touch outreach to crypto funds; due diligence. Talked to many crypto fund managers to assess their suitability for the 21e6 Crypto Fund of Funds (21e6 Crypto FoF).
    * We hired seasoned professionals and received funding commitments to scale the business. The Swiss 21e6 Capital AG (stock-based corporation, Aktiengesellschaft) was incorporated.
* University of St. Gallen
    * Completed Ph.D. courses in econometrics, natural language processing, and software for AI (S4AI). 
* Spoerico GmbH
    * Incorporated a GmbH to bundle my business activities into a more professional corporate structure/legal entity to reduce personal liability and to reduce my tax burden.
    * Developed a massive scraper-based product for a large HR/recruitment agency (Personalvermittlung/Headhunter).
    * Failed to get a permanent software-as-a-service contract.
    * Put the scraper on my shelf; maybe it becomes useful later. (A partner and I own all rights.)

### 2020

* Commerzbank Big Data Division
    * Continued development of a D3-/React-based web UI for transaction monitoring (network diagram).
    * Implemented a micro application with Java Servlets and connected it to an HBase.
    * Deployed the micro application with OpenShift.
* 21e6 Capital AG
    * Developed and refined a business model for the startup.
    * High-touch outreach to professional investors (sales) to test the market. Business development and hypothesis validation.

### 2019

* ITSA e.V.: Occasionally supporting ITSA in promoting their blockchain database (TOKENBASE) through creating insightful visualizations and stories from their data. Created Tableau-based diagram templates that produce insightful visualizations about the blockchain space.
* Conducted a comprehensive market study for a Swiss private equity company.
* Developed a comprehensive backtesting software in Python that provides practically all financial metrics relevant for (quantitative) asset managers. The key characteristic of the software is that it has an interface to blockchain price data, making backtesting for algorithmic blockchain trading possible relatively easily. Analyses of the software were sold to several companies, but the source code is still owned by me and can be used again.
* Supported a German startup in the luxury segment with finance, accounting, and ERP issues.

Specific areas of competence included: Cost center accounting, management accounting/controlling, cash management/treasury, venture capital financing, external reporting, profitability analyses, ERP troubleshooting, database design, competition analyses, algorithmic trading, backtesting, trading dashboard, risk management dashboards, text extraction, text classification, natural language processing, and web scraping.

## Freelancer Platform Profiles

* [Twago](https://www.twago.de/p/jan-sporer/433005/)
* [Apollo](https://www.apollo.io/companies/Jan-Sp-rer-Consulting/5e57ec274a6b110001ead30e)
* [Freelancermap](https://www.freelancermap.de/profile/139240/)

{% if page.is_series == true %}
    {% assign posts = site.posts | where: "is_series", true | where: "series_title", page.series_title | sort: 'date' %}
    {% if posts.size > 1 %}
        
<h3 class="text-success p-3 pb-0">Read More From the {{ page.series_title }} Series</h3>
        {% for post in posts %}
                {% if post.title == page.title %}
<p class="nav-link bullet-pointer mb-0">{{ post.title }}</p>
                {% else %}
<a class="nav-link bullet-hash" href="{{ post.url }}">{{ post.title }}</a>
                {% endif %}
        {% endfor %}
    {% endif %}
{% endif %}