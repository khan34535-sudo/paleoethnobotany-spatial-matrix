<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>README · Mesoamerican 3D Aerial GIS Prototype</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Merriweather:wght@400;700;900&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#0b1711;
    --bg-elev:#11231A;
    --border:rgba(212,175,55,.25);
    --border-strong:rgba(212,175,55,.5);
    --gold:#D4AF37;
    --gold-bright:#F0D57E;
    --terracotta:#C85A32;
    --forest:#2E5A44;
    --text:#F4EFE6;
    --text-dim:rgba(244,239,230,.72);
    --text-mute:rgba(244,239,230,.5);
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth}
  body{
    font-family:'Inter',sans-serif;
    background:var(--bg);
    color:var(--text);
    line-height:1.65;
    font-size:15px;
    -webkit-font-smoothing:antialiased;
    position:relative;
    overflow-x:hidden;
  }
  body::before{
    content:'';
    position:fixed;inset:0;
    background-image:
      linear-gradient(rgba(212,175,55,.02) 1px,transparent 1px),
      linear-gradient(90deg,rgba(200,90,50,.02) 1px,transparent 1px);
    background-size:48px 48px;
    pointer-events:none;z-index:0;
  }
  .wrap{max-width:960px;margin:0 auto;padding:60px 24px 80px;position:relative;z-index:1}

  /* ============ HERO ============ */
  .hero{
    text-align:center;
    padding-bottom:44px;
    border-bottom:1px solid var(--border);
    margin-bottom:48px;
  }
  .hero .badge{
    display:inline-flex;align-items:center;gap:8px;
    padding:6px 14px;
    background:rgba(212,175,55,.12);
    border:1px solid var(--border-strong);
    border-radius:999px;
    color:var(--gold);
    font-size:11px;
    letter-spacing:.15em;
    text-transform:uppercase;
    font-weight:700;
    margin-bottom:20px;
  }
  .hero .badge::before{
    content:'';
    width:6px;height:6px;border-radius:50%;
    background:var(--gold);
    box-shadow:0 0 10px var(--gold);
  }
  h1{
    font-family:'Merriweather',serif;
    font-size:clamp(28px,4vw,40px);
    font-weight:900;
    line-height:1.2;
    letter-spacing:-.01em;
    margin-bottom:16px;
    color:#fff;
  }
  h1 .accent{color:var(--gold)}
  .hero .tagline{
    font-size:16px;
    color:var(--text-dim);
    max-width:640px;
    margin:0 auto 24px;
  }
  .hero .author{
    display:inline-flex;align-items:center;gap:10px;
    padding:10px 18px;
    background:var(--bg-elev);
    border:1px solid var(--border);
    border-radius:12px;
    font-size:13px;
  }
  .hero .author .name{font-weight:600;color:#fff}
  .hero .author .role{color:var(--text-dim);font-size:12px}

  /* ============ SECTIONS ============ */
  section{margin-bottom:56px}
  h2{
    font-family:'Merriweather',serif;
    font-size:22px;
    font-weight:700;
    color:var(--gold);
    margin-bottom:16px;
    padding-bottom:10px;
    border-bottom:1px solid var(--border);
    display:flex;align-items:center;gap:12px;
  }
  h2 .num{
    font-family:'JetBrains Mono',monospace;
    font-size:12px;
    color:var(--terracotta);
    background:rgba(200,90,50,.15);
    padding:3px 10px;
    border-radius:6px;
    border:1px solid rgba(200,90,50,.3);
    letter-spacing:.08em;
  }
  h3{
    font-family:'Merriweather',serif;
    font-size:16px;
    font-weight:700;
    color:var(--text);
    margin:20px 0 10px;
  }
  p{margin-bottom:14px;color:var(--text-dim)}
  p strong{color:var(--text);font-weight:600}
  a{color:var(--gold-bright);text-decoration:none;border-bottom:1px dotted rgba(212,175,55,.4)}
  a:hover{color:var(--gold);border-bottom-color:var(--gold)}

  /* ============ CALLOUTS ============ */
  .callout{
    background:var(--bg-elev);
    border:1px solid var(--border);
    border-left:3px solid var(--terracotta);
    border-radius:10px;
    padding:20px 24px;
    margin:20px 0;
  }
  .callout.gold{border-left-color:var(--gold)}
  .callout.gold strong{color:var(--gold)}
  .callout.warn{
    border-left-color:#e0a020;
    background:rgba(224,160,32,.06);
  }
  .callout.warn strong{color:#f0c674}
  .callout .title{
    font-family:'Merriweather',serif;
    font-weight:700;
    font-size:14px;
    color:var(--gold);
    margin-bottom:8px;
    display:flex;align-items:center;gap:8px;
  }
  .callout p{color:var(--text);margin-bottom:8px}
  .callout p:last-child{margin-bottom:0}

  /* ============ GRID ============ */
  .grid{display:grid;gap:16px;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));margin:20px 0}
  .card{
    background:var(--bg-elev);
    border:1px solid var(--border);
    border-radius:12px;
    padding:20px;
    transition:all .25s ease;
  }
  .card:hover{
    border-color:var(--border-strong);
    transform:translateY(-2px);
    box-shadow:0 8px 24px rgba(0,0,0,.4);
  }
  .card .icon{
    width:36px;height:36px;
    border-radius:9px;
    background:linear-gradient(135deg,var(--terracotta),var(--gold));
    display:flex;align-items:center;justify-content:center;
    color:#0b1711;
    font-size:16px;
    margin-bottom:14px;
    font-weight:700;
  }
  .card h4{
    font-family:'Merriweather',serif;
    font-size:15px;
    font-weight:700;
    color:#fff;
    margin-bottom:8px;
  }
  .card p{font-size:13.5px;color:var(--text-dim);margin:0;line-height:1.6}

  /* ============ FEATURE LIST ============ */
  ul.features{list-style:none;margin:16px 0}
  ul.features li{
    padding:10px 0 10px 32px;
    position:relative;
    color:var(--text-dim);
    border-bottom:1px solid rgba(212,175,55,.08);
    font-size:14px;
  }
  ul.features li:last-child{border-bottom:none}
  ul.features li::before{
    content:'◆';
    position:absolute;left:8px;top:9px;
    color:var(--gold);
    font-size:10px;
  }
  ul.features li strong{color:var(--text)}

  /* ============ STATUS ROWS ============ */
  .placeholder-row{
    display:flex;gap:14px;
    padding:14px 0;
    border-bottom:1px solid rgba(212,175,55,.08);
    font-size:13.5px;
  }
  .placeholder-row:last-child{border-bottom:none}
  .placeholder-row .pill{
    flex-shrink:0;
    font-family:'JetBrains Mono',monospace;
    font-size:10px;
    padding:3px 10px;
    border-radius:6px;
    letter-spacing:.08em;
    height:fit-content;
    margin-top:2px;
  }
  .pill.real{background:rgba(46,90,68,.6);color:#7ee3a8;border:1px solid rgba(126,227,168,.3)}
  .pill.placeholder{background:rgba(200,90,50,.15);color:#ff9c72;border:1px solid rgba(255,156,114,.3)}
  .pill.partial{background:rgba(212,175,55,.15);color:var(--gold);border:1px solid rgba(212,175,55,.35)}
  .placeholder-row .desc{color:var(--text-dim)}
  .placeholder-row .desc strong{color:var(--text);display:block;margin-bottom:2px}

  /* ============ CODE ============ */
  pre, code{
    font-family:'JetBrains Mono',monospace;
    font-size:12.5px;
  }
  code{
    background:rgba(212,175,55,.1);
    padding:2px 8px;
    border-radius:5px;
    color:var(--gold-bright);
    border:1px solid rgba(212,175,55,.18);
  }
  pre{
    background:#080f0c;
    border:1px solid var(--border);
    border-radius:10px;
    padding:18px 20px;
    overflow-x:auto;
    margin:16px 0;
    color:var(--text-dim);
    line-height:1.6;
  }
  pre code{background:none;padding:0;border:none;color:inherit}

  /* ============ TABLE ============ */
  table{
    width:100%;
    border-collapse:collapse;
    margin:16px 0;
    font-size:13.5px;
    background:var(--bg-elev);
    border:1px solid var(--border);
    border-radius:10px;
    overflow:hidden;
  }
  th{
    background:rgba(212,175,55,.08);
    color:var(--gold);
    text-align:left;
    padding:12px 16px;
    font-weight:600;
    font-size:11.5px;
    letter-spacing:.08em;
    text-transform:uppercase;
    border-bottom:1px solid var(--border);
  }
  td{
    padding:12px 16px;
    border-bottom:1px solid rgba(212,175,55,.08);
    color:var(--text-dim);
  }
  tr:last-child td{border-bottom:none}

  /* ============ LAND ACK ============ */
  .land-ack{
    background:linear-gradient(135deg,rgba(46,90,68,.35),rgba(200,90,50,.15));
    border:1px solid rgba(212,175,55,.3);
    border-radius:12px;
    padding:24px 28px;
    margin:24px 0;
    font-size:14px;
    color:var(--text);
    line-height:1.7;
  }
  .land-ack .title{
    font-family:'Merriweather',serif;
    font-size:13px;
    font-weight:700;
    color:var(--gold);
    text-transform:uppercase;
    letter-spacing:.12em;
    margin-bottom:10px;
  }

  /* ============ LICENSE BLOCK ============ */
  .license-block{
    background:linear-gradient(135deg,rgba(17,35,26,.9),rgba(8,15,12,.95));
    border:1px solid var(--border-strong);
    border-radius:14px;
    padding:32px 36px;
    margin-top:24px;
    text-align:center;
    position:relative;
    overflow:hidden;
  }
  .license-block::before{
    content:'';
    position:absolute;
    top:0;left:0;right:0;
    height:3px;
    background:linear-gradient(90deg,var(--terracotta),var(--gold),var(--forest));
  }
  .license-block .copyright{
    font-family:'JetBrains Mono',monospace;
    font-size:11px;
    letter-spacing:.2em;
    color:var(--gold);
    text-transform:uppercase;
    margin-bottom:14px;
  }
  .license-block h3{
    font-family:'Merriweather',serif;
    font-size:22px;
    font-weight:900;
    color:#fff;
    margin:0 0 16px;
    letter-spacing:.02em;
  }
  .license-block p{
    color:var(--text-dim);
    font-size:14px;
    max-width:640px;
    margin:0 auto 12px;
    line-height:1.7;
  }
  .license-block p:last-child{margin-bottom:0}
  .license-block .seal{
    display:inline-block;
    margin-top:20px;
    padding:8px 18px;
    border:1px solid var(--border-strong);
    border-radius:999px;
    font-family:'JetBrains Mono',monospace;
    font-size:10px;
    letter-spacing:.2em;
    color:var(--gold);
    text-transform:uppercase;
  }

  /* ============ FOOTER ============ */
  footer{
    margin-top:60px;
    padding-top:32px;
    border-top:1px solid var(--border);
    text-align:center;
    font-size:12.5px;
    color:var(--text-mute);
  }
  footer .signature{
    font-family:'Merriweather',serif;
    font-size:14px;
    color:var(--text-dim);
    margin-bottom:12px;
  }
  footer .links{
    display:flex;gap:24px;justify-content:center;
    margin-top:16px;flex-wrap:wrap;
  }
  footer .links a{
    border:none;
    font-size:12px;
    letter-spacing:.05em;
    text-transform:uppercase;
    color:var(--text-mute);
  }
  footer .links a:hover{color:var(--gold)}

  /* ============ RESPONSIVE ============ */
  @media(max-width:640px){
    .wrap{padding:40px 18px 60px}
    .license-block{padding:24px 20px}
    h1{font-size:26px}
    h2{font-size:19px}
  }
</style>
</head>
<body>
<div class="wrap">

  <!-- ==================== HERO ==================== -->
  <div class="hero">
    <span class="badge">Prototype · Demonstrator Only</span>
    <h1>Mesoamerican <span class="accent">3D Aerial GIS</span><br>& Paleoethnobotany Matrix</h1>
    <p class="tagline">
      An experimental interface exploring how archaeological, paleoethnobotanical, and bioarchaeological data might be presented interactively — through satellite terrain, 3D specimen models, and multi-proxy narratives.
    </p>
    <div class="author">
      <div>
        <div class="name">Asia Khan, Hon. BA (McMaster University)</div>
        <div class="role">Behavioral UX Researcher &amp; Design Anthropologist</div>
      </div>
    </div>
  </div>

  <!-- ==================== 01 DISCLAIMER ==================== -->
  <section>
    <h2><span class="num">01</span> Disclaimer &amp; Scope</h2>

    <div class="callout warn">
      <div class="title">⚠ Prototype — Not for Research Citation</div>
      <p>This is a <strong>design prototype and demonstrator</strong>. It is intended to show <em>how</em> archaeological information could be presented, not to serve as a primary research source.</p>
      <p>While site names, publication citations, and archaeological concepts reference real academic literature, the specific pairings, spatial coordinates, artifact descriptions, and numerical indices shown in the interface are <strong>illustrative examples</strong> — not verified research outputs.</p>
      <p><strong>Do not cite this prototype in academic work.</strong> Always consult the original publications listed in the APA references.</p>
    </div>

    <div class="callout gold">
      <div class="title">◆ Purpose of This Prototype</div>
      <p>To explore <strong>alternative ways of presenting archaeological knowledge</strong> — moving beyond static figures and PDFs toward spatial, tactile, and multi-sensory interfaces that connect artifacts, contexts, and interpretations in one view.</p>
    </div>
  </section>

  <!-- ==================== 02 WHAT THIS DEMONSTRATES ==================== -->
  <section>
    <h2><span class="num">02</span> What This Prototype Demonstrates</h2>

    <div class="grid">
      <div class="card">
        <div class="icon">◈</div>
        <h4>Spatial Context</h4>
        <p>Real satellite imagery with 3D terrain, hosting archaeological sites as clickable spatial anchors rather than map pins in a list.</p>
      </div>
      <div class="card">
        <div class="icon">◆</div>
        <h4>3D Specimen Models</h4>
        <p>Procedural Three.js models of starch grains, phytoliths, cacao pods, and bioarchaeological specimens — replacing static photographs with rotatable geometry.</p>
      </div>
      <div class="card">
        <div class="icon">◉</div>
        <h4>Multi-Proxy Integration</h4>
        <p>Placing macroremains, microremains, bioarchaeology, ritual objects, and climate archives side-by-side in a single navigable interface.</p>
      </div>
      <div class="card">
        <div class="icon">◇</div>
        <h4>Resilience Narratives</h4>
        <p>Simulating how communities responded to climate and colonial pressures — turning static data into explorable scenarios.</p>
      </div>
      <div class="card">
        <div class="icon">✧</div>
        <h4>Readable Citations</h4>
        <p>Every panel surfaces its own APA 7th reference, keeping academic provenance visible in the interface itself.</p>
      </div>
      <div class="card">
        <div class="icon">◆</div>
        <h4>Accessible Theming</h4>
        <p>Multiple theme modes (Neural Cyan, Amber Parchment, Midnight Indigo, Obsidian) — supporting different viewing conditions and readability needs.</p>
      </div>
    </div>
  </section>

  <!-- ==================== 03 REAL VS PLACEHOLDER ==================== -->
  <section>
    <h2><span class="num">03</span> What's Real vs. Placeholder</h2>

    <p>Transparency about which parts of this prototype reference verified information and which are illustrative:</p>

    <div style="background:var(--bg-elev);border:1px solid var(--border);border-radius:12px;padding:8px 20px;margin-top:16px">

      <div class="placeholder-row">
        <span class="pill real">REAL</span>
        <div class="desc">
          <strong>Site names &amp; regional contexts</strong>
          La Consentida, Cerro Palenque, Los Naranjos, Currusté — these are real archaeological sites with published literature.
        </div>
      </div>

      <div class="placeholder-row">
        <span class="pill real">REAL</span>
        <div class="desc">
          <strong>APA 7th citations</strong>
          All references point to actual peer-reviewed publications (Bérubé et al. 2019; Morell-Hart et al. 2014; etc.).
        </div>
      </div>

      <div class="placeholder-row">
        <span class="pill real">REAL</span>
        <div class="desc">
          <strong>Archaeological concepts</strong>
          Starch grain analysis, phytolith extraction, dental calculus, coprolite analysis — these are established methodologies.
        </div>
      </div>

      <div class="placeholder-row">
        <span class="pill partial">PARTIAL</span>
        <div class="desc">
          <strong>Site coordinates</strong>
          Latitude/longitude are approximate regional centroids — not precision excavation coordinates.
        </div>
      </div>

      <div class="placeholder-row">
        <span class="pill placeholder">PLACEHOLDER</span>
        <div class="desc">
          <strong>All 3D specimen models</strong>
          Procedurally generated in Three.js. They suggest <em>shape and structure</em>, not actual specimen geometry.
        </div>
      </div>

      <div class="placeholder-row">
        <span class="pill placeholder">PLACEHOLDER</span>
        <div class="desc">
          <strong>Artifact images &amp; diagrams</strong>
          All visual representations of artifacts, glyphs, and specimens are abstract placeholders.
        </div>
      </div>

      <div class="placeholder-row">
        <span class="pill placeholder">PLACEHOLDER</span>
        <div class="desc">
          <strong>Numerical indices (Resilience scores)</strong>
          Percentage values shown in the Resilience tab are illustrative — not derived from any published dataset.
        </div>
      </div>

      <div class="placeholder-row">
        <span class="pill placeholder">PLACEHOLDER</span>
        <div class="desc">
          <strong>Site-level descriptive text</strong>
          Context narratives are synthesised from public literature to demonstrate the UI, not quoted directly from publications.
        </div>
      </div>

    </div>
  </section>

  <!-- ==================== 04 AUDIENCE ==================== -->
  <section>
    <h2><span class="num">04</span> Intended Audience</h2>

    <ul class="features">
      <li><strong>Design researchers</strong> exploring non-traditional interfaces for scholarly data</li>
      <li><strong>Archaeologists &amp; paleoethnobotanists</strong> curious about spatial and interactive presentation formats</li>
      <li><strong>Educators</strong> looking for teaching aids that bridge fieldwork and public understanding</li>
      <li><strong>Museum &amp; heritage professionals</strong> prototyping digital exhibit components</li>
      <li><strong>Students</strong> in archaeology, anthropology, or HCI interested in data visualisation approaches</li>
    </ul>

    <div class="callout">
      <p><strong>This prototype is not a substitute for fieldwork, laboratory analysis, or peer-reviewed publication.</strong> Its value is in the <em>interface thinking</em>, not the data accuracy.</p>
    </div>
  </section>

  <!-- ==================== 05 TECH STACK ==================== -->
  <section>
    <h2><span class="num">05</span> Technology &amp; Dependencies</h2>

    <table>
      <thead>
        <tr><th>Layer</th><th>Library</th><th>Purpose</th></tr>
      </thead>
      <tbody>
        <tr><td>Map engine</td><td>MapLibre GL JS 3.6</td><td>Satellite imagery, terrain 3D, flyover modes</td></tr>
        <tr><td>Imagery</td><td>Esri World Imagery</td><td>Free public satellite tiles (with attribution)</td></tr>
        <tr><td>Terrain</td><td>AWS Terrain DEM</td><td>Elevation data (Terrarium encoding)</td></tr>
        <tr><td>3D rendering</td><td>Three.js r128</td><td>Procedural 3D models of artifacts &amp; specimens</td></tr>
        <tr><td>Styling</td><td>Tailwind CSS (CDN)</td><td>Utility-first responsive layout</td></tr>
        <tr><td>Typography</td><td>Google Fonts</td><td>Merriweather (headings), Inter (body), JetBrains Mono (code)</td></tr>
        <tr><td>Icons</td><td>Font Awesome 6.4</td><td>UI iconography</td></tr>
      </tbody>
    </table>

    <p style="margin-top:16px"><strong>No build step required.</strong> Open the HTML file directly in a modern browser, or serve via any static host (GitHub Pages, Netlify, Vercel, Cloudflare Pages).</p>
  </section>

  <!-- ==================== 06 LIMITATIONS ==================== -->
  <section>
    <h2><span class="num">06</span> Known Limitations</h2>

    <ul class="features">
      <li><strong>Approximate coordinates.</strong> Site markers land near but not on actual excavation locations.</li>
      <li><strong>Fictional specimen geometries.</strong> 3D models are illustrative — not scanned real specimens.</li>
      <li><strong>Synthesised descriptive text.</strong> Context narratives demonstrate UI, not verbatim research findings.</li>
      <li><strong>Resilience indices are demo values.</strong> Percentages do not derive from a published dataset.</li>
      <li><strong>Geolocation disabled on <code>file://</code>.</strong> The "Find Me" feature requires a local server or HTTPS hosting.</li>
      <li><strong>Mobile-first layout pending.</strong> Optimised for desktop and tablet viewports.</li>
      <li><strong>No accessibility audit yet.</strong> Colour contrast, keyboard navigation, and screen reader support need formal testing.</li>
    </ul>
  </section>

  <!-- ==================== 07 DESIGN PRINCIPLES ==================== -->
  <section>
    <h2><span class="num">07</span> Design Principles</h2>

    <div class="grid">
      <div class="card">
        <div class="icon">1</div>
        <h4>Provenance in the Interface</h4>
        <p>Every claim surfaces its citation. Users never lose sight of <em>where</em> information comes from.</p>
      </div>
      <div class="card">
        <div class="icon">2</div>
        <h4>Spatial over Sequential</h4>
        <p>Information is navigated by place, not by list. Clicking a landscape reveals its narrative.</p>
      </div>
      <div class="card">
        <div class="icon">3</div>
        <h4>Layered Multi-Proxy</h4>
        <p>Microremains, macroremains, bioarchaeology, ritual, and climate coexist — respecting how archaeologists actually work.</p>
      </div>
      <div class="card">
        <div class="icon">4</div>
        <h4>Honest About Uncertainty</h4>
        <p>Prototype status is stated visibly, not buried in a footer.</p>
      </div>
    </div>
  </section>

  <!-- ==================== 08 ETHICS ==================== -->
  <section>
    <h2><span class="num">08</span> Ethics &amp; Indigenous Heritage</h2>

    <div class="land-ack">
      <div class="title">Land Acknowledgment</div>
      <p>
        The sites referenced in this prototype are located on the ancestral and unceded lands of the Zapotec, Mixtec, Maya, and Lenca peoples, among others. These living communities have stewarded these landscapes and their botanical knowledge for millennia.
      </p>
      <p style="margin-top:10px">
        Any digital presentation of this heritage must be done with <strong>respect, attribution, and consultation</strong> — and preferably in partnership with descendant communities. This prototype is a technical demonstration only; it is <em>not</em> a definitive interpretation and does not claim authority over cultural narratives.
      </p>
    </div>

    <p><strong>Researchers and institutions</strong> wanting to build on this work should:</p>
    <ul class="features">
      <li>Consult source publications and their original authors</li>
      <li>Seek permissions from descendant communities for any cultural depictions</li>
      <li>Follow the CARE Principles for Indigenous Data Governance</li>
      <li>Consider FAIR principles for data sharing where appropriate</li>
      <li>Credit contributors — archaeologists, paleoethnobotanists, illustrators, and local collaborators</li>
    </ul>
  </section>

  <!-- ==================== 09 ROADMAP ==================== -->
  <section>
    <h2><span class="num">09</span> Possible Directions</h2>

    <p>If this prototype were developed further, natural next steps would include:</p>

    <ul class="features">
      <li>Replace placeholder 3D models with <strong>actual scanned specimens</strong> from reference collections</li>
      <li>Link each site to its <strong>published datasets</strong> (tDAR, Open Context, museum catalogs)</li>
      <li>Add a <strong>stratigraphic section viewer</strong> alongside the map</li>
      <li>Integrate <strong>real climate proxy data</strong> (stalagmite δ¹⁸O, sediment cores) as time-series</li>
      <li>Build a <strong>public-facing educational mode</strong> with simplified language and audio narration</li>
      <li>Conduct a <strong>formal accessibility audit</strong> (WCAG 2.1 AA)</li>
      <li>Partner with descendant communities for <strong>co-designed narratives</strong></li>
    </ul>
  </section>

  <!-- ==================== 10 USAGE ==================== -->
  <section>
    <h2><span class="num">10</span> Running Locally</h2>

    <p>Some browser features (geolocation, certain tile servers) require a proper HTTP origin. Run a local server:</p>

    <pre><code># Python 3 (built-in)
python3 -m http.server 8000

# or Node.js
npx serve -p 8000</code></pre>

    <p>Then open <code>http://localhost:8000/mesoamerican-lab.html</code> in your browser.</p>

    <p><strong>Alternatively, deploy free</strong> via GitHub Pages, Netlify Drop, Vercel, or Cloudflare Pages — all support static HTML.</p>
  </section>

  <!-- ==================== 11 CREDITS ==================== -->
  <section>
    <h2><span class="num">11</span> Credits &amp; Attribution</h2>

    <p><strong>Prototype designed and built by</strong><br>
    Asia Khan, Hon. BA (McMaster University)<br>
    Behavioral UX Researcher &amp; Design Anthropologist</p>

    <p style="margin-top:16px"><strong>Inspired by the work of</strong><br>
    Dr. Shanti Morell-Hart (McMaster University) — Social Paleoethnobotany Lab</p>

    <p style="margin-top:16px"><strong>Imagery &amp; data providers</strong><br>
    Esri World Imagery · AWS Terrain Tiles · MapLibre GL · OpenStreetMap contributors</p>

    <div class="callout gold" style="margin-top:24px">
      <div class="title">◆ A Note on the Prototype Philosophy</div>
      <p>This is not a finished product, a research database, or a public archaeology resource. It is an <strong>exploration</strong> — a sketch of what interactive scholarly interfaces could feel like when they prioritise context, curiosity, and transparency over certainty.</p>
      <p>Feedback, critiques, and collaborations are welcome.</p>
    </div>
  </section>

  <!-- ==================== 12 LICENSE ==================== -->
  <section>
    <h2><span class="num">12</span> License</h2>

    <div class="license-block">
      <div class="copyright">© 2026 Asia Khan · All Rights Reserved</div>
      <h3>All Rights Reserved</h3>
      <p>
        This prototype, including its source code, interface design, written content, and procedural 3D models, is the intellectual property of the author. No part of this work may be reproduced, distributed, modified, or transmitted in any form or by any means without prior written permission from the author.
      </p>
      <p>
        The prototype is provided <strong>"as is"</strong> for demonstration and educational viewing purposes only, without warranty of any kind — express or implied — including but not limited to the warranties of merchantability, fitness for a particular purpose, and non-infringement.
      </p>
      <p>
        In no event shall the author be liable for any claim, damages, or other liability arising from, out of, or in connection with the prototype or its use.
      </p>
      <p style="margin-top:16px;font-size:13px;color:var(--text-mute)">
        <em>Third-party libraries (MapLibre GL, Three.js, Tailwind CSS, Google Fonts, Font Awesome, Esri imagery, AWS terrain tiles) are used under their respective licenses and remain the property of their original creators.</em>
      </p>
      <span class="seal">◆ © All Rights Reserved ◆</span>
    </div>
  </section>

  <!-- ==================== FOOTER ==================== -->
  <footer>
    <div class="signature">
      ◈ Prototype Sample · Asia Khan, Hon. BA (McMaster University)
    </div>
    <p style="font-size:12px;color:var(--text-mute);max-width:600px;margin:0 auto">
      All information presented is for demonstration purposes only.<br>
      Do not cite without consulting original publications.
    </p>
    <div class="links">
      <a href="#">GitHub</a>
      <a href="#">Prototype</a>
      <a href="#">Contact</a>
      <a href="#">Morell-Hart Lab</a>
    </div>
  </footer>

</div>
</body>
</html>
