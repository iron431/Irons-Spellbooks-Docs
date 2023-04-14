---
layout: post
icon: fa-regular fa-gem
order: 6
toc: true
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

.card-footer2 {
  background-color: #303030;
  display: flex;
  align-items: center;
  padding: 5px 10px;
  margin-top: 0;
  margin-bottom: 0;
  border-top: 1px solid rgba(0,0,0,.125);
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

{% assign sorted = site.data.item_data | sort: 'name'%}
{% for recipe in sorted %}
<div class="card-container">
  <div class="card-header2">
    <h3 id="{{recipe.path}}" class="card-title">{{recipe.name}}</h3>
  </div>
  <div class="card-body">
    <div style="display: flex">
      <div style="min-width: 160px; max-width: 160px; position: relative; padding-left: 30px">
        <div id="image_wrapper" style="position: relative"> 
          <img src="/img/spell_frame.png" style="width: 120px; image-rendering: pixelated; position: relative; top:30px; left: 10px;">
          <img src="/img/item_background.png" style="width: 80px; image-rendering: pixelated; position: absolute; top: 65px; left: 30px;">
          <img src="{{recipe.path}}" style="width: 75px; image-rendering: pixelated; position: absolute; top: 68px; left: 31px;" title="{{recipe.name}}">
        </div>
      </div>
      <div style="min-width: 420px; max-width:420px; position: relative; margin: auto">
          <img id="crafting_table" src="/img/crafting_table.png" style="width: 420px; image-rendering: pixelated; position: relative; top:0; left: 0;">
          <img id="slot1" src="{{recipe.item0Path}}" style="width: 50px; image-rendering: pixelated; position: absolute; top: 24px; left: 19px;" title="{{recipe.item0}}">
          <img id="slot2" src="{{recipe.item1Path}}" style="width: 50px; image-rendering: pixelated; position: absolute; top: 24px; left: 78px;" title="{{recipe.item1}}">
          <img id="slot3" src="{{recipe.item2Path}}" style="width: 50px; image-rendering: pixelated; position: absolute; top: 24px; left: 137px;" title="{{recipe.item2}}">
          <img id="slot4" src="{{recipe.item3Path}}" style="width: 50px; image-rendering: pixelated; position: absolute; top: 83px; left: 19px;" title="{{recipe.item3}}">
          <img id="slot5" src="{{recipe.item4Path}}" style="width: 50px; image-rendering: pixelated; position: absolute; top: 83px; left: 78px;" title="{{recipe.item4}}">
          <img id="slot6" src="{{recipe.item5Path}}" style="width: 50px; image-rendering: pixelated; position: absolute; top: 83px; left: 137px;" title="{{recipe.item5}}">
          <img id="slot7" src="{{recipe.item6Path}}" style="width: 50px; image-rendering: pixelated; position: absolute; top: 142px; left: 19px;" title="{{recipe.item6}}">
          <img id="slot8" src="{{recipe.item7Path}}" style="width: 50px; image-rendering: pixelated; position: absolute; top: 142px; left: 78px;" title="{{recipe.item7}}">
          <img id="slot9" src="{{recipe.item8Path}}" style="width: 50px; image-rendering: pixelated; position: absolute; top: 142px; left: 137px;" title="{{recipe.item8}}">
          <img id="output" src="{{recipe.path}}" style="width: 75px; image-rendering: pixelated; position: absolute; top: 72px; left: 315px;" title="{{recipe.name}}">
      </div>
    </div>
  </div>
  <div class="card-footer2">
    <div style="padding: 5px;">
      {{recipe.description}}
    </div>
  </div>
</div>
{% endfor %}

<!-- buffer for the TOC -->
<div style="height: 800px"></div>



