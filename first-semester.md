---
layout: default
title: First Semester
permalink: /first-semester/
---

# First Semester

{% for post in site.posts %}
{% if post.semester == "first" %}
<div class="post-card">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
</div>
{% endif %}
{% endfor %}
