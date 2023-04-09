---
layout: post
icon: fas fa-scroll
order: 1
toc: true
---

{% assign grouped_spells = site.spells | group_by: 'school' | sort: 'school' %}
{% assign schools = grouped_spells | sort: 'name'%}
{% for spells in schools %}
## {{spells.name}} Spells 
<hr>
{% assign sorted_spells = spells.items | sort: 'name' %}
{% for spell in sorted_spells %}
### {{spell.name}}
- {{spell.description}}
- {{spell.stats}}
- {{spell.icon}}
{% endfor %}
{% endfor %}

<style>
.card {
  /* Add shadows to create the "card" effect */
  background: var(--card-bg);
  padding: 8px;
}

/* On mouse-over, add a deeper shadow */
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

/* Add some padding inside the card container */
.container {
  padding: 2px 16px;
}
</style>

<div class="card">
  <img src="../img/spells/angel_wing.png" style="width: 64px;">
  <div class="">
    <h3><b>John Doe</b></h3>
    <p>Architect & Engineer</p>
  </div>
</div>

<!-- buffer for the TOC -->
<div style="height: 800px"></div>



