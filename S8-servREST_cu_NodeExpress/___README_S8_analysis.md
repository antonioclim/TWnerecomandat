# Seminarul S8 — REST cu Node/Express (standalone & monorepo) — Analiză integrată a arhivelor și ghidurilor

*Generat la 2025-09-21 05:02.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar8_Partea2_p2-monorepo.zip

```
package.json
packages/api/README.md
packages/api/jest.config.cjs
packages/api/package.json
packages/api/src/app.js
packages/api/src/controllers/clubs.controller.js
packages/api/src/controllers/registrations.controller.js
packages/api/src/errors/problem.js
packages/api/src/middlewares/correlationId.js
packages/api/src/middlewares/errors.js
packages/api/src/middlewares/logger.js
packages/api/src/middlewares/notFound.js
packages/api/src/middlewares/validate.js
packages/api/src/repo/inMemoryStore.js
packages/api/src/routes/clubs.routes.js
packages/api/src/routes/health.routes.js
packages/api/src/routes/registrations.routes.js
packages/api/src/schemas/club.schema.js
packages/api/src/schemas/registration.schema.js
packages/api/src/server.js
packages/api/src/utils/etag.js
packages/api/src/utils/pagination.js
packages/api/tests/jest/http.test.cjs
packages/api/tests/jest/unit.test.cjs
packages/api/tests/vitest/http.test.ts
packages/api/tests/vitest/unit.test.ts
packages/api/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 5, docs: 1, code: 18, tests: 4.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s8p2-monorepo` type=`commonjs` workspaces=True
  - **Scripturi:**
  - `test:vitest` → `pnpm -r --filter ./packages run test:vitest`
  - `test:jest` → `pnpm -r --filter ./packages run test:jest`
  - `test` → `pnpm -r --filter ./packages run test`
  - **Deps:** 
  - **DevDeps:** pnpm, vitest, jest, supertest, nodemon
- `packages/api/package.json`: name=`s8-rest-api` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest

### Seminar8_Partea2_p2-standalone.zip

```
README.md
jest.config.cjs
package.json
src/app.js
src/controllers/clubs.controller.js
src/controllers/registrations.controller.js
src/errors/problem.js
src/middlewares/correlationId.js
src/middlewares/errors.js
src/middlewares/logger.js
src/middlewares/notFound.js
src/middlewares/validate.js
src/repo/inMemoryStore.js
src/routes/clubs.routes.js
src/routes/health.routes.js
src/routes/registrations.routes.js
src/schemas/club.schema.js
src/schemas/registration.schema.js
src/server.js
src/utils/etag.js
src/utils/pagination.js
tests/jest/http.test.cjs
tests/jest/unit.test.cjs
tests/vitest/http.test.ts
tests/vitest/unit.test.ts
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 3, docs: 1, code: 18, tests: 4.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s8-rest-api` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest

### Seminar8_Partea3_p3-monorepo.zip

```
package.json
packages/l1-p01/README.md
packages/l1-p01/jest.config.cjs
packages/l1-p01/package.json
packages/l1-p01/src/app.js
packages/l1-p01/src/errors/problem.js
packages/l1-p01/src/middlewares/correlationId.js
packages/l1-p01/src/middlewares/errors.js
packages/l1-p01/src/middlewares/logger.js
packages/l1-p01/src/middlewares/notFound.js
packages/l1-p01/src/routes/health.routes.js
packages/l1-p01/src/server.js
packages/l1-p01/tests/config.json
packages/l1-p01/tests/jest/http-smoke.jest.test.cjs
packages/l1-p01/tests/jest/patterns.jest.test.cjs
packages/l1-p01/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p01/tests/vitest/patterns.vitest.test.ts
packages/l1-p01/vitest.config.ts
packages/l1-p02/README.md
packages/l1-p02/jest.config.cjs
packages/l1-p02/package.json
packages/l1-p02/src/app.js
packages/l1-p02/src/errors/problem.js
packages/l1-p02/src/middlewares/correlationId.js
packages/l1-p02/src/middlewares/errors.js
packages/l1-p02/src/middlewares/logger.js
packages/l1-p02/src/middlewares/notFound.js
packages/l1-p02/src/routes/health.routes.js
packages/l1-p02/src/server.js
packages/l1-p02/tests/config.json
packages/l1-p02/tests/jest/http-smoke.jest.test.cjs
packages/l1-p02/tests/jest/patterns.jest.test.cjs
packages/l1-p02/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p02/tests/vitest/patterns.vitest.test.ts
packages/l1-p02/vitest.config.ts
packages/l1-p03/README.md
packages/l1-p03/jest.config.cjs
packages/l1-p03/package.json
packages/l1-p03/src/app.js
packages/l1-p03/src/errors/problem.js
packages/l1-p03/src/middlewares/correlationId.js
packages/l1-p03/src/middlewares/errors.js
packages/l1-p03/src/middlewares/logger.js
packages/l1-p03/src/middlewares/notFound.js
packages/l1-p03/src/routes/health.routes.js
packages/l1-p03/src/server.js
packages/l1-p03/tests/config.json
packages/l1-p03/tests/jest/http-smoke.jest.test.cjs
packages/l1-p03/tests/jest/patterns.jest.test.cjs
packages/l1-p03/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p03/tests/vitest/patterns.vitest.test.ts
packages/l1-p03/vitest.config.ts
packages/l1-p04/README.md
packages/l1-p04/jest.config.cjs
packages/l1-p04/package.json
packages/l1-p04/src/app.js
packages/l1-p04/src/errors/problem.js
packages/l1-p04/src/middlewares/correlationId.js
packages/l1-p04/src/middlewares/errors.js
packages/l1-p04/src/middlewares/logger.js
packages/l1-p04/src/middlewares/notFound.js
packages/l1-p04/src/routes/health.routes.js
packages/l1-p04/src/server.js
packages/l1-p04/tests/config.json
packages/l1-p04/tests/jest/http-smoke.jest.test.cjs
packages/l1-p04/tests/jest/patterns.jest.test.cjs
packages/l1-p04/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p04/tests/vitest/patterns.vitest.test.ts
packages/l1-p04/vitest.config.ts
packages/l1-p05/README.md
packages/l1-p05/jest.config.cjs
packages/l1-p05/package.json
packages/l1-p05/src/app.js
packages/l1-p05/src/errors/problem.js
packages/l1-p05/src/middlewares/correlationId.js
packages/l1-p05/src/middlewares/errors.js
packages/l1-p05/src/middlewares/logger.js
packages/l1-p05/src/middlewares/notFound.js
packages/l1-p05/src/routes/health.routes.js
packages/l1-p05/src/server.js
packages/l1-p05/tests/config.json
packages/l1-p05/tests/jest/http-smoke.jest.test.cjs
packages/l1-p05/tests/jest/patterns.jest.test.cjs
packages/l1-p05/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p05/tests/vitest/patterns.vitest.test.ts
packages/l1-p05/vitest.config.ts
packages/l1-p06/README.md
packages/l1-p06/jest.config.cjs
packages/l1-p06/package.json
packages/l1-p06/src/app.js
packages/l1-p06/src/errors/problem.js
packages/l1-p06/src/middlewares/correlationId.js
packages/l1-p06/src/middlewares/errors.js
packages/l1-p06/src/middlewares/logger.js
packages/l1-p06/src/middlewares/notFound.js
packages/l1-p06/src/routes/health.routes.js
packages/l1-p06/src/server.js
packages/l1-p06/tests/config.json
packages/l1-p06/tests/jest/http-smoke.jest.test.cjs
packages/l1-p06/tests/jest/patterns.jest.test.cjs
packages/l1-p06/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p06/tests/vitest/patterns.vitest.test.ts
packages/l1-p06/vitest.config.ts
packages/l1-p07/README.md
packages/l1-p07/jest.config.cjs
packages/l1-p07/package.json
packages/l1-p07/src/app.js
packages/l1-p07/src/errors/problem.js
packages/l1-p07/src/middlewares/correlationId.js
packages/l1-p07/src/middlewares/errors.js
packages/l1-p07/src/middlewares/logger.js
packages/l1-p07/src/middlewares/notFound.js
packages/l1-p07/src/routes/health.routes.js
packages/l1-p07/src/server.js
packages/l1-p07/tests/config.json
packages/l1-p07/tests/jest/http-smoke.jest.test.cjs
packages/l1-p07/tests/jest/patterns.jest.test.cjs
packages/l1-p07/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p07/tests/vitest/patterns.vitest.test.ts
packages/l1-p07/vitest.config.ts
packages/l1-p08/README.md
packages/l1-p08/jest.config.cjs
packages/l1-p08/package.json
packages/l1-p08/src/app.js
packages/l1-p08/src/errors/problem.js
packages/l1-p08/src/middlewares/correlationId.js
packages/l1-p08/src/middlewares/errors.js
packages/l1-p08/src/middlewares/logger.js
packages/l1-p08/src/middlewares/notFound.js
packages/l1-p08/src/routes/health.routes.js
packages/l1-p08/src/server.js
packages/l1-p08/tests/config.json
packages/l1-p08/tests/jest/http-smoke.jest.test.cjs
packages/l1-p08/tests/jest/patterns.jest.test.cjs
packages/l1-p08/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p08/tests/vitest/patterns.vitest.test.ts
packages/l1-p08/vitest.config.ts
packages/l1-p09/README.md
packages/l1-p09/jest.config.cjs
packages/l1-p09/package.json
packages/l1-p09/src/app.js
packages/l1-p09/src/errors/problem.js
packages/l1-p09/src/middlewares/correlationId.js
packages/l1-p09/src/middlewares/errors.js
packages/l1-p09/src/middlewares/logger.js
packages/l1-p09/src/middlewares/notFound.js
packages/l1-p09/src/routes/health.routes.js
packages/l1-p09/src/server.js
packages/l1-p09/tests/config.json
packages/l1-p09/tests/jest/http-smoke.jest.test.cjs
packages/l1-p09/tests/jest/patterns.jest.test.cjs
packages/l1-p09/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p09/tests/vitest/patterns.vitest.test.ts
packages/l1-p09/vitest.config.ts
packages/l1-p10/README.md
packages/l1-p10/jest.config.cjs
packages/l1-p10/package.json
packages/l1-p10/src/app.js
packages/l1-p10/src/errors/problem.js
packages/l1-p10/src/middlewares/correlationId.js
packages/l1-p10/src/middlewares/errors.js
packages/l1-p10/src/middlewares/logger.js
packages/l1-p10/src/middlewares/notFound.js
packages/l1-p10/src/routes/health.routes.js
packages/l1-p10/src/server.js
packages/l1-p10/tests/config.json
packages/l1-p10/tests/jest/http-smoke.jest.test.cjs
packages/l1-p10/tests/jest/patterns.jest.test.cjs
packages/l1-p10/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p10/tests/vitest/patterns.vitest.test.ts
packages/l1-p10/vitest.config.ts
packages/l1-p11/README.md
packages/l1-p11/jest.config.cjs
packages/l1-p11/package.json
packages/l1-p11/src/app.js
packages/l1-p11/src/errors/problem.js
packages/l1-p11/src/middlewares/correlationId.js
packages/l1-p11/src/middlewares/errors.js
packages/l1-p11/src/middlewares/logger.js
packages/l1-p11/src/middlewares/notFound.js
packages/l1-p11/src/routes/health.routes.js
packages/l1-p11/src/server.js
packages/l1-p11/tests/config.json
packages/l1-p11/tests/jest/http-smoke.jest.test.cjs
packages/l1-p11/tests/jest/patterns.jest.test.cjs
packages/l1-p11/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p11/tests/vitest/patterns.vitest.test.ts
packages/l1-p11/vitest.config.ts
packages/l1-p12/README.md
packages/l1-p12/jest.config.cjs
packages/l1-p12/package.json
packages/l1-p12/src/app.js
packages/l1-p12/src/errors/problem.js
packages/l1-p12/src/middlewares/correlationId.js
packages/l1-p12/src/middlewares/errors.js
packages/l1-p12/src/middlewares/logger.js
packages/l1-p12/src/middlewares/notFound.js
packages/l1-p12/src/routes/health.routes.js
packages/l1-p12/src/server.js
packages/l1-p12/tests/config.json
packages/l1-p12/tests/jest/http-smoke.jest.test.cjs
packages/l1-p12/tests/jest/patterns.jest.test.cjs
packages/l1-p12/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p12/tests/vitest/patterns.vitest.test.ts
packages/l1-p12/vitest.config.ts
packages/l1-p13/README.md
packages/l1-p13/jest.config.cjs
packages/l1-p13/package.json
packages/l1-p13/src/app.js
packages/l1-p13/src/errors/problem.js
packages/l1-p13/src/middlewares/correlationId.js
packages/l1-p13/src/middlewares/errors.js
packages/l1-p13/src/middlewares/logger.js
packages/l1-p13/src/middlewares/notFound.js
packages/l1-p13/src/routes/health.routes.js
packages/l1-p13/src/server.js
packages/l1-p13/tests/config.json
packages/l1-p13/tests/jest/http-smoke.jest.test.cjs
packages/l1-p13/tests/jest/patterns.jest.test.cjs
packages/l1-p13/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p13/tests/vitest/patterns.vitest.test.ts
packages/l1-p13/vitest.config.ts
packages/l1-p14/README.md
packages/l1-p14/jest.config.cjs
packages/l1-p14/package.json
packages/l1-p14/src/app.js
packages/l1-p14/src/errors/problem.js
packages/l1-p14/src/middlewares/correlationId.js
packages/l1-p14/src/middlewares/errors.js
packages/l1-p14/src/middlewares/logger.js
packages/l1-p14/src/middlewares/notFound.js
packages/l1-p14/src/routes/health.routes.js
packages/l1-p14/src/server.js
packages/l1-p14/tests/config.json
packages/l1-p14/tests/jest/http-smoke.jest.test.cjs
packages/l1-p14/tests/jest/patterns.jest.test.cjs
packages/l1-p14/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p14/tests/vitest/patterns.vitest.test.ts
packages/l1-p14/vitest.config.ts
packages/l1-p15/README.md
packages/l1-p15/jest.config.cjs
packages/l1-p15/package.json
packages/l1-p15/src/app.js
packages/l1-p15/src/errors/problem.js
packages/l1-p15/src/middlewares/correlationId.js
packages/l1-p15/src/middlewares/errors.js
packages/l1-p15/src/middlewares/logger.js
packages/l1-p15/src/middlewares/notFound.js
packages/l1-p15/src/routes/health.routes.js
packages/l1-p15/src/server.js
packages/l1-p15/tests/config.json
packages/l1-p15/tests/jest/http-smoke.jest.test.cjs
packages/l1-p15/tests/jest/patterns.jest.test.cjs
packages/l1-p15/tests/vitest/http-smoke.vitest.test.ts
packages/l1-p15/tests/vitest/patterns.vitest.test.ts
packages/l1-p15/vitest.config.ts
packages/l2-p01/README.md
packages/l2-p01/jest.config.cjs
packages/l2-p01/package.json
packages/l2-p01/src/app.js
packages/l2-p01/src/errors/problem.js
packages/l2-p01/src/middlewares/correlationId.js
packages/l2-p01/src/middlewares/errors.js
packages/l2-p01/src/middlewares/logger.js
packages/l2-p01/src/middlewares/notFound.js
packages/l2-p01/src/routes/health.routes.js
packages/l2-p01/src/server.js
packages/l2-p01/tests/config.json
packages/l2-p01/tests/jest/http-smoke.jest.test.cjs
packages/l2-p01/tests/jest/patterns.jest.test.cjs
packages/l2-p01/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p01/tests/vitest/patterns.vitest.test.ts
packages/l2-p01/vitest.config.ts
packages/l2-p02/README.md
packages/l2-p02/jest.config.cjs
packages/l2-p02/package.json
packages/l2-p02/src/app.js
packages/l2-p02/src/errors/problem.js
packages/l2-p02/src/middlewares/correlationId.js
packages/l2-p02/src/middlewares/errors.js
packages/l2-p02/src/middlewares/logger.js
packages/l2-p02/src/middlewares/notFound.js
packages/l2-p02/src/routes/health.routes.js
packages/l2-p02/src/server.js
packages/l2-p02/tests/config.json
packages/l2-p02/tests/jest/http-smoke.jest.test.cjs
packages/l2-p02/tests/jest/patterns.jest.test.cjs
packages/l2-p02/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p02/tests/vitest/patterns.vitest.test.ts
packages/l2-p02/vitest.config.ts
packages/l2-p03/README.md
packages/l2-p03/jest.config.cjs
packages/l2-p03/package.json
packages/l2-p03/src/app.js
packages/l2-p03/src/errors/problem.js
packages/l2-p03/src/middlewares/correlationId.js
packages/l2-p03/src/middlewares/errors.js
packages/l2-p03/src/middlewares/logger.js
packages/l2-p03/src/middlewares/notFound.js
packages/l2-p03/src/routes/health.routes.js
packages/l2-p03/src/server.js
packages/l2-p03/tests/config.json
packages/l2-p03/tests/jest/http-smoke.jest.test.cjs
packages/l2-p03/tests/jest/patterns.jest.test.cjs
packages/l2-p03/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p03/tests/vitest/patterns.vitest.test.ts
packages/l2-p03/vitest.config.ts
packages/l2-p04/README.md
packages/l2-p04/jest.config.cjs
packages/l2-p04/package.json
packages/l2-p04/src/app.js
packages/l2-p04/src/errors/problem.js
packages/l2-p04/src/middlewares/correlationId.js
packages/l2-p04/src/middlewares/errors.js
packages/l2-p04/src/middlewares/logger.js
packages/l2-p04/src/middlewares/notFound.js
packages/l2-p04/src/routes/health.routes.js
packages/l2-p04/src/server.js
packages/l2-p04/tests/config.json
packages/l2-p04/tests/jest/http-smoke.jest.test.cjs
packages/l2-p04/tests/jest/patterns.jest.test.cjs
packages/l2-p04/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p04/tests/vitest/patterns.vitest.test.ts
packages/l2-p04/vitest.config.ts
packages/l2-p05/README.md
packages/l2-p05/jest.config.cjs
packages/l2-p05/package.json
packages/l2-p05/src/app.js
packages/l2-p05/src/errors/problem.js
packages/l2-p05/src/middlewares/correlationId.js
packages/l2-p05/src/middlewares/errors.js
packages/l2-p05/src/middlewares/logger.js
packages/l2-p05/src/middlewares/notFound.js
packages/l2-p05/src/routes/health.routes.js
packages/l2-p05/src/server.js
packages/l2-p05/tests/config.json
packages/l2-p05/tests/jest/http-smoke.jest.test.cjs
packages/l2-p05/tests/jest/patterns.jest.test.cjs
packages/l2-p05/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p05/tests/vitest/patterns.vitest.test.ts
packages/l2-p05/vitest.config.ts
packages/l2-p06/README.md
packages/l2-p06/jest.config.cjs
packages/l2-p06/package.json
packages/l2-p06/src/app.js
packages/l2-p06/src/errors/problem.js
packages/l2-p06/src/middlewares/correlationId.js
packages/l2-p06/src/middlewares/errors.js
packages/l2-p06/src/middlewares/logger.js
packages/l2-p06/src/middlewares/notFound.js
packages/l2-p06/src/routes/health.routes.js
packages/l2-p06/src/server.js
packages/l2-p06/tests/config.json
packages/l2-p06/tests/jest/http-smoke.jest.test.cjs
packages/l2-p06/tests/jest/patterns.jest.test.cjs
packages/l2-p06/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p06/tests/vitest/patterns.vitest.test.ts
packages/l2-p06/vitest.config.ts
packages/l2-p07/README.md
packages/l2-p07/jest.config.cjs
packages/l2-p07/package.json
packages/l2-p07/src/app.js
packages/l2-p07/src/errors/problem.js
packages/l2-p07/src/middlewares/correlationId.js
packages/l2-p07/src/middlewares/errors.js
packages/l2-p07/src/middlewares/logger.js
packages/l2-p07/src/middlewares/notFound.js
packages/l2-p07/src/routes/health.routes.js
packages/l2-p07/src/server.js
packages/l2-p07/tests/config.json
packages/l2-p07/tests/jest/http-smoke.jest.test.cjs
packages/l2-p07/tests/jest/patterns.jest.test.cjs
packages/l2-p07/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p07/tests/vitest/patterns.vitest.test.ts
packages/l2-p07/vitest.config.ts
packages/l2-p08/README.md
packages/l2-p08/jest.config.cjs
packages/l2-p08/package.json
packages/l2-p08/src/app.js
packages/l2-p08/src/errors/problem.js
packages/l2-p08/src/middlewares/correlationId.js
packages/l2-p08/src/middlewares/errors.js
packages/l2-p08/src/middlewares/logger.js
packages/l2-p08/src/middlewares/notFound.js
packages/l2-p08/src/routes/health.routes.js
packages/l2-p08/src/server.js
packages/l2-p08/tests/config.json
packages/l2-p08/tests/jest/http-smoke.jest.test.cjs
packages/l2-p08/tests/jest/patterns.jest.test.cjs
packages/l2-p08/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p08/tests/vitest/patterns.vitest.test.ts
packages/l2-p08/vitest.config.ts
packages/l2-p09/README.md
packages/l2-p09/jest.config.cjs
packages/l2-p09/package.json
packages/l2-p09/src/app.js
packages/l2-p09/src/errors/problem.js
packages/l2-p09/src/middlewares/correlationId.js
packages/l2-p09/src/middlewares/errors.js
packages/l2-p09/src/middlewares/logger.js
packages/l2-p09/src/middlewares/notFound.js
packages/l2-p09/src/routes/health.routes.js
packages/l2-p09/src/server.js
packages/l2-p09/tests/config.json
packages/l2-p09/tests/jest/http-smoke.jest.test.cjs
packages/l2-p09/tests/jest/patterns.jest.test.cjs
packages/l2-p09/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p09/tests/vitest/patterns.vitest.test.ts
packages/l2-p09/vitest.config.ts
packages/l2-p10/README.md
packages/l2-p10/jest.config.cjs
packages/l2-p10/package.json
packages/l2-p10/src/app.js
packages/l2-p10/src/errors/problem.js
packages/l2-p10/src/middlewares/correlationId.js
packages/l2-p10/src/middlewares/errors.js
packages/l2-p10/src/middlewares/logger.js
packages/l2-p10/src/middlewares/notFound.js
packages/l2-p10/src/routes/health.routes.js
packages/l2-p10/src/server.js
packages/l2-p10/tests/config.json
packages/l2-p10/tests/jest/http-smoke.jest.test.cjs
packages/l2-p10/tests/jest/patterns.jest.test.cjs
packages/l2-p10/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p10/tests/vitest/patterns.vitest.test.ts
packages/l2-p10/vitest.config.ts
packages/l2-p11/README.md
packages/l2-p11/jest.config.cjs
packages/l2-p11/package.json
packages/l2-p11/src/app.js
packages/l2-p11/src/errors/problem.js
packages/l2-p11/src/middlewares/correlationId.js
packages/l2-p11/src/middlewares/errors.js
packages/l2-p11/src/middlewares/logger.js
packages/l2-p11/src/middlewares/notFound.js
packages/l2-p11/src/routes/health.routes.js
packages/l2-p11/src/server.js
packages/l2-p11/tests/config.json
packages/l2-p11/tests/jest/http-smoke.jest.test.cjs
packages/l2-p11/tests/jest/patterns.jest.test.cjs
packages/l2-p11/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p11/tests/vitest/patterns.vitest.test.ts
packages/l2-p11/vitest.config.ts
packages/l2-p12/README.md
packages/l2-p12/jest.config.cjs
packages/l2-p12/package.json
packages/l2-p12/src/app.js
packages/l2-p12/src/errors/problem.js
packages/l2-p12/src/middlewares/correlationId.js
packages/l2-p12/src/middlewares/errors.js
packages/l2-p12/src/middlewares/logger.js
packages/l2-p12/src/middlewares/notFound.js
packages/l2-p12/src/routes/health.routes.js
packages/l2-p12/src/server.js
packages/l2-p12/tests/config.json
packages/l2-p12/tests/jest/http-smoke.jest.test.cjs
packages/l2-p12/tests/jest/patterns.jest.test.cjs
packages/l2-p12/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p12/tests/vitest/patterns.vitest.test.ts
packages/l2-p12/vitest.config.ts
packages/l2-p13/README.md
packages/l2-p13/jest.config.cjs
packages/l2-p13/package.json
packages/l2-p13/src/app.js
packages/l2-p13/src/errors/problem.js
packages/l2-p13/src/middlewares/correlationId.js
packages/l2-p13/src/middlewares/errors.js
packages/l2-p13/src/middlewares/logger.js
packages/l2-p13/src/middlewares/notFound.js
packages/l2-p13/src/routes/health.routes.js
packages/l2-p13/src/server.js
packages/l2-p13/tests/config.json
packages/l2-p13/tests/jest/http-smoke.jest.test.cjs
packages/l2-p13/tests/jest/patterns.jest.test.cjs
packages/l2-p13/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p13/tests/vitest/patterns.vitest.test.ts
packages/l2-p13/vitest.config.ts
packages/l2-p14/README.md
packages/l2-p14/jest.config.cjs
packages/l2-p14/package.json
packages/l2-p14/src/app.js
packages/l2-p14/src/errors/problem.js
packages/l2-p14/src/middlewares/correlationId.js
packages/l2-p14/src/middlewares/errors.js
packages/l2-p14/src/middlewares/logger.js
packages/l2-p14/src/middlewares/notFound.js
packages/l2-p14/src/routes/health.routes.js
packages/l2-p14/src/server.js
packages/l2-p14/tests/config.json
packages/l2-p14/tests/jest/http-smoke.jest.test.cjs
packages/l2-p14/tests/jest/patterns.jest.test.cjs
packages/l2-p14/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p14/tests/vitest/patterns.vitest.test.ts
packages/l2-p14/vitest.config.ts
packages/l2-p15/README.md
packages/l2-p15/jest.config.cjs
packages/l2-p15/package.json
packages/l2-p15/src/app.js
packages/l2-p15/src/errors/problem.js
packages/l2-p15/src/middlewares/correlationId.js
packages/l2-p15/src/middlewares/errors.js
packages/l2-p15/src/middlewares/logger.js
packages/l2-p15/src/middlewares/notFound.js
packages/l2-p15/src/routes/health.routes.js
packages/l2-p15/src/server.js
packages/l2-p15/tests/config.json
packages/l2-p15/tests/jest/http-smoke.jest.test.cjs
packages/l2-p15/tests/jest/patterns.jest.test.cjs
packages/l2-p15/tests/vitest/http-smoke.vitest.test.ts
packages/l2-p15/tests/vitest/patterns.vitest.test.ts
packages/l2-p15/vitest.config.ts
packages/l3-p01/README.md
packages/l3-p01/jest.config.cjs
packages/l3-p01/package.json
packages/l3-p01/src/app.js
packages/l3-p01/src/errors/problem.js
packages/l3-p01/src/middlewares/correlationId.js
packages/l3-p01/src/middlewares/errors.js
packages/l3-p01/src/middlewares/logger.js
packages/l3-p01/src/middlewares/notFound.js
packages/l3-p01/src/routes/health.routes.js
packages/l3-p01/src/server.js
packages/l3-p01/tests/config.json
packages/l3-p01/tests/jest/http-smoke.jest.test.cjs
packages/l3-p01/tests/jest/patterns.jest.test.cjs
packages/l3-p01/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p01/tests/vitest/patterns.vitest.test.ts
packages/l3-p01/vitest.config.ts
packages/l3-p02/README.md
packages/l3-p02/jest.config.cjs
packages/l3-p02/package.json
packages/l3-p02/src/app.js
packages/l3-p02/src/errors/problem.js
packages/l3-p02/src/middlewares/correlationId.js
packages/l3-p02/src/middlewares/errors.js
packages/l3-p02/src/middlewares/logger.js
packages/l3-p02/src/middlewares/notFound.js
packages/l3-p02/src/routes/health.routes.js
packages/l3-p02/src/server.js
packages/l3-p02/tests/config.json
packages/l3-p02/tests/jest/http-smoke.jest.test.cjs
packages/l3-p02/tests/jest/patterns.jest.test.cjs
packages/l3-p02/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p02/tests/vitest/patterns.vitest.test.ts
packages/l3-p02/vitest.config.ts
packages/l3-p03/README.md
packages/l3-p03/jest.config.cjs
packages/l3-p03/package.json
packages/l3-p03/src/app.js
packages/l3-p03/src/errors/problem.js
packages/l3-p03/src/middlewares/correlationId.js
packages/l3-p03/src/middlewares/errors.js
packages/l3-p03/src/middlewares/logger.js
packages/l3-p03/src/middlewares/notFound.js
packages/l3-p03/src/routes/health.routes.js
packages/l3-p03/src/server.js
packages/l3-p03/tests/config.json
packages/l3-p03/tests/jest/http-smoke.jest.test.cjs
packages/l3-p03/tests/jest/patterns.jest.test.cjs
packages/l3-p03/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p03/tests/vitest/patterns.vitest.test.ts
packages/l3-p03/vitest.config.ts
packages/l3-p04/README.md
packages/l3-p04/jest.config.cjs
packages/l3-p04/package.json
packages/l3-p04/src/app.js
packages/l3-p04/src/errors/problem.js
packages/l3-p04/src/middlewares/correlationId.js
packages/l3-p04/src/middlewares/errors.js
packages/l3-p04/src/middlewares/logger.js
packages/l3-p04/src/middlewares/notFound.js
packages/l3-p04/src/routes/health.routes.js
packages/l3-p04/src/server.js
packages/l3-p04/tests/config.json
packages/l3-p04/tests/jest/http-smoke.jest.test.cjs
packages/l3-p04/tests/jest/patterns.jest.test.cjs
packages/l3-p04/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p04/tests/vitest/patterns.vitest.test.ts
packages/l3-p04/vitest.config.ts
packages/l3-p05/README.md
packages/l3-p05/jest.config.cjs
packages/l3-p05/package.json
packages/l3-p05/src/app.js
packages/l3-p05/src/errors/problem.js
packages/l3-p05/src/middlewares/correlationId.js
packages/l3-p05/src/middlewares/errors.js
packages/l3-p05/src/middlewares/logger.js
packages/l3-p05/src/middlewares/notFound.js
packages/l3-p05/src/routes/health.routes.js
packages/l3-p05/src/server.js
packages/l3-p05/tests/config.json
packages/l3-p05/tests/jest/http-smoke.jest.test.cjs
packages/l3-p05/tests/jest/patterns.jest.test.cjs
packages/l3-p05/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p05/tests/vitest/patterns.vitest.test.ts
packages/l3-p05/vitest.config.ts
packages/l3-p06/README.md
packages/l3-p06/jest.config.cjs
packages/l3-p06/package.json
packages/l3-p06/src/app.js
packages/l3-p06/src/errors/problem.js
packages/l3-p06/src/middlewares/correlationId.js
packages/l3-p06/src/middlewares/errors.js
packages/l3-p06/src/middlewares/logger.js
packages/l3-p06/src/middlewares/notFound.js
packages/l3-p06/src/routes/health.routes.js
packages/l3-p06/src/server.js
packages/l3-p06/tests/config.json
packages/l3-p06/tests/jest/http-smoke.jest.test.cjs
packages/l3-p06/tests/jest/patterns.jest.test.cjs
packages/l3-p06/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p06/tests/vitest/patterns.vitest.test.ts
packages/l3-p06/vitest.config.ts
packages/l3-p07/README.md
packages/l3-p07/jest.config.cjs
packages/l3-p07/package.json
packages/l3-p07/src/app.js
packages/l3-p07/src/errors/problem.js
packages/l3-p07/src/middlewares/correlationId.js
packages/l3-p07/src/middlewares/errors.js
packages/l3-p07/src/middlewares/logger.js
packages/l3-p07/src/middlewares/notFound.js
packages/l3-p07/src/routes/health.routes.js
packages/l3-p07/src/server.js
packages/l3-p07/tests/config.json
packages/l3-p07/tests/jest/http-smoke.jest.test.cjs
packages/l3-p07/tests/jest/patterns.jest.test.cjs
packages/l3-p07/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p07/tests/vitest/patterns.vitest.test.ts
packages/l3-p07/vitest.config.ts
packages/l3-p08/README.md
packages/l3-p08/jest.config.cjs
packages/l3-p08/package.json
packages/l3-p08/src/app.js
packages/l3-p08/src/errors/problem.js
packages/l3-p08/src/middlewares/correlationId.js
packages/l3-p08/src/middlewares/errors.js
packages/l3-p08/src/middlewares/logger.js
packages/l3-p08/src/middlewares/notFound.js
packages/l3-p08/src/routes/health.routes.js
packages/l3-p08/src/server.js
packages/l3-p08/tests/config.json
packages/l3-p08/tests/jest/http-smoke.jest.test.cjs
packages/l3-p08/tests/jest/patterns.jest.test.cjs
packages/l3-p08/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p08/tests/vitest/patterns.vitest.test.ts
packages/l3-p08/vitest.config.ts
packages/l3-p09/README.md
packages/l3-p09/jest.config.cjs
packages/l3-p09/package.json
packages/l3-p09/src/app.js
packages/l3-p09/src/errors/problem.js
packages/l3-p09/src/middlewares/correlationId.js
packages/l3-p09/src/middlewares/errors.js
packages/l3-p09/src/middlewares/logger.js
packages/l3-p09/src/middlewares/notFound.js
packages/l3-p09/src/routes/health.routes.js
packages/l3-p09/src/server.js
packages/l3-p09/tests/config.json
packages/l3-p09/tests/jest/http-smoke.jest.test.cjs
packages/l3-p09/tests/jest/patterns.jest.test.cjs
packages/l3-p09/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p09/tests/vitest/patterns.vitest.test.ts
packages/l3-p09/vitest.config.ts
packages/l3-p10/README.md
packages/l3-p10/jest.config.cjs
packages/l3-p10/package.json
packages/l3-p10/src/app.js
packages/l3-p10/src/errors/problem.js
packages/l3-p10/src/middlewares/correlationId.js
packages/l3-p10/src/middlewares/errors.js
packages/l3-p10/src/middlewares/logger.js
packages/l3-p10/src/middlewares/notFound.js
packages/l3-p10/src/routes/health.routes.js
packages/l3-p10/src/server.js
packages/l3-p10/tests/config.json
packages/l3-p10/tests/jest/http-smoke.jest.test.cjs
packages/l3-p10/tests/jest/patterns.jest.test.cjs
packages/l3-p10/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p10/tests/vitest/patterns.vitest.test.ts
packages/l3-p10/vitest.config.ts
packages/l3-p11/README.md
packages/l3-p11/jest.config.cjs
packages/l3-p11/package.json
packages/l3-p11/src/app.js
packages/l3-p11/src/errors/problem.js
packages/l3-p11/src/middlewares/correlationId.js
packages/l3-p11/src/middlewares/errors.js
packages/l3-p11/src/middlewares/logger.js
packages/l3-p11/src/middlewares/notFound.js
packages/l3-p11/src/routes/health.routes.js
packages/l3-p11/src/server.js
packages/l3-p11/tests/config.json
packages/l3-p11/tests/jest/http-smoke.jest.test.cjs
packages/l3-p11/tests/jest/patterns.jest.test.cjs
packages/l3-p11/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p11/tests/vitest/patterns.vitest.test.ts
packages/l3-p11/vitest.config.ts
packages/l3-p12/README.md
packages/l3-p12/jest.config.cjs
packages/l3-p12/package.json
packages/l3-p12/src/app.js
packages/l3-p12/src/errors/problem.js
packages/l3-p12/src/middlewares/correlationId.js
packages/l3-p12/src/middlewares/errors.js
packages/l3-p12/src/middlewares/logger.js
packages/l3-p12/src/middlewares/notFound.js
packages/l3-p12/src/routes/health.routes.js
packages/l3-p12/src/server.js
packages/l3-p12/tests/config.json
packages/l3-p12/tests/jest/http-smoke.jest.test.cjs
packages/l3-p12/tests/jest/patterns.jest.test.cjs
packages/l3-p12/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p12/tests/vitest/patterns.vitest.test.ts
packages/l3-p12/vitest.config.ts
packages/l3-p13/README.md
packages/l3-p13/jest.config.cjs
packages/l3-p13/package.json
packages/l3-p13/src/app.js
packages/l3-p13/src/errors/problem.js
packages/l3-p13/src/middlewares/correlationId.js
packages/l3-p13/src/middlewares/errors.js
packages/l3-p13/src/middlewares/logger.js
packages/l3-p13/src/middlewares/notFound.js
packages/l3-p13/src/routes/health.routes.js
packages/l3-p13/src/server.js
packages/l3-p13/tests/config.json
packages/l3-p13/tests/jest/http-smoke.jest.test.cjs
packages/l3-p13/tests/jest/patterns.jest.test.cjs
packages/l3-p13/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p13/tests/vitest/patterns.vitest.test.ts
packages/l3-p13/vitest.config.ts
packages/l3-p14/README.md
packages/l3-p14/jest.config.cjs
packages/l3-p14/package.json
packages/l3-p14/src/app.js
packages/l3-p14/src/errors/problem.js
packages/l3-p14/src/middlewares/correlationId.js
packages/l3-p14/src/middlewares/errors.js
packages/l3-p14/src/middlewares/logger.js
packages/l3-p14/src/middlewares/notFound.js
packages/l3-p14/src/routes/health.routes.js
packages/l3-p14/src/server.js
packages/l3-p14/tests/config.json
packages/l3-p14/tests/jest/http-smoke.jest.test.cjs
packages/l3-p14/tests/jest/patterns.jest.test.cjs
packages/l3-p14/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p14/tests/vitest/patterns.vitest.test.ts
packages/l3-p14/vitest.config.ts
packages/l3-p15/README.md
packages/l3-p15/jest.config.cjs
packages/l3-p15/package.json
packages/l3-p15/src/app.js
packages/l3-p15/src/errors/problem.js
packages/l3-p15/src/middlewares/correlationId.js
packages/l3-p15/src/middlewares/errors.js
packages/l3-p15/src/middlewares/logger.js
packages/l3-p15/src/middlewares/notFound.js
packages/l3-p15/src/routes/health.routes.js
packages/l3-p15/src/server.js
packages/l3-p15/tests/config.json
packages/l3-p15/tests/jest/http-smoke.jest.test.cjs
packages/l3-p15/tests/jest/patterns.jest.test.cjs
packages/l3-p15/tests/vitest/http-smoke.vitest.test.ts
packages/l3-p15/tests/vitest/patterns.vitest.test.ts
packages/l3-p15/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 137, docs: 45, code: 360, tests: 225.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s8p3-monorepo` type=`commonjs` workspaces=True
  - **Scripturi:**
  - `test:vitest` → `pnpm -r --filter ./packages run test:vitest`
  - `test:jest` → `pnpm -r --filter ./packages run test:jest`
  - `test` → `pnpm -r --filter ./packages run test`
  - **Deps:** 
  - **DevDeps:** pnpm, vitest, jest, supertest, nodemon, cors, express
- `packages/l1-p01/package.json`: name=`l1-p01` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p02/package.json`: name=`l1-p02` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p03/package.json`: name=`l1-p03` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p04/package.json`: name=`l1-p04` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p05/package.json`: name=`l1-p05` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p06/package.json`: name=`l1-p06` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p07/package.json`: name=`l1-p07` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p08/package.json`: name=`l1-p08` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p09/package.json`: name=`l1-p09` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p10/package.json`: name=`l1-p10` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p11/package.json`: name=`l1-p11` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p12/package.json`: name=`l1-p12` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p13/package.json`: name=`l1-p13` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p14/package.json`: name=`l1-p14` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l1-p15/package.json`: name=`l1-p15` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p01/package.json`: name=`l2-p01` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p02/package.json`: name=`l2-p02` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p03/package.json`: name=`l2-p03` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p04/package.json`: name=`l2-p04` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p05/package.json`: name=`l2-p05` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p06/package.json`: name=`l2-p06` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p07/package.json`: name=`l2-p07` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p08/package.json`: name=`l2-p08` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p09/package.json`: name=`l2-p09` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p10/package.json`: name=`l2-p10` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p11/package.json`: name=`l2-p11` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p12/package.json`: name=`l2-p12` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p13/package.json`: name=`l2-p13` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p14/package.json`: name=`l2-p14` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l2-p15/package.json`: name=`l2-p15` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p01/package.json`: name=`l3-p01` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p02/package.json`: name=`l3-p02` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p03/package.json`: name=`l3-p03` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p04/package.json`: name=`l3-p04` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p05/package.json`: name=`l3-p05` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p06/package.json`: name=`l3-p06` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p07/package.json`: name=`l3-p07` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p08/package.json`: name=`l3-p08` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p09/package.json`: name=`l3-p09` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p10/package.json`: name=`l3-p10` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p11/package.json`: name=`l3-p11` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p12/package.json`: name=`l3-p12` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p13/package.json`: name=`l3-p13` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p14/package.json`: name=`l3-p14` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `packages/l3-p15/package.json`: name=`l3-p15` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest

### Seminar8_Partea3_p3-standalone.zip

```
l1-p01/README.md
l1-p01/jest.config.cjs
l1-p01/package.json
l1-p01/src/app.js
l1-p01/src/errors/problem.js
l1-p01/src/middlewares/correlationId.js
l1-p01/src/middlewares/errors.js
l1-p01/src/middlewares/logger.js
l1-p01/src/middlewares/notFound.js
l1-p01/src/routes/health.routes.js
l1-p01/src/server.js
l1-p01/tests/config.json
l1-p01/tests/jest/http-smoke.jest.test.cjs
l1-p01/tests/jest/patterns.jest.test.cjs
l1-p01/tests/vitest/http-smoke.vitest.test.ts
l1-p01/tests/vitest/patterns.vitest.test.ts
l1-p01/vitest.config.ts
l1-p02/README.md
l1-p02/jest.config.cjs
l1-p02/package.json
l1-p02/src/app.js
l1-p02/src/errors/problem.js
l1-p02/src/middlewares/correlationId.js
l1-p02/src/middlewares/errors.js
l1-p02/src/middlewares/logger.js
l1-p02/src/middlewares/notFound.js
l1-p02/src/routes/health.routes.js
l1-p02/src/server.js
l1-p02/tests/config.json
l1-p02/tests/jest/http-smoke.jest.test.cjs
l1-p02/tests/jest/patterns.jest.test.cjs
l1-p02/tests/vitest/http-smoke.vitest.test.ts
l1-p02/tests/vitest/patterns.vitest.test.ts
l1-p02/vitest.config.ts
l1-p03/README.md
l1-p03/jest.config.cjs
l1-p03/package.json
l1-p03/src/app.js
l1-p03/src/errors/problem.js
l1-p03/src/middlewares/correlationId.js
l1-p03/src/middlewares/errors.js
l1-p03/src/middlewares/logger.js
l1-p03/src/middlewares/notFound.js
l1-p03/src/routes/health.routes.js
l1-p03/src/server.js
l1-p03/tests/config.json
l1-p03/tests/jest/http-smoke.jest.test.cjs
l1-p03/tests/jest/patterns.jest.test.cjs
l1-p03/tests/vitest/http-smoke.vitest.test.ts
l1-p03/tests/vitest/patterns.vitest.test.ts
l1-p03/vitest.config.ts
l1-p04/README.md
l1-p04/jest.config.cjs
l1-p04/package.json
l1-p04/src/app.js
l1-p04/src/errors/problem.js
l1-p04/src/middlewares/correlationId.js
l1-p04/src/middlewares/errors.js
l1-p04/src/middlewares/logger.js
l1-p04/src/middlewares/notFound.js
l1-p04/src/routes/health.routes.js
l1-p04/src/server.js
l1-p04/tests/config.json
l1-p04/tests/jest/http-smoke.jest.test.cjs
l1-p04/tests/jest/patterns.jest.test.cjs
l1-p04/tests/vitest/http-smoke.vitest.test.ts
l1-p04/tests/vitest/patterns.vitest.test.ts
l1-p04/vitest.config.ts
l1-p05/README.md
l1-p05/jest.config.cjs
l1-p05/package.json
l1-p05/src/app.js
l1-p05/src/errors/problem.js
l1-p05/src/middlewares/correlationId.js
l1-p05/src/middlewares/errors.js
l1-p05/src/middlewares/logger.js
l1-p05/src/middlewares/notFound.js
l1-p05/src/routes/health.routes.js
l1-p05/src/server.js
l1-p05/tests/config.json
l1-p05/tests/jest/http-smoke.jest.test.cjs
l1-p05/tests/jest/patterns.jest.test.cjs
l1-p05/tests/vitest/http-smoke.vitest.test.ts
l1-p05/tests/vitest/patterns.vitest.test.ts
l1-p05/vitest.config.ts
l1-p06/README.md
l1-p06/jest.config.cjs
l1-p06/package.json
l1-p06/src/app.js
l1-p06/src/errors/problem.js
l1-p06/src/middlewares/correlationId.js
l1-p06/src/middlewares/errors.js
l1-p06/src/middlewares/logger.js
l1-p06/src/middlewares/notFound.js
l1-p06/src/routes/health.routes.js
l1-p06/src/server.js
l1-p06/tests/config.json
l1-p06/tests/jest/http-smoke.jest.test.cjs
l1-p06/tests/jest/patterns.jest.test.cjs
l1-p06/tests/vitest/http-smoke.vitest.test.ts
l1-p06/tests/vitest/patterns.vitest.test.ts
l1-p06/vitest.config.ts
l1-p07/README.md
l1-p07/jest.config.cjs
l1-p07/package.json
l1-p07/src/app.js
l1-p07/src/errors/problem.js
l1-p07/src/middlewares/correlationId.js
l1-p07/src/middlewares/errors.js
l1-p07/src/middlewares/logger.js
l1-p07/src/middlewares/notFound.js
l1-p07/src/routes/health.routes.js
l1-p07/src/server.js
l1-p07/tests/config.json
l1-p07/tests/jest/http-smoke.jest.test.cjs
l1-p07/tests/jest/patterns.jest.test.cjs
l1-p07/tests/vitest/http-smoke.vitest.test.ts
l1-p07/tests/vitest/patterns.vitest.test.ts
l1-p07/vitest.config.ts
l1-p08/README.md
l1-p08/jest.config.cjs
l1-p08/package.json
l1-p08/src/app.js
l1-p08/src/errors/problem.js
l1-p08/src/middlewares/correlationId.js
l1-p08/src/middlewares/errors.js
l1-p08/src/middlewares/logger.js
l1-p08/src/middlewares/notFound.js
l1-p08/src/routes/health.routes.js
l1-p08/src/server.js
l1-p08/tests/config.json
l1-p08/tests/jest/http-smoke.jest.test.cjs
l1-p08/tests/jest/patterns.jest.test.cjs
l1-p08/tests/vitest/http-smoke.vitest.test.ts
l1-p08/tests/vitest/patterns.vitest.test.ts
l1-p08/vitest.config.ts
l1-p09/README.md
l1-p09/jest.config.cjs
l1-p09/package.json
l1-p09/src/app.js
l1-p09/src/errors/problem.js
l1-p09/src/middlewares/correlationId.js
l1-p09/src/middlewares/errors.js
l1-p09/src/middlewares/logger.js
l1-p09/src/middlewares/notFound.js
l1-p09/src/routes/health.routes.js
l1-p09/src/server.js
l1-p09/tests/config.json
l1-p09/tests/jest/http-smoke.jest.test.cjs
l1-p09/tests/jest/patterns.jest.test.cjs
l1-p09/tests/vitest/http-smoke.vitest.test.ts
l1-p09/tests/vitest/patterns.vitest.test.ts
l1-p09/vitest.config.ts
l1-p10/README.md
l1-p10/jest.config.cjs
l1-p10/package.json
l1-p10/src/app.js
l1-p10/src/errors/problem.js
l1-p10/src/middlewares/correlationId.js
l1-p10/src/middlewares/errors.js
l1-p10/src/middlewares/logger.js
l1-p10/src/middlewares/notFound.js
l1-p10/src/routes/health.routes.js
l1-p10/src/server.js
l1-p10/tests/config.json
l1-p10/tests/jest/http-smoke.jest.test.cjs
l1-p10/tests/jest/patterns.jest.test.cjs
l1-p10/tests/vitest/http-smoke.vitest.test.ts
l1-p10/tests/vitest/patterns.vitest.test.ts
l1-p10/vitest.config.ts
l1-p11/README.md
l1-p11/jest.config.cjs
l1-p11/package.json
l1-p11/src/app.js
l1-p11/src/errors/problem.js
l1-p11/src/middlewares/correlationId.js
l1-p11/src/middlewares/errors.js
l1-p11/src/middlewares/logger.js
l1-p11/src/middlewares/notFound.js
l1-p11/src/routes/health.routes.js
l1-p11/src/server.js
l1-p11/tests/config.json
l1-p11/tests/jest/http-smoke.jest.test.cjs
l1-p11/tests/jest/patterns.jest.test.cjs
l1-p11/tests/vitest/http-smoke.vitest.test.ts
l1-p11/tests/vitest/patterns.vitest.test.ts
l1-p11/vitest.config.ts
l1-p12/README.md
l1-p12/jest.config.cjs
l1-p12/package.json
l1-p12/src/app.js
l1-p12/src/errors/problem.js
l1-p12/src/middlewares/correlationId.js
l1-p12/src/middlewares/errors.js
l1-p12/src/middlewares/logger.js
l1-p12/src/middlewares/notFound.js
l1-p12/src/routes/health.routes.js
l1-p12/src/server.js
l1-p12/tests/config.json
l1-p12/tests/jest/http-smoke.jest.test.cjs
l1-p12/tests/jest/patterns.jest.test.cjs
l1-p12/tests/vitest/http-smoke.vitest.test.ts
l1-p12/tests/vitest/patterns.vitest.test.ts
l1-p12/vitest.config.ts
l1-p13/README.md
l1-p13/jest.config.cjs
l1-p13/package.json
l1-p13/src/app.js
l1-p13/src/errors/problem.js
l1-p13/src/middlewares/correlationId.js
l1-p13/src/middlewares/errors.js
l1-p13/src/middlewares/logger.js
l1-p13/src/middlewares/notFound.js
l1-p13/src/routes/health.routes.js
l1-p13/src/server.js
l1-p13/tests/config.json
l1-p13/tests/jest/http-smoke.jest.test.cjs
l1-p13/tests/jest/patterns.jest.test.cjs
l1-p13/tests/vitest/http-smoke.vitest.test.ts
l1-p13/tests/vitest/patterns.vitest.test.ts
l1-p13/vitest.config.ts
l1-p14/README.md
l1-p14/jest.config.cjs
l1-p14/package.json
l1-p14/src/app.js
l1-p14/src/errors/problem.js
l1-p14/src/middlewares/correlationId.js
l1-p14/src/middlewares/errors.js
l1-p14/src/middlewares/logger.js
l1-p14/src/middlewares/notFound.js
l1-p14/src/routes/health.routes.js
l1-p14/src/server.js
l1-p14/tests/config.json
l1-p14/tests/jest/http-smoke.jest.test.cjs
l1-p14/tests/jest/patterns.jest.test.cjs
l1-p14/tests/vitest/http-smoke.vitest.test.ts
l1-p14/tests/vitest/patterns.vitest.test.ts
l1-p14/vitest.config.ts
l1-p15/README.md
l1-p15/jest.config.cjs
l1-p15/package.json
l1-p15/src/app.js
l1-p15/src/errors/problem.js
l1-p15/src/middlewares/correlationId.js
l1-p15/src/middlewares/errors.js
l1-p15/src/middlewares/logger.js
l1-p15/src/middlewares/notFound.js
l1-p15/src/routes/health.routes.js
l1-p15/src/server.js
l1-p15/tests/config.json
l1-p15/tests/jest/http-smoke.jest.test.cjs
l1-p15/tests/jest/patterns.jest.test.cjs
l1-p15/tests/vitest/http-smoke.vitest.test.ts
l1-p15/tests/vitest/patterns.vitest.test.ts
l1-p15/vitest.config.ts
l2-p01/README.md
l2-p01/jest.config.cjs
l2-p01/package.json
l2-p01/src/app.js
l2-p01/src/errors/problem.js
l2-p01/src/middlewares/correlationId.js
l2-p01/src/middlewares/errors.js
l2-p01/src/middlewares/logger.js
l2-p01/src/middlewares/notFound.js
l2-p01/src/routes/health.routes.js
l2-p01/src/server.js
l2-p01/tests/config.json
l2-p01/tests/jest/http-smoke.jest.test.cjs
l2-p01/tests/jest/patterns.jest.test.cjs
l2-p01/tests/vitest/http-smoke.vitest.test.ts
l2-p01/tests/vitest/patterns.vitest.test.ts
l2-p01/vitest.config.ts
l2-p02/README.md
l2-p02/jest.config.cjs
l2-p02/package.json
l2-p02/src/app.js
l2-p02/src/errors/problem.js
l2-p02/src/middlewares/correlationId.js
l2-p02/src/middlewares/errors.js
l2-p02/src/middlewares/logger.js
l2-p02/src/middlewares/notFound.js
l2-p02/src/routes/health.routes.js
l2-p02/src/server.js
l2-p02/tests/config.json
l2-p02/tests/jest/http-smoke.jest.test.cjs
l2-p02/tests/jest/patterns.jest.test.cjs
l2-p02/tests/vitest/http-smoke.vitest.test.ts
l2-p02/tests/vitest/patterns.vitest.test.ts
l2-p02/vitest.config.ts
l2-p03/README.md
l2-p03/jest.config.cjs
l2-p03/package.json
l2-p03/src/app.js
l2-p03/src/errors/problem.js
l2-p03/src/middlewares/correlationId.js
l2-p03/src/middlewares/errors.js
l2-p03/src/middlewares/logger.js
l2-p03/src/middlewares/notFound.js
l2-p03/src/routes/health.routes.js
l2-p03/src/server.js
l2-p03/tests/config.json
l2-p03/tests/jest/http-smoke.jest.test.cjs
l2-p03/tests/jest/patterns.jest.test.cjs
l2-p03/tests/vitest/http-smoke.vitest.test.ts
l2-p03/tests/vitest/patterns.vitest.test.ts
l2-p03/vitest.config.ts
l2-p04/README.md
l2-p04/jest.config.cjs
l2-p04/package.json
l2-p04/src/app.js
l2-p04/src/errors/problem.js
l2-p04/src/middlewares/correlationId.js
l2-p04/src/middlewares/errors.js
l2-p04/src/middlewares/logger.js
l2-p04/src/middlewares/notFound.js
l2-p04/src/routes/health.routes.js
l2-p04/src/server.js
l2-p04/tests/config.json
l2-p04/tests/jest/http-smoke.jest.test.cjs
l2-p04/tests/jest/patterns.jest.test.cjs
l2-p04/tests/vitest/http-smoke.vitest.test.ts
l2-p04/tests/vitest/patterns.vitest.test.ts
l2-p04/vitest.config.ts
l2-p05/README.md
l2-p05/jest.config.cjs
l2-p05/package.json
l2-p05/src/app.js
l2-p05/src/errors/problem.js
l2-p05/src/middlewares/correlationId.js
l2-p05/src/middlewares/errors.js
l2-p05/src/middlewares/logger.js
l2-p05/src/middlewares/notFound.js
l2-p05/src/routes/health.routes.js
l2-p05/src/server.js
l2-p05/tests/config.json
l2-p05/tests/jest/http-smoke.jest.test.cjs
l2-p05/tests/jest/patterns.jest.test.cjs
l2-p05/tests/vitest/http-smoke.vitest.test.ts
l2-p05/tests/vitest/patterns.vitest.test.ts
l2-p05/vitest.config.ts
l2-p06/README.md
l2-p06/jest.config.cjs
l2-p06/package.json
l2-p06/src/app.js
l2-p06/src/errors/problem.js
l2-p06/src/middlewares/correlationId.js
l2-p06/src/middlewares/errors.js
l2-p06/src/middlewares/logger.js
l2-p06/src/middlewares/notFound.js
l2-p06/src/routes/health.routes.js
l2-p06/src/server.js
l2-p06/tests/config.json
l2-p06/tests/jest/http-smoke.jest.test.cjs
l2-p06/tests/jest/patterns.jest.test.cjs
l2-p06/tests/vitest/http-smoke.vitest.test.ts
l2-p06/tests/vitest/patterns.vitest.test.ts
l2-p06/vitest.config.ts
l2-p07/README.md
l2-p07/jest.config.cjs
l2-p07/package.json
l2-p07/src/app.js
l2-p07/src/errors/problem.js
l2-p07/src/middlewares/correlationId.js
l2-p07/src/middlewares/errors.js
l2-p07/src/middlewares/logger.js
l2-p07/src/middlewares/notFound.js
l2-p07/src/routes/health.routes.js
l2-p07/src/server.js
l2-p07/tests/config.json
l2-p07/tests/jest/http-smoke.jest.test.cjs
l2-p07/tests/jest/patterns.jest.test.cjs
l2-p07/tests/vitest/http-smoke.vitest.test.ts
l2-p07/tests/vitest/patterns.vitest.test.ts
l2-p07/vitest.config.ts
l2-p08/README.md
l2-p08/jest.config.cjs
l2-p08/package.json
l2-p08/src/app.js
l2-p08/src/errors/problem.js
l2-p08/src/middlewares/correlationId.js
l2-p08/src/middlewares/errors.js
l2-p08/src/middlewares/logger.js
l2-p08/src/middlewares/notFound.js
l2-p08/src/routes/health.routes.js
l2-p08/src/server.js
l2-p08/tests/config.json
l2-p08/tests/jest/http-smoke.jest.test.cjs
l2-p08/tests/jest/patterns.jest.test.cjs
l2-p08/tests/vitest/http-smoke.vitest.test.ts
l2-p08/tests/vitest/patterns.vitest.test.ts
l2-p08/vitest.config.ts
l2-p09/README.md
l2-p09/jest.config.cjs
l2-p09/package.json
l2-p09/src/app.js
l2-p09/src/errors/problem.js
l2-p09/src/middlewares/correlationId.js
l2-p09/src/middlewares/errors.js
l2-p09/src/middlewares/logger.js
l2-p09/src/middlewares/notFound.js
l2-p09/src/routes/health.routes.js
l2-p09/src/server.js
l2-p09/tests/config.json
l2-p09/tests/jest/http-smoke.jest.test.cjs
l2-p09/tests/jest/patterns.jest.test.cjs
l2-p09/tests/vitest/http-smoke.vitest.test.ts
l2-p09/tests/vitest/patterns.vitest.test.ts
l2-p09/vitest.config.ts
l2-p10/README.md
l2-p10/jest.config.cjs
l2-p10/package.json
l2-p10/src/app.js
l2-p10/src/errors/problem.js
l2-p10/src/middlewares/correlationId.js
l2-p10/src/middlewares/errors.js
l2-p10/src/middlewares/logger.js
l2-p10/src/middlewares/notFound.js
l2-p10/src/routes/health.routes.js
l2-p10/src/server.js
l2-p10/tests/config.json
l2-p10/tests/jest/http-smoke.jest.test.cjs
l2-p10/tests/jest/patterns.jest.test.cjs
l2-p10/tests/vitest/http-smoke.vitest.test.ts
l2-p10/tests/vitest/patterns.vitest.test.ts
l2-p10/vitest.config.ts
l2-p11/README.md
l2-p11/jest.config.cjs
l2-p11/package.json
l2-p11/src/app.js
l2-p11/src/errors/problem.js
l2-p11/src/middlewares/correlationId.js
l2-p11/src/middlewares/errors.js
l2-p11/src/middlewares/logger.js
l2-p11/src/middlewares/notFound.js
l2-p11/src/routes/health.routes.js
l2-p11/src/server.js
l2-p11/tests/config.json
l2-p11/tests/jest/http-smoke.jest.test.cjs
l2-p11/tests/jest/patterns.jest.test.cjs
l2-p11/tests/vitest/http-smoke.vitest.test.ts
l2-p11/tests/vitest/patterns.vitest.test.ts
l2-p11/vitest.config.ts
l2-p12/README.md
l2-p12/jest.config.cjs
l2-p12/package.json
l2-p12/src/app.js
l2-p12/src/errors/problem.js
l2-p12/src/middlewares/correlationId.js
l2-p12/src/middlewares/errors.js
l2-p12/src/middlewares/logger.js
l2-p12/src/middlewares/notFound.js
l2-p12/src/routes/health.routes.js
l2-p12/src/server.js
l2-p12/tests/config.json
l2-p12/tests/jest/http-smoke.jest.test.cjs
l2-p12/tests/jest/patterns.jest.test.cjs
l2-p12/tests/vitest/http-smoke.vitest.test.ts
l2-p12/tests/vitest/patterns.vitest.test.ts
l2-p12/vitest.config.ts
l2-p13/README.md
l2-p13/jest.config.cjs
l2-p13/package.json
l2-p13/src/app.js
l2-p13/src/errors/problem.js
l2-p13/src/middlewares/correlationId.js
l2-p13/src/middlewares/errors.js
l2-p13/src/middlewares/logger.js
l2-p13/src/middlewares/notFound.js
l2-p13/src/routes/health.routes.js
l2-p13/src/server.js
l2-p13/tests/config.json
l2-p13/tests/jest/http-smoke.jest.test.cjs
l2-p13/tests/jest/patterns.jest.test.cjs
l2-p13/tests/vitest/http-smoke.vitest.test.ts
l2-p13/tests/vitest/patterns.vitest.test.ts
l2-p13/vitest.config.ts
l2-p14/README.md
l2-p14/jest.config.cjs
l2-p14/package.json
l2-p14/src/app.js
l2-p14/src/errors/problem.js
l2-p14/src/middlewares/correlationId.js
l2-p14/src/middlewares/errors.js
l2-p14/src/middlewares/logger.js
l2-p14/src/middlewares/notFound.js
l2-p14/src/routes/health.routes.js
l2-p14/src/server.js
l2-p14/tests/config.json
l2-p14/tests/jest/http-smoke.jest.test.cjs
l2-p14/tests/jest/patterns.jest.test.cjs
l2-p14/tests/vitest/http-smoke.vitest.test.ts
l2-p14/tests/vitest/patterns.vitest.test.ts
l2-p14/vitest.config.ts
l2-p15/README.md
l2-p15/jest.config.cjs
l2-p15/package.json
l2-p15/src/app.js
l2-p15/src/errors/problem.js
l2-p15/src/middlewares/correlationId.js
l2-p15/src/middlewares/errors.js
l2-p15/src/middlewares/logger.js
l2-p15/src/middlewares/notFound.js
l2-p15/src/routes/health.routes.js
l2-p15/src/server.js
l2-p15/tests/config.json
l2-p15/tests/jest/http-smoke.jest.test.cjs
l2-p15/tests/jest/patterns.jest.test.cjs
l2-p15/tests/vitest/http-smoke.vitest.test.ts
l2-p15/tests/vitest/patterns.vitest.test.ts
l2-p15/vitest.config.ts
l3-p01/README.md
l3-p01/jest.config.cjs
l3-p01/package.json
l3-p01/src/app.js
l3-p01/src/errors/problem.js
l3-p01/src/middlewares/correlationId.js
l3-p01/src/middlewares/errors.js
l3-p01/src/middlewares/logger.js
l3-p01/src/middlewares/notFound.js
l3-p01/src/routes/health.routes.js
l3-p01/src/server.js
l3-p01/tests/config.json
l3-p01/tests/jest/http-smoke.jest.test.cjs
l3-p01/tests/jest/patterns.jest.test.cjs
l3-p01/tests/vitest/http-smoke.vitest.test.ts
l3-p01/tests/vitest/patterns.vitest.test.ts
l3-p01/vitest.config.ts
l3-p02/README.md
l3-p02/jest.config.cjs
l3-p02/package.json
l3-p02/src/app.js
l3-p02/src/errors/problem.js
l3-p02/src/middlewares/correlationId.js
l3-p02/src/middlewares/errors.js
l3-p02/src/middlewares/logger.js
l3-p02/src/middlewares/notFound.js
l3-p02/src/routes/health.routes.js
l3-p02/src/server.js
l3-p02/tests/config.json
l3-p02/tests/jest/http-smoke.jest.test.cjs
l3-p02/tests/jest/patterns.jest.test.cjs
l3-p02/tests/vitest/http-smoke.vitest.test.ts
l3-p02/tests/vitest/patterns.vitest.test.ts
l3-p02/vitest.config.ts
l3-p03/README.md
l3-p03/jest.config.cjs
l3-p03/package.json
l3-p03/src/app.js
l3-p03/src/errors/problem.js
l3-p03/src/middlewares/correlationId.js
l3-p03/src/middlewares/errors.js
l3-p03/src/middlewares/logger.js
l3-p03/src/middlewares/notFound.js
l3-p03/src/routes/health.routes.js
l3-p03/src/server.js
l3-p03/tests/config.json
l3-p03/tests/jest/http-smoke.jest.test.cjs
l3-p03/tests/jest/patterns.jest.test.cjs
l3-p03/tests/vitest/http-smoke.vitest.test.ts
l3-p03/tests/vitest/patterns.vitest.test.ts
l3-p03/vitest.config.ts
l3-p04/README.md
l3-p04/jest.config.cjs
l3-p04/package.json
l3-p04/src/app.js
l3-p04/src/errors/problem.js
l3-p04/src/middlewares/correlationId.js
l3-p04/src/middlewares/errors.js
l3-p04/src/middlewares/logger.js
l3-p04/src/middlewares/notFound.js
l3-p04/src/routes/health.routes.js
l3-p04/src/server.js
l3-p04/tests/config.json
l3-p04/tests/jest/http-smoke.jest.test.cjs
l3-p04/tests/jest/patterns.jest.test.cjs
l3-p04/tests/vitest/http-smoke.vitest.test.ts
l3-p04/tests/vitest/patterns.vitest.test.ts
l3-p04/vitest.config.ts
l3-p05/README.md
l3-p05/jest.config.cjs
l3-p05/package.json
l3-p05/src/app.js
l3-p05/src/errors/problem.js
l3-p05/src/middlewares/correlationId.js
l3-p05/src/middlewares/errors.js
l3-p05/src/middlewares/logger.js
l3-p05/src/middlewares/notFound.js
l3-p05/src/routes/health.routes.js
l3-p05/src/server.js
l3-p05/tests/config.json
l3-p05/tests/jest/http-smoke.jest.test.cjs
l3-p05/tests/jest/patterns.jest.test.cjs
l3-p05/tests/vitest/http-smoke.vitest.test.ts
l3-p05/tests/vitest/patterns.vitest.test.ts
l3-p05/vitest.config.ts
l3-p06/README.md
l3-p06/jest.config.cjs
l3-p06/package.json
l3-p06/src/app.js
l3-p06/src/errors/problem.js
l3-p06/src/middlewares/correlationId.js
l3-p06/src/middlewares/errors.js
l3-p06/src/middlewares/logger.js
l3-p06/src/middlewares/notFound.js
l3-p06/src/routes/health.routes.js
l3-p06/src/server.js
l3-p06/tests/config.json
l3-p06/tests/jest/http-smoke.jest.test.cjs
l3-p06/tests/jest/patterns.jest.test.cjs
l3-p06/tests/vitest/http-smoke.vitest.test.ts
l3-p06/tests/vitest/patterns.vitest.test.ts
l3-p06/vitest.config.ts
l3-p07/README.md
l3-p07/jest.config.cjs
l3-p07/package.json
l3-p07/src/app.js
l3-p07/src/errors/problem.js
l3-p07/src/middlewares/correlationId.js
l3-p07/src/middlewares/errors.js
l3-p07/src/middlewares/logger.js
l3-p07/src/middlewares/notFound.js
l3-p07/src/routes/health.routes.js
l3-p07/src/server.js
l3-p07/tests/config.json
l3-p07/tests/jest/http-smoke.jest.test.cjs
l3-p07/tests/jest/patterns.jest.test.cjs
l3-p07/tests/vitest/http-smoke.vitest.test.ts
l3-p07/tests/vitest/patterns.vitest.test.ts
l3-p07/vitest.config.ts
l3-p08/README.md
l3-p08/jest.config.cjs
l3-p08/package.json
l3-p08/src/app.js
l3-p08/src/errors/problem.js
l3-p08/src/middlewares/correlationId.js
l3-p08/src/middlewares/errors.js
l3-p08/src/middlewares/logger.js
l3-p08/src/middlewares/notFound.js
l3-p08/src/routes/health.routes.js
l3-p08/src/server.js
l3-p08/tests/config.json
l3-p08/tests/jest/http-smoke.jest.test.cjs
l3-p08/tests/jest/patterns.jest.test.cjs
l3-p08/tests/vitest/http-smoke.vitest.test.ts
l3-p08/tests/vitest/patterns.vitest.test.ts
l3-p08/vitest.config.ts
l3-p09/README.md
l3-p09/jest.config.cjs
l3-p09/package.json
l3-p09/src/app.js
l3-p09/src/errors/problem.js
l3-p09/src/middlewares/correlationId.js
l3-p09/src/middlewares/errors.js
l3-p09/src/middlewares/logger.js
l3-p09/src/middlewares/notFound.js
l3-p09/src/routes/health.routes.js
l3-p09/src/server.js
l3-p09/tests/config.json
l3-p09/tests/jest/http-smoke.jest.test.cjs
l3-p09/tests/jest/patterns.jest.test.cjs
l3-p09/tests/vitest/http-smoke.vitest.test.ts
l3-p09/tests/vitest/patterns.vitest.test.ts
l3-p09/vitest.config.ts
l3-p10/README.md
l3-p10/jest.config.cjs
l3-p10/package.json
l3-p10/src/app.js
l3-p10/src/errors/problem.js
l3-p10/src/middlewares/correlationId.js
l3-p10/src/middlewares/errors.js
l3-p10/src/middlewares/logger.js
l3-p10/src/middlewares/notFound.js
l3-p10/src/routes/health.routes.js
l3-p10/src/server.js
l3-p10/tests/config.json
l3-p10/tests/jest/http-smoke.jest.test.cjs
l3-p10/tests/jest/patterns.jest.test.cjs
l3-p10/tests/vitest/http-smoke.vitest.test.ts
l3-p10/tests/vitest/patterns.vitest.test.ts
l3-p10/vitest.config.ts
l3-p11/README.md
l3-p11/jest.config.cjs
l3-p11/package.json
l3-p11/src/app.js
l3-p11/src/errors/problem.js
l3-p11/src/middlewares/correlationId.js
l3-p11/src/middlewares/errors.js
l3-p11/src/middlewares/logger.js
l3-p11/src/middlewares/notFound.js
l3-p11/src/routes/health.routes.js
l3-p11/src/server.js
l3-p11/tests/config.json
l3-p11/tests/jest/http-smoke.jest.test.cjs
l3-p11/tests/jest/patterns.jest.test.cjs
l3-p11/tests/vitest/http-smoke.vitest.test.ts
l3-p11/tests/vitest/patterns.vitest.test.ts
l3-p11/vitest.config.ts
l3-p12/README.md
l3-p12/jest.config.cjs
l3-p12/package.json
l3-p12/src/app.js
l3-p12/src/errors/problem.js
l3-p12/src/middlewares/correlationId.js
l3-p12/src/middlewares/errors.js
l3-p12/src/middlewares/logger.js
l3-p12/src/middlewares/notFound.js
l3-p12/src/routes/health.routes.js
l3-p12/src/server.js
l3-p12/tests/config.json
l3-p12/tests/jest/http-smoke.jest.test.cjs
l3-p12/tests/jest/patterns.jest.test.cjs
l3-p12/tests/vitest/http-smoke.vitest.test.ts
l3-p12/tests/vitest/patterns.vitest.test.ts
l3-p12/vitest.config.ts
l3-p13/README.md
l3-p13/jest.config.cjs
l3-p13/package.json
l3-p13/src/app.js
l3-p13/src/errors/problem.js
l3-p13/src/middlewares/correlationId.js
l3-p13/src/middlewares/errors.js
l3-p13/src/middlewares/logger.js
l3-p13/src/middlewares/notFound.js
l3-p13/src/routes/health.routes.js
l3-p13/src/server.js
l3-p13/tests/config.json
l3-p13/tests/jest/http-smoke.jest.test.cjs
l3-p13/tests/jest/patterns.jest.test.cjs
l3-p13/tests/vitest/http-smoke.vitest.test.ts
l3-p13/tests/vitest/patterns.vitest.test.ts
l3-p13/vitest.config.ts
l3-p14/README.md
l3-p14/jest.config.cjs
l3-p14/package.json
l3-p14/src/app.js
l3-p14/src/errors/problem.js
l3-p14/src/middlewares/correlationId.js
l3-p14/src/middlewares/errors.js
l3-p14/src/middlewares/logger.js
l3-p14/src/middlewares/notFound.js
l3-p14/src/routes/health.routes.js
l3-p14/src/server.js
l3-p14/tests/config.json
l3-p14/tests/jest/http-smoke.jest.test.cjs
l3-p14/tests/jest/patterns.jest.test.cjs
l3-p14/tests/vitest/http-smoke.vitest.test.ts
l3-p14/tests/vitest/patterns.vitest.test.ts
l3-p14/vitest.config.ts
l3-p15/README.md
l3-p15/jest.config.cjs
l3-p15/package.json
l3-p15/src/app.js
l3-p15/src/errors/problem.js
l3-p15/src/middlewares/correlationId.js
l3-p15/src/middlewares/errors.js
l3-p15/src/middlewares/logger.js
l3-p15/src/middlewares/notFound.js
l3-p15/src/routes/health.routes.js
l3-p15/src/server.js
l3-p15/tests/config.json
l3-p15/tests/jest/http-smoke.jest.test.cjs
l3-p15/tests/jest/patterns.jest.test.cjs
l3-p15/tests/vitest/http-smoke.vitest.test.ts
l3-p15/tests/vitest/patterns.vitest.test.ts
l3-p15/vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 135, docs: 45, code: 360, tests: 225.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `l1-p01/package.json`: name=`l1-p01` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p02/package.json`: name=`l1-p02` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p03/package.json`: name=`l1-p03` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p04/package.json`: name=`l1-p04` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p05/package.json`: name=`l1-p05` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p06/package.json`: name=`l1-p06` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p07/package.json`: name=`l1-p07` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p08/package.json`: name=`l1-p08` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p09/package.json`: name=`l1-p09` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p10/package.json`: name=`l1-p10` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p11/package.json`: name=`l1-p11` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p12/package.json`: name=`l1-p12` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p13/package.json`: name=`l1-p13` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p14/package.json`: name=`l1-p14` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l1-p15/package.json`: name=`l1-p15` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p01/package.json`: name=`l2-p01` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p02/package.json`: name=`l2-p02` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p03/package.json`: name=`l2-p03` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p04/package.json`: name=`l2-p04` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p05/package.json`: name=`l2-p05` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p06/package.json`: name=`l2-p06` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p07/package.json`: name=`l2-p07` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p08/package.json`: name=`l2-p08` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p09/package.json`: name=`l2-p09` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p10/package.json`: name=`l2-p10` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p11/package.json`: name=`l2-p11` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p12/package.json`: name=`l2-p12` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p13/package.json`: name=`l2-p13` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p14/package.json`: name=`l2-p14` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l2-p15/package.json`: name=`l2-p15` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p01/package.json`: name=`l3-p01` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p02/package.json`: name=`l3-p02` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p03/package.json`: name=`l3-p03` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p04/package.json`: name=`l3-p04` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p05/package.json`: name=`l3-p05` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p06/package.json`: name=`l3-p06` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p07/package.json`: name=`l3-p07` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p08/package.json`: name=`l3-p08` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p09/package.json`: name=`l3-p09` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p10/package.json`: name=`l3-p10` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p11/package.json`: name=`l3-p11` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p12/package.json`: name=`l3-p12` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p13/package.json`: name=`l3-p13` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p14/package.json`: name=`l3-p14` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest
- `l3-p15/package.json`: name=`l3-p15` type=`commonjs` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** express, cors
  - **DevDeps:** nodemon, vitest, jest, supertest

### Seminar8_Partea3_p3-READMEs.zip

```
l1-p01-README.md
l1-p02-README.md
l1-p03-README.md
l1-p04-README.md
l1-p05-README.md
l1-p06-README.md
l1-p07-README.md
l1-p08-README.md
l1-p09-README.md
l1-p10-README.md
l1-p11-README.md
l1-p12-README.md
l1-p13-README.md
l1-p14-README.md
l1-p15-README.md
l2-p01-README.md
l2-p02-README.md
l2-p03-README.md
l2-p04-README.md
l2-p05-README.md
l2-p06-README.md
l2-p07-README.md
l2-p08-README.md
l2-p09-README.md
l2-p10-README.md
l2-p11-README.md
l2-p12-README.md
l2-p13-README.md
l2-p14-README.md
l2-p15-README.md
l3-p01-README.md
l3-p02-README.md
l3-p03-README.md
l3-p04-README.md
l3-p05-README.md
l3-p06-README.md
l3-p07-README.md
l3-p08-README.md
l3-p09-README.md
l3-p10-README.md
l3-p11-README.md
l3-p12-README.md
l3-p13-README.md
l3-p14-README.md
l3-p15-README.md
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** docs: 45.

## 2. Sinteza documentelor DOCX (teorie ↔ laborator ↔ proiecte)

### Seminar8_Partea1_Teorie.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 8 — REST cu Node/Express: rute, validări, erori
Partea 1: Teorie (extinsă)
- Hook realist: 48 de ore până la lansare — cum proiectezi un REST API care „ține” în fața UI‑ului și a realității
- Imaginați-vă că sunteți responsabil de infrastructura pentru „Clubs & Associations Hub”, un portal universitar care trebuie să deschidă înscrierile la cluburi studențești vineri, la ora 18:00. UI‑ul (partea client) e deja conturat — formulare accesibile, Fetch API robust, validări client‑side, micro‑cache și mesaje prietenoase, așa cum le-am dezvoltat la Seminarul 7. Lipsă: un serviciu REST care să livreze datele despre cluburi și să primească înscrierile. Constrângeri: disponibilitate rezonabilă, timp de răspuns previzibil, erori inteligibile (în format standard), reguli clare pentru duplicate, trasabilitate (un „correlation-id” pentru fiecare cerere) și o arhitectură suficient de curată încât să poată fi extinsă rapid după lansare.
În asemenea contexte, a greși „mic” (de exemplu, să mapi un caz de input invalid la 500) nu înseamnă doar o „nota proastă” la cod — înseamnă suport supraaglomerat, încredere scăzută și costuri reputaționale. În plus, tot ce face UI‑ul pe client se reflectă în server: dacă acolo vorbim de **timeout**, **retry** și **problem+json**, atunci serverul trebuie să aibă contracte ferme și o gestiune a erorilor care să reducă ambiguitățile. În această parte teoretică vom construi „harta mentală” a unui API REST solid în **Node.js + Express**: de la modelarea resurselor și semantica HTTP până la validări stratificate, erori standardizate și politici precum ETag, CORS și idempotency‑key.

### Seminar8_Partea2_Ghid_Arhive.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Partea 2 (Laborator)
- 1) Ce conțin arhivele
- • **s8p2-standalone.zip** — proiect unic `s8p2-standalone/` cu API complet + teste Vitest & Jest + README.

### Seminar8_Partea2_Laborator_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 8 — Partea 2: Laborator (extins)
- Obiectivul laboratorului
- Construim incremental un **REST API** în **Node.js + Express** pentru domeniul „Clubs & Associations Hub”, urmând principii stricte de proiectare: rute clare, validări robuste (input și, selectiv, output), erori standardizate **RFC 7807** (`application/problem+json`), CORS configurat prudent, **ETag** și condițional (demo), **Idempotency-Key** (demo) și o **observabilitate** minimă (correlation‑id + loguri structurate). Vom susține toate acestea cu **teste** rulate în paralel, în două cadre: **Vitest** și **Jest** (side‑by‑side).

### Seminar8_Partea3_Ghid_Arhive.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhive Partea 3 (Seminarul 8)
- Ce conțin arhivele
- • **s8p3-projects-standalone.zip** — toți cei 45 de itemi, fiecare cu `starter/` și `solution/`.

### Seminar8_Partea3_Proiecte_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 8 — Partea 3: Proiecte/teme (extinsă)
- Această Partea 3 reunește **45 de proiecte** distribuite pe trei niveluri — **L1 (Fundamente)**, **L2 (Intermediar)**, **L3 (Avansat)** — pentru a consolida competențele REST pe **Node/Express**. Fiecare proiect include: **scop didactic**, **specificații**, **criterii de acceptare**, **pași recomandați**, **soluție (rezumat)** și **AI‑assist (VSL)**. La final, ai **arhive ZIP** (starter standalone și monorepo PNPM) și un **ghid DOCX** de utilizare. Testele „smoke” (Vitest & Jest) rulează imediat; testele de „pattern” sunt marcate `todo`, pentru a le activa când vrei să verifici automat prezența conceptelor cheie (ETag, Idempotency‑Key etc.).
- Cum folosești pachetul de proiecte

## 3. Monorepo vs. standalone — analiză comparativă


**Manageri de pachete & workspaces.** Monorepo (PNPM) declară `packages/*` în `pnpm-workspace.yaml` și/sau `workspaces` în `package.json`, cu instalare la rădăcină (`pnpm i -w`). Standalone instalează local (`npm i`).

**Comenzi de instalare/testare.** Monorepo: `pnpm -w run test` sau `pnpm --filter <pkg> run test`. Standalone: `npm test`. Testare duală (Vitest & Jest) conform laboratorului. 

**Integrare CI.** Monorepo agregă pipelines (lint, unit, e2e) în `.github/workflows/*` ; standalone tinde să le aibă per proiect. 

**Avantaje/Dezavantaje.** Standalone — simplitate pentru începători; Monorepo — scalare pentru colecții mari (ex. 45 proiecte L1–L3), partajare de configuri și execuții rapide în CI; costul este înțelegerea filtrării PNPM și a dependențelor partajate.
## 4. Rolul fișierelor cheie (config, cod, teste, extra)

| Fișier / tip | Rol |
|---|---|
| `package.json` | Manifestul proiectului: metadate, dependențe, scripturi; definește `type:"module"` pentru ESM. |
| `pnpm-workspace.yaml` | Declară pachetele din monorepo pentru PNPM. |
| `vitest.config.ts` | Configurarea Vitest (Node/JSDOM, reporters, setup). |
| `jest.config.cjs` | Configurarea Jest (Node/JSDOM, transform ESM cu `--experimental-vm-modules` sau `babel-jest`). |
| `src/app.js` | Compoziție Express (middlewares, rute `/api/*`, handler erori RFC 7807). |
| `src/server.js` | Pornire HTTP (citește `.env`, setează `PORT`). |
| `errors/problem.js` | Factory & serializer `application/problem+json` (RFC 7807). |
| `utils/etag.js` | Calcul „weak ETag” pentru resurse; suport `If-None-Match → 304`. |

## 5. Corelații cod ↔ configurări ↔ teste


- **Rutele** din `routes/*.js` (ex. `GET /api/clubs`, `GET /api/clubs/:id`, `POST /api/registrations`) sunt verificate în **ambele suite** (Vitest & Jest) cu **Supertest**, fără a porni serverul pe port.  
- **`.env.example`**: variabilele (ex. `PORT`) sunt citite de `src/server.js` (via `dotenv`), ceea ce separă compunerea `app` de pornirea serverului — util în teste.  
- **ESLint + CI**: rulează `lint` și `test` în workflows; erorile de stil și de API contract sunt blocate înainte de merge.  
- **ETag + condițional**: `utils/etag.js` calculează ETag; testele verifică `If-None-Match → 304`.  
- **Idempotency‑Key** la `POST /api/registrations`: serviciul păstrează rezultatul per cheie; testele confirmă același `id` la repetare.  
- **CORS & observabilitate**: middleware‑urile setează antete corecte și `X‑Correlation‑Id`; testele pot aserta prezența lor.  
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S8 consolidează proiectarea **REST API** pe **Node.js + Express**, de la modelarea resurselor și semantica HTTP la validări, erori standardizate **RFC 7807**, **ETag**/condiționale, **Idempotency‑Key**, **CORS** și observabilitate. Arhivele sunt livrate în variante **standalone** și **monorepo** (PNPM), cu **testare dublă** (Vitest & Jest) pe aceleași scenarii. ### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; rădăcină + `packages/*` |
| Instalare | `npm i` | `pnpm i -w` |
| Testare | `npm test` (Vitest & Jest) | `pnpm -w run test` sau `--filter` |
| CI | Workflows simple per proiect | Workflows agregate, matrice pe pachete |
| Scalare (45 proiecte) | multiplicare directoare | pachete dedicate în `packages/*` |
| Public țintă | începători | echipe/colecții avansate |
### Inventar pe arhivă (roluri)

- **Seminar8_Partea2_p2-monorepo.zip** — config=5, docs=1, code=18, tests=4.
- **Seminar8_Partea2_p2-standalone.zip** — config=3, docs=1, code=18, tests=4.
- **Seminar8_Partea3_p3-monorepo.zip** — config=137, docs=45, code=360, tests=225.
- **Seminar8_Partea3_p3-standalone.zip** — config=135, docs=45, code=360, tests=225.
- **Seminar8_Partea3_p3-READMEs.zip** — docs=45.
### Explicații fișier-cu-fișier

Consultați tabelul din §4; detaliile de configurare și testare sunt aliniate cu **Laboratorul** și cu **Ghidul de arhive**.
### Corelații între fișiere


- `routes/*` & `controllers/*` ↔ `tests/*`: aceleași scenarii în Vitest & Jest (statusuri, antete, forme JSON).  
- `utils/etag.js` ↔ `tests/*`: `If-None-Match → 304`.  
- `services/registrations.service.js` ↔ `tests/*`: `Idempotency-Key`.  
- `.github/workflows/*` ↔ `lint`/`test`: pipeline determinist pentru PR-uri.  
### Recomandări pentru studenți


1) **Începeți în standalone**, apoi scalați în monorepo pentru colecții mari.  
2) **Scrieți validatori „puri”** și **serializați erorile** exclusiv prin `problem+json`.  
3) **Testați dublu** (Vitest & Jest) aceleași scenarii (inclusiv negative).  
4) **Modelați ETag/condiționale** și **Idempotency‑Key** ca politici observabile.  
5) **Mențineți CORS prudent** și **observabilitate** (correlation‑id + loguri JSON).  
6) **Documentați contractele** și păstrați README-urile locale actualizate.  
### Instrucțiuni „Quick start” per arhivă


**Partea 2 — standalone:**
```bash
unzip "Seminar8_Partea2_p2-standalone.zip" -d s8p2-standalone
cd s8p2-standalone
npm i
npm test          # rulează Vitest & Jest
npm run dev       # pornește API (ex.: http://localhost:5380)
```

**Partea 2 — monorepo:**
```bash
unzip "Seminar8_Partea2_p2-monorepo.zip" -d s8p2-monorepo
cd s8p2-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter ./packages/api run dev
```

**Partea 3 — monorepo (proiecte):**
```bash
unzip "Seminar8_Partea3_p3-monorepo.zip" -d s8p3-monorepo
cd s8p3-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter l1-p01-starter run dev
```

**Partea 3 — standalone (proiecte):**
```bash
unzip "Seminar8_Partea3_p3-standalone.zip" -d s8p3-standalone
cd s8p3-standalone/L1/L1-P01/starter
npm i
npm test
npm run dev
```
### Troubleshooting (erori frecvente)


- **`422` vs `400`** → JSON invalid → `400`; JSON valid dar semantic invalid → `422`.  
- **ETag nu răspunde `304`** → verificați `If-None-Match` și calculul hash‑ului; asigurați actualizarea `updatedAt`.  
- **Idempotency neefectiv** → headerul `Idempotency-Key` lipsește sau storage‑ul nu persistă; pentru demo este `in‑memory`.  
- **ESM/Jest** → rulați Jest într‑un proiect CJS sau configurați `babel-jest`; Vitest folosește ESM.  
- **CORS** → originea UI nu e permisă: ajustați lista/regexul din middleware.  
- **PNPM filter** → verificați `pnpm-workspace.yaml` și câmpul `name` din `package.json`.  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** — modelarea resurselor, semantica HTTP, problem+json, ETag/condiționale, CORS, idempotency, observabilitate.  
- **Partea 2 (Laborator)** — rute `clubs`/`registrations`, validări input/output, ETag & `If-None-Match`, `Idempotency-Key`, testare dublă.  
- **Partea 3 (Ghid Arhive)** — cum rulezi standalone/monorepo, comenzi PNPM și structură pe niveluri; **Proiecte** — 45 itemi L1–L3 cu *starter*/*solution* și teste echivalente.  
### Prompt-șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S8** (standalone & monorepo) un REST API Node/Express cu rutele `clubs`/`registrations`, validări „pure”, erori **RFC 7807**, **ETag**/condiționale, **Idempotency‑Key**, CORS și observabilitate; scrie testele **Vitest** și **Jest** cu Supertest, CI, README cu Quick start & Troubleshooting și variante **starter**/**solution**.”
