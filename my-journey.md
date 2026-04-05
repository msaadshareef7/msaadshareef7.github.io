---
layout: default
title: My Journey
permalink: /blog/
---

<input class="search" placeholder="Search posts...">

<div class="posts-container">
{% assign sorted_posts = site.posts | reverse %}
{% for post in sorted_posts %}
  <div class="post-card">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt }}</p>
  </div>
{% endfor %}
</div>
