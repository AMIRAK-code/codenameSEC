# Overseer — Enterprise AI Gateway & Usage Overseer

Landing page for the Overseer proposal: an AI gateway and DLP proxy that checks the intent of every prompt against the sender's role, masks sensitive data, and meters token spend before requests reach Claude or OpenAI.

`index.html` is a single self-contained page:

- **Three.js (r128)** renders one fixed WebGL stage with a 3,400-particle field, the gate rings, the Overseer core, a telemetry grid and an orbit halo.
- **Scroll-driven scenes**: each chapter (`data-scene`) maps to a particle formation and camera pose. Scroll position is turned into a continuous scene index, and particles morph between formations with a per-particle stagger.
- Pointer parallax on desktop, a reduced-motion path, and a lighter field on phones.

Open `index.html` in a browser, or serve the folder with any static host (Vercel, Render, GitHub Pages).
