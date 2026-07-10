---
layout: page
title:
---

<section class="hero-section">

  <div class="hero-content">

    <p class="hero-eyebrow">Hello, I'm Vallisri.</p>

    <h1>AI, ML & Backend Developer</h1>

    <p class="hero-subtitle">
      I write practical notes on <strong>AI, Machine Learning, Python, Java, Backend Development</strong>,
      and technical project learnings.
    </p>

    <div class="hero-buttons">
      <a href="/projects/" class="btn-primary">View Projects</a>
      <a href="/blogs/" class="btn-secondary">Read Blogs</a>
      <a href="/resume/" class="btn-secondary">Resume</a>
    </div>

    <div class="hero-tags">
      <span>AI</span>
      <span>Machine Learning</span>
      <span>RAG</span>
      <span>Java</span>
      <span>Python</span>
      <span>Spring Boot</span>
    </div>

  </div>

  <div class="hero-visual">
    <div class="hero-card">
      <div class="hero-card-dots">
        <span></span>
        <span></span>
        <span></span>
      </div>

<pre><code>&gt; learning.log

AI       : notes
ML       : concepts
Java     : backend
Python   : examples
Projects : portfolio</code></pre>

    </div>
  </div>

</section>

<section class="section-block">

## Featured Projects

<div class="card-grid">

<div class="info-card">
<h3>Password Rotation Agent</h3>
<p>Agentic AI workflow using Java Spring Boot, LangChain4j, and LLM tools.</p>
<a href="/projects/">View project</a>
</div>

<div class="info-card">
<h3>RAG Document Generator</h3>
<p>Retrieval-Augmented Generation workflow for creating structured technical documents.</p>
<a href="/projects/">View project</a>
</div>

<div class="info-card">
<h3>RTM Transaction Portal</h3>
<p>Backend portal for searching and tracking middleware transactions.</p>
<a href="/projects/">View project</a>
</div>

</div>

</section>

<section class="section-block">

## Latest Blogs

<ul class="latest-posts">
{% for post in site.posts limit:5 %}
  <li>
    <span>{{ post.date | date: "%b %-d, %Y" }}</span>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>

</section>
