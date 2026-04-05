---
layout: default
title: My Journey
permalink: /my-journey/
---

<input class="search" placeholder="Search posts...">

{% for post in site.posts %}
<div class="post-card" onclick="location.href='{{ post.url }}'">
  <h2>{{ post.title }}</h2>
  <p>{{ post.excerpt }}</p>
</div>
{% endfor %}
