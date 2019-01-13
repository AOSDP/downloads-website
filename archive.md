---
title: Archive
permalink: /archive/
layout: page
---

These builds are archived! Always use latest one.

<ul class="files-archived">
    {% for file in site.files %}
        {% if file.archived == true %}
            <h1>{{ file.file_name }}</h1>

            Stable: {{ file.stable }}

            <h4>Downloads</h4>

            {{ file.content | markdownify }}
        {% endif %}
    {% endfor %}
</ul>
