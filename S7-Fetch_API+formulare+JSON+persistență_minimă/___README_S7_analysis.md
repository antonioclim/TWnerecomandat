# Seminarul S7 — Fetch API + Formulare + JSON + Persitență minimă — Analiză integrată (standalone & monorepo)

*Generat la 2025-09-21 05:07.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar7_Partea2_p2-lab.zip

```
README.md
jest.config.cjs
package.json
public/enrol.html
public/index.html
server.mjs
src/api/fetchClient.js
src/forms/enrolController.js
src/forms/validation.js
src/main.js
src/pages/clubsPage.js
src/pages/enrolPage.js
src/services/clubs.js
src/utils/storage.js
styles.css
tests/fixtures/clubs.json
tests/fixtures/registration.ok.json
tests/fixtures/registration.problem.json
tests/unit/fetchClient.jest.test.cjs
tests/unit/fetchClient.vitest.test.ts
tests/unit/persistence.jest.test.cjs
tests/unit/persistence.vitest.test.ts
tests/unit/render.jest.test.cjs
tests/unit/render.vitest.test.ts
tests/unit/validation.jest.test.cjs
tests/unit/validation.vitest.test.ts
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** other: 1, config: 4, docs: 1, public: 2, code: 8, tests: 11.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`seminar7-part2-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors

### Seminar7_Partea2_p2-monorepo.zip

```
package.json
packages/app/README.md
packages/app/jest.config.cjs
packages/app/package.json
packages/app/public/enrol.html
packages/app/public/index.html
packages/app/server.mjs
packages/app/src/api/fetchClient.js
packages/app/src/forms/enrolController.js
packages/app/src/forms/validation.js
packages/app/src/main.js
packages/app/src/pages/clubsPage.js
packages/app/src/pages/enrolPage.js
packages/app/src/services/clubs.js
packages/app/src/utils/storage.js
packages/app/styles.css
packages/app/tests/fixtures/clubs.json
packages/app/tests/fixtures/registration.ok.json
packages/app/tests/fixtures/registration.problem.json
packages/app/tests/unit/fetchClient.jest.test.cjs
packages/app/tests/unit/fetchClient.vitest.test.ts
packages/app/tests/unit/persistence.jest.test.cjs
packages/app/tests/unit/persistence.vitest.test.ts
packages/app/tests/unit/render.jest.test.cjs
packages/app/tests/unit/render.vitest.test.ts
packages/app/tests/unit/validation.jest.test.cjs
packages/app/tests/unit/validation.vitest.test.ts
packages/app/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 6, other: 1, docs: 1, public: 2, code: 8, tests: 11.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s7p2-monorepo` type=`module` workspaces=True
  - **Scripturi:**
  - `dev` → `pnpm --filter ./packages/app run dev`
  - `test:vitest` → `pnpm -r --filter ./packages run test:vitest`
  - `test:jest` → `pnpm -r --filter ./packages run test:jest`
  - `test` → `pnpm -r --filter ./packages run test`
  - **Deps:** 
  - **DevDeps:** pnpm, vitest, jest, jsdom, express, cors
- `packages/app/package.json`: name=`seminar7-part2-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors

### Seminar7_Partea3_p3-monorepo.zip

```
package.json
packages/l1-p01/README.md
packages/l1-p01/jest.config.cjs
packages/l1-p01/package.json
packages/l1-p01/public/index.html
packages/l1-p01/server.mjs
packages/l1-p01/src/addons/advanced.js
packages/l1-p01/src/api/fetchClient.js
packages/l1-p01/src/forms/enrolController.js
packages/l1-p01/src/forms/validation.js
packages/l1-p01/src/main.js
packages/l1-p01/src/pages/clubsPage.js
packages/l1-p01/src/pages/enrolPage.js
packages/l1-p01/src/services/clubs.js
packages/l1-p01/src/utils/storage.js
packages/l1-p01/styles.css
packages/l1-p01/tests/config.json
packages/l1-p01/tests/fixtures/clubs.json
packages/l1-p01/tests/unit/patterns.jest.test.cjs
packages/l1-p01/tests/unit/patterns.vitest.test.ts
packages/l1-p01/vitest.config.ts
packages/l1-p02/README.md
packages/l1-p02/jest.config.cjs
packages/l1-p02/package.json
packages/l1-p02/public/index.html
packages/l1-p02/server.mjs
packages/l1-p02/src/addons/advanced.js
packages/l1-p02/src/api/fetchClient.js
packages/l1-p02/src/forms/enrolController.js
packages/l1-p02/src/forms/validation.js
packages/l1-p02/src/main.js
packages/l1-p02/src/pages/clubsPage.js
packages/l1-p02/src/pages/enrolPage.js
packages/l1-p02/src/services/clubs.js
packages/l1-p02/src/utils/storage.js
packages/l1-p02/styles.css
packages/l1-p02/tests/config.json
packages/l1-p02/tests/fixtures/clubs.json
packages/l1-p02/tests/unit/patterns.jest.test.cjs
packages/l1-p02/tests/unit/patterns.vitest.test.ts
packages/l1-p02/vitest.config.ts
packages/l1-p03/README.md
packages/l1-p03/jest.config.cjs
packages/l1-p03/package.json
packages/l1-p03/public/index.html
packages/l1-p03/server.mjs
packages/l1-p03/src/addons/advanced.js
packages/l1-p03/src/api/fetchClient.js
packages/l1-p03/src/forms/enrolController.js
packages/l1-p03/src/forms/validation.js
packages/l1-p03/src/main.js
packages/l1-p03/src/pages/clubsPage.js
packages/l1-p03/src/pages/enrolPage.js
packages/l1-p03/src/services/clubs.js
packages/l1-p03/src/utils/storage.js
packages/l1-p03/styles.css
packages/l1-p03/tests/config.json
packages/l1-p03/tests/fixtures/clubs.json
packages/l1-p03/tests/unit/patterns.jest.test.cjs
packages/l1-p03/tests/unit/patterns.vitest.test.ts
packages/l1-p03/vitest.config.ts
packages/l1-p04/README.md
packages/l1-p04/jest.config.cjs
packages/l1-p04/package.json
packages/l1-p04/public/index.html
packages/l1-p04/server.mjs
packages/l1-p04/src/addons/advanced.js
packages/l1-p04/src/api/fetchClient.js
packages/l1-p04/src/forms/enrolController.js
packages/l1-p04/src/forms/validation.js
packages/l1-p04/src/main.js
packages/l1-p04/src/pages/clubsPage.js
packages/l1-p04/src/pages/enrolPage.js
packages/l1-p04/src/services/clubs.js
packages/l1-p04/src/utils/storage.js
packages/l1-p04/styles.css
packages/l1-p04/tests/config.json
packages/l1-p04/tests/fixtures/clubs.json
packages/l1-p04/tests/unit/patterns.jest.test.cjs
packages/l1-p04/tests/unit/patterns.vitest.test.ts
packages/l1-p04/vitest.config.ts
packages/l1-p05/README.md
packages/l1-p05/jest.config.cjs
packages/l1-p05/package.json
packages/l1-p05/public/index.html
packages/l1-p05/server.mjs
packages/l1-p05/src/addons/advanced.js
packages/l1-p05/src/api/fetchClient.js
packages/l1-p05/src/forms/enrolController.js
packages/l1-p05/src/forms/validation.js
packages/l1-p05/src/main.js
packages/l1-p05/src/pages/clubsPage.js
packages/l1-p05/src/pages/enrolPage.js
packages/l1-p05/src/services/clubs.js
packages/l1-p05/src/utils/storage.js
packages/l1-p05/styles.css
packages/l1-p05/tests/config.json
packages/l1-p05/tests/fixtures/clubs.json
packages/l1-p05/tests/unit/patterns.jest.test.cjs
packages/l1-p05/tests/unit/patterns.vitest.test.ts
packages/l1-p05/vitest.config.ts
packages/l1-p06/README.md
packages/l1-p06/jest.config.cjs
packages/l1-p06/package.json
packages/l1-p06/public/index.html
packages/l1-p06/server.mjs
packages/l1-p06/src/addons/advanced.js
packages/l1-p06/src/api/fetchClient.js
packages/l1-p06/src/forms/enrolController.js
packages/l1-p06/src/forms/validation.js
packages/l1-p06/src/main.js
packages/l1-p06/src/pages/clubsPage.js
packages/l1-p06/src/pages/enrolPage.js
packages/l1-p06/src/services/clubs.js
packages/l1-p06/src/utils/storage.js
packages/l1-p06/styles.css
packages/l1-p06/tests/config.json
packages/l1-p06/tests/fixtures/clubs.json
packages/l1-p06/tests/unit/patterns.jest.test.cjs
packages/l1-p06/tests/unit/patterns.vitest.test.ts
packages/l1-p06/vitest.config.ts
packages/l1-p07/README.md
packages/l1-p07/jest.config.cjs
packages/l1-p07/package.json
packages/l1-p07/public/index.html
packages/l1-p07/server.mjs
packages/l1-p07/src/addons/advanced.js
packages/l1-p07/src/api/fetchClient.js
packages/l1-p07/src/forms/enrolController.js
packages/l1-p07/src/forms/validation.js
packages/l1-p07/src/main.js
packages/l1-p07/src/pages/clubsPage.js
packages/l1-p07/src/pages/enrolPage.js
packages/l1-p07/src/services/clubs.js
packages/l1-p07/src/utils/storage.js
packages/l1-p07/styles.css
packages/l1-p07/tests/config.json
packages/l1-p07/tests/fixtures/clubs.json
packages/l1-p07/tests/unit/patterns.jest.test.cjs
packages/l1-p07/tests/unit/patterns.vitest.test.ts
packages/l1-p07/vitest.config.ts
packages/l1-p08/README.md
packages/l1-p08/jest.config.cjs
packages/l1-p08/package.json
packages/l1-p08/public/index.html
packages/l1-p08/server.mjs
packages/l1-p08/src/addons/advanced.js
packages/l1-p08/src/api/fetchClient.js
packages/l1-p08/src/forms/enrolController.js
packages/l1-p08/src/forms/validation.js
packages/l1-p08/src/main.js
packages/l1-p08/src/pages/clubsPage.js
packages/l1-p08/src/pages/enrolPage.js
packages/l1-p08/src/services/clubs.js
packages/l1-p08/src/utils/storage.js
packages/l1-p08/styles.css
packages/l1-p08/tests/config.json
packages/l1-p08/tests/fixtures/clubs.json
packages/l1-p08/tests/unit/patterns.jest.test.cjs
packages/l1-p08/tests/unit/patterns.vitest.test.ts
packages/l1-p08/vitest.config.ts
packages/l1-p09/README.md
packages/l1-p09/jest.config.cjs
packages/l1-p09/package.json
packages/l1-p09/public/index.html
packages/l1-p09/server.mjs
packages/l1-p09/src/addons/advanced.js
packages/l1-p09/src/api/fetchClient.js
packages/l1-p09/src/forms/enrolController.js
packages/l1-p09/src/forms/validation.js
packages/l1-p09/src/main.js
packages/l1-p09/src/pages/clubsPage.js
packages/l1-p09/src/pages/enrolPage.js
packages/l1-p09/src/services/clubs.js
packages/l1-p09/src/utils/storage.js
packages/l1-p09/styles.css
packages/l1-p09/tests/config.json
packages/l1-p09/tests/fixtures/clubs.json
packages/l1-p09/tests/unit/patterns.jest.test.cjs
packages/l1-p09/tests/unit/patterns.vitest.test.ts
packages/l1-p09/vitest.config.ts
packages/l1-p10/README.md
packages/l1-p10/jest.config.cjs
packages/l1-p10/package.json
packages/l1-p10/public/index.html
packages/l1-p10/server.mjs
packages/l1-p10/src/addons/advanced.js
packages/l1-p10/src/api/fetchClient.js
packages/l1-p10/src/forms/enrolController.js
packages/l1-p10/src/forms/validation.js
packages/l1-p10/src/main.js
packages/l1-p10/src/pages/clubsPage.js
packages/l1-p10/src/pages/enrolPage.js
packages/l1-p10/src/services/clubs.js
packages/l1-p10/src/utils/storage.js
packages/l1-p10/styles.css
packages/l1-p10/tests/config.json
packages/l1-p10/tests/fixtures/clubs.json
packages/l1-p10/tests/unit/patterns.jest.test.cjs
packages/l1-p10/tests/unit/patterns.vitest.test.ts
packages/l1-p10/vitest.config.ts
packages/l1-p11/README.md
packages/l1-p11/jest.config.cjs
packages/l1-p11/package.json
packages/l1-p11/public/index.html
packages/l1-p11/server.mjs
packages/l1-p11/src/addons/advanced.js
packages/l1-p11/src/api/fetchClient.js
packages/l1-p11/src/forms/enrolController.js
packages/l1-p11/src/forms/validation.js
packages/l1-p11/src/main.js
packages/l1-p11/src/pages/clubsPage.js
packages/l1-p11/src/pages/enrolPage.js
packages/l1-p11/src/services/clubs.js
packages/l1-p11/src/utils/storage.js
packages/l1-p11/styles.css
packages/l1-p11/tests/config.json
packages/l1-p11/tests/fixtures/clubs.json
packages/l1-p11/tests/unit/patterns.jest.test.cjs
packages/l1-p11/tests/unit/patterns.vitest.test.ts
packages/l1-p11/vitest.config.ts
packages/l1-p12/README.md
packages/l1-p12/jest.config.cjs
packages/l1-p12/package.json
packages/l1-p12/public/index.html
packages/l1-p12/server.mjs
packages/l1-p12/src/addons/advanced.js
packages/l1-p12/src/api/fetchClient.js
packages/l1-p12/src/forms/enrolController.js
packages/l1-p12/src/forms/validation.js
packages/l1-p12/src/main.js
packages/l1-p12/src/pages/clubsPage.js
packages/l1-p12/src/pages/enrolPage.js
packages/l1-p12/src/services/clubs.js
packages/l1-p12/src/utils/storage.js
packages/l1-p12/styles.css
packages/l1-p12/tests/config.json
packages/l1-p12/tests/fixtures/clubs.json
packages/l1-p12/tests/unit/patterns.jest.test.cjs
packages/l1-p12/tests/unit/patterns.vitest.test.ts
packages/l1-p12/vitest.config.ts
packages/l1-p13/README.md
packages/l1-p13/jest.config.cjs
packages/l1-p13/package.json
packages/l1-p13/public/index.html
packages/l1-p13/server.mjs
packages/l1-p13/src/addons/advanced.js
packages/l1-p13/src/api/fetchClient.js
packages/l1-p13/src/forms/enrolController.js
packages/l1-p13/src/forms/validation.js
packages/l1-p13/src/main.js
packages/l1-p13/src/pages/clubsPage.js
packages/l1-p13/src/pages/enrolPage.js
packages/l1-p13/src/services/clubs.js
packages/l1-p13/src/utils/storage.js
packages/l1-p13/styles.css
packages/l1-p13/tests/config.json
packages/l1-p13/tests/fixtures/clubs.json
packages/l1-p13/tests/unit/patterns.jest.test.cjs
packages/l1-p13/tests/unit/patterns.vitest.test.ts
packages/l1-p13/vitest.config.ts
packages/l1-p14/README.md
packages/l1-p14/jest.config.cjs
packages/l1-p14/package.json
packages/l1-p14/public/index.html
packages/l1-p14/server.mjs
packages/l1-p14/src/addons/advanced.js
packages/l1-p14/src/api/fetchClient.js
packages/l1-p14/src/forms/enrolController.js
packages/l1-p14/src/forms/validation.js
packages/l1-p14/src/main.js
packages/l1-p14/src/pages/clubsPage.js
packages/l1-p14/src/pages/enrolPage.js
packages/l1-p14/src/services/clubs.js
packages/l1-p14/src/utils/storage.js
packages/l1-p14/styles.css
packages/l1-p14/tests/config.json
packages/l1-p14/tests/fixtures/clubs.json
packages/l1-p14/tests/unit/patterns.jest.test.cjs
packages/l1-p14/tests/unit/patterns.vitest.test.ts
packages/l1-p14/vitest.config.ts
packages/l1-p15/README.md
packages/l1-p15/jest.config.cjs
packages/l1-p15/package.json
packages/l1-p15/public/index.html
packages/l1-p15/server.mjs
packages/l1-p15/src/addons/advanced.js
packages/l1-p15/src/api/fetchClient.js
packages/l1-p15/src/forms/enrolController.js
packages/l1-p15/src/forms/validation.js
packages/l1-p15/src/main.js
packages/l1-p15/src/pages/clubsPage.js
packages/l1-p15/src/pages/enrolPage.js
packages/l1-p15/src/services/clubs.js
packages/l1-p15/src/utils/storage.js
packages/l1-p15/styles.css
packages/l1-p15/tests/config.json
packages/l1-p15/tests/fixtures/clubs.json
packages/l1-p15/tests/unit/patterns.jest.test.cjs
packages/l1-p15/tests/unit/patterns.vitest.test.ts
packages/l1-p15/vitest.config.ts
packages/l2-p01/README.md
packages/l2-p01/jest.config.cjs
packages/l2-p01/package.json
packages/l2-p01/public/index.html
packages/l2-p01/server.mjs
packages/l2-p01/src/addons/advanced.js
packages/l2-p01/src/api/fetchClient.js
packages/l2-p01/src/forms/enrolController.js
packages/l2-p01/src/forms/validation.js
packages/l2-p01/src/main.js
packages/l2-p01/src/pages/clubsPage.js
packages/l2-p01/src/pages/enrolPage.js
packages/l2-p01/src/services/clubs.js
packages/l2-p01/src/utils/storage.js
packages/l2-p01/styles.css
packages/l2-p01/tests/config.json
packages/l2-p01/tests/fixtures/clubs.json
packages/l2-p01/tests/unit/patterns.jest.test.cjs
packages/l2-p01/tests/unit/patterns.vitest.test.ts
packages/l2-p01/vitest.config.ts
packages/l2-p02/README.md
packages/l2-p02/jest.config.cjs
packages/l2-p02/package.json
packages/l2-p02/public/index.html
packages/l2-p02/server.mjs
packages/l2-p02/src/addons/advanced.js
packages/l2-p02/src/api/fetchClient.js
packages/l2-p02/src/forms/enrolController.js
packages/l2-p02/src/forms/validation.js
packages/l2-p02/src/main.js
packages/l2-p02/src/pages/clubsPage.js
packages/l2-p02/src/pages/enrolPage.js
packages/l2-p02/src/services/clubs.js
packages/l2-p02/src/utils/storage.js
packages/l2-p02/styles.css
packages/l2-p02/tests/config.json
packages/l2-p02/tests/fixtures/clubs.json
packages/l2-p02/tests/unit/patterns.jest.test.cjs
packages/l2-p02/tests/unit/patterns.vitest.test.ts
packages/l2-p02/vitest.config.ts
packages/l2-p03/README.md
packages/l2-p03/jest.config.cjs
packages/l2-p03/package.json
packages/l2-p03/public/index.html
packages/l2-p03/server.mjs
packages/l2-p03/src/addons/advanced.js
packages/l2-p03/src/api/fetchClient.js
packages/l2-p03/src/forms/enrolController.js
packages/l2-p03/src/forms/validation.js
packages/l2-p03/src/main.js
packages/l2-p03/src/pages/clubsPage.js
packages/l2-p03/src/pages/enrolPage.js
packages/l2-p03/src/services/clubs.js
packages/l2-p03/src/utils/storage.js
packages/l2-p03/styles.css
packages/l2-p03/tests/config.json
packages/l2-p03/tests/fixtures/clubs.json
packages/l2-p03/tests/unit/patterns.jest.test.cjs
packages/l2-p03/tests/unit/patterns.vitest.test.ts
packages/l2-p03/vitest.config.ts
packages/l2-p04/README.md
packages/l2-p04/jest.config.cjs
packages/l2-p04/package.json
packages/l2-p04/public/index.html
packages/l2-p04/server.mjs
packages/l2-p04/src/addons/advanced.js
packages/l2-p04/src/api/fetchClient.js
packages/l2-p04/src/forms/enrolController.js
packages/l2-p04/src/forms/validation.js
packages/l2-p04/src/main.js
packages/l2-p04/src/pages/clubsPage.js
packages/l2-p04/src/pages/enrolPage.js
packages/l2-p04/src/services/clubs.js
packages/l2-p04/src/utils/storage.js
packages/l2-p04/styles.css
packages/l2-p04/tests/config.json
packages/l2-p04/tests/fixtures/clubs.json
packages/l2-p04/tests/unit/patterns.jest.test.cjs
packages/l2-p04/tests/unit/patterns.vitest.test.ts
packages/l2-p04/vitest.config.ts
packages/l2-p05/README.md
packages/l2-p05/jest.config.cjs
packages/l2-p05/package.json
packages/l2-p05/public/index.html
packages/l2-p05/server.mjs
packages/l2-p05/src/addons/advanced.js
packages/l2-p05/src/api/fetchClient.js
packages/l2-p05/src/forms/enrolController.js
packages/l2-p05/src/forms/validation.js
packages/l2-p05/src/main.js
packages/l2-p05/src/pages/clubsPage.js
packages/l2-p05/src/pages/enrolPage.js
packages/l2-p05/src/services/clubs.js
packages/l2-p05/src/utils/storage.js
packages/l2-p05/styles.css
packages/l2-p05/tests/config.json
packages/l2-p05/tests/fixtures/clubs.json
packages/l2-p05/tests/unit/patterns.jest.test.cjs
packages/l2-p05/tests/unit/patterns.vitest.test.ts
packages/l2-p05/vitest.config.ts
packages/l2-p06/README.md
packages/l2-p06/jest.config.cjs
packages/l2-p06/package.json
packages/l2-p06/public/index.html
packages/l2-p06/server.mjs
packages/l2-p06/src/addons/advanced.js
packages/l2-p06/src/api/fetchClient.js
packages/l2-p06/src/forms/enrolController.js
packages/l2-p06/src/forms/validation.js
packages/l2-p06/src/main.js
packages/l2-p06/src/pages/clubsPage.js
packages/l2-p06/src/pages/enrolPage.js
packages/l2-p06/src/services/clubs.js
packages/l2-p06/src/utils/storage.js
packages/l2-p06/styles.css
packages/l2-p06/tests/config.json
packages/l2-p06/tests/fixtures/clubs.json
packages/l2-p06/tests/unit/patterns.jest.test.cjs
packages/l2-p06/tests/unit/patterns.vitest.test.ts
packages/l2-p06/vitest.config.ts
packages/l2-p07/README.md
packages/l2-p07/jest.config.cjs
packages/l2-p07/package.json
packages/l2-p07/public/index.html
packages/l2-p07/server.mjs
packages/l2-p07/src/addons/advanced.js
packages/l2-p07/src/api/fetchClient.js
packages/l2-p07/src/forms/enrolController.js
packages/l2-p07/src/forms/validation.js
packages/l2-p07/src/main.js
packages/l2-p07/src/pages/clubsPage.js
packages/l2-p07/src/pages/enrolPage.js
packages/l2-p07/src/services/clubs.js
packages/l2-p07/src/utils/storage.js
packages/l2-p07/styles.css
packages/l2-p07/tests/config.json
packages/l2-p07/tests/fixtures/clubs.json
packages/l2-p07/tests/unit/patterns.jest.test.cjs
packages/l2-p07/tests/unit/patterns.vitest.test.ts
packages/l2-p07/vitest.config.ts
packages/l2-p08/README.md
packages/l2-p08/jest.config.cjs
packages/l2-p08/package.json
packages/l2-p08/public/index.html
packages/l2-p08/server.mjs
packages/l2-p08/src/addons/advanced.js
packages/l2-p08/src/api/fetchClient.js
packages/l2-p08/src/forms/enrolController.js
packages/l2-p08/src/forms/validation.js
packages/l2-p08/src/main.js
packages/l2-p08/src/pages/clubsPage.js
packages/l2-p08/src/pages/enrolPage.js
packages/l2-p08/src/services/clubs.js
packages/l2-p08/src/utils/storage.js
packages/l2-p08/styles.css
packages/l2-p08/tests/config.json
packages/l2-p08/tests/fixtures/clubs.json
packages/l2-p08/tests/unit/patterns.jest.test.cjs
packages/l2-p08/tests/unit/patterns.vitest.test.ts
packages/l2-p08/vitest.config.ts
packages/l2-p09/README.md
packages/l2-p09/jest.config.cjs
packages/l2-p09/package.json
packages/l2-p09/public/index.html
packages/l2-p09/server.mjs
packages/l2-p09/src/addons/advanced.js
packages/l2-p09/src/api/fetchClient.js
packages/l2-p09/src/forms/enrolController.js
packages/l2-p09/src/forms/validation.js
packages/l2-p09/src/main.js
packages/l2-p09/src/pages/clubsPage.js
packages/l2-p09/src/pages/enrolPage.js
packages/l2-p09/src/services/clubs.js
packages/l2-p09/src/utils/storage.js
packages/l2-p09/styles.css
packages/l2-p09/tests/config.json
packages/l2-p09/tests/fixtures/clubs.json
packages/l2-p09/tests/unit/patterns.jest.test.cjs
packages/l2-p09/tests/unit/patterns.vitest.test.ts
packages/l2-p09/vitest.config.ts
packages/l2-p10/README.md
packages/l2-p10/jest.config.cjs
packages/l2-p10/package.json
packages/l2-p10/public/index.html
packages/l2-p10/server.mjs
packages/l2-p10/src/addons/advanced.js
packages/l2-p10/src/api/fetchClient.js
packages/l2-p10/src/forms/enrolController.js
packages/l2-p10/src/forms/validation.js
packages/l2-p10/src/main.js
packages/l2-p10/src/pages/clubsPage.js
packages/l2-p10/src/pages/enrolPage.js
packages/l2-p10/src/services/clubs.js
packages/l2-p10/src/utils/storage.js
packages/l2-p10/styles.css
packages/l2-p10/tests/config.json
packages/l2-p10/tests/fixtures/clubs.json
packages/l2-p10/tests/unit/patterns.jest.test.cjs
packages/l2-p10/tests/unit/patterns.vitest.test.ts
packages/l2-p10/vitest.config.ts
packages/l2-p11/README.md
packages/l2-p11/jest.config.cjs
packages/l2-p11/package.json
packages/l2-p11/public/index.html
packages/l2-p11/server.mjs
packages/l2-p11/src/addons/advanced.js
packages/l2-p11/src/api/fetchClient.js
packages/l2-p11/src/forms/enrolController.js
packages/l2-p11/src/forms/validation.js
packages/l2-p11/src/main.js
packages/l2-p11/src/pages/clubsPage.js
packages/l2-p11/src/pages/enrolPage.js
packages/l2-p11/src/services/clubs.js
packages/l2-p11/src/utils/storage.js
packages/l2-p11/styles.css
packages/l2-p11/tests/config.json
packages/l2-p11/tests/fixtures/clubs.json
packages/l2-p11/tests/unit/patterns.jest.test.cjs
packages/l2-p11/tests/unit/patterns.vitest.test.ts
packages/l2-p11/vitest.config.ts
packages/l2-p12/README.md
packages/l2-p12/jest.config.cjs
packages/l2-p12/package.json
packages/l2-p12/public/index.html
packages/l2-p12/server.mjs
packages/l2-p12/src/addons/advanced.js
packages/l2-p12/src/api/fetchClient.js
packages/l2-p12/src/forms/enrolController.js
packages/l2-p12/src/forms/validation.js
packages/l2-p12/src/main.js
packages/l2-p12/src/pages/clubsPage.js
packages/l2-p12/src/pages/enrolPage.js
packages/l2-p12/src/services/clubs.js
packages/l2-p12/src/utils/storage.js
packages/l2-p12/styles.css
packages/l2-p12/tests/config.json
packages/l2-p12/tests/fixtures/clubs.json
packages/l2-p12/tests/unit/patterns.jest.test.cjs
packages/l2-p12/tests/unit/patterns.vitest.test.ts
packages/l2-p12/vitest.config.ts
packages/l2-p13/README.md
packages/l2-p13/jest.config.cjs
packages/l2-p13/package.json
packages/l2-p13/public/index.html
packages/l2-p13/server.mjs
packages/l2-p13/src/addons/advanced.js
packages/l2-p13/src/api/fetchClient.js
packages/l2-p13/src/forms/enrolController.js
packages/l2-p13/src/forms/validation.js
packages/l2-p13/src/main.js
packages/l2-p13/src/pages/clubsPage.js
packages/l2-p13/src/pages/enrolPage.js
packages/l2-p13/src/services/clubs.js
packages/l2-p13/src/utils/storage.js
packages/l2-p13/styles.css
packages/l2-p13/tests/config.json
packages/l2-p13/tests/fixtures/clubs.json
packages/l2-p13/tests/unit/patterns.jest.test.cjs
packages/l2-p13/tests/unit/patterns.vitest.test.ts
packages/l2-p13/vitest.config.ts
packages/l2-p14/README.md
packages/l2-p14/jest.config.cjs
packages/l2-p14/package.json
packages/l2-p14/public/index.html
packages/l2-p14/server.mjs
packages/l2-p14/src/addons/advanced.js
packages/l2-p14/src/api/fetchClient.js
packages/l2-p14/src/forms/enrolController.js
packages/l2-p14/src/forms/validation.js
packages/l2-p14/src/main.js
packages/l2-p14/src/pages/clubsPage.js
packages/l2-p14/src/pages/enrolPage.js
packages/l2-p14/src/services/clubs.js
packages/l2-p14/src/utils/storage.js
packages/l2-p14/styles.css
packages/l2-p14/tests/config.json
packages/l2-p14/tests/fixtures/clubs.json
packages/l2-p14/tests/unit/patterns.jest.test.cjs
packages/l2-p14/tests/unit/patterns.vitest.test.ts
packages/l2-p14/vitest.config.ts
packages/l2-p15/README.md
packages/l2-p15/jest.config.cjs
packages/l2-p15/package.json
packages/l2-p15/public/index.html
packages/l2-p15/server.mjs
packages/l2-p15/src/addons/advanced.js
packages/l2-p15/src/api/fetchClient.js
packages/l2-p15/src/forms/enrolController.js
packages/l2-p15/src/forms/validation.js
packages/l2-p15/src/main.js
packages/l2-p15/src/pages/clubsPage.js
packages/l2-p15/src/pages/enrolPage.js
packages/l2-p15/src/services/clubs.js
packages/l2-p15/src/utils/storage.js
packages/l2-p15/styles.css
packages/l2-p15/tests/config.json
packages/l2-p15/tests/fixtures/clubs.json
packages/l2-p15/tests/unit/patterns.jest.test.cjs
packages/l2-p15/tests/unit/patterns.vitest.test.ts
packages/l2-p15/vitest.config.ts
packages/l3-p01/README.md
packages/l3-p01/jest.config.cjs
packages/l3-p01/package.json
packages/l3-p01/public/index.html
packages/l3-p01/server.mjs
packages/l3-p01/src/addons/advanced.js
packages/l3-p01/src/api/fetchClient.js
packages/l3-p01/src/forms/enrolController.js
packages/l3-p01/src/forms/validation.js
packages/l3-p01/src/main.js
packages/l3-p01/src/pages/clubsPage.js
packages/l3-p01/src/pages/enrolPage.js
packages/l3-p01/src/services/clubs.js
packages/l3-p01/src/utils/storage.js
packages/l3-p01/styles.css
packages/l3-p01/tests/config.json
packages/l3-p01/tests/fixtures/clubs.json
packages/l3-p01/tests/unit/patterns.jest.test.cjs
packages/l3-p01/tests/unit/patterns.vitest.test.ts
packages/l3-p01/vitest.config.ts
packages/l3-p02/README.md
packages/l3-p02/jest.config.cjs
packages/l3-p02/package.json
packages/l3-p02/public/index.html
packages/l3-p02/server.mjs
packages/l3-p02/src/addons/advanced.js
packages/l3-p02/src/api/fetchClient.js
packages/l3-p02/src/forms/enrolController.js
packages/l3-p02/src/forms/validation.js
packages/l3-p02/src/main.js
packages/l3-p02/src/pages/clubsPage.js
packages/l3-p02/src/pages/enrolPage.js
packages/l3-p02/src/services/clubs.js
packages/l3-p02/src/utils/storage.js
packages/l3-p02/styles.css
packages/l3-p02/tests/config.json
packages/l3-p02/tests/fixtures/clubs.json
packages/l3-p02/tests/unit/patterns.jest.test.cjs
packages/l3-p02/tests/unit/patterns.vitest.test.ts
packages/l3-p02/vitest.config.ts
packages/l3-p03/README.md
packages/l3-p03/jest.config.cjs
packages/l3-p03/package.json
packages/l3-p03/public/index.html
packages/l3-p03/server.mjs
packages/l3-p03/src/addons/advanced.js
packages/l3-p03/src/api/fetchClient.js
packages/l3-p03/src/forms/enrolController.js
packages/l3-p03/src/forms/validation.js
packages/l3-p03/src/main.js
packages/l3-p03/src/pages/clubsPage.js
packages/l3-p03/src/pages/enrolPage.js
packages/l3-p03/src/services/clubs.js
packages/l3-p03/src/utils/storage.js
packages/l3-p03/styles.css
packages/l3-p03/tests/config.json
packages/l3-p03/tests/fixtures/clubs.json
packages/l3-p03/tests/unit/patterns.jest.test.cjs
packages/l3-p03/tests/unit/patterns.vitest.test.ts
packages/l3-p03/vitest.config.ts
packages/l3-p04/README.md
packages/l3-p04/jest.config.cjs
packages/l3-p04/package.json
packages/l3-p04/public/index.html
packages/l3-p04/server.mjs
packages/l3-p04/src/addons/advanced.js
packages/l3-p04/src/api/fetchClient.js
packages/l3-p04/src/forms/enrolController.js
packages/l3-p04/src/forms/validation.js
packages/l3-p04/src/main.js
packages/l3-p04/src/pages/clubsPage.js
packages/l3-p04/src/pages/enrolPage.js
packages/l3-p04/src/services/clubs.js
packages/l3-p04/src/utils/storage.js
packages/l3-p04/styles.css
packages/l3-p04/tests/config.json
packages/l3-p04/tests/fixtures/clubs.json
packages/l3-p04/tests/unit/patterns.jest.test.cjs
packages/l3-p04/tests/unit/patterns.vitest.test.ts
packages/l3-p04/vitest.config.ts
packages/l3-p05/README.md
packages/l3-p05/jest.config.cjs
packages/l3-p05/package.json
packages/l3-p05/public/index.html
packages/l3-p05/server.mjs
packages/l3-p05/src/addons/advanced.js
packages/l3-p05/src/api/fetchClient.js
packages/l3-p05/src/forms/enrolController.js
packages/l3-p05/src/forms/validation.js
packages/l3-p05/src/main.js
packages/l3-p05/src/pages/clubsPage.js
packages/l3-p05/src/pages/enrolPage.js
packages/l3-p05/src/services/clubs.js
packages/l3-p05/src/utils/storage.js
packages/l3-p05/styles.css
packages/l3-p05/tests/config.json
packages/l3-p05/tests/fixtures/clubs.json
packages/l3-p05/tests/unit/patterns.jest.test.cjs
packages/l3-p05/tests/unit/patterns.vitest.test.ts
packages/l3-p05/vitest.config.ts
packages/l3-p06/README.md
packages/l3-p06/jest.config.cjs
packages/l3-p06/package.json
packages/l3-p06/public/index.html
packages/l3-p06/server.mjs
packages/l3-p06/src/addons/advanced.js
packages/l3-p06/src/api/fetchClient.js
packages/l3-p06/src/forms/enrolController.js
packages/l3-p06/src/forms/validation.js
packages/l3-p06/src/main.js
packages/l3-p06/src/pages/clubsPage.js
packages/l3-p06/src/pages/enrolPage.js
packages/l3-p06/src/services/clubs.js
packages/l3-p06/src/utils/storage.js
packages/l3-p06/styles.css
packages/l3-p06/tests/config.json
packages/l3-p06/tests/fixtures/clubs.json
packages/l3-p06/tests/unit/patterns.jest.test.cjs
packages/l3-p06/tests/unit/patterns.vitest.test.ts
packages/l3-p06/vitest.config.ts
packages/l3-p07/README.md
packages/l3-p07/jest.config.cjs
packages/l3-p07/package.json
packages/l3-p07/public/index.html
packages/l3-p07/server.mjs
packages/l3-p07/src/addons/advanced.js
packages/l3-p07/src/api/fetchClient.js
packages/l3-p07/src/forms/enrolController.js
packages/l3-p07/src/forms/validation.js
packages/l3-p07/src/main.js
packages/l3-p07/src/pages/clubsPage.js
packages/l3-p07/src/pages/enrolPage.js
packages/l3-p07/src/services/clubs.js
packages/l3-p07/src/utils/storage.js
packages/l3-p07/styles.css
packages/l3-p07/tests/config.json
packages/l3-p07/tests/fixtures/clubs.json
packages/l3-p07/tests/unit/patterns.jest.test.cjs
packages/l3-p07/tests/unit/patterns.vitest.test.ts
packages/l3-p07/vitest.config.ts
packages/l3-p08/README.md
packages/l3-p08/jest.config.cjs
packages/l3-p08/package.json
packages/l3-p08/public/index.html
packages/l3-p08/server.mjs
packages/l3-p08/src/addons/advanced.js
packages/l3-p08/src/api/fetchClient.js
packages/l3-p08/src/forms/enrolController.js
packages/l3-p08/src/forms/validation.js
packages/l3-p08/src/main.js
packages/l3-p08/src/pages/clubsPage.js
packages/l3-p08/src/pages/enrolPage.js
packages/l3-p08/src/services/clubs.js
packages/l3-p08/src/utils/storage.js
packages/l3-p08/styles.css
packages/l3-p08/tests/config.json
packages/l3-p08/tests/fixtures/clubs.json
packages/l3-p08/tests/unit/patterns.jest.test.cjs
packages/l3-p08/tests/unit/patterns.vitest.test.ts
packages/l3-p08/vitest.config.ts
packages/l3-p09/README.md
packages/l3-p09/jest.config.cjs
packages/l3-p09/package.json
packages/l3-p09/public/index.html
packages/l3-p09/server.mjs
packages/l3-p09/src/addons/advanced.js
packages/l3-p09/src/api/fetchClient.js
packages/l3-p09/src/forms/enrolController.js
packages/l3-p09/src/forms/validation.js
packages/l3-p09/src/main.js
packages/l3-p09/src/pages/clubsPage.js
packages/l3-p09/src/pages/enrolPage.js
packages/l3-p09/src/services/clubs.js
packages/l3-p09/src/utils/storage.js
packages/l3-p09/styles.css
packages/l3-p09/tests/config.json
packages/l3-p09/tests/fixtures/clubs.json
packages/l3-p09/tests/unit/patterns.jest.test.cjs
packages/l3-p09/tests/unit/patterns.vitest.test.ts
packages/l3-p09/vitest.config.ts
packages/l3-p10/README.md
packages/l3-p10/jest.config.cjs
packages/l3-p10/package.json
packages/l3-p10/public/index.html
packages/l3-p10/server.mjs
packages/l3-p10/src/addons/advanced.js
packages/l3-p10/src/api/fetchClient.js
packages/l3-p10/src/forms/enrolController.js
packages/l3-p10/src/forms/validation.js
packages/l3-p10/src/main.js
packages/l3-p10/src/pages/clubsPage.js
packages/l3-p10/src/pages/enrolPage.js
packages/l3-p10/src/services/clubs.js
packages/l3-p10/src/utils/storage.js
packages/l3-p10/styles.css
packages/l3-p10/tests/config.json
packages/l3-p10/tests/fixtures/clubs.json
packages/l3-p10/tests/unit/patterns.jest.test.cjs
packages/l3-p10/tests/unit/patterns.vitest.test.ts
packages/l3-p10/vitest.config.ts
packages/l3-p11/README.md
packages/l3-p11/jest.config.cjs
packages/l3-p11/package.json
packages/l3-p11/public/index.html
packages/l3-p11/server.mjs
packages/l3-p11/src/addons/advanced.js
packages/l3-p11/src/api/fetchClient.js
packages/l3-p11/src/forms/enrolController.js
packages/l3-p11/src/forms/validation.js
packages/l3-p11/src/main.js
packages/l3-p11/src/pages/clubsPage.js
packages/l3-p11/src/pages/enrolPage.js
packages/l3-p11/src/services/clubs.js
packages/l3-p11/src/utils/storage.js
packages/l3-p11/styles.css
packages/l3-p11/tests/config.json
packages/l3-p11/tests/fixtures/clubs.json
packages/l3-p11/tests/unit/patterns.jest.test.cjs
packages/l3-p11/tests/unit/patterns.vitest.test.ts
packages/l3-p11/vitest.config.ts
packages/l3-p12/README.md
packages/l3-p12/jest.config.cjs
packages/l3-p12/package.json
packages/l3-p12/public/index.html
packages/l3-p12/server.mjs
packages/l3-p12/src/addons/advanced.js
packages/l3-p12/src/api/fetchClient.js
packages/l3-p12/src/forms/enrolController.js
packages/l3-p12/src/forms/validation.js
packages/l3-p12/src/main.js
packages/l3-p12/src/pages/clubsPage.js
packages/l3-p12/src/pages/enrolPage.js
packages/l3-p12/src/services/clubs.js
packages/l3-p12/src/utils/storage.js
packages/l3-p12/styles.css
packages/l3-p12/tests/config.json
packages/l3-p12/tests/fixtures/clubs.json
packages/l3-p12/tests/unit/patterns.jest.test.cjs
packages/l3-p12/tests/unit/patterns.vitest.test.ts
packages/l3-p12/vitest.config.ts
packages/l3-p13/README.md
packages/l3-p13/jest.config.cjs
packages/l3-p13/package.json
packages/l3-p13/public/index.html
packages/l3-p13/server.mjs
packages/l3-p13/src/addons/advanced.js
packages/l3-p13/src/api/fetchClient.js
packages/l3-p13/src/forms/enrolController.js
packages/l3-p13/src/forms/validation.js
packages/l3-p13/src/main.js
packages/l3-p13/src/pages/clubsPage.js
packages/l3-p13/src/pages/enrolPage.js
packages/l3-p13/src/services/clubs.js
packages/l3-p13/src/utils/storage.js
packages/l3-p13/styles.css
packages/l3-p13/tests/config.json
packages/l3-p13/tests/fixtures/clubs.json
packages/l3-p13/tests/unit/patterns.jest.test.cjs
packages/l3-p13/tests/unit/patterns.vitest.test.ts
packages/l3-p13/vitest.config.ts
packages/l3-p14/README.md
packages/l3-p14/jest.config.cjs
packages/l3-p14/package.json
packages/l3-p14/public/index.html
packages/l3-p14/server.mjs
packages/l3-p14/src/addons/advanced.js
packages/l3-p14/src/api/fetchClient.js
packages/l3-p14/src/forms/enrolController.js
packages/l3-p14/src/forms/validation.js
packages/l3-p14/src/main.js
packages/l3-p14/src/pages/clubsPage.js
packages/l3-p14/src/pages/enrolPage.js
packages/l3-p14/src/services/clubs.js
packages/l3-p14/src/utils/storage.js
packages/l3-p14/styles.css
packages/l3-p14/tests/config.json
packages/l3-p14/tests/fixtures/clubs.json
packages/l3-p14/tests/unit/patterns.jest.test.cjs
packages/l3-p14/tests/unit/patterns.vitest.test.ts
packages/l3-p14/vitest.config.ts
packages/l3-p15/README.md
packages/l3-p15/jest.config.cjs
packages/l3-p15/package.json
packages/l3-p15/public/index.html
packages/l3-p15/server.mjs
packages/l3-p15/src/addons/advanced.js
packages/l3-p15/src/api/fetchClient.js
packages/l3-p15/src/forms/enrolController.js
packages/l3-p15/src/forms/validation.js
packages/l3-p15/src/main.js
packages/l3-p15/src/pages/clubsPage.js
packages/l3-p15/src/pages/enrolPage.js
packages/l3-p15/src/services/clubs.js
packages/l3-p15/src/utils/storage.js
packages/l3-p15/styles.css
packages/l3-p15/tests/config.json
packages/l3-p15/tests/fixtures/clubs.json
packages/l3-p15/tests/unit/patterns.jest.test.cjs
packages/l3-p15/tests/unit/patterns.vitest.test.ts
packages/l3-p15/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 182, other: 45, docs: 45, public: 45, code: 405, tests: 180.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s7p3-monorepo` type=`module` workspaces=True
  - **Scripturi:**
  - `test:vitest` → `pnpm -r --filter ./packages run test:vitest`
  - `test:jest` → `pnpm -r --filter ./packages run test:jest`
  - `test` → `pnpm -r --filter ./packages run test`
  - `dev` → `echo 'rulează dev per pachet: pnpm --filter <pkg> run dev'`
  - **Deps:** 
  - **DevDeps:** pnpm, vitest, jest, jsdom, express, cors
- `packages/l1-p01/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p02/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p03/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p04/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p05/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p06/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p07/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p08/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p09/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p10/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p11/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p12/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p13/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p14/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l1-p15/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p01/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p02/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p03/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p04/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p05/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p06/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p07/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p08/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p09/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p10/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p11/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p12/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p13/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p14/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l2-p15/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p01/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p02/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p03/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p04/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p05/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p06/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p07/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p08/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p09/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p10/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p11/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p12/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p13/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p14/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `packages/l3-p15/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors

### Seminar7_Partea3_p3-standalone.zip

```
l1-p01/README.md
l1-p01/jest.config.cjs
l1-p01/package.json
l1-p01/public/index.html
l1-p01/server.mjs
l1-p01/src/addons/advanced.js
l1-p01/src/api/fetchClient.js
l1-p01/src/forms/enrolController.js
l1-p01/src/forms/validation.js
l1-p01/src/main.js
l1-p01/src/pages/clubsPage.js
l1-p01/src/pages/enrolPage.js
l1-p01/src/services/clubs.js
l1-p01/src/utils/storage.js
l1-p01/styles.css
l1-p01/tests/config.json
l1-p01/tests/fixtures/clubs.json
l1-p01/tests/unit/patterns.jest.test.cjs
l1-p01/tests/unit/patterns.vitest.test.ts
l1-p01/vitest.config.ts
l1-p02/README.md
l1-p02/jest.config.cjs
l1-p02/package.json
l1-p02/public/index.html
l1-p02/server.mjs
l1-p02/src/addons/advanced.js
l1-p02/src/api/fetchClient.js
l1-p02/src/forms/enrolController.js
l1-p02/src/forms/validation.js
l1-p02/src/main.js
l1-p02/src/pages/clubsPage.js
l1-p02/src/pages/enrolPage.js
l1-p02/src/services/clubs.js
l1-p02/src/utils/storage.js
l1-p02/styles.css
l1-p02/tests/config.json
l1-p02/tests/fixtures/clubs.json
l1-p02/tests/unit/patterns.jest.test.cjs
l1-p02/tests/unit/patterns.vitest.test.ts
l1-p02/vitest.config.ts
l1-p03/README.md
l1-p03/jest.config.cjs
l1-p03/package.json
l1-p03/public/index.html
l1-p03/server.mjs
l1-p03/src/addons/advanced.js
l1-p03/src/api/fetchClient.js
l1-p03/src/forms/enrolController.js
l1-p03/src/forms/validation.js
l1-p03/src/main.js
l1-p03/src/pages/clubsPage.js
l1-p03/src/pages/enrolPage.js
l1-p03/src/services/clubs.js
l1-p03/src/utils/storage.js
l1-p03/styles.css
l1-p03/tests/config.json
l1-p03/tests/fixtures/clubs.json
l1-p03/tests/unit/patterns.jest.test.cjs
l1-p03/tests/unit/patterns.vitest.test.ts
l1-p03/vitest.config.ts
l1-p04/README.md
l1-p04/jest.config.cjs
l1-p04/package.json
l1-p04/public/index.html
l1-p04/server.mjs
l1-p04/src/addons/advanced.js
l1-p04/src/api/fetchClient.js
l1-p04/src/forms/enrolController.js
l1-p04/src/forms/validation.js
l1-p04/src/main.js
l1-p04/src/pages/clubsPage.js
l1-p04/src/pages/enrolPage.js
l1-p04/src/services/clubs.js
l1-p04/src/utils/storage.js
l1-p04/styles.css
l1-p04/tests/config.json
l1-p04/tests/fixtures/clubs.json
l1-p04/tests/unit/patterns.jest.test.cjs
l1-p04/tests/unit/patterns.vitest.test.ts
l1-p04/vitest.config.ts
l1-p05/README.md
l1-p05/jest.config.cjs
l1-p05/package.json
l1-p05/public/index.html
l1-p05/server.mjs
l1-p05/src/addons/advanced.js
l1-p05/src/api/fetchClient.js
l1-p05/src/forms/enrolController.js
l1-p05/src/forms/validation.js
l1-p05/src/main.js
l1-p05/src/pages/clubsPage.js
l1-p05/src/pages/enrolPage.js
l1-p05/src/services/clubs.js
l1-p05/src/utils/storage.js
l1-p05/styles.css
l1-p05/tests/config.json
l1-p05/tests/fixtures/clubs.json
l1-p05/tests/unit/patterns.jest.test.cjs
l1-p05/tests/unit/patterns.vitest.test.ts
l1-p05/vitest.config.ts
l1-p06/README.md
l1-p06/jest.config.cjs
l1-p06/package.json
l1-p06/public/index.html
l1-p06/server.mjs
l1-p06/src/addons/advanced.js
l1-p06/src/api/fetchClient.js
l1-p06/src/forms/enrolController.js
l1-p06/src/forms/validation.js
l1-p06/src/main.js
l1-p06/src/pages/clubsPage.js
l1-p06/src/pages/enrolPage.js
l1-p06/src/services/clubs.js
l1-p06/src/utils/storage.js
l1-p06/styles.css
l1-p06/tests/config.json
l1-p06/tests/fixtures/clubs.json
l1-p06/tests/unit/patterns.jest.test.cjs
l1-p06/tests/unit/patterns.vitest.test.ts
l1-p06/vitest.config.ts
l1-p07/README.md
l1-p07/jest.config.cjs
l1-p07/package.json
l1-p07/public/index.html
l1-p07/server.mjs
l1-p07/src/addons/advanced.js
l1-p07/src/api/fetchClient.js
l1-p07/src/forms/enrolController.js
l1-p07/src/forms/validation.js
l1-p07/src/main.js
l1-p07/src/pages/clubsPage.js
l1-p07/src/pages/enrolPage.js
l1-p07/src/services/clubs.js
l1-p07/src/utils/storage.js
l1-p07/styles.css
l1-p07/tests/config.json
l1-p07/tests/fixtures/clubs.json
l1-p07/tests/unit/patterns.jest.test.cjs
l1-p07/tests/unit/patterns.vitest.test.ts
l1-p07/vitest.config.ts
l1-p08/README.md
l1-p08/jest.config.cjs
l1-p08/package.json
l1-p08/public/index.html
l1-p08/server.mjs
l1-p08/src/addons/advanced.js
l1-p08/src/api/fetchClient.js
l1-p08/src/forms/enrolController.js
l1-p08/src/forms/validation.js
l1-p08/src/main.js
l1-p08/src/pages/clubsPage.js
l1-p08/src/pages/enrolPage.js
l1-p08/src/services/clubs.js
l1-p08/src/utils/storage.js
l1-p08/styles.css
l1-p08/tests/config.json
l1-p08/tests/fixtures/clubs.json
l1-p08/tests/unit/patterns.jest.test.cjs
l1-p08/tests/unit/patterns.vitest.test.ts
l1-p08/vitest.config.ts
l1-p09/README.md
l1-p09/jest.config.cjs
l1-p09/package.json
l1-p09/public/index.html
l1-p09/server.mjs
l1-p09/src/addons/advanced.js
l1-p09/src/api/fetchClient.js
l1-p09/src/forms/enrolController.js
l1-p09/src/forms/validation.js
l1-p09/src/main.js
l1-p09/src/pages/clubsPage.js
l1-p09/src/pages/enrolPage.js
l1-p09/src/services/clubs.js
l1-p09/src/utils/storage.js
l1-p09/styles.css
l1-p09/tests/config.json
l1-p09/tests/fixtures/clubs.json
l1-p09/tests/unit/patterns.jest.test.cjs
l1-p09/tests/unit/patterns.vitest.test.ts
l1-p09/vitest.config.ts
l1-p10/README.md
l1-p10/jest.config.cjs
l1-p10/package.json
l1-p10/public/index.html
l1-p10/server.mjs
l1-p10/src/addons/advanced.js
l1-p10/src/api/fetchClient.js
l1-p10/src/forms/enrolController.js
l1-p10/src/forms/validation.js
l1-p10/src/main.js
l1-p10/src/pages/clubsPage.js
l1-p10/src/pages/enrolPage.js
l1-p10/src/services/clubs.js
l1-p10/src/utils/storage.js
l1-p10/styles.css
l1-p10/tests/config.json
l1-p10/tests/fixtures/clubs.json
l1-p10/tests/unit/patterns.jest.test.cjs
l1-p10/tests/unit/patterns.vitest.test.ts
l1-p10/vitest.config.ts
l1-p11/README.md
l1-p11/jest.config.cjs
l1-p11/package.json
l1-p11/public/index.html
l1-p11/server.mjs
l1-p11/src/addons/advanced.js
l1-p11/src/api/fetchClient.js
l1-p11/src/forms/enrolController.js
l1-p11/src/forms/validation.js
l1-p11/src/main.js
l1-p11/src/pages/clubsPage.js
l1-p11/src/pages/enrolPage.js
l1-p11/src/services/clubs.js
l1-p11/src/utils/storage.js
l1-p11/styles.css
l1-p11/tests/config.json
l1-p11/tests/fixtures/clubs.json
l1-p11/tests/unit/patterns.jest.test.cjs
l1-p11/tests/unit/patterns.vitest.test.ts
l1-p11/vitest.config.ts
l1-p12/README.md
l1-p12/jest.config.cjs
l1-p12/package.json
l1-p12/public/index.html
l1-p12/server.mjs
l1-p12/src/addons/advanced.js
l1-p12/src/api/fetchClient.js
l1-p12/src/forms/enrolController.js
l1-p12/src/forms/validation.js
l1-p12/src/main.js
l1-p12/src/pages/clubsPage.js
l1-p12/src/pages/enrolPage.js
l1-p12/src/services/clubs.js
l1-p12/src/utils/storage.js
l1-p12/styles.css
l1-p12/tests/config.json
l1-p12/tests/fixtures/clubs.json
l1-p12/tests/unit/patterns.jest.test.cjs
l1-p12/tests/unit/patterns.vitest.test.ts
l1-p12/vitest.config.ts
l1-p13/README.md
l1-p13/jest.config.cjs
l1-p13/package.json
l1-p13/public/index.html
l1-p13/server.mjs
l1-p13/src/addons/advanced.js
l1-p13/src/api/fetchClient.js
l1-p13/src/forms/enrolController.js
l1-p13/src/forms/validation.js
l1-p13/src/main.js
l1-p13/src/pages/clubsPage.js
l1-p13/src/pages/enrolPage.js
l1-p13/src/services/clubs.js
l1-p13/src/utils/storage.js
l1-p13/styles.css
l1-p13/tests/config.json
l1-p13/tests/fixtures/clubs.json
l1-p13/tests/unit/patterns.jest.test.cjs
l1-p13/tests/unit/patterns.vitest.test.ts
l1-p13/vitest.config.ts
l1-p14/README.md
l1-p14/jest.config.cjs
l1-p14/package.json
l1-p14/public/index.html
l1-p14/server.mjs
l1-p14/src/addons/advanced.js
l1-p14/src/api/fetchClient.js
l1-p14/src/forms/enrolController.js
l1-p14/src/forms/validation.js
l1-p14/src/main.js
l1-p14/src/pages/clubsPage.js
l1-p14/src/pages/enrolPage.js
l1-p14/src/services/clubs.js
l1-p14/src/utils/storage.js
l1-p14/styles.css
l1-p14/tests/config.json
l1-p14/tests/fixtures/clubs.json
l1-p14/tests/unit/patterns.jest.test.cjs
l1-p14/tests/unit/patterns.vitest.test.ts
l1-p14/vitest.config.ts
l1-p15/README.md
l1-p15/jest.config.cjs
l1-p15/package.json
l1-p15/public/index.html
l1-p15/server.mjs
l1-p15/src/addons/advanced.js
l1-p15/src/api/fetchClient.js
l1-p15/src/forms/enrolController.js
l1-p15/src/forms/validation.js
l1-p15/src/main.js
l1-p15/src/pages/clubsPage.js
l1-p15/src/pages/enrolPage.js
l1-p15/src/services/clubs.js
l1-p15/src/utils/storage.js
l1-p15/styles.css
l1-p15/tests/config.json
l1-p15/tests/fixtures/clubs.json
l1-p15/tests/unit/patterns.jest.test.cjs
l1-p15/tests/unit/patterns.vitest.test.ts
l1-p15/vitest.config.ts
l2-p01/README.md
l2-p01/jest.config.cjs
l2-p01/package.json
l2-p01/public/index.html
l2-p01/server.mjs
l2-p01/src/addons/advanced.js
l2-p01/src/api/fetchClient.js
l2-p01/src/forms/enrolController.js
l2-p01/src/forms/validation.js
l2-p01/src/main.js
l2-p01/src/pages/clubsPage.js
l2-p01/src/pages/enrolPage.js
l2-p01/src/services/clubs.js
l2-p01/src/utils/storage.js
l2-p01/styles.css
l2-p01/tests/config.json
l2-p01/tests/fixtures/clubs.json
l2-p01/tests/unit/patterns.jest.test.cjs
l2-p01/tests/unit/patterns.vitest.test.ts
l2-p01/vitest.config.ts
l2-p02/README.md
l2-p02/jest.config.cjs
l2-p02/package.json
l2-p02/public/index.html
l2-p02/server.mjs
l2-p02/src/addons/advanced.js
l2-p02/src/api/fetchClient.js
l2-p02/src/forms/enrolController.js
l2-p02/src/forms/validation.js
l2-p02/src/main.js
l2-p02/src/pages/clubsPage.js
l2-p02/src/pages/enrolPage.js
l2-p02/src/services/clubs.js
l2-p02/src/utils/storage.js
l2-p02/styles.css
l2-p02/tests/config.json
l2-p02/tests/fixtures/clubs.json
l2-p02/tests/unit/patterns.jest.test.cjs
l2-p02/tests/unit/patterns.vitest.test.ts
l2-p02/vitest.config.ts
l2-p03/README.md
l2-p03/jest.config.cjs
l2-p03/package.json
l2-p03/public/index.html
l2-p03/server.mjs
l2-p03/src/addons/advanced.js
l2-p03/src/api/fetchClient.js
l2-p03/src/forms/enrolController.js
l2-p03/src/forms/validation.js
l2-p03/src/main.js
l2-p03/src/pages/clubsPage.js
l2-p03/src/pages/enrolPage.js
l2-p03/src/services/clubs.js
l2-p03/src/utils/storage.js
l2-p03/styles.css
l2-p03/tests/config.json
l2-p03/tests/fixtures/clubs.json
l2-p03/tests/unit/patterns.jest.test.cjs
l2-p03/tests/unit/patterns.vitest.test.ts
l2-p03/vitest.config.ts
l2-p04/README.md
l2-p04/jest.config.cjs
l2-p04/package.json
l2-p04/public/index.html
l2-p04/server.mjs
l2-p04/src/addons/advanced.js
l2-p04/src/api/fetchClient.js
l2-p04/src/forms/enrolController.js
l2-p04/src/forms/validation.js
l2-p04/src/main.js
l2-p04/src/pages/clubsPage.js
l2-p04/src/pages/enrolPage.js
l2-p04/src/services/clubs.js
l2-p04/src/utils/storage.js
l2-p04/styles.css
l2-p04/tests/config.json
l2-p04/tests/fixtures/clubs.json
l2-p04/tests/unit/patterns.jest.test.cjs
l2-p04/tests/unit/patterns.vitest.test.ts
l2-p04/vitest.config.ts
l2-p05/README.md
l2-p05/jest.config.cjs
l2-p05/package.json
l2-p05/public/index.html
l2-p05/server.mjs
l2-p05/src/addons/advanced.js
l2-p05/src/api/fetchClient.js
l2-p05/src/forms/enrolController.js
l2-p05/src/forms/validation.js
l2-p05/src/main.js
l2-p05/src/pages/clubsPage.js
l2-p05/src/pages/enrolPage.js
l2-p05/src/services/clubs.js
l2-p05/src/utils/storage.js
l2-p05/styles.css
l2-p05/tests/config.json
l2-p05/tests/fixtures/clubs.json
l2-p05/tests/unit/patterns.jest.test.cjs
l2-p05/tests/unit/patterns.vitest.test.ts
l2-p05/vitest.config.ts
l2-p06/README.md
l2-p06/jest.config.cjs
l2-p06/package.json
l2-p06/public/index.html
l2-p06/server.mjs
l2-p06/src/addons/advanced.js
l2-p06/src/api/fetchClient.js
l2-p06/src/forms/enrolController.js
l2-p06/src/forms/validation.js
l2-p06/src/main.js
l2-p06/src/pages/clubsPage.js
l2-p06/src/pages/enrolPage.js
l2-p06/src/services/clubs.js
l2-p06/src/utils/storage.js
l2-p06/styles.css
l2-p06/tests/config.json
l2-p06/tests/fixtures/clubs.json
l2-p06/tests/unit/patterns.jest.test.cjs
l2-p06/tests/unit/patterns.vitest.test.ts
l2-p06/vitest.config.ts
l2-p07/README.md
l2-p07/jest.config.cjs
l2-p07/package.json
l2-p07/public/index.html
l2-p07/server.mjs
l2-p07/src/addons/advanced.js
l2-p07/src/api/fetchClient.js
l2-p07/src/forms/enrolController.js
l2-p07/src/forms/validation.js
l2-p07/src/main.js
l2-p07/src/pages/clubsPage.js
l2-p07/src/pages/enrolPage.js
l2-p07/src/services/clubs.js
l2-p07/src/utils/storage.js
l2-p07/styles.css
l2-p07/tests/config.json
l2-p07/tests/fixtures/clubs.json
l2-p07/tests/unit/patterns.jest.test.cjs
l2-p07/tests/unit/patterns.vitest.test.ts
l2-p07/vitest.config.ts
l2-p08/README.md
l2-p08/jest.config.cjs
l2-p08/package.json
l2-p08/public/index.html
l2-p08/server.mjs
l2-p08/src/addons/advanced.js
l2-p08/src/api/fetchClient.js
l2-p08/src/forms/enrolController.js
l2-p08/src/forms/validation.js
l2-p08/src/main.js
l2-p08/src/pages/clubsPage.js
l2-p08/src/pages/enrolPage.js
l2-p08/src/services/clubs.js
l2-p08/src/utils/storage.js
l2-p08/styles.css
l2-p08/tests/config.json
l2-p08/tests/fixtures/clubs.json
l2-p08/tests/unit/patterns.jest.test.cjs
l2-p08/tests/unit/patterns.vitest.test.ts
l2-p08/vitest.config.ts
l2-p09/README.md
l2-p09/jest.config.cjs
l2-p09/package.json
l2-p09/public/index.html
l2-p09/server.mjs
l2-p09/src/addons/advanced.js
l2-p09/src/api/fetchClient.js
l2-p09/src/forms/enrolController.js
l2-p09/src/forms/validation.js
l2-p09/src/main.js
l2-p09/src/pages/clubsPage.js
l2-p09/src/pages/enrolPage.js
l2-p09/src/services/clubs.js
l2-p09/src/utils/storage.js
l2-p09/styles.css
l2-p09/tests/config.json
l2-p09/tests/fixtures/clubs.json
l2-p09/tests/unit/patterns.jest.test.cjs
l2-p09/tests/unit/patterns.vitest.test.ts
l2-p09/vitest.config.ts
l2-p10/README.md
l2-p10/jest.config.cjs
l2-p10/package.json
l2-p10/public/index.html
l2-p10/server.mjs
l2-p10/src/addons/advanced.js
l2-p10/src/api/fetchClient.js
l2-p10/src/forms/enrolController.js
l2-p10/src/forms/validation.js
l2-p10/src/main.js
l2-p10/src/pages/clubsPage.js
l2-p10/src/pages/enrolPage.js
l2-p10/src/services/clubs.js
l2-p10/src/utils/storage.js
l2-p10/styles.css
l2-p10/tests/config.json
l2-p10/tests/fixtures/clubs.json
l2-p10/tests/unit/patterns.jest.test.cjs
l2-p10/tests/unit/patterns.vitest.test.ts
l2-p10/vitest.config.ts
l2-p11/README.md
l2-p11/jest.config.cjs
l2-p11/package.json
l2-p11/public/index.html
l2-p11/server.mjs
l2-p11/src/addons/advanced.js
l2-p11/src/api/fetchClient.js
l2-p11/src/forms/enrolController.js
l2-p11/src/forms/validation.js
l2-p11/src/main.js
l2-p11/src/pages/clubsPage.js
l2-p11/src/pages/enrolPage.js
l2-p11/src/services/clubs.js
l2-p11/src/utils/storage.js
l2-p11/styles.css
l2-p11/tests/config.json
l2-p11/tests/fixtures/clubs.json
l2-p11/tests/unit/patterns.jest.test.cjs
l2-p11/tests/unit/patterns.vitest.test.ts
l2-p11/vitest.config.ts
l2-p12/README.md
l2-p12/jest.config.cjs
l2-p12/package.json
l2-p12/public/index.html
l2-p12/server.mjs
l2-p12/src/addons/advanced.js
l2-p12/src/api/fetchClient.js
l2-p12/src/forms/enrolController.js
l2-p12/src/forms/validation.js
l2-p12/src/main.js
l2-p12/src/pages/clubsPage.js
l2-p12/src/pages/enrolPage.js
l2-p12/src/services/clubs.js
l2-p12/src/utils/storage.js
l2-p12/styles.css
l2-p12/tests/config.json
l2-p12/tests/fixtures/clubs.json
l2-p12/tests/unit/patterns.jest.test.cjs
l2-p12/tests/unit/patterns.vitest.test.ts
l2-p12/vitest.config.ts
l2-p13/README.md
l2-p13/jest.config.cjs
l2-p13/package.json
l2-p13/public/index.html
l2-p13/server.mjs
l2-p13/src/addons/advanced.js
l2-p13/src/api/fetchClient.js
l2-p13/src/forms/enrolController.js
l2-p13/src/forms/validation.js
l2-p13/src/main.js
l2-p13/src/pages/clubsPage.js
l2-p13/src/pages/enrolPage.js
l2-p13/src/services/clubs.js
l2-p13/src/utils/storage.js
l2-p13/styles.css
l2-p13/tests/config.json
l2-p13/tests/fixtures/clubs.json
l2-p13/tests/unit/patterns.jest.test.cjs
l2-p13/tests/unit/patterns.vitest.test.ts
l2-p13/vitest.config.ts
l2-p14/README.md
l2-p14/jest.config.cjs
l2-p14/package.json
l2-p14/public/index.html
l2-p14/server.mjs
l2-p14/src/addons/advanced.js
l2-p14/src/api/fetchClient.js
l2-p14/src/forms/enrolController.js
l2-p14/src/forms/validation.js
l2-p14/src/main.js
l2-p14/src/pages/clubsPage.js
l2-p14/src/pages/enrolPage.js
l2-p14/src/services/clubs.js
l2-p14/src/utils/storage.js
l2-p14/styles.css
l2-p14/tests/config.json
l2-p14/tests/fixtures/clubs.json
l2-p14/tests/unit/patterns.jest.test.cjs
l2-p14/tests/unit/patterns.vitest.test.ts
l2-p14/vitest.config.ts
l2-p15/README.md
l2-p15/jest.config.cjs
l2-p15/package.json
l2-p15/public/index.html
l2-p15/server.mjs
l2-p15/src/addons/advanced.js
l2-p15/src/api/fetchClient.js
l2-p15/src/forms/enrolController.js
l2-p15/src/forms/validation.js
l2-p15/src/main.js
l2-p15/src/pages/clubsPage.js
l2-p15/src/pages/enrolPage.js
l2-p15/src/services/clubs.js
l2-p15/src/utils/storage.js
l2-p15/styles.css
l2-p15/tests/config.json
l2-p15/tests/fixtures/clubs.json
l2-p15/tests/unit/patterns.jest.test.cjs
l2-p15/tests/unit/patterns.vitest.test.ts
l2-p15/vitest.config.ts
l3-p01/README.md
l3-p01/jest.config.cjs
l3-p01/package.json
l3-p01/public/index.html
l3-p01/server.mjs
l3-p01/src/addons/advanced.js
l3-p01/src/api/fetchClient.js
l3-p01/src/forms/enrolController.js
l3-p01/src/forms/validation.js
l3-p01/src/main.js
l3-p01/src/pages/clubsPage.js
l3-p01/src/pages/enrolPage.js
l3-p01/src/services/clubs.js
l3-p01/src/utils/storage.js
l3-p01/styles.css
l3-p01/tests/config.json
l3-p01/tests/fixtures/clubs.json
l3-p01/tests/unit/patterns.jest.test.cjs
l3-p01/tests/unit/patterns.vitest.test.ts
l3-p01/vitest.config.ts
l3-p02/README.md
l3-p02/jest.config.cjs
l3-p02/package.json
l3-p02/public/index.html
l3-p02/server.mjs
l3-p02/src/addons/advanced.js
l3-p02/src/api/fetchClient.js
l3-p02/src/forms/enrolController.js
l3-p02/src/forms/validation.js
l3-p02/src/main.js
l3-p02/src/pages/clubsPage.js
l3-p02/src/pages/enrolPage.js
l3-p02/src/services/clubs.js
l3-p02/src/utils/storage.js
l3-p02/styles.css
l3-p02/tests/config.json
l3-p02/tests/fixtures/clubs.json
l3-p02/tests/unit/patterns.jest.test.cjs
l3-p02/tests/unit/patterns.vitest.test.ts
l3-p02/vitest.config.ts
l3-p03/README.md
l3-p03/jest.config.cjs
l3-p03/package.json
l3-p03/public/index.html
l3-p03/server.mjs
l3-p03/src/addons/advanced.js
l3-p03/src/api/fetchClient.js
l3-p03/src/forms/enrolController.js
l3-p03/src/forms/validation.js
l3-p03/src/main.js
l3-p03/src/pages/clubsPage.js
l3-p03/src/pages/enrolPage.js
l3-p03/src/services/clubs.js
l3-p03/src/utils/storage.js
l3-p03/styles.css
l3-p03/tests/config.json
l3-p03/tests/fixtures/clubs.json
l3-p03/tests/unit/patterns.jest.test.cjs
l3-p03/tests/unit/patterns.vitest.test.ts
l3-p03/vitest.config.ts
l3-p04/README.md
l3-p04/jest.config.cjs
l3-p04/package.json
l3-p04/public/index.html
l3-p04/server.mjs
l3-p04/src/addons/advanced.js
l3-p04/src/api/fetchClient.js
l3-p04/src/forms/enrolController.js
l3-p04/src/forms/validation.js
l3-p04/src/main.js
l3-p04/src/pages/clubsPage.js
l3-p04/src/pages/enrolPage.js
l3-p04/src/services/clubs.js
l3-p04/src/utils/storage.js
l3-p04/styles.css
l3-p04/tests/config.json
l3-p04/tests/fixtures/clubs.json
l3-p04/tests/unit/patterns.jest.test.cjs
l3-p04/tests/unit/patterns.vitest.test.ts
l3-p04/vitest.config.ts
l3-p05/README.md
l3-p05/jest.config.cjs
l3-p05/package.json
l3-p05/public/index.html
l3-p05/server.mjs
l3-p05/src/addons/advanced.js
l3-p05/src/api/fetchClient.js
l3-p05/src/forms/enrolController.js
l3-p05/src/forms/validation.js
l3-p05/src/main.js
l3-p05/src/pages/clubsPage.js
l3-p05/src/pages/enrolPage.js
l3-p05/src/services/clubs.js
l3-p05/src/utils/storage.js
l3-p05/styles.css
l3-p05/tests/config.json
l3-p05/tests/fixtures/clubs.json
l3-p05/tests/unit/patterns.jest.test.cjs
l3-p05/tests/unit/patterns.vitest.test.ts
l3-p05/vitest.config.ts
l3-p06/README.md
l3-p06/jest.config.cjs
l3-p06/package.json
l3-p06/public/index.html
l3-p06/server.mjs
l3-p06/src/addons/advanced.js
l3-p06/src/api/fetchClient.js
l3-p06/src/forms/enrolController.js
l3-p06/src/forms/validation.js
l3-p06/src/main.js
l3-p06/src/pages/clubsPage.js
l3-p06/src/pages/enrolPage.js
l3-p06/src/services/clubs.js
l3-p06/src/utils/storage.js
l3-p06/styles.css
l3-p06/tests/config.json
l3-p06/tests/fixtures/clubs.json
l3-p06/tests/unit/patterns.jest.test.cjs
l3-p06/tests/unit/patterns.vitest.test.ts
l3-p06/vitest.config.ts
l3-p07/README.md
l3-p07/jest.config.cjs
l3-p07/package.json
l3-p07/public/index.html
l3-p07/server.mjs
l3-p07/src/addons/advanced.js
l3-p07/src/api/fetchClient.js
l3-p07/src/forms/enrolController.js
l3-p07/src/forms/validation.js
l3-p07/src/main.js
l3-p07/src/pages/clubsPage.js
l3-p07/src/pages/enrolPage.js
l3-p07/src/services/clubs.js
l3-p07/src/utils/storage.js
l3-p07/styles.css
l3-p07/tests/config.json
l3-p07/tests/fixtures/clubs.json
l3-p07/tests/unit/patterns.jest.test.cjs
l3-p07/tests/unit/patterns.vitest.test.ts
l3-p07/vitest.config.ts
l3-p08/README.md
l3-p08/jest.config.cjs
l3-p08/package.json
l3-p08/public/index.html
l3-p08/server.mjs
l3-p08/src/addons/advanced.js
l3-p08/src/api/fetchClient.js
l3-p08/src/forms/enrolController.js
l3-p08/src/forms/validation.js
l3-p08/src/main.js
l3-p08/src/pages/clubsPage.js
l3-p08/src/pages/enrolPage.js
l3-p08/src/services/clubs.js
l3-p08/src/utils/storage.js
l3-p08/styles.css
l3-p08/tests/config.json
l3-p08/tests/fixtures/clubs.json
l3-p08/tests/unit/patterns.jest.test.cjs
l3-p08/tests/unit/patterns.vitest.test.ts
l3-p08/vitest.config.ts
l3-p09/README.md
l3-p09/jest.config.cjs
l3-p09/package.json
l3-p09/public/index.html
l3-p09/server.mjs
l3-p09/src/addons/advanced.js
l3-p09/src/api/fetchClient.js
l3-p09/src/forms/enrolController.js
l3-p09/src/forms/validation.js
l3-p09/src/main.js
l3-p09/src/pages/clubsPage.js
l3-p09/src/pages/enrolPage.js
l3-p09/src/services/clubs.js
l3-p09/src/utils/storage.js
l3-p09/styles.css
l3-p09/tests/config.json
l3-p09/tests/fixtures/clubs.json
l3-p09/tests/unit/patterns.jest.test.cjs
l3-p09/tests/unit/patterns.vitest.test.ts
l3-p09/vitest.config.ts
l3-p10/README.md
l3-p10/jest.config.cjs
l3-p10/package.json
l3-p10/public/index.html
l3-p10/server.mjs
l3-p10/src/addons/advanced.js
l3-p10/src/api/fetchClient.js
l3-p10/src/forms/enrolController.js
l3-p10/src/forms/validation.js
l3-p10/src/main.js
l3-p10/src/pages/clubsPage.js
l3-p10/src/pages/enrolPage.js
l3-p10/src/services/clubs.js
l3-p10/src/utils/storage.js
l3-p10/styles.css
l3-p10/tests/config.json
l3-p10/tests/fixtures/clubs.json
l3-p10/tests/unit/patterns.jest.test.cjs
l3-p10/tests/unit/patterns.vitest.test.ts
l3-p10/vitest.config.ts
l3-p11/README.md
l3-p11/jest.config.cjs
l3-p11/package.json
l3-p11/public/index.html
l3-p11/server.mjs
l3-p11/src/addons/advanced.js
l3-p11/src/api/fetchClient.js
l3-p11/src/forms/enrolController.js
l3-p11/src/forms/validation.js
l3-p11/src/main.js
l3-p11/src/pages/clubsPage.js
l3-p11/src/pages/enrolPage.js
l3-p11/src/services/clubs.js
l3-p11/src/utils/storage.js
l3-p11/styles.css
l3-p11/tests/config.json
l3-p11/tests/fixtures/clubs.json
l3-p11/tests/unit/patterns.jest.test.cjs
l3-p11/tests/unit/patterns.vitest.test.ts
l3-p11/vitest.config.ts
l3-p12/README.md
l3-p12/jest.config.cjs
l3-p12/package.json
l3-p12/public/index.html
l3-p12/server.mjs
l3-p12/src/addons/advanced.js
l3-p12/src/api/fetchClient.js
l3-p12/src/forms/enrolController.js
l3-p12/src/forms/validation.js
l3-p12/src/main.js
l3-p12/src/pages/clubsPage.js
l3-p12/src/pages/enrolPage.js
l3-p12/src/services/clubs.js
l3-p12/src/utils/storage.js
l3-p12/styles.css
l3-p12/tests/config.json
l3-p12/tests/fixtures/clubs.json
l3-p12/tests/unit/patterns.jest.test.cjs
l3-p12/tests/unit/patterns.vitest.test.ts
l3-p12/vitest.config.ts
l3-p13/README.md
l3-p13/jest.config.cjs
l3-p13/package.json
l3-p13/public/index.html
l3-p13/server.mjs
l3-p13/src/addons/advanced.js
l3-p13/src/api/fetchClient.js
l3-p13/src/forms/enrolController.js
l3-p13/src/forms/validation.js
l3-p13/src/main.js
l3-p13/src/pages/clubsPage.js
l3-p13/src/pages/enrolPage.js
l3-p13/src/services/clubs.js
l3-p13/src/utils/storage.js
l3-p13/styles.css
l3-p13/tests/config.json
l3-p13/tests/fixtures/clubs.json
l3-p13/tests/unit/patterns.jest.test.cjs
l3-p13/tests/unit/patterns.vitest.test.ts
l3-p13/vitest.config.ts
l3-p14/README.md
l3-p14/jest.config.cjs
l3-p14/package.json
l3-p14/public/index.html
l3-p14/server.mjs
l3-p14/src/addons/advanced.js
l3-p14/src/api/fetchClient.js
l3-p14/src/forms/enrolController.js
l3-p14/src/forms/validation.js
l3-p14/src/main.js
l3-p14/src/pages/clubsPage.js
l3-p14/src/pages/enrolPage.js
l3-p14/src/services/clubs.js
l3-p14/src/utils/storage.js
l3-p14/styles.css
l3-p14/tests/config.json
l3-p14/tests/fixtures/clubs.json
l3-p14/tests/unit/patterns.jest.test.cjs
l3-p14/tests/unit/patterns.vitest.test.ts
l3-p14/vitest.config.ts
l3-p15/README.md
l3-p15/jest.config.cjs
l3-p15/package.json
l3-p15/public/index.html
l3-p15/server.mjs
l3-p15/src/addons/advanced.js
l3-p15/src/api/fetchClient.js
l3-p15/src/forms/enrolController.js
l3-p15/src/forms/validation.js
l3-p15/src/main.js
l3-p15/src/pages/clubsPage.js
l3-p15/src/pages/enrolPage.js
l3-p15/src/services/clubs.js
l3-p15/src/utils/storage.js
l3-p15/styles.css
l3-p15/tests/config.json
l3-p15/tests/fixtures/clubs.json
l3-p15/tests/unit/patterns.jest.test.cjs
l3-p15/tests/unit/patterns.vitest.test.ts
l3-p15/vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** other: 45, config: 180, docs: 45, public: 45, code: 405, tests: 180.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `l1-p01/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p02/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p03/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p04/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p05/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p06/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p07/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p08/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p09/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p10/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p11/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p12/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p13/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p14/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l1-p15/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p01/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p02/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p03/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p04/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p05/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p06/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p07/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p08/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p09/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p10/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p11/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p12/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p13/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p14/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l2-p15/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p01/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p02/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p03/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p04/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p05/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p06/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p07/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p08/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p09/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p10/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p11/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p12/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p13/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p14/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors
- `l3-p15/package.json`: name=`s7p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `node server.mjs`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express
  - **DevDeps:** vitest, jest, jsdom, cors

### Seminar7_Partea3_p3-READMEs.zip

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

## 2. Sinteza documentelor DOCX (teorie ↔ laborator ↔ proiecte)

### Seminar7_Partea1_Teorie.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 7 — Fetch API + formulare + JSON + persistență minimă
Partea 1: Teorie (extins)
- Hook realist: înscriere la hackathon în câteva ore, doar cu „vanilla” web
- Dimineața, ora 10:00. La ora 16:00 are loc lansarea înscrierilor pentru hackathonul organizat de „Clubs & Associations Hub”. Ți se cere o pagină publică ce listează cluburile disponibile (sursă: un API simplu) și un formular prin care studenții se pot înscrie. Cerințele par „banale”: validezi câmpuri (nume, e‑mail, acord), trimiți **JSON** la server, afișezi mesaje de succes sau eroare și salvezi local progresul dacă pică rețeaua. Nu ai voie framework‑uri; lucrezi cu **HTML** semantic, **CSS** moderat, **JavaScript** modern și **Fetch API**. Persistența este „minimală”: **localStorage** pentru cache de listă și „draft autosave” pentru formular; eventual, un mic **mock server** (Express) în laborator. Timpul este scurt, greșelile tipice (validare ascunsă, mesaje criptice, blocaje UI, lipsa time‑out‑ului) se plătesc scump. Acest seminar este planul tău de zbor.

### Seminar7_Partea2_Ghid_Arhive.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhivele pentru Seminarul 7, Partea 2
- Ce conțin arhivele
- • **s7p2-lab.zip (standalone)**: proiect unic cu `public/`, `src/`, `tests/` (Vitest & Jest), `server.mjs`, `package.json`, `styles.css`.

### Seminar7_Partea2_Laborator_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 7 — Partea 2: Laborator (extins)
Fetch API + formulare + JSON + persistență minimă
- Obiectivul laboratorului și scenariul pe care îl implementăm
- În acest laborator construim, pas cu pas, o experiență completă „form + listă de date” pentru **Clubs & Associations Hub**, folosind strict browser APIs moderne: **Fetch API** pentru comunicarea HTTP, **HTML forms** cu **Constraint Validation API** + validare custom, **JSON** pentru schimb de date și o **persistență minimă** pe client (cache + draft autosave) pentru reziliență. Vom urmări o abordare **mobile‑first**, vom proiecta fluxul ca pe o **mașină de stări** (`idle → loading → success|error`) și vom scrie **teste unitare** în paralel (Vitest & Jest) pentru părțile critice: `fetchClient` (timeout/retry), validare (predicates pure), persistență (TTL/draft) și actualizări UI.

### Seminar7_Partea3_Arhive_Ghid.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhivele Partea 3
- Ce conțin arhivele
- • **Standalone**: 45 proiecte (`l1-p01` … `l3-p15`), fiecare cu `public/index.html`, `styles.css`, `src/` (api/forms/services/pages/utils/addons), `tests/` (Vitest+Jest, checker de pattern), `server.mjs`, `package.json`, `README.md`.

### Seminar7_Partea3_Proiecte_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 7 — Partea 3: Proiecte/teme (extins)
- Metodologie & obiective
- Partea 3 livrează **45 de proiecte** axate pe **Fetch API, formulare, JSON și persistență minimă**. Fiecare proiect include: **Scop didactic**, **Specificații**, **Criterii de acceptare** (măsurabile), **Soluție (rezumat)** și **AI‑assist (VSL)**. Arhivele conțin startere executabile (mock Express, structuri modulare, teste unitare Vitest & Jest).

## 3. Monorepo vs. standalone — analiză comparativă


**Manageri de pachete & workspaces.** Monorepo (PNPM 9+) declară `packages/*` în `pnpm-workspace.yaml` și/sau `workspaces` în `package.json`, cu instalare la rădăcină (`pnpm i -w`). Standalone instalează local (`npm i`).

**Comenzi de instalare/testare.** Monorepo: `pnpm -w run test` sau `pnpm --filter <pkg> run test`. Standalone: `npm test`. Testele sunt **oglindite** (Vitest & Jest) pe aceleași contracte (retry/timeout, validare, TTL/draft, UI states). 

**Integrare CI.** Monorepo agregă pipelines (lint, unit, e2e) în `.github/workflows/*` ; standalone tinde să le aibă per proiect. 

**Avantaje/Dezavantaje.** Standalone — simplitate pentru începători; Monorepo — scalare pentru colecții mari (ex. 45 proiecte L1–L3), partajare de configuri și execuții rapide în CI; costul este înțelegerea filtrării PNPM și a dependențelor partajate.
## 4. Rolul fișierelor cheie (config, cod, teste, extra)

| Fișier / tip | Rol |
|---|---|
| `server.mjs` | Mock Express: rute `GET /api/clubs` și `POST /api/registrations`. |
| `package.json` | Manifestul proiectului: metadate, dependențe, scripturi; definește `type:"module"` pentru ESM. |
| `vitest.config.ts` | Configurarea Vitest (JSDOM/Node, reporters, setup). |
| `jest.config.cjs` | Configurarea Jest (JSDOM, transform ESM cu `--experimental-vm-modules` sau `babel-jest`). |
| `pnpm-workspace.yaml` | Declară pachetele din monorepo pentru PNPM. |
| `public/index.html` | Pagină listă clubs; include `<ul id="clubs">` și aria-live pentru status. |
| `public/enrol.html` | Formular semantic; aria-live pentru status și câmpuri necesare. |
| `src/api/fetchClient.js` | Wrapper Fetch cu timeout, retry(backoff+jitter), helperi JSON și `HttpError`. |
| `src/forms/validation.js` | Validare „pură” `{ ok, data, errors }` pentru înscriere. |
| `src/forms/enrolController.js` | `attachEnrolForm()`, mașină de stări submit, autosave & reset. |
| `src/utils/storage.js` | Namespace localStorage, TTL + draft autosave. |

## 5. Corelații cod ↔ configurări ↔ teste


- **Formular (`public/enrol.html`) + controller (`src/forms/enrolController.js`)**: submit JSON (mașină de stări), mesaje `aria-live`, reset pe succes, autosave — verificate în **ambele suite** (Vitest & Jest).  
- **`src/api/fetchClient.js`**: `timeout` + `retry(3)` (5xx/rețea) cu backoff+jitter; `jsonGet/jsonPost` ridică `HttpError` cu payload; testele asertă comportamentul.  
- **`src/services/clubs.js`**: cache **TTL 5 min** + **SWR** (livrezi cache, reîmprospătezi în fundal) — testat pe ambele motoare.  
- **`.env.example`** — dacă apare în unele pachete, ghidează portul/mock‑ul; `server.mjs` citește `PORT` (dacă e configurat).  
- **ESLint + CI**: rulează `lint` și `test` în workflows; erorile de stil și de contract sunt blocate înainte de merge.  
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S7 antrenează competențe fundamentale pentru **interacțiunea client–server** în web‑ul modern: **Fetch API**, **formulare semantice**, **JSON** și **persistență minimă** (cache TTL + SWR, „draft autosave”). Laboratorul livrează un mock server Express, iar proiectele (L1–L3) scafoldează treptat către politici robuste (timeout, retry, idempotency guard), accesibilitate și observabilitate ușoară. ### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; rădăcină + `packages/*` |
| Instalare | `npm i` | `pnpm i -w` |
| Testare | `npm test` (Vitest & Jest) | `pnpm -w run test` sau `--filter` |
| CI | Workflows simple per proiect | Workflows agregate, matrice pe pachete |
| Scalare (45 proiecte) | multiplicare directoare | pachete dedicate în `packages/*` |
| Public țintă | începători | echipe/colecții avansate |
### Inventar pe arhivă (roluri)

- **Seminar7_Partea2_p2-lab.zip** — other=1, config=4, docs=1, public=2, code=8, tests=11.
- **Seminar7_Partea2_p2-monorepo.zip** — config=6, other=1, docs=1, public=2, code=8, tests=11.
- **Seminar7_Partea3_p3-monorepo.zip** — config=182, other=45, docs=45, public=45, code=405, tests=180.
- **Seminar7_Partea3_p3-standalone.zip** — other=45, config=180, docs=45, public=45, code=405, tests=180.
- **Seminar7_Partea3_p3-READMEs.zip** — docs=45.
### Explicații fișier-cu-fișier

Consultați tabelul din §4; laboratoarele folosesc aceleași convenții (module `api/`, `forms/`, `services/`, `pages/`, `utils/`; testele sunt dublate Vitest/Jest).
### Corelații între fișiere


- `src/api/fetchClient.js` ↔ `tests/*`: retry/timeout, JSON helpers, `HttpError`.  
- `src/forms/validation.js` ↔ `tests/*`: predicates pure (nume/email/consent).  
- `src/utils/storage.js` ↔ `tests/*`: TTL și draft autosave.  
- `.github/workflows/*` ↔ `lint`/`test`: pipeline determinist pentru PR-uri.  
### Recomandări pentru studenți


1) **Începeți în standalone**, apoi scalați în monorepo pentru colecții mari.  
2) **Gândiți în contracte**: aceeași semnătură a funcțiilor testată în Vitest **și** Jest.  
3) **Implementați `AbortController` + timeout** și **retry controlat** (doar 5xx/rețea).  
4) **Separați validarea** (funcții pure) de DOM; folosiți `aria-live` și focus management.  
5) **Persistență minimă**: TTL + SWR pentru GET; autosave pentru formular; curățați draftul la succes.  
6) **Evitați XSS** (folosiți `textContent`) și păstrați un mic **logger** non‑PII.  
### Instrucțiuni „Quick start” per arhivă


**Partea 2 — standalone (p2-lab):**
```bash
unzip "Seminar7_Partea2_p2-lab.zip" -d s7p2-standalone
cd s7p2-standalone
npm i
npm run dev     # pornește mock server (ex.: http://localhost:5270)
npm test        # rulează Vitest & Jest
```

**Partea 2 — monorepo:**
```bash
unzip "Seminar7_Partea2_p2-monorepo.zip" -d s7p2-monorepo
cd s7p2-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter ./packages/app run dev
```

**Partea 3 — monorepo (proiecte):**
```bash
unzip "Seminar7_Partea3_p3-monorepo.zip" -d s7p3-monorepo
cd s7p3-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter ./packages/l1-p01 run dev
```

**Partea 3 — standalone (proiecte):**
```bash
unzip "Seminar7_Partea3_p3-standalone.zip" -d s7p3-standalone
cd s7p3-standalone/l1-p01
npm i
npm test
npm run dev
```
### Troubleshooting (erori frecvente)


- **CORS**: pentru back‑end real, configurează antetele `Access-Control-Allow-*`; mock‑ul folosește `cors()`.  
- **Timeout prea scurt/lung**: 6–8s e pragmatic; ajustează și folosește `AbortController`.  
- **Retry pe 4xx**: evită; aplică retry doar pentru `5xx`/rețea.  
- **TTL**: în test folosește TTL mic; verifică `expiresAt`.  
- **Jest ESM**: rulează cu `--experimental-vm-modules` sau `babel-jest`.  
- **Port ocupat**: schimbă `PORT` în `server.mjs`.  
- **PNPM filter**: verifică `pnpm-workspace.yaml` și câmpul `name` din `package.json`.  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** — HTTP, Fetch, formulare, JSON, persist. minimă, a11y, securitate; toate se regăsesc în `api/forms/services/utils` și în testele aferente.  
- **Partea 2 (Laborator extins)** — „Clubs & Enrol”: wrapper Fetch (timeout/retry), validare pură, TTL + SWR, autosave; testare dublă Vitest/Jest; reflectat în structuri și scripturi.  
- **Partea 3 (Ghid Arhive + Proiecte)** — 45 proiecte L1–L3 (standalone & monorepo), addons (Playwright, SW demo) și rubrică; mapping direct în inventare și instrucțiuni.  
### Prompt-șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S7** (standalone & monorepo) un set „Clubs & Enrol” cu Fetch API, formulare semantice, JSON, timeout+retry (5xx/rețea), cache TTL + SWR, draft autosave, testare dublă **Vitest/Jest**, CI, README cu Quick start & Troubleshooting, și variante **starter**/**solution**.”
