# Seminarul S2 — Funcții & Array‑uri (map/filter/reduce, utilitare, chaining) — Analiză integrată (standalone & monorepo)

*Generat la 2025-09-21 10:09.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar2_Partea2_p2-lab.zip

```
.gitignore
README.md
babel.config.cjs
bin/cli.js
data/sample.csv
data/sample.json
eslint.config.mjs
jest.config.cjs
package.json
src/cli-runner.js
src/index.js
src/lib/collect.js
src/lib/normalize.js
src/lib/predicates.js
src/lib/sorters.js
tests/jest/cli.jest.test.js
tests/jest/collect.jest.test.js
tests/jest/normalize.jest.test.js
tests/jest/predicates-sorters.jest.test.js
tests/vitest/cli.test.js
tests/vitest/collect.test.js
tests/vitest/normalize.test.js
tests/vitest/predicates-sorters.test.js
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 6, docs: 1, other: 3, code: 6, tests: 8.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s2p2-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js

### Seminar2_Partea3_p3-monorepo.zip

```
.github/workflows/e2e.yml
.github/workflows/lint.yml
.github/workflows/unit-jest.yml
.github/workflows/unit-vitest.yml
.github/workflows/workbox-sw.yml
.gitignore
babel.config.cjs
jest.config.cjs
package.json
packages/L1-01/package.json
packages/L1-01/src/index.js
packages/L1-01/tests/jest/spec.jest.test.js
packages/L1-01/tests/vitest/spec.test.js
packages/L1-02/package.json
packages/L1-02/src/index.js
packages/L1-02/tests/jest/spec.jest.test.js
packages/L1-02/tests/vitest/spec.test.js
packages/L1-03/package.json
packages/L1-03/src/index.js
packages/L1-03/tests/jest/spec.jest.test.js
packages/L1-03/tests/vitest/spec.test.js
packages/L1-04/package.json
packages/L1-04/src/index.js
packages/L1-04/tests/jest/spec.jest.test.js
packages/L1-04/tests/vitest/spec.test.js
packages/L1-05/package.json
packages/L1-05/src/index.js
packages/L1-05/tests/jest/spec.jest.test.js
packages/L1-05/tests/vitest/spec.test.js
packages/L1-06/package.json
packages/L1-06/src/index.js
packages/L1-06/tests/jest/spec.jest.test.js
packages/L1-06/tests/vitest/spec.test.js
packages/L1-07/package.json
packages/L1-07/src/index.js
packages/L1-07/tests/jest/spec.jest.test.js
packages/L1-07/tests/vitest/spec.test.js
packages/L1-08/package.json
packages/L1-08/src/index.js
packages/L1-08/tests/jest/spec.jest.test.js
packages/L1-08/tests/vitest/spec.test.js
packages/L1-09/package.json
packages/L1-09/src/index.js
packages/L1-09/tests/jest/spec.jest.test.js
packages/L1-09/tests/vitest/spec.test.js
packages/L1-10/package.json
packages/L1-10/src/index.js
packages/L1-10/tests/jest/spec.jest.test.js
packages/L1-10/tests/vitest/spec.test.js
packages/L1-11/package.json
packages/L1-11/src/index.js
packages/L1-11/tests/jest/spec.jest.test.js
packages/L1-11/tests/vitest/spec.test.js
packages/L1-12/package.json
packages/L1-12/src/index.js
packages/L1-12/tests/jest/spec.jest.test.js
packages/L1-12/tests/vitest/spec.test.js
packages/L1-13/package.json
packages/L1-13/src/index.js
packages/L1-13/tests/jest/spec.jest.test.js
packages/L1-13/tests/vitest/spec.test.js
packages/L1-14/package.json
packages/L1-14/src/index.js
packages/L1-14/tests/jest/spec.jest.test.js
packages/L1-14/tests/vitest/spec.test.js
packages/L1-15/package.json
packages/L1-15/src/index.js
packages/L1-15/tests/jest/spec.jest.test.js
packages/L1-15/tests/vitest/spec.test.js
packages/L2-01/package.json
packages/L2-01/src/index.js
packages/L2-01/tests/jest/spec.jest.test.js
packages/L2-01/tests/vitest/spec.test.js
packages/L2-02/package.json
packages/L2-02/src/index.js
packages/L2-02/tests/jest/spec.jest.test.js
packages/L2-02/tests/vitest/spec.test.js
packages/L2-03/package.json
packages/L2-03/src/index.js
packages/L2-03/tests/jest/spec.jest.test.js
packages/L2-03/tests/vitest/spec.test.js
packages/L2-04/package.json
packages/L2-04/src/index.js
packages/L2-04/tests/jest/spec.jest.test.js
packages/L2-04/tests/vitest/spec.test.js
packages/L2-05/package.json
packages/L2-05/src/index.js
packages/L2-05/tests/jest/spec.jest.test.js
packages/L2-05/tests/vitest/spec.test.js
packages/L2-06/package.json
packages/L2-06/src/index.js
packages/L2-06/tests/jest/spec.jest.test.js
packages/L2-06/tests/vitest/spec.test.js
packages/L2-07/package.json
packages/L2-07/src/index.js
packages/L2-07/tests/jest/spec.jest.test.js
packages/L2-07/tests/vitest/spec.test.js
packages/L2-08/package.json
packages/L2-08/src/index.js
packages/L2-08/tests/jest/spec.jest.test.js
packages/L2-08/tests/vitest/spec.test.js
packages/L2-09/package.json
packages/L2-09/src/index.js
packages/L2-09/tests/jest/spec.jest.test.js
packages/L2-09/tests/vitest/spec.test.js
packages/L2-10/package.json
packages/L2-10/src/index.js
packages/L2-10/tests/jest/spec.jest.test.js
packages/L2-10/tests/vitest/spec.test.js
packages/L2-11/package.json
packages/L2-11/src/index.js
packages/L2-11/tests/jest/spec.jest.test.js
packages/L2-11/tests/vitest/spec.test.js
packages/L2-12/package.json
packages/L2-12/src/index.js
packages/L2-12/tests/jest/spec.jest.test.js
packages/L2-12/tests/vitest/spec.test.js
packages/L2-13/package.json
packages/L2-13/src/index.js
packages/L2-13/tests/jest/spec.jest.test.js
packages/L2-13/tests/vitest/spec.test.js
packages/L2-14/package.json
packages/L2-14/src/index.js
packages/L2-14/tests/jest/spec.jest.test.js
packages/L2-14/tests/vitest/spec.test.js
packages/L2-15/package.json
packages/L2-15/tests/jest/spec.jest.test.js
packages/L2-15/tests/vitest/spec.test.js
packages/L3-01/package.json
packages/L3-01/src/index.js
packages/L3-01/tests/jest/spec.jest.test.js
packages/L3-01/tests/vitest/spec.test.js
packages/L3-02/package.json
packages/L3-02/src/index.js
packages/L3-02/tests/jest/spec.jest.test.js
packages/L3-02/tests/vitest/spec.test.js
packages/L3-03/package.json
packages/L3-03/src/index.js
packages/L3-03/tests/jest/spec.jest.test.js
packages/L3-03/tests/vitest/spec.test.js
packages/L3-04/package.json
packages/L3-04/src/index.js
packages/L3-04/tests/jest/spec.jest.test.js
packages/L3-04/tests/vitest/spec.test.js
packages/L3-05/package.json
packages/L3-05/src/index.js
packages/L3-05/tests/jest/spec.jest.test.js
packages/L3-05/tests/vitest/spec.test.js
packages/L3-06/package.json
packages/L3-06/src/index.js
packages/L3-06/tests/jest/spec.jest.test.js
packages/L3-06/tests/vitest/spec.test.js
packages/L3-07/package.json
packages/L3-07/src/index.js
packages/L3-07/tests/jest/spec.jest.test.js
packages/L3-07/tests/vitest/spec.test.js
packages/L3-07/web/index.html
packages/L3-07/web/report.json
packages/L3-07/web/script.js
packages/L3-08/package.json
packages/L3-08/src/index.js
packages/L3-08/tests/jest/spec.jest.test.js
packages/L3-08/tests/vitest/spec.test.js
packages/L3-09/package.json
packages/L3-09/src/index.js
packages/L3-09/tests/jest/spec.jest.test.js
packages/L3-09/tests/vitest/spec.test.js
packages/L3-10/package.json
packages/L3-10/src/index.js
packages/L3-10/tests/jest/spec.jest.test.js
packages/L3-10/tests/vitest/spec.test.js
packages/L3-11/package.json
packages/L3-11/src/index.js
packages/L3-11/tests/jest/spec.jest.test.js
packages/L3-11/tests/vitest/spec.test.js
packages/L3-12/package.json
packages/L3-12/src/index.js
packages/L3-12/tests/jest/spec.jest.test.js
packages/L3-12/tests/vitest/spec.test.js
packages/L3-13/package.json
packages/L3-13/src/index.js
packages/L3-13/tests/jest/spec.jest.test.js
packages/L3-13/tests/vitest/spec.test.js
packages/L3-14/package.json
packages/L3-14/src/index.js
packages/L3-14/tests/jest/spec.jest.test.js
packages/L3-14/tests/vitest/spec.test.js
packages/L3-15/package.json
packages/L3-15/src/index.js
packages/L3-15/tests/jest/spec.jest.test.js
packages/L3-15/tests/vitest/spec.test.js
playwright.config.ts
pnpm-workspace.yaml
scripts/build-sw.js
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 52, other: 3, code: 44, tests: 90, public: 1, ci: 5.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s2p3-monorepo` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `pnpm -r --filter './packages/*' exec vitest run --reporter verbose`
  - `test:jest` → `pnpm -r --filter './packages/*' exec jest --runInBand`
  - `test` → `pnpm run test:vitest && pnpm run test:jest`
  - `e2e` → `pnpm -r --filter './packages/L3-*' exec playwright test`
  - `workbox` → `pnpm -r --filter './packages/L3-*' exec node ../../scripts/build-sw.js`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/L1-01/package.json`: name=`@s2/L1-01` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-02/package.json`: name=`@s2/L1-02` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-03/package.json`: name=`@s2/L1-03` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-04/package.json`: name=`@s2/L1-04` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-05/package.json`: name=`@s2/L1-05` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-06/package.json`: name=`@s2/L1-06` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-07/package.json`: name=`@s2/L1-07` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-08/package.json`: name=`@s2/L1-08` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-09/package.json`: name=`@s2/L1-09` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-10/package.json`: name=`@s2/L1-10` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-11/package.json`: name=`@s2/L1-11` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-12/package.json`: name=`@s2/L1-12` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-13/package.json`: name=`@s2/L1-13` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-14/package.json`: name=`@s2/L1-14` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-15/package.json`: name=`@s2/L1-15` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-01/package.json`: name=`@s2/L2-01` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-02/package.json`: name=`@s2/L2-02` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-03/package.json`: name=`@s2/L2-03` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-04/package.json`: name=`@s2/L2-04` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-05/package.json`: name=`@s2/L2-05` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-06/package.json`: name=`@s2/L2-06` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-07/package.json`: name=`@s2/L2-07` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-08/package.json`: name=`@s2/L2-08` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-09/package.json`: name=`@s2/L2-09` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-10/package.json`: name=`@s2/L2-10` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-11/package.json`: name=`@s2/L2-11` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-12/package.json`: name=`@s2/L2-12` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-13/package.json`: name=`@s2/L2-13` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-14/package.json`: name=`@s2/L2-14` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-15/package.json`: name=`@s2/L2-15` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-01/package.json`: name=`@s2/L3-01` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-02/package.json`: name=`@s2/L3-02` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-03/package.json`: name=`@s2/L3-03` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-04/package.json`: name=`@s2/L3-04` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-05/package.json`: name=`@s2/L3-05` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-06/package.json`: name=`@s2/L3-06` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-07/package.json`: name=`@s2/L3-07` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-08/package.json`: name=`@s2/L3-08` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-09/package.json`: name=`@s2/L3-09` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-10/package.json`: name=`@s2/L3-10` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-11/package.json`: name=`@s2/L3-11` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-12/package.json`: name=`@s2/L3-12` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-13/package.json`: name=`@s2/L3-13` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-14/package.json`: name=`@s2/L3-14` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-15/package.json`: name=`@s2/L3-15` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`

### Seminar2_Partea3_p3-standalone.zip

```
.github/workflows/e2e.yml
.github/workflows/lint.yml
.github/workflows/unit-jest.yml
.github/workflows/unit-vitest.yml
.github/workflows/workbox-sw.yml
.gitignore
README.md
babel.config.cjs
eslint.config.mjs
jest.config.cjs
package.json
playwright.config.ts
projects/L1-01/solution/README.md
projects/L1-01/solution/src/index.js
projects/L1-01/solution/tests/jest/spec.jest.test.js
projects/L1-01/solution/tests/vitest/spec.test.js
projects/L1-01/starter/README.md
projects/L1-01/starter/src/index.js
projects/L1-01/starter/tests/jest/spec.jest.test.js
projects/L1-01/starter/tests/vitest/spec.test.js
projects/L1-02/solution/README.md
projects/L1-02/solution/src/index.js
projects/L1-02/solution/tests/jest/spec.jest.test.js
projects/L1-02/solution/tests/vitest/spec.test.js
projects/L1-02/starter/README.md
projects/L1-02/starter/src/index.js
projects/L1-02/starter/tests/jest/spec.jest.test.js
projects/L1-02/starter/tests/vitest/spec.test.js
projects/L1-03/solution/README.md
projects/L1-03/solution/src/index.js
projects/L1-03/solution/tests/jest/spec.jest.test.js
projects/L1-03/solution/tests/vitest/spec.test.js
projects/L1-03/starter/README.md
projects/L1-03/starter/src/index.js
projects/L1-03/starter/tests/jest/spec.jest.test.js
projects/L1-03/starter/tests/vitest/spec.test.js
projects/L1-04/solution/README.md
projects/L1-04/solution/src/index.js
projects/L1-04/solution/tests/jest/spec.jest.test.js
projects/L1-04/solution/tests/vitest/spec.test.js
projects/L1-04/starter/README.md
projects/L1-04/starter/src/index.js
projects/L1-04/starter/tests/jest/spec.jest.test.js
projects/L1-04/starter/tests/vitest/spec.test.js
projects/L1-05/solution/README.md
projects/L1-05/solution/src/index.js
projects/L1-05/solution/tests/jest/spec.jest.test.js
projects/L1-05/solution/tests/vitest/spec.test.js
projects/L1-05/starter/README.md
projects/L1-05/starter/src/index.js
projects/L1-05/starter/tests/jest/spec.jest.test.js
projects/L1-05/starter/tests/vitest/spec.test.js
projects/L1-06/solution/README.md
projects/L1-06/solution/src/index.js
projects/L1-06/solution/tests/jest/spec.jest.test.js
projects/L1-06/solution/tests/vitest/spec.test.js
projects/L1-06/starter/README.md
projects/L1-06/starter/src/index.js
projects/L1-06/starter/tests/jest/spec.jest.test.js
projects/L1-06/starter/tests/vitest/spec.test.js
projects/L1-07/solution/README.md
projects/L1-07/solution/src/index.js
projects/L1-07/solution/tests/jest/spec.jest.test.js
projects/L1-07/solution/tests/vitest/spec.test.js
projects/L1-07/starter/README.md
projects/L1-07/starter/src/index.js
projects/L1-07/starter/tests/jest/spec.jest.test.js
projects/L1-07/starter/tests/vitest/spec.test.js
projects/L1-08/solution/README.md
projects/L1-08/solution/src/index.js
projects/L1-08/solution/tests/jest/spec.jest.test.js
projects/L1-08/solution/tests/vitest/spec.test.js
projects/L1-08/starter/README.md
projects/L1-08/starter/src/index.js
projects/L1-08/starter/tests/jest/spec.jest.test.js
projects/L1-08/starter/tests/vitest/spec.test.js
projects/L1-09/solution/README.md
projects/L1-09/solution/src/index.js
projects/L1-09/solution/tests/jest/spec.jest.test.js
projects/L1-09/solution/tests/vitest/spec.test.js
projects/L1-09/starter/README.md
projects/L1-09/starter/src/index.js
projects/L1-09/starter/tests/jest/spec.jest.test.js
projects/L1-09/starter/tests/vitest/spec.test.js
projects/L1-10/solution/README.md
projects/L1-10/solution/src/index.js
projects/L1-10/solution/tests/jest/spec.jest.test.js
projects/L1-10/solution/tests/vitest/spec.test.js
projects/L1-10/starter/README.md
projects/L1-10/starter/src/index.js
projects/L1-10/starter/tests/jest/spec.jest.test.js
projects/L1-10/starter/tests/vitest/spec.test.js
projects/L1-11/solution/README.md
projects/L1-11/solution/src/index.js
projects/L1-11/solution/tests/jest/spec.jest.test.js
projects/L1-11/solution/tests/vitest/spec.test.js
projects/L1-11/starter/README.md
projects/L1-11/starter/src/index.js
projects/L1-11/starter/tests/jest/spec.jest.test.js
projects/L1-11/starter/tests/vitest/spec.test.js
projects/L1-12/solution/README.md
projects/L1-12/solution/src/index.js
projects/L1-12/solution/tests/jest/spec.jest.test.js
projects/L1-12/solution/tests/vitest/spec.test.js
projects/L1-12/starter/README.md
projects/L1-12/starter/src/index.js
projects/L1-12/starter/tests/jest/spec.jest.test.js
projects/L1-12/starter/tests/vitest/spec.test.js
projects/L1-13/solution/README.md
projects/L1-13/solution/src/index.js
projects/L1-13/solution/tests/jest/spec.jest.test.js
projects/L1-13/solution/tests/vitest/spec.test.js
projects/L1-13/starter/README.md
projects/L1-13/starter/src/index.js
projects/L1-13/starter/tests/jest/spec.jest.test.js
projects/L1-13/starter/tests/vitest/spec.test.js
projects/L1-14/solution/README.md
projects/L1-14/solution/src/index.js
projects/L1-14/solution/tests/jest/spec.jest.test.js
projects/L1-14/solution/tests/vitest/spec.test.js
projects/L1-14/starter/README.md
projects/L1-14/starter/src/index.js
projects/L1-14/starter/tests/jest/spec.jest.test.js
projects/L1-14/starter/tests/vitest/spec.test.js
projects/L1-15/solution/README.md
projects/L1-15/solution/src/index.js
projects/L1-15/solution/tests/jest/spec.jest.test.js
projects/L1-15/solution/tests/vitest/spec.test.js
projects/L1-15/starter/README.md
projects/L1-15/starter/src/index.js
projects/L1-15/starter/tests/jest/spec.jest.test.js
projects/L1-15/starter/tests/vitest/spec.test.js
projects/L2-01/solution/README.md
projects/L2-01/solution/src/index.js
projects/L2-01/solution/tests/jest/spec.jest.test.js
projects/L2-01/solution/tests/vitest/spec.test.js
projects/L2-01/starter/README.md
projects/L2-01/starter/src/index.js
projects/L2-01/starter/tests/jest/spec.jest.test.js
projects/L2-01/starter/tests/vitest/spec.test.js
projects/L2-02/solution/README.md
projects/L2-02/solution/src/index.js
projects/L2-02/solution/tests/jest/spec.jest.test.js
projects/L2-02/solution/tests/vitest/spec.test.js
projects/L2-02/starter/README.md
projects/L2-02/starter/src/index.js
projects/L2-02/starter/tests/jest/spec.jest.test.js
projects/L2-02/starter/tests/vitest/spec.test.js
projects/L2-03/solution/README.md
projects/L2-03/solution/src/index.js
projects/L2-03/solution/tests/jest/spec.jest.test.js
projects/L2-03/solution/tests/vitest/spec.test.js
projects/L2-03/starter/README.md
projects/L2-03/starter/src/index.js
projects/L2-03/starter/tests/jest/spec.jest.test.js
projects/L2-03/starter/tests/vitest/spec.test.js
projects/L2-04/solution/README.md
projects/L2-04/solution/src/index.js
projects/L2-04/solution/tests/jest/spec.jest.test.js
projects/L2-04/solution/tests/vitest/spec.test.js
projects/L2-04/starter/README.md
projects/L2-04/starter/src/index.js
projects/L2-04/starter/tests/jest/spec.jest.test.js
projects/L2-04/starter/tests/vitest/spec.test.js
projects/L2-05/solution/README.md
projects/L2-05/solution/src/index.js
projects/L2-05/solution/tests/jest/spec.jest.test.js
projects/L2-05/solution/tests/vitest/spec.test.js
projects/L2-05/starter/README.md
projects/L2-05/starter/src/index.js
projects/L2-05/starter/tests/jest/spec.jest.test.js
projects/L2-05/starter/tests/vitest/spec.test.js
projects/L2-06/solution/README.md
projects/L2-06/solution/src/index.js
projects/L2-06/solution/tests/jest/spec.jest.test.js
projects/L2-06/solution/tests/vitest/spec.test.js
projects/L2-06/starter/README.md
projects/L2-06/starter/src/index.js
projects/L2-06/starter/tests/jest/spec.jest.test.js
projects/L2-06/starter/tests/vitest/spec.test.js
projects/L2-07/solution/README.md
projects/L2-07/solution/src/index.js
projects/L2-07/solution/tests/jest/spec.jest.test.js
projects/L2-07/solution/tests/vitest/spec.test.js
projects/L2-07/starter/README.md
projects/L2-07/starter/src/index.js
projects/L2-07/starter/tests/jest/spec.jest.test.js
projects/L2-07/starter/tests/vitest/spec.test.js
projects/L2-08/solution/README.md
projects/L2-08/solution/src/index.js
projects/L2-08/solution/tests/jest/spec.jest.test.js
projects/L2-08/solution/tests/vitest/spec.test.js
projects/L2-08/starter/README.md
projects/L2-08/starter/src/index.js
projects/L2-08/starter/tests/jest/spec.jest.test.js
projects/L2-08/starter/tests/vitest/spec.test.js
projects/L2-09/solution/README.md
projects/L2-09/solution/src/index.js
projects/L2-09/solution/tests/jest/spec.jest.test.js
projects/L2-09/solution/tests/vitest/spec.test.js
projects/L2-09/starter/README.md
projects/L2-09/starter/src/index.js
projects/L2-09/starter/tests/jest/spec.jest.test.js
projects/L2-09/starter/tests/vitest/spec.test.js
projects/L2-10/solution/README.md
projects/L2-10/solution/src/index.js
projects/L2-10/solution/tests/jest/spec.jest.test.js
projects/L2-10/solution/tests/vitest/spec.test.js
projects/L2-10/starter/README.md
projects/L2-10/starter/src/index.js
projects/L2-10/starter/tests/jest/spec.jest.test.js
projects/L2-10/starter/tests/vitest/spec.test.js
projects/L2-11/solution/README.md
projects/L2-11/solution/src/index.js
projects/L2-11/solution/tests/jest/spec.jest.test.js
projects/L2-11/solution/tests/vitest/spec.test.js
projects/L2-11/starter/README.md
projects/L2-11/starter/src/index.js
projects/L2-11/starter/tests/jest/spec.jest.test.js
projects/L2-11/starter/tests/vitest/spec.test.js
projects/L2-12/solution/README.md
projects/L2-12/solution/src/index.js
projects/L2-12/solution/tests/jest/spec.jest.test.js
projects/L2-12/solution/tests/vitest/spec.test.js
projects/L2-12/starter/README.md
projects/L2-12/starter/src/index.js
projects/L2-12/starter/tests/jest/spec.jest.test.js
projects/L2-12/starter/tests/vitest/spec.test.js
projects/L2-13/solution/README.md
projects/L2-13/solution/src/index.js
projects/L2-13/solution/tests/jest/spec.jest.test.js
projects/L2-13/solution/tests/vitest/spec.test.js
projects/L2-13/starter/README.md
projects/L2-13/starter/src/index.js
projects/L2-13/starter/tests/jest/spec.jest.test.js
projects/L2-13/starter/tests/vitest/spec.test.js
projects/L2-14/solution/README.md
projects/L2-14/solution/src/index.js
projects/L2-14/solution/tests/jest/spec.jest.test.js
projects/L2-14/solution/tests/vitest/spec.test.js
projects/L2-14/starter/README.md
projects/L2-14/starter/src/index.js
projects/L2-14/starter/tests/jest/spec.jest.test.js
projects/L2-14/starter/tests/vitest/spec.test.js
projects/L2-15/solution/README.md
projects/L2-15/solution/tests/jest/spec.jest.test.js
projects/L2-15/solution/tests/vitest/spec.test.js
projects/L2-15/starter/README.md
projects/L2-15/starter/tests/jest/spec.jest.test.js
projects/L2-15/starter/tests/vitest/spec.test.js
projects/L3-01/solution/README.md
projects/L3-01/solution/src/index.js
projects/L3-01/solution/tests/jest/spec.jest.test.js
projects/L3-01/solution/tests/vitest/spec.test.js
projects/L3-01/starter/README.md
projects/L3-01/starter/src/index.js
projects/L3-01/starter/tests/jest/spec.jest.test.js
projects/L3-01/starter/tests/vitest/spec.test.js
projects/L3-02/solution/README.md
projects/L3-02/solution/src/index.js
projects/L3-02/solution/tests/jest/spec.jest.test.js
projects/L3-02/solution/tests/vitest/spec.test.js
projects/L3-02/starter/README.md
projects/L3-02/starter/src/index.js
projects/L3-02/starter/tests/jest/spec.jest.test.js
projects/L3-02/starter/tests/vitest/spec.test.js
projects/L3-03/solution/README.md
projects/L3-03/solution/src/index.js
projects/L3-03/solution/tests/jest/spec.jest.test.js
projects/L3-03/solution/tests/vitest/spec.test.js
projects/L3-03/starter/README.md
projects/L3-03/starter/src/index.js
projects/L3-03/starter/tests/jest/spec.jest.test.js
projects/L3-03/starter/tests/vitest/spec.test.js
projects/L3-04/solution/README.md
projects/L3-04/solution/src/index.js
projects/L3-04/solution/tests/jest/spec.jest.test.js
projects/L3-04/solution/tests/vitest/spec.test.js
projects/L3-04/starter/README.md
projects/L3-04/starter/src/index.js
projects/L3-04/starter/tests/jest/spec.jest.test.js
projects/L3-04/starter/tests/vitest/spec.test.js
projects/L3-05/solution/README.md
projects/L3-05/solution/src/index.js
projects/L3-05/solution/tests/jest/spec.jest.test.js
projects/L3-05/solution/tests/vitest/spec.test.js
projects/L3-05/starter/README.md
projects/L3-05/starter/src/index.js
projects/L3-05/starter/tests/jest/spec.jest.test.js
projects/L3-05/starter/tests/vitest/spec.test.js
projects/L3-06/solution/README.md
projects/L3-06/solution/src/index.js
projects/L3-06/solution/tests/jest/spec.jest.test.js
projects/L3-06/solution/tests/vitest/spec.test.js
projects/L3-06/starter/README.md
projects/L3-06/starter/src/index.js
projects/L3-06/starter/tests/jest/spec.jest.test.js
projects/L3-06/starter/tests/vitest/spec.test.js
projects/L3-07/solution/README.md
projects/L3-07/solution/src/index.js
projects/L3-07/solution/tests/jest/spec.jest.test.js
projects/L3-07/solution/tests/vitest/spec.test.js
projects/L3-07/starter/README.md
projects/L3-07/starter/src/index.js
projects/L3-07/starter/tests/e2e/viewer.spec.ts
projects/L3-07/starter/tests/jest/spec.jest.test.js
projects/L3-07/starter/tests/vitest/spec.test.js
projects/L3-07/starter/web/index.html
projects/L3-07/starter/web/report.json
projects/L3-07/starter/web/script.js
projects/L3-08/solution/README.md
projects/L3-08/solution/src/index.js
projects/L3-08/solution/tests/jest/spec.jest.test.js
projects/L3-08/solution/tests/vitest/spec.test.js
projects/L3-08/starter/README.md
projects/L3-08/starter/src/index.js
projects/L3-08/starter/tests/jest/spec.jest.test.js
projects/L3-08/starter/tests/vitest/spec.test.js
projects/L3-09/solution/README.md
projects/L3-09/solution/src/index.js
projects/L3-09/solution/tests/jest/spec.jest.test.js
projects/L3-09/solution/tests/vitest/spec.test.js
projects/L3-09/starter/README.md
projects/L3-09/starter/src/index.js
projects/L3-09/starter/tests/jest/spec.jest.test.js
projects/L3-09/starter/tests/vitest/spec.test.js
projects/L3-10/solution/README.md
projects/L3-10/solution/src/index.js
projects/L3-10/solution/tests/jest/spec.jest.test.js
projects/L3-10/solution/tests/vitest/spec.test.js
projects/L3-10/starter/README.md
projects/L3-10/starter/src/index.js
projects/L3-10/starter/tests/jest/spec.jest.test.js
projects/L3-10/starter/tests/vitest/spec.test.js
projects/L3-11/solution/README.md
projects/L3-11/solution/src/index.js
projects/L3-11/solution/tests/jest/spec.jest.test.js
projects/L3-11/solution/tests/vitest/spec.test.js
projects/L3-11/starter/README.md
projects/L3-11/starter/src/index.js
projects/L3-11/starter/tests/jest/spec.jest.test.js
projects/L3-11/starter/tests/vitest/spec.test.js
projects/L3-12/solution/README.md
projects/L3-12/solution/src/index.js
projects/L3-12/solution/tests/jest/spec.jest.test.js
projects/L3-12/solution/tests/vitest/spec.test.js
projects/L3-12/starter/README.md
projects/L3-12/starter/src/index.js
projects/L3-12/starter/tests/jest/spec.jest.test.js
projects/L3-12/starter/tests/vitest/spec.test.js
projects/L3-13/solution/README.md
projects/L3-13/solution/src/index.js
projects/L3-13/solution/tests/jest/spec.jest.test.js
projects/L3-13/solution/tests/vitest/spec.test.js
projects/L3-13/starter/README.md
projects/L3-13/starter/src/index.js
projects/L3-13/starter/tests/jest/spec.jest.test.js
projects/L3-13/starter/tests/vitest/spec.test.js
projects/L3-14/solution/README.md
projects/L3-14/solution/src/index.js
projects/L3-14/solution/tests/jest/spec.jest.test.js
projects/L3-14/solution/tests/vitest/spec.test.js
projects/L3-14/starter/README.md
projects/L3-14/starter/src/index.js
projects/L3-14/starter/tests/jest/spec.jest.test.js
projects/L3-14/starter/tests/vitest/spec.test.js
projects/L3-15/solution/README.md
projects/L3-15/solution/src/index.js
projects/L3-15/solution/tests/jest/spec.jest.test.js
projects/L3-15/solution/tests/vitest/spec.test.js
projects/L3-15/starter/README.md
projects/L3-15/starter/src/index.js
projects/L3-15/starter/tests/jest/spec.jest.test.js
projects/L3-15/starter/tests/vitest/spec.test.js
scripts/build-sw.js
server.js
vitest.config.ts
```

**Variante detectate:** solution: 179, starter: 183.

**Categorii de fișiere:** config: 7, other: 4, docs: 91, code: 88, tests: 181, public: 1, ci: 5.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s2p3-standalone` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `serve` → `node server.js`
  - `e2e` → `playwright test`
  - `workbox` → `node scripts/build-sw.js`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build

### Seminar2_Partea3_p3-READMEs.zip

```
L1-01.README.md
L1-02.README.md
L1-03.README.md
L1-04.README.md
L1-05.README.md
L1-06.README.md
L1-07.README.md
L1-08.README.md
L1-09.README.md
L1-10.README.md
L1-11.README.md
L1-12.README.md
L1-13.README.md
L1-14.README.md
L1-15.README.md
L2-01.README.md
L2-02.README.md
L2-03.README.md
L2-04.README.md
L2-05.README.md
L2-06.README.md
L2-07.README.md
L2-08.README.md
L2-09.README.md
L2-10.README.md
L2-11.README.md
L2-12.README.md
L2-13.README.md
L2-14.README.md
L2-15.README.md
L3-01.README.md
L3-02.README.md
L3-03.README.md
L3-04.README.md
L3-05.README.md
L3-06.README.md
L3-07.README.md
L3-08.README.md
L3-09.README.md
L3-10.README.md
L3-11.README.md
L3-12.README.md
L3-13.README.md
L3-14.README.md
L3-15.README.md
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** docs: 45.

## 2. Sinteza documentelor DOCX (teorie ↔ laborator ↔ proiecte)

### Seminar2_Partea1_Teorie.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 2 — Partea 1 (Teorie, extins)
- Seminarul 2 — Partea 1 (Teorie, extins)
- Titlu: De la liste brute la informație utilă — funcții și array‑uri în JavaScript (map / filter / reduce, utilitare, chaining)

### Seminar2_Partea2_Laborator.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 2 — Partea 2 (Laborator, extins)
- Seminarul 2 — Partea 2 (Laborator, extins): „De la micro‑utilitare la pipeline robust”

### Seminar2_Partea2_P2_Ghid_Arhiva.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhivă s2p2-lab.zip
- Conținutul arhivei:
- s2p2-lab/

### Seminar2_Partea3_P3_Arhive_Ghid.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhive Partea 3
- Arhive:
- • s2p3-standalone.zip — proiect unic cu 45 proiecte (starter+solution), toolchain comun.

### Seminar2_Partea3_Proiecte_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 2 — Partea 3 (Proiecte/teme extinse)
- Această parte conține 45 de proiecte (15 × L1/L2/L3), fiecare cu specificații și soluții (idee + algoritm), aliniate la principiile Partelor 1–2: funcții pure, compoziție declarativă, contracte testabile, suite Vitest/Jest în oglindă. Arhivele asociate includ variante starter/solution, o variantă monorepo (PNPM workspaces) și workflows CI (lint, unit-vitest, unit-jest, e2e, workbox-sw). Proiectele L3 includ un viewer web static testat cu Playwright și pregătit pentru PWA prin Workbox.
- Nivel L1 (Fundamental) — L1-01: Top‑K interese (map/flatMap → countBy → sort stabil → slice)

## 3. Monorepo vs. standalone — analiză comparativă


**Manageri de pachete & workspaces.** Variantele monorepo folosesc `pnpm-workspace.yaml` și/sau `workspaces` în `package.json` pentru orchestrare; standalone izolează dependențele pe proiect.

**Comenzi de instalare/testare.** Monorepo: `pnpm i -w`, `pnpm --filter <pkg> run test`. Standalone: `npm i`, `npm test`. Suitele sunt **oglindite** (Vitest & Jest), pe aceleași contracte funcționale. 

**Integrare CI.** Monorepo agregă workflows (lint, unit Vitest/Jest, e2e/Workbox la L3), în timp ce standalone le definește per proiect.

**Avantaje/Dezavantaje.** Standalone — simplitate cognitivă (ideal începători). Monorepo — scalabil pentru seturi mari (ex. 45 proiecte L1–L3), partajare de configuri și execuții rapide în CI; cost: curba PNPM și filtrarea pachetelor.
## 4. Rolul fișierelor cheie (config, cod, teste, extra)

| Fișier / tip | Rol |
|---|---|
| `package.json` | Manifest proiect: metadate, dependențe, scripturi. |
| `eslint.config.mjs` | Flat config ESLint; reguli minime pentru stil & erori comune. |
| `vitest.config.ts` | Configurare Vitest (env node/jsdom). |
| `jest.config.cjs` | Configurare Jest (babel-jest la nevoie). |
| `babel.config.cjs` | Preseturi pentru Jest (`@babel/preset-env`). |
| `pnpm-workspace.yaml` | Workspace PNPM pentru monorepo. |
| `src/lib/collect.js` | Utilitare pure (groupBy, countBy, keyBy, partition, uniqBy, difference/intersection, chunk/zip/flatten, compact). |
| `src/lib/predicates.js` | Predicates: byFaculty/hasInterest/isValidRecord. |
| `src/lib/sorters.js` | Comparatoare deterministe (byCountThenAlpha). |
| `src/lib/normalize.js` | Adaptor de normalizare pentru CSV/JSON (canon e‑mail, faculty, interests). |
| `src/cli-runner.js` | Orchestrator `run(argv, io)`; compune pipeline + formate `table|json`. |
| `bin/cli.js` | Entry CLI; parsează argv și apelează runner-ul. |

## 5. Corelații cod ↔ configurări ↔ teste


- **Utilitare pure** (`src/lib/*`) sunt validate în **ambele suite** (Vitest & Jest) pe **aceleași contracte** (ex.: `groupBy`, `countBy`, `uniqBy`, `difference/intersection`).  
- **Runner CLI** (`src/cli-runner.js`) are I/O injectabil pentru teste deterministe; `bin/cli.js` este doar stratul POSIX.  
- **`.env.example`** (dacă este prezent) documentează `REPORT_LIMIT`/`REF_DATE`; opțiunile CLI le pot suprascrie.  
- **ESLint + CI**: workflows rulează `lint` și `test` pe toate pachetele/proiectele; în L3 intervin **Playwright** (e2e) și **Workbox** (PWA).  
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S2 aprofundează **prelucrarea declarativă a listelor** prin `map/filter/reduce`, o trusă de **utilitare pure** și compoziții `pipe/compose/tap`. Teoria este mapată direct în laborator (mini‑bibliotecă + pipeline + CLI) și în proiectele Partea 3 (L1–L3) — variante **standalone** și **monorepo** — cu **teste în oglindă** (Vitest & Jest) pentru transfer de competență. ### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; rădăcină + `packages/*` |
| Instalare | `npm i` | `pnpm i -w` |
| Testare | `npm test` (Vitest & Jest) | `pnpm -w run test` sau `--filter` |
| CI | Workflows simple per proiect | Workflows agregate, matrice pe pachete |
| Scalare (45 proiecte) | multiplicare directoare | pachete dedicate în `packages/*` |
| Public țintă | începători | echipe/colecții avansate |
### Inventar pe arhivă (roluri)

- **Seminar2_Partea2_p2-lab.zip** — config=6, docs=1, other=3, code=6, tests=8.
- **Seminar2_Partea3_p3-monorepo.zip** — config=52, other=3, code=44, tests=90, public=1, ci=5.
- **Seminar2_Partea3_p3-standalone.zip** — config=7, other=4, docs=91, code=88, tests=181, public=1, ci=5.
- **Seminar2_Partea3_p3-READMEs.zip** — docs=45.
### Explicații fișier-cu-fișier

Consultați tabelul din §4; maparea exactă a utilitarelor/pipeline‑ului/CLI pe cerințele laboratorului și proiectelor este în ghiduri și worksheet. 
### Corelații între fișiere


- `src/lib/collect.js` ↔ `tests/*`: `groupBy`, `countBy`, `uniqBy`, `difference/intersection`, `chunk/zip/flatten/compact`.  
- `src/lib/predicates.js` & `src/lib/sorters.js` ↔ `tests/*`: `byFaculty`, `hasInterest`, `isValidRecord`, `byCountThenAlpha` (determinist).  
- `src/lib/normalize.js` ↔ `tests/*`: canon e‑mail/faculty/interests pentru CSV/JSON.  
- `src/cli-runner.js` & `bin/cli.js` ↔ `tests/*`: coduri de ieșire, opțiuni, formate.  
- `.github/workflows/*` ↔ `lint`/`test`: pipeline determinist pentru PR-uri.  
### Recomandări pentru studenți


1) **Separă logica de I/O** (funcții pure vs. runner/CLI).  
2) **Testează în oglindă** (Vitest & Jest) exact aceleași contracte.  
3) **Normalizează explicit** — nu te baza pe coerciuni implicite.  
4) **Comparatori stabili** — adaugă tie‑break alfabetic.  
5) **Documentează politicile** (duplicați, chei lipsă) în README per proiect.  
6) **CI** ca gardian: `lint` + `test` înainte de fiecare push.  
### Instrucțiuni „Quick start” per arhivă


**Partea 2 — laborator (p2-lab.zip):**
```bash
unzip "Seminar2_Partea2_p2-lab.zip" -d s2p2-lab
cd s2p2-lab
npm i
npm test            # rulează Vitest & Jest (oglindă)
npm run dev         # exemple pe data/sample.csv & data/sample.json
node bin/cli.js data/sample.csv --limit 5 --format json
```
**Partea 3 — standalone (p3-standalone.zip):**
```bash
unzip "Seminar2_Partea3_p3-standalone.zip" -d s2p3-standalone
cd s2p3-standalone/L1/L1-P01/starter
npm i
npm test
npm run dev
```
**Partea 3 — monorepo (p3-monorepo.zip, PNPM):**
```bash
unzip "Seminar2_Partea3_p3-monorepo.zip" -d s2p3-monorepo
cd s2p3-monorepo
pnpm i -w
pnpm --filter l1-p01-starter run test
pnpm --filter l1-p01-starter run dev
```
**Partea 3 — README-uri agregate (p3-READMEs.zip):**
```bash
unzip "Seminar2_Partea3_p3-READMEs.zip" -d s2p3-readmes
ls s2p3-readmes | head -n 10
```
### Troubleshooting (erori frecvente)


- **ESM în Jest** → configurează `babel-jest` + `extensionsToTreatAsEsm` (unde e cazul).  
- **CSV „zgomotos”** → normalizează delimitatori/newline; tratează antetul ca schemă.  
- **Nedeterminism la egalități** → adaugă tie‑break alfabetic (`Intl.Collator` dacă e necesar).  
- **Diferențe table vs. json** → separă strict `formatTable` de `toJSON`.  
- **CI roșu pe e2e/Workbox** (doar L3) → rulează `npm run pw:install` și `npm run build:sw`.  
- **PNPM filter** → verifică `pnpm-workspace.yaml` și câmpul `name` din `package.json`.  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** — map/filter/reduce, utilitare, compoziție, contracte; filozofia funcțională urmărită în tot pachetul.  
- **Partea 2 (Laborator & Ghid arhivă)** — mini‑bibliotecă + pipeline + CLI cu suite în oglindă și instrucțiuni de rulare.  
- **Partea 3 (Ghid & Proiecte)** — 45 proiecte L1–L3 (starter/solution), monorepo vs. standalone, CI, e2e & Workbox pentru L3.  
### Prompt-șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S2** (standalone & monorepo) o mini‑bibliotecă funcțională `src/lib/*` + `src/cli-runner.js` + `bin/cli.js`, cu **teste în oglindă** (Vitest & Jest), README cu Quick start & Troubleshooting, CI (lint/unit; e2e & Workbox doar la L3) și variante **starter**/**solution**. Contractele definesc comportamentele (map/filter/reduce, utilitare, comparator stabil, normalizare).”
