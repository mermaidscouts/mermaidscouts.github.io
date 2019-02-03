---
layout: page
title: gallery
date: 2019-02-02
comments: false
---

{% capture images %}
    {% for file in directory %}
	    {{ file.url }}
	{% endfor %}
{% endcapture %}
{% include gallery images=images caption="Mermaid Images" cols=2 %}
