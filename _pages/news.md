---
layout: page
title: News
permalink: /news/
---

<style>
  h1 {
    text-transform: uppercase;
  }
</style>

<!-- _pages/news.md — entries live in _news/, rendered as a list newest first -->

<ul style="list-style: none; padding-left: 0; margin-top: 1.5rem">
  {% assign sorted_news = site.news | sort: "date" | reverse %}
  {% for item in sorted_news %}
    <li style="display: flex; gap: 1rem; margin-bottom: 0.9rem">
      <span style="flex: 0 0 5.5rem; white-space: nowrap; opacity: 0.7">{{ item.date | date: "%b %Y" }}</span>
      <span>{{ item.content | remove: '<p>' | remove: '</p>' }}</span>
    </li>
  {% endfor %}
</ul>
