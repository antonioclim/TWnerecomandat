# Seminarul S5 — CSS Selectors & Layout (pseudo‑clase, form styling, grid 3×3) — Analiză integrată (standalone & monorepo)

*Generat la 2025-09-21 05:23.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar5_Partea2_starter.zip

```
jest.config.cjs
package.json
public/index.html
server.mjs
src/main.js
src/utils/dom.js
styles/base.css
styles/components.css
styles/forms.css
styles/layout.css
tests/unit/selectors.jest.test.mjs
tests/unit/selectors.vitest.test.ts
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 4, public: 1, styles: 4, code: 2, tests: 2.

**package.json — sinteză (scripturi, workspaces, dependențe)**

- `package.json`: name=`seminar5-part2-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom

### Seminar5_Partea3_monorepo.zip

```
package.json
packages/l1-p01/README.md
packages/l1-p01/jest.config.cjs
packages/l1-p01/package.json
packages/l1-p01/public/index.html
packages/l1-p01/server.mjs
packages/l1-p01/styles.css
packages/l1-p01/tests/config.json
packages/l1-p01/tests/selectors.jest.test.mjs
packages/l1-p01/tests/selectors.vitest.test.ts
packages/l1-p01/vitest.config.ts
packages/l1-p02/README.md
packages/l1-p02/jest.config.cjs
packages/l1-p02/package.json
packages/l1-p02/public/index.html
packages/l1-p02/server.mjs
packages/l1-p02/styles.css
packages/l1-p02/tests/config.json
packages/l1-p02/tests/selectors.jest.test.mjs
packages/l1-p02/tests/selectors.vitest.test.ts
packages/l1-p02/vitest.config.ts
packages/l1-p03/README.md
packages/l1-p03/jest.config.cjs
packages/l1-p03/package.json
packages/l1-p03/public/index.html
packages/l1-p03/server.mjs
packages/l1-p03/styles.css
packages/l1-p03/tests/config.json
packages/l1-p03/tests/selectors.jest.test.mjs
packages/l1-p03/tests/selectors.vitest.test.ts
packages/l1-p03/vitest.config.ts
packages/l1-p04/README.md
packages/l1-p04/jest.config.cjs
packages/l1-p04/package.json
packages/l1-p04/public/index.html
packages/l1-p04/server.mjs
packages/l1-p04/styles.css
packages/l1-p04/tests/config.json
packages/l1-p04/tests/selectors.jest.test.mjs
packages/l1-p04/tests/selectors.vitest.test.ts
packages/l1-p04/vitest.config.ts
packages/l1-p05/README.md
packages/l1-p05/jest.config.cjs
packages/l1-p05/package.json
packages/l1-p05/public/index.html
packages/l1-p05/server.mjs
packages/l1-p05/styles.css
packages/l1-p05/tests/config.json
packages/l1-p05/tests/selectors.jest.test.mjs
packages/l1-p05/tests/selectors.vitest.test.ts
packages/l1-p05/vitest.config.ts
packages/l1-p06/README.md
packages/l1-p06/jest.config.cjs
packages/l1-p06/package.json
packages/l1-p06/public/index.html
packages/l1-p06/server.mjs
packages/l1-p06/styles.css
packages/l1-p06/tests/config.json
packages/l1-p06/tests/selectors.jest.test.mjs
packages/l1-p06/tests/selectors.vitest.test.ts
packages/l1-p06/vitest.config.ts
packages/l1-p07/README.md
packages/l1-p07/jest.config.cjs
packages/l1-p07/package.json
packages/l1-p07/public/index.html
packages/l1-p07/server.mjs
packages/l1-p07/styles.css
packages/l1-p07/tests/config.json
packages/l1-p07/tests/selectors.jest.test.mjs
packages/l1-p07/tests/selectors.vitest.test.ts
packages/l1-p07/vitest.config.ts
packages/l1-p08/README.md
packages/l1-p08/jest.config.cjs
packages/l1-p08/package.json
packages/l1-p08/public/index.html
packages/l1-p08/server.mjs
packages/l1-p08/styles.css
packages/l1-p08/tests/config.json
packages/l1-p08/tests/selectors.jest.test.mjs
packages/l1-p08/tests/selectors.vitest.test.ts
packages/l1-p08/vitest.config.ts
packages/l1-p09/README.md
packages/l1-p09/jest.config.cjs
packages/l1-p09/package.json
packages/l1-p09/public/index.html
packages/l1-p09/server.mjs
packages/l1-p09/styles.css
packages/l1-p09/tests/config.json
packages/l1-p09/tests/selectors.jest.test.mjs
packages/l1-p09/tests/selectors.vitest.test.ts
packages/l1-p09/vitest.config.ts
packages/l1-p10/README.md
packages/l1-p10/jest.config.cjs
packages/l1-p10/package.json
packages/l1-p10/public/index.html
packages/l1-p10/server.mjs
packages/l1-p10/styles.css
packages/l1-p10/tests/config.json
packages/l1-p10/tests/selectors.jest.test.mjs
packages/l1-p10/tests/selectors.vitest.test.ts
packages/l1-p10/vitest.config.ts
packages/l1-p11/README.md
packages/l1-p11/jest.config.cjs
packages/l1-p11/package.json
packages/l1-p11/public/index.html
packages/l1-p11/server.mjs
packages/l1-p11/styles.css
packages/l1-p11/tests/config.json
packages/l1-p11/tests/selectors.jest.test.mjs
packages/l1-p11/tests/selectors.vitest.test.ts
packages/l1-p11/vitest.config.ts
packages/l1-p12/README.md
packages/l1-p12/jest.config.cjs
packages/l1-p12/package.json
packages/l1-p12/public/index.html
packages/l1-p12/server.mjs
packages/l1-p12/styles.css
packages/l1-p12/tests/config.json
packages/l1-p12/tests/selectors.jest.test.mjs
packages/l1-p12/tests/selectors.vitest.test.ts
packages/l1-p12/vitest.config.ts
packages/l1-p13/README.md
packages/l1-p13/jest.config.cjs
packages/l1-p13/package.json
packages/l1-p13/public/index.html
packages/l1-p13/server.mjs
packages/l1-p13/styles.css
packages/l1-p13/tests/config.json
packages/l1-p13/tests/selectors.jest.test.mjs
packages/l1-p13/tests/selectors.vitest.test.ts
packages/l1-p13/vitest.config.ts
packages/l1-p14/README.md
packages/l1-p14/jest.config.cjs
packages/l1-p14/package.json
packages/l1-p14/public/index.html
packages/l1-p14/server.mjs
packages/l1-p14/styles.css
packages/l1-p14/tests/config.json
packages/l1-p14/tests/selectors.jest.test.mjs
packages/l1-p14/tests/selectors.vitest.test.ts
packages/l1-p14/vitest.config.ts
packages/l1-p15/README.md
packages/l1-p15/jest.config.cjs
packages/l1-p15/package.json
packages/l1-p15/public/index.html
packages/l1-p15/server.mjs
packages/l1-p15/styles.css
packages/l1-p15/tests/config.json
packages/l1-p15/tests/selectors.jest.test.mjs
packages/l1-p15/tests/selectors.vitest.test.ts
packages/l1-p15/vitest.config.ts
packages/l2-p01/README.md
packages/l2-p01/jest.config.cjs
packages/l2-p01/package.json
packages/l2-p01/public/index.html
packages/l2-p01/server.mjs
packages/l2-p01/styles.css
packages/l2-p01/tests/config.json
packages/l2-p01/tests/selectors.jest.test.mjs
packages/l2-p01/tests/selectors.vitest.test.ts
packages/l2-p01/vitest.config.ts
packages/l2-p02/README.md
packages/l2-p02/jest.config.cjs
packages/l2-p02/package.json
packages/l2-p02/public/index.html
packages/l2-p02/server.mjs
packages/l2-p02/styles.css
packages/l2-p02/tests/config.json
packages/l2-p02/tests/selectors.jest.test.mjs
packages/l2-p02/tests/selectors.vitest.test.ts
packages/l2-p02/vitest.config.ts
packages/l2-p03/README.md
packages/l2-p03/jest.config.cjs
packages/l2-p03/package.json
packages/l2-p03/public/index.html
packages/l2-p03/server.mjs
packages/l2-p03/styles.css
packages/l2-p03/tests/config.json
packages/l2-p03/tests/selectors.jest.test.mjs
packages/l2-p03/tests/selectors.vitest.test.ts
packages/l2-p03/vitest.config.ts
packages/l2-p04/README.md
packages/l2-p04/jest.config.cjs
packages/l2-p04/package.json
packages/l2-p04/public/index.html
packages/l2-p04/server.mjs
packages/l2-p04/styles.css
packages/l2-p04/tests/config.json
packages/l2-p04/tests/selectors.jest.test.mjs
packages/l2-p04/tests/selectors.vitest.test.ts
packages/l2-p04/vitest.config.ts
packages/l2-p05/README.md
packages/l2-p05/jest.config.cjs
packages/l2-p05/package.json
packages/l2-p05/public/index.html
packages/l2-p05/server.mjs
packages/l2-p05/styles.css
packages/l2-p05/tests/config.json
packages/l2-p05/tests/selectors.jest.test.mjs
packages/l2-p05/tests/selectors.vitest.test.ts
packages/l2-p05/vitest.config.ts
packages/l2-p06/README.md
packages/l2-p06/jest.config.cjs
packages/l2-p06/package.json
packages/l2-p06/public/index.html
packages/l2-p06/server.mjs
packages/l2-p06/styles.css
packages/l2-p06/tests/config.json
packages/l2-p06/tests/selectors.jest.test.mjs
packages/l2-p06/tests/selectors.vitest.test.ts
packages/l2-p06/vitest.config.ts
packages/l2-p07/README.md
packages/l2-p07/jest.config.cjs
packages/l2-p07/package.json
packages/l2-p07/public/index.html
packages/l2-p07/server.mjs
packages/l2-p07/styles.css
packages/l2-p07/tests/config.json
packages/l2-p07/tests/selectors.jest.test.mjs
packages/l2-p07/tests/selectors.vitest.test.ts
packages/l2-p07/vitest.config.ts
packages/l2-p08/README.md
packages/l2-p08/jest.config.cjs
packages/l2-p08/package.json
packages/l2-p08/public/index.html
packages/l2-p08/server.mjs
packages/l2-p08/styles.css
packages/l2-p08/tests/config.json
packages/l2-p08/tests/selectors.jest.test.mjs
packages/l2-p08/tests/selectors.vitest.test.ts
packages/l2-p08/vitest.config.ts
packages/l2-p09/README.md
packages/l2-p09/jest.config.cjs
packages/l2-p09/package.json
packages/l2-p09/public/index.html
packages/l2-p09/server.mjs
packages/l2-p09/styles.css
packages/l2-p09/tests/config.json
packages/l2-p09/tests/selectors.jest.test.mjs
packages/l2-p09/tests/selectors.vitest.test.ts
packages/l2-p09/vitest.config.ts
packages/l2-p10/README.md
packages/l2-p10/jest.config.cjs
packages/l2-p10/package.json
packages/l2-p10/public/index.html
packages/l2-p10/server.mjs
packages/l2-p10/styles.css
packages/l2-p10/tests/config.json
packages/l2-p10/tests/selectors.jest.test.mjs
packages/l2-p10/tests/selectors.vitest.test.ts
packages/l2-p10/vitest.config.ts
packages/l2-p11/README.md
packages/l2-p11/jest.config.cjs
packages/l2-p11/package.json
packages/l2-p11/public/index.html
packages/l2-p11/server.mjs
packages/l2-p11/styles.css
packages/l2-p11/tests/config.json
packages/l2-p11/tests/selectors.jest.test.mjs
packages/l2-p11/tests/selectors.vitest.test.ts
packages/l2-p11/vitest.config.ts
packages/l2-p12/README.md
packages/l2-p12/jest.config.cjs
packages/l2-p12/package.json
packages/l2-p12/public/index.html
packages/l2-p12/server.mjs
packages/l2-p12/styles.css
packages/l2-p12/tests/config.json
packages/l2-p12/tests/selectors.jest.test.mjs
packages/l2-p12/tests/selectors.vitest.test.ts
packages/l2-p12/vitest.config.ts
packages/l2-p13/README.md
packages/l2-p13/jest.config.cjs
packages/l2-p13/package.json
packages/l2-p13/public/index.html
packages/l2-p13/server.mjs
packages/l2-p13/styles.css
packages/l2-p13/tests/config.json
packages/l2-p13/tests/selectors.jest.test.mjs
packages/l2-p13/tests/selectors.vitest.test.ts
packages/l2-p13/vitest.config.ts
packages/l2-p14/README.md
packages/l2-p14/jest.config.cjs
packages/l2-p14/package.json
packages/l2-p14/public/index.html
packages/l2-p14/server.mjs
packages/l2-p14/styles.css
packages/l2-p14/tests/config.json
packages/l2-p14/tests/selectors.jest.test.mjs
packages/l2-p14/tests/selectors.vitest.test.ts
packages/l2-p14/vitest.config.ts
packages/l2-p15/README.md
packages/l2-p15/jest.config.cjs
packages/l2-p15/package.json
packages/l2-p15/public/index.html
packages/l2-p15/server.mjs
packages/l2-p15/styles.css
packages/l2-p15/tests/config.json
packages/l2-p15/tests/selectors.jest.test.mjs
packages/l2-p15/tests/selectors.vitest.test.ts
packages/l2-p15/vitest.config.ts
packages/l3-p01/README.md
packages/l3-p01/jest.config.cjs
packages/l3-p01/package.json
packages/l3-p01/public/index.html
packages/l3-p01/server.mjs
packages/l3-p01/styles.css
packages/l3-p01/tests/config.json
packages/l3-p01/tests/selectors.jest.test.mjs
packages/l3-p01/tests/selectors.vitest.test.ts
packages/l3-p01/vitest.config.ts
packages/l3-p02/README.md
packages/l3-p02/jest.config.cjs
packages/l3-p02/package.json
packages/l3-p02/public/index.html
packages/l3-p02/server.mjs
packages/l3-p02/styles.css
packages/l3-p02/tests/config.json
packages/l3-p02/tests/selectors.jest.test.mjs
packages/l3-p02/tests/selectors.vitest.test.ts
packages/l3-p02/vitest.config.ts
packages/l3-p03/README.md
packages/l3-p03/jest.config.cjs
packages/l3-p03/package.json
packages/l3-p03/public/index.html
packages/l3-p03/server.mjs
packages/l3-p03/styles.css
packages/l3-p03/tests/config.json
packages/l3-p03/tests/selectors.jest.test.mjs
packages/l3-p03/tests/selectors.vitest.test.ts
packages/l3-p03/vitest.config.ts
packages/l3-p04/README.md
packages/l3-p04/jest.config.cjs
packages/l3-p04/package.json
packages/l3-p04/public/index.html
packages/l3-p04/server.mjs
packages/l3-p04/styles.css
packages/l3-p04/tests/config.json
packages/l3-p04/tests/selectors.jest.test.mjs
packages/l3-p04/tests/selectors.vitest.test.ts
packages/l3-p04/vitest.config.ts
packages/l3-p05/README.md
packages/l3-p05/jest.config.cjs
packages/l3-p05/package.json
packages/l3-p05/public/index.html
packages/l3-p05/server.mjs
packages/l3-p05/styles.css
packages/l3-p05/tests/config.json
packages/l3-p05/tests/selectors.jest.test.mjs
packages/l3-p05/tests/selectors.vitest.test.ts
packages/l3-p05/vitest.config.ts
packages/l3-p06/README.md
packages/l3-p06/jest.config.cjs
packages/l3-p06/package.json
packages/l3-p06/public/index.html
packages/l3-p06/server.mjs
packages/l3-p06/styles.css
packages/l3-p06/tests/config.json
packages/l3-p06/tests/selectors.jest.test.mjs
packages/l3-p06/tests/selectors.vitest.test.ts
packages/l3-p06/vitest.config.ts
packages/l3-p07/README.md
packages/l3-p07/jest.config.cjs
packages/l3-p07/package.json
packages/l3-p07/public/index.html
packages/l3-p07/server.mjs
packages/l3-p07/styles.css
packages/l3-p07/tests/config.json
packages/l3-p07/tests/selectors.jest.test.mjs
packages/l3-p07/tests/selectors.vitest.test.ts
packages/l3-p07/vitest.config.ts
packages/l3-p08/README.md
packages/l3-p08/jest.config.cjs
packages/l3-p08/package.json
packages/l3-p08/public/index.html
packages/l3-p08/server.mjs
packages/l3-p08/styles.css
packages/l3-p08/tests/config.json
packages/l3-p08/tests/selectors.jest.test.mjs
packages/l3-p08/tests/selectors.vitest.test.ts
packages/l3-p08/vitest.config.ts
packages/l3-p09/README.md
packages/l3-p09/jest.config.cjs
packages/l3-p09/package.json
packages/l3-p09/public/index.html
packages/l3-p09/server.mjs
packages/l3-p09/styles.css
packages/l3-p09/tests/config.json
packages/l3-p09/tests/selectors.jest.test.mjs
packages/l3-p09/tests/selectors.vitest.test.ts
packages/l3-p09/vitest.config.ts
packages/l3-p10/README.md
packages/l3-p10/jest.config.cjs
packages/l3-p10/package.json
packages/l3-p10/public/index.html
packages/l3-p10/server.mjs
packages/l3-p10/styles.css
packages/l3-p10/tests/config.json
packages/l3-p10/tests/selectors.jest.test.mjs
packages/l3-p10/tests/selectors.vitest.test.ts
packages/l3-p10/vitest.config.ts
packages/l3-p11/README.md
packages/l3-p11/jest.config.cjs
packages/l3-p11/package.json
packages/l3-p11/public/index.html
packages/l3-p11/server.mjs
packages/l3-p11/styles.css
packages/l3-p11/tests/config.json
packages/l3-p11/tests/selectors.jest.test.mjs
packages/l3-p11/tests/selectors.vitest.test.ts
packages/l3-p11/vitest.config.ts
packages/l3-p12/README.md
packages/l3-p12/jest.config.cjs
packages/l3-p12/package.json
packages/l3-p12/public/index.html
packages/l3-p12/server.mjs
packages/l3-p12/styles.css
packages/l3-p12/tests/config.json
packages/l3-p12/tests/selectors.jest.test.mjs
packages/l3-p12/tests/selectors.vitest.test.ts
packages/l3-p12/vitest.config.ts
packages/l3-p13/README.md
packages/l3-p13/jest.config.cjs
packages/l3-p13/package.json
packages/l3-p13/public/index.html
packages/l3-p13/server.mjs
packages/l3-p13/styles.css
packages/l3-p13/tests/config.json
packages/l3-p13/tests/selectors.jest.test.mjs
packages/l3-p13/tests/selectors.vitest.test.ts
packages/l3-p13/vitest.config.ts
packages/l3-p14/README.md
packages/l3-p14/jest.config.cjs
packages/l3-p14/package.json
packages/l3-p14/public/index.html
packages/l3-p14/server.mjs
packages/l3-p14/styles.css
packages/l3-p14/tests/config.json
packages/l3-p14/tests/selectors.jest.test.mjs
packages/l3-p14/tests/selectors.vitest.test.ts
packages/l3-p14/vitest.config.ts
packages/l3-p15/README.md
packages/l3-p15/jest.config.cjs
packages/l3-p15/package.json
packages/l3-p15/public/index.html
packages/l3-p15/server.mjs
packages/l3-p15/styles.css
packages/l3-p15/tests/config.json
packages/l3-p15/tests/selectors.jest.test.mjs
packages/l3-p15/tests/selectors.vitest.test.ts
packages/l3-p15/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 182, styles: 45, docs: 45, public: 45, tests: 135.

**package.json — sinteză (scripturi, workspaces, dependențe)**

- `package.json`: name=`s5p3-monorepo` type=`module` workspaces=True
  - **Scripturi:**
  - `test:vitest` → `pnpm -r --filter ./packages run test:vitest`
  - `test:jest` → `pnpm -r --filter ./packages run test:jest`
  - `test` → `pnpm -r --filter ./packages run test`
  - `dev` → `echo 'rulează dev per pachet: pnpm --filter <pkg> run dev'`
  - **Deps:** 
  - **DevDeps:** pnpm, vitest, jest, jsdom, express
- `packages/l1-p01/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p02/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p03/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p04/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p05/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p06/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p07/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p08/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p09/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p10/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p11/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p12/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p13/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p14/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l1-p15/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p01/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p02/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p03/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p04/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p05/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p06/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p07/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p08/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p09/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p10/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p11/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p12/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p13/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p14/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l2-p15/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p01/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p02/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p03/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p04/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p05/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p06/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p07/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p08/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p09/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p10/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p11/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p12/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p13/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p14/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `packages/l3-p15/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom

### Seminar5_Partea3_standalone.zip

```
l1-p01/README.md
l1-p01/jest.config.cjs
l1-p01/package.json
l1-p01/public/index.html
l1-p01/server.mjs
l1-p01/styles.css
l1-p01/tests/config.json
l1-p01/tests/selectors.jest.test.mjs
l1-p01/tests/selectors.vitest.test.ts
l1-p01/vitest.config.ts
l1-p02/README.md
l1-p02/jest.config.cjs
l1-p02/package.json
l1-p02/public/index.html
l1-p02/server.mjs
l1-p02/styles.css
l1-p02/tests/config.json
l1-p02/tests/selectors.jest.test.mjs
l1-p02/tests/selectors.vitest.test.ts
l1-p02/vitest.config.ts
l1-p03/README.md
l1-p03/jest.config.cjs
l1-p03/package.json
l1-p03/public/index.html
l1-p03/server.mjs
l1-p03/styles.css
l1-p03/tests/config.json
l1-p03/tests/selectors.jest.test.mjs
l1-p03/tests/selectors.vitest.test.ts
l1-p03/vitest.config.ts
l1-p04/README.md
l1-p04/jest.config.cjs
l1-p04/package.json
l1-p04/public/index.html
l1-p04/server.mjs
l1-p04/styles.css
l1-p04/tests/config.json
l1-p04/tests/selectors.jest.test.mjs
l1-p04/tests/selectors.vitest.test.ts
l1-p04/vitest.config.ts
l1-p05/README.md
l1-p05/jest.config.cjs
l1-p05/package.json
l1-p05/public/index.html
l1-p05/server.mjs
l1-p05/styles.css
l1-p05/tests/config.json
l1-p05/tests/selectors.jest.test.mjs
l1-p05/tests/selectors.vitest.test.ts
l1-p05/vitest.config.ts
l1-p06/README.md
l1-p06/jest.config.cjs
l1-p06/package.json
l1-p06/public/index.html
l1-p06/server.mjs
l1-p06/styles.css
l1-p06/tests/config.json
l1-p06/tests/selectors.jest.test.mjs
l1-p06/tests/selectors.vitest.test.ts
l1-p06/vitest.config.ts
l1-p07/README.md
l1-p07/jest.config.cjs
l1-p07/package.json
l1-p07/public/index.html
l1-p07/server.mjs
l1-p07/styles.css
l1-p07/tests/config.json
l1-p07/tests/selectors.jest.test.mjs
l1-p07/tests/selectors.vitest.test.ts
l1-p07/vitest.config.ts
l1-p08/README.md
l1-p08/jest.config.cjs
l1-p08/package.json
l1-p08/public/index.html
l1-p08/server.mjs
l1-p08/styles.css
l1-p08/tests/config.json
l1-p08/tests/selectors.jest.test.mjs
l1-p08/tests/selectors.vitest.test.ts
l1-p08/vitest.config.ts
l1-p09/README.md
l1-p09/jest.config.cjs
l1-p09/package.json
l1-p09/public/index.html
l1-p09/server.mjs
l1-p09/styles.css
l1-p09/tests/config.json
l1-p09/tests/selectors.jest.test.mjs
l1-p09/tests/selectors.vitest.test.ts
l1-p09/vitest.config.ts
l1-p10/README.md
l1-p10/jest.config.cjs
l1-p10/package.json
l1-p10/public/index.html
l1-p10/server.mjs
l1-p10/styles.css
l1-p10/tests/config.json
l1-p10/tests/selectors.jest.test.mjs
l1-p10/tests/selectors.vitest.test.ts
l1-p10/vitest.config.ts
l1-p11/README.md
l1-p11/jest.config.cjs
l1-p11/package.json
l1-p11/public/index.html
l1-p11/server.mjs
l1-p11/styles.css
l1-p11/tests/config.json
l1-p11/tests/selectors.jest.test.mjs
l1-p11/tests/selectors.vitest.test.ts
l1-p11/vitest.config.ts
l1-p12/README.md
l1-p12/jest.config.cjs
l1-p12/package.json
l1-p12/public/index.html
l1-p12/server.mjs
l1-p12/styles.css
l1-p12/tests/config.json
l1-p12/tests/selectors.jest.test.mjs
l1-p12/tests/selectors.vitest.test.ts
l1-p12/vitest.config.ts
l1-p13/README.md
l1-p13/jest.config.cjs
l1-p13/package.json
l1-p13/public/index.html
l1-p13/server.mjs
l1-p13/styles.css
l1-p13/tests/config.json
l1-p13/tests/selectors.jest.test.mjs
l1-p13/tests/selectors.vitest.test.ts
l1-p13/vitest.config.ts
l1-p14/README.md
l1-p14/jest.config.cjs
l1-p14/package.json
l1-p14/public/index.html
l1-p14/server.mjs
l1-p14/styles.css
l1-p14/tests/config.json
l1-p14/tests/selectors.jest.test.mjs
l1-p14/tests/selectors.vitest.test.ts
l1-p14/vitest.config.ts
l1-p15/README.md
l1-p15/jest.config.cjs
l1-p15/package.json
l1-p15/public/index.html
l1-p15/server.mjs
l1-p15/styles.css
l1-p15/tests/config.json
l1-p15/tests/selectors.jest.test.mjs
l1-p15/tests/selectors.vitest.test.ts
l1-p15/vitest.config.ts
l2-p01/README.md
l2-p01/jest.config.cjs
l2-p01/package.json
l2-p01/public/index.html
l2-p01/server.mjs
l2-p01/styles.css
l2-p01/tests/config.json
l2-p01/tests/selectors.jest.test.mjs
l2-p01/tests/selectors.vitest.test.ts
l2-p01/vitest.config.ts
l2-p02/README.md
l2-p02/jest.config.cjs
l2-p02/package.json
l2-p02/public/index.html
l2-p02/server.mjs
l2-p02/styles.css
l2-p02/tests/config.json
l2-p02/tests/selectors.jest.test.mjs
l2-p02/tests/selectors.vitest.test.ts
l2-p02/vitest.config.ts
l2-p03/README.md
l2-p03/jest.config.cjs
l2-p03/package.json
l2-p03/public/index.html
l2-p03/server.mjs
l2-p03/styles.css
l2-p03/tests/config.json
l2-p03/tests/selectors.jest.test.mjs
l2-p03/tests/selectors.vitest.test.ts
l2-p03/vitest.config.ts
l2-p04/README.md
l2-p04/jest.config.cjs
l2-p04/package.json
l2-p04/public/index.html
l2-p04/server.mjs
l2-p04/styles.css
l2-p04/tests/config.json
l2-p04/tests/selectors.jest.test.mjs
l2-p04/tests/selectors.vitest.test.ts
l2-p04/vitest.config.ts
l2-p05/README.md
l2-p05/jest.config.cjs
l2-p05/package.json
l2-p05/public/index.html
l2-p05/server.mjs
l2-p05/styles.css
l2-p05/tests/config.json
l2-p05/tests/selectors.jest.test.mjs
l2-p05/tests/selectors.vitest.test.ts
l2-p05/vitest.config.ts
l2-p06/README.md
l2-p06/jest.config.cjs
l2-p06/package.json
l2-p06/public/index.html
l2-p06/server.mjs
l2-p06/styles.css
l2-p06/tests/config.json
l2-p06/tests/selectors.jest.test.mjs
l2-p06/tests/selectors.vitest.test.ts
l2-p06/vitest.config.ts
l2-p07/README.md
l2-p07/jest.config.cjs
l2-p07/package.json
l2-p07/public/index.html
l2-p07/server.mjs
l2-p07/styles.css
l2-p07/tests/config.json
l2-p07/tests/selectors.jest.test.mjs
l2-p07/tests/selectors.vitest.test.ts
l2-p07/vitest.config.ts
l2-p08/README.md
l2-p08/jest.config.cjs
l2-p08/package.json
l2-p08/public/index.html
l2-p08/server.mjs
l2-p08/styles.css
l2-p08/tests/config.json
l2-p08/tests/selectors.jest.test.mjs
l2-p08/tests/selectors.vitest.test.ts
l2-p08/vitest.config.ts
l2-p09/README.md
l2-p09/jest.config.cjs
l2-p09/package.json
l2-p09/public/index.html
l2-p09/server.mjs
l2-p09/styles.css
l2-p09/tests/config.json
l2-p09/tests/selectors.jest.test.mjs
l2-p09/tests/selectors.vitest.test.ts
l2-p09/vitest.config.ts
l2-p10/README.md
l2-p10/jest.config.cjs
l2-p10/package.json
l2-p10/public/index.html
l2-p10/server.mjs
l2-p10/styles.css
l2-p10/tests/config.json
l2-p10/tests/selectors.jest.test.mjs
l2-p10/tests/selectors.vitest.test.ts
l2-p10/vitest.config.ts
l2-p11/README.md
l2-p11/jest.config.cjs
l2-p11/package.json
l2-p11/public/index.html
l2-p11/server.mjs
l2-p11/styles.css
l2-p11/tests/config.json
l2-p11/tests/selectors.jest.test.mjs
l2-p11/tests/selectors.vitest.test.ts
l2-p11/vitest.config.ts
l2-p12/README.md
l2-p12/jest.config.cjs
l2-p12/package.json
l2-p12/public/index.html
l2-p12/server.mjs
l2-p12/styles.css
l2-p12/tests/config.json
l2-p12/tests/selectors.jest.test.mjs
l2-p12/tests/selectors.vitest.test.ts
l2-p12/vitest.config.ts
l2-p13/README.md
l2-p13/jest.config.cjs
l2-p13/package.json
l2-p13/public/index.html
l2-p13/server.mjs
l2-p13/styles.css
l2-p13/tests/config.json
l2-p13/tests/selectors.jest.test.mjs
l2-p13/tests/selectors.vitest.test.ts
l2-p13/vitest.config.ts
l2-p14/README.md
l2-p14/jest.config.cjs
l2-p14/package.json
l2-p14/public/index.html
l2-p14/server.mjs
l2-p14/styles.css
l2-p14/tests/config.json
l2-p14/tests/selectors.jest.test.mjs
l2-p14/tests/selectors.vitest.test.ts
l2-p14/vitest.config.ts
l2-p15/README.md
l2-p15/jest.config.cjs
l2-p15/package.json
l2-p15/public/index.html
l2-p15/server.mjs
l2-p15/styles.css
l2-p15/tests/config.json
l2-p15/tests/selectors.jest.test.mjs
l2-p15/tests/selectors.vitest.test.ts
l2-p15/vitest.config.ts
l3-p01/README.md
l3-p01/jest.config.cjs
l3-p01/package.json
l3-p01/public/index.html
l3-p01/server.mjs
l3-p01/styles.css
l3-p01/tests/config.json
l3-p01/tests/selectors.jest.test.mjs
l3-p01/tests/selectors.vitest.test.ts
l3-p01/vitest.config.ts
l3-p02/README.md
l3-p02/jest.config.cjs
l3-p02/package.json
l3-p02/public/index.html
l3-p02/server.mjs
l3-p02/styles.css
l3-p02/tests/config.json
l3-p02/tests/selectors.jest.test.mjs
l3-p02/tests/selectors.vitest.test.ts
l3-p02/vitest.config.ts
l3-p03/README.md
l3-p03/jest.config.cjs
l3-p03/package.json
l3-p03/public/index.html
l3-p03/server.mjs
l3-p03/styles.css
l3-p03/tests/config.json
l3-p03/tests/selectors.jest.test.mjs
l3-p03/tests/selectors.vitest.test.ts
l3-p03/vitest.config.ts
l3-p04/README.md
l3-p04/jest.config.cjs
l3-p04/package.json
l3-p04/public/index.html
l3-p04/server.mjs
l3-p04/styles.css
l3-p04/tests/config.json
l3-p04/tests/selectors.jest.test.mjs
l3-p04/tests/selectors.vitest.test.ts
l3-p04/vitest.config.ts
l3-p05/README.md
l3-p05/jest.config.cjs
l3-p05/package.json
l3-p05/public/index.html
l3-p05/server.mjs
l3-p05/styles.css
l3-p05/tests/config.json
l3-p05/tests/selectors.jest.test.mjs
l3-p05/tests/selectors.vitest.test.ts
l3-p05/vitest.config.ts
l3-p06/README.md
l3-p06/jest.config.cjs
l3-p06/package.json
l3-p06/public/index.html
l3-p06/server.mjs
l3-p06/styles.css
l3-p06/tests/config.json
l3-p06/tests/selectors.jest.test.mjs
l3-p06/tests/selectors.vitest.test.ts
l3-p06/vitest.config.ts
l3-p07/README.md
l3-p07/jest.config.cjs
l3-p07/package.json
l3-p07/public/index.html
l3-p07/server.mjs
l3-p07/styles.css
l3-p07/tests/config.json
l3-p07/tests/selectors.jest.test.mjs
l3-p07/tests/selectors.vitest.test.ts
l3-p07/vitest.config.ts
l3-p08/README.md
l3-p08/jest.config.cjs
l3-p08/package.json
l3-p08/public/index.html
l3-p08/server.mjs
l3-p08/styles.css
l3-p08/tests/config.json
l3-p08/tests/selectors.jest.test.mjs
l3-p08/tests/selectors.vitest.test.ts
l3-p08/vitest.config.ts
l3-p09/README.md
l3-p09/jest.config.cjs
l3-p09/package.json
l3-p09/public/index.html
l3-p09/server.mjs
l3-p09/styles.css
l3-p09/tests/config.json
l3-p09/tests/selectors.jest.test.mjs
l3-p09/tests/selectors.vitest.test.ts
l3-p09/vitest.config.ts
l3-p10/README.md
l3-p10/jest.config.cjs
l3-p10/package.json
l3-p10/public/index.html
l3-p10/server.mjs
l3-p10/styles.css
l3-p10/tests/config.json
l3-p10/tests/selectors.jest.test.mjs
l3-p10/tests/selectors.vitest.test.ts
l3-p10/vitest.config.ts
l3-p11/README.md
l3-p11/jest.config.cjs
l3-p11/package.json
l3-p11/public/index.html
l3-p11/server.mjs
l3-p11/styles.css
l3-p11/tests/config.json
l3-p11/tests/selectors.jest.test.mjs
l3-p11/tests/selectors.vitest.test.ts
l3-p11/vitest.config.ts
l3-p12/README.md
l3-p12/jest.config.cjs
l3-p12/package.json
l3-p12/public/index.html
l3-p12/server.mjs
l3-p12/styles.css
l3-p12/tests/config.json
l3-p12/tests/selectors.jest.test.mjs
l3-p12/tests/selectors.vitest.test.ts
l3-p12/vitest.config.ts
l3-p13/README.md
l3-p13/jest.config.cjs
l3-p13/package.json
l3-p13/public/index.html
l3-p13/server.mjs
l3-p13/styles.css
l3-p13/tests/config.json
l3-p13/tests/selectors.jest.test.mjs
l3-p13/tests/selectors.vitest.test.ts
l3-p13/vitest.config.ts
l3-p14/README.md
l3-p14/jest.config.cjs
l3-p14/package.json
l3-p14/public/index.html
l3-p14/server.mjs
l3-p14/styles.css
l3-p14/tests/config.json
l3-p14/tests/selectors.jest.test.mjs
l3-p14/tests/selectors.vitest.test.ts
l3-p14/vitest.config.ts
l3-p15/README.md
l3-p15/jest.config.cjs
l3-p15/package.json
l3-p15/public/index.html
l3-p15/server.mjs
l3-p15/styles.css
l3-p15/tests/config.json
l3-p15/tests/selectors.jest.test.mjs
l3-p15/tests/selectors.vitest.test.ts
l3-p15/vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** styles: 45, config: 180, docs: 45, public: 45, tests: 135.

**package.json — sinteză (scripturi, workspaces, dependențe)**

- `l1-p01/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p02/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p03/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p04/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p05/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p06/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p07/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p08/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p09/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p10/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p11/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p12/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p13/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p14/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l1-p15/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p01/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p02/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p03/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p04/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p05/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p06/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p07/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p08/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p09/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p10/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p11/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p12/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p13/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p14/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l2-p15/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p01/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p02/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p03/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p04/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p05/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p06/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p07/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p08/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p09/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p10/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p11/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p12/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p13/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p14/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom
- `l3-p15/package.json`: name=`s5p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom

## 2. Sinteza documentelor DOCX/MD (teorie ↔ laborator ↔ proiecte)

### Seminar5_Partea1_Teorie.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 5 — CSS Selectors & Layout
Partea 1: Teorie (extins)
- Hook realist: "Hub-ul Asociațiilor Studențești" în 15 minute, fără framework-uri
- Imaginați-vă că, la ora 08:30, primiți un mesaj de la coordonatorul asociațiilor studențești: 
„La 10:00 avem un stand deschis pentru noii studenți; pune, te rog, online o pagină simplă cu 
carduri pentru cluburi, un formular de înscriere și un layout 3×3 care să arate bine pe orice ecran.” 
Nu aveți voie să folosiți framework‑uri CSS (Bootstrap/Tailwind). Aveți doar **CSS selectors** bine alese, 
pseudo‑clase moderne (de ex. `:focus-visible`, `:has()`), **form styling** accesibil și un **grid 3×3**
care colapsează elegant pe mobil. În 90 de minute, veți livra o pagină curată, lizibilă și predictibilă. 
Acesta este exercițiul mental al seminarului: să formăm un mod de gândire orientat pe **selectors**, 
**stări** și **pattern‑uri** de layout — astfel încât nevoile reale să devină simple compoziții CSS.

### Seminar5_Partea2_Laborator.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 5 — CSS Selectors & Layout
Partea 2: Laborator (extins)
- Context, obiective și criterii de evaluare
- Această parte a laboratorului transformă conceptele teoretice din Partea 1 într‑o practică aplicată, folosind o temă comună: „Clubs & Associations Hub”. Vei construi o pagină cu un **grid 3×3** de carduri și un **formular de înscriere** a studenților, de la simplu la complex, exclusiv cu **CSS selectors** bine alese, **pseudo‑clase** orientate pe stări de UI și **layout** modern cu **Grid**. Pe parcurs, menținem un nivel înalt de lizibilitate și accesibilitate (focus vizibil, contraste, spațiere), susținute de principii HCI.

### Seminar5_Partea2_README.md

**Titluri/Heading-uri (eșantion):**

- Seminarul 5 — Partea 2 (Laborator): CSS Selectors & Layout — pseudo‑clase, form styling, grid 3×3
- Structură
- Rulare

**Headings principale (eșantion):**

- Seminarul 5 — Partea 2 (Laborator): CSS Selectors & Layout — pseudo‑clase, form styling, grid 3×3
- Structură
- Rulare
- Worksheet — checklist (scurt)

**Idei cheie (liste):**

- **selectors moderni** (`:is()`, `:where()`, `:has()`),
- **form styling** accesibil (`:focus-visible`, `:invalid/:valid`, `accent-color`, `::file-selector-button`),
- **grid 3×3** responsiv (`display: grid`, `grid-template-columns`, `gap`, `aspect-ratio`).
- Ai **focus ring** vizibil pe linkuri/butoane/inputuri (`:focus-visible`)?
- Stilizezi **grupurile cu erori** prin `:has(input:invalid)`?
- Formularul conține **required**/`novalidate` și mesaje de eroare locale?
- Gridul „**3×3**” funcționează și **colapsează** la 2/1 coloane?
- Folosești `:where()` pentru a **nu** crește specificitatea?

### Seminar5_Partea3_Arhive_Ghid.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare a arhivelor — Standalone & Monorepo (PNPM workspaces)
- **Ce conțin arhivele**
- • Standalone: 45 directoare (câte unul per proiect), fiecare cu `public/index.html`, `styles.css`, `tests/`, `vitest.config.ts`, `jest.config.cjs`, `server.mjs`, `package.json`, `README.md`.

### Seminar5_Partea3_Proiecte_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 5 — Partea 3: Proiecte/teme (extins)
- Introducere și metodologie
- Această parte livrează **45 de proiecte** (15 × L1, 15 × L2, 15 × L3) concepute pentru a consolida „gândirea în selectori” și fluența în layout‑uri moderne. Fiecare proiect are o **temă unică**, dar toate gravitează în jurul aceleiași aplicații narative — „Clubs & Associations Hub”: listări în **grid 3×3**, formulare accesibile, componente CSS-only și theming cu **CSS custom properties**. Pentru fiecare proiect oferim: **Scop didactic**, **Specificații (Cerințe)**, **Criterii de acceptare**, **Soluție (rezumat)** și **AI‑assist prompts** (VSL — very short loop).

## 3. Monorepo vs. standalone — analiză comparativă


**Manageri de pachete & workspaces.** Monorepo (PNPM 9+) declară `packages/*` în `pnpm-workspace.yaml` și/sau `workspaces` în `package.json`, cu instalare la rădăcină (`pnpm i -w`). Standalone izolează dependențele per proiect (`npm i`).

**Comenzi de instalare/testare.** Monorepo: `pnpm -w run test` sau `pnpm --filter <pkg> run dev/test`. Standalone: `npm test`, `npm run dev`. Testele sunt **oglindite** (Vitest & Jest) și validează **convențiile CSS/HTML** pe aceleași scenarii. 

**Integrare CI.** Monorepo agregă workflows (`.github/workflows/*`) pentru lint/unit/e2e (unde există), în timp ce standalone definește workflows simple per proiect.

**Avantaje/Dezavantaje.** Standalone — cognitiv mai simplu (ideal pentru începători). Monorepo — scalare pentru colecții mari (ex. 45 proiecte L1–L3), partajare de configuri și execuții rapide; costul este înțelegerea filtrării PNPM și a grafului de pachete.
## 4. Rolul fișierelor cheie (config, cod, teste, extra)

| Fișier / tip | Rol |
|---|---|
| `vitest.config.ts` | Configurarea Vitest (jsdom) — verificări de convenții în CSS/HTML. |
| `jest.config.cjs` | Configurarea Jest (jsdom) — oglindește suitele Vitest. |
| `server.mjs` | Server Express minimal; servește `public/` și `styles/`. |
| `package.json` | Manifestul proiectului: metadate, dependențe, scripturi; definește rularea testelor Vitest/Jest. |
| `pnpm-workspace.yaml` | Declară pachetele din monorepo pentru PNPM. |
| `public/index.html` | Pagină „Hub” cu grid de carduri 3×3 și formular `novalidate` cu câmpuri `required`. |
| `styles/forms.css` | Stări native (`:invalid/:valid`), `:focus-within`, `:has()` pentru grupuri, `::file-selector-button`, `accent-color`. |
| `styles/layout.css` | Grid 3×3 + media queries 3→2→1, stări `.card:where(:hover, :focus-within)`; `aspect-ratio`/`object-fit`. |
| `styles/base.css` | Tokens + focus ring (`:focus-visible`), container. |
| `src/main.js` | Validare live minimală și sumar erori (aria-live). |

## 5. Corelații cod ↔ configurări ↔ teste


- **Convențiile CSS/HTML** din `styles/*.css` și `public/index.html` sunt verificate în **ambele suite** (Vitest & Jest, jsdom): `:focus-visible`, `:has()`, `:invalid`, `display: grid` + `grid-template-columns: repeat(3, 1fr)`, `@media` pentru 3→2→1, `aspect-ratio`/`object-fit`. 
- **`.env.example`** — dacă apare în unele proiecte — documentează portul; `server.mjs` servește static și oferă un URL stabil pentru testare manuală. 
- **ESLint + CI**: workflows rulează `lint` + `test`, blocând regresiile de stil și încălcările convențiilor. 
- **Playwright/Workbox** (unde există) extind aria către e2e respectiv PWA demo; nu sunt obligatorii în acest seminar.
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S5 fixează **gândirea în selectori** și **layout‑uri moderne** fără framework‑uri: pseudo‑clase orientate pe stări (focus, validare, UI), **Grid 3×3** responsiv, și un **form styling** accesibil. Conținutul teoretic este mapat direct pe laborator și pe proiectele L1–L3, iar testarea duală (Vitest & Jest) asigură verificări deterministe ale convențiilor. fileciteturn8file0### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; rădăcină + `packages/*` |
| Instalare | `npm i` | `pnpm i -w` |
| Testare | `npm test` (Vitest & Jest) | `pnpm -w run test` sau `--filter` |
| CI | Workflows simple per proiect | Workflows agregate, matrice pe pachete |
| Scalare (45 proiecte) | multiplicare directoare | pachete dedicate în `packages/*` |
| Public țintă | începători | echipe/colecții avansate |
### Inventar pe arhivă (roluri și observații)

- **Seminar5_Partea2_starter.zip** — config=4, public=1, styles=4, code=2, tests=2.
- **Seminar5_Partea3_monorepo.zip** — config=182, styles=45, docs=45, public=45, tests=135.
- **Seminar5_Partea3_standalone.zip** — styles=45, config=180, docs=45, public=45, tests=135.
### Explicații fișier‑cu‑fișier

Consultați tabelul din §4. Mappingul exact între fișierele din **starter** și cerințele laboratorului se regăsește în README‑ul Părții 2 și în docx‑ul laboratorului (checklist, scripturi, structură). fileciteturn8file2 fileciteturn8file1
### Corelații între fișiere


- `styles/forms.css` ↔ `tests/unit/*` — `:focus-visible`, `:has()`, `:invalid`. fileciteturn8file1  
- `styles/layout.css` ↔ `tests/unit/*` — `display: grid` + `grid-template-columns: repeat(3, 1fr)`; MQ 3→2→1. fileciteturn8file1  
- `public/index.html` ↔ `tests/unit/*` — formular `novalidate`, câmpuri `required`, `aria-live` pentru erori. fileciteturn8file1  
- `.github/workflows/*` ↔ `lint`/`test` — pipeline determinist în monorepo/standalone. fileciteturn8file3  
### Recomandări pentru studenți


1) **Gândiți în convenții**: testați prezența regulilor‑cheie în CSS/HTML (nu style computed).  
2) **Reduceți specificitatea**: prefixați lanțurile cu `:where(...)`; grupați stările cu `:is(...)`. fileciteturn8file0  
3) **Form styling robust**: validați nativ (`:invalid/:valid`), accentuați grupul cu `:has()` și asigurați focus ring consecvent. fileciteturn8file0  
4) **Grid 3×3 responsiv**: folosiți `repeat(3, 1fr)` + MQ 900px/520px sau `auto-fit + minmax`. fileciteturn8file0  
5) **CI ca gardian**: rulați `lint` + `test` înainte de push; folosiți profilele `tests/config.json` în proiecte. fileciteturn8file3  
### Instrucțiuni „Quick start” per arhivă (comenzi)


**Partea 2 — starter (standalone):**
```bash
unzip "Seminar5_Partea2_starter.zip" -d s5p2-starter
cd s5p2-starter
npm i
npm run dev           # http://localhost:5175 (redirect la /public/index.html)
npm run test:vitest
npm run test:jest
npm test
```
fileciteturn8file2

**Partea 3 — monorepo (proiecte):**
```bash
unzip "Seminar5_Partea3_monorepo.zip" -d s5p3-monorepo
cd s5p3-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter ./packages/l1-p01 run dev
```
fileciteturn8file3

**Partea 3 — standalone (proiecte):**
```bash
unzip "Seminar5_Partea3_standalone.zip" -d s5p3-standalone
cd s5p3-standalone/l1-p01
npm i
npm test
npm run dev
```
fileciteturn8file3
### Troubleshooting (erori frecvente)


- **Focus ring „dispare”** — folosești `:focus` în loc de `:focus-visible` sau ai `outline: none`. fileciteturn8file2  
- **Grid nu colapsează corect** — verifică ordinea foilor CSS și MQ (900px, 520px). fileciteturn8file1  
- **`:has()` pare inactiv** — în unit tests verificăm doar **prezența**; pentru fallback adaugă o clasă JS (`is-invalid`). fileciteturn8file2  
- **Specificitate excesivă** — mută prefixele în `:where(...)`. fileciteturn8file0  
- **CI/PNPM** — confirmă Node 20+ și PNPM 9+; în proiecte, consultă `tests/config.json`. fileciteturn8file3  
### Integrarea ghidurilor (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** → principii de cascadă/specificitate/moștenire, pseudo‑clase moderne, form styling, grid 3×3, HCI/contrast: fundamente pentru `styles/*.css` și testele aferente. fileciteturn8file0  
- **Partea 2 (Laborator)** → scenariul „Clubs & Associations Hub”, starter code, checklist și teste oglindite (Vitest & Jest). fileciteturn8file1 fileciteturn8file2  
- **Partea 3 (Ghid arhive + Proiecte)** → organizarea celor **45 de proiecte** în standalone/monorepo, profilare `tests/config.json`, rubrică și prompts VSL. fileciteturn8file3 fileciteturn8file4  
### Prompt‑șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S5** (standalone & monorepo) un set „Clubs & Associations Hub” cu **CSS selectors** moderni (`:is()`, `:where()`, `:has()`), **form styling** accesibil (`:focus-visible`, `:invalid/:valid`, `accent-color`, `::file-selector-button`), **grid 3×3** responsiv (3→2→1, `aspect-ratio`/`object-fit`), testare dublă **Vitest/Jest**, CI, README cu Quick start & Troubleshooting, și variante **starter**/**solution**.”
