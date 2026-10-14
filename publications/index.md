---
title: Publications
nav:
  order: 1
  tooltip: Published works
---

# {% include icon.html icon="fa-solid fa-microscope" %}Publications

{% include section.html %}

<style>
  :root {
    --pub-bio:   #B4E4D6;
    --pub-tools: #FFCA88;
    --pub-phys:  #f89c74;
  
  }
/*  style="text-align:center;" */
  /* Legend */
  .legend {display: flex; flex-wrap: wrap; gap: .75rem; margin-bottom: 2rem; }
  .legend-item { display: flex; align-items: center; gap: .4rem; font-size: .85rem; font-weight: 600; }
  .dot { width: 12px; height: 12px; border-radius: 50%; flex-shrink: 0; }

  /* Thematic grid */
  .theme-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1rem; margin-bottom: 2.5rem; }
  .theme-card { background: var(--background); border-radius: 10px; padding: 1.1rem 1.2rem;
    box-shadow: 0 1px 6px #0001; border-top: 5px solid; }
  .theme-card h4 { font-size: .95rem; font-weight: 700; margin: 0 0 .5rem; }
  .theme-card ul { list-style: none; padding: 0; margin: 0; }
  .theme-card ul li { font-size: .82rem; color: var(--dark-gray); padding: .2rem 0;
    border-bottom: 1px solid #f0f0f0; }
  .theme-card ul li:last-child { border-bottom: none; }
  .theme-card.bio   { border-color: var(--pub-bio); }
  .theme-card.tools { border-color: var(--pub-tools); }
  .theme-card.phys  { border-color: var(--pub-phys); }
  .theme-card.dev   { border-color: var(--pub-dev); }

  /* Timeline */
  .timeline { position: relative; padding-left: 56px; margin-bottom: 3rem; }
  .timeline::before { content: ''; position: absolute; left: 22px; top: 0; bottom: 0;
    width: 3px; background: #e0e0ef; border-radius: 2px; }

  .entry { position: relative; margin-bottom: 1.5rem; }
  .year-bubble { position: absolute; left: -56px; width: 44px; height: 44px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: .72rem; font-weight: 700; color: #fff; background: #bdbdbd; }
  .t-card { background: var(--background); border-radius: 10px; padding: 1rem 1.2rem;
    box-shadow: 0 1px 6px #0001; border-left: 4px solid; }
  .t-card h3 { font-size: .95rem; font-weight: 700; margin: 0 0 .25rem; line-height: 1.35; }
  .t-card h3 a { color: inherit; text-decoration: none; }
  .t-card .meta { font-size: .8rem; color: var(--dark-gray); margin-bottom: .35rem; }
  .t-card .badge { display: inline-block; font-size: .72rem; font-weight: 600;
    padding: .15rem .55rem; border-radius: 20px; color: #fff; }
  .t-card .authors { font-size: .78rem; color: var(--dark-gray); margin-top: .4rem; }
  .me { font-weight: 700; color: var(--text); }

  .entry.bio   .badge { background: var(--pub-bio); }
  .entry.bio   .t-card { border-color: var(--pub-bio); }
  .entry.tools .badge { background: var(--pub-tools); }
  .entry.tools .t-card { border-color: var(--pub-tools); }
  .entry.phys  .badge { background: var(--pub-phys); }
  .entry.phys  .t-card { border-color: var(--pub-phys); }
</style>
<ul></ul>
<div class="legend" >
  <div class="legend-item"><div class="dot" style="background:var(--pub-bio)"></div> Developmental biology</div>
  <div class="legend-item"><div class="dot" style="background:var(--pub-tools)"></div> Computational tools </div>
  <div class="legend-item"><div class="dot" style="background:var(--pub-phys)"></div> Theory &amp; imaging </div>
</div>

<div class="theme-grid">

  <div class="theme-card bio">
    <h4 style="text-align:center;">🔬 Developmental biology</h4>
    <ul>
      <li>Boundary constraints &amp; patterning (2026)</li>
      <li>Apoptosis in neural tube bending (2022)</li>
      <li>Arp2/3 morphogenetic robustness (2021)</li>
      <li>EMT mechanics in Drosophila (2019)</li>
    </ul>
  </div>

  <div class="theme-card tools">
    <h4 style="text-align:center;">🛠 Computational tools</h4>
    <ul>
      <li>CellMet — 3D shape metrics (2025)</li>
      <li>DISSECT — 3D segmentation (2023)</li>
      <li>Tyssue — epithelium simulation (2021)</li>
    </ul>
  </div>

  <div class="theme-card phys">
    <h4 style="text-align:center;">📐 Theory and imaging</h4>
    <ul>
      <li>Fluorophore optimisation in Drosophila (2026)</li>
      <li>Stress anisotropy in 3D curved tissue (2026)</li>
      <li>Curvature-driven cell rearrangements (2023)</li>
    </ul>
  </div>

</div>

{% include section.html %}
## Highlighted

{% assign highlighted = site.data.citations | where: "id", "doi:10.1371/journal.pcbi.1013260" %}
{% for d in highlighted %}{% include pub-card.html d=d %}{% endfor %}

{% include section.html %}

## Preprint
{% assign preprints = site.data.citations | where_exp: "d", "d.preprint == true" | sort: "date" | reverse %}
{% for d in preprints %}{% include pub-card.html d=d %}{% endfor %}

{% include section.html %}


## All

{% assign pubs = site.data.citations | where_exp: "d", "d.preprint != true" | sort: "date" | reverse %}
<div class="timeline">
{% assign prev_year = "" %}
{% for d in pubs %}
  {% assign year = d.date | date: "%Y" %}
  {% if year != prev_year %}
    {% include pub-card.html d=d year=year %}
    {% assign prev_year = year %}
  {% else %}
    {% include pub-card.html d=d %}
  {% endif %}
{% endfor %}
</div>
