---
title: Downloads
permalink: /
layout: page
---

<ul class="staff">
	{% for file in site.files %}
		<h1>{{ file.file_name }}</h1>

        <h4>Downloads</h4>
        {{ file.content | markdownify }}
	{% endfor %}
</ul>