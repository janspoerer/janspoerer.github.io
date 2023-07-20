---
layout: post
title: "2023-07-20: Health Tracking for Employee Wellbeing"
date: 2023-07-20
categories: post
tags: business
is_series: true
series_title: "Business"
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

# Some Background

Some years ago, I became interested in the longevity movement. You may have heard about David Sinclair, Rhonda Patrick, Valter Longo, and Bryan Johnson, who are thought leaders in the field.

One of the means of achieving a long life is tracking one's biomarkers. Biomarkers tell us how healthy we are. We all know blood pressure and blood sugar as important health metrics, but there are many more biomarkers that are [well-summarized](https://blueprint.bryanjohnson.co/#routine-measurement) by Bryan Johnson's Blueprint.

Sleep, nutrition, and exercise are probably the most relevant determinants of these biomarkers, and, consequently, health. But stress is also a relevant one. **Heart rate variability** (HRV) and **heart rate** can be used as measures of stress that a simple smartwatch can provide **in real-time**.

# Why This is Relevant for Business

This brings me to why companies can utilize biomarkers in their employee retention efforts. Most large companies advertise themselves to employees as caring and generally "employee-friendly."

We all know these claims, but how can companies systematically measure and track employees' health to
<ol>
  <li><b>prove</b> that they are good employers,</li>
  <li>and how can they track whether their employee <b>wellbeing programs are successful</b>?</li>
</ol>
The answer is health tracking.

So that's what I recently did. I bought a smartwatch with HRV and heart rate functionality to track how stressed I am during the day.

As soon as I understand whether these measurements are meaningful, I will gradually expand the use of smartwatches and smart rings to my colleagues as well.

I envision that one day, one could

# How to Get Into the Health Tracking Rabbit Hole

If you would like to talk about my experiences with business-related health tracking, other health tracking, and longevity in general, I am always happy to talk. Please reach out to me at any time.

In general, I cannot recommend these books highly enough:
* Sleep: [Why We Sleep by Matthew Walker](https://www.goodreads.com/book/show/34466963-why-we-sleep?ac=1&from_search=true&qid=6YPDc2gKob&rank=1).
* Nutrition: [How Not to Die by Michael Greger](https://www.goodreads.com/book/show/25663961-how-not-to-die?from_search=true&from_srp=true&qid=7yfzGngtRT&rank=1).
* Exercise: None yet! Please recommend one great book to me if you have one!
* Health tracking: Everything that Bryan Johnson from [Blueprint](https://blueprint.bryanjohnson.co/#routine-measurement) does.

And these are my top thought leaders in the longevity space (as alluded to before):
* David Sinclair
* Rhonda Patrick
* Bryan Johnson

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