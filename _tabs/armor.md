---
layout: post
icon: fas fa-shield
order: 3
toc: true
---
{% assign lastGroup = 'XXX' %}
{% assign sorted = site.data.armor_data | sort: 'name'%}

{% for recipe in sorted %}
  {% if recipe.group != lastGroup %}
  <h2 id="{{recipe.group}}"> {{recipe.group}}</h2>
  <hr>
  {% endif %}
  {% include crafting-table-card.html %}
  {% assign lastGroup = recipe.group %}
{% endfor %}

<!-- buffer for the TOC -->
<div style="height: 800px"></div>

