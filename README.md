---
layout: default
title: Home
---

<div class="hero">
  <h1>Curated lists, tools, and digital finds</h1>
  <p>
    I collect useful resources, creative tools, and standout finds across AI, design, and online business.
  </p>
</div>

<h2>Featured Lists</h2>

<div class="card-grid">
  {% assign featured_lists = site.lists | where: "featured", true %}
  {% for list in featured_lists %}
    <div class="card">
      <h3><a href="{{ list.url | relative_url }}">{{ list.title }}</a></h3>
      <p>{{ list.description }}</p>
    </div>
  {% endfor %}
</div>

<h2>All Lists</h2>

<div class="card-grid">
  {% for list in site.lists %}
    <div class="card">
      <h3><a href="{{ list.url | relative_url }}">{{ list.title }}</a></h3>
      <p>{{ list.description }}</p>
    </div>
  {% endfor %}
</div>
