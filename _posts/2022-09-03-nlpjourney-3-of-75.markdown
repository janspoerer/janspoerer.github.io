---
layout: post
title: "2022-09-04: Update 3/75 - Back on Track and Back to Vallendar"
date: 2022-09-04
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

**Let me finally give you some more detail on what I'm actually working on.** The first paper will probably be called "FinRAG," pointing to the combination between Retrieval-Augmented Generation (RAG, Lewis et al., 2020) and the application to the financial domain.

**FinRAG** will be a method that takes a set of PDFs and a question as input and will provide an **answer to the question based on the PDFs**. It will also provide the page number, the file name, and the context that the information was taken from. This is **relevant for financial and law professionals**, because they often need to manually double-check any machine-provided information to avoid mistakes.

You can follow these updates on: [Substack](https://nlpjourney.substack.com/) [Blog](https://janspoerer.github.io/phdstudies/) [Telegram](https://t.me/+gmkAaVlKPh4xZTky) [WhatsApp](https://chat.whatsapp.com/F6901LMMJWIGlxrahkgBcq) [LinkedIn](https://www.linkedin.com/in/janspoerer/) [Medium](https://medium.com/@janspoerer/about) [Twitter](https://twitter.com/JanSpoerer) [Calendly](https://calendly.com/janspoerer/60m-private)

## What Happened Since Last Week?

First off, I did not follow through with Jo Karajanov's suggestions to try a new approach to taking breaks. (Her approach: Take a break every 15 minutes by walking around for a minute in the room. After about three times, one can take a longer break or walk outside.) I jumped into work, and when I realized that I was not following the break method, it was already too late, and I preferred to just get the work done. Furthermore, the work involved waiting for a long time for the code to finish, so I was not fully utilized at all times. I will do this in the coming weeks!

I met with the organizers (Tolga Bastürk and Benedikt Buchner) of the Machine Learning Community in Commerzbank. We have set a date where I will present the latest developments in the field of document retrieval and retrieval-augmented generation.

On Saturday, I had an alumni event at my B.Sc. alma mater, WHU - Otto Beisheim School of Management in Vallendar. I met many old and some new people there, and I'm still tired from the outstanding party on Saturday. On the title picture, you can see one of the more relaxed moments of this event.

## What Were the Biggest Obstacles?

The computing power needed to produce embeddings for a new text might be higher than expected. **This might make near-time processing of user-inputted PDFs impossible**. My initially intended use case of uploading PDFs and a set of questions and then getting an answer immediately might thus be unrealistic at this point.

That could turn out to be a big problem. 

But I think and hope that I may have just made a mistake in the configuration of the algorithm, and the algorithm will be faster upon closer inspection.

## Which Goals Did I Meet?

Goal 1 from last week: My supervisors scheduled an appointment with me to discuss my research proposal. This will be in two weeks.

Goal 2 from last week: Shoutout to Thomas Huber for sending me a code snippet that I gratefully copied from. The MVP is now working (from PDF to a PDF-based answer)!

Goal 3 from last week: Added the planned set of literature about document retrieval and related methods to my literature database. 

## Which Goals Did I Miss?

Yay, all good this week!

## Was It a Good Week?

Yes, all goals met! The MVP goal was a big one. Scheduling the meeting with my supervisors was also crucial.

And I had a great WHU Alumni Homecoming on Saturday, and one of my besties and WHU friends Jan Tenenbaum came to visit from Berlin already on Friday. Thanks for the great time.

## Short-Term Tasks for The Coming Week

<ol>
  <li>When generating answers from PDFs, the software should be able to track pages and titles (provide context for the result). This is important for users because they often need to manually verify whether the generated answers are correct.</li>
  <li>CLI entry points: To make the module more versatile, I want to provide a convenient command line entry point. A developer can point to a folder with input PDFs and insert the question/query, and can execute the program directly from the shell.</li>
  <li>Prepare the research proposal meeting with my supervisors.</li>
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