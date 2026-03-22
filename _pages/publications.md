---
layout: page
title: publications
permalink: /publications/
description: Published papers and preprints
nav: true
nav_order: 2
years: [2025, 2024, 2023, 2022, 2021]
---

<style>
  /* field-based badge colors — override al-folio default */
  .bibliography .badge.badge-geom { background-color: #1D9E75 !important; }
  .bibliography .badge.badge-pde { background-color: #7F77DD !important; }
  .bibliography .badge.badge-net { background-color: #EF9F27 !important; }
  .bibliography .badge.badge-pre { background-color: #888780 !important; }

  /* legend */
  .pub-legend { display: flex; gap: 14px; flex-wrap: wrap; margin-bottom: 1.5rem; }
  .pub-legend-item { display: flex; align-items: center; gap: 5px; font-size: 13px; color: #888; }
  .pub-legend-dot { width: 10px; height: 10px; border-radius: 3px; }
</style>

<div class="pub-legend">
  <div class="pub-legend-item"><div class="pub-legend-dot" style="background:#1D9E75;"></div> geometric analysis</div>
  <div class="pub-legend-item"><div class="pub-legend-dot" style="background:#7F77DD;"></div> analysis &amp; PDE</div>
  <div class="pub-legend-item"><div class="pub-legend-dot" style="background:#EF9F27;"></div> networks &amp; applied</div>
</div>

<!-- al-folio default bibliography rendering -->
{% bibliography %}

<script>
document.addEventListener('DOMContentLoaded', function() {
  var fieldMap = {
    'Adv. Math.': 'geom',
    'Math. Ann.': 'geom',
    'Trans. AMS': 'geom',
    'Proc. AMS': 'geom',
    'Calc. Var. PDE': 'geom',
    'Adv. Nonlinear Anal.': 'geom',
    'IMRN': 'pde',
    'JDE': 'pde',
    'Nonlinear Anal.': 'pde',
    'Phys. Rev. E': 'net',
    'Preprint': 'pre',
    'Submitted': 'pre'
  };
  document.querySelectorAll('.bibliography .badge').forEach(function(badge) {
    var text = badge.textContent.trim();
    var field = fieldMap[text];
    if (field) {
      badge.classList.add('badge-' + field);
    }
  });
});
</script>
