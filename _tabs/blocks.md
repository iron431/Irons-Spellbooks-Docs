---
layout: post
icon: fas fa-cube
order: 5
toc: true
---

{% assign sorted = site.data.block_data | sort: 'name'%}
{% for recipe in sorted %}
{% include crafting-table-card.html %}
{% endfor %}

<!-- buffer for the TOC -->
<div style="height: 800px"></div>

