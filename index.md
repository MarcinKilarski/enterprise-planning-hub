---
layout: default
title: Home
---

# Industry Insights & Summaries

Welcome to the Enterprise Planning Hub. Below is a collection of summaries, independent critiques, and technical reviews of leading industry whitepapers and strategies.

### Recent Articles
{% for post in site.posts %}
* **[{{ post.title }}]({{ post.url }})** — *{{ post.date | date: "%b %d, %Y" }}* {{ post.excerpt | strip_html | truncatewords: 20 }}
{% endfor %}
