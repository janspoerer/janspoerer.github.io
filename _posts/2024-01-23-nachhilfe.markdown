---
layout: post
title: "2024-01-23: Nachhilfe für Studenten - Informatik, KI, Mathematik, Finanzmathematik (German only)"
date: 2024-01-23
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

> Unlike the other posts, this one is in German only as it is targeted at German-speaking students seeking for tutoring.

Bereits seit der Schulzeit gebe ich gerne Nachhilfe. Mittlerweile sind es vor allem Studenten und Berufstätige, die meine Nachhilfe in Anspruch nehmen. Wenn du Hilfe braucht in den Fächern Informatik/Programmierung, KI, Mathematik oder Finanzmathematik, bin ich für dich da!

# Kompetenzen

Im Bereich BWL kann ich dir helfen mit:

<ul>
  <li>Rechnungswesen.</li>
  <li>Finanzen und Finanzmärkte.</li>
  <li>VWL, Mikro- und Makroökonomie.</li>
</ul>

Im Bereich Informatik helfe ich dir mit:

<ul>
  <li>Einführung in diverse Programmiersprachen und Frameworks.</li>
  <li>Python (inkl. PyTorch und TensorFlow), Java, Angular, React, JavaScript, TypeScript, Git, GitHub, LaTeX.</li>
  <li>Auswahl der richtigen Tools, um produktiv arbeiten zu können.</li>
</ul>

Finanzspezifisch:

<ul>
  <li>Option Pricing und allgemeine Derivatebewertung (Futures, Forwards).</li>
  <li>Systematische Handelsstrategien; Portfoliobacktesting; Faktormodellierung.</li>
  <li>Auslesen von Daten aus Datenbanken wie Bloomberg und CUSIP.</li>
</ul>

Wissenschaftliches Schreiben:

<ul>
  <li>LaTeX, Formatierung von Abschlussarbeiten.</li>
  <li>Lektorat.</li>
  <li>Prüfung von wissenschaftlichen Methoden.</li>
</ul>

# Wo man mich findet

Hier kannst du Nachhilfetermine für 50€/h buchen: 

> [https://calendar.app.google/EH6nSsTtL3oPmofUA](https://calendar.app.google/EH6nSsTtL3oPmofUA). 

Du kannst alternativ auch über Superprof einen Termin buchen. Die Links zu meinen Superprof-Anzeigen befinden sich unten in der Sektion "Referenzen".

# Referenzen

<ul>
    <li> Diversen Studenten auf Superprof geholfen. Bewertungen der Studenten: </li>
    <ul>
        <li><a href="https://www.superprof.de/informatik-und-mathenachhilfe-von-informatikdoktorand-aus-frankfurt-bereits-erfahrung-mit-nachhilfe-kinder-und-erwachsene.html">Bewertungen für Informatik-Nachhilfe</a></li>
        <li><a href="https://www.superprof.de/nachhilfe-von-informatikdoktorand-fokus-auf-programmiersprachen-und-anwendungen-finanzbereich-machine-learning.html">Bewertungen für BWL-Nachhilfe</a></li>
    </ul>
    <li> Offizieller Dozent an einer Universität für Informatik im Master.</li>
    <li> Offizieller Tutor an einer Universität für Finanzkurse im Bachelor (bis zu 200 Teilnehmer).</li>
    <li> Nachhilfe in der Mittelstufe für Schüler in den Klassen 6 bis 8 (alle Fächer, einzeln und in Kleingruppen).</li>
</ul>

# Impressum

Das Impressum für dieses Angebot befindet sich unter dem Buchungslink (in der Textbeschreibung unten):

> [https://calendar.app.google/EH6nSsTtL3oPmofUA](https://calendar.app.google/EH6nSsTtL3oPmofUA).

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