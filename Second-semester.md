---
layout: default
title: Second Semester
permalink: /second-semester/
---

# Second Semester

{% for post in site.posts %}
{% if post.semester == "second" %}
<div class="post-card">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
</div>
{% endif %}
{% endfor %}
