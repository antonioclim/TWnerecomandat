# Seminarul 6 — Partea 2 (Laborator, extins)
**CSS Layout & Media Queries — Flexbox, Grid, responsive UI**

Acest pachet conține **starter code** pentru laborator:
- **HTML**: `public/index.html`, `public/detail.html`
- **CSS**: `styles/{base,typography,layout,components,utilities}.css`
- **JS**: `src/main.js` (minim; layout-ul este CSS-driven)
- **Teste**: Vitest & Jest (jsdom) în `tests/unit`
- **Server**: `server.mjs` (Express) pentru previzualizare locală

## Rulare
```bash
npm i
npm run dev           # http://localhost:5196  (redirect la /public/index.html)
npm run test:vitest   # rulează testele Vitest
npm run test:jest     # rulează testele Jest
npm test              # rulează ambele
```

## Checklist de predare (scurt)
- ✅ Cel puțin **3 media queries** (480 / 768 / 1200) — și opțional 1920 pentru panou
- ✅ **Grid** pentru listă de carduri cu `repeat(auto-fit, minmax(16rem, 1fr))`
- ✅ **Flex** cu `flex-wrap` și `gap` pentru nav/toolbars
- ✅ Imagini cu `aspect-ratio: 4/3` și `object-fit: cover`
- ✅ Tipografie fluidă cu `clamp()`
- ✅ Pagina de detaliu folosește **grid-template-areas**

Pentru explicații complete (pași, rubrică, troubleshooting, AI‑assist VSL), vezi documentul **DOCX** livrat pentru Partea 2.
