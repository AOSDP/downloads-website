---
title: Downloads
permalink: /
layout: page
---

# Stable

<ul class="files-stable">
    {% for file in site.files %}
        {% if file.stable == true and file.archived == false and file.gsi == false %}
            <h1>{{ file.file_name }}</h1>

            <h4>Downloads</h4>
            
            {{ file.content | markdownify }}
	          <h5>Maintainer : {{ file.builder }}</h5>
        {% endif %}
    {% endfor %}
</ul>

# Testing

Warning! These files may be unstable. Please report any problems to our [Telegram group](https://t.me/AOSDPx/39).

<ul class="files-unstable">
    {% for file in site.files %}
        {% if file.stable == false and file.archived == false and file.gsi == false %}
            <h1>{{ file.file_name }}</h1>

	    <h4>Downloads</h4>

            {{ file.content | markdownify }}
	          <h5>Maintainer : {{ file.builder }}</h5>
        {% endif %}
	{% endfor %}
</ul>

# Other builds

<iframe src="https://ams01.downloads.aosdp.com/?iframe=true&ignore={% for file in site.files %}{% if file.gsi == false %}{{ file.file_name|replace:'.zip'}},{% endif %}{% endfor %}gsi" style="width: 100%; height: 500px;" frameborder="0"></iframe>

<small><a href="https://par01.downloads.aosdp.com">View in full screen</a></small>

# For older build

Please head to the archived section, [Archived](https://downloads.aosdp.com/archive/).

# For the GSI (Generic System Image)

Please head to the GSI section, [GSI](https://downloads.aosdp.com/gsi/).
