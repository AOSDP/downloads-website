---
title: GSI
permalink: /gsi/
layout: page
---

# Stable

<ul class="files-stable">
    {% for file in site.files %}
        {% if file.stable == true and file.archived == true and file.gsi == false%}
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
        {% if file.stable == false and file.archived == true and file.gsi == false%}
            <h1>{{ file.file_name }}</h1>

            <h4>Downloads</h4>

            {{ file.content | markdownify }}
        {% endif %}
	{% endfor %}
</ul>
