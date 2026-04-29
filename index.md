---
title: home
layout: home
type: parent
order: 1
---

<div class="section header">
		<h1 class="title">Cameron Marsh Artwork</h1>
		<div id="navbar-wrapper">
			<div id="navbar" class="close">
				<a onclick="menuExpand()"><img id="brand" class="hide" src="{{ relative_url }}"></a>
				{% assign mypages = site.pages | where: "type", "parent" | sort: "order" %}
				{% for page in mypages %}
				<a class="button" href="{{ page.url | relative_url }}">{{ page.title }}</a>
				{% endfor %}
			</div>
		</div>
</div>

<div class="section main">
	<div class="container gallery">
		<div class="row" id="gallery">
			{% assign coll = site.collections | where: "label", "home" | first %}
			{% assign list = coll.files %}
			{% assign l = coll.files.size | divided_by: 2 | ceil %}
			<div class="one-half column">
				{% for image in list offset: l %}
				<article class="thumb">
					<img class="lozad u-max-full-width" data-src="{{ coll.label | append: '/' | append: image.name }}" alt="{{ image.basename }}" />
				</article>
				{% endfor %}
			</div>
			<div class="one-half column">
				{% for image in list offset: l+1 %}
				<article class="thumb">
					<img class="lozad u-max-full-width" data-src="{{ coll.label | append: '/' | append: image.name }}" alt="{{ image.basename }}" />
				</article>
				{% endfor %}
			</div>
		</div>
	</div>
</div>