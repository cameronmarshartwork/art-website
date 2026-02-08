---
title: Landscape
layout: gallery
type: parent
order: 5
---

<div class="section main">
	<div class="container">
		{% assign mypages = site.pages | where: "type", "lanscape" %}
		{% for page in mypages %}
		<a class="button" href="{{ page.url | relative_url }}">{{ page.title }}</a>
		{% endfor %}
	</div>