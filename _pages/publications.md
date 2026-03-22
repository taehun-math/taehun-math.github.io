---
layout: page
title: publications
permalink: /publications/
description: Published papers, preprints, and collaborators
nav: true
nav_order: 2
---

<style>
  .pub-filters { margin-bottom: 1.5rem; }
  .pub-filter-label { font-size: 12px; font-weight: 600; color: #999; text-transform: uppercase; letter-spacing: 0.5px; margin-bottom: 8px; }
  .pub-chips { display: flex; flex-wrap: wrap; gap: 6px; }
  .pub-chip { font-size: 12px; padding: 4px 12px; border-radius: 20px; border: 1px solid #ddd; background: none; color: #666; cursor: pointer; font-family: inherit; transition: all 0.15s; }
  .pub-chip:hover { border-color: #999; color: #333; }
  .pub-chip.active { background: #1a1a1a; color: #fff; border-color: #1a1a1a; }

  .pub-section-label { font-size: 13px; font-weight: 600; color: #999; text-transform: uppercase; letter-spacing: 0.5px; margin: 1.5rem 0 0.8rem; padding-bottom: 6px; border-bottom: 1px solid #eee; }

  .pub-list { display: flex; flex-direction: column; gap: 0; }
  .pub-item { padding: 14px 0; border-bottom: 1px solid #f5f5f5; display: grid; grid-template-columns: 90px minmax(0,1fr); gap: 14px; transition: opacity 0.2s; }
  .pub-item:last-child { border-bottom: none; }
  .pub-item.hidden { display: none; }

  .pub-badge { display: inline-block; font-size: 10px; padding: 3px 8px; border-radius: 4px; font-weight: 600; text-align: center; line-height: 1.3; width: 82px; word-wrap: break-word; }
  .b-geom { background: #E1F5EE; color: #085041; }
  .b-pde { background: #EEEDFE; color: #3C3489; }
  .b-net { background: #FAEEDA; color: #633806; }
  .b-pre { background: #F1EFE8; color: #444441; }

  .pub-title { font-size: 14px; font-weight: 600; color: #1a1a1a; line-height: 1.45; margin-bottom: 3px; }
  .pub-authors { font-size: 13px; color: #666; margin-bottom: 3px; line-height: 1.5; }
  .pub-authors .me { font-weight: 600; color: #1a1a1a; }
  .pub-authors .coauthor { cursor: pointer; }
  .pub-authors .coauthor:hover { color: #1a73e8; text-decoration: underline; }
  .pub-journal { font-size: 12px; color: #999; }
  .pub-links { margin-top: 4px; display: flex; gap: 6px; flex-wrap: wrap; }
  .pub-link { font-size: 11px; padding: 2px 8px; border-radius: 4px; border: 1px solid #ddd; color: #666; text-decoration: none; transition: all 0.15s; }
  .pub-link:hover { border-color: #999; color: #333; }

  .pub-year-marker { font-size: 22px; font-weight: 600; color: #ddd; padding-top: 6px; text-align: right; }

  /* coworker section */
  .coworker-section { margin-top: 2.5rem; padding-top: 1.5rem; border-top: 1px solid #eee; }
  .coworker-grid { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 10px; }
  .coworker-btn { font-size: 13px; padding: 6px 14px; border-radius: 8px; border: 1px solid #eee; background: #fff; color: #333; cursor: pointer; font-family: inherit; transition: all 0.15s; }
  .coworker-btn:hover { border-color: #999; }
  .coworker-btn.active { background: #1a1a1a; color: #fff; border-color: #1a1a1a; }
  .coworker-count { font-size: 11px; color: #bbb; margin-left: 4px; }

  /* legend */
  .pub-legend { display: flex; gap: 14px; flex-wrap: wrap; margin-bottom: 1.2rem; }
  .pub-legend-item { display: flex; align-items: center; gap: 5px; font-size: 12px; color: #888; }
  .pub-legend-dot { width: 10px; height: 10px; border-radius: 3px; }

  /* dark mode */
  html[data-theme="dark"] .pub-chip { border-color: #444; color: #aaa; }
  html[data-theme="dark"] .pub-chip:hover { border-color: #777; color: #e0e0e0; }
  html[data-theme="dark"] .pub-chip.active { background: #e0e0e0; color: #1a1a1a; border-color: #e0e0e0; }
  html[data-theme="dark"] .pub-section-label { color: #777; border-bottom-color: #333; }
  html[data-theme="dark"] .pub-item { border-bottom-color: #222; }
  html[data-theme="dark"] .pub-title { color: #e0e0e0; }
  html[data-theme="dark"] .pub-authors { color: #aaa; }
  html[data-theme="dark"] .pub-authors .me { color: #e0e0e0; }
  html[data-theme="dark"] .pub-authors .coauthor:hover { color: #5b9cf6; }
  html[data-theme="dark"] .pub-link { border-color: #444; color: #aaa; }
  html[data-theme="dark"] .pub-link:hover { border-color: #777; color: #e0e0e0; }
  html[data-theme="dark"] .pub-year-marker { color: #333; }
  html[data-theme="dark"] .coworker-section { border-top-color: #333; }
  html[data-theme="dark"] .coworker-btn { background: #1a1a1a; border-color: #333; color: #ccc; }
  html[data-theme="dark"] .coworker-btn:hover { border-color: #666; }
  html[data-theme="dark"] .coworker-btn.active { background: #e0e0e0; color: #1a1a1a; border-color: #e0e0e0; }
  html[data-theme="dark"] .b-geom { background: #04342C; color: #9FE1CB; }
  html[data-theme="dark"] .b-pde { background: #26215C; color: #CECBF6; }
  html[data-theme="dark"] .b-net { background: #412402; color: #FAC775; }
  html[data-theme="dark"] .b-pre { background: #2C2C2A; color: #D3D1C7; }
</style>

<div class="pub-legend">
  <div class="pub-legend-item"><div class="pub-legend-dot" style="background:#1D9E75;"></div> geometry &amp; convexity</div>
  <div class="pub-legend-item"><div class="pub-legend-dot" style="background:#7F77DD;"></div> analysis &amp; PDE</div>
  <div class="pub-legend-item"><div class="pub-legend-dot" style="background:#EF9F27;"></div> networks &amp; applied</div>
</div>

<!-- ============================================================ -->
<!--                       PUBLISHED                              -->
<!-- ============================================================ -->
<div class="pub-section-label">Published</div>
<div class="pub-list">

  <!-- 2025 -->
  <div class="pub-item" data-authors="kang,kiahm" data-field="geom">
    <div><div class="pub-badge b-geom">Adv. Nonlinear Anal.</div><div class="pub-year-marker">2025</div></div>
    <div>
      <div class="pub-title">&alpha;-mean curvature flow of non-compact complete convex hypersurface</div>
      <div class="pub-authors">Hyunsuk Kang, <span class="coauthor" onclick="filterCoauthor('kiahm')">Ki-Ahm Lee</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://www.degruyterbrill.com/document/doi/10.1515/anona-2025-0101/html" target="_blank">journal</a>
      </div>
    </div>
  </div>

  <div class="pub-item" data-authors="choiks,huang" data-field="geom">
    <div><div class="pub-badge b-geom">Trans. AMS</div></div>
    <div>
      <div class="pub-title">Ancient mean curvature flows with finite total curvature</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('choiks')">Kyeongsu Choi</span>, Jiuzhou Huang, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://www.ams.org/journals/tran/2025-378-09/S0002-9947-2025-09473-X/home.html" target="_blank">journal</a>
        <a class="pub-link" href="https://arxiv.org/abs/2405.01062" target="_blank">arXiv</a>
      </div>
    </div>
  </div>

  <!-- 2024 -->
  <div class="pub-item" data-authors="choiks,minhyun" data-field="geom">
    <div><div class="pub-badge b-geom">Adv. Math.</div><div class="pub-year-marker">2024</div></div>
    <div>
      <div class="pub-title">Curvature bound for L<sub>p</sub> Minkowski problem</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('choiks')">Kyeongsu Choi</span>, <span class="coauthor" onclick="filterCoauthor('minhyun')">Minhyun Kim</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://www.sciencedirect.com/science/article/pii/S0001870824004742" target="_blank">journal</a>
        <a class="pub-link" href="https://arxiv.org/abs/2304.11617" target="_blank">arXiv</a>
      </div>
    </div>
  </div>

  <div class="pub-item" data-authors="minhyun" data-field="geom">
    <div><div class="pub-badge b-geom">Proc. AMS</div></div>
    <div>
      <div class="pub-title">Diameter estimate for planar L<sub>p</sub> dual Minkowski problem</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('minhyun')">Minhyun Kim</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://www.ams.org/journals/proc/0000-000-00/S0002-9939-2024-16464-9/" target="_blank">journal</a>
        <a class="pub-link" href="https://arxiv.org/abs/2208.06284" target="_blank">arXiv</a>
      </div>
    </div>
  </div>

  <!-- 2023 -->
  <div class="pub-item" data-authors="kiahm" data-field="geom">
    <div><div class="pub-badge b-geom">Math. Ann.</div><div class="pub-year-marker">2023</div></div>
    <div>
      <div class="pub-title">Gauss curvature flow with shrinking obstacle</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('kiahm')">Ki-Ahm Lee</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://link.springer.com/article/10.1007/s00208-023-02739-y" target="_blank">journal</a>
        <a class="pub-link" href="https://arxiv.org/abs/2310.02668" target="_blank">arXiv</a>
      </div>
    </div>
  </div>

  <div class="pub-item" data-authors="" data-field="pde">
    <div><div class="pub-badge b-pde">IMRN</div></div>
    <div>
      <div class="pub-title">An eigenvalue problem for prescribed curvature equations</div>
      <div class="pub-authors"><span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://academic.oup.com/imrn/advance-article/doi/10.1093/imrn/rnad220/7277559" target="_blank">journal</a>
        <a class="pub-link" href="https://arxiv.org/abs/2304.07614" target="_blank">arXiv</a>
      </div>
    </div>
  </div>

  <!-- 2022 -->
  <div class="pub-item" data-authors="kangju,kiahm,kook" data-field="net">
    <div><div class="pub-badge b-net">Phys. Rev. E</div><div class="pub-year-marker">2022</div></div>
    <div>
      <div class="pub-title">Fractional centralities on networks: consolidating the local and the global</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('kangju')">Kang-Ju Lee</span>, <span class="coauthor" onclick="filterCoauthor('kiahm')">Ki-Ahm Lee</span>, <span class="coauthor" onclick="filterCoauthor('kook')">Woong Kook</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://journals.aps.org/pre/abstract/10.1103/PhysRevE.106.034310" target="_blank">journal</a>
      </div>
    </div>
  </div>

  <div class="pub-item" data-authors="kiahm,park" data-field="pde">
    <div><div class="pub-badge b-pde">JDE</div></div>
    <div>
      <div class="pub-title">The obstacle problem for parabolic Monge-Amp&egrave;re equation</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('kiahm')">Ki-Ahm Lee</span>, <span class="coauthor" onclick="filterCoauthor('park')">Jinwan Park</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://www.sciencedirect.com/science/article/abs/pii/S0022039621007488" target="_blank">journal</a>
      </div>
    </div>
  </div>

  <!-- 2021 -->
  <div class="pub-item" data-authors="kiahm,park" data-field="pde">
    <div><div class="pub-badge b-pde">Nonlinear Anal.</div><div class="pub-year-marker">2021</div></div>
    <div>
      <div class="pub-title">The obstacle problem for the Monge-Amp&egrave;re equation with the lower obstacle</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('kiahm')">Ki-Ahm Lee</span>, <span class="coauthor" onclick="filterCoauthor('park')">Jinwan Park</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://www.sciencedirect.com/science/article/abs/pii/S0362546X21000821" target="_blank">journal</a>
      </div>
    </div>
  </div>

  <div class="pub-item" data-authors="gonzalez,kiahm" data-field="pde">
    <div><div class="pub-badge b-pde">JDE</div></div>
    <div>
      <div class="pub-title">Optimal configuration and symmetry breaking phenomena in the composite membrane problem with fractional Laplacian</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('gonzalez')">Maria del Mar Gonzalez</span>, <span class="coauthor" onclick="filterCoauthor('kiahm')">Ki-Ahm Lee</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://www.sciencedirect.com/science/article/abs/pii/S002203962030591X" target="_blank">journal</a>
        <a class="pub-link" href="https://arxiv.org/abs/2004.08983" target="_blank">arXiv</a>
      </div>
    </div>
  </div>

  <div class="pub-item" data-authors="kiahm" data-field="geom">
    <div><div class="pub-badge b-geom">Calc. Var. PDE</div></div>
    <div>
      <div class="pub-title">Gauss curvature flow with an obstacle</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('kiahm')">Ki-Ahm Lee</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://link.springer.com/article/10.1007/s00526-021-02029-y" target="_blank">journal</a>
      </div>
    </div>
  </div>

</div>

<!-- ============================================================ -->
<!--                       PREPRINTS                              -->
<!-- ============================================================ -->
<div class="pub-section-label">Preprints</div>
<div class="pub-list">

  <div class="pub-item" data-authors="takwon" data-field="pde">
    <div><div class="pub-badge b-pde">arXiv 2025</div></div>
    <div>
      <div class="pub-title">Liouville-type theorems for Lane–Emden inequalities involving nonlocal operators</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('takwon')">Takwon Kim</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://arxiv.org/abs/2602.13822" target="_blank">arXiv</a>
      </div>
    </div>
  </div>

  <div class="pub-item" data-authors="sanghoon" data-field="pde">
    <div><div class="pub-badge b-pde">arXiv 2025</div></div>
    <div>
      <div class="pub-title">Nodal set comparison for Allen–Cahn solutions with conical asymptotics</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('sanghoon')">Sanghoon Lee</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://arxiv.org/abs/2601.05015" target="_blank">arXiv</a>
      </div>
    </div>
  </div>

  <div class="pub-item" data-authors="kangju,kiahm,kook" data-field="net">
    <div><div class="pub-badge b-net">Submitted</div></div>
    <div>
      <div class="pub-title">Fractional degree centrality for directed networks</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('kangju')">Kang-Ju Lee</span>, <span class="coauthor" onclick="filterCoauthor('kiahm')">Ki-Ahm Lee</span>, <span class="coauthor" onclick="filterCoauthor('kook')">Woong Kook</span>, <span class="me">Taehun Lee</span></div>
    </div>
  </div>

  <div class="pub-item" data-authors="kiahm" data-field="geom">
    <div><div class="pub-badge b-geom">arXiv 2023</div></div>
    <div>
      <div class="pub-title">On the uniqueness of energy-minimizing curves in constrained spaces</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('kiahm')">Ki-Ahm Lee</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://arxiv.org/abs/2306.07511" target="_blank">arXiv</a>
      </div>
    </div>
  </div>

  <div class="pub-item" data-authors="minhyun" data-field="geom">
    <div><div class="pub-badge b-geom">arXiv 2021</div></div>
    <div>
      <div class="pub-title">The discrete logarithmic Minkowski problem for the electrostatic &#x1D52D;-capacity</div>
      <div class="pub-authors"><span class="coauthor" onclick="filterCoauthor('minhyun')">Minhyun Kim</span>, <span class="me">Taehun Lee</span></div>
      <div class="pub-links">
        <a class="pub-link" href="https://arxiv.org/abs/2111.07321" target="_blank">arXiv</a>
      </div>
    </div>
  </div>

</div>

<!-- ============================================================ -->
<!--                      COLLABORATORS                           -->
<!-- ============================================================ -->
<div class="coworker-section">
  <div class="pub-filter-label">Filter by collaborator</div>
  <div class="coworker-grid">
    <button class="coworker-btn" onclick="filterCoauthor('kiahm')">Ki-Ahm Lee <span class="coworker-count">8</span></button>
    <button class="coworker-btn" onclick="filterCoauthor('choiks')">Kyeongsu Choi <span class="coworker-count">2</span></button>
    <button class="coworker-btn" onclick="filterCoauthor('minhyun')">Minhyun Kim <span class="coworker-count">3</span></button>
    <button class="coworker-btn" onclick="filterCoauthor('park')">Jinwan Park <span class="coworker-count">2</span></button>
    <button class="coworker-btn" onclick="filterCoauthor('kangju')">Kang-Ju Lee <span class="coworker-count">2</span></button>
    <button class="coworker-btn" onclick="filterCoauthor('kook')">Woong Kook <span class="coworker-count">2</span></button>
    <button class="coworker-btn" onclick="filterCoauthor('gonzalez')">M. del Mar Gonzalez <span class="coworker-count">1</span></button>
    <button class="coworker-btn" onclick="filterCoauthor('takwon')">Takwon Kim <span class="coworker-count">1</span></button>
    <button class="coworker-btn" onclick="filterCoauthor('sanghoon')">Sanghoon Lee <span class="coworker-count">1</span></button>
    <button class="coworker-btn" onclick="filterCoauthor('kang')">Hyunsuk Kang <span class="coworker-count">1</span></button>
    <button class="coworker-btn" onclick="filterCoauthor('huang')">Jiuzhou Huang <span class="coworker-count">1</span></button>
  </div>
</div>

<script>
var activeFilter = null;

function filterCoauthor(id) {
  var items = document.querySelectorAll('.pub-item');
  var buttons = document.querySelectorAll('.coworker-btn');

  if (activeFilter === id) {
    activeFilter = null;
    items.forEach(function(el) { el.classList.remove('hidden'); });
    buttons.forEach(function(el) { el.classList.remove('active'); });
    return;
  }

  activeFilter = id;
  items.forEach(function(el) {
    var authors = el.getAttribute('data-authors');
    if (authors && authors.split(',').indexOf(id) !== -1) {
      el.classList.remove('hidden');
    } else {
      el.classList.add('hidden');
    }
  });

  buttons.forEach(function(el) {
    var onclick = el.getAttribute('onclick');
    if (onclick && onclick.indexOf("'" + id + "'") !== -1) {
      el.classList.add('active');
    } else {
      el.classList.remove('active');
    }
  });
}
</script>
