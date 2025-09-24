# Proiect 1 — Catalog de cărți
**Titlu complet:** Catalog de cărți — gestiunea unei colecții de cărți pentru o bibliotecă mică  
**Sesiune:** 2025-2026

## 1) Titlu & meta
- Nr. proiect: 1
- Sesiune: 2025-2026
- Dată: 2025-09-23

## 2) Rezumat executiv
- Aplicație incrementală, 13 pași (Sem.0→Sem.12), CRUD cărți & autori, UI React + Redux, REST + SQLite/Sequelize, testare Vitest & Jest.

## 3) Obiective de învățare
- Design modular (ESM), REST, persistență, React/Redux, testare în oglindă, calitate (ESLint, Prettier).

## 4) Cerințe funcționale
- Listare/filtrare/sortare cărți; CRUD; API REST; UI reactivă.

## 5) Cerințe nefuncționale
- Accesibilitate, i18n minim, performanță percepută bună.

## 6) Setup mediu & toolchain
- Node ≥ 18, npm, Git, Vite, ESLint, Prettier, Vitest, Jest, Firefox (F12), LibreOffice, Pandoc.
- Windows/Ubuntu: inițializare director, `git init`, `npm init -y`, instalare dev deps.

## 7) Plan pe pași (Sem.0→Sem.12)
- **Sem.0**: Express `/ping → pong`, `public/index.html`.  
- **Sem.1**: `concat`, `cmp`, `sum`, `fib`, `freq`, CLI.  
- **Sem.2**: `map/filter/reduce`, `format`, `myMap`, `censor`.  
- **Sem.3**: entități, erori, `memoize`, `withTimeout/withRetry`, semafor.  
- **Sem.4**: ESM în browser, DOM, delegare evenimente.  
- **Sem.5**: Selectori CSS, grilă 3×3.  
- **Sem.6**: Flexbox/Grid + responsive.  
- **Sem.7**: Fetch + form, fallback localStorage.  
- **Sem.8**: REST CRUD /api/books.  
- **Sem.9**: SQLite/Sequelize (Book, Author).  
- **Sem.10**: React — listă + formular.  
- **Sem.11**: Redux Toolkit — slice & store.  
- **Sem.12**: DataTable & export CSV.

## 8) Integrare & calitate
- Scripturi: `lint`, `format`, `test`. `.gitignore` standard.

## 9) Evaluare & DoD
- Corectitudine (35%), Async & robustețe (25%), Performanță & memoizare (15%), Teste (15%), Calitate (10%).
- DoD: toate funcționalitățile minime + teste verzi; proiect funcțional în penultima săptămână.

## 10) Prompts utile
- Testare: „Generează 10 edge‑cases pentru filtrare cărți și scrie teste Vitest & Jest.”
- Refactor: „Rescrie `sortBooks` păstrând semnătura; explică trade‑off‑urile.”
- Robustețe: „Adaugă `withTimeout`/`withRetry` și semafor pentru `/api/books`.”

## 11) Bibliografie (APA 7; DOI)
- Wirfs‑Brock, A., & Eich, B. (2020). *JavaScript: The first 20 years*. https://doi.org/10.1145/3386327
- Fielding, R., & Taylor, R. (2000). *Principled design of the modern Web architecture*. https://doi.org/10.1145/337180.337228
- Parnas, D. L. (1972). *On the criteria...*. https://doi.org/10.1145/361598.361623

## 12) Anexe
- Scripturi utilitare: `withTimeout`, `withRetry`, semafor; memoizare cu TTL.
