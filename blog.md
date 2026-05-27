---
layout: default
title: "Blog"
description: "Complete archive of Enterprise Planning Hub articles, ordered by publication date."
---

# Blog

<p class="archive-count">{{ site.posts | size }} articles, most recent first.</p>

{% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
{% for year in posts_by_year %}
<h2 class="archive-year">{{ year.name }}</h2>
<ul class="archive-list">
  {% for post in year.items %}
  <li class="archive-item">
    <span class="archive-date">{{ post.date | date: "%b %d" }}</span>
    <div class="archive-content">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.description %}<p>{{ post.description }}</p>{% endif %}
    </div>
  </li>
  {% endfor %}
</ul>
{% endfor %}
