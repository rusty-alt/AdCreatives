# Vercel Web Interface Guidelines audit

Audit target: `index.html`, `styles.css`, `app.js`  
Guidelines fetched: 2026-07-11 from `vercel-labs/web-interface-guidelines`.

## First-pass findings

- `index.html:7` — missing `theme-color` meta for the light full-bleed surface.
- `index.html:36` — above-fold product image missing `fetchpriority="high"`.
- `index.html:86` — asynchronous purchase-selection confirmation missing `aria-live`.
- `styles.css:1` — anchor targets missing `scroll-margin-top`.
- `styles.css:1` — headings missing `text-wrap: balance`.
- `styles.css:3` — 375px hero display text forces horizontal overflow.
- `styles.css:3` — mobile proof row preserves wide min-content and overflows.
- `styles.css:3` — mobile header CTA clips at the viewport edge.

## Improvements applied

- Added theme color and high-priority hero image loading.
- Added polite announcement semantics to the purchase-selection confirmation.
- Added visible focus treatment, balanced headings, tap highlight, and anchor offsets.
- Reduced mobile display scale, constrained grid children, stacked proof items, and removed the redundant mobile header CTA.
- Confirmed semantic buttons, labels, fieldset/legend, image dimensions, lazy loading below fold, skip link, reduced-motion support, and explicit transition properties.

## Result

No remaining critical accessibility or interaction violations found in the final static implementation. Stateful mechanism tabs remain client-side by design; the section itself is directly linkable at `#science`.
