---
layout: post
icon: fa-regular fa-gem
order: 4
toc: true
---

{% assign sorted = site.data.item_data | sort: 'name'%}
{% for recipe in sorted %}
  {% include crafting-table-card.html %}
{% endfor %}

<!-- buffer for the TOC -->
<div style="height: 800px"></div>



