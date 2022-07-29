---
layout: post
title: "2022-07-24: Hello World!"
date: 2022-07-24
categories: post
tags: spoerico
is_series: true
series_title: "Spoerico"
---
This is my first post. I am looking forward to use posts like this one to share something about me in the future.

In the meantime, check my [LinkedIn](https://www.linkedin.com/in/janspoerer/) for seeing what I am up to.

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