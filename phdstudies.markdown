---
layout: default
title: Ph.D. Studies
permalink: /phdstudies/
tags: phd
is_series: true
series_title: "75 Steps Toward a Ph.D. in NLP"
---

# Ph.D. Studies

This is the [chair's website](https://ics.unisg.ch/chair-ds-nlp-handschuh/).

## Dissertation Progress

```
Course #1:          |##########| 100%
Course #2:          |##########| 100%
Course #3:          |##########| 100%
Proposal:           |##########| 100% Done and passed.
Research software:  |##--------| 20% (MVP is ready) -> Decided not to write a big overarching software project; each individual paper is based on its own code.
Paper #1:           |##########| 100% Published.
Paper #2:           |##########| 100% Published.
Paper #3:           |##########| 100% Published.
Paper #4:           |##########| 100% Published.
Paper #5:           |##########| 100% Published.
Defense:            |##########|  0%
```

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