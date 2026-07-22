---
layout: default
title: Writing
permalink: /blog/
---
<div class="section">
  <div class="wrap prose">
    <div class="section-head">
      <span class="eyebrow">Writing</span>
      <h1>Notes on product, integrations, and fintech</h1>
    </div>

    {% if site.posts.size > 0 %}
    <ul class="post-list">
      {% for post in site.posts %}
      <li class="post-list-item">
        <span class="post-date">{{ post.date | date: "%-d %B %Y" }}</span>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>{% endif %}
      </li>
      {% endfor %}
    </ul>
    {% else %}
    <p>Nothing published yet — check back soon.</p>
    {% endif %}
  </div>
</div>
