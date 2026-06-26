
---

layout: default
title: My Journey
permalink: /my-journey/
-----------------------

# My Journey

<input
type="text"
id="searchInput"
placeholder="🔍 Search posts..."
style="width:100%;padding:12px;margin-bottom:20px;border-radius:8px;border:1px solid #ccc;"

>

<div id="postsList">

{% for post in site.posts %}

<div class="journey-card">

<h2>
<a href="{{ post.url | relative_url }}">
{{ post.title }}
</a>
</h2>

<p>
📅 {{ post.date | date: "%d %B %Y" }}
</p>

<p>
{{ post.excerpt | strip_html | truncate: 150 }}
</p>

</div>

{% endfor %}

</div>

<style>
.journey-container{
    max-width:900px;
    margin:auto;
    padding:40px 20px;
}

.journey-card{
    background:#1f2942;
    color:white;
    padding:30px;
    margin:20px 0;
    border-radius:15px;
}

.journey-card a{
    color:white;
    text-decoration:none;
}

.journey-card a:hover{
    text-decoration:underline;
}
</style>

<script>
document.addEventListener("DOMContentLoaded", function() {

    const searchInput = document.getElementById("searchInput");

    searchInput.addEventListener("keyup", function() {

        let filter = this.value.toLowerCase();

        let posts = document.querySelectorAll(".journey-card");

        posts.forEach(function(post) {

            let text = post.innerText.toLowerCase();

            if(text.includes(filter)){
                post.style.display = "block";
            } else {
                post.style.display = "none";
            }

        });

    });

});
</script>

</style>
