---
layout: page
title: teaching
permalink: /teaching/
description: Courses at Konkuk University and Seoul National University
nav: true
nav_order: 4
---

<style>
  .tl { position: relative; padding-left: 28px; }
  .tl::before { content: ''; position: absolute; left: 7px; top: 0; bottom: 0; width: 1.5px; background: #ddd; }
  .tl-sem { position: relative; margin-bottom: 2rem; }
  .tl-dot { position: absolute; left: -28px; top: 3px; width: 15px; height: 15px; border-radius: 50%; border: 2px solid #bbb; background: #fff; z-index: 1; }
  .tl-dot.now { border-color: #1a73e8; background: #e8f0fe; }
  .tl-sem-label { font-size: 15px; font-weight: 600; color: #1a1a1a; margin-bottom: 10px; }
  .tl-inst { font-size: 13px; font-weight: 400; color: #999; margin-left: 6px; }
  .tl-now-tag { display: inline-block; font-size: 10px; padding: 2px 8px; border-radius: 4px; background: #e8f0fe; color: #1a73e8; font-weight: 600; margin-left: 8px; vertical-align: middle; }
  .tl-cards { display: flex; flex-wrap: wrap; gap: 10px; }
  .tl-card { background: #fff; border: 1px solid #eee; border-radius: 10px; padding: 12px 16px; min-width: 200px; flex: 1; max-width: 340px; transition: border-color 0.15s; }
  .tl-card:hover { border-color: #ccc; }
  .tl-badge { display: inline-block; font-size: 10px; padding: 2px 8px; border-radius: 4px; font-weight: 600; margin-bottom: 6px; }
  .b-grad { background: #EEEDFE; color: #3C3489; }
  .b-ugrad { background: #E1F5EE; color: #085041; }
  .b-calc { background: #FAEEDA; color: #633806; }
  .b-guest { background: #FAECE7; color: #712B13; }
  .tl-cname { font-size: 14px; font-weight: 600; color: #1a1a1a; margin-bottom: 3px; }
  .tl-cmeta { font-size: 12px; color: #999; line-height: 1.5; }

  /* dark mode */
  html[data-theme="dark"] .tl::before { background: #333; }
  html[data-theme="dark"] .tl-dot { border-color: #555; background: #1a1a1a; }
  html[data-theme="dark"] .tl-dot.now { border-color: #5b9cf6; background: #1e2a3a; }
  html[data-theme="dark"] .tl-sem-label { color: #e0e0e0; }
  html[data-theme="dark"] .tl-inst { color: #777; }
  html[data-theme="dark"] .tl-now-tag { background: #1e2a3a; color: #5b9cf6; }
  html[data-theme="dark"] .tl-card { background: #1a1a1a; border-color: #333; }
  html[data-theme="dark"] .tl-card:hover { border-color: #555; }
  html[data-theme="dark"] .tl-cname { color: #e0e0e0; }
  html[data-theme="dark"] .tl-cmeta { color: #777; }
  html[data-theme="dark"] .b-grad { background: #26215C; color: #CECBF6; }
  html[data-theme="dark"] .b-ugrad { background: #04342C; color: #9FE1CB; }
  html[data-theme="dark"] .b-calc { background: #412402; color: #FAC775; }
  html[data-theme="dark"] .b-guest { background: #4A1B0C; color: #F5C4B3; }
</style>

<div class="tl">

  <div class="tl-sem">
    <div class="tl-dot now"></div>
    <div class="tl-sem-label">Spring 2026 <span class="tl-inst">Konkuk University</span> <span class="tl-now-tag">current</span></div>
    <div class="tl-cards">
      <div class="tl-card">
        <span class="tl-badge b-ugrad">Undergraduate</span>
        <div class="tl-cname">Introduction to Analysis 1</div>
        <div class="tl-cmeta">Abbott, 2nd ed.</div>
      </div>
      <div class="tl-card">
        <span class="tl-badge b-grad">Graduate</span>
        <div class="tl-cname">Real Analysis 1</div>
        <div class="tl-cmeta">Royden &amp; Fitzpatrick, 4th ed.</div>
      </div>
    </div>
  </div>

  <div class="tl-sem">
    <div class="tl-dot"></div>
    <div class="tl-sem-label">Fall 2025 <span class="tl-inst">Konkuk University</span></div>
    <div class="tl-cards">
      <div class="tl-card">
        <span class="tl-badge b-ugrad">Undergraduate</span>
        <div class="tl-cname">Introduction to Analysis 2</div>
      </div>
      <div class="tl-card">
        <span class="tl-badge b-grad">Graduate</span>
        <div class="tl-cname">Topics in Analysis 2</div>
      </div>
    </div>
  </div>

  <div class="tl-sem">
    <div class="tl-dot"></div>
    <div class="tl-sem-label">Spring 2025 <span class="tl-inst">Konkuk University</span></div>
    <div class="tl-cards">
      <div class="tl-card">
        <span class="tl-badge b-ugrad">Undergraduate</span>
        <div class="tl-cname">Introduction to Analysis 1</div>
      </div>
      <div class="tl-card">
        <span class="tl-badge b-calc">Calculus</span>
        <div class="tl-cname">College Mathematics 1</div>
      </div>
    </div>
  </div>

  <div class="tl-sem">
    <div class="tl-dot"></div>
    <div class="tl-sem-label">Spring 2024 <span class="tl-inst">Seoul National University</span></div>
    <div class="tl-cards">
      <div class="tl-card">
        <span class="tl-badge b-guest">Dept. of Math Education</span>
        <div class="tl-cname">Differential Geometry</div>
      </div>
    </div>
  </div>

</div>
