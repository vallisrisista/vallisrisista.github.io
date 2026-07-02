---
layout: page
title: Categories
permalink: /categories/
---

# Categories

{% assign categories = site.categories | sort %}

{% for category in categories %}
## {{ category[0] }}

{% for post in category[1] %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%b %-d, %Y" }}
{% endfor %}

{% endfor %}
