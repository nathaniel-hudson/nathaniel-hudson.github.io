---
layout: page
permalink: /publications/
title: publications
description: Peer-reviewed journal and conference publications.
years: [2023, 2022, 2021, 2020, 2019] # [1967, 1956, 1950, 1935, 1905]
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
