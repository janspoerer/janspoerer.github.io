---
layout: post
title: "2022-10-02: Update 7/75 - Leaving the Phone at Home"
date: 2022-10-02
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

This week was a success, simply because I **left the phone at home on Thursday** and I was [ultraproductive](https://www.linkedin.com/posts/christianpoensgen_we-use-our-phones-from-the-moment-we-wake-activity-6938049822918651904-nBiJ?utm_source=share&utm_medium=member_desktop).

You can follow these updates on: [Substack](https://nlpjourney.substack.com/) [Blog](https://janspoerer.github.io/phdstudies/) [Telegram](https://t.me/+gmkAaVlKPh4xZTky) [WhatsApp](https://chat.whatsapp.com/F6901LMMJWIGlxrahkgBcq) [LinkedIn](https://www.linkedin.com/in/janspoerer/) [Medium](https://medium.com/@janspoerer/about) [Twitter](https://twitter.com/JanSpoerer) [Calendly](https://calendly.com/janspoerer/60m-private)

## What Happened Since Last Week?

I held a presentation about research methods in computer science on Friday.

The weekly with my supervisor was canceled due to an urgent unexpected issue that entered his schedule. That was compensated by scheduling my presentation on research methods for Friday. I got feedback on this presentation, and this replaced the weekly, so all is good.

## What Were the Biggest Obstacles?

This week brought me back on track. The biggest obstacle is usually called "me," and this week I was able to refocus by leaving my phone at home. 

## Which Goals Did I Meet?

<ul>
  <li>Done: <i>When generating answers from PDFs, the software should be able to track pages and titles (provide context for the result). This is essential for users because they typically need to verify whether the generated answers are correct manually.</i> </li>
  <li>Done: <i>Refine the presentation about research methods in computer science as per my supervisors' suggestions.</i></li>
  <li>Done: <i>Refine the research proposal using my supervisors' suggestions.</i></li>
</ul>

## Which Goals Did I Miss?

None.

## Was It a Good Week?

Yes. Learning: Leave the phone at home!

How can one leave the phone at home? It is not so easy! **These things help me to leave the phone at home**: 
<ol>
    <li>Having passwords ready that one needs to join calls (Google Meet and Microsoft Teams),</li>
    <li>having a two-factor authentication method that does not require a phone (Yubikey), and</li>
    <li>scheduling meetings in batches on one particular day or in short succession on the same day.</li>
</ol>

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