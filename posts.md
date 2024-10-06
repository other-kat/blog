---
layout: page
title: posts
permalink: /posts/
---

<h2><a href="https://blog.otherkat.com">home</a></h2>
<h2>posts -- </h2>
 <div id="post">
		{% assign posts = site.posts | sort: date | reverse %}
		{% for post in posts limit:5  %}
		    {{ post.title }} --
			{{ post.date | date: "%d/%m/%Y" }}
			{{ post.content }}
		{% endfor %}
