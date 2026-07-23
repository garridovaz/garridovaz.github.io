---
layout: default
title: Archive
permalink: /blog/archive/
---
<div class="section">
  <div class="wrap prose">
    <div class="section-head">
      <span class="eyebrow">Archive</span>
      <h1>Older posts</h1>
    </div>

    {% assign year_open = false %}
    {% assign last_year = "" %}
    {% for post in site.posts %}
      {% assign post_date_str = post.date | date: '%Y-%m-%d' %}
      {% if post_date_str < site.relaunch_date %}
        {% assign year = post.date | date: '%Y' %}
        {% if year != last_year %}
          {% if year_open %}</ul>{% endif %}
          <h2 class="mono" style="margin-top:2rem; font-size:1rem; color:#8A6D3B;">{{ year }}</h2>
          <ul class="post-list">
          {% assign last_year = year %}
          {% assign year_open = true %}
        {% endif %}
        <li class="post-list-item">
          <span class="post-date">{{ post.date | date: "%-d %B %Y" }}</span>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        </li>
      {% endif %}
    {% endfor %}
    {% if year_open %}</ul>{% endif %}
    {% unless year_open %}<p>No archived posts yet.</p>{% endunless %}
  </div>
</div>
