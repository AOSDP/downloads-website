---
title: Downloads
permalink: /
layout: page
---

# Stable

<ul class="files-stable">
    {% for file in site.files %}
        {% if file.stable == true %}
            <h1>{{ file.file_name }}</h1>

            <h4>Downloads</h4>
            
            {{ file.content | markdownify }}
        {% endif %}
    {% endfor %}
</ul>

# Testing

Warning! These files may be unstable. Please report any problems to our [Telegram group](https://t.me/AOSDPx/39).

<ul class="files-unstable">
    {% for file in site.files %}
        {% if file.stable == false %}
            <h1>{{ file.file_name }}</h1>

            <h4>Downloads</h4>

            {{ file.content | markdownify }}
        {% endif %}
	{% endfor %}
</ul>

# Old Build

These build are old! Always use lastest one.

<ul class="files-old">
    {% for file in site.files %}
        {% if file.old == true %}
            <h1>{{ file.file_name }}</h1>

            <h4>Downloads</h4>

            {{ file.content | markdownify }}
        {% endif %}
        {% endfor %}
</ul>
