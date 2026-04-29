---
title: still life 
layout: default 
type: parent
order: 6
---

<div class="section main">
	<div class="container">
		{% assign mypages = site.pages | where: "type", "still life" %}
		{% for page in mypages %}
		<a class="button" href="{{ page.url | relative_url }}">{{ page.title }}</a>
		{% endfor %}
	</div>