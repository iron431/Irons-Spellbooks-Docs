---
layout: post
icon: fas fa-scroll
order: 1
toc: true
test: #2C2B2B;
---
<style>
.card-container {
  background-color: #2C2B2B;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
  margin-bottom: 40px;
  overflow: hidden;
}

.card-header2 {
  background-color: #232324;
  display: flex;
  align-items: center;
  padding: 5px 10px;
  margin-bottom: 0;
  border-bottom: 1px solid rgba(0,0,0,.125);
}

.card-title {
  font-size: 1.5rem;
  margin: 0 0 0 10px !important;
}

.card-body {
  padding-left: 20px;
  display: block;
  box-sizing: border-box;
}

.card-text {
  font-size: 1.2rem;
  line-height: 1.5;
  margin-left: 10px;
}

.table-wrapper {
  --tb-even-bg: #2C2B2B;
  --tb-odd-bg: #2C2B2B;
  --tb-border-color: rgba(255,255,255,.2);
}

.table-cell-label{
  text-align: right;
  padding: 0.2rem .5rem !important;
}

.table-cell-data{
  text-align: left;
  padding-left: 0px !important;
  padding-right: 0px !important;
  margin-left: 0px !important;
}

.table-cell-spacer{
  padding-left: 0px !important;
  padding-right: 0px !important;
  margin-left: 0px !important;
}

.unique_info {
  margin: 10px;
  padding-left: 8px;
  border: 1px solid rgba(255,255,255,.2);
  width: 180px;
  height: 120px;
}
</style>

{% assign grouped_schools = site.data.spell_data | group_by: 'school' | sort: 'school' %}
{% assign sorted_schools = grouped_schools | sort: 'name'%}
{% for spell_group in sorted_schools %}

## {{spell_group.name}} Spells

<hr>
{% assign sorted_spells = spell_group.items | sort: 'name' %}
{% for spell in sorted_spells %}
<div class="card-container">
  <div class="card-header2">
    <h3 id="{{spell.name}}" class="card-title">{{spell.name}}</h3>
  </div>
  <div class="card-body">
    <div style="display: flex">
      <div style="min-width: 130px; max-width: 130px; float: left">
        <div id="image_wrapper" style="position: relative"> 
          <img src="/img/spell_frame.png" style="width: 120px; image-rendering: pixelated; position: relative; top:0; left: 0;">
          <img src="{{spell.icon}}" style="width: 80px; image-rendering: pixelated; position: absolute; top: 43px; left: 20px;">
        </div>
      </div>
      <div style="min-width: 420px; max-width:420px; float: left">
        <table style="width: 100%;">
        <tr>
          <td class="table-cell-label">School:</td>
          <td class="table-cell-data">{{spell_group.name}}</td>
          <td class="table-cell-spacer"></td>
          <td class="table-cell-label">Level:</td>
          <td class="table-cell-data">{{spell.level}}</td>
        </tr>
        <tr>
          <td class="table-cell-label">Cooldown:</td>
          <td class="table-cell-data">{{spell.cooldown}}</td>
          <td class="table-cell-spacer"></td>
          <td class="table-cell-label">Mana:</td>
          <td class="table-cell-data">{{spell.mana}}</td>
        </tr>
        <tr>
          <td class="table-cell-label">Cast Type:</td>
          <td class="table-cell-data">{{spell.cast_type}}</td>
          <td class="table-cell-spacer"></td>
          <td class="table-cell-label">Rarity:</td>
          <td class="table-cell-data">{{spell.rarity}}</td>
        </tr>
        </table>
      </div>
      {% if spell.u1 != "" %}
      <div style="display: flex; float: right;">
        <div class="unique_info">
          {{spell.u1}}<br>
          {{spell.u2}}<br>
          {{spell.u3}}<br>
          {{spell.u4}}<br>
        </div>
      </div>
      {% endif %}
    </div>
    <div style="">
      {{spell.description}}
    </div>
  </div>
</div>
{% endfor %}
{% endfor %}
<!-- buffer for the TOC -->
<div style="height: 800px"></div>



