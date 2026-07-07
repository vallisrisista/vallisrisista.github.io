---
layout: page
title: Categories
permalink: /categories/
---


{% assign categories = site.categories | sort %}

{% for category in categories %}
## {{ category[0] }}

<ul>
{% for post in category[1] %}
  <li>
    <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>

{% endfor %}
