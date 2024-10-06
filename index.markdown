---
layout: home
---

<h1>kat's blog</h1>

{% include about.html %}

<h2><a href="posts">posts</a></h2>
 <div id="post">
		{% assign posts = site.posts | sort: date | reverse %}
		{% for post in posts limit:5  %}
		    {{ post.title }} --
			{{ post.date | date: "%d/%m/%Y" }}
			{{ post.content | truncatewords:50}}
		{% endfor %}