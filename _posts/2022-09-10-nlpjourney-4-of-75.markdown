---
layout: post
title: "2022-09-10: Update 4/75 - Long Test Runtime; Retriever Works"
date: 2022-09-10
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

For the first time, the model returns document-specific answers. To recap, retrieval-augmented generation is designed for the very purpose of finding and outputting information from the documents provided. But in previous weeks, I have not had an eye on the model outputs' quality. 

I wrote a software test to check whether document-provided information is prioritized over parameterized, language model knowledge. From now on, I will notice whether the model's quality has deteriorated significantly.

Retreival-augmented generators (RAG) have **two components**: a language model (parametric knowledge) and a retriever that accesses knowledge from texts/documents (non-parametric knowledge). If we ask RAG about the revenue of a well-known company for a specific year without giving a document that contains this answer, it will likely still provide the correct answer. It can achieve this by utilizing knowledge from the language model (parametric memory). But for more obscure knowledge, we cannot rely on the language model and need a powerful retriever that accesses documents.

Even though factual information is retrieved successfully from documents, I noticed that the model cannot properly identify synonyms such as "revenue" and "turnover." So when I provide a question asking about the **revenue** of a company in year X, the model will usually not be able to find this information when the documents say "The company had a **turnover** of Y in year X." **Fine-tuning the model to the financial domain will hopefully solve this issue.**

You can follow these updates on: [Substack](https://nlpjourney.substack.com/) [Blog](https://janspoerer.github.io/phdstudies/) [Telegram](https://t.me/+gmkAaVlKPh4xZTky) [WhatsApp](https://chat.whatsapp.com/F6901LMMJWIGlxrahkgBcq) [LinkedIn](https://www.linkedin.com/in/janspoerer/) [Medium](https://medium.com/@janspoerer/about) [Twitter](https://twitter.com/JanSpoerer) [Calendly](https://calendly.com/janspoerer/60m-private)

## What Happened Since Last Week?

I finally used Jo Karajanov's break suggestions. I had more uninterrupted time to work on Ph.D. tasks this week and it felt easier to do these small walking breaks every 15 minutes. I will continue to be more conscious about my break habits from now on, it really helps.

Leisure-wise, I will go mountain climbing tomorrow, on Germany's highest mountain, Zugspitze.

## What Were the Biggest Obstacles?

I struggled with handling command line arguments in Python, and especially with making those testable.

Also, the test runtime increased manifold this week. I added some end-to-end tests this week, and they take a very long time to run, even though they only perform inference. From now on, I have to test very carefully, only testing the modules that I've recently changed. A pre-commit test hook is implemented, meaning that the full set of tests will continue to run before every commit. (A commit is a versioning snapshot in coding. Each versioning snapshot should be working properly, so it is good practice to run tests before each snapshot.)

## Which Goals Did I Meet?

<ul>
  <li><b>CLI entry points:</b> To make the module more versatile, I want to provide a convenient command line entry point. A developer can point to a folder with input PDFs and insert the question/query, and can execute the program directly from the shell.</li>
  <li>Prepare the research proposal <b>meeting with my supervisors</b>.</li>
</ul>

## Which Goals Did I Miss?

When generating answers from PDFs, the software should be able to track pages and titles (provide context for the result). This is important for users because they oftne need to manually verify whether the generated answers are correct.

I was not able to complete this because I did not have enough time left to understand how Hugginface retrieval-augmented generation model handles contexts and how they can be accessed along with the answer result. I'll have to dig deeper into the model's implementation.

## Was It a Good Week?

Yes. I did not expect to be able to work on my tasks with so few interruptions. **This was the most productive week in a long time.** The context task was not successful, but that's ok.

## Short-Term Tasks for The Coming Week

<ol>
  <li>Carried over from last week: When generating answers from PDFs, the software should be able to track pages and titles (provide context for the result). This is important for users because they oftne need to manually verify whether the generated answers are correct.</li>
  <li>Start first paper, write outline, and identify initial outlets for publication.</li>
  <li>Conduct the research proposal meeting with my supervisors.</li>
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