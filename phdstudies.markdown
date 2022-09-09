---
layout: default
title: Ph.D. Studies
permalink: /phdstudies/
tags: phd
is_series: true
series_title: "75 Steps Toward a Ph.D. in NLP"
---

# Ph.D. Studies

## Overview

I am working on a dissertation in the field of natural language processing (NLP). The dissertation is part of a computer science Ph.D. program at the University of St. Gallen.

The tool, which is developed as part of the dissertation, will be a retrieval-augmented generator for financial documents. This means that one can provide a question and a PDF (with an annual report, for example) and get the answer to the question based on the PDF.

Modules in the `finrag-sequence` project:
```
|-pdf
|-embeddings
|-document_retriever
|-generator
```

This is the [chair's website](https://ics.unisg.ch/chair-ds-nlp-handschuh/).

## Dissertation Progress

```
Course #1:          |##########| 100%
Course #2:          |##########| 100%
Course #3:          |##########| 100%
Proposal:           |########--| 80% (discussion with supervisors outstanding)
Research software:  |##--------| 20% (MVP is ready)
Paper #1:           |#---------| 10% (will be focused on when proposal is finished)
Paper #2:           |----------|  0%
Paper #3:           |----------|  0%
Defense:            |----------|  0%
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