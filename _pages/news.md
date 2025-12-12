<<<<<<< HEAD
---
layout: page
permalink: /news/
title: news
description: Full news ordered in reverse chronological order.
years: [2022, 2021] # [1967, 1956, 1950, 1935, 1905]
nav: true
nav_order: 1
---
<!-- _pages/news.md -->
<div class="news">

    {% if site.news != blank -%}
    {%- assign news_size = site.news | size -%}
    <div class="table-responsive" {% if site.news_scrollable and news_size > 3 %}style="max-height: 10vw"{% endif %}>
        <table class="table table-sm table-borderless">
        {%- assign news = site.news | reverse -%}
        {% for item in news %}
        <tr>
            <th scope="row" class="news-date">{{ item.date | date: "%b %-d, %Y" }}</th>
            <td>
            {% if item.inline -%}
                {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
            {%- else -%}
                <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
            {%- endif %}
            </td>
        </tr>
        {%- endfor %}
        </table>
    </div>
    {%- else -%}
    <p>No news so far...</p>
    {%- endif %}

</div>
||||||| 2fadee6a
=======
---
layout: page
title: news
permalink: /news/
---

{% include news.liquid %}
>>>>>>> upstream/master
