---
layout: post
title: "2022-08-28: Update 2/75 - Literature Review"
date: 2022-08-28
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

Thanks for checking in for the second update - the first one with a weekly review.

If this is your first time reading an "NLP Journey in 75 Weekly Steps" update, welcome to being my real-time weekly witness on my journey toward getting a Ph.D.!

These weekly updates are always structured in the same way. So let's continue.

You can follow these updates on: [Substack](https://nlpjourney.substack.com/) [Blog](https://janspoerer.github.io/phdstudies/) [Telegram](https://t.me/+gmkAaVlKPh4xZTky) [WhatsApp](https://chat.whatsapp.com/F6901LMMJWIGlxrahkgBcq) [LinkedIn](https://www.linkedin.com/in/janspoerer/) [Medium](https://medium.com/@janspoerer/about) [Twitter](https://twitter.com/JanSpoerer) [Calendly](https://calendly.com/janspoerer/30m)

## What Happened Since Last Week?

I participated in the [Frankfurt Data Science Cocktail Night With DALL-E 2](https://www.meetup.com/de-DE/FrankfurtDataScience/?_cookie-check=qLxLguQbNAeLwUoJ) this week. Made a couple of new connections there and talked to many old ones. I recommend the [Frankfurt Data Science Meetup](https://www.meetup.com/de-DE/frankfurtdatascience/), make sure to check it out if and when you are in Frankfurt! The organizer is [Eldar Rakhmatullaev](https://www.linkedin.com/in/eldarr/), and this is their Meetup page: [Frankfurt Data Science Meetup](https://www.meetup.com/de-DE/frankfurtdatascience/). I met [Saurabh Chakravorty](https://www.linkedin.com/in/saurabh-chakravorty-1212b0106/), [Zheng Ma](https://www.linkedin.com/in/zheng-ma/), [Shivam Agrawal](https://www.linkedin.com/in/shivam-agrawal-ab879a141/), [Marcel Grimm](https://www.linkedin.com/in/marcel-grimm-843b68201/), and [Katharina Sturm](https://www.linkedin.com/in/katharina-sturm-838ab459/) there!

Also, I had a good conversation with [Christian Strässle](https://www.linkedin.com/in/christian-str%C3%A4ssle/) from [ValueFocus AG](https://valuefocus.ch/), a Swiss asset manager that cooperates with the [Chair of Data Science and Natural Language Processing](https://ics.unisg.ch/chair-ds-nlp-handschuh/). We will announce details of the [company cooperation](https://valuefocus.ch/risiko-aus-sicht-des-value-investors-2/) in the coming months.

## What Were the Biggest Obstacles?

Unlike last week, there were **no major distractions** by my corporate work. Some minor private distractions (but worthy ones). All good.

## Which Goals Did I Meet?

Goal 2 from last week: I've set up the GitLab **documentation** for the dissertation code. It's working well, and I may make the page publicly available in the future.

## Which Goals Did I Miss?

Goal 1 from last week: The appointment with my supervisors is **still not scheduled**. This is due to things outside my direct control, but not a big issue. I'll carry this goal over to the next week.

Goal 3 from last week: End-to-end document processing for the Python code is still not working. **I simply did not put enough time into this one.**

## Was It a Good Week?

Well, 2/3 goals were missed, so it was not a good week. The appointment goal is not fully in my control, and for the MVP goal, I think my schedule was too scattered to complete the MVP task. 

I need a couple of hours of deep concentration to finish the MVP task. While I did have enough gross time allocated to Ph.D. tasks, I did not have a long, uninterrupted period of time when I could focus on this task. 

So next week, I will lock myself in a room for a day without access to my phone and will not schedule any calls on that day.

## Short-Term Tasks for The Coming Week

<ol>
  <li>Carried over from last week: Make an appointment with my supervisor to discuss my Ph.D. dissertation proposal.</li>
  <li>Carried over from last week: First successful end-to-end document processing with the Python module (MVP). (With >80% test coverage and all tests passing.)</li>
  <li>Literature review:</li>
  <ol>
    <li>Add the following retrieval-augmented generation (RAG) papers to my literature database: Guu et al., 2020 (REALM), Yogatama et al., 2021, Bordeaud et al., 2021, Izacard & Grave, 2020, Min et al., 2020</li>
    <li>Add this text-to-text framework paper to my literature database: Raffel et al., 2019</li>
    <li>Add Contriever paper (Izacard et al., 2022, unsupervised training & continuous dense embeddings) to my literature database.</li>
  </ol>
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