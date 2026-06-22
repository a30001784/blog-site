---
layout: page
title: Archive
permalink: /archive/
---

Browse every post by date. Use the calendar and archive columns on the
[home page]({{ '/' | relative_url }}) to jump straight to a month or year.

{% assign by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
{% for year in by_year %}
<h2 id="{{ year.name }}">{{ year.name }}</h2>
{% assign by_month = year.items | group_by_exp: "post", "post.date | date: '%Y-%m'" %}
{% for month in by_month %}
<h3 id="{{ month.name }}">{{ month.name | append: '-01' | date: "%B %Y" }}</h3>
<ul>
{% for post in month.items %}
  <li><strong>{{ post.date | date: "%b %-d" }}</strong> — <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></li>
{% endfor %}
</ul>
{% endfor %}
{% endfor %}
