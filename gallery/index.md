---
layout: page
title: Gallery
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


{% include gallery images=images caption="" cols=2 %}
