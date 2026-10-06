# Mesoamerican 3D Aerial GIS · Prototype

**⚠ Prototype Sample · Demonstrator Only · Not for Research Citation**

An experimental interface exploring how archaeological, paleoethnobotanical, and bioarchaeological data might be presented interactively — through satellite terrain, 3D specimen models, and multi-proxy narratives.

**Asia Khan, Hon. BA (McMaster University)**  
Behavioral UX Researcher & Design Anthropologist

---

## 🔗 Live Prototype

**[→ View the interactive prototype](https://khan34535-sudo.github.io/paleoethnobotany-spatial-matrix/)**

*(If the link doesn't work, enable GitHub Pages in Settings → Pages → main branch → / (root))*

---

## ⚠ Disclaimer

This is a **design prototype and demonstrator**. It is intended to show *how* archaeological information *could* be presented, not to serve as a primary research source.

- Site names and APA citations point to **real literature**
- Coordinates, artifact descriptions, and numerical indices are **illustrative examples**
- **All 3D models and artifact images are placeholders**
- **Do not cite this prototype in academic work** — consult original publications

## What This Demonstrates

- **Spatial context** — Real satellite imagery with 3D terrain, hosting sites as spatial anchors
- **3D specimen models** — Procedural Three.js models of starch grains, phytoliths, cacao, and bioarchaeological specimens
- **Multi-proxy integration** — Macroremains, microremains, bioarchaeology, ritual objects, and climate archives side-by-side
- **Resilience narratives** — Explorable scenarios for climate and colonial pressures
- **Readable citations** — Every panel surfaces its own APA 7th reference
- **Accessible theming** — Multiple visual themes for different viewing conditions

## What's Real vs. Placeholder

| Status | Item |
|---|---|
| ✅ Real | Site names & regional contexts |
| ✅ Real | APA 7th citations |
| ✅ Real | Archaeological concepts |
| ⚠ Partial | Site coordinates (regional centroids only) |
| ❌ Placeholder | All 3D specimen models |
| ❌ Placeholder | Artifact images & diagrams |
| ❌ Placeholder | Numerical resilience indices |
| ❌ Placeholder | Site-level descriptive text |

## Running Locally

Ethics & Indigenous Heritage
The sites referenced are located on the ancestral and unceded lands of the Zapotec, Mixtec, Maya, and Lenca peoples, among others. Any digital presentation of this heritage must be done with respect, attribution, and consultation with descendant communities.

This prototype is a technical demonstration only.

Tech Stack
MapLibre GL JS — satellite + terrain

Esri World Imagery — free public tiles

AWS Terrain DEM — elevation

Three.js r128 — 3D models

Tailwind CSS — layout

Google Fonts — Merriweather + Inter + JetBrains Mono

Credits
Prototype: Asia Khan, Hon. BA (McMaster University)

Inspired by: Dr. Shanti Morell-Hart Lab, McMaster University

Imagery: Esri · AWS · OpenStreetMap contributors

License
© 2026 Asia Khan · All Rights Reserved

This prototype, including its source code, interface design, written content, and procedural 3D models, is the intellectual property of the author. No part of this work may be reproduced, distributed, modified, or transmitted in any form or by any means without prior written permission from the author.

The prototype is provided "as is" for demonstration and educational viewing purposes only, without warranty of any kind.

Third-party libraries (MapLibre GL, Three.js, Tailwind CSS, Google Fonts, Font Awesome, Esri imagery, AWS terrain tiles) are used under their respective licenses and remain the property of their original creators.

```bash
python3 -m http.server 8000
# then open http://localhost:8000
