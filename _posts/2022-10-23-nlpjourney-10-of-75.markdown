---
layout: post
title: "2022-10-23: Update 10/75 - Still Unsure About the Dataset"
date: 2022-10-23
categories: post
tags: phd
is_series: true
series_title: "75 Steps Toward a Ph.D. in NLP"
image: "/assets/images/2022-10-23.jpg"
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

All signs indicate that we will create our own dataset. There is no dataset yet for our domain-task combination. (I'm almost certain about that by now.)

That's a good thing because building a dataset allows us to venture into uncharted territory and possibly leave a big scientific mark in our field.

I hope to finalize the "dataset - make or take" question, which I originally planned to take this week, in the coming week... As mentioned, I am now even more certain than last week that we will "make" and not "take."

We want to be sure before we go in this direction. Building a dataset would involve a significant commitment of our resources.

You can follow these updates: [Substack](https://nlpjourney.substack.com/) [Blog](https://janspoerer.github.io/phdstudies/) [Telegram](https://t.me/+gmkAaVlKPh4xZTky) [WhatsApp](https://chat.whatsapp.com/F6901LMMJWIGlxrahkgBcq) [LinkedIn](https://www.linkedin.com/in/janspoerer/) [Medium](https://medium.com/@janspoerer/about) [Twitter](https://twitter.com/JanSpoerer) [Calendly](https://calendly.com/janspoerer/60m-private)

![I usually don't do Ph.D. work from Commerzbank's office, but it was convenient that day.]({{ page.image }})
<sup>I usually don't do Ph.D. work from Commerzbank's office, but it was convenient that day.</sup>

## What Happened Since Last Week?

I re-read a [paper (FinBERT, by Yang, Uy, Huang from 2020)](https://arxiv.org/abs/2006.08097) that I may cite in our research. To my delight, I noticed that since I last read this paper, I have understood **much** more.

It's always good to see that one is making progress.

Apart from that, I set up everything to start a website that can serve us to advertise and inform about our planned new dataset. These benchmarking/dataset websites usually contain a leaderboard (with the scores each research team has received on the dataset with their algorithms) and instructions for downloading, using, and evaluating the dataset.

## What Were the Biggest Obstacles?

All good. Great week!

## Which Goals Did I Meet?

<ol>
  <li>Align the outlet (conference) with my supervisor. (I.e., ask him if he likes the conference and thinks it fits my research question.</li>
  <li>Prepare a website for advertising our dataset. (This goal was not in the previous update, it came up spontaneously.)</li>
  <li>Write instructions for using our dataset in the format of a mini-paper. (This goal was not in the previous update, it came up spontaneously.)</li>
</ol>

## Which Goals Did I Miss?

<ol>
  <li>Decide on whether to prepare a dataset ourselves or take an existing dataset.</li>
</ol>

## Was It a Good Week?

Yes.

I re-activated my YouTube Premium subscriptions and noticed that listening to music without interruptions is a significant productivity boost for me.

## Short-Term Tasks for The Coming Week

<ol>
  <li>None. I'll wait and see what comes up in Tuesday's meeting with my supervisor. Now that I have meetings with my supervisor on Tuesdays, I have less certainty about my weekly to-dos on Sundays.
  </li>
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