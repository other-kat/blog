---
layout: home
---

<h1>kat's blog</h1>

{% include about.html %}

<h2>posts</h2>
 <div id="post">
		{% assign posts = site.posts | sort: date | reverse %}
		{% if post.status == 'published' %}
		{% endif %}
		{% for post in posts limit:5  %}
<a href="{{ post.url }}">{{ post.title }} - {{ post.date | date: "%d/%m/%Y" }}</a><br>
		{{ post.content | truncatewords:50}}<br><br>
		{% endfor %}

<a href="/posts/">more</a>