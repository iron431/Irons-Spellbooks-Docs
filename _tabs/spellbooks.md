---
layout: post
icon: fas fa-book
order: 2
---
{% assign sorted = site.data.spellbook_data | sort: 'name'%}
{% for recipe in sorted %}
  {% include crafting-table-card.html %}
{% endfor %}

<!-- buffer for the TOC -->
<div style="height: 800px"></div>

