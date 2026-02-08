---
title: Etching
layout: gallery
description: I try to make people pose sometimes.
type: parent
order: 4
---

<div class="section main">
	<div class="container">
		{% assign mypages = site.pages | where: "type", "etching" %}
		{% for page in mypages %}
		<a class="button" href="{{ page.url | relative_url }}">{{ page.title }}</a>
		{% endfor %}
	</div>