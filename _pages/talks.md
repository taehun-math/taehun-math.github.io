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

<!-- ============================================================ -->
<!--                      SEMINAR TALKS                           -->
<!-- ============================================================ -->
<div id="seminars" class="tk-section active">

<div class="tk-legend">
  <div class="tk-legend-item"><div class="tk-legend-dot" style="background:#378ADD;"></div> seminar</div>
  <div class="tk-legend-item"><div class="tk-legend-dot" style="background:#7F77DD;"></div> conference</div>
  <div class="tk-legend-item"><div class="tk-legend-dot" style="background:#1D9E75;"></div> workshop</div>
  <div class="tk-legend-item"><div class="tk-legend-dot" style="background:#EF9F27;"></div> school</div>
  <div class="tk-legend-item"><div class="tk-legend-dot" style="background:#D85A30;"></div> colloquium</div>
</div>

<div class="tk-tl">

  <!-- 2026 -->
  <div class="tk-year">
    <div class="tk-dot now"></div>
    <div class="tk-year-label" onclick="toggleYear(this)">2026 <span class="tk-count">(6)</span> <span class="tk-now-tag">recent</span> <span class="tk-toggle open">&#9654;</span></div>
    <div class="tk-list">
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue">Korea-China 2026 PDE Workshop, SNU</div><div class="tk-loc">Seoul, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue">Workshop on Nonlinear Partial Differential Equations, Harmonic Analysis, and Free Boundary Problems, KTH</div><div class="tk-loc">Stockholm, Sweden</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-conf">conference</span>
        <div><div class="tk-venue"><a href="https://aimsconference.org/conferences/2026/index.html">The 15th AIMS Conference on Dynamical Systems, Differential Equations and Applications</a></div>
<div class="tk-loc">Athens, Greece</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-colloq">colloquium</span>
        <div><div class="tk-venue">Colloquium, UNIST</div><div class="tk-loc">Ulsan, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-colloq">colloquium</span>
        <div><div class="tk-venue"><a href="https://math.sogang.ac.kr/front/cmsboardview.do?currentPage=1&searchField=ALL&searchValue=&searchLowItem=ALL&bbsConfigFK=1948&siteId=math&pkid=933773">Colloquium, Sogang University</a></div><div class="tk-loc">Seoul, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue">Hanyang University</div><div class="tk-loc">Seoul, Korea</div></div>
      </div>
    </div>
  </div>

  <!-- 2025 -->
  <div class="tk-year">
    <div class="tk-dot"></div>
    <div class="tk-year-label" onclick="toggleYear(this)">2025 <span class="tk-count">(12)</span> <span class="tk-toggle open">&#9654;</span></div>
    <div class="tk-list">
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue"><a href="https://sites.google.com/view/repp-seminar">Seminar on Regularity in Elliptic and Parabolic Problems (REPP)</a></div><div class="tk-loc">Online</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-conf">conference</span>
        <div><div class="tk-venue"><a href="https://ksiam.org/Conference/ConferenceView.asp?AC=0&CODE=CC20250901&CpPage=#CONF">2025 KSIAM Fall Meetings</a></div><div class="tk-loc">Gyeongju, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="https://sites.google.com/view/rims-viscosity2025/">Viscosity Solutions of Differential Equations and Related Topics</a></div><div class="tk-loc">RIMS, Kyoto University, Japan</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-colloq">colloquium</span>
        <div><div class="tk-venue">Sookmyung Women's University</div><div class="tk-loc">Seoul, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue"><a href="https://ncts.ntu.edu.tw/events_1_detail.php?nid=3000">NCTS Differential Geometry Seminar</a></div><div class="tk-loc">Online, Taiwan</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-conf">conference</span>
        <div><div class="tk-venue"><a href="https://www.kms.or.kr/conference/meeting/?period=90">2025 KMS Annual Meeting: Special Session-11</a></div><div class="tk-loc">ST Center, Seoul, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="https://math.ustc.edu.cn/2025/0605/c18653a687016/page.htm">2025 China-Korea Workshop on Partial Differential Equations</a></div><div class="tk-loc">Anhui, China</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-school">school</span>
        <div><div class="tk-venue"><a href="https://sites.google.com/view/2025-pde-summer/">2025 Summer School on Elliptic &amp; Parabolic PDEs</a></div><div class="tk-loc">Jeju, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue"><a href="http://newton.kias.re.kr/~appseminar/app2025.html">KIAS APP Seminar</a></div><div class="tk-loc">Seoul, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-conf">conference</span>
        <div><div class="tk-venue"><a href="https://ksiam.org/Conference/ConferenceView.asp?AC=0&CODE=CC20250301&CpPage=259#CONF">Recent Advances in Nonlinear PDEs I</a></div><div class="tk-loc">KSIAM, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="https://sites.google.com/hanyang.ac.kr/pdeswithoutscreens/home">Diving into PDEs without Screens</a></div><div class="tk-loc">Hanyang University, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-school">school</span>
        <div><div class="tk-venue"><a href="https://sites.google.com/view/pdeschool-2025/">The 11th Korea PDE Winter School at UNIST</a></div><div class="tk-loc">Ulsan, Korea</div></div>
      </div>
    </div>
  </div>

  <!-- 2024 -->
  <div class="tk-year">
    <div class="tk-dot"></div>
    <div class="tk-year-label" onclick="toggleYear(this)">2024 <span class="tk-count">(6)</span> <span class="tk-toggle">&#9654;</span></div>
    <div class="tk-list collapsed">
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue">CM2LA Seminar at POSTECH</div><div class="tk-loc">Pohang, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-conf">conference</span>
        <div><div class="tk-venue">2024 KMS Annual Meeting: Special Session-08</div><div class="tk-loc">Suwon, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-school">school</span>
        <div><div class="tk-venue"><a href="https://sites.google.com/view/summer-school-pde-2024/main">Summer School on Elliptic &amp; Parabolic PDEs</a></div><div class="tk-loc">Seoul, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue">PNU Geometry and Topology Seminar</div><div class="tk-loc">Pusan, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue">East Asia Workshop on Nonlinear Evolution Equations</div><div class="tk-loc">Tokyo, Japan</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue">Winter Workshop on Elliptic and Parabolic Problems and Related Topics</div><div class="tk-loc">Jeongseon, Korea</div></div>
      </div>
    </div>
  </div>

  <!-- 2023 -->
  <div class="tk-year">
    <div class="tk-dot"></div>
    <div class="tk-year-label" onclick="toggleYear(this)">2023 <span class="tk-count">(9)</span> <span class="tk-toggle">&#9654;</span></div>
    <div class="tk-list collapsed">
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue"><a href="https://www.math.uu.se/the-department/calendar/event/?eventId=84952">PDEA Seminar, Uppsala University</a></div><div class="tk-loc">Uppsala, Sweden</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue">UAM-ICMAT Seminar, Autonomous University of Madrid</div><div class="tk-loc">Madrid, Spain</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-conf">conference</span>
        <div><div class="tk-venue"><a href="https://www.kms.or.kr/conference/2023_fall/general/contents.html?period=85&idx=292">KMS Special Conference with 2022 Fields Medalists</a></div><div class="tk-loc">Seoul National University, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="http://events.kias.re.kr/h/YoungGeometersM/?pageNo=5233">Young Geometers Meeting</a></div><div class="tk-loc">KIAS, Seoul, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue"><a href="https://math.cau.ac.kr/notice/news.php?keyfield=&keyword=&page=1&board_table=seminar&work=view&No=79">Analysis and PDE Seminar, Chung-Ang University</a></div><div class="tk-loc">Seoul, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-conf">conference</span>
        <div><div class="tk-venue"><a href="https://www.kms.or.kr/conference/2023_spring/index.html?period=84">2023 KMS Annual Meeting: SS-16 &amp; SS-06</a></div><div class="tk-loc">Daejeon, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue"><a href="https://sites.google.com/view/minhyunkim/seminar">Seminar, Hanyang University</a></div><div class="tk-loc">Seoul, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-school">school</span>
        <div><div class="tk-venue"><a href="http://events.kias.re.kr/h/WSG23/">18th KIAS Geometry Winter School</a></div><div class="tk-loc">Jeongseon, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="https://sites.google.com/view/geometrybrl/workshops">Workshop on Geometric Analysis and Related Topics IV</a></div><div class="tk-loc">Jeongseon, Korea</div></div>
      </div>
    </div>
  </div>

  <!-- 2022 -->
  <div class="tk-year">
    <div class="tk-dot"></div>
    <div class="tk-year-label" onclick="toggleYear(this)">2022 <span class="tk-count">(8)</span> <span class="tk-toggle">&#9654;</span></div>
    <div class="tk-list collapsed">
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue"><a href="https://hkumath.hku.hk/~imr/event/CUHK_HKU_UNIST_Analysis_and_PDE/index.php">Analysis and PDE Seminar (CUHK, HKU, UNIST)</a></div><div class="tk-loc">Online</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="http://qsms.math.snu.ac.kr/board_axne29/2388">Rookies Workshop</a></div><div class="tk-loc">Yangpyeong, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue"><a href="https://www.maths.usyd.edu.au/u/Asia-Pacific-APDESeminar/Talks2022.html">Asia-Pacific Analysis and PDE Seminar</a></div><div class="tk-loc">Online</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="http://jinyeongpark.com/?cat=5">HY-PDE Workshop 2022</a></div><div class="tk-loc">Hanyang University, Seoul, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue">KIAS pseudo-New Member Seminar</div><div class="tk-loc">KIAS, Seoul, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue">KNU Seminar</div><div class="tk-loc">Daegu, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="https://sites.google.com/view/caupdeworkshop2022/">CAU Nonlinear PDE Center Workshop</a></div><div class="tk-loc">Online</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="https://math.yonsei.ac.kr/math/math/event_calendar.do?mode=view&articleNo=134262">PDE Workshop</a></div><div class="tk-loc">Busan, Korea</div></div>
      </div>
    </div>
  </div>

  <!-- 2020-2021 -->
  <div class="tk-year">
    <div class="tk-dot"></div>
    <div class="tk-year-label" onclick="toggleYear(this)">2020 – 2021 <span class="tk-count">(6)</span> <span class="tk-toggle">&#9654;</span></div>
    <div class="tk-list collapsed">
      <div class="tk-item">
        <span class="tk-badge b-conf">conference</span>
        <div><div class="tk-venue"><a href="https://www.kms.or.kr/meetings/fall2021/">2021 KMS Annual Meeting: Special Session-08</a></div><div class="tk-loc">Online</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="https://jinyeongpark.com/?p=224097">HY-PDE Workshop 2021</a></div><div class="tk-loc">Online</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="http://events.kias.re.kr/h/WSG21/">16th KIAS Workshop on Geometry</a></div><div class="tk-loc">Online</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-conf">conference</span>
        <div><div class="tk-venue"><a href="http://events.kias.re.kr/h/SeoulTokyo20/?pageNo=4301">2020 Seoul-Tokyo Conference: Partial Differential Equations</a></div><div class="tk-loc">Online</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue">2020 Partial Differential Equation Camp</div><div class="tk-loc">Jeju, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue">2020 Workshop on Elliptic and Parabolic PDEs</div><div class="tk-loc">Yangyang, Korea</div></div>
      </div>
    </div>
  </div>

  <!-- 2014-2017 -->
  <div class="tk-year">
    <div class="tk-dot"></div>
    <div class="tk-year-label" onclick="toggleYear(this)">2014 – 2017 <span class="tk-count">(4)</span> <span class="tk-toggle">&#9654;</span></div>
    <div class="tk-list collapsed">
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue">Seminar, Autonomous University of Madrid</div><div class="tk-loc">Madrid, Spain (2017)</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-workshop">workshop</span>
        <div><div class="tk-venue"><a href="http://www.math.snu.ac.kr/~byun/2016WORKSHOP/index.htm">2016 Workshop on Nonlinear Elliptic and Parabolic Equations</a></div><div class="tk-loc">Seoul National University, Korea</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-seminar">seminar</span>
        <div><div class="tk-venue">2015 Seminari D'EDP'S I Aplicacions, Polytechnic University of Catalonia</div><div class="tk-loc">Barcelona, Spain</div></div>
      </div>
      <div class="tk-item">
        <span class="tk-badge b-conf">conference</span>
        <div><div class="tk-venue"><a href="https://www.math.sci.hokudai.ac.jp/sympo/snu/2014/index_en.html">The 10th HU and SNU Symposium on Mathematics</a></div><div class="tk-loc">Hokkaido University, Japan (2014)</div></div>
      </div>
    </div>
  </div>

</div>
</div>

<!-- ============================================================ -->
<!--                     SERIES LECTURES                          -->
<!-- ============================================================ -->
<div id="series" class="tk-section">
<div class="tk-cards">
  <div class="tk-card">
    <span class="tk-card-badge b-series">series lecture</span>
    <div class="tk-card-title"><a href="http://events.kias.re.kr/h/WSG24/?pageNo=5344">19th KIAS Geometry Winter School</a></div>
    <div class="tk-card-sub">On Morse index of minimal surfaces I, II</div>
    <div class="tk-card-meta">2024 · Jeongseon, Korea</div>
  </div>
  <div class="tk-card">
    <span class="tk-card-badge b-series">series lecture</span>
    <div class="tk-card-title"><a href="https://www.dropbox.com/scl/fi/5r1f7oby8501m0ca3ywbf/2023_Pusan_ABP.png?rlkey=qvtz5mxaas118maxezhqqnafj&dl=0">2023 Summer School on Elliptic and Parabolic Equations</a></div>
    <div class="tk-card-sub">Alexandrov–Bakelman–Pucci estimate and applications to geometric inequalities I, II</div>
    <div class="tk-card-meta">2023 · Pusan, Korea</div>
  </div>
  <div class="tk-card">
    <span class="tk-card-badge b-series">series lecture</span>
    <div class="tk-card-title"><a href="http://events.kias.re.kr/h/PWSG22/?pageNo=4573">Geometric Flow Winter School</a></div>
    <div class="tk-card-sub">Asymptotic behavior of complete graphical curves under the curve shortening flow I, II, III</div>
    <div class="tk-card-meta">2022 · Online</div>
  </div>
  <div class="tk-card">
    <span class="tk-card-badge b-series">series lecture</span>
    <div class="tk-card-title">2022 Workshop on Elliptic and Parabolic PDEs</div>
    <div class="tk-card-sub">Minkowski-type problems I, II, III</div>
    <div class="tk-card-meta">2022 · Jeju, Korea</div>
  </div>
  <div class="tk-card">
    <span class="tk-card-badge b-series">series lecture</span>
    <div class="tk-card-title"><a href="https://sites.google.com/view/geometrybrl/home">Seminar, Submanifold Geometry Lab, Pusan National University</a></div>
    <div class="tk-card-sub">Free boundary problems in curvature flows I, II</div>
    <div class="tk-card-meta">2021 · Online</div>
  </div>
</div>
</div>

<!-- ============================================================ -->
<!--                  CONFERENCE ORGANIZATION                     -->
<!-- ============================================================ -->
<div id="org" class="tk-section">
<div class="tk-cards">
  <div class="tk-card">
    <span class="tk-card-badge b-org">organizer</span>
    <div class="tk-card-title"><a href="https://sites.google.com/view/2024-korean-japanese-workshop">Korean-Japanese Workshop on Elliptic and Parabolic Equations</a></div>
    <div class="tk-card-meta">November 15–16, 2024 · Seoul, Korea</div>
  </div>
  <div class="tk-card">
    <span class="tk-card-badge b-org">organizer</span>
    <div class="tk-card-title"><a href="https://sites.google.com/view/2023npde/home">2023 Workshop on Elliptic &amp; Parabolic PDEs and Related Topics</a></div>
    <div class="tk-card-meta">December 18–20, 2023 · Jeju, Korea</div>
  </div>
  <div class="tk-card">
    <span class="tk-card-badge b-org">organizer</span>
    <div class="tk-card-title"><a href="http://events.kias.re.kr/h/WNA21/?pageNo=4514">KIAS Workshop on Nonlinear Analysis</a></div>
    <div class="tk-card-meta">December 2–4, 2021 · Online</div>
  </div>
</div>
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
