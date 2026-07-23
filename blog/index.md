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

    {% assign has_posts = false %}
    <ul class="post-list">
    {% for post in site.posts %}
      {% assign post_date_str = post.date | date: '%Y-%m-%d' %}
      {% if post_date_str >= site.relaunch_date %}
        {% assign has_posts = true %}
        <li class="post-list-item">
          <span class="post-date">{{ post.date | date: "%-d %B %Y" }}</span>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>{% endif %}
        </li>
      {% endif %}
    {% endfor %}
    </ul>
    {% unless has_posts %}
    <p>Nothing published yet — check back soon.</p>
    {% endunless %}

    <p style="margin-top:3rem;"><a class="mono" href="{{ '/blog/archive/' | relative_url }}" style="color:#8A6D3B;">Looking for older posts? Browse the archive →</a></p>
  </div>
</div>
