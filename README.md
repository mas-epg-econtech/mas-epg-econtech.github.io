# Economic Dashboards — Landing Page

A single-page landing site that links out to six economic dashboards built with Cowork.
Designed for the MAS internal AI showcase (May 2026). Polished corporate aesthetic,
A1-poster-friendly card layout, renders cleanly on desktop and mobile.

## Contents

```
index.html            The landing page. Self-contained, no build step.
images/
  grocery.svg         Singapore grocery price tracker
  shipping.svg        Global shipping nowcast
  iran.svg            Iran crisis trade monitor
  sgx.svg             SGX sentiment index
  property.svg        Singapore property market
  asean.svg           ASEAN markets dashboard
```

The page uses six hand-drawn SVG hero illustrations. No external CSS/JS dependencies,
no fonts loaded from the network (system fonts + Georgia), no trackers.

## Publishing to GitHub Pages

1. **Create a new repository** on GitHub (suggested name: `econ-ai-showcase` —
   the page will live at `https://econtech-mas.github.io/econ-ai-showcase/`).

2. **Push these files** to the repo's default branch:

   ```bash
   cd econ-ai-landing
   git init
   git add index.html images/ README.md
   git commit -m "Initial landing page"
   git branch -M main
   git remote add origin git@github.com:econtech-mas/econ-ai-showcase.git
   git push -u origin main
   ```

3. **Enable Pages** in the repo: Settings → Pages → Build from branch →
   `main` / `/ (root)` → Save. Wait a minute or two, then the URL appears
   at the top of the Pages settings tab.

4. **Test the live link** on your phone as well — this will be the QR-code target
   at the booth.

## Editing the copy

All text lives inside `index.html`. Each card is a single `<a class="card">` block
containing the image, a category kicker, a headline, and a one-sentence description.
Edit in place; no rebuild required.

## Notes for the booth

- The landing page itself is unauthenticated. Four of the six linked dashboards
  currently sit behind a client-side password gate — consider whether you want
  that gate lifted for the showcase period.
- For the A1 printed poster, you can reuse any of the six SVGs as decorative
  elements or reprint them at scale (they are resolution-independent vector files).
- Add a QR code on the poster that points to the landing page URL once Pages is live.
