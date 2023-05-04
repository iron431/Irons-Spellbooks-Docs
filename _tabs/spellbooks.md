---
layout: post
icon: fas fa-book
order: 2
toc: true
---
{% assign sorted = site.data.spellbook_data | sort: 'name'%}
{% for recipe in sorted %}
  {% include crafting-table-card.html pixelated="true" %}
{% endfor %}

<!-- buffer for the TOC -->
<div style="height: 800px"></div>

