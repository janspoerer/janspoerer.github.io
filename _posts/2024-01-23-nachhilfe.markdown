---
layout: post
title: "2024-01-23: Nachhilfe für Studenten - Informatik, KI, Mathematik, Finanzmathematik"
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

> Please find the English version below. 🇬🇧 

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

Hier kannst du Nachhilfetermine buchen und direkt bezahlen: 

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

<br>
<br>
<br>
<br>
<br>

---
<br>

# English Version 🇬🇧 




I enjoyed being a tutor in middle school and continued tutoring throughout college and my master's. Nowadays, especially university students and professionals use my services. If you need help in computer science, coding, programming, artificial intelligence (AI), mathematics, or financial mathematics, I am here for you!

# Competencies

Business:

<ul>
  <li>Accounting.</li>
  <li>Finance and financial markets.</li>
  <li>Economics, microeconomics, and macroeconomics.</li>
</ul>

Computer science:

<ul>
  <li>Introduction to various programming languages and frameworks.</li>
  <li>Python (incl. PyTorch and TensorFlow), Java, Angular, React, JavaScript, TypeScript, Git, GitHub, LaTeX.</li>
  <li>Choice of the best tools for productive work.</li>
</ul>

Finance-specific:

<ul>
  <li>Options pricing and general derivatives pricing (futures, forwards).</li>
  <li>Systematic trading strategies; portfolio backtesting; factor modeling.</li>
  <li>Using databases such as Bloomberg and CUSIP.</li>
</ul>

Academic writing:

<ul>
  <li>LaTeX, formatting of theses.</li>
  <li>Lectorate, editing.</li>
  <li>Checking of scientific methods.</li>
</ul>

# Where you can find me

Here you can book and pay for tutoring: 

> [https://calendar.app.google/EH6nSsTtL3oPmofUA](https://calendar.app.google/EH6nSsTtL3oPmofUA). 

Alternatively, you can do this via Superprof. The Superprof links are above in the German version under the section "Referenzen".

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