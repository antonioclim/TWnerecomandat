# Seminarul 5 — Partea 2 (Laborator): CSS Selectors & Layout — pseudo‑clase, form styling, grid 3×3

Acest repo conține **starter code** pentru laboratorul din Partea 2 (Seminarul 5). Vei lucra pe:
- **selectors moderni** (`:is()`, `:where()`, `:has()`), 
- **form styling** accesibil (`:focus-visible`, `:invalid/:valid`, `accent-color`, `::file-selector-button`),
- **grid 3×3** responsiv (`display: grid`, `grid-template-columns`, `gap`, `aspect-ratio`).

## Structură
```
s5p2-starter/
  public/index.html
  styles/{base.css, forms.css, layout.css, components.css}
  src/{utils/dom.js, main.js}
  tests/unit/{selectors.vitest.test.ts, selectors.jest.test.mjs}
  vitest.config.ts
  jest.config.cjs
  server.mjs
  package.json
```

## Rulare
```bash
npm i
npm run dev           # http://localhost:5175 (redirect la /public/index.html)
npm run test:vitest
npm run test:jest
```

## Worksheet — checklist (scurt)
- Ai **focus ring** vizibil pe linkuri/butoane/inputuri (`:focus-visible`)?
- Stilizezi **grupurile cu erori** prin `:has(input:invalid)`?
- Formularul conține **required**/`novalidate` și mesaje de eroare locale?
- Gridul „**3×3**” funcționează și **colapsează** la 2/1 coloane?
- Folosești `:where()` pentru a **nu** crește specificitatea?

> Pentru enunțul complet, explicațiile pas cu pas, rubrică de evaluare și troubleshoot, vezi documentul **DOCX** al Părții 2.
