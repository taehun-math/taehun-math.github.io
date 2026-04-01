---
layout: page
title: talks
permalink: /talks/
description: Seminar talks, series lectures, and conference organization
nav: true
nav_order: 3
---

<style>
  .tk-tabs { display: flex; gap: 0; border-bottom: 1px solid #ddd; margin-bottom: 1.8rem; }
  .tk-tab { padding: 8px 16px; font-size: 14px; color: #888; cursor: pointer; border-bottom: 2px solid transparent; background: none; border-top: none; border-left: none; border-right: none; font-family: inherit; }
  .tk-tab.active { color: #333; border-bottom-color: #333; font-weight: 600; }
  .tk-tab:hover:not(.active) { color: #555; }
  .tk-section { display: none; }
  .tk-section.active { display: block; }

  .tk-tl { position: relative; padding-left: 28px; }
  .tk-tl::before { content: ''; position: absolute; left: 7px; top: 0; bottom: 0; width: 1.5px; background: #ddd; }
  .tk-year { position: relative; margin-bottom: 1.8rem; }
  .tk-dot { position: absolute; left: -28px; top: 4px; width: 15px; height: 15px; border-radius: 50%; border: 2px solid #bbb; background: #fff; z-index: 1; }
  .tk-dot.now { border-color: #1a73e8; background: #e8f0fe; }
  .tk-year-label { font-size: 15px; font-weight: 600; color: #1a1a1a; margin-bottom: 10px; cursor: pointer; user-select: none; }
  .tk-year-label .tk-toggle { font-size: 12px; color: #bbb; margin-left: 6px; transition: transform 0.2s; display: inline-block; }
  .tk-year-label .tk-toggle.open { transform: rotate(90deg); }
  .tk-count { font-size: 12px; font-weight: 400; color: #999; margin-left: 4px; }
  .tk-now-tag { display: inline-block; font-size: 10px; padding: 2px 8px; border-radius: 4px; background: #e8f0fe; color: #1a73e8; font-weight: 600; margin-left: 8px; vertical-align: middle; }

  .tk-list { display: flex; flex-direction: column; gap: 6px; }
  .tk-list.collapsed { display: none; }
  .tk-item { display: flex; gap: 10px; align-items: baseline; padding: 6px 0; border-bottom: 1px solid #f5f5f5; }
  .tk-item:last-child { border-bottom: none; }
  .tk-badge { flex-shrink: 0; display: inline-block; font-size: 10px; padding: 2px 8px; border-radius: 4px; font-weight: 600; min-width: 70px; text-align: center; }
  .b-seminar { background: #E6F1FB; color: #0C447C; }
  .b-conf { background: #EEEDFE; color: #3C3489; }
  .b-workshop { background: #E1F5EE; color: #085041; }
  .b-school { background: #FAEEDA; color: #633806; }
  .b-colloq { background: #FAECE7; color: #712B13; }
  .tk-venue { font-size: 13px; color: #1a1a1a; line-height: 1.5; }
  .tk-venue a { color: #1a73e8; text-decoration: none; }
  .tk-venue a:hover { text-decoration: underline; }
  .tk-loc { font-size: 12px; color: #999; }

  .tk-cards { display: flex; flex-direction: column; gap: 10px; }
  .tk-card { background: #fff; border: 1px solid #eee; border-radius: 10px; padding: 14px 18px; transition: border-color 0.15s; }
  .tk-card:hover { border-color: #ccc; }
  .tk-card-title { font-size: 14px; font-weight: 600; color: #1a1a1a; margin-bottom: 4px; line-height: 1.4; }
  .tk-card-title a { color: #1a73e8; text-decoration: none; }
  .tk-card-title a:hover { text-decoration: underline; }
  .tk-card-sub { font-size: 13px; color: #666; line-height: 1.5; margin-bottom: 2px; }
  .tk-card-meta { font-size: 12px; color: #999; }
  .tk-card-badge { display: inline-block; font-size: 10px; padding: 2px 8px; border-radius: 4px; font-weight: 600; margin-bottom: 6px; }
  .b-series { background: #FBEAF0; color: #72243E; }
  .b-org { background: #FAECE7; color: #712B13; }

  .tk-legend { display: flex; gap: 12px; flex-wrap: wrap; margin-bottom: 1.2rem; }
  .tk-legend-item { display: flex; align-items: center; gap: 5px; font-size: 12px; color: #888; }
  .tk-legend-dot { width: 10px; height: 10px; border-radius: 3px; }

  /* dark mode */
  html[data-theme="dark"] .tk-tl::before { background: #333; }
  html[data-theme="dark"] .tk-dot { border-color: #555; background: #1a1a1a; }
  html[data-theme="dark"] .tk-dot.now { border-color: #5b9cf6; background: #1e2a3a; }
  html[data-theme="dark"] .tk-year-label { color: #e0e0e0; }
  html[data-theme="dark"] .tk-now-tag { background: #1e2a3a; color: #5b9cf6; }
  html[data-theme="dark"] .tk-venue { color: #e0e0e0; }
  html[data-theme="dark"] .tk-venue a { color: #5b9cf6; }
  html[data-theme="dark"] .tk-item { border-bottom-color: #222; }
  html[data-theme="dark"] .tk-card { background: #1a1a1a; border-color: #333; }
  html[data-theme="dark"] .tk-card:hover { border-color: #555; }
  html[data-theme="dark"] .tk-card-title { color: #e0e0e0; }
  html[data-theme="dark"] .tk-card-title a { color: #5b9cf6; }
  html[data-theme="dark"] .tk-card-sub { color: #aaa; }
  html[data-theme="dark"] .tk-tabs { border-bottom-color: #333; }
  html[data-theme="dark"] .tk-tab { color: #777; }
  html[data-theme="dark"] .tk-tab.active { color: #e0e0e0; border-bottom-color: #e0e0e0; }
  html[data-theme="dark"] .b-seminar { background: #042C53; color: #B5D4F4; }
  html[data-theme="dark"] .b-conf { background: #26215C; color: #CECBF6; }
  html[data-theme="dark"] .b-workshop { background: #04342C; color: #9FE1CB; }
  html[data-theme="dark"] .b-school { background: #412402; color: #FAC775; }
  html[data-theme="dark"] .b-colloq { background: #4A1B0C; color: #F5C4B3; }
  html[data-theme="dark"] .b-series { background: #4B1528; color: #F4C0D1; }
  html[data-theme="dark"] .b-org { background: #4A1B0C; color: #F5C4B3; }
</style>

<div class="tk-tabs">
  <button class="tk-tab active" onclick="showTkTab('seminars', this)">seminar talks</button>
  <button class="tk-tab" onclick="showTkTab('series', this)">series lectures</button>
  <button class="tk-tab" onclick="showTkTab('org', this)">organization</button>
</div>

<div id="seminars" class="tk-section active">
{% include talks_seminars.liquid %}
</div>

<div id="series" class="tk-section">
{% include talks_series.liquid %}
</div>

<div id="org" class="tk-section">
{% include talks_organization.liquid %}
</div>

<script>
function showTkTab(id, btn) {
  document.querySelectorAll('.tk-section').forEach(function(el) { el.classList.remove('active'); });
  document.querySelectorAll('.tk-tab').forEach(function(el) { el.classList.remove('active'); });
  document.getElementById(id).classList.add('active');
  btn.classList.add('active');
}
function toggleYear(label) {
  var list = label.nextElementSibling;
  var toggle = label.querySelector('.tk-toggle');
  list.classList.toggle('collapsed');
  toggle.classList.toggle('open');
}
</script>
