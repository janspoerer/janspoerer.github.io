---
layout: post
title: "2022-09-26: Update 6/75 - Reading Group"
date: 2022-09-26
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

In the first regular weekly meeting with my supervisor, he asked me to make a presentation about a paper on research methods in computer science. I will take the methodology from this paper as a basis for my revised research proposal.

The presentation will be held in front of the chair in a couple of weeks.

I'm not sure whether the paper is supposed to be publicly available, so I do not provide a link to my Google Drive to the paper for now. But I will do so after confirming that it can be shared!

You can follow these updates on: [Substack](https://nlpjourney.substack.com/) [Blog](https://janspoerer.github.io/phdstudies/) [Telegram](https://t.me/+gmkAaVlKPh4xZTky) [WhatsApp](https://chat.whatsapp.com/F6901LMMJWIGlxrahkgBcq) [LinkedIn](https://www.linkedin.com/in/janspoerer/) [Medium](https://medium.com/@janspoerer/about) [Twitter](https://twitter.com/JanSpoerer) [Calendly](https://calendly.com/janspoerer/60m-private)

## What Happened Since Last Week?

I've read the paper proposed by my supervisor, summarized it, and made a presentation draft from it.

## What Were the Biggest Obstacles?

Besides the fact that there was too little time, everything was fine.

## Which Goals Did I Meet?

<ul>
  <li>Done: <i><b>Presentation on research methods in computer science: </b>The draft is done. Please note that this was an ad-hoc task that I did not mention in last week's post.</i></li>
  <li>Done: <i><b>Outline for my literature review paper: </b>The outline is done and ready for review by my supervisor.</i></li>
  <li>Done: <i><b>Improvements to the proposal: </b>The refined proposal with explicitly defined research questions and hypotheses (as per the methodology paper mentioned above) is done and ready for review by my supervisor.</i></li>
</ul>

## Which Goals Did I Miss?

<ul>
  <li>Miss: <i>When generating answers from PDFs, the software should be able to track pages and titles (provide context for the result). This is essential for users because they typically need to verify whether the generated answers are correct manually.</i> - I did not work on this.</li>
</ul>

## Was It a Good Week?

The paper on research methods in computer science was insightful. I have much more clarity now about my research plan and about how to approach my research articles.

But, I am still not satisfied with my focus. Thus, I am currently writing this weekly update while my phone is at home. The phone is a big issue that I need to be more aware of, and additionally I will again enforce that I have days without any meetings to have a less scattered daily structure. A synergy effect of having meeting-free days is that this eliminates the need to bring a phone.

## Short-Term Tasks for The Coming Week

<ol>
  <li>Refine the presentation about research methods in computer science as per my supervisors' suggestions.</li>
  <li>Refine the research proposal my supervisors' suggestions.</li>
  <li>Carried over from last week: When generating answers from PDFs, the software should be able to track pages and titles (provide context for the result). This is essential for users because they typically need to verify whether the generated answers are correct manually.</li>
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