---
layout: default
title: "题目列表"
---

<ul class="post-list">
  {% assign sorted_posts = site.Ti | sort: 'date' | reverse %}
  {% for post in sorted_posts %}
    <li class="post-item">
      <h2 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <div class="post-excerpt">
        {{ post.excerpt | strip_html | truncatewords: 100 }}
      </div>
    </li>
  {% endfor %}
</ul>