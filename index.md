---
layout: default
---

{{ site.baseurl }}

## About

This mod adds several elements to Civ 5's game mechanics.

{% for category in site.categories %}

### {{ category[0] | capitalize }}

<ul class="posts">
{% for post in site.posts %}
	{% if post.categories contains category[0] %}
		<li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
	{% endif %} 
{% endfor %}
</ul>
{% endfor %}