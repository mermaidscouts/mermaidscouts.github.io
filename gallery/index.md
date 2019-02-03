---
layout: page
title: gallery
date: 2019-02-02
comments: false
---

{% capture images %}
    {% for file in site.gallery %}
	    {{ file.url }}
	{% endfor %}
{% endcapture %}
{% for file in site.gallery %}
    <p>{{ file.url }}</p>
{% endfor %}
{% include gallery images=images caption="Mermaid Images" cols=2 %}
