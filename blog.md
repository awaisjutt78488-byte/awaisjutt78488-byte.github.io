---
title: Blog / My Journey of CE
layout: default
permalink: /blog/
---

<h1>My Blog & Personal Experiences</h1>

<p>Here you can read about my learning journey, projects, challenges, and daily experiences.</p>

<h2>All Posts</h2>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small> — {{ post.date | date: "%B %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
