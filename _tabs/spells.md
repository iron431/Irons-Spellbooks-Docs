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

.unique_info {
  margin: 10px;
  padding: 10px;
  border: 1px solid rgba(255,255,255,.2);
  display: block;
}

</style>


{% assign grouped_schools = site.spells | group_by: 'school' | sort: 'school' %}
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
      <div style="display: inline-block; min-width: 130px; max-width: 130px;">
        <div id="image_wrapper" style="position: relative"> 
          <img src="../img/spell_frame.png" style="width: 120px; image-rendering: pixelated; position: relative; top:0; left: 0;">
          <img src="../img/spells/angel_wing.png" style="width: 80px; image-rendering: pixelated; position: absolute; top: 43px; left: 20px;">
        </div>
      </div>
      <div style="display: inline-block;">
        <table>
        <tr>
          <td>School:</td>
          <td>{{spell_group.name}}</td>
          <td></td>
          <td>Cast Type:</td>
          <td>Long</td>
        </tr>
        <tr>
          <td>Level:</td>
          <td>1 to 10</td>
          <td></td>
          <td>Mana:</td>
          <td>50 to 100</td>
        </tr>
        <tr>
          <td>Cooldown:</td>
          <td>5s</td>
          <td></td>
          <td>Rarity:</td>
          <td>X to Y</td>
        </tr>
        </table>
      </div>
      <div>
        <div class="unique_info">
          Testing sldkfjsdlkj<br>
          Testing sldkfjsdlkj<br>
          Testing sldkfjsdlkj<br>
        </div>
      </div>
    </div>
    <div style="">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </div>
  </div>
</div>
{% endfor %}
{% endfor %}
<!-- buffer for the TOC -->
<div style="height: 800px"></div>



