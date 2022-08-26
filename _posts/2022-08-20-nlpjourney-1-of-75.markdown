---
layout: post
title: "2022-08-20: Update 1/75 - Kicking Off the Journey Toward a Ph.D. in NLP"
date: 2022-08-20
categories: post
tags: phd
is_series: true
series_title: "75 Steps Toward a Ph.D. in NLP"
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

Nice that you've clicked through!

This is just the beginning of a lengthy process of writing my Ph.D. dissertation in Natural Language Processing, and you will be my real-time weekly witness!

These weekly updates will always be structured in the same way. So let's get started.

You can follow these updates on: [Substack](https://nlpjourney.substack.com/) [Blog](https://janspoerer.github.io/phdstudies/) [Telegram](https://t.me/+gmkAaVlKPh4xZTky) [WhatsApp](https://chat.whatsapp.com/F6901LMMJWIGlxrahkgBcq) [LinkedIn](https://www.linkedin.com/in/janspoerer/) [Medium](https://medium.com/@janspoerer/about) [Twitter](https://twitter.com/JanSpoerer) [Calendly](https://calendly.com/janspoerer/60m-private)

## What Happened Since Last Week?

I've set up a continuous integration pipeline for the code I'm working on. The code will now test itself automatically, and I will get notified if some code is broken. Code tests require proper test coverage monitoring to be helpful, so I've set up test coverage monitoring. I've also set up various other technical bits and pieces, such as a documentation template. The code is still in a private repository, but maybe this can be changed in the future! In another update, I'll go into more detail on my dissertation.

## What were the Biggest Obstacles?

I got distracted by demands from my job(s), which is the biggest no-go for this week.

## Which Goals Did I Meet?

I should mention that I've been enrolled in this Ph.D. program for two years already, and since then, I have finished the Ph.D. coursework and handed in my dissertation proposal. So now it's time to write articles.

## Which Goals Did I Miss?

I'll skip this. The second post will have this section!

## Was It a Good Week?

Yes! I feel some momentum to start documenting this journey and am happy to have you on board.

## Short-Term Tasks for The Coming Week

1) Make an appointment with my supervisor to discuss my Ph.D. dissertation proposal.

2) Go live for the GitLab documentation page of the Python module (I still need to figure out how to configure the hosting of this static documentation web page that I've already created this week).

3) First successful end-to-end document processing with the Python module (MVP). (With >80% test coverage and all tests passing.)

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