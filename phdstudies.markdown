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
Proposal:           |##########| 100% Done and passed.
Research software:  |##--------| 20% (MVP is ready) -> Decided not to write a big overarching software project; each individual paper is based on its own code.
Paper #1:           |########--| 80% Needs to be published.
Paper #2:           |########--| 80% Needs to be published.
Paper #3:           |##--------| 20% Being written...
Paper #4:           |##--------| 20% Being written...
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