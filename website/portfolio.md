---
layout: default
title: Portfolio
permalink: /portfolio/
usemathjax: true
---

# Resume
This is my resume
{% assign item = site.portfolio | where: "title", "Resume" | first %}
{% include item-card-h.html item=item %}

# Professional Portfolio
<p>Makani: {{ makani_paper.title }}</p>

{% assign item = site.portfolio | where: "title", "Makani Paper" | first %}
{% include item-card-h.html item=item %}
