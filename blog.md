---
layout: default
title: Blog
---

<section class="content-card">
  <p class="section-label">Blog</p>
  <h2>My Posts</h2>
  <p>This page shows all post links. Click any post to open the full article and read the complete experience.</p>
</section>

<section class="posts-grid">
  {% for post in site.posts %}
    <article class="post-preview-card">
      <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt | strip_html | truncate: 170 }}</p>
      <a class="read-more" href="{{ post.url | relative_url }}">Read full post</a>
    </article>
  {% endfor %}
</section>
