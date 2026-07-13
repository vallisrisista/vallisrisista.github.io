---
layout: page
title: Hi, I'm Vallisri.
---

I write about AI, machine learning, and backend systems — and share the projects I build along the way.

<div class="hero-buttons">
  <a href="/projects/" class="btn-primary">View Projects</a>
  <a href="/blogs/" class="btn-secondary">Read Blogs</a>
  <a href="/resume/" class="btn-secondary">Resume</a>
</div>

## Focus Areas

<div class="skill-grid">
  <span>AI</span>
  <span>Machine Learning</span>
  <span>RAG</span>
  <span>Python</span>
  <span>Java</span>
  <span>Spring Boot</span>
  <span>Backend Development</span>
</div>

## Latest Blogs

<ul class="latest-posts">
{% for post in site.posts limit:5 %}
  <li>
    <span>{{ post.date | date: "%b %-d, %Y" }}</span>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
