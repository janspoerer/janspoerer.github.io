---
layout: post
title: "2022-10-09: Update 8/75 - Finding a Conference"
date: 2022-10-09
categories: post
tags: phd
is_series: true
series_title: "75 Steps Toward a Ph.D. in NLP"
image: "/assets/images/2022-10-09.jpg"
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

Reading the books displayed in this post’s picture created a sense of urgency for finding a venue for publication. 

Finding a potential conference or journal for my first paper was already crossed from my to-do list, and the next step is to align the selection with my supervisor.

You can follow these updates on: [Substack](https://nlpjourney.substack.com/) [Blog](https://janspoerer.github.io/phdstudies/) [Telegram](https://t.me/+gmkAaVlKPh4xZTky) [WhatsApp](https://chat.whatsapp.com/F6901LMMJWIGlxrahkgBcq) [LinkedIn](https://www.linkedin.com/in/janspoerer/) [Medium](https://medium.com/@janspoerer/about) [Twitter](https://twitter.com/JanSpoerer) [Calendly](https://calendly.com/janspoerer/30m)

![Two good books: 1) Scientific English and 2) How to Write and Publish a Scientific Paper.]({{ page.image }})
<sup>Two good books: 1) Scientific English and 2) How to Write and Publish a Scientific Paper.</sup>

## What Happened Since Last Week?

I have read a book about "Scientific English" (see picture) and read half of the book "How to Write and Publish a Scientific Paper". My supervisor suggested reading these books.

Who knows, maybe the grammar and style of these posts will improve! The books are certainly helpful for my writing, and I can recommend them. My supervisor suggested reading these books.

## What Were the Biggest Obstacles?

While last week’s post was a rant about my lack of focus, this week I simply did not put in enough time. No excuses here; I just prioritized work-related and other activities over working on my dissertation.

The learning from that is to be more realistic when agreeing to other activities. A couple of hours of non-Ph.D. work will often erase an entire day of dissertation progress.

## Which Goals Did I Meet?

None. 

Replacing tasks with other tasks is no excuse for not following through with plans. But I would still like to mention that I have at least read most of the above-mentioned books. (I only read half of “How to Write and Publish a Scientific Paper” so far.)

## Which Goals Did I Miss?

<ol>
  <li>Write one section for the first paper. The first paper will be a literature review/state-of-the-art.</li>
  <li>Identify a conference for the state-of-the-art.</li>
  <li>Align the outlet (conference) with my supervisor. (I.e., ask him if he likes the conference and thinks that it fits my research question.</li>
</ol>

## Was It a Good Week?

No. My progress reading books about academic writing was good. But my reading and coding progress was poor. 

I missed all goals that I originally intended to achieve.

## Short-Term Tasks for The Coming Week

<ol>
  <li>Write one section for the first paper. The first paper will be a literature review/state-of-the-art.</li>
  <li>Identify a conference for the state-of-the-art.</li>
  <li>Align the outlet (conference) with my supervisor. (I.e., ask him if he likes the conference and thinks that it fits to my research question.</li>
</ol>

____________________________________

## About "75-Step Journey Toward a Ph.D. in Natural Language Processing"

You will, from now on, witness my grind. Feel my blood, sweat, and tears.

With this series of articles, you become a real-life weekly witness of my dissertation progress, all in 75 steps. This has multiple purposes: 

1) Forcing myself to keep moving through the power of public shame!

2) Helping other (prospective) Ph.D. students to stay motivated and to show that hard times are normal when going through this process. 

3) Getting support from the community when I go through hard times.

Share this with your Ph.D. student friends: [Substack](https://nlpjourney.substack.com/) [Blog](https://janspoerer.github.io/phdstudies/) [Telegram](https://t.me/+gmkAaVlKPh4xZTky) [WhatsApp](https://chat.whatsapp.com/F6901LMMJWIGlxrahkgBcq) [LinkedIn](https://www.linkedin.com/in/janspoerer/) [Medium](https://medium.com/@janspoerer/about) [Twitter](https://twitter.com/JanSpoerer) [Calendly](https://calendly.com/janspoerer/30m).

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