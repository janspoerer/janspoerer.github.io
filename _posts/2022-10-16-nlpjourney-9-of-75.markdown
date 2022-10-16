---
layout: post
title: "2022-10-14: Update 9/75 - Dataset - Make or Take"
date: 2022-10-14
categories: post
tags: phd
is_series: true
series_title: "75 Steps Toward a Ph.D. in NLP"
image: "/assets/images/2022-10-16.jpg"
# https://shantoroy.com/jekyll/add-latex-math-to-jekyll-blog-minimal-mistakes/
---
<script type="text/javascript" async
    src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.6/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        extensions: ["tex2jax.js"],
        jax: ["input/TeX", "output/HTML-CSS"],
        tex2jax: {
        inlineMath: [ ['$','$'], ["\\(","\\)"] ],
        displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
        processEscapes: true
        },
        "HTML-CSS": { availableFonts: ["TeX"] }
    });
</script>

This week, I tried to decide between taking an existing dataset for question answering for financial documents vs. making a new one.

I gathered some pros and cons, and identified potential datasets.

My supervisor and I will discuss the results and make a decision in the upcoming week.

You can follow these updates on: [Substack](https://nlpjourney.substack.com/) [Blog](https://janspoerer.github.io/phdstudies/) [Telegram](https://t.me/+gmkAaVlKPh4xZTky) [WhatsApp](https://chat.whatsapp.com/F6901LMMJWIGlxrahkgBcq) [LinkedIn](https://www.linkedin.com/in/janspoerer/) [Medium](https://medium.com/@janspoerer/about) [Twitter](https://twitter.com/JanSpoerer) [Calendly](https://calendly.com/janspoerer/60m-private)

![This large screen makes me more productive.]({{ page.image }})
<sup>This large screen makes me more productive.</sup>

## What Happened Since Last Week?

I finished the other half of the book "How to Write and Publish a Scientific Paper" by Robert Day. Good book.

My supervisor suggested a dataset that I might use for benchmarking my algorithms. If this dataset is suitable for my research, it can save me much time as I would not have to create a dataset on my own. I reflected on this dataset and am not sure if it is suitable for me. I will discuss this with my supervisor on Tuesday.

My colleague [Thomas Huber](https://www.linkedin.com/in/thomas-huber-a74396119/) held a presentation at the [Chair of Data Science and NLP](https://ics.unisg.ch/chair-ds-nlp-handschuh/) about the introspection of transformer-based language models [[LM-Debugger - An Interactive Tool for Inspection and Intervention in Transformer-Based Language Models (Geva et al, 2022)](https://arxiv.org/abs/2204.12130)]. The paper presents a method to accurately change the behavior of language models for specific prompts (among other research contributions).

On the private side of things, I catched up with my friends [Johannes Diehl](https://www.linkedin.com/in/johannes-diehl/) and [Kim Schröter](https://www.linkedin.com/in/kim-lara-schroeter/). They spent the weekend in Bonn and we drank a couple of Apfelwein together. Thanks for the good time!

## What Were the Biggest Obstacles?

No major obstacles. I left the phone at home again today, and it was great.

## Which Goals Did I Meet?

<ol>
  <li>Write one section for the first paper. The first paper will be a literature review/state-of-the-art.</li>
  <li>Identify a conference for the state-of-the-art.</li>
</ol>

## Which Goals Did I Miss?

<ol>
  <li>Align the outlet (conference) with my supervisor. (I.e., ask him if he likes the conference and thinks that it fits my research question.</li>
</ol>

## Was It a Good Week?

No. My progress reading books about academic writing was good. But my reading and coding progress was poor. 

I missed all goals that I originally intended to achieve.

## Short-Term Tasks for The Coming Week

<ol>
  <li>Align the outlet (conference) with my supervisor. (I.e., ask him if he likes the conference and thinks that it fits my research question.</li>
  <li>Decide on whether to prepare a dataset ourselves or take an existing dataset.</li>
</ol>

____________________________________

## About "75-Step Journey Toward a Ph.D. in Natural Language Processing"

You will, from now on, witness my grind. Feel my blood, sweat, and tears.

With this series of articles, you become a real-life weekly witness of my dissertation progress, all in 75 steps. This has multiple purposes: 

1) Forcing myself to keep moving through the power of public shame!

2) Helping other (prospective) Ph.D. students to stay motivated and to show that hard times are normal when going through this process. 

3) Getting support from the community when I go through hard times.

Share this with your Ph.D. student friends: [Substack](https://nlpjourney.substack.com/) [Blog](https://janspoerer.github.io/phdstudies/) [Telegram](https://t.me/+gmkAaVlKPh4xZTky) [WhatsApp](https://chat.whatsapp.com/F6901LMMJWIGlxrahkgBcq) [LinkedIn](https://www.linkedin.com/in/janspoerer/) [Medium](https://medium.com/@janspoerer/about) [Twitter](https://twitter.com/JanSpoerer) [Calendly](https://calendly.com/janspoerer/60m-private).

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