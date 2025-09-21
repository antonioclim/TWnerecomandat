# Seminarul S6 — CSS Layout & Media Queries (Flexbox, Grid, responsive UI) — Analiză integrată (standalone & monorepo)

*Generat la 2025-09-21 05:11.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar6_Partea2_lab.zip

```
README.md
jest.config.cjs
package.json
public/detail.html
public/index.html
server.mjs
src/main.js
styles/base.css
styles/components.css
styles/layout.css
styles/typography.css
styles/utilities.css
tests/unit/layout.jest.test.mjs
tests/unit/layout.vitest.test.ts
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 4, docs: 1, public: 2, styles: 5, code: 1, tests: 2.

**package.json — sinteză (scripturi, workspaces, dependențe)**

- `package.json`: name=`seminar6-part2-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom

### Seminar6_Partea3_monorepo.zip

```
package.json
packages/l1-p01/README.md
packages/l1-p01/jest.config.cjs
packages/l1-p01/package.json
packages/l1-p01/public/index.html
packages/l1-p01/server.mjs
packages/l1-p01/src/main.js
packages/l1-p01/styles.css
packages/l1-p01/tests/config.json
packages/l1-p01/tests/layout.jest.test.cjs
packages/l1-p01/tests/layout.vitest.test.ts
packages/l1-p01/vitest.config.ts
packages/l1-p02/README.md
packages/l1-p02/jest.config.cjs
packages/l1-p02/package.json
packages/l1-p02/public/index.html
packages/l1-p02/server.mjs
packages/l1-p02/src/main.js
packages/l1-p02/styles.css
packages/l1-p02/tests/config.json
packages/l1-p02/tests/layout.jest.test.cjs
packages/l1-p02/tests/layout.vitest.test.ts
packages/l1-p02/vitest.config.ts
packages/l1-p03/README.md
packages/l1-p03/jest.config.cjs
packages/l1-p03/package.json
packages/l1-p03/public/index.html
packages/l1-p03/server.mjs
packages/l1-p03/src/main.js
packages/l1-p03/styles.css
packages/l1-p03/tests/config.json
packages/l1-p03/tests/layout.jest.test.cjs
packages/l1-p03/tests/layout.vitest.test.ts
packages/l1-p03/vitest.config.ts
packages/l1-p04/README.md
packages/l1-p04/jest.config.cjs
packages/l1-p04/package.json
packages/l1-p04/public/index.html
packages/l1-p04/server.mjs
packages/l1-p04/src/main.js
packages/l1-p04/styles.css
packages/l1-p04/tests/config.json
packages/l1-p04/tests/layout.jest.test.cjs
packages/l1-p04/tests/layout.vitest.test.ts
packages/l1-p04/vitest.config.ts
packages/l1-p05/README.md
packages/l1-p05/jest.config.cjs
packages/l1-p05/package.json
packages/l1-p05/public/index.html
packages/l1-p05/server.mjs
packages/l1-p05/src/main.js
packages/l1-p05/styles.css
packages/l1-p05/tests/config.json
packages/l1-p05/tests/layout.jest.test.cjs
packages/l1-p05/tests/layout.vitest.test.ts
packages/l1-p05/vitest.config.ts
packages/l1-p06/README.md
packages/l1-p06/jest.config.cjs
packages/l1-p06/package.json
packages/l1-p06/public/index.html
packages/l1-p06/server.mjs
packages/l1-p06/src/main.js
packages/l1-p06/styles.css
packages/l1-p06/tests/config.json
packages/l1-p06/tests/layout.jest.test.cjs
packages/l1-p06/tests/layout.vitest.test.ts
packages/l1-p06/vitest.config.ts
packages/l1-p07/README.md
packages/l1-p07/jest.config.cjs
packages/l1-p07/package.json
packages/l1-p07/public/index.html
packages/l1-p07/server.mjs
packages/l1-p07/src/main.js
packages/l1-p07/styles.css
packages/l1-p07/tests/config.json
packages/l1-p07/tests/layout.jest.test.cjs
packages/l1-p07/tests/layout.vitest.test.ts
packages/l1-p07/vitest.config.ts
packages/l1-p08/README.md
packages/l1-p08/jest.config.cjs
packages/l1-p08/package.json
packages/l1-p08/public/index.html
packages/l1-p08/server.mjs
packages/l1-p08/src/main.js
packages/l1-p08/styles.css
packages/l1-p08/tests/config.json
packages/l1-p08/tests/layout.jest.test.cjs
packages/l1-p08/tests/layout.vitest.test.ts
packages/l1-p08/vitest.config.ts
packages/l1-p09/README.md
packages/l1-p09/jest.config.cjs
packages/l1-p09/package.json
packages/l1-p09/public/index.html
packages/l1-p09/server.mjs
packages/l1-p09/src/main.js
packages/l1-p09/styles.css
packages/l1-p09/tests/config.json
packages/l1-p09/tests/layout.jest.test.cjs
packages/l1-p09/tests/layout.vitest.test.ts
packages/l1-p09/vitest.config.ts
packages/l1-p10/README.md
packages/l1-p10/jest.config.cjs
packages/l1-p10/package.json
packages/l1-p10/public/index.html
packages/l1-p10/server.mjs
packages/l1-p10/src/main.js
packages/l1-p10/styles.css
packages/l1-p10/tests/config.json
packages/l1-p10/tests/layout.jest.test.cjs
packages/l1-p10/tests/layout.vitest.test.ts
packages/l1-p10/vitest.config.ts
packages/l1-p11/README.md
packages/l1-p11/jest.config.cjs
packages/l1-p11/package.json
packages/l1-p11/public/index.html
packages/l1-p11/server.mjs
packages/l1-p11/src/main.js
packages/l1-p11/styles.css
packages/l1-p11/tests/config.json
packages/l1-p11/tests/layout.jest.test.cjs
packages/l1-p11/tests/layout.vitest.test.ts
packages/l1-p11/vitest.config.ts
packages/l1-p12/README.md
packages/l1-p12/jest.config.cjs
packages/l1-p12/package.json
packages/l1-p12/public/index.html
packages/l1-p12/server.mjs
packages/l1-p12/src/main.js
packages/l1-p12/styles.css
packages/l1-p12/tests/config.json
packages/l1-p12/tests/layout.jest.test.cjs
packages/l1-p12/tests/layout.vitest.test.ts
packages/l1-p12/vitest.config.ts
packages/l1-p13/README.md
packages/l1-p13/jest.config.cjs
packages/l1-p13/package.json
packages/l1-p13/public/index.html
packages/l1-p13/server.mjs
packages/l1-p13/src/main.js
packages/l1-p13/styles.css
packages/l1-p13/tests/config.json
packages/l1-p13/tests/layout.jest.test.cjs
packages/l1-p13/tests/layout.vitest.test.ts
packages/l1-p13/vitest.config.ts
packages/l1-p14/README.md
packages/l1-p14/jest.config.cjs
packages/l1-p14/package.json
packages/l1-p14/public/index.html
packages/l1-p14/server.mjs
packages/l1-p14/src/main.js
packages/l1-p14/styles.css
packages/l1-p14/tests/config.json
packages/l1-p14/tests/layout.jest.test.cjs
packages/l1-p14/tests/layout.vitest.test.ts
packages/l1-p14/vitest.config.ts
packages/l1-p15/README.md
packages/l1-p15/jest.config.cjs
packages/l1-p15/package.json
packages/l1-p15/public/index.html
packages/l1-p15/server.mjs
packages/l1-p15/src/main.js
packages/l1-p15/styles.css
packages/l1-p15/tests/config.json
packages/l1-p15/tests/layout.jest.test.cjs
packages/l1-p15/tests/layout.vitest.test.ts
packages/l1-p15/vitest.config.ts
packages/l2-p01/README.md
packages/l2-p01/jest.config.cjs
packages/l2-p01/package.json
packages/l2-p01/public/index.html
packages/l2-p01/server.mjs
packages/l2-p01/src/main.js
packages/l2-p01/styles.css
packages/l2-p01/tests/config.json
packages/l2-p01/tests/layout.jest.test.cjs
packages/l2-p01/tests/layout.vitest.test.ts
packages/l2-p01/vitest.config.ts
packages/l2-p02/README.md
packages/l2-p02/jest.config.cjs
packages/l2-p02/package.json
packages/l2-p02/public/index.html
packages/l2-p02/server.mjs
packages/l2-p02/src/main.js
packages/l2-p02/styles.css
packages/l2-p02/tests/config.json
packages/l2-p02/tests/layout.jest.test.cjs
packages/l2-p02/tests/layout.vitest.test.ts
packages/l2-p02/vitest.config.ts
packages/l2-p03/README.md
packages/l2-p03/jest.config.cjs
packages/l2-p03/package.json
packages/l2-p03/public/index.html
packages/l2-p03/server.mjs
packages/l2-p03/src/main.js
packages/l2-p03/styles.css
packages/l2-p03/tests/config.json
packages/l2-p03/tests/layout.jest.test.cjs
packages/l2-p03/tests/layout.vitest.test.ts
packages/l2-p03/vitest.config.ts
packages/l2-p04/README.md
packages/l2-p04/jest.config.cjs
packages/l2-p04/package.json
packages/l2-p04/public/index.html
packages/l2-p04/server.mjs
packages/l2-p04/src/main.js
packages/l2-p04/styles.css
packages/l2-p04/tests/config.json
packages/l2-p04/tests/layout.jest.test.cjs
packages/l2-p04/tests/layout.vitest.test.ts
packages/l2-p04/vitest.config.ts
packages/l2-p05/README.md
packages/l2-p05/jest.config.cjs
packages/l2-p05/package.json
packages/l2-p05/public/index.html
packages/l2-p05/server.mjs
packages/l2-p05/src/main.js
packages/l2-p05/styles.css
packages/l2-p05/tests/config.json
packages/l2-p05/tests/layout.jest.test.cjs
packages/l2-p05/tests/layout.vitest.test.ts
packages/l2-p05/vitest.config.ts
packages/l2-p06/README.md
packages/l2-p06/jest.config.cjs
packages/l2-p06/package.json
packages/l2-p06/public/index.html
packages/l2-p06/server.mjs
packages/l2-p06/src/main.js
packages/l2-p06/styles.css
packages/l2-p06/tests/config.json
packages/l2-p06/tests/layout.jest.test.cjs
packages/l2-p06/tests/layout.vitest.test.ts
packages/l2-p06/vitest.config.ts
packages/l2-p07/README.md
packages/l2-p07/jest.config.cjs
packages/l2-p07/package.json
packages/l2-p07/public/index.html
packages/l2-p07/server.mjs
packages/l2-p07/src/main.js
packages/l2-p07/styles.css
packages/l2-p07/tests/config.json
packages/l2-p07/tests/layout.jest.test.cjs
packages/l2-p07/tests/layout.vitest.test.ts
packages/l2-p07/vitest.config.ts
packages/l2-p08/README.md
packages/l2-p08/jest.config.cjs
packages/l2-p08/package.json
packages/l2-p08/public/index.html
packages/l2-p08/server.mjs
packages/l2-p08/src/main.js
packages/l2-p08/styles.css
packages/l2-p08/tests/config.json
packages/l2-p08/tests/layout.jest.test.cjs
packages/l2-p08/tests/layout.vitest.test.ts
packages/l2-p08/vitest.config.ts
packages/l2-p09/README.md
packages/l2-p09/jest.config.cjs
packages/l2-p09/package.json
packages/l2-p09/public/index.html
packages/l2-p09/server.mjs
packages/l2-p09/src/main.js
packages/l2-p09/styles.css
packages/l2-p09/tests/config.json
packages/l2-p09/tests/layout.jest.test.cjs
packages/l2-p09/tests/layout.vitest.test.ts
packages/l2-p09/vitest.config.ts
packages/l2-p10/README.md
packages/l2-p10/jest.config.cjs
packages/l2-p10/package.json
packages/l2-p10/public/index.html
packages/l2-p10/server.mjs
packages/l2-p10/src/main.js
packages/l2-p10/styles.css
packages/l2-p10/tests/config.json
packages/l2-p10/tests/layout.jest.test.cjs
packages/l2-p10/tests/layout.vitest.test.ts
packages/l2-p10/vitest.config.ts
packages/l2-p11/README.md
packages/l2-p11/jest.config.cjs
packages/l2-p11/package.json
packages/l2-p11/public/index.html
packages/l2-p11/server.mjs
packages/l2-p11/src/main.js
packages/l2-p11/styles.css
packages/l2-p11/tests/config.json
packages/l2-p11/tests/layout.jest.test.cjs
packages/l2-p11/tests/layout.vitest.test.ts
packages/l2-p11/vitest.config.ts
packages/l2-p12/README.md
packages/l2-p12/jest.config.cjs
packages/l2-p12/package.json
packages/l2-p12/public/index.html
packages/l2-p12/server.mjs
packages/l2-p12/src/main.js
packages/l2-p12/styles.css
packages/l2-p12/tests/config.json
packages/l2-p12/tests/layout.jest.test.cjs
packages/l2-p12/tests/layout.vitest.test.ts
packages/l2-p12/vitest.config.ts
packages/l2-p13/README.md
packages/l2-p13/jest.config.cjs
packages/l2-p13/package.json
packages/l2-p13/public/index.html
packages/l2-p13/server.mjs
packages/l2-p13/src/main.js
packages/l2-p13/styles.css
packages/l2-p13/tests/config.json
packages/l2-p13/tests/layout.jest.test.cjs
packages/l2-p13/tests/layout.vitest.test.ts
packages/l2-p13/vitest.config.ts
packages/l2-p14/README.md
packages/l2-p14/jest.config.cjs
packages/l2-p14/package.json
packages/l2-p14/public/index.html
packages/l2-p14/server.mjs
packages/l2-p14/src/main.js
packages/l2-p14/styles.css
packages/l2-p14/tests/config.json
packages/l2-p14/tests/layout.jest.test.cjs
packages/l2-p14/tests/layout.vitest.test.ts
packages/l2-p14/vitest.config.ts
packages/l2-p15/README.md
packages/l2-p15/jest.config.cjs
packages/l2-p15/package.json
packages/l2-p15/public/index.html
packages/l2-p15/server.mjs
packages/l2-p15/src/main.js
packages/l2-p15/styles.css
packages/l2-p15/tests/config.json
packages/l2-p15/tests/layout.jest.test.cjs
packages/l2-p15/tests/layout.vitest.test.ts
packages/l2-p15/vitest.config.ts
packages/l3-p01/README.md
packages/l3-p01/jest.config.cjs
packages/l3-p01/package.json
packages/l3-p01/public/index.html
packages/l3-p01/server.mjs
packages/l3-p01/src/main.js
packages/l3-p01/styles.css
packages/l3-p01/tests/config.json
packages/l3-p01/tests/layout.jest.test.cjs
packages/l3-p01/tests/layout.vitest.test.ts
packages/l3-p01/vitest.config.ts
packages/l3-p02/README.md
packages/l3-p02/jest.config.cjs
packages/l3-p02/package.json
packages/l3-p02/public/index.html
packages/l3-p02/server.mjs
packages/l3-p02/src/main.js
packages/l3-p02/styles.css
packages/l3-p02/tests/config.json
packages/l3-p02/tests/layout.jest.test.cjs
packages/l3-p02/tests/layout.vitest.test.ts
packages/l3-p02/vitest.config.ts
packages/l3-p03/README.md
packages/l3-p03/jest.config.cjs
packages/l3-p03/package.json
packages/l3-p03/public/index.html
packages/l3-p03/server.mjs
packages/l3-p03/src/main.js
packages/l3-p03/styles.css
packages/l3-p03/tests/config.json
packages/l3-p03/tests/layout.jest.test.cjs
packages/l3-p03/tests/layout.vitest.test.ts
packages/l3-p03/vitest.config.ts
packages/l3-p04/README.md
packages/l3-p04/jest.config.cjs
packages/l3-p04/package.json
packages/l3-p04/public/index.html
packages/l3-p04/server.mjs
packages/l3-p04/src/main.js
packages/l3-p04/styles.css
packages/l3-p04/tests/config.json
packages/l3-p04/tests/layout.jest.test.cjs
packages/l3-p04/tests/layout.vitest.test.ts
packages/l3-p04/vitest.config.ts
packages/l3-p05/README.md
packages/l3-p05/jest.config.cjs
packages/l3-p05/package.json
packages/l3-p05/public/index.html
packages/l3-p05/server.mjs
packages/l3-p05/src/main.js
packages/l3-p05/styles.css
packages/l3-p05/tests/config.json
packages/l3-p05/tests/layout.jest.test.cjs
packages/l3-p05/tests/layout.vitest.test.ts
packages/l3-p05/vitest.config.ts
packages/l3-p06/README.md
packages/l3-p06/jest.config.cjs
packages/l3-p06/package.json
packages/l3-p06/public/index.html
packages/l3-p06/server.mjs
packages/l3-p06/src/main.js
packages/l3-p06/styles.css
packages/l3-p06/tests/config.json
packages/l3-p06/tests/layout.jest.test.cjs
packages/l3-p06/tests/layout.vitest.test.ts
packages/l3-p06/vitest.config.ts
packages/l3-p07/README.md
packages/l3-p07/jest.config.cjs
packages/l3-p07/package.json
packages/l3-p07/public/index.html
packages/l3-p07/server.mjs
packages/l3-p07/src/main.js
packages/l3-p07/styles.css
packages/l3-p07/tests/config.json
packages/l3-p07/tests/layout.jest.test.cjs
packages/l3-p07/tests/layout.vitest.test.ts
packages/l3-p07/vitest.config.ts
packages/l3-p08/README.md
packages/l3-p08/jest.config.cjs
packages/l3-p08/package.json
packages/l3-p08/public/index.html
packages/l3-p08/server.mjs
packages/l3-p08/src/main.js
packages/l3-p08/styles.css
packages/l3-p08/tests/config.json
packages/l3-p08/tests/layout.jest.test.cjs
packages/l3-p08/tests/layout.vitest.test.ts
packages/l3-p08/vitest.config.ts
packages/l3-p09/README.md
packages/l3-p09/jest.config.cjs
packages/l3-p09/package.json
packages/l3-p09/public/index.html
packages/l3-p09/server.mjs
packages/l3-p09/src/main.js
packages/l3-p09/styles.css
packages/l3-p09/tests/config.json
packages/l3-p09/tests/layout.jest.test.cjs
packages/l3-p09/tests/layout.vitest.test.ts
packages/l3-p09/vitest.config.ts
packages/l3-p10/README.md
packages/l3-p10/jest.config.cjs
packages/l3-p10/package.json
packages/l3-p10/public/index.html
packages/l3-p10/server.mjs
packages/l3-p10/src/main.js
packages/l3-p10/styles.css
packages/l3-p10/tests/config.json
packages/l3-p10/tests/layout.jest.test.cjs
packages/l3-p10/tests/layout.vitest.test.ts
packages/l3-p10/vitest.config.ts
packages/l3-p11/README.md
packages/l3-p11/jest.config.cjs
packages/l3-p11/package.json
packages/l3-p11/public/index.html
packages/l3-p11/server.mjs
packages/l3-p11/src/main.js
packages/l3-p11/styles.css
packages/l3-p11/tests/config.json
packages/l3-p11/tests/layout.jest.test.cjs
packages/l3-p11/tests/layout.vitest.test.ts
packages/l3-p11/vitest.config.ts
packages/l3-p12/README.md
packages/l3-p12/jest.config.cjs
packages/l3-p12/package.json
packages/l3-p12/public/index.html
packages/l3-p12/server.mjs
packages/l3-p12/src/main.js
packages/l3-p12/styles.css
packages/l3-p12/tests/config.json
packages/l3-p12/tests/layout.jest.test.cjs
packages/l3-p12/tests/layout.vitest.test.ts
packages/l3-p12/vitest.config.ts
packages/l3-p13/README.md
packages/l3-p13/jest.config.cjs
packages/l3-p13/package.json
packages/l3-p13/public/index.html
packages/l3-p13/server.mjs
packages/l3-p13/src/main.js
packages/l3-p13/styles.css
packages/l3-p13/tests/config.json
packages/l3-p13/tests/layout.jest.test.cjs
packages/l3-p13/tests/layout.vitest.test.ts
packages/l3-p13/vitest.config.ts
packages/l3-p14/README.md
packages/l3-p14/jest.config.cjs
packages/l3-p14/package.json
packages/l3-p14/public/index.html
packages/l3-p14/server.mjs
packages/l3-p14/src/main.js
packages/l3-p14/styles.css
packages/l3-p14/tests/config.json
packages/l3-p14/tests/layout.jest.test.cjs
packages/l3-p14/tests/layout.vitest.test.ts
packages/l3-p14/vitest.config.ts
packages/l3-p15/README.md
packages/l3-p15/jest.config.cjs
packages/l3-p15/package.json
packages/l3-p15/public/index.html
packages/l3-p15/server.mjs
packages/l3-p15/src/main.js
packages/l3-p15/styles.css
packages/l3-p15/tests/config.json
packages/l3-p15/tests/layout.jest.test.cjs
packages/l3-p15/tests/layout.vitest.test.ts
packages/l3-p15/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 182, other: 45, docs: 45, public: 45, code: 45, tests: 135.

**package.json — sinteză (scripturi, workspaces, dependențe)**

- `package.json`: name=`s6p3-monorepo` type=`module` workspaces=True
  - **Scripturi:**
  - `test:vitest` → `pnpm -r --filter ./packages run test:vitest`
  - `test:jest` → `pnpm -r --filter ./packages run test:jest`
  - `test` → `pnpm -r --filter ./packages run test`
  - `dev` → `echo 'rulează dev per pachet: pnpm --filter <pkg> run dev'`
  - **Deps:** 
  - **DevDeps:** pnpm, vitest, jest, jsdom, express
- `packages/l1-p01/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p02/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p03/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p04/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p05/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p06/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p07/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p08/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p09/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p10/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p11/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p12/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p13/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p14/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p15/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p01/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p02/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p03/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p04/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p05/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p06/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p07/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p08/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p09/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p10/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p11/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p12/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p13/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p14/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p15/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p01/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p02/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p03/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p04/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p05/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p06/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p07/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p08/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p09/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p10/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p11/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p12/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p13/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p14/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p15/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom

### Seminar6_Partea3_standalone.zip

```
l1-p01/README.md
l1-p01/jest.config.cjs
l1-p01/package.json
l1-p01/public/index.html
l1-p01/server.mjs
l1-p01/src/main.js
l1-p01/styles.css
l1-p01/tests/config.json
l1-p01/tests/layout.jest.test.cjs
l1-p01/tests/layout.vitest.test.ts
l1-p01/vitest.config.ts
l1-p02/README.md
l1-p02/jest.config.cjs
l1-p02/package.json
l1-p02/public/index.html
l1-p02/server.mjs
l1-p02/src/main.js
l1-p02/styles.css
l1-p02/tests/config.json
l1-p02/tests/layout.jest.test.cjs
l1-p02/tests/layout.vitest.test.ts
l1-p02/vitest.config.ts
l1-p03/README.md
l1-p03/jest.config.cjs
l1-p03/package.json
l1-p03/public/index.html
l1-p03/server.mjs
l1-p03/src/main.js
l1-p03/styles.css
l1-p03/tests/config.json
l1-p03/tests/layout.jest.test.cjs
l1-p03/tests/layout.vitest.test.ts
l1-p03/vitest.config.ts
l1-p04/README.md
l1-p04/jest.config.cjs
l1-p04/package.json
l1-p04/public/index.html
l1-p04/server.mjs
l1-p04/src/main.js
l1-p04/styles.css
l1-p04/tests/config.json
l1-p04/tests/layout.jest.test.cjs
l1-p04/tests/layout.vitest.test.ts
l1-p04/vitest.config.ts
l1-p05/README.md
l1-p05/jest.config.cjs
l1-p05/package.json
l1-p05/public/index.html
l1-p05/server.mjs
l1-p05/src/main.js
l1-p05/styles.css
l1-p05/tests/config.json
l1-p05/tests/layout.jest.test.cjs
l1-p05/tests/layout.vitest.test.ts
l1-p05/vitest.config.ts
l1-p06/README.md
l1-p06/jest.config.cjs
l1-p06/package.json
l1-p06/public/index.html
l1-p06/server.mjs
l1-p06/src/main.js
l1-p06/styles.css
l1-p06/tests/config.json
l1-p06/tests/layout.jest.test.cjs
l1-p06/tests/layout.vitest.test.ts
l1-p06/vitest.config.ts
l1-p07/README.md
l1-p07/jest.config.cjs
l1-p07/package.json
l1-p07/public/index.html
l1-p07/server.mjs
l1-p07/src/main.js
l1-p07/styles.css
l1-p07/tests/config.json
l1-p07/tests/layout.jest.test.cjs
l1-p07/tests/layout.vitest.test.ts
l1-p07/vitest.config.ts
l1-p08/README.md
l1-p08/jest.config.cjs
l1-p08/package.json
l1-p08/public/index.html
l1-p08/server.mjs
l1-p08/src/main.js
l1-p08/styles.css
l1-p08/tests/config.json
l1-p08/tests/layout.jest.test.cjs
l1-p08/tests/layout.vitest.test.ts
l1-p08/vitest.config.ts
l1-p09/README.md
l1-p09/jest.config.cjs
l1-p09/package.json
l1-p09/public/index.html
l1-p09/server.mjs
l1-p09/src/main.js
l1-p09/styles.css
l1-p09/tests/config.json
l1-p09/tests/layout.jest.test.cjs
l1-p09/tests/layout.vitest.test.ts
l1-p09/vitest.config.ts
l1-p10/README.md
l1-p10/jest.config.cjs
l1-p10/package.json
l1-p10/public/index.html
l1-p10/server.mjs
l1-p10/src/main.js
l1-p10/styles.css
l1-p10/tests/config.json
l1-p10/tests/layout.jest.test.cjs
l1-p10/tests/layout.vitest.test.ts
l1-p10/vitest.config.ts
l1-p11/README.md
l1-p11/jest.config.cjs
l1-p11/package.json
l1-p11/public/index.html
l1-p11/server.mjs
l1-p11/src/main.js
l1-p11/styles.css
l1-p11/tests/config.json
l1-p11/tests/layout.jest.test.cjs
l1-p11/tests/layout.vitest.test.ts
l1-p11/vitest.config.ts
l1-p12/README.md
l1-p12/jest.config.cjs
l1-p12/package.json
l1-p12/public/index.html
l1-p12/server.mjs
l1-p12/src/main.js
l1-p12/styles.css
l1-p12/tests/config.json
l1-p12/tests/layout.jest.test.cjs
l1-p12/tests/layout.vitest.test.ts
l1-p12/vitest.config.ts
l1-p13/README.md
l1-p13/jest.config.cjs
l1-p13/package.json
l1-p13/public/index.html
l1-p13/server.mjs
l1-p13/src/main.js
l1-p13/styles.css
l1-p13/tests/config.json
l1-p13/tests/layout.jest.test.cjs
l1-p13/tests/layout.vitest.test.ts
l1-p13/vitest.config.ts
l1-p14/README.md
l1-p14/jest.config.cjs
l1-p14/package.json
l1-p14/public/index.html
l1-p14/server.mjs
l1-p14/src/main.js
l1-p14/styles.css
l1-p14/tests/config.json
l1-p14/tests/layout.jest.test.cjs
l1-p14/tests/layout.vitest.test.ts
l1-p14/vitest.config.ts
l1-p15/README.md
l1-p15/jest.config.cjs
l1-p15/package.json
l1-p15/public/index.html
l1-p15/server.mjs
l1-p15/src/main.js
l1-p15/styles.css
l1-p15/tests/config.json
l1-p15/tests/layout.jest.test.cjs
l1-p15/tests/layout.vitest.test.ts
l1-p15/vitest.config.ts
l2-p01/README.md
l2-p01/jest.config.cjs
l2-p01/package.json
l2-p01/public/index.html
l2-p01/server.mjs
l2-p01/src/main.js
l2-p01/styles.css
l2-p01/tests/config.json
l2-p01/tests/layout.jest.test.cjs
l2-p01/tests/layout.vitest.test.ts
l2-p01/vitest.config.ts
l2-p02/README.md
l2-p02/jest.config.cjs
l2-p02/package.json
l2-p02/public/index.html
l2-p02/server.mjs
l2-p02/src/main.js
l2-p02/styles.css
l2-p02/tests/config.json
l2-p02/tests/layout.jest.test.cjs
l2-p02/tests/layout.vitest.test.ts
l2-p02/vitest.config.ts
l2-p03/README.md
l2-p03/jest.config.cjs
l2-p03/package.json
l2-p03/public/index.html
l2-p03/server.mjs
l2-p03/src/main.js
l2-p03/styles.css
l2-p03/tests/config.json
l2-p03/tests/layout.jest.test.cjs
l2-p03/tests/layout.vitest.test.ts
l2-p03/vitest.config.ts
l2-p04/README.md
l2-p04/jest.config.cjs
l2-p04/package.json
l2-p04/public/index.html
l2-p04/server.mjs
l2-p04/src/main.js
l2-p04/styles.css
l2-p04/tests/config.json
l2-p04/tests/layout.jest.test.cjs
l2-p04/tests/layout.vitest.test.ts
l2-p04/vitest.config.ts
l2-p05/README.md
l2-p05/jest.config.cjs
l2-p05/package.json
l2-p05/public/index.html
l2-p05/server.mjs
l2-p05/src/main.js
l2-p05/styles.css
l2-p05/tests/config.json
l2-p05/tests/layout.jest.test.cjs
l2-p05/tests/layout.vitest.test.ts
l2-p05/vitest.config.ts
l2-p06/README.md
l2-p06/jest.config.cjs
l2-p06/package.json
l2-p06/public/index.html
l2-p06/server.mjs
l2-p06/src/main.js
l2-p06/styles.css
l2-p06/tests/config.json
l2-p06/tests/layout.jest.test.cjs
l2-p06/tests/layout.vitest.test.ts
l2-p06/vitest.config.ts
l2-p07/README.md
l2-p07/jest.config.cjs
l2-p07/package.json
l2-p07/public/index.html
l2-p07/server.mjs
l2-p07/src/main.js
l2-p07/styles.css
l2-p07/tests/config.json
l2-p07/tests/layout.jest.test.cjs
l2-p07/tests/layout.vitest.test.ts
l2-p07/vitest.config.ts
l2-p08/README.md
l2-p08/jest.config.cjs
l2-p08/package.json
l2-p08/public/index.html
l2-p08/server.mjs
l2-p08/src/main.js
l2-p08/styles.css
l2-p08/tests/config.json
l2-p08/tests/layout.jest.test.cjs
l2-p08/tests/layout.vitest.test.ts
l2-p08/vitest.config.ts
l2-p09/README.md
l2-p09/jest.config.cjs
l2-p09/package.json
l2-p09/public/index.html
l2-p09/server.mjs
l2-p09/src/main.js
l2-p09/styles.css
l2-p09/tests/config.json
l2-p09/tests/layout.jest.test.cjs
l2-p09/tests/layout.vitest.test.ts
l2-p09/vitest.config.ts
l2-p10/README.md
l2-p10/jest.config.cjs
l2-p10/package.json
l2-p10/public/index.html
l2-p10/server.mjs
l2-p10/src/main.js
l2-p10/styles.css
l2-p10/tests/config.json
l2-p10/tests/layout.jest.test.cjs
l2-p10/tests/layout.vitest.test.ts
l2-p10/vitest.config.ts
l2-p11/README.md
l2-p11/jest.config.cjs
l2-p11/package.json
l2-p11/public/index.html
l2-p11/server.mjs
l2-p11/src/main.js
l2-p11/styles.css
l2-p11/tests/config.json
l2-p11/tests/layout.jest.test.cjs
l2-p11/tests/layout.vitest.test.ts
l2-p11/vitest.config.ts
l2-p12/README.md
l2-p12/jest.config.cjs
l2-p12/package.json
l2-p12/public/index.html
l2-p12/server.mjs
l2-p12/src/main.js
l2-p12/styles.css
l2-p12/tests/config.json
l2-p12/tests/layout.jest.test.cjs
l2-p12/tests/layout.vitest.test.ts
l2-p12/vitest.config.ts
l2-p13/README.md
l2-p13/jest.config.cjs
l2-p13/package.json
l2-p13/public/index.html
l2-p13/server.mjs
l2-p13/src/main.js
l2-p13/styles.css
l2-p13/tests/config.json
l2-p13/tests/layout.jest.test.cjs
l2-p13/tests/layout.vitest.test.ts
l2-p13/vitest.config.ts
l2-p14/README.md
l2-p14/jest.config.cjs
l2-p14/package.json
l2-p14/public/index.html
l2-p14/server.mjs
l2-p14/src/main.js
l2-p14/styles.css
l2-p14/tests/config.json
l2-p14/tests/layout.jest.test.cjs
l2-p14/tests/layout.vitest.test.ts
l2-p14/vitest.config.ts
l2-p15/README.md
l2-p15/jest.config.cjs
l2-p15/package.json
l2-p15/public/index.html
l2-p15/server.mjs
l2-p15/src/main.js
l2-p15/styles.css
l2-p15/tests/config.json
l2-p15/tests/layout.jest.test.cjs
l2-p15/tests/layout.vitest.test.ts
l2-p15/vitest.config.ts
l3-p01/README.md
l3-p01/jest.config.cjs
l3-p01/package.json
l3-p01/public/index.html
l3-p01/server.mjs
l3-p01/src/main.js
l3-p01/styles.css
l3-p01/tests/config.json
l3-p01/tests/layout.jest.test.cjs
l3-p01/tests/layout.vitest.test.ts
l3-p01/vitest.config.ts
l3-p02/README.md
l3-p02/jest.config.cjs
l3-p02/package.json
l3-p02/public/index.html
l3-p02/server.mjs
l3-p02/src/main.js
l3-p02/styles.css
l3-p02/tests/config.json
l3-p02/tests/layout.jest.test.cjs
l3-p02/tests/layout.vitest.test.ts
l3-p02/vitest.config.ts
l3-p03/README.md
l3-p03/jest.config.cjs
l3-p03/package.json
l3-p03/public/index.html
l3-p03/server.mjs
l3-p03/src/main.js
l3-p03/styles.css
l3-p03/tests/config.json
l3-p03/tests/layout.jest.test.cjs
l3-p03/tests/layout.vitest.test.ts
l3-p03/vitest.config.ts
l3-p04/README.md
l3-p04/jest.config.cjs
l3-p04/package.json
l3-p04/public/index.html
l3-p04/server.mjs
l3-p04/src/main.js
l3-p04/styles.css
l3-p04/tests/config.json
l3-p04/tests/layout.jest.test.cjs
l3-p04/tests/layout.vitest.test.ts
l3-p04/vitest.config.ts
l3-p05/README.md
l3-p05/jest.config.cjs
l3-p05/package.json
l3-p05/public/index.html
l3-p05/server.mjs
l3-p05/src/main.js
l3-p05/styles.css
l3-p05/tests/config.json
l3-p05/tests/layout.jest.test.cjs
l3-p05/tests/layout.vitest.test.ts
l3-p05/vitest.config.ts
l3-p06/README.md
l3-p06/jest.config.cjs
l3-p06/package.json
l3-p06/public/index.html
l3-p06/server.mjs
l3-p06/src/main.js
l3-p06/styles.css
l3-p06/tests/config.json
l3-p06/tests/layout.jest.test.cjs
l3-p06/tests/layout.vitest.test.ts
l3-p06/vitest.config.ts
l3-p07/README.md
l3-p07/jest.config.cjs
l3-p07/package.json
l3-p07/public/index.html
l3-p07/server.mjs
l3-p07/src/main.js
l3-p07/styles.css
l3-p07/tests/config.json
l3-p07/tests/layout.jest.test.cjs
l3-p07/tests/layout.vitest.test.ts
l3-p07/vitest.config.ts
l3-p08/README.md
l3-p08/jest.config.cjs
l3-p08/package.json
l3-p08/public/index.html
l3-p08/server.mjs
l3-p08/src/main.js
l3-p08/styles.css
l3-p08/tests/config.json
l3-p08/tests/layout.jest.test.cjs
l3-p08/tests/layout.vitest.test.ts
l3-p08/vitest.config.ts
l3-p09/README.md
l3-p09/jest.config.cjs
l3-p09/package.json
l3-p09/public/index.html
l3-p09/server.mjs
l3-p09/src/main.js
l3-p09/styles.css
l3-p09/tests/config.json
l3-p09/tests/layout.jest.test.cjs
l3-p09/tests/layout.vitest.test.ts
l3-p09/vitest.config.ts
l3-p10/README.md
l3-p10/jest.config.cjs
l3-p10/package.json
l3-p10/public/index.html
l3-p10/server.mjs
l3-p10/src/main.js
l3-p10/styles.css
l3-p10/tests/config.json
l3-p10/tests/layout.jest.test.cjs
l3-p10/tests/layout.vitest.test.ts
l3-p10/vitest.config.ts
l3-p11/README.md
l3-p11/jest.config.cjs
l3-p11/package.json
l3-p11/public/index.html
l3-p11/server.mjs
l3-p11/src/main.js
l3-p11/styles.css
l3-p11/tests/config.json
l3-p11/tests/layout.jest.test.cjs
l3-p11/tests/layout.vitest.test.ts
l3-p11/vitest.config.ts
l3-p12/README.md
l3-p12/jest.config.cjs
l3-p12/package.json
l3-p12/public/index.html
l3-p12/server.mjs
l3-p12/src/main.js
l3-p12/styles.css
l3-p12/tests/config.json
l3-p12/tests/layout.jest.test.cjs
l3-p12/tests/layout.vitest.test.ts
l3-p12/vitest.config.ts
l3-p13/README.md
l3-p13/jest.config.cjs
l3-p13/package.json
l3-p13/public/index.html
l3-p13/server.mjs
l3-p13/src/main.js
l3-p13/styles.css
l3-p13/tests/config.json
l3-p13/tests/layout.jest.test.cjs
l3-p13/tests/layout.vitest.test.ts
l3-p13/vitest.config.ts
l3-p14/README.md
l3-p14/jest.config.cjs
l3-p14/package.json
l3-p14/public/index.html
l3-p14/server.mjs
l3-p14/src/main.js
l3-p14/styles.css
l3-p14/tests/config.json
l3-p14/tests/layout.jest.test.cjs
l3-p14/tests/layout.vitest.test.ts
l3-p14/vitest.config.ts
l3-p15/README.md
l3-p15/jest.config.cjs
l3-p15/package.json
l3-p15/public/index.html
l3-p15/server.mjs
l3-p15/src/main.js
l3-p15/styles.css
l3-p15/tests/config.json
l3-p15/tests/layout.jest.test.cjs
l3-p15/tests/layout.vitest.test.ts
l3-p15/vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** other: 45, config: 180, docs: 45, public: 45, code: 45, tests: 135.

**package.json — sinteză (scripturi, workspaces, dependențe)**

- `l1-p01/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p02/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p03/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p04/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p05/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p06/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p07/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p08/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p09/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p10/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p11/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p12/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p13/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p14/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p15/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p01/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p02/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p03/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p04/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p05/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p06/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p07/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p08/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p09/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p10/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p11/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p12/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p13/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p14/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p15/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p01/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p02/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p03/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p04/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p05/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p06/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p07/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p08/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p09/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p10/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p11/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p12/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p13/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p14/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p15/package.json`: name=`s6p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom

### Seminar6_Partea3_READMEs.zip

```
l1-p01/README.md
l1-p02/README.md
l1-p03/README.md
l1-p04/README.md
l1-p05/README.md
l1-p06/README.md
l1-p07/README.md
l1-p08/README.md
l1-p09/README.md
l1-p10/README.md
l1-p11/README.md
l1-p12/README.md
l1-p13/README.md
l1-p14/README.md
l1-p15/README.md
l2-p01/README.md
l2-p02/README.md
l2-p03/README.md
l2-p04/README.md
l2-p05/README.md
l2-p06/README.md
l2-p07/README.md
l2-p08/README.md
l2-p09/README.md
l2-p10/README.md
l2-p11/README.md
l2-p12/README.md
l2-p13/README.md
l2-p14/README.md
l2-p15/README.md
l3-p01/README.md
l3-p02/README.md
l3-p03/README.md
l3-p04/README.md
l3-p05/README.md
l3-p06/README.md
l3-p07/README.md
l3-p08/README.md
l3-p09/README.md
l3-p10/README.md
l3-p11/README.md
l3-p12/README.md
l3-p13/README.md
l3-p14/README.md
l3-p15/README.md
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** docs: 45.

## 2. Sinteza documentelor (teorie ↔ laborator ↔ proiecte)

### Seminar6_Partea1_Teorie.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 6 — CSS Layout & Media Queries
Partea 1: Teorie (extins)
- Hook realist: patru ecrane, un singur CSS (de la telefon la panou 4K)
- La ora 08:00 primești o cerință: până la prânz trebuie să publici o pagină de prezentare pentru „Clubs & Associations Hub”. Va rula pe patru tipuri de ecrane aflate în campus: telefoane mici (320–400 px), tablete (≈768–1024 px), laptopuri de laborator (≈1280 px) și un panou 4K din hol. Nu ai voie framework‑uri; trebuie să livrezi doar cu **CSS**: **Flexbox**, **Grid**, **media queries**, imagini nedistorsionate, spațiere coerentă și tipografie lizibilă. Nu există timp pentru „încercări norocoase” („pixel pushing”), ci doar pentru decizii bune, reproductibile.
În acest seminar învățăm să gândim layout‑ul „de jos în sus” (**mobile‑first**), cu reguli stabile, **unități fluide** și **funcții CSS** moderne, să alegem **breakpoints** în funcție de conținut (nu de „device marketing”) și să combinăm **Flexbox** cu **Grid** în mod sistematic. Vom lega deciziile de principii HCI (ergonomie, viteză de scanare vizuală) și vom include „micro‑tooling” mental: checklist‑uri, convenții de denumire și teste automate care confirmă practicile implementate.

### Seminar6_Partea2_Laborator.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 6 — CSS Layout & Media Queries
Partea 2: Laborator (extins)
- Context, obiective și rezultat așteptat
- În Partea 2 construim, pas cu pas, o interfață **responsive** pentru „Clubs & Associations Hub” folosind **Flexbox**, **CSS Grid** și **media queries** alese după **conținut**, nu după dispozitive. Scopul este să obții un layout stabil de la 320px la 4K, cu o **scară tipografică fluidă** (`clamp()`), imagini cu **raport 4:3** (`aspect-ratio`) și **cropping** corect (`object-fit: cover`). Practicăm „**mobile‑first**” + „**content‑out**” și verificăm convențiile prin **teste unitare** (Vitest & Jest) care caută prezența pattern‑urilor cheie în CSS/HTML.

### Seminar6_Partea2_README.md

**Titluri/Heading-uri (eșantion):**

- Seminarul 6 — Partea 2 (Laborator, extins)
- Rulare
- Checklist de predare (scurt)

**Headings principale (eșantion):**

- Seminarul 6 — Partea 2 (Laborator, extins)
- Rulare
- Checklist de predare (scurt)

**Idei cheie (liste):**

- **CSS Layout & Media Queries — Flexbox, Grid, responsive UI**
- **HTML**: `public/index.html`, `public/detail.html`
- **CSS**: `styles/{base,typography,layout,components,utilities}.css`
- **JS**: `src/main.js` (minim; layout-ul este CSS-driven)
- **Teste**: Vitest & Jest (jsdom) în `tests/unit`
- **Server**: `server.mjs` (Express) pentru previzualizare locală
- ✅ Cel puțin **3 media queries** (480 / 768 / 1200) — și opțional 1920 pentru panou
- ✅ **Grid** pentru listă de carduri cu `repeat(auto-fit, minmax(16rem, 1fr))`
- ✅ **Flex** cu `flex-wrap` și `gap` pentru nav/toolbars
- ✅ Imagini cu `aspect-ratio: 4/3` și `object-fit: cover`
- ✅ Tipografie fluidă cu `clamp()`
- ✅ Pagina de detaliu folosește **grid-template-areas**

### Seminar6_Partea3_Arhive_Ghid.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhivele Partea 3
- Ce conțin arhivele
- • **Standalone**: 45 proiecte (`l1-p01` … `l3-p15`), fiecare cu `public/index.html`, `styles.css`, `src/main.js`, `tests/` (Vitest+Jest), `vitest.config.ts`, `jest.config.cjs`, `server.mjs`, `package.json`, `README.md`.

### Seminar6_Partea3_Proiecte_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 6 — Partea 3: Proiecte/teme (extins)
- Viziune & metodologie
- Partea 3 propune **45 de proiecte** (15 × L1, 15 × L2, 15 × L3) orientate pe **CSS Layout & Media Queries** (Flexbox, Grid, responsive UI). Scopul este să antreneze gândirea „**mobile‑first** + **content‑out**” și selecția între **Flex (1D)** și **Grid (2D)**. Fiecare proiect include **Scop**, **Specificații**, **Criterii de acceptare** (măsurabile), **Soluție (rezumat)**, precum și **AI‑assist prompts (VSL)** pentru accelerare cu Copilot/LLM. Pachetele livrate conțin și **teste unitare** (Vitest + Jest) care verifică convențiile CSS/HTML (nu rezultatul vizual).

## 3. Monorepo vs. standalone — analiză comparativă


**Manageri de pachete & workspaces.** Monorepo (PNPM 9+) declară `packages/*` în `pnpm-workspace.yaml` și/sau `workspaces` în `package.json`, cu instalare la rădăcină (`pnpm i -w`). Standalone izolează dependențele per proiect (`npm i`).

**Comenzi de instalare/testare.** Monorepo: `pnpm -w run test` sau `pnpm --filter <pkg> run dev/test`. Standalone: `npm test`, `npm run dev`. Testele sunt **oglindite** (Vitest & Jest) și verifică **prezența convențiilor CSS/HTML** (nu stilul calculat), conform laboratorului.

**Integrare CI.** Monorepo agregă workflows (`.github/workflows/*`) pentru lint/unit/e2e (acolo unde e cazul), în timp ce standalone definește workflows simple per proiect.

**Avantaje/Dezavantaje.** Standalone — cognitiv mai simplu (ideal pentru începători). Monorepo — scalare pentru colecții mari (ex. 45 proiecte L1–L3), partajare de configuri și execuții rapide; costul este înțelegerea filtrării PNPM și a grafului de pachete.
## 4. Rolul fișierelor cheie (config, cod, teste, extra)

| Fișier / tip | Rol |
|---|---|
| `vitest.config.ts` | Configurarea Vitest (jsdom), include fișiere CSS/HTML în testele de convenție. |
| `jest.config.cjs` | Configurarea Jest (jsdom), aliniată cu suitele Vitest pentru oglindire. |
| `server.mjs` | Server Express minimal; servește fișierele statice `public/` și `styles/`. |
| `package.json` | Manifestul proiectului: metadate, dependențe, scripturi; definește rularea testelor Vitest/Jest. |
| `pnpm-workspace.yaml` | Declară pachetele din monorepo pentru PNPM. |
| `public/index.html` | Pagină „Home”: nav în Flex + listă carduri în Grid. |
| `public/detail.html` | Pagină „Club details”: layout cu `grid-template-areas`. |
| `styles/layout.css` | Flex + Grid + media queries content-based (480/768/1200/1920). |
| `styles/typography.css` | Scară tipografică fluidă cu `clamp()` (body/h2/h1). |

## 5. Corelații cod ↔ configurări ↔ teste


- **Layout CSS** (Flex/Grid/MQ) din `styles/*.css` este verificat prin **ambele suite** (Vitest & Jest) care caută expresii-cheie (`@media 480/768/1200`, `repeat(auto-fit, minmax(16rem,1fr))`, `flex-wrap: wrap`, `gap`, `aspect-ratio`, `object-fit`, `clamp()`). 
- **Serverul `server.mjs`** servește static din `public/` și `styles/`, permițând previzualizarea rapidă și un mediu determinist pentru teste. 
- **ESLint + CI**: workflows rânduiesc `lint` și `test`, blocând regresiile (nume BEM, fără `!important`, specificitate redusă). 
- **PWA/e2e (dacă sunt prezente)**: `playwright.config.ts` & `workbox-config.js` extind verificarea către navigare de fum (smoke) și precache (demo). 
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S6 antrenează construirea riguroasă a unei interfețe **responsive** fără framework‑uri, folosind **Flexbox**, **CSS Grid**, **media queries** justificate de conținut, **tipografie fluidă** cu `clamp()`, imagini cu **raport 4:3** (`aspect-ratio`) și **cropping** corect (`object-fit: cover`). Testarea este **duală** (Vitest & Jest) și validează **convenții** (nu randări), ceea ce susține coerența între teorie, laborator și proiecte (L1–L3).### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; rădăcină + `packages/*` |
| Instalare | `npm i` | `pnpm i -w` |
| Testare | `npm test` (Vitest & Jest) | `pnpm -w run test` sau `--filter <pkg>` |
| CI | Workflows simple per proiect | Workflows agregate, matrice pe pachete |
| Scalare (45 proiecte) | multiplicare directoare | pachete dedicate în `packages/*` |
| Public țintă | începători | colecții avansate / echipe |
### Inventar pe arhivă (roluri și observații)

- **Seminar6_Partea2_lab.zip** — config=4, docs=1, public=2, styles=5, code=1, tests=2.
- **Seminar6_Partea3_monorepo.zip** — config=182, other=45, docs=45, public=45, code=45, tests=135.
- **Seminar6_Partea3_standalone.zip** — other=45, config=180, docs=45, public=45, code=45, tests=135.
- **Seminar6_Partea3_READMEs.zip** — docs=45.
### Explicații fișier‑cu‑fișier

Consultați tabelul din §4. În plus, dacă apar fișiere `addons` (Playwright, Workbox/`sw.js`), acestea extind laboratorul cu e2e și PWA educațional.
### Corelații între fișiere


- `styles/layout.css` ↔ `tests/unit/*`: MQ la 480/768/1200 (±1920), Grid auto‑fit/minmax, Flex `wrap + gap`.  
- `styles/typography.css` ↔ `tests/unit/*`: `clamp()` pentru body/h2/h1.  
- `public/detail.html` ↔ `tests/unit/*`: `grid-template-areas` pentru pagina de detaliu.  
- `.github/workflows/*` ↔ lint/test: pipeline determinist pentru PR-uri.  
### Recomandări pentru studenți


1) **Porniți mobile‑first**: flux vertical curat fără MQ, apoi „relaxați” constrângerile cu Grid/Flex.  
2) **Folosiți unități fluide** și `clamp()` — MQ devin *tuning*, nu cârje.  
3) **Alegeți corect Flex vs. Grid** (1D vs. 2D); evitați lanțuri de selectori adânci.  
4) **Accesibilitate**: focus vizibil (`:focus-visible`), contrast adecvat, măsură de text 45–75ch.  
5) **Testați convențiile** cu ambele suite; păstrați structura fișierelor (`base/`, `layout/`, `components/`, `utilities/`).  
6) **CI ca gardian**: rulați `lint` + `test` înainte de push; evitați `!important`.  
### Instrucțiuni „Quick start” per arhivă


**Partea 2 — laborator (zip):**
```bash
unzip "Seminar6_Partea2_lab.zip" -d s6p2-lab
cd s6p2-lab
npm i
npm run dev           # http://localhost:5196 (servește public/ și styles/)
npm run test:vitest
npm run test:jest
npm test              # rulează ambele suite
```

**Partea 3 — monorepo (proiecte):**
```bash
unzip "Seminar6_Partea3_monorepo.zip" -d s6p3-monorepo
cd s6p3-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter ./packages/l1-p01 run dev
```

**Partea 3 — standalone (proiecte):**
```bash
unzip "Seminar6_Partea3_standalone.zip" -d s6p3-standalone
cd s6p3-standalone/l1-p01
npm i
npm test
npm run dev
```

**Partea 3 — README-uri agregate (referință rapidă):**
```bash
unzip "Seminar6_Partea3_READMEs.zip" -d s6p3-readmes
ls s6p3-readmes | head -n 10
```
### Troubleshooting (erori frecvente)


- **MQ lipsesc sau greșite** → verificați prezența `@media (min-width: 480px)`, `768px`, `1200px` (± `1920px`).  
- **Grid nu se ajustează fluid** → folosiți `repeat(auto-fit, minmax(16rem, 1fr))` și verificați suprascrieri ulterioare.  
- **Nav se „sparge” pe mobil** → adăugați `flex-wrap: wrap` & `gap`.  
- **Imagini deformate** → adăugați `aspect-ratio: 4/3` + `object-fit: cover`; reglați `object-position`.  
- **Text disproporționat pe extreme** → ajustați capetele `clamp()`; evitați `vw` pur.  
- **Jest ESM** → rulați cu `--experimental-vm-modules` sau configurați `babel-jest`.  
- **Port ocupat** → schimbați `PORT` în `server.mjs`.  
- **PNPM filter** → corectați `pnpm-workspace.yaml` și câmpul `name` în `package.json`.  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** — mobile‑first, content‑out, Flex vs. Grid, `clamp()`, `aspect-ratio`/`object-fit`, a11y & performanță.  
- **Partea 2 (Laborator)** — structură `public/` + `styles/`, teste pentru convenții CSS/HTML, server Express minimal.  
- **Partea 3 (Proiecte)** — 45 proiecte (L1–L3) cu specificații măsurabile și teste unitare (Vitest & Jest).  
### Prompt‑șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S6** (standalone & monorepo) o interfață responsive (Flex + Grid) cu MQ content‑based (480/768/1200 ±1920), tipografie fluidă cu `clamp()`, imagini 4:3 cu `object-fit: cover`, testare dublă **Vitest/Jest** a convențiilor CSS/HTML, CI, README cu Quick start & Troubleshooting, și variante **starter**/**solution**.”
