---
layout: page
title: Development Log
permalink: /devlog/
---

Welcome to the Official Development Log

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.date | date: "%Y %b %-d" }}
    </li>
  {% endfor %}
</ul>