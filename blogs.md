---
layout: page
title: Blog
permalink: /blog/
---

# Blog

Technical notes on AI, Machine Learning, Python, Java, and backend  development.

<ul class="blog-list">
{% for post in site.posts %}
  <li>
    <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    {% if post.excerpt %}
      <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>
