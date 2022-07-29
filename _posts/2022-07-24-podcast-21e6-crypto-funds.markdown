---
layout: post
title: "2022-07-24: Podcast on Crypto Funds"
date: 2022-07-24
categories: post
tags: 21e6
is_series: true
series_title: "21e6"
---
Check me out [being interviewed](https://open.spotify.com/episode/0ucfbvFGrU7AGtsLxDCVly?si=0a9761d2fd174942&nd=1) by Maximilian Bruckner on the topic of crypto funds.

[21e6's podcast](https://assets.21e6.io/crypto-for-family-offices/new-podcast-krypto-im-portfolio-launched) covers guests from the crypto portfolio management industry.

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