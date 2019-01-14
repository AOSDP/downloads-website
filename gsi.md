---
title: GSI
permalink: /gsi/
layout: page
---

# Stable


<ul class="files-stable">
    {% for file in site.files %}
        {% if file.stable == true and file.archived == false and file.gsi == true %}
            <h1>{{ file.file_name }}</h1>

            <h4>Downloads</h4>
            
            {{ file.content | markdownify }}
	          <h5>Maintainer : {{ file.builder }}</h5>
        {% endif %}
    {% endfor %}
</ul>

# Testing

Warning! These files may be unstable. Please report any problems to our [Telegram group](https://t.me/AOSDPx/39).
But actually, GSI is not stable so....

<ul class="files-unstable">
    {% for file in site.files %}
        {% if file.stable == false and file.archived == false and file.gsi == true %}
            <h1>{{ file.file_name }}</h1>

            <h4>Downloads</h4>

            {{ file.content | markdownify }}
	          <h5>Maintainer : {{ file.builder }}</h5>
        {% endif %}
	{% endfor %}
</ul>
