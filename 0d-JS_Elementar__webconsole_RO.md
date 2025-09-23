# JSbasics_webconsole_RO — versiune extinsă **integrală**

Această versiune include **integral** conținutul „JSbasics_webconsole_RO.md” și adaugă, în mod selectiv și logic, secțiuni relevante din materialele încărcate («Seminar 0 — Toolchain, inițializare proiect, server minimal»).

**Instrucțiune:** Rămân valabile regulile: comentariile/narațiunile în română; comenzile și noțiunile netraductibile păstrate exact.

## Cuprins
- Partea I — Conținut integral «JSbasics_webconsole_RO.md»
- Partea II — Extensii selectate din «Seminar 0» (toolchain, server minimal, HTTP/HTML, exemple rulabile)
- Bibliografie (APA 7)

---

## Partea I — Conținut integral «JSbasics_webconsole_RO.md»

# Bazele JavaScript pentru **Consola Web din Firefox**
_Un ghid compact, orientat academic, cu exerciții practice și comparații concise cu Python și C++._  
**Context de utilizare:** Deschide Firefox → Consola Web (`Ctrl`+`Shift`+`K`). Poți lipi direct blocurile de cod și observa rezultatele.

---

## 0) Pornirea în consola browserului
- Consola Web evaluează codul _în contextul paginii_ (are acces la `window`, la API-urile DOM etc.).  
- Folosește `console.log(valoare)` pentru a afișa rezultate explicit (consola mai afișează și ultima expresie evaluată).  
- Șterge consola cu `Ctrl`+`L` (sau cu pictograma coș de gunoi).  
- Input pe mai multe linii: apasă `Shift`+`Enter` pentru linie nouă fără executare.

> **Diferențe de mediu**
> - **JS (browser)**: asincron, event loop, acces la DOM.  
> - **Python (REPL)**: multiparadigmă, biblioteci standard bogate; fără DOM.  
> - **C++ (REPL prin cling etc.)**: compilat, tipare statice; fără DOM; ecosistem de build manual.

---

## 1) Declarații: `var`, `let`, `const`
**Esențial:**  
- `var` → scope de funcție; poate fi redeclarat în același scope; este hoisted.  
- `let` → scope de bloc; **nu** poate fi redeclarat în același bloc; există _temporal dead zone_ înainte de inițializare.  
- `const` → binding constant; obiectele pot fi modificate intern, dar nu se poate reasigna identificatorul.

```js
// 'var' — scope de funcție, redeclarabil
var a = 10;
console.log(a); // 10
var a = 20;     // redeclarare permisă
console.log(a); // 20

// 'let' — scope de bloc, nere-declarabil în același bloc
let b = 5;
b = 7;          
console.log(b); // 7
// let b = 8;   // ❌ Eroare: redeclarare în același scope

// 'const' — binding fix
const c = 3.14;
console.log(c); // 3.14
// c = 2.71;    // ❌ Eroare: nu se poate reasigna

// 'const' cu obiecte: binding fix, interior modificabil
const cfg = { mode: "dev" };
cfg.mode = "prod";        // permis
console.log(cfg.mode);    // "prod"
```

**Atenție (hoisting & TDZ):**
```js
// Hoisting cu var:
console.log(x); // undefined (declararea e ridicată, inițializarea nu)
var x = 1;

// TDZ cu let/const:
try {
  console.log(y); // ReferenceError
} catch (e) { console.log(e.name); }
let y = 1;
```

> **Diferențe**
> - **Python**: un singur tip de declarație; variabile re-asignabile; nu există hoisting.  
> - **C++**: tipuri explicite sau `auto`; scope strict pe bloc; `const` profund (obiectul nu poate fi modificat).

---

## 2) Tipuri & `typeof`
Tipuri primitive: `number`, `string`, `boolean`, `undefined`, `symbol`, `bigint` și `null` (unde `typeof null === "object"` e o particularitate istorică).

```js
let num = 42;
let text = "Salut";
let flag = true;
let nothing = null;
let notDefined;
let big = 10n;
let sym = Symbol("id");

console.log(typeof num);        // "number"
console.log(typeof text);       // "string"
console.log(typeof flag);       // "boolean"
console.log(typeof nothing);    // "object" (istoric)
console.log(typeof notDefined); // "undefined"
console.log(typeof big);        // "bigint"
console.log(typeof sym);        // "symbol"
```

> **Diferențe**
> - **Python**: `int` nelimitat, `float`, `bool`, `None`.  
> - **C++**: tipuri primitive fixe; `nullptr` pentru nul.

---

## 3) Numere și operații aritmetice
JS folosește IEEE-754 dublă precizie pentru `number`. `BigInt` pentru întregi mari. Nu se pot amesteca `number` și `bigint`.

```js
let x = 10, y = 3;
console.log(x + y);   // 13
console.log(x - y);   // 7
console.log(x * y);   // 30
console.log(x / y);   // 3.333...
console.log(x % y);   // 1
console.log(x ** y);  // 1000

// Problema clasică cu zecimale
console.log(0.1 + 0.2);       // 0.30000000000000004
```

> **Diferențe**
> - **Python**: `int` precis nelimitat; `Decimal` pentru calcule exacte.  
> - **C++**: tipuri separate pentru întregi și float; risc de overflow.

---

## 4) Egalitate și adevăr
Preferă `===` și `!==` pentru a evita conversii implicite.

```js
console.log(5 == "5");   // true (conversie)
console.log(5 === "5");  // false

console.log(null == undefined);   // true
console.log(null === undefined);  // false

// Truthy / falsy
console.log(Boolean(""));     // false
console.log(Boolean(" "));    // true
console.log(Boolean(0));      // false
console.log(Boolean([]));     // true
console.log(Boolean({}));     // true
```

> **Diferențe**
> - **Python**: `==` vs `is`; colecțiile goale sunt false.  
> - **C++**: fără conversii string↔număr; `==` compară valori.

---

## 5) Șiruri de caractere
Șirurile sunt imutabile. Template literals (`) pentru interpolare.

```js
let s = "JavaScript";
console.log(s.length);         
console.log(s.toUpperCase());  
console.log(s.includes("Script")); 

let nume = "lume";
console.log(`Salut, ${nume}!`);
```

> **Diferențe**
> - **Python**: șiruri Unicode, f-strings.  
> - **C++**: `std::string` mutabil.

---

## 6) Tablouri (arrays)
Tablouri dinamice cu metode utile.

```js
let arr = [1, 2, 3];
arr.push(4);           
arr.pop();             
arr[0] = 99;           
console.log(arr.map(x => x * 2)); 
```

> **Diferențe**
> - **Python**: liste cu slicing, comprehensiuni.  
> - **C++**: `std::vector`, `std::array` fixe.

---

## 7) Obiecte
Structuri de tip dicționar.

```js
let persoana = { nume: "Ana", varsta: 25 };
console.log(persoana.nume);
persoana.varsta = 26;
persoana.oras = "București";
console.log(Object.keys(persoana));
```

---

## 8) Funcții
```js
// Funcție declarată (hoisted)
function salut(nume) {
  return "Salut, " + nume;
}
console.log(salut("Ion"));

// Funcție săgeată
const patrat = n => n * n;
console.log(patrat(5));
```

---

## 9) Control
```js
let scor = 80;
if (scor >= 90) console.log("A");
else if (scor >= 70) console.log("B"); // "B"
else console.log("C");

for (let i = 1; i <= 3; i++) console.log(i);

let n = 0;
while (n < 3) { console.log(n); n++; }
```

---

## 10) Erori
```js
try {
  JSON.parse("{gresit}");
} catch (e) {
  console.log(e.name); 
} finally {
  console.log("Rulează oricum");
}
```

---

## 11) DOM (specific browserului)
```js
document.title;
document.querySelectorAll("a").length;
const el = document.createElement("div");
el.textContent = "Salut DOM";
document.body.appendChild(el);
```

---

### Mini test rapid
```js
// 1) Ce se afișează?
let p = [];
console.log(Boolean(p), p.length); 

// 2) Egalitate?
console.log(0 == false, 0 === false); 

// 3) Hoisting?
var d;
console.log(d); // undefined
d = 1;
console.log(d);

// 4) BigInt?
try { console.log(1n + 1); } catch (e) { console.log(e.name); }

// 5) this?
const ctx = { v: 7, g(){ return this.v; } };
console.log(ctx.g()); // 7
```

---

### Extensii potrivite din «Seminar0_Toolchain_Server_MinimalSTEP1.md»


## 2. Mediu & reflex de testare rapidă (Node REPL, Firefox Console)

**Verificări de 10–30 secunde:**

```bash
node --version
npm --version
git --version
```

**Firefox → F12 / Console:**

```js
console.log("Salut din browser!"),
document.body ? "DOM disponibil" : "DOM indisponibil";
```

**Node REPL:**

```js
console.log("Salut din Node!"), typeof window === "undefined"
```

---


## 3. Teorie

### 3.1 HTTP (protocol) vs. HTML (limbaj de marcare)

- **HTTP**: protocol request/response, statusuri și anteturi.
- **HTML**: structură și semantica documentelor; browserul construiește **DOM**.
- Serverul răspunde la cereri **HTTP** cu resurse (HTML/CSS/JS/JSON).

### 3.2 Node.js (runtime) & npm (package manager)

- **Node.js** rulează JS pe server; expune API‑uri (`fs`, `http`, `path`).
- **npm** gestionează pachete și **scripts**; `package.json` descrie proiectul.
- **ESM** recomandat în 2025: setează `"type": "module"`.

### 3.3 Git/GitHub — disciplina minimă

- Repo local, commit‑uri mici, *remote* `origin`, **push** pe `main`.
- Mesaje gen **Conventional Commits** (`feat:`, `fix:`, `docs:`) clarifică istoria.

### 3.4 Structura de proiect minimală

```
tw-seminar-0/
  public/
    index.html
  src/
    app.js
    index.js
  package.json
  README.md
```

### 3.5 Ciclu editare → rulare → testare

Editare (VS Code) → rulare (npm scripts) → test (Vitest/Jest sau probe `curl`) → commit & push.

---


### 3.1 HTTP (protocol) vs. HTML (limbaj de marcare)

- **HTTP**: protocol request/response, statusuri și anteturi.
- **HTML**: structură și semantica documentelor; browserul construiește **DOM**.
- Serverul răspunde la cereri **HTTP** cu resurse (HTML/CSS/JS/JSON).


### 3.2 Node.js (runtime) & npm (package manager)

- **Node.js** rulează JS pe server; expune API‑uri (`fs`, `http`, `path`).
- **npm** gestionează pachete și **scripts**; `package.json` descrie proiectul.
- **ESM** recomandat în 2025: setează `"type": "module"`.


### 3.4 Structura de proiect minimală

```
tw-seminar-0/
  public/
    index.html
  src/
    app.js
    index.js
  package.json
  README.md
```


### 3.5 Ciclu editare → rulare → testare

Editare (VS Code) → rulare (npm scripts) → test (Vitest/Jest sau probe `curl`) → commit & push.

---


## 4. Aplicații/Cod/Comenzi

> Format: **(a)** specificație • **(b)** cod • **(c)** comenzi • **(d)** de ce funcționează • **(e)** JS↔Python↔C++ • **(f)** test • **(g)** erori.

### E1. Inițializare proiect + repo Git

**(a)** Creează director, repo Git, `README.md`, `package.json`.

**(b/c) Comenzi:**

```bash
mkdir tw-seminar-0 && cd tw-seminar-0
git init
echo "# TW Seminar 0" > README.md
git add -A && git commit -m "chore: initial commit (scaffold repo)"
npm init -y
```

**(d)** `git init` creează `.git/`; `npm init -y` definește `package.json`.

**(e)** Python: `python -m venv .venv` + `pip`. C++: CMake/MSBuild + vcpkg (fără manager universal).

**(f)** `git status`, `cat package.json`.

**(g)** Git lipsă → instalează „Git for Windows”.

### E2. Server Express minimal + static

**(a)** Servește `public/index.html` și definește `GET /ping → "pong"`.

**(b)** Instalare și structură:

```bash
npm i express
npm i -D nodemon
mkdir -p public src
printf '<!doctype html><html lang="ro"><meta charset="utf-8"><body><h1>hello web</h1></body></html>' > public/index.html
```

**`src/app.js`:**

```js
import express from "express";
import path from "path";
import { fileURLToPath } from "url";

const __filename = fileURLToPath(import.meta.url);
const __dirname = path.dirname(__filename);

export function createApp() {
  const app = express();
  app.use(express.json());
  app.use(express.static(path.join(__dirname, "../public")));
  app.get("/ping", (req, res) => res.send("pong"));
  return app;
}
```

**`src/index.js`:**

```js
import { createApp } from "./app.js";
const PORT = process.env.PORT || 3000;
createApp().listen(PORT, () => console.log(`Server on http://localhost:${PORT}`));
```

**(c)** Scripturi & rulare:

```bash
npm pkg set type=module
npm pkg set scripts.dev="nodemon src/index.js"
npm pkg set scripts.start="node src/index.js"
npm run dev
```

**(d)** `express.static` mapează directorul `public`; `listen` atașează socketul la port.

**(e)** Python (Flask) și C++ (Boost.Asio) au echivalente conceptuale pentru server/endpoint.

**(f)** `curl http://localhost:3000/ping` → `pong`; browser la `/`.

**(g)** 404 la `/` → verifică `public/index.html` și calea lui `express.static`.

### E3. GET /api/time (JSON)

**(a)** Returnează ora curentă în ISO‑8601.

**(b)**

```js
// în createApp()
app.get("/api/time", (req, res) => res.json({ now: new Date().toISOString() }));
```

**(c)** `curl http://localhost:3000/api/time` → `{"now":"...Z"}`.

**(d)** `res.json` setează automat `Content-Type: application/json`.

**(e)** Python: `return {"now": datetime.utcnow().isoformat()+"Z"}`; C++: serializare manuală.

**(f)** Va fi testată la E5.

**(g)** „Cannot set headers...” → trimite răspuns o singură dată.

### E4. Scripturi npm & nodemon

```bash
npm pkg set scripts.test="echo "(temporar)""
```

*`dev`* repornește la schimbări; *`start`* pornește serverul fără nodemon.

### E5. Testare în oglindă: Vitest & Jest

```bash
npm i -D vitest jest babel-jest @babel/preset-env supertest
npm pkg set scripts.test:vitest="vitest run --reporter verbose"
npm pkg set scripts.test:jest="jest --runInBand"
npm pkg set scripts.test="npm run test:vitest && npm run test:jest"
```

**Vitest — `tests/vitest/app.test.js`:**

```js
import request from "supertest";
import { createApp } from "../../src/app.js";
import { describe, it, expect } from "vitest";

describe("GET /ping", () => {
  it("200 cu 'pong'", async () => {
    const app = createApp();
    await request(app).get("/ping").expect(200, "pong");
  });
});
```

**Jest — `tests/jest/app.jest.test.js`:**

```js
import request from "supertest";
import { createApp } from "../../src/app.js";

describe("GET /ping", () => {
  it("200 cu 'pong'", async () => {
    const app = createApp();
    await request(app).get("/ping").expect(200, "pong");
  });
});
```

**Rulare:** `npm test` → ambele suite.

### E6. Publicare pe GitHub

```bash
git branch -M main
git remote add origin https://github.com/<user>/tw-seminar-0.git
git push -u origin main
```

### E7. Bonus: fetch cu timeout/abort

```js
function withTimeout(ms, { signal } = {}) {
  const ctrl = new AbortController();
  const id = setTimeout(() => ctrl.abort(new Error("Timeout")), ms);
  if (signal) signal.addEventListener("abort", () => ctrl.abort(signal.reason));
  return { signal: ctrl.signal, done: () => clearTimeout(id) };
}

async function getTime(base = "http://localhost:3000") {
  const t = withTimeout(1000);
  try {
    const r = await fetch(`${base}/api/time`, { signal: t.signal });
    if (!r.ok) throw new Error(`HTTP {r.status}`);
    return await r.json();
  } finally { t.done(); }
}
```

---

---

### Extensii potrivite din «Seminar0_Toolchain_Server_MinimalSTEP1-extins.md»


## 3. Teorie (progresiv)

### 3.1 HTTP (protocol) vs. HTML (limbaj de marcare)
HTTP definește schimbul de mesaje (metode, coduri, antete). HTML definește structura documentului. Serverul răspunde pe HTTP, browserul interpretează HTML.

**Experiment (10 sec., Firefox):**
```js
fetch("https://httpbin.org/get").then(r=>r.status)
```

### 3.2 Rolul Node.js și npm
Node rulează JS pe server; npm gestionează pachete și scripturi. `package.json` descrie proiectul.

### 3.3 Git/GitHub
Istoric, ramuri, remote. Practici minime: commit‑uri mici, `.gitignore`, README, `main`.

### 3.4 Structura minimală & ciclu de lucru
`public/` (static), `src/` (server). Ciclul: editezi → `npm run dev` → testezi (`curl`/Firefox).

### 3.5 ESM vs. CJS (2025)
Activezi ESM cu `"type":"module"`. Specifică extensiile (`./x.js`). Pentru CJS‑only, folosește import dinamic sau versiuni compatibile.


### 3.1 HTTP (protocol) vs. HTML (limbaj de marcare)
HTTP definește schimbul de mesaje (metode, coduri, antete). HTML definește structura documentului. Serverul răspunde pe HTTP, browserul interpretează HTML.

**Experiment (10 sec., Firefox):**
```js
fetch("https://httpbin.org/get").then(r=>r.status)
```


### 3.2 Rolul Node.js și npm
Node rulează JS pe server; npm gestionează pachete și scripturi. `package.json` descrie proiectul.


### 3.4 Structura minimală & ciclu de lucru
`public/` (static), `src/` (server). Ciclul: editezi → `npm run dev` → testezi (`curl`/Firefox).


### 3.5 ESM vs. CJS (2025)
Activezi ESM cu `"type":"module"`. Specifică extensiile (`./x.js`). Pentru CJS‑only, folosește import dinamic sau versiuni compatibile.


## 4. Aplicații / Cod / Comenzi (exemple rulabile)

### Exemplul A — „Hello, web” static + `express.static`
**Specificație:** `GET /` servește `public/index.html`.
**Cod și rulare:**
```bash
mkdir tw-seminar-0 && cd tw-seminar-0
npm init -y && npm i express
mkdir public && printf "<!doctype html><meta charset='utf-8'><h1>hello web</h1>" > public/index.html
printf "import express from 'express';\nconst app=express();\napp.use(express.static('public'));\napp.listen(3000,()=>console.log('http://localhost:3000'))" > index.js
node index.js
```
**Test:** `curl -s -o /dev/null -w "%{http_code}\n" http://localhost:3000/` → `200`.

### Exemplul B — `GET /ping → pong`
```js
import express from 'express';
const app = express();
app.get('/ping', (_,res)=>res.send('pong'));
app.listen(3000);
```
**Test:** `curl http://localhost:3000/ping` → `pong`.

### Exemplul C — `GET /api/time → { now }`
```js
app.get('/api/time', (_,res)=>res.json({ now: new Date().toISOString() }));
```
**Firefox:** `fetch("http://localhost:3000/api/time").then(r=>r.json())`.

### Exemplul D — Scripturi `dev`/`start`
`package.json`:
```json
{ "type":"module",
  "scripts":{"dev":"nodemon index.js","start":"node index.js"},
  "devDependencies": {"nodemon":"^3.0.0"}, "dependencies":{"express":"^4.19.0"}
}
```
**Rulare:** `npm run dev` (watch) / `npm start`.

### Exemplul E — GitHub (remote origin, push)
```bash
git init && git add -A && git commit -m "chore: initial"
git branch -M main
git remote add origin https://github.com/<user>/tw-seminar-0.git
git push -u origin main
```

### Exemplul F — Test în oglindă (Vitest & Jest)
```bash
npm i -D vitest jest supertest babel-jest @babel/preset-env
```
Vitest:
```js
import {describe,it,expect} from 'vitest'; import express from 'express'; import req from 'supertest';
describe('GET /ping', ()=>{
  it('200 & pong', async ()=>{
    const app=express().get('/ping',(_,res)=>res.send('pong'));
    const r=await req(app).get('/ping'); expect(r.status).toBe(200); expect(r.text).toBe('pong');
  });
});
```
Jest: același contract, alt runner.

### Exemplul G — Comandă compusă
```bash
mkdir tw-seminar-0 && cd tw-seminar-0 && npm init -y
```
`&&` execută secvențial doar dacă pasul precedent a reușit.


### Exemplul A — „Hello, web” static + `express.static`
**Specificație:** `GET /` servește `public/index.html`.
**Cod și rulare:**
```bash
mkdir tw-seminar-0 && cd tw-seminar-0
npm init -y && npm i express
mkdir public && printf "<!doctype html><meta charset='utf-8'><h1>hello web</h1>" > public/index.html
printf "import express from 'express';\nconst app=express();\napp.use(express.static('public'));\napp.listen(3000,()=>console.log('http://localhost:3000'))" > index.js
node index.js
```
**Test:** `curl -s -o /dev/null -w "%{http_code}\n" http://localhost:3000/` → `200`.


### Exemplul B — `GET /ping → pong`
```js
import express from 'express';
const app = express();
app.get('/ping', (_,res)=>res.send('pong'));
app.listen(3000);
```
**Test:** `curl http://localhost:3000/ping` → `pong`.


### Exemplul C — `GET /api/time → { now }`
```js
app.get('/api/time', (_,res)=>res.json({ now: new Date().toISOString() }));
```
**Firefox:** `fetch("http://localhost:3000/api/time").then(r=>r.json())`.


### Exemplul D — Scripturi `dev`/`start`
`package.json`:
```json
{ "type":"module",
  "scripts":{"dev":"nodemon index.js","start":"node index.js"},
  "devDependencies": {"nodemon":"^3.0.0"}, "dependencies":{"express":"^4.19.0"}
}
```
**Rulare:** `npm run dev` (watch) / `npm start`.


### Exemplul E — GitHub (remote origin, push)
```bash
git init && git add -A && git commit -m "chore: initial"
git branch -M main
git remote add origin https://github.com/<user>/tw-seminar-0.git
git push -u origin main
```


## 5. Mini‑laborator progresiv (L1→L2→L3)

**L1:** scaffold, static, `/ping`.  
**L2:** `/api/time`, `createApp()`/`listen()`, teste Vitest/Jest.  
**L3:** `.env` pentru `PORT`, antete no‑cache, health.json, push pe GitHub.  
**Checklist:** rute ok, scripturi, teste verzi, README.


## 6. Anti‑pattern‑uri, capcane și troubleshooting

- Magie în scripturi → păstrează comenzi explicite.
- Amestec responsabilități → separă `createApp()` de `listen()`.
- Fără health‑check → adaugă `/ping`.
- Port blocat → schimbă `PORT` sau oprește procesul vechi.
- CJS/ESM confuz → verifică `"type":"module"` și extensiile.
- Dependențe inutile → instalează strict necesarul.

---

## Bibliografie (APA 7)
- Wirfs‑Brock, A., & Eich, B. (2020). JavaScript: The first 20 years. *Proceedings of the ACM on Programming Languages (HOPL)*, 4(HOPL), 1–189. https://doi.org/10.1145/3386327
- Fielding, R., Nottingham, M., & Reschke, J. (2022). HTTP Semantics (RFC 9110). IETF. https://doi.org/10.17487/RFC9110
