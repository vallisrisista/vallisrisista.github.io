---
layout: page
title: Home
---

# Hi, I'm Vallisri Sista

This is my personal blog where I share my learnings on concepts of  ** AI, Machine Learning, Python Java, Backend Development **.

<div class="hero-buttons">
  <a href="/projects/" class="btn-primary">View Projects</a>
  <a href="/blog/" class="btn-secondary">Read Blog</a>
  <a href="/resume/" class="btn-secondary">Resume</a>
</div>

## Focus Areas

<div class="skill-grid">
  <span>AI & Machine Learning</span>
  <span>Generative AI</span>
  <span>RAG</span>
  <span>Java</span>
  <span>Spring Boot</span>
  <span>Python</span>
  <span>Backend Development</span>
</div>

## Featured Projects

<div class="card-grid">

<div class="info-card">
<h3>Password Rotation Agent</h3>
<p>Agentic AI system using Java Spring Boot, LangChain4j, and LLM tools to automate password rotation workflows.</p>
<a href="/projects/">View project</a>
</div>

<div class="info-card">
<h3>RAG Document Generator</h3>
<p>Retrieval-Augmented Generation workflow for generating structured technical documents from existing files.</p>
<a href="/projects/">View project</a>
</div>



</div>

## Latest Blog Posts

<ul class="latest-posts">
{% for post in site.posts limit:5 %}
  <li>
    <span>{{ post.date | date: "%b %-d, %Y" }}</span>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
