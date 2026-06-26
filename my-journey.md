---

layout: default
title: My Journey
permalink: /my-journey/
---

# My Journey

<input
type="text"
id="searchInput"
placeholder="🔍 Search posts..."
style="width:100%;padding:12px;border-radius:10px;border:none;margin:20px 0;font-size:16px;">

<div id="postsContainer">

{% for post in site.posts %}

<div class="post-card post-item">

<h2>
<a href="{{ post.url | relative_url }}" style="color:white;text-decoration:none;">
{{ post.title }}
</a>
</h2>

<p>
{{ post.date | date: "%B %d, %Y" }}
</p>

<p>
{{ post.excerpt | strip_html | truncate: 150 }}
</p>

</div>

{% endfor %}

</div>

<script>
document.addEventListener("DOMContentLoaded", function() {

const searchInput = document.getElementById("searchInput");

searchInput.addEventListener("keyup", function() {

const filter = this.value.toLowerCase();

const posts = document.querySelectorAll(".post-item");

posts.forEach(post => {

const text = post.innerText.toLowerCase();

if(text.includes(filter)){
post.style.display = "block";
}else{
post.style.display = "none";
}

});

});

});
</script>
