---
title: "Proiect 2 — Programări medicale (mini-clinic)"
date: "2025-09-23"
version: "1.0.0"
---

# Proiect 2 — Programări medicale (mini-clinic)

**Sesiune:** 2025–2026 • **Nr.:** 2 • **Slug:** `mini-clinic`

## Cuprins
- [Rezumat executiv](#rezumat-executiv)
- [Obiective de învățare](#obiective-de-învățare)
- [Cerințe funcționale](#cerințe-funcționale)
- [Cerințe nefuncționale](#cerințe-nefuncționale)
- [Setup mediu (Win11 / Ubuntu 25.04)](#setup-mediu-win11--ubuntu-2504)
- [Plan pe pași aliniați seminariilor 0→12](#plan-pe-pași-aliniați-seminariilor-012)
- [CI & calitate](#ci--calitate)
- [Evaluare & DoD](#evaluare--dod)
- [Prompts utile (VSL)](#prompts-utile-vsl)
- [Bibliografie (scurtă)](#bibliografie-scurtă)
- [Anexe](#anexe)

---

## Rezumat executiv
- Aplicație de gestionare a **programărilor medicale**; evoluează incremental pe parcursul seminariilor.
- **Back‑end**: Express → REST → (stub) SQLite/Sequelize; **Front‑end**: HTML/CSS → DOM/Events → Fetch → React/Redux/Charts (schelete).
- **Testare în oglindă** (Vitest & Jest) pe contracte de bază.
- Accesibilitate și i18n minimal, robustețe (timeout/retry/semafor) unde e potrivit.
- Echipe de **2** studenți; repo GitHub la fiecare membru; README standardizat.

## Obiective de învățare
1. Inițializare corectă a proiectelor Node/Express.
2. Utilizare ESM, scriere funcții pure și CLI.
3. Practică pe `map/filter/reduce` + imutabilitate.
4. Modelare entități/erori, memoizare, asincronie.
5. DOM/Events; Fetch/REST; React/Redux; Charts.
6. Configurare lint/format/test + CI simplu.

## Cerințe funcționale
- CRUD pentru **Medici**, **Pacienți**, **Programări** (mock → REST → DB).
- Calendar simplu, verificare slot disponibil, validări de bază.
- Interfață *responsive*; export CSV (client-side) opțional.

## Cerințe nefuncționale
- Răspuns sub 100ms pentru listări în mock; mesaje de eroare clare.
- Accesibilitate: label-uri, aria, focus vizibil.
- Portabilitate: Node 18/20+, test rapid în Firefox (F12).

## Setup mediu (Win11 / Ubuntu 25.04)
**Windows 11 (PowerShell):**
1. Instalează Node.js LTS și Git. Verifică: `node -v`, `npm -v`, `git --version`.
2. VS Code + extensii: ESLint, Prettier.
3. Firefox pentru teste rapide (F12).

**Ubuntu 25.04:**
```bash
sudo apt update && sudo apt install -y git curl firefox
curl -fsSL https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc && nvm install --lts && nvm use --lts
node -v && npm -v && git --version
```

## Plan pe pași aliniați seminariilor 0→12
### Sem.0 — Toolchain & server minimal
- **Spec:** `npm init -y`; Express static + `/ping → pong`.
- **Rulare:** `npm i && npm run dev` → `http://localhost:3000`.
- **Test:** `curl -s localhost:3000/ping` ⇒ `pong`.

### Sem.1 — JS modern, funcții, CLI
- **Spec:** funcție `sum(...xs)` + CLI: `node bin/cli.js 1 2 3` ⇒ `6`.
- **Teste:** Vitest & Jest (același contract).

### Sem.2 — Funcții & array‑uri
- **Spec:** `evens(xs)`; discuție despre `map/filter/reduce`.

### Sem.3 — OOP, erori, memoization
- **Spec:** entitate `Doctor` (invariante); raport `countPerDoctor` memoizat.

### Sem.4 — Module, evenimente & DOM
- **Spec:** form + listă; delegare evenimente; *serve* static.

### Sem.5–12 — schelete
- CSS selectors/layout; responsive; Fetch; REST; DB; React; Redux; Charts (în arhivă sunt READMEs & stubs).

## CI & calitate
- `.gitignore`, ESLint/Prettier (exemplu în COMMON).
- Scripturi: `test:vitest`, `test:jest`.

## Evaluare & DoD
- Corectitudine (35%), Async (25%), Performanță & memoizare (15%), Teste (15%), Calitate (10%).
- **DoD:** minimul funcțional implementat; testele verzi; README clar.

## Prompts utile (VSL)
- „Generează edge‑cases pentru `createAppointment` și scrie teste Vitest/Jest.”
- „Refactor `withRetry` cu backoff păstrând semnătura.”

## Bibliografie (scurtă)
- Wirfs‑Brock, A., & Eich, B. (2020). *JavaScript: The first 20 years*. https://doi.org/10.1145/3386327
- Maffeis, S., Mitchell, J. C., & Taly, A. (2008). *Operational semantics for JavaScript*. https://doi.org/10.1007/978-3-540-89330-1_22

## Anexe
- Diagrame simple client/server; checklist de release.
