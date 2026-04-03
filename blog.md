---
layout: default
title: Blog
permalink: /blog/
---

<section class="content-card">
  <p class="section-label">Blog</p>
  <h2>My Posts</h2>
  <p>This page shows all post links. Click any post to open the full article and read the complete experience.</p>
</section>

<section class="media-panel">
  <div class="content-card media-copy">
    <p class="section-label">Stories</p>
    <h2>Learning, effort, and personal growth</h2>
    <p>My posts collect the lessons I am learning from university life, hostel challenges, study habits, and semester experiences.</p>
  </div>
  <figure class="feature-visual">
    <img src="{{ '/assets/images/site/uet-library.jpg' | relative_url }}" alt="UET Library building" loading="lazy" decoding="async" />
    <figcaption>UET Library, representing study, reflection, and steady learning. <a href="https://commons.wikimedia.org/wiki/File:UET_Library.jpg">Photo source</a></figcaption>
  </figure>
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
