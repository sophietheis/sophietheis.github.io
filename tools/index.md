---
title: Tools
nav:
  order: 3
  tooltip: Software, datasets, and more
---

# {% include icon.html icon="fa-solid fa-computer" %}Tools

{% include section.html %}

<style>
    * { box-sizing: border-box; margin: 0; padding: 0; }

  .tools-subtitle {
    color: #666;
    font-size: 0.92rem;
    margin-bottom: 44px;
    margin-top: 4px;
  }

  /* ── CARDS ── */
  .tool-cards {
    display: grid;
    grid-template-columns: 1fr;
    gap: 22px;
    margin-bottom: 44px;
  }
  .tool-cards .card {
    background: #fff;
    border-radius: 16px;
    padding: 22px 22px 18px;
    box-shadow: 0 2px 10px rgba(0,0,0,.07);
    border-top: 5px solid;
    display: flex;
    flex-direction: column;
    align-items: stretch;
    gap: 14px;
    width: auto;
    max-width: none;
    margin: 0;
  }
  .tool-cards .card-dissect { border-color: #f4a261; }
  .tool-cards .card-cellmet { border-color: #4477ce; }
  .tool-cards .card-tyssue  { border-color: #2a9d6f; }
  .card-header { display: flex; align-items: center; gap: 12px; }
  .card-header .icon { font-size: 1.8rem; }
  .card-header h2 { font-size: 1.1rem; font-weight: 800; margin: 0; }
  .badge { font-size: 0.7rem; padding: 2px 8px; border-radius: 20px; font-weight: 600; margin-top: 2px; display: inline-block; }
  .badge-dissect { background: #ffecd2; color: #7c3a00; }
  .badge-cellmet { background: #dde8ff; color: #112255; }
  .badge-tyssue  { background: #d8f5e8; color: #0a3d25; }
  .card p { font-size: 0.84rem; color: #444; line-height: 1.6; }
  .io-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .io-box { border-radius: 10px; padding: 10px 12px; font-size: 0.78rem; line-height: 1.5; }
  .io-box strong { display: block; font-size: 0.72rem; text-transform: uppercase; letter-spacing: .5px; margin-bottom: 4px; opacity: .7; }
  .io-in  { background: #f5f5f5; }
  .io-out { background: #f0f8ff; }
  .tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .tag { font-size: 0.7rem; padding: 3px 10px; border-radius: 20px; background: #eee; color: #444; font-weight: 500; }
  .pub-ref { font-size: 0.72rem; color: #888; border-top: 1px solid #eee; padding-top: 10px; line-height: 1.5; }
  .pub-ref a { color: #4477ce; text-decoration: none; }

</style>

<body>
<p class="tools-subtitle">
  Understanding how tissues bend, fold and rearrange during development requires bridging two worlds that rarely talk to each other: the 
  <strong>microscope</strong> and the <strong>mathematical model</strong>. These three open-source tools form a continuous pipeline that does exactly that — 
  starting from raw 3D fluorescence images of living tissues, extracting quantitative geometric and mechanical information from every cell, 
  and feeding those measurements into physics-based simulations to test and generate hypotheses about morphogenetic mechanisms.
  Together they make it possible to go from <em>seeing</em> a tissue deform to <em>understanding why</em> it deforms the way it does.
</p>
<!-- CARDS -->
<div class="tool-cards">

  <!-- DISSECT -->
  <div class="card card-dissect">
    <div class="card-header">
      <div class="icon">🔬</div>
      <div>
        <h2>DISSECT</h2>
        <div class="badge badge-dissect">Segmentation · Analysis</div>
      </div>
    </div>
    <p>Addresses the challenge of segmenting and analysing cells in <strong>highly curved or deformed 3D epithelia</strong>, where conventional tools fail.</p>
    <div class="io-grid">
      <div class="io-box io-in">
        <strong>Input</strong>
        Fluorescence microscopy (confocal / light-sheet) of the apical surface of 3D epithelial tissues
      </div>
      <div class="io-box io-out">
        <strong>Output</strong>
        Segmented cell meshes, fluorescence, shape metrics
      </div>
    </div>
    <div class="tags">
      <span class="tag">3D segmentation</span>
      <span class="tag">cell mechanics</span>
      <span class="tag">deformed epithelia</span>
    </div>
    <div class="pub-ref">
      Merle, Theis et al. <em>Developmental Cell</em> 58(20), 2023.
    </div>
  </div>

  <!-- CELLMET -->
  <div class="card card-cellmet">
    <div class="card-header">
      <div class="icon">📐</div>
      <div>
        <h2>CellMet</h2>
        <div class="badge badge-cellmet">Quantification · Topology</div>
      </div>
    </div>
    <p>A dedicated toolkit for computing <strong>3D shape and topological descriptors</strong> of cells packed within tissues. Goes beyond simple volume/area to capture neighbour relationships, curvature, and connectivity.</p>
    <div class="io-grid">
      <div class="io-box io-in">
        <strong>Input</strong>
        3D segmented cell meshes
      </div>
      <div class="io-box io-out">
        <strong>Output</strong>
        Shape metrics (volume, surface, aspect ratio), topology graphs, neighbour statistics
      </div>
    </div>
    <div class="tags">
      <span class="tag">shape metrics</span>
      <span class="tag">topology</span>
      <span class="tag">3D analysis</span>
      <span class="tag">confluent cells</span>
    </div>
    <div class="pub-ref">
      <strong>Theis</strong> et al. <em>PLOS Computational Biology</em> 21(7), 2025.
    </div>
  </div>

  <!-- TYSSUE -->
  <div class="card card-tyssue">
    <div class="card-header">
      <div class="icon">⚙️</div>
      <div>
        <h2>Tyssue</h2>
        <div class="badge badge-tyssue">Simulation · Library</div>
      </div>
    </div>
    <p>An open-source Python library for <strong>simulating epithelial tissue mechanics</strong>. Implements vertex models and energy-based frameworks to simulate cell rearrangements, deformations, and morphogenetic events — parameterisable from experimental measurements.</p>
    <div class="io-grid">
      <div class="io-box io-in">
        <strong>Input</strong>
        Cell geometry (vertex positions), mechanical parameters (tensions, elasticities)
      </div>
      <div class="io-box io-out">
        <strong>Output</strong>
        Simulated tissue dynamics, force maps, energy landscapes, deformation trajectories
      </div>
    </div>
    <div class="tags">
      <span class="tag">vertex model</span>
      <span class="tag">epithelial mechanics</span>
      <span class="tag">Python library</span>
      <span class="tag">morphogenesis</span>
    </div>
    <div class="pub-ref">
      <strong>Theis</strong>, Suzanne & Gay. <em>Journal of Open Source Software</em> 6(62), 2021.
    </div>
  </div>

</div>

</body>


