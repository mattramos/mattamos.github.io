---
layout: page
permalink: /publications/
title: publications
description: Publications both in preperation (top) and published (below). *s denote equal authorship.
years: [InPrep, 2022, 2021, 2020]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
