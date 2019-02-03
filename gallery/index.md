---
layout: page
title: gallery
date: 2019-02-02
comments: false
---

{% capture images %}
    {% for image in site.static_files %}
	    {% if image.path contains 'assets/img/gallery' %}
	        {{ image.path }}
	    {% endif %}
	{% endfor %}
{% endcapture %}
{% for image in site.static_files %}
    {% if image.path contains 'assets/img/gallery' %}
        <p>{{ image.path }}</p>
    {% endif %}
{% endfor %}
{% include gallery images=images caption="Mermaid Images" cols=2 %}
