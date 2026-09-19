---
layout: note
title: "Ti 列表"
---

<ul class="post-list">
  {% assign items = site.Ti | sort: 'date' | reverse %}
  {% for item in items %}
    {% unless item.url == page.url %}
    <li class="post-item">
      <h2 class="post-title">
        <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
      </h2>
      {% if item.date %}
        <div class="post-date">{{ item.date | date: "%Y-%m-%d" }}</div>
      {% endif %}
      <div class="post-excerpt">
        {{ item.excerpt | strip_html | truncatewords: 100 }}
      </div>
    </li>
    {% endunless %}
  {% endfor %}
</ul>