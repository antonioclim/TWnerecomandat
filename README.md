# Tehnologii Web — **README total** pentru seminarele S0–S12

> Acest fișier oferă o privire unitară asupra întregii serii de seminare (0–12), astfel cum sunt organizate în depozitul Git: **un folder per seminar** (S0…S12), iar în interior trei subfoldere standard: **Partea 1 (Teorie)**, **Partea 2 (Laborator)**, **Partea 3 (Proiecte)**. Pentru fiecare seminar există și o analiză detaliată în `__README_Sx_analysis.md` aflată în rădăcina folderului seminarului.

*Generat la 2025-09-21 10:55.*

---

## 1. Structura depozitului

```
root/
├─ S0-Git&Tools/
│  ├─ Partea 1 (Teorie)/
│  ├─ Partea 2 (Laborator)/
│  ├─ Partea 3 (Proiecte)/
│  └─ __README_S0_analysis.md
├─ S1-Intro_JavaScript/
│  ├─ Partea 1 (Teorie)/ …
│  └─ __README_S1_analysis.md
├─ S2-Funcții& array-uri/
│  └─ __README_S2_analysis.md
├─ S3-Obj&OOP_JS/
│  └─ __README_S3_analysis.md
├─ S4-Module_evenimente&DOM/
│  └─ __README_S4_analysis.md
├─ S5-CSS_Selectors&Layout/
│  └─ __README_S5_analysis.md
├─ S6-CSS_Layout&Media_Queries/
│  └─ __README_S6_analysis.md
├─ S7-Fetch_API+formulare+JSON+persistență/
│  └─ __README_S7_analysis.md
├─ S8-servREST_cu_NodeExpress/
│  └─ __README_S8_analysis.md
├─ S9-Persistență_SQLite&SeQueLize/
│  └─ __README_S9_analysis.md
├─ S10-componente_React&JSX/
│  └─ __README_S10_analysis.md
├─ S11-Redux_Toolkit/
│  └─ __README_S11_analysis.md
└─ S12-Componente_externe-tabele_și_grafice/
   └─ __README_S12_analysis.md
```

> **Notă:** Denumirile exacte ale folderelor pot conține diacritice/semne speciale. Dacă anumite linkuri relative nu funcționează pe o platformă, consultați direct fișierul `__README_Sx_analysis.md` din folderul corespunzător.

---

## 2. Convenții metodologice (valabile pentru toate seminarele)

- **Dublă testare**: fiecare proiect are suite **Vitest** și **Jest** cu aserții oglindă, pentru transfer de competență între ecosisteme.
- **Calitate & CI**: reguli **ESLint** (flat/non‑flat), rulare în **CI** (workflows separate pentru lint, unit, e2e, PWA).
- **Variante**: acolo unde este cazul există **starter** și **solution** (și pentru niveluri L1–L3 în Partea 3).
- **.env.example**: catalog minimal de variabile (ex. `PORT`, `REPORT_LIMIT`, `TTL_MS`, `VITE_*`). `index.js`/`server.mjs` sau scripturile citesc/propagă aceste variabile.
- **PWA/E2E**: numai în subsetele avansate (L3) — **Workbox** (`sw.js`, `build-sw.mjs`) și **Playwright** (smoke/e2e).

---

## 3. Tabel de navigație (temă + link către analiza seminarului)

| Cod | Tema centrală | Analiza detaliată |
|---|---|---|
| **S0** | Git & Toolchain (ESM, Express, testare duală, CI) | `S0-Git&Tools/__README_S0_analysis.md` |
| **S1** | Introducere în JS: funcții, iterație, utilitar **CLI** | `S1-Intro_JavaScript/__README_S1_analysis.md` |
| **S2** | Map/Filter/Reduce, utilitare pure, pipeline & CLI | `S2-Funcții& array-uri/__README_S2_analysis.md` |
| **S3** | Obiecte, erori tipizate, memoization, async/await | `S3-Obj&OOP_JS/__README_S3_analysis.md` |
| **S4** | **ES Modules** în browser, Events & DOM, CSP | `S4-Module_evenimente&DOM/__README_S4_analysis.md` |
| **S5** | CSS Selectors & Layout (form styling, grid 3×3) | `S5-CSS_Selectors&Layout/__README_S5_analysis.md` |
| **S6** | CSS Layout & Media Queries (Flexbox, Grid, tipografie fluidă) | `S6-CSS_Layout&Media_Queries/__README_S6_analysis.md` |
| **S7** | Fetch API + formulare + JSON + persistență minimă | `S7-Fetch_API+formulare+JSON+persistență/__README_S7_analysis.md` |
| **S8** | Servicii **REST** cu Node/Express (ETag, CORS, RFC 7807) | `S8-servREST_cu_NodeExpress/__README_S8_analysis.md` |
| **S9** | Persistență cu **SQLite & Sequelize** (ACID, tranzacții) | `S9-Persistență_SQLite&SeQueLize/__README_S9_analysis.md` |
| **S10** | React: componente & **JSX** (Vite, RTL, accesibilitate) | `S10-componente_React&JSX/__README_S10_analysis.md` |
| **S11** | **Redux Toolkit** (entityAdapter, thunks, RTK Query) | `S11-Redux_Toolkit/__README_S11_analysis.md` |
| **S12** | Componente externe: **tabele & grafice** (TanStack, Chart.js) | `S12-Componente_externe-tabele_și_grafice/__README_S12_analysis.md` |

> Dacă structura locală folosește alte nume de directoare, accesați fișierele `__README_Sx_analysis.md` din fiecare folder Sx.

---

## 4. Ghid unificat de pornire (root)

### 4.1. Variante **standalone**
```bash
# Exemple tipice (rulate în interiorul fiecărui proiect)
npm i
npm test              # rulează Vitest + Jest (oglindă)
npm run dev           # server dev (Vite) sau aplicație CLI, după caz
```

### 4.2. Variante **monorepo** (PNPM)
```bash
pnpm i -w             # instalare la rădăcină
pnpm -w run test      # rulează toate testele
pnpm --filter <pachet> run dev   # pornește doar pachetul țintă
```

### 4.3. E2E & PWA (numai în L3)
```bash
# Playwright
npx playwright install --with-deps
pnpm -w run test:e2e

# Workbox
node build-sw.mjs     # sau npm run build:sw, după proiect
```

---

## 5. Recomandări didactice transversale

1. **Contracte înaintea implementării** — scrieți testele (Vitest & Jest) cu aceleași aserții, apoi codul.  
2. **Separarea preocupărilor** — funcții pure (fără I/O) + straturi „la margine” (CLI, rețea, DOM).  
3. **Accesibilitate prin design** — atribute ARIA, `:focus-visible`, contrast, măsură de text.  
4. **Calitate continuă** — rulați `lint` + `test` local, apoi în CI; PR‑urile trebuie să treacă toate suitele.  
5. **Operaționalizare** — `.env.example` ca document al configurației; nu comiteți `.env` real.  
6. **Scalare** — începeți în **standalone**, treceți la **monorepo** când colecția de proiecte crește/variază.  

---

## 6. Hărți rapide către artefacte comune

- **Workflows CI**: `.github/workflows/*` (lint, unit‑vitest, unit‑jest, e2e, workbox).  
- **Testare**: `tests/vitest/**` și `tests/jest/**` — oglinzi de funcționalitate.  
- **Config**: `vitest.config.ts`, `jest.config.cjs`, `babel.config.cjs`, `eslint.config.*`, `pnpm-workspace.yaml`.  
- **PWA/E2E** (L3): `workbox-config.js`, `build-sw.mjs`, `playwright.config.*`.  

---

## 7. Index descărcări (versiunile sintetizate generate în analiză)

Pentru consultare rapidă (copii ale analizelor generate în această sesiune):

- [README_S0_analysis.md](sandbox:/mnt/data/README_S0_analysis.md)  
- [README_S1_analysis.md](sandbox:/mnt/data/README_S1_analysis.md)  
- [README_S2_analysis.md](sandbox:/mnt/data/README_S2_analysis.md)  
- [README_S3_analysis.md](sandbox:/mnt/data/README_S3_analysis.md)  
- [README_S4_analysis.md](sandbox:/mnt/data/README_S4_analysis.md)  
- [README_S5_analysis.md](sandbox:/mnt/data/README_S5_analysis.md)  
- [README_S6_analysis.md](sandbox:/mnt/data/README_S6_analysis.md)  
- [README_S7_analysis.md](sandbox:/mnt/data/README_S7_analysis.md)  
- [README_S8_analysis.md](sandbox:/mnt/data/README_S8_analysis.md)  
- [README_S9_analysis.md](sandbox:/mnt/data/README_S9_analysis.md)  
- [README_S10_analysis.md](sandbox:/mnt/data/README_S10_analysis.md)  
- [README_S11_analysis.md](sandbox:/mnt/data/README_S11_analysis.md)  
- [README_S12_analysis.md](sandbox:/mnt/data/README_S12_analysis.md)  

---

## 8. Prompt reutilizabil (scurt) pentru noi seminare

> „Generează pentru **Seminarul Sx** (standalone & monorepo) codul + testele **Vitest/Jest** (oglindă), **CI**, README cu **Quick start** & **Troubleshooting**, variante **starter/solution** și, pentru L3, extensii **E2E/PWA**. Integrează teorie ↔ laborator ↔ proiecte și marchează eventualele lipsuri.”

---

**Licență & bune practici.** Respectați licențele pachetelor terțe, politica de confidențialitate și legile privind datele personale. Pentru conținutul educațional propriu, includeți o licență (ex. CC BY‑SA) în rădăcina depozitului.
