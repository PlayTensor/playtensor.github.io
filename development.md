---
layout: page
title: Development Log
permalink: /devlog/
nav_order: 3
---

Welcome to the Official News Feed and Development Log

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.date | date: "%Y %b %-d" }}
    </li>
  {% endfor %}
</ul>
