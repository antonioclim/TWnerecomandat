# Seminarul S9 — Persistență cu SQLite & Sequelize (standalone & monorepo) — Analiză integrată a arhivelor și ghidurilor

*Generat la 2025-09-21 04:57.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar9_Partea2_p2-standalone.zip

```
README.md
jest.config.cjs
package.json
src/app.js
src/db/associations.js
src/db/connection.js
src/db/index.js
src/db/models/club.js
src/db/models/event.js
src/db/models/member.js
src/db/models/registration.js
src/db/services/enroll.js
src/server.js
tests/jest/models.jest.test.cjs
tests/jest/trx.jest.test.cjs
tests/vitest/eager.vitest.test.ts
tests/vitest/models.vitest.test.ts
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 3, docs: 1, code: 10, tests: 4.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s9p2-sequelize-sqlite-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest

### Seminar9_Partea3_p3-monorepo.zip

```
package.json
packages/L1-P01/README.md
packages/L1-P01/jest.config.cjs
packages/L1-P01/package.json
packages/L1-P01/src/app.js
packages/L1-P01/src/db/associations.js
packages/L1-P01/src/db/connection.js
packages/L1-P01/src/db/index.js
packages/L1-P01/src/db/models/club.js
packages/L1-P01/src/db/models/event.js
packages/L1-P01/src/db/models/member.js
packages/L1-P01/src/db/models/registration.js
packages/L1-P01/src/db/seed.js
packages/L1-P01/src/db/services/enroll.js
packages/L1-P01/src/server.js
packages/L1-P01/tests/config.json
packages/L1-P01/tests/jest.test.mjs
packages/L1-P01/tests/vitest.test.ts
packages/L1-P01/vitest.config.ts
packages/L1-P02/README.md
packages/L1-P02/jest.config.cjs
packages/L1-P02/package.json
packages/L1-P02/src/app.js
packages/L1-P02/src/db/associations.js
packages/L1-P02/src/db/connection.js
packages/L1-P02/src/db/index.js
packages/L1-P02/src/db/models/club.js
packages/L1-P02/src/db/models/event.js
packages/L1-P02/src/db/models/member.js
packages/L1-P02/src/db/models/registration.js
packages/L1-P02/src/db/seed.js
packages/L1-P02/src/db/services/enroll.js
packages/L1-P02/src/server.js
packages/L1-P02/tests/config.json
packages/L1-P02/tests/jest.test.mjs
packages/L1-P02/tests/vitest.test.ts
packages/L1-P02/vitest.config.ts
packages/L1-P03/README.md
packages/L1-P03/jest.config.cjs
packages/L1-P03/package.json
packages/L1-P03/src/app.js
packages/L1-P03/src/db/associations.js
packages/L1-P03/src/db/connection.js
packages/L1-P03/src/db/index.js
packages/L1-P03/src/db/models/club.js
packages/L1-P03/src/db/models/event.js
packages/L1-P03/src/db/models/member.js
packages/L1-P03/src/db/models/registration.js
packages/L1-P03/src/db/seed.js
packages/L1-P03/src/db/services/enroll.js
packages/L1-P03/src/server.js
packages/L1-P03/tests/config.json
packages/L1-P03/tests/jest.test.mjs
packages/L1-P03/tests/vitest.test.ts
packages/L1-P03/vitest.config.ts
packages/L1-P04/README.md
packages/L1-P04/jest.config.cjs
packages/L1-P04/package.json
packages/L1-P04/src/app.js
packages/L1-P04/src/db/associations.js
packages/L1-P04/src/db/connection.js
packages/L1-P04/src/db/index.js
packages/L1-P04/src/db/models/club.js
packages/L1-P04/src/db/models/event.js
packages/L1-P04/src/db/models/member.js
packages/L1-P04/src/db/models/registration.js
packages/L1-P04/src/db/seed.js
packages/L1-P04/src/db/services/enroll.js
packages/L1-P04/src/server.js
packages/L1-P04/tests/config.json
packages/L1-P04/tests/jest.test.mjs
packages/L1-P04/tests/vitest.test.ts
packages/L1-P04/vitest.config.ts
packages/L1-P05/README.md
packages/L1-P05/jest.config.cjs
packages/L1-P05/package.json
packages/L1-P05/src/app.js
packages/L1-P05/src/db/associations.js
packages/L1-P05/src/db/connection.js
packages/L1-P05/src/db/index.js
packages/L1-P05/src/db/models/club.js
packages/L1-P05/src/db/models/event.js
packages/L1-P05/src/db/models/member.js
packages/L1-P05/src/db/models/registration.js
packages/L1-P05/src/db/seed.js
packages/L1-P05/src/db/services/enroll.js
packages/L1-P05/src/server.js
packages/L1-P05/tests/config.json
packages/L1-P05/tests/jest.test.mjs
packages/L1-P05/tests/vitest.test.ts
packages/L1-P05/vitest.config.ts
packages/L1-P06/README.md
packages/L1-P06/jest.config.cjs
packages/L1-P06/package.json
packages/L1-P06/src/app.js
packages/L1-P06/src/db/associations.js
packages/L1-P06/src/db/connection.js
packages/L1-P06/src/db/index.js
packages/L1-P06/src/db/models/club.js
packages/L1-P06/src/db/models/event.js
packages/L1-P06/src/db/models/member.js
packages/L1-P06/src/db/models/registration.js
packages/L1-P06/src/db/seed.js
packages/L1-P06/src/db/services/enroll.js
packages/L1-P06/src/server.js
packages/L1-P06/tests/config.json
packages/L1-P06/tests/jest.test.mjs
packages/L1-P06/tests/vitest.test.ts
packages/L1-P06/vitest.config.ts
packages/L1-P07/README.md
packages/L1-P07/jest.config.cjs
packages/L1-P07/package.json
packages/L1-P07/src/app.js
packages/L1-P07/src/db/associations.js
packages/L1-P07/src/db/connection.js
packages/L1-P07/src/db/index.js
packages/L1-P07/src/db/models/club.js
packages/L1-P07/src/db/models/event.js
packages/L1-P07/src/db/models/member.js
packages/L1-P07/src/db/models/registration.js
packages/L1-P07/src/db/seed.js
packages/L1-P07/src/db/services/enroll.js
packages/L1-P07/src/server.js
packages/L1-P07/tests/config.json
packages/L1-P07/tests/jest.test.mjs
packages/L1-P07/tests/vitest.test.ts
packages/L1-P07/vitest.config.ts
packages/L1-P08/README.md
packages/L1-P08/jest.config.cjs
packages/L1-P08/package.json
packages/L1-P08/src/app.js
packages/L1-P08/src/db/associations.js
packages/L1-P08/src/db/connection.js
packages/L1-P08/src/db/index.js
packages/L1-P08/src/db/models/club.js
packages/L1-P08/src/db/models/event.js
packages/L1-P08/src/db/models/member.js
packages/L1-P08/src/db/models/registration.js
packages/L1-P08/src/db/seed.js
packages/L1-P08/src/db/services/enroll.js
packages/L1-P08/src/server.js
packages/L1-P08/tests/config.json
packages/L1-P08/tests/jest.test.mjs
packages/L1-P08/tests/vitest.test.ts
packages/L1-P08/vitest.config.ts
packages/L1-P09/README.md
packages/L1-P09/jest.config.cjs
packages/L1-P09/package.json
packages/L1-P09/src/app.js
packages/L1-P09/src/db/associations.js
packages/L1-P09/src/db/connection.js
packages/L1-P09/src/db/index.js
packages/L1-P09/src/db/models/club.js
packages/L1-P09/src/db/models/event.js
packages/L1-P09/src/db/models/member.js
packages/L1-P09/src/db/models/registration.js
packages/L1-P09/src/db/seed.js
packages/L1-P09/src/db/services/enroll.js
packages/L1-P09/src/server.js
packages/L1-P09/tests/config.json
packages/L1-P09/tests/jest.test.mjs
packages/L1-P09/tests/vitest.test.ts
packages/L1-P09/vitest.config.ts
packages/L1-P10/README.md
packages/L1-P10/jest.config.cjs
packages/L1-P10/package.json
packages/L1-P10/src/app.js
packages/L1-P10/src/db/associations.js
packages/L1-P10/src/db/connection.js
packages/L1-P10/src/db/index.js
packages/L1-P10/src/db/models/club.js
packages/L1-P10/src/db/models/event.js
packages/L1-P10/src/db/models/member.js
packages/L1-P10/src/db/models/registration.js
packages/L1-P10/src/db/seed.js
packages/L1-P10/src/db/services/enroll.js
packages/L1-P10/src/server.js
packages/L1-P10/tests/config.json
packages/L1-P10/tests/jest.test.mjs
packages/L1-P10/tests/vitest.test.ts
packages/L1-P10/vitest.config.ts
packages/L1-P11/README.md
packages/L1-P11/jest.config.cjs
packages/L1-P11/package.json
packages/L1-P11/src/app.js
packages/L1-P11/src/db/associations.js
packages/L1-P11/src/db/connection.js
packages/L1-P11/src/db/index.js
packages/L1-P11/src/db/models/club.js
packages/L1-P11/src/db/models/event.js
packages/L1-P11/src/db/models/member.js
packages/L1-P11/src/db/models/registration.js
packages/L1-P11/src/db/seed.js
packages/L1-P11/src/db/services/enroll.js
packages/L1-P11/src/server.js
packages/L1-P11/tests/config.json
packages/L1-P11/tests/jest.test.mjs
packages/L1-P11/tests/vitest.test.ts
packages/L1-P11/vitest.config.ts
packages/L1-P12/README.md
packages/L1-P12/jest.config.cjs
packages/L1-P12/package.json
packages/L1-P12/src/app.js
packages/L1-P12/src/db/associations.js
packages/L1-P12/src/db/connection.js
packages/L1-P12/src/db/index.js
packages/L1-P12/src/db/models/club.js
packages/L1-P12/src/db/models/event.js
packages/L1-P12/src/db/models/member.js
packages/L1-P12/src/db/models/registration.js
packages/L1-P12/src/db/seed.js
packages/L1-P12/src/db/services/enroll.js
packages/L1-P12/src/server.js
packages/L1-P12/tests/config.json
packages/L1-P12/tests/jest.test.mjs
packages/L1-P12/tests/vitest.test.ts
packages/L1-P12/vitest.config.ts
packages/L1-P13/README.md
packages/L1-P13/jest.config.cjs
packages/L1-P13/package.json
packages/L1-P13/src/app.js
packages/L1-P13/src/db/associations.js
packages/L1-P13/src/db/connection.js
packages/L1-P13/src/db/index.js
packages/L1-P13/src/db/models/club.js
packages/L1-P13/src/db/models/event.js
packages/L1-P13/src/db/models/member.js
packages/L1-P13/src/db/models/registration.js
packages/L1-P13/src/db/seed.js
packages/L1-P13/src/db/services/enroll.js
packages/L1-P13/src/server.js
packages/L1-P13/tests/config.json
packages/L1-P13/tests/jest.test.mjs
packages/L1-P13/tests/vitest.test.ts
packages/L1-P13/vitest.config.ts
packages/L1-P14/README.md
packages/L1-P14/jest.config.cjs
packages/L1-P14/package.json
packages/L1-P14/src/app.js
packages/L1-P14/src/db/associations.js
packages/L1-P14/src/db/connection.js
packages/L1-P14/src/db/index.js
packages/L1-P14/src/db/models/club.js
packages/L1-P14/src/db/models/event.js
packages/L1-P14/src/db/models/member.js
packages/L1-P14/src/db/models/registration.js
packages/L1-P14/src/db/seed.js
packages/L1-P14/src/db/services/enroll.js
packages/L1-P14/src/server.js
packages/L1-P14/tests/config.json
packages/L1-P14/tests/jest.test.mjs
packages/L1-P14/tests/vitest.test.ts
packages/L1-P14/vitest.config.ts
packages/L1-P15/README.md
packages/L1-P15/jest.config.cjs
packages/L1-P15/package.json
packages/L1-P15/src/app.js
packages/L1-P15/src/db/associations.js
packages/L1-P15/src/db/connection.js
packages/L1-P15/src/db/index.js
packages/L1-P15/src/db/models/club.js
packages/L1-P15/src/db/models/event.js
packages/L1-P15/src/db/models/member.js
packages/L1-P15/src/db/models/registration.js
packages/L1-P15/src/db/seed.js
packages/L1-P15/src/db/services/enroll.js
packages/L1-P15/src/server.js
packages/L1-P15/tests/config.json
packages/L1-P15/tests/jest.test.mjs
packages/L1-P15/tests/vitest.test.ts
packages/L1-P15/vitest.config.ts
packages/L2-P01/README.md
packages/L2-P01/jest.config.cjs
packages/L2-P01/package.json
packages/L2-P01/src/app.js
packages/L2-P01/src/db/associations.js
packages/L2-P01/src/db/connection.js
packages/L2-P01/src/db/index.js
packages/L2-P01/src/db/models/club.js
packages/L2-P01/src/db/models/event.js
packages/L2-P01/src/db/models/member.js
packages/L2-P01/src/db/models/registration.js
packages/L2-P01/src/db/seed.js
packages/L2-P01/src/db/services/enroll.js
packages/L2-P01/src/server.js
packages/L2-P01/tests/config.json
packages/L2-P01/tests/jest.test.mjs
packages/L2-P01/tests/vitest.test.ts
packages/L2-P01/vitest.config.ts
packages/L2-P02/README.md
packages/L2-P02/jest.config.cjs
packages/L2-P02/package.json
packages/L2-P02/src/app.js
packages/L2-P02/src/db/associations.js
packages/L2-P02/src/db/connection.js
packages/L2-P02/src/db/index.js
packages/L2-P02/src/db/models/club.js
packages/L2-P02/src/db/models/event.js
packages/L2-P02/src/db/models/member.js
packages/L2-P02/src/db/models/registration.js
packages/L2-P02/src/db/seed.js
packages/L2-P02/src/db/services/enroll.js
packages/L2-P02/src/server.js
packages/L2-P02/tests/config.json
packages/L2-P02/tests/jest.test.mjs
packages/L2-P02/tests/vitest.test.ts
packages/L2-P02/vitest.config.ts
packages/L2-P03/README.md
packages/L2-P03/jest.config.cjs
packages/L2-P03/package.json
packages/L2-P03/src/app.js
packages/L2-P03/src/db/associations.js
packages/L2-P03/src/db/connection.js
packages/L2-P03/src/db/index.js
packages/L2-P03/src/db/models/club.js
packages/L2-P03/src/db/models/event.js
packages/L2-P03/src/db/models/member.js
packages/L2-P03/src/db/models/registration.js
packages/L2-P03/src/db/seed.js
packages/L2-P03/src/db/services/enroll.js
packages/L2-P03/src/server.js
packages/L2-P03/tests/config.json
packages/L2-P03/tests/jest.test.mjs
packages/L2-P03/tests/vitest.test.ts
packages/L2-P03/vitest.config.ts
packages/L2-P04/README.md
packages/L2-P04/jest.config.cjs
packages/L2-P04/package.json
packages/L2-P04/src/app.js
packages/L2-P04/src/db/associations.js
packages/L2-P04/src/db/connection.js
packages/L2-P04/src/db/index.js
packages/L2-P04/src/db/models/club.js
packages/L2-P04/src/db/models/event.js
packages/L2-P04/src/db/models/member.js
packages/L2-P04/src/db/models/registration.js
packages/L2-P04/src/db/seed.js
packages/L2-P04/src/db/services/enroll.js
packages/L2-P04/src/server.js
packages/L2-P04/tests/config.json
packages/L2-P04/tests/jest.test.mjs
packages/L2-P04/tests/vitest.test.ts
packages/L2-P04/vitest.config.ts
packages/L2-P05/README.md
packages/L2-P05/jest.config.cjs
packages/L2-P05/package.json
packages/L2-P05/src/app.js
packages/L2-P05/src/db/associations.js
packages/L2-P05/src/db/connection.js
packages/L2-P05/src/db/index.js
packages/L2-P05/src/db/models/club.js
packages/L2-P05/src/db/models/event.js
packages/L2-P05/src/db/models/member.js
packages/L2-P05/src/db/models/registration.js
packages/L2-P05/src/db/seed.js
packages/L2-P05/src/db/services/enroll.js
packages/L2-P05/src/server.js
packages/L2-P05/tests/config.json
packages/L2-P05/tests/jest.test.mjs
packages/L2-P05/tests/vitest.test.ts
packages/L2-P05/vitest.config.ts
packages/L2-P06/README.md
packages/L2-P06/jest.config.cjs
packages/L2-P06/package.json
packages/L2-P06/src/app.js
packages/L2-P06/src/db/associations.js
packages/L2-P06/src/db/connection.js
packages/L2-P06/src/db/index.js
packages/L2-P06/src/db/models/club.js
packages/L2-P06/src/db/models/event.js
packages/L2-P06/src/db/models/member.js
packages/L2-P06/src/db/models/registration.js
packages/L2-P06/src/db/seed.js
packages/L2-P06/src/db/services/enroll.js
packages/L2-P06/src/server.js
packages/L2-P06/tests/config.json
packages/L2-P06/tests/jest.test.mjs
packages/L2-P06/tests/vitest.test.ts
packages/L2-P06/vitest.config.ts
packages/L2-P07/README.md
packages/L2-P07/jest.config.cjs
packages/L2-P07/package.json
packages/L2-P07/src/app.js
packages/L2-P07/src/db/associations.js
packages/L2-P07/src/db/connection.js
packages/L2-P07/src/db/index.js
packages/L2-P07/src/db/models/club.js
packages/L2-P07/src/db/models/event.js
packages/L2-P07/src/db/models/member.js
packages/L2-P07/src/db/models/registration.js
packages/L2-P07/src/db/seed.js
packages/L2-P07/src/db/services/enroll.js
packages/L2-P07/src/server.js
packages/L2-P07/tests/config.json
packages/L2-P07/tests/jest.test.mjs
packages/L2-P07/tests/vitest.test.ts
packages/L2-P07/vitest.config.ts
packages/L2-P08/README.md
packages/L2-P08/jest.config.cjs
packages/L2-P08/package.json
packages/L2-P08/src/app.js
packages/L2-P08/src/db/associations.js
packages/L2-P08/src/db/connection.js
packages/L2-P08/src/db/index.js
packages/L2-P08/src/db/models/club.js
packages/L2-P08/src/db/models/event.js
packages/L2-P08/src/db/models/member.js
packages/L2-P08/src/db/models/registration.js
packages/L2-P08/src/db/seed.js
packages/L2-P08/src/db/services/enroll.js
packages/L2-P08/src/server.js
packages/L2-P08/tests/config.json
packages/L2-P08/tests/jest.test.mjs
packages/L2-P08/tests/vitest.test.ts
packages/L2-P08/vitest.config.ts
packages/L2-P09/README.md
packages/L2-P09/jest.config.cjs
packages/L2-P09/package.json
packages/L2-P09/src/app.js
packages/L2-P09/src/db/associations.js
packages/L2-P09/src/db/connection.js
packages/L2-P09/src/db/index.js
packages/L2-P09/src/db/models/club.js
packages/L2-P09/src/db/models/event.js
packages/L2-P09/src/db/models/member.js
packages/L2-P09/src/db/models/registration.js
packages/L2-P09/src/db/seed.js
packages/L2-P09/src/db/services/enroll.js
packages/L2-P09/src/server.js
packages/L2-P09/tests/config.json
packages/L2-P09/tests/jest.test.mjs
packages/L2-P09/tests/vitest.test.ts
packages/L2-P09/vitest.config.ts
packages/L2-P10/README.md
packages/L2-P10/jest.config.cjs
packages/L2-P10/package.json
packages/L2-P10/src/app.js
packages/L2-P10/src/db/associations.js
packages/L2-P10/src/db/connection.js
packages/L2-P10/src/db/index.js
packages/L2-P10/src/db/models/club.js
packages/L2-P10/src/db/models/event.js
packages/L2-P10/src/db/models/member.js
packages/L2-P10/src/db/models/registration.js
packages/L2-P10/src/db/seed.js
packages/L2-P10/src/db/services/enroll.js
packages/L2-P10/src/server.js
packages/L2-P10/tests/config.json
packages/L2-P10/tests/jest.test.mjs
packages/L2-P10/tests/vitest.test.ts
packages/L2-P10/vitest.config.ts
packages/L2-P11/README.md
packages/L2-P11/jest.config.cjs
packages/L2-P11/package.json
packages/L2-P11/src/app.js
packages/L2-P11/src/db/associations.js
packages/L2-P11/src/db/connection.js
packages/L2-P11/src/db/index.js
packages/L2-P11/src/db/models/club.js
packages/L2-P11/src/db/models/event.js
packages/L2-P11/src/db/models/member.js
packages/L2-P11/src/db/models/registration.js
packages/L2-P11/src/db/seed.js
packages/L2-P11/src/db/services/enroll.js
packages/L2-P11/src/server.js
packages/L2-P11/tests/config.json
packages/L2-P11/tests/jest.test.mjs
packages/L2-P11/tests/vitest.test.ts
packages/L2-P11/vitest.config.ts
packages/L2-P12/README.md
packages/L2-P12/jest.config.cjs
packages/L2-P12/package.json
packages/L2-P12/src/app.js
packages/L2-P12/src/db/associations.js
packages/L2-P12/src/db/connection.js
packages/L2-P12/src/db/index.js
packages/L2-P12/src/db/models/club.js
packages/L2-P12/src/db/models/event.js
packages/L2-P12/src/db/models/member.js
packages/L2-P12/src/db/models/registration.js
packages/L2-P12/src/db/seed.js
packages/L2-P12/src/db/services/enroll.js
packages/L2-P12/src/server.js
packages/L2-P12/tests/config.json
packages/L2-P12/tests/jest.test.mjs
packages/L2-P12/tests/vitest.test.ts
packages/L2-P12/vitest.config.ts
packages/L2-P13/README.md
packages/L2-P13/jest.config.cjs
packages/L2-P13/package.json
packages/L2-P13/src/app.js
packages/L2-P13/src/db/associations.js
packages/L2-P13/src/db/connection.js
packages/L2-P13/src/db/index.js
packages/L2-P13/src/db/models/club.js
packages/L2-P13/src/db/models/event.js
packages/L2-P13/src/db/models/member.js
packages/L2-P13/src/db/models/registration.js
packages/L2-P13/src/db/seed.js
packages/L2-P13/src/db/services/enroll.js
packages/L2-P13/src/server.js
packages/L2-P13/tests/config.json
packages/L2-P13/tests/jest.test.mjs
packages/L2-P13/tests/vitest.test.ts
packages/L2-P13/vitest.config.ts
packages/L2-P14/README.md
packages/L2-P14/jest.config.cjs
packages/L2-P14/package.json
packages/L2-P14/src/app.js
packages/L2-P14/src/db/associations.js
packages/L2-P14/src/db/connection.js
packages/L2-P14/src/db/index.js
packages/L2-P14/src/db/models/club.js
packages/L2-P14/src/db/models/event.js
packages/L2-P14/src/db/models/member.js
packages/L2-P14/src/db/models/registration.js
packages/L2-P14/src/db/seed.js
packages/L2-P14/src/db/services/enroll.js
packages/L2-P14/src/server.js
packages/L2-P14/tests/config.json
packages/L2-P14/tests/jest.test.mjs
packages/L2-P14/tests/vitest.test.ts
packages/L2-P14/vitest.config.ts
packages/L2-P15/README.md
packages/L2-P15/jest.config.cjs
packages/L2-P15/package.json
packages/L2-P15/src/app.js
packages/L2-P15/src/db/associations.js
packages/L2-P15/src/db/connection.js
packages/L2-P15/src/db/index.js
packages/L2-P15/src/db/models/club.js
packages/L2-P15/src/db/models/event.js
packages/L2-P15/src/db/models/member.js
packages/L2-P15/src/db/models/registration.js
packages/L2-P15/src/db/seed.js
packages/L2-P15/src/db/services/enroll.js
packages/L2-P15/src/server.js
packages/L2-P15/tests/config.json
packages/L2-P15/tests/jest.test.mjs
packages/L2-P15/tests/vitest.test.ts
packages/L2-P15/vitest.config.ts
packages/L3-P01/README.md
packages/L3-P01/jest.config.cjs
packages/L3-P01/package.json
packages/L3-P01/src/app.js
packages/L3-P01/src/db/associations.js
packages/L3-P01/src/db/connection.js
packages/L3-P01/src/db/index.js
packages/L3-P01/src/db/models/club.js
packages/L3-P01/src/db/models/event.js
packages/L3-P01/src/db/models/member.js
packages/L3-P01/src/db/models/registration.js
packages/L3-P01/src/db/seed.js
packages/L3-P01/src/db/services/enroll.js
packages/L3-P01/src/server.js
packages/L3-P01/tests/config.json
packages/L3-P01/tests/jest.test.mjs
packages/L3-P01/tests/vitest.test.ts
packages/L3-P01/vitest.config.ts
packages/L3-P02/README.md
packages/L3-P02/jest.config.cjs
packages/L3-P02/package.json
packages/L3-P02/src/app.js
packages/L3-P02/src/db/associations.js
packages/L3-P02/src/db/connection.js
packages/L3-P02/src/db/index.js
packages/L3-P02/src/db/models/club.js
packages/L3-P02/src/db/models/event.js
packages/L3-P02/src/db/models/member.js
packages/L3-P02/src/db/models/registration.js
packages/L3-P02/src/db/seed.js
packages/L3-P02/src/db/services/enroll.js
packages/L3-P02/src/server.js
packages/L3-P02/tests/config.json
packages/L3-P02/tests/jest.test.mjs
packages/L3-P02/tests/vitest.test.ts
packages/L3-P02/vitest.config.ts
packages/L3-P03/README.md
packages/L3-P03/jest.config.cjs
packages/L3-P03/package.json
packages/L3-P03/src/app.js
packages/L3-P03/src/db/associations.js
packages/L3-P03/src/db/connection.js
packages/L3-P03/src/db/index.js
packages/L3-P03/src/db/models/club.js
packages/L3-P03/src/db/models/event.js
packages/L3-P03/src/db/models/member.js
packages/L3-P03/src/db/models/registration.js
packages/L3-P03/src/db/seed.js
packages/L3-P03/src/db/services/enroll.js
packages/L3-P03/src/server.js
packages/L3-P03/tests/config.json
packages/L3-P03/tests/jest.test.mjs
packages/L3-P03/tests/vitest.test.ts
packages/L3-P03/vitest.config.ts
packages/L3-P04/README.md
packages/L3-P04/jest.config.cjs
packages/L3-P04/package.json
packages/L3-P04/src/app.js
packages/L3-P04/src/db/associations.js
packages/L3-P04/src/db/connection.js
packages/L3-P04/src/db/index.js
packages/L3-P04/src/db/models/club.js
packages/L3-P04/src/db/models/event.js
packages/L3-P04/src/db/models/member.js
packages/L3-P04/src/db/models/registration.js
packages/L3-P04/src/db/seed.js
packages/L3-P04/src/db/services/enroll.js
packages/L3-P04/src/server.js
packages/L3-P04/tests/config.json
packages/L3-P04/tests/jest.test.mjs
packages/L3-P04/tests/vitest.test.ts
packages/L3-P04/vitest.config.ts
packages/L3-P05/README.md
packages/L3-P05/jest.config.cjs
packages/L3-P05/package.json
packages/L3-P05/src/app.js
packages/L3-P05/src/db/associations.js
packages/L3-P05/src/db/connection.js
packages/L3-P05/src/db/index.js
packages/L3-P05/src/db/models/club.js
packages/L3-P05/src/db/models/event.js
packages/L3-P05/src/db/models/member.js
packages/L3-P05/src/db/models/registration.js
packages/L3-P05/src/db/seed.js
packages/L3-P05/src/db/services/enroll.js
packages/L3-P05/src/server.js
packages/L3-P05/tests/config.json
packages/L3-P05/tests/jest.test.mjs
packages/L3-P05/tests/vitest.test.ts
packages/L3-P05/vitest.config.ts
packages/L3-P06/README.md
packages/L3-P06/jest.config.cjs
packages/L3-P06/package.json
packages/L3-P06/src/app.js
packages/L3-P06/src/db/associations.js
packages/L3-P06/src/db/connection.js
packages/L3-P06/src/db/index.js
packages/L3-P06/src/db/models/club.js
packages/L3-P06/src/db/models/event.js
packages/L3-P06/src/db/models/member.js
packages/L3-P06/src/db/models/registration.js
packages/L3-P06/src/db/seed.js
packages/L3-P06/src/db/services/enroll.js
packages/L3-P06/src/server.js
packages/L3-P06/tests/config.json
packages/L3-P06/tests/jest.test.mjs
packages/L3-P06/tests/vitest.test.ts
packages/L3-P06/vitest.config.ts
packages/L3-P07/README.md
packages/L3-P07/jest.config.cjs
packages/L3-P07/package.json
packages/L3-P07/src/app.js
packages/L3-P07/src/db/associations.js
packages/L3-P07/src/db/connection.js
packages/L3-P07/src/db/index.js
packages/L3-P07/src/db/models/club.js
packages/L3-P07/src/db/models/event.js
packages/L3-P07/src/db/models/member.js
packages/L3-P07/src/db/models/registration.js
packages/L3-P07/src/db/seed.js
packages/L3-P07/src/db/services/enroll.js
packages/L3-P07/src/server.js
packages/L3-P07/tests/config.json
packages/L3-P07/tests/jest.test.mjs
packages/L3-P07/tests/vitest.test.ts
packages/L3-P07/vitest.config.ts
packages/L3-P08/README.md
packages/L3-P08/jest.config.cjs
packages/L3-P08/package.json
packages/L3-P08/src/app.js
packages/L3-P08/src/db/associations.js
packages/L3-P08/src/db/connection.js
packages/L3-P08/src/db/index.js
packages/L3-P08/src/db/models/club.js
packages/L3-P08/src/db/models/event.js
packages/L3-P08/src/db/models/member.js
packages/L3-P08/src/db/models/registration.js
packages/L3-P08/src/db/seed.js
packages/L3-P08/src/db/services/enroll.js
packages/L3-P08/src/server.js
packages/L3-P08/tests/config.json
packages/L3-P08/tests/jest.test.mjs
packages/L3-P08/tests/vitest.test.ts
packages/L3-P08/vitest.config.ts
packages/L3-P09/README.md
packages/L3-P09/jest.config.cjs
packages/L3-P09/package.json
packages/L3-P09/src/app.js
packages/L3-P09/src/db/associations.js
packages/L3-P09/src/db/connection.js
packages/L3-P09/src/db/index.js
packages/L3-P09/src/db/models/club.js
packages/L3-P09/src/db/models/event.js
packages/L3-P09/src/db/models/member.js
packages/L3-P09/src/db/models/registration.js
packages/L3-P09/src/db/seed.js
packages/L3-P09/src/db/services/enroll.js
packages/L3-P09/src/server.js
packages/L3-P09/tests/config.json
packages/L3-P09/tests/jest.test.mjs
packages/L3-P09/tests/vitest.test.ts
packages/L3-P09/vitest.config.ts
packages/L3-P10/README.md
packages/L3-P10/jest.config.cjs
packages/L3-P10/package.json
packages/L3-P10/src/app.js
packages/L3-P10/src/db/associations.js
packages/L3-P10/src/db/connection.js
packages/L3-P10/src/db/index.js
packages/L3-P10/src/db/models/club.js
packages/L3-P10/src/db/models/event.js
packages/L3-P10/src/db/models/member.js
packages/L3-P10/src/db/models/registration.js
packages/L3-P10/src/db/seed.js
packages/L3-P10/src/db/services/enroll.js
packages/L3-P10/src/server.js
packages/L3-P10/tests/config.json
packages/L3-P10/tests/jest.test.mjs
packages/L3-P10/tests/vitest.test.ts
packages/L3-P10/vitest.config.ts
packages/L3-P11/README.md
packages/L3-P11/jest.config.cjs
packages/L3-P11/package.json
packages/L3-P11/src/app.js
packages/L3-P11/src/db/associations.js
packages/L3-P11/src/db/connection.js
packages/L3-P11/src/db/index.js
packages/L3-P11/src/db/models/club.js
packages/L3-P11/src/db/models/event.js
packages/L3-P11/src/db/models/member.js
packages/L3-P11/src/db/models/registration.js
packages/L3-P11/src/db/seed.js
packages/L3-P11/src/db/services/enroll.js
packages/L3-P11/src/server.js
packages/L3-P11/tests/config.json
packages/L3-P11/tests/jest.test.mjs
packages/L3-P11/tests/vitest.test.ts
packages/L3-P11/vitest.config.ts
packages/L3-P12/README.md
packages/L3-P12/jest.config.cjs
packages/L3-P12/package.json
packages/L3-P12/src/app.js
packages/L3-P12/src/db/associations.js
packages/L3-P12/src/db/connection.js
packages/L3-P12/src/db/index.js
packages/L3-P12/src/db/models/club.js
packages/L3-P12/src/db/models/event.js
packages/L3-P12/src/db/models/member.js
packages/L3-P12/src/db/models/registration.js
packages/L3-P12/src/db/seed.js
packages/L3-P12/src/db/services/enroll.js
packages/L3-P12/src/server.js
packages/L3-P12/tests/config.json
packages/L3-P12/tests/jest.test.mjs
packages/L3-P12/tests/vitest.test.ts
packages/L3-P12/vitest.config.ts
packages/L3-P13/README.md
packages/L3-P13/jest.config.cjs
packages/L3-P13/package.json
packages/L3-P13/src/app.js
packages/L3-P13/src/db/associations.js
packages/L3-P13/src/db/connection.js
packages/L3-P13/src/db/index.js
packages/L3-P13/src/db/models/club.js
packages/L3-P13/src/db/models/event.js
packages/L3-P13/src/db/models/member.js
packages/L3-P13/src/db/models/registration.js
packages/L3-P13/src/db/seed.js
packages/L3-P13/src/db/services/enroll.js
packages/L3-P13/src/server.js
packages/L3-P13/tests/config.json
packages/L3-P13/tests/jest.test.mjs
packages/L3-P13/tests/vitest.test.ts
packages/L3-P13/vitest.config.ts
packages/L3-P14/README.md
packages/L3-P14/jest.config.cjs
packages/L3-P14/package.json
packages/L3-P14/src/app.js
packages/L3-P14/src/db/associations.js
packages/L3-P14/src/db/connection.js
packages/L3-P14/src/db/index.js
packages/L3-P14/src/db/models/club.js
packages/L3-P14/src/db/models/event.js
packages/L3-P14/src/db/models/member.js
packages/L3-P14/src/db/models/registration.js
packages/L3-P14/src/db/seed.js
packages/L3-P14/src/db/services/enroll.js
packages/L3-P14/src/server.js
packages/L3-P14/tests/config.json
packages/L3-P14/tests/jest.test.mjs
packages/L3-P14/tests/vitest.test.ts
packages/L3-P14/vitest.config.ts
packages/L3-P15/README.md
packages/L3-P15/jest.config.cjs
packages/L3-P15/package.json
packages/L3-P15/src/app.js
packages/L3-P15/src/db/associations.js
packages/L3-P15/src/db/connection.js
packages/L3-P15/src/db/index.js
packages/L3-P15/src/db/models/club.js
packages/L3-P15/src/db/models/event.js
packages/L3-P15/src/db/models/member.js
packages/L3-P15/src/db/models/registration.js
packages/L3-P15/src/db/seed.js
packages/L3-P15/src/db/services/enroll.js
packages/L3-P15/src/server.js
packages/L3-P15/tests/config.json
packages/L3-P15/tests/jest.test.mjs
packages/L3-P15/tests/vitest.test.ts
packages/L3-P15/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 137, docs: 45, code: 495, tests: 135.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s9p3-monorepo` type=`module` workspaces=True
  - **Scripturi:**
  - `test` → `pnpm -r --filter ./packages run test`
  - `test:vitest` → `pnpm -r --filter ./packages run test:vitest`
  - `test:jest` → `pnpm -r --filter ./packages run test:jest`
  - **Deps:** 
  - **DevDeps:** pnpm, vitest, jest, supertest, nodemon, express, sequelize, sqlite3, cors
- `packages/L1-P01/package.json`: name=`@l1/p01` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P02/package.json`: name=`@l1/p02` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P03/package.json`: name=`@l1/p03` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P04/package.json`: name=`@l1/p04` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P05/package.json`: name=`@l1/p05` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P06/package.json`: name=`@l1/p06` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P07/package.json`: name=`@l1/p07` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P08/package.json`: name=`@l1/p08` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P09/package.json`: name=`@l1/p09` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P10/package.json`: name=`@l1/p10` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P11/package.json`: name=`@l1/p11` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P12/package.json`: name=`@l1/p12` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P13/package.json`: name=`@l1/p13` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P14/package.json`: name=`@l1/p14` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L1-P15/package.json`: name=`@l1/p15` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P01/package.json`: name=`@l2/p01` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P02/package.json`: name=`@l2/p02` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P03/package.json`: name=`@l2/p03` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P04/package.json`: name=`@l2/p04` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P05/package.json`: name=`@l2/p05` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P06/package.json`: name=`@l2/p06` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P07/package.json`: name=`@l2/p07` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P08/package.json`: name=`@l2/p08` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P09/package.json`: name=`@l2/p09` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P10/package.json`: name=`@l2/p10` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P11/package.json`: name=`@l2/p11` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P12/package.json`: name=`@l2/p12` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P13/package.json`: name=`@l2/p13` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P14/package.json`: name=`@l2/p14` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L2-P15/package.json`: name=`@l2/p15` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P01/package.json`: name=`@l3/p01` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P02/package.json`: name=`@l3/p02` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P03/package.json`: name=`@l3/p03` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P04/package.json`: name=`@l3/p04` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P05/package.json`: name=`@l3/p05` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P06/package.json`: name=`@l3/p06` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P07/package.json`: name=`@l3/p07` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P08/package.json`: name=`@l3/p08` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P09/package.json`: name=`@l3/p09` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P10/package.json`: name=`@l3/p10` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P11/package.json`: name=`@l3/p11` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P12/package.json`: name=`@l3/p12` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P13/package.json`: name=`@l3/p13` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P14/package.json`: name=`@l3/p14` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `packages/L3-P15/package.json`: name=`@l3/p15` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest

### Seminar9_Partea3_p3-standalone.zip

> Structura este mare; se afișează începutul și sfârșitul.

```
L1/L1-P01/solution/README.md
L1/L1-P01/solution/jest.config.cjs
L1/L1-P01/solution/package.json
L1/L1-P01/solution/src/app.js
L1/L1-P01/solution/src/db/associations.js
L1/L1-P01/solution/src/db/connection.js
L1/L1-P01/solution/src/db/index.js
L1/L1-P01/solution/src/db/models/club.js
L1/L1-P01/solution/src/db/models/event.js
L1/L1-P01/solution/src/db/models/member.js
L1/L1-P01/solution/src/db/models/registration.js
L1/L1-P01/solution/src/db/seed.js
L1/L1-P01/solution/src/db/services/enroll.js
L1/L1-P01/solution/src/server.js
L1/L1-P01/solution/tests/config.json
L1/L1-P01/solution/tests/jest.test.mjs
L1/L1-P01/solution/tests/vitest.test.ts
L1/L1-P01/solution/vitest.config.ts
L1/L1-P01/starter/README.md
L1/L1-P01/starter/jest.config.cjs
L1/L1-P01/starter/package.json
L1/L1-P01/starter/src/app.js
L1/L1-P01/starter/src/db/associations.js
L1/L1-P01/starter/src/db/connection.js
L1/L1-P01/starter/src/db/index.js
L1/L1-P01/starter/src/db/models/club.js
L1/L1-P01/starter/src/db/models/event.js
L1/L1-P01/starter/src/db/models/member.js
L1/L1-P01/starter/src/db/models/registration.js
L1/L1-P01/starter/src/db/seed.js
L1/L1-P01/starter/src/db/services/enroll.js
L1/L1-P01/starter/src/server.js
L1/L1-P01/starter/tests/config.json
L1/L1-P01/starter/tests/jest.test.mjs
L1/L1-P01/starter/tests/vitest.test.ts
L1/L1-P01/starter/vitest.config.ts
L1/L1-P02/solution/README.md
L1/L1-P02/solution/jest.config.cjs
L1/L1-P02/solution/package.json
L1/L1-P02/solution/src/app.js
L1/L1-P02/solution/src/db/associations.js
L1/L1-P02/solution/src/db/connection.js
L1/L1-P02/solution/src/db/index.js
L1/L1-P02/solution/src/db/models/club.js
L1/L1-P02/solution/src/db/models/event.js
L1/L1-P02/solution/src/db/models/member.js
L1/L1-P02/solution/src/db/models/registration.js
L1/L1-P02/solution/src/db/seed.js
L1/L1-P02/solution/src/db/services/enroll.js
L1/L1-P02/solution/src/server.js
L1/L1-P02/solution/tests/config.json
L1/L1-P02/solution/tests/jest.test.mjs
L1/L1-P02/solution/tests/vitest.test.ts
L1/L1-P02/solution/vitest.config.ts
L1/L1-P02/starter/README.md
L1/L1-P02/starter/jest.config.cjs
L1/L1-P02/starter/package.json
L1/L1-P02/starter/src/app.js
L1/L1-P02/starter/src/db/associations.js
L1/L1-P02/starter/src/db/connection.js
L1/L1-P02/starter/src/db/index.js
L1/L1-P02/starter/src/db/models/club.js
L1/L1-P02/starter/src/db/models/event.js
L1/L1-P02/starter/src/db/models/member.js
L1/L1-P02/starter/src/db/models/registration.js
L1/L1-P02/starter/src/db/seed.js
L1/L1-P02/starter/src/db/services/enroll.js
L1/L1-P02/starter/src/server.js
L1/L1-P02/starter/tests/config.json
L1/L1-P02/starter/tests/jest.test.mjs
L1/L1-P02/starter/tests/vitest.test.ts
L1/L1-P02/starter/vitest.config.ts
L1/L1-P03/solution/README.md
L1/L1-P03/solution/jest.config.cjs
L1/L1-P03/solution/package.json
L1/L1-P03/solution/src/app.js
L1/L1-P03/solution/src/db/associations.js
L1/L1-P03/solution/src/db/connection.js
L1/L1-P03/solution/src/db/index.js
L1/L1-P03/solution/src/db/models/club.js
L1/L1-P03/solution/src/db/models/event.js
L1/L1-P03/solution/src/db/models/member.js
L1/L1-P03/solution/src/db/models/registration.js
L1/L1-P03/solution/src/db/seed.js
L1/L1-P03/solution/src/db/services/enroll.js
L1/L1-P03/solution/src/server.js
L1/L1-P03/solution/tests/config.json
L1/L1-P03/solution/tests/jest.test.mjs
L1/L1-P03/solution/tests/vitest.test.ts
L1/L1-P03/solution/vitest.config.ts
L1/L1-P03/starter/README.md
L1/L1-P03/starter/jest.config.cjs
L1/L1-P03/starter/package.json
L1/L1-P03/starter/src/app.js
L1/L1-P03/starter/src/db/associations.js
L1/L1-P03/starter/src/db/connection.js
L1/L1-P03/starter/src/db/index.js
L1/L1-P03/starter/src/db/models/club.js
L1/L1-P03/starter/src/db/models/event.js
L1/L1-P03/starter/src/db/models/member.js
L1/L1-P03/starter/src/db/models/registration.js
L1/L1-P03/starter/src/db/seed.js
L1/L1-P03/starter/src/db/services/enroll.js
L1/L1-P03/starter/src/server.js
L1/L1-P03/starter/tests/config.json
L1/L1-P03/starter/tests/jest.test.mjs
L1/L1-P03/starter/tests/vitest.test.ts
L1/L1-P03/starter/vitest.config.ts
L1/L1-P04/solution/README.md
L1/L1-P04/solution/jest.config.cjs
L1/L1-P04/solution/package.json
L1/L1-P04/solution/src/app.js
L1/L1-P04/solution/src/db/associations.js
L1/L1-P04/solution/src/db/connection.js
L1/L1-P04/solution/src/db/index.js
L1/L1-P04/solution/src/db/models/club.js
L1/L1-P04/solution/src/db/models/event.js
L1/L1-P04/solution/src/db/models/member.js
L1/L1-P04/solution/src/db/models/registration.js
L1/L1-P04/solution/src/db/seed.js
L1/L1-P04/solution/src/db/services/enroll.js
L1/L1-P04/solution/src/server.js
L1/L1-P04/solution/tests/config.json
L1/L1-P04/solution/tests/jest.test.mjs
L1/L1-P04/solution/tests/vitest.test.ts
L1/L1-P04/solution/vitest.config.ts
L1/L1-P04/starter/README.md
L1/L1-P04/starter/jest.config.cjs
L1/L1-P04/starter/package.json
L1/L1-P04/starter/src/app.js
L1/L1-P04/starter/src/db/associations.js
L1/L1-P04/starter/src/db/connection.js
L1/L1-P04/starter/src/db/index.js
L1/L1-P04/starter/src/db/models/club.js
L1/L1-P04/starter/src/db/models/event.js
L1/L1-P04/starter/src/db/models/member.js
L1/L1-P04/starter/src/db/models/registration.js
L1/L1-P04/starter/src/db/seed.js
L1/L1-P04/starter/src/db/services/enroll.js
L1/L1-P04/starter/src/server.js
L1/L1-P04/starter/tests/config.json
L1/L1-P04/starter/tests/jest.test.mjs
L1/L1-P04/starter/tests/vitest.test.ts
L1/L1-P04/starter/vitest.config.ts
L1/L1-P05/solution/README.md
L1/L1-P05/solution/jest.config.cjs
L1/L1-P05/solution/package.json
L1/L1-P05/solution/src/app.js
L1/L1-P05/solution/src/db/associations.js
L1/L1-P05/solution/src/db/connection.js
L1/L1-P05/solution/src/db/index.js
L1/L1-P05/solution/src/db/models/club.js
L1/L1-P05/solution/src/db/models/event.js
L1/L1-P05/solution/src/db/models/member.js
L1/L1-P05/solution/src/db/models/registration.js
L1/L1-P05/solution/src/db/seed.js
L1/L1-P05/solution/src/db/services/enroll.js
L1/L1-P05/solution/src/server.js
L1/L1-P05/solution/tests/config.json
L1/L1-P05/solution/tests/jest.test.mjs
L1/L1-P05/solution/tests/vitest.test.ts
L1/L1-P05/solution/vitest.config.ts
L1/L1-P05/starter/README.md
L1/L1-P05/starter/jest.config.cjs
L1/L1-P05/starter/package.json
L1/L1-P05/starter/src/app.js
L1/L1-P05/starter/src/db/associations.js
L1/L1-P05/starter/src/db/connection.js
L1/L1-P05/starter/src/db/index.js
L1/L1-P05/starter/src/db/models/club.js
L1/L1-P05/starter/src/db/models/event.js
L1/L1-P05/starter/src/db/models/member.js
L1/L1-P05/starter/src/db/models/registration.js
L1/L1-P05/starter/src/db/seed.js
L1/L1-P05/starter/src/db/services/enroll.js
L1/L1-P05/starter/src/server.js
L1/L1-P05/starter/tests/config.json
L1/L1-P05/starter/tests/jest.test.mjs
L1/L1-P05/starter/tests/vitest.test.ts
L1/L1-P05/starter/vitest.config.ts
L1/L1-P06/solution/README.md
L1/L1-P06/solution/jest.config.cjs
L1/L1-P06/solution/package.json
L1/L1-P06/solution/src/app.js
L1/L1-P06/solution/src/db/associations.js
L1/L1-P06/solution/src/db/connection.js
L1/L1-P06/solution/src/db/index.js
L1/L1-P06/solution/src/db/models/club.js
L1/L1-P06/solution/src/db/models/event.js
L1/L1-P06/solution/src/db/models/member.js
L1/L1-P06/solution/src/db/models/registration.js
L1/L1-P06/solution/src/db/seed.js
L1/L1-P06/solution/src/db/services/enroll.js
L1/L1-P06/solution/src/server.js
L1/L1-P06/solution/tests/config.json
L1/L1-P06/solution/tests/jest.test.mjs
L1/L1-P06/solution/tests/vitest.test.ts
L1/L1-P06/solution/vitest.config.ts
L1/L1-P06/starter/README.md
L1/L1-P06/starter/jest.config.cjs
L1/L1-P06/starter/package.json
L1/L1-P06/starter/src/app.js
L1/L1-P06/starter/src/db/associations.js
L1/L1-P06/starter/src/db/connection.js
L1/L1-P06/starter/src/db/index.js
L1/L1-P06/starter/src/db/models/club.js
L1/L1-P06/starter/src/db/models/event.js
L1/L1-P06/starter/src/db/models/member.js
L1/L1-P06/starter/src/db/models/registration.js
L1/L1-P06/starter/src/db/seed.js
L1/L1-P06/starter/src/db/services/enroll.js
L1/L1-P06/starter/src/server.js
L1/L1-P06/starter/tests/config.json
L1/L1-P06/starter/tests/jest.test.mjs
L1/L1-P06/starter/tests/vitest.test.ts
L1/L1-P06/starter/vitest.config.ts
L1/L1-P07/solution/README.md
L1/L1-P07/solution/jest.config.cjs
L1/L1-P07/solution/package.json
L1/L1-P07/solution/src/app.js
L1/L1-P07/solution/src/db/associations.js
L1/L1-P07/solution/src/db/connection.js
L1/L1-P07/solution/src/db/index.js
L1/L1-P07/solution/src/db/models/club.js
L1/L1-P07/solution/src/db/models/event.js
L1/L1-P07/solution/src/db/models/member.js
L1/L1-P07/solution/src/db/models/registration.js
L1/L1-P07/solution/src/db/seed.js
L1/L1-P07/solution/src/db/services/enroll.js
L1/L1-P07/solution/src/server.js
L1/L1-P07/solution/tests/config.json
L1/L1-P07/solution/tests/jest.test.mjs
L1/L1-P07/solution/tests/vitest.test.ts
L1/L1-P07/solution/vitest.config.ts
L1/L1-P07/starter/README.md
L1/L1-P07/starter/jest.config.cjs
L1/L1-P07/starter/package.json
L1/L1-P07/starter/src/app.js
L1/L1-P07/starter/src/db/associations.js
L1/L1-P07/starter/src/db/connection.js
L1/L1-P07/starter/src/db/index.js
L1/L1-P07/starter/src/db/models/club.js
L1/L1-P07/starter/src/db/models/event.js
L1/L1-P07/starter/src/db/models/member.js
L1/L1-P07/starter/src/db/models/registration.js
L1/L1-P07/starter/src/db/seed.js
L1/L1-P07/starter/src/db/services/enroll.js
L1/L1-P07/starter/src/server.js
L1/L1-P07/starter/tests/config.json
L1/L1-P07/starter/tests/jest.test.mjs
L1/L1-P07/starter/tests/vitest.test.ts
L1/L1-P07/starter/vitest.config.ts
L1/L1-P08/solution/README.md
L1/L1-P08/solution/jest.config.cjs
L1/L1-P08/solution/package.json
L1/L1-P08/solution/src/app.js
L1/L1-P08/solution/src/db/associations.js
L1/L1-P08/solution/src/db/connection.js
L1/L1-P08/solution/src/db/index.js
L1/L1-P08/solution/src/db/models/club.js
L1/L1-P08/solution/src/db/models/event.js
L1/L1-P08/solution/src/db/models/member.js
L1/L1-P08/solution/src/db/models/registration.js
L1/L1-P08/solution/src/db/seed.js
L1/L1-P08/solution/src/db/services/enroll.js
L1/L1-P08/solution/src/server.js
L1/L1-P08/solution/tests/config.json
L1/L1-P08/solution/tests/jest.test.mjs
L1/L1-P08/solution/tests/vitest.test.ts
L1/L1-P08/solution/vitest.config.ts
L1/L1-P08/starter/README.md
L1/L1-P08/starter/jest.config.cjs
L1/L1-P08/starter/package.json
L1/L1-P08/starter/src/app.js
L1/L1-P08/starter/src/db/associations.js
L1/L1-P08/starter/src/db/connection.js
L1/L1-P08/starter/src/db/index.js
L1/L1-P08/starter/src/db/models/club.js
L1/L1-P08/starter/src/db/models/event.js
L1/L1-P08/starter/src/db/models/member.js
L1/L1-P08/starter/src/db/models/registration.js
L1/L1-P08/starter/src/db/seed.js
L1/L1-P08/starter/src/db/services/enroll.js
L1/L1-P08/starter/src/server.js
L1/L1-P08/starter/tests/config.json
L1/L1-P08/starter/tests/jest.test.mjs
L1/L1-P08/starter/tests/vitest.test.ts
L1/L1-P08/starter/vitest.config.ts
L1/L1-P09/solution/README.md
L1/L1-P09/solution/jest.config.cjs
L1/L1-P09/solution/package.json
L1/L1-P09/solution/src/app.js
L1/L1-P09/solution/src/db/associations.js
L1/L1-P09/solution/src/db/connection.js
L1/L1-P09/solution/src/db/index.js
L1/L1-P09/solution/src/db/models/club.js
L1/L1-P09/solution/src/db/models/event.js
L1/L1-P09/solution/src/db/models/member.js
L1/L1-P09/solution/src/db/models/registration.js
L1/L1-P09/solution/src/db/seed.js
L1/L1-P09/solution/src/db/services/enroll.js
L1/L1-P09/solution/src/server.js
L1/L1-P09/solution/tests/config.json
L1/L1-P09/solution/tests/jest.test.mjs
L1/L1-P09/solution/tests/vitest.test.ts
L1/L1-P09/solution/vitest.config.ts
L1/L1-P09/starter/README.md
L1/L1-P09/starter/jest.config.cjs
L1/L1-P09/starter/package.json
L1/L1-P09/starter/src/app.js
L1/L1-P09/starter/src/db/associations.js
L1/L1-P09/starter/src/db/connection.js
L1/L1-P09/starter/src/db/index.js
L1/L1-P09/starter/src/db/models/club.js
L1/L1-P09/starter/src/db/models/event.js
L1/L1-P09/starter/src/db/models/member.js
L1/L1-P09/starter/src/db/models/registration.js
L1/L1-P09/starter/src/db/seed.js
L1/L1-P09/starter/src/db/services/enroll.js
L1/L1-P09/starter/src/server.js
L1/L1-P09/starter/tests/config.json
L1/L1-P09/starter/tests/jest.test.mjs
L1/L1-P09/starter/tests/vitest.test.ts
L1/L1-P09/starter/vitest.config.ts
L1/L1-P10/solution/README.md
L1/L1-P10/solution/jest.config.cjs
L1/L1-P10/solution/package.json
L1/L1-P10/solution/src/app.js
L1/L1-P10/solution/src/db/associations.js
L1/L1-P10/solution/src/db/connection.js
L1/L1-P10/solution/src/db/index.js
L1/L1-P10/solution/src/db/models/club.js
L1/L1-P10/solution/src/db/models/event.js
L1/L1-P10/solution/src/db/models/member.js
L1/L1-P10/solution/src/db/models/registration.js
L1/L1-P10/solution/src/db/seed.js
L1/L1-P10/solution/src/db/services/enroll.js
L1/L1-P10/solution/src/server.js
L1/L1-P10/solution/tests/config.json
L1/L1-P10/solution/tests/jest.test.mjs
L1/L1-P10/solution/tests/vitest.test.ts
L1/L1-P10/solution/vitest.config.ts
L1/L1-P10/starter/README.md
L1/L1-P10/starter/jest.config.cjs
L1/L1-P10/starter/package.json
L1/L1-P10/starter/src/app.js
L1/L1-P10/starter/src/db/associations.js
L1/L1-P10/starter/src/db/connection.js
L1/L1-P10/starter/src/db/index.js
L1/L1-P10/starter/src/db/models/club.js
L1/L1-P10/starter/src/db/models/event.js
L1/L1-P10/starter/src/db/models/member.js
L1/L1-P10/starter/src/db/models/registration.js
L1/L1-P10/starter/src/db/seed.js
L1/L1-P10/starter/src/db/services/enroll.js
L1/L1-P10/starter/src/server.js
L1/L1-P10/starter/tests/config.json
L1/L1-P10/starter/tests/jest.test.mjs
L1/L1-P10/starter/tests/vitest.test.ts
L1/L1-P10/starter/vitest.config.ts
L1/L1-P11/solution/README.md
L1/L1-P11/solution/jest.config.cjs
L1/L1-P11/solution/package.json
L1/L1-P11/solution/src/app.js
L1/L1-P11/solution/src/db/associations.js
L1/L1-P11/solution/src/db/connection.js
L1/L1-P11/solution/src/db/index.js
L1/L1-P11/solution/src/db/models/club.js
L1/L1-P11/solution/src/db/models/event.js
L1/L1-P11/solution/src/db/models/member.js
L1/L1-P11/solution/src/db/models/registration.js
L1/L1-P11/solution/src/db/seed.js
L1/L1-P11/solution/src/db/services/enroll.js
L1/L1-P11/solution/src/server.js
L1/L1-P11/solution/tests/config.json
L1/L1-P11/solution/tests/jest.test.mjs
L1/L1-P11/solution/tests/vitest.test.ts
L1/L1-P11/solution/vitest.config.ts
L1/L1-P11/starter/README.md
L1/L1-P11/starter/jest.config.cjs
L1/L1-P11/starter/package.json
L1/L1-P11/starter/src/app.js
L1/L1-P11/starter/src/db/associations.js
L1/L1-P11/starter/src/db/connection.js
L1/L1-P11/starter/src/db/index.js
L1/L1-P11/starter/src/db/models/club.js
L1/L1-P11/starter/src/db/models/event.js
L1/L1-P11/starter/src/db/models/member.js
L1/L1-P11/starter/src/db/models/registration.js
L1/L1-P11/starter/src/db/seed.js
L1/L1-P11/starter/src/db/services/enroll.js
L1/L1-P11/starter/src/server.js
L1/L1-P11/starter/tests/config.json
L1/L1-P11/starter/tests/jest.test.mjs
L1/L1-P11/starter/tests/vitest.test.ts
L1/L1-P11/starter/vitest.config.ts
L1/L1-P12/solution/README.md
L1/L1-P12/solution/jest.config.cjs
L1/L1-P12/solution/package.json
L1/L1-P12/solution/src/app.js
L1/L1-P12/solution/src/db/associations.js
L1/L1-P12/solution/src/db/connection.js
L1/L1-P12/solution/src/db/index.js
L1/L1-P12/solution/src/db/models/club.js
L1/L1-P12/solution/src/db/models/event.js
L1/L1-P12/solution/src/db/models/member.js
L1/L1-P12/solution/src/db/models/registration.js
L1/L1-P12/solution/src/db/seed.js
L1/L1-P12/solution/src/db/services/enroll.js
L1/L1-P12/solution/src/server.js
L1/L1-P12/solution/tests/config.json
L1/L1-P12/solution/tests/jest.test.mjs
L1/L1-P12/solution/tests/vitest.test.ts
L1/L1-P12/solution/vitest.config.ts
L1/L1-P12/starter/README.md
L1/L1-P12/starter/jest.config.cjs
L1/L1-P12/starter/package.json
L1/L1-P12/starter/src/app.js
L1/L1-P12/starter/src/db/associations.js
L1/L1-P12/starter/src/db/connection.js
L1/L1-P12/starter/src/db/index.js
L1/L1-P12/starter/src/db/models/club.js
L1/L1-P12/starter/src/db/models/event.js
L1/L1-P12/starter/src/db/models/member.js
L1/L1-P12/starter/src/db/models/registration.js
L1/L1-P12/starter/src/db/seed.js
L1/L1-P12/starter/src/db/services/enroll.js
L1/L1-P12/starter/src/server.js
L1/L1-P12/starter/tests/config.json
L1/L1-P12/starter/tests/jest.test.mjs
L1/L1-P12/starter/tests/vitest.test.ts
L1/L1-P12/starter/vitest.config.ts
L1/L1-P13/solution/README.md
L1/L1-P13/solution/jest.config.cjs
L1/L1-P13/solution/package.json
L1/L1-P13/solution/src/app.js
L1/L1-P13/solution/src/db/associations.js
L1/L1-P13/solution/src/db/connection.js
L1/L1-P13/solution/src/db/index.js
L1/L1-P13/solution/src/db/models/club.js
L1/L1-P13/solution/src/db/models/event.js
L1/L1-P13/solution/src/db/models/member.js
L1/L1-P13/solution/src/db/models/registration.js
L1/L1-P13/solution/src/db/seed.js
L1/L1-P13/solution/src/db/services/enroll.js
L1/L1-P13/solution/src/server.js
L1/L1-P13/solution/tests/config.json
L1/L1-P13/solution/tests/jest.test.mjs
L1/L1-P13/solution/tests/vitest.test.ts
L1/L1-P13/solution/vitest.config.ts
L1/L1-P13/starter/README.md
L1/L1-P13/starter/jest.config.cjs
L1/L1-P13/starter/package.json
L1/L1-P13/starter/src/app.js
L1/L1-P13/starter/src/db/associations.js
L1/L1-P13/starter/src/db/connection.js
L1/L1-P13/starter/src/db/index.js
L1/L1-P13/starter/src/db/models/club.js
L1/L1-P13/starter/src/db/models/event.js
L1/L1-P13/starter/src/db/models/member.js
L1/L1-P13/starter/src/db/models/registration.js
L1/L1-P13/starter/src/db/seed.js
L1/L1-P13/starter/src/db/services/enroll.js
L1/L1-P13/starter/src/server.js
L1/L1-P13/starter/tests/config.json
L1/L1-P13/starter/tests/jest.test.mjs
L1/L1-P13/starter/tests/vitest.test.ts
L1/L1-P13/starter/vitest.config.ts
L1/L1-P14/solution/README.md
L1/L1-P14/solution/jest.config.cjs
L1/L1-P14/solution/package.json
L1/L1-P14/solution/src/app.js
L1/L1-P14/solution/src/db/associations.js
L1/L1-P14/solution/src/db/connection.js
L1/L1-P14/solution/src/db/index.js
L1/L1-P14/solution/src/db/models/club.js
L1/L1-P14/solution/src/db/models/event.js
L1/L1-P14/solution/src/db/models/member.js
L1/L1-P14/solution/src/db/models/registration.js
L1/L1-P14/solution/src/db/seed.js
L1/L1-P14/solution/src/db/services/enroll.js
L1/L1-P14/solution/src/server.js
L1/L1-P14/solution/tests/config.json
L1/L1-P14/solution/tests/jest.test.mjs
L1/L1-P14/solution/tests/vitest.test.ts
L1/L1-P14/solution/vitest.config.ts
L1/L1-P14/starter/README.md
L1/L1-P14/starter/jest.config.cjs
L1/L1-P14/starter/package.json
L1/L1-P14/starter/src/app.js
L1/L1-P14/starter/src/db/associations.js
L1/L1-P14/starter/src/db/connection.js
L1/L1-P14/starter/src/db/index.js
L1/L1-P14/starter/src/db/models/club.js
L1/L1-P14/starter/src/db/models/event.js
L1/L1-P14/starter/src/db/models/member.js
L1/L1-P14/starter/src/db/models/registration.js
L1/L1-P14/starter/src/db/seed.js
L1/L1-P14/starter/src/db/services/enroll.js
L1/L1-P14/starter/src/server.js
L1/L1-P14/starter/tests/config.json
L1/L1-P14/starter/tests/jest.test.mjs
L1/L1-P14/starter/tests/vitest.test.ts
L1/L1-P14/starter/vitest.config.ts
L1/L1-P15/solution/README.md
L1/L1-P15/solution/jest.config.cjs
L1/L1-P15/solution/package.json
L1/L1-P15/solution/src/app.js
L1/L1-P15/solution/src/db/associations.js
L1/L1-P15/solution/src/db/connection.js
L1/L1-P15/solution/src/db/index.js
L1/L1-P15/solution/src/db/models/club.js
L1/L1-P15/solution/src/db/models/event.js
L1/L1-P15/solution/src/db/models/member.js
L1/L1-P15/solution/src/db/models/registration.js
L1/L1-P15/solution/src/db/seed.js
L1/L1-P15/solution/src/db/services/enroll.js
L1/L1-P15/solution/src/server.js
L1/L1-P15/solution/tests/config.json
L1/L1-P15/solution/tests/jest.test.mjs
L1/L1-P15/solution/tests/vitest.test.ts
L1/L1-P15/solution/vitest.config.ts
L1/L1-P15/starter/README.md
L1/L1-P15/starter/jest.config.cjs
L1/L1-P15/starter/package.json
L1/L1-P15/starter/src/app.js
L1/L1-P15/starter/src/db/associations.js
L1/L1-P15/starter/src/db/connection.js
L1/L1-P15/starter/src/db/index.js
L1/L1-P15/starter/src/db/models/club.js
L1/L1-P15/starter/src/db/models/event.js
L1/L1-P15/starter/src/db/models/member.js
L1/L1-P15/starter/src/db/models/registration.js
L1/L1-P15/starter/src/db/seed.js
L1/L1-P15/starter/src/db/services/enroll.js
L1/L1-P15/starter/src/server.js
L1/L1-P15/starter/tests/config.json
L1/L1-P15/starter/tests/jest.test.mjs
L1/L1-P15/starter/tests/vitest.test.ts
L1/L1-P15/starter/vitest.config.ts
L2/L2-P01/solution/README.md
L2/L2-P01/solution/jest.config.cjs
L2/L2-P01/solution/package.json
L2/L2-P01/solution/src/app.js
L2/L2-P01/solution/src/db/associations.js
L2/L2-P01/solution/src/db/connection.js
L2/L2-P01/solution/src/db/index.js
L2/L2-P01/solution/src/db/models/club.js
L2/L2-P01/solution/src/db/models/event.js
L2/L2-P01/solution/src/db/models/member.js
L2/L2-P01/solution/src/db/models/registration.js
L2/L2-P01/solution/src/db/seed.js
L2/L2-P01/solution/src/db/services/enroll.js
L2/L2-P01/solution/src/server.js
L2/L2-P01/solution/tests/config.json
L2/L2-P01/solution/tests/jest.test.mjs
L2/L2-P01/solution/tests/vitest.test.ts
L2/L2-P01/solution/vitest.config.ts
L2/L2-P01/starter/README.md
L2/L2-P01/starter/jest.config.cjs
L2/L2-P01/starter/package.json
L2/L2-P01/starter/src/app.js
L2/L2-P01/starter/src/db/associations.js
L2/L2-P01/starter/src/db/connection.js
L2/L2-P01/starter/src/db/index.js
L2/L2-P01/starter/src/db/models/club.js
L2/L2-P01/starter/src/db/models/event.js
L2/L2-P01/starter/src/db/models/member.js
L2/L2-P01/starter/src/db/models/registration.js
L2/L2-P01/starter/src/db/seed.js
L2/L2-P01/starter/src/db/services/enroll.js
L2/L2-P01/starter/src/server.js
L2/L2-P01/starter/tests/config.json
L2/L2-P01/starter/tests/jest.test.mjs
L2/L2-P01/starter/tests/vitest.test.ts
L2/L2-P01/starter/vitest.config.ts
L2/L2-P02/solution/README.md
L2/L2-P02/solution/jest.config.cjs
L2/L2-P02/solution/package.json
L2/L2-P02/solution/src/app.js
L2/L2-P02/solution/src/db/associations.js
L2/L2-P02/solution/src/db/connection.js
L2/L2-P02/solution/src/db/index.js
L2/L2-P02/solution/src/db/models/club.js
L2/L2-P02/solution/src/db/models/event.js
L2/L2-P02/solution/src/db/models/member.js
L2/L2-P02/solution/src/db/models/registration.js
L2/L2-P02/solution/src/db/seed.js
L2/L2-P02/solution/src/db/services/enroll.js
L2/L2-P02/solution/src/server.js
L2/L2-P02/solution/tests/config.json
L2/L2-P02/solution/tests/jest.test.mjs
L2/L2-P02/solution/tests/vitest.test.ts
L2/L2-P02/solution/vitest.config.ts
L2/L2-P02/starter/README.md
L2/L2-P02/starter/jest.config.cjs
L2/L2-P02/starter/package.json
L2/L2-P02/starter/src/app.js
L2/L2-P02/starter/src/db/associations.js
L2/L2-P02/starter/src/db/connection.js
…
L2/L2-P14/solution/src/db/services/enroll.js
L2/L2-P14/solution/src/server.js
L2/L2-P14/solution/tests/config.json
L2/L2-P14/solution/tests/jest.test.mjs
L2/L2-P14/solution/tests/vitest.test.ts
L2/L2-P14/solution/vitest.config.ts
L2/L2-P14/starter/README.md
L2/L2-P14/starter/jest.config.cjs
L2/L2-P14/starter/package.json
L2/L2-P14/starter/src/app.js
L2/L2-P14/starter/src/db/associations.js
L2/L2-P14/starter/src/db/connection.js
L2/L2-P14/starter/src/db/index.js
L2/L2-P14/starter/src/db/models/club.js
L2/L2-P14/starter/src/db/models/event.js
L2/L2-P14/starter/src/db/models/member.js
L2/L2-P14/starter/src/db/models/registration.js
L2/L2-P14/starter/src/db/seed.js
L2/L2-P14/starter/src/db/services/enroll.js
L2/L2-P14/starter/src/server.js
L2/L2-P14/starter/tests/config.json
L2/L2-P14/starter/tests/jest.test.mjs
L2/L2-P14/starter/tests/vitest.test.ts
L2/L2-P14/starter/vitest.config.ts
L2/L2-P15/solution/README.md
L2/L2-P15/solution/jest.config.cjs
L2/L2-P15/solution/package.json
L2/L2-P15/solution/src/app.js
L2/L2-P15/solution/src/db/associations.js
L2/L2-P15/solution/src/db/connection.js
L2/L2-P15/solution/src/db/index.js
L2/L2-P15/solution/src/db/models/club.js
L2/L2-P15/solution/src/db/models/event.js
L2/L2-P15/solution/src/db/models/member.js
L2/L2-P15/solution/src/db/models/registration.js
L2/L2-P15/solution/src/db/seed.js
L2/L2-P15/solution/src/db/services/enroll.js
L2/L2-P15/solution/src/server.js
L2/L2-P15/solution/tests/config.json
L2/L2-P15/solution/tests/jest.test.mjs
L2/L2-P15/solution/tests/vitest.test.ts
L2/L2-P15/solution/vitest.config.ts
L2/L2-P15/starter/README.md
L2/L2-P15/starter/jest.config.cjs
L2/L2-P15/starter/package.json
L2/L2-P15/starter/src/app.js
L2/L2-P15/starter/src/db/associations.js
L2/L2-P15/starter/src/db/connection.js
L2/L2-P15/starter/src/db/index.js
L2/L2-P15/starter/src/db/models/club.js
L2/L2-P15/starter/src/db/models/event.js
L2/L2-P15/starter/src/db/models/member.js
L2/L2-P15/starter/src/db/models/registration.js
L2/L2-P15/starter/src/db/seed.js
L2/L2-P15/starter/src/db/services/enroll.js
L2/L2-P15/starter/src/server.js
L2/L2-P15/starter/tests/config.json
L2/L2-P15/starter/tests/jest.test.mjs
L2/L2-P15/starter/tests/vitest.test.ts
L2/L2-P15/starter/vitest.config.ts
L3/L3-P01/solution/README.md
L3/L3-P01/solution/jest.config.cjs
L3/L3-P01/solution/package.json
L3/L3-P01/solution/src/app.js
L3/L3-P01/solution/src/db/associations.js
L3/L3-P01/solution/src/db/connection.js
L3/L3-P01/solution/src/db/index.js
L3/L3-P01/solution/src/db/models/club.js
L3/L3-P01/solution/src/db/models/event.js
L3/L3-P01/solution/src/db/models/member.js
L3/L3-P01/solution/src/db/models/registration.js
L3/L3-P01/solution/src/db/seed.js
L3/L3-P01/solution/src/db/services/enroll.js
L3/L3-P01/solution/src/server.js
L3/L3-P01/solution/tests/config.json
L3/L3-P01/solution/tests/jest.test.mjs
L3/L3-P01/solution/tests/vitest.test.ts
L3/L3-P01/solution/vitest.config.ts
L3/L3-P01/starter/README.md
L3/L3-P01/starter/jest.config.cjs
L3/L3-P01/starter/package.json
L3/L3-P01/starter/src/app.js
L3/L3-P01/starter/src/db/associations.js
L3/L3-P01/starter/src/db/connection.js
L3/L3-P01/starter/src/db/index.js
L3/L3-P01/starter/src/db/models/club.js
L3/L3-P01/starter/src/db/models/event.js
L3/L3-P01/starter/src/db/models/member.js
L3/L3-P01/starter/src/db/models/registration.js
L3/L3-P01/starter/src/db/seed.js
L3/L3-P01/starter/src/db/services/enroll.js
L3/L3-P01/starter/src/server.js
L3/L3-P01/starter/tests/config.json
L3/L3-P01/starter/tests/jest.test.mjs
L3/L3-P01/starter/tests/vitest.test.ts
L3/L3-P01/starter/vitest.config.ts
L3/L3-P02/solution/README.md
L3/L3-P02/solution/jest.config.cjs
L3/L3-P02/solution/package.json
L3/L3-P02/solution/src/app.js
L3/L3-P02/solution/src/db/associations.js
L3/L3-P02/solution/src/db/connection.js
L3/L3-P02/solution/src/db/index.js
L3/L3-P02/solution/src/db/models/club.js
L3/L3-P02/solution/src/db/models/event.js
L3/L3-P02/solution/src/db/models/member.js
L3/L3-P02/solution/src/db/models/registration.js
L3/L3-P02/solution/src/db/seed.js
L3/L3-P02/solution/src/db/services/enroll.js
L3/L3-P02/solution/src/server.js
L3/L3-P02/solution/tests/config.json
L3/L3-P02/solution/tests/jest.test.mjs
L3/L3-P02/solution/tests/vitest.test.ts
L3/L3-P02/solution/vitest.config.ts
L3/L3-P02/starter/README.md
L3/L3-P02/starter/jest.config.cjs
L3/L3-P02/starter/package.json
L3/L3-P02/starter/src/app.js
L3/L3-P02/starter/src/db/associations.js
L3/L3-P02/starter/src/db/connection.js
L3/L3-P02/starter/src/db/index.js
L3/L3-P02/starter/src/db/models/club.js
L3/L3-P02/starter/src/db/models/event.js
L3/L3-P02/starter/src/db/models/member.js
L3/L3-P02/starter/src/db/models/registration.js
L3/L3-P02/starter/src/db/seed.js
L3/L3-P02/starter/src/db/services/enroll.js
L3/L3-P02/starter/src/server.js
L3/L3-P02/starter/tests/config.json
L3/L3-P02/starter/tests/jest.test.mjs
L3/L3-P02/starter/tests/vitest.test.ts
L3/L3-P02/starter/vitest.config.ts
L3/L3-P03/solution/README.md
L3/L3-P03/solution/jest.config.cjs
L3/L3-P03/solution/package.json
L3/L3-P03/solution/src/app.js
L3/L3-P03/solution/src/db/associations.js
L3/L3-P03/solution/src/db/connection.js
L3/L3-P03/solution/src/db/index.js
L3/L3-P03/solution/src/db/models/club.js
L3/L3-P03/solution/src/db/models/event.js
L3/L3-P03/solution/src/db/models/member.js
L3/L3-P03/solution/src/db/models/registration.js
L3/L3-P03/solution/src/db/seed.js
L3/L3-P03/solution/src/db/services/enroll.js
L3/L3-P03/solution/src/server.js
L3/L3-P03/solution/tests/config.json
L3/L3-P03/solution/tests/jest.test.mjs
L3/L3-P03/solution/tests/vitest.test.ts
L3/L3-P03/solution/vitest.config.ts
L3/L3-P03/starter/README.md
L3/L3-P03/starter/jest.config.cjs
L3/L3-P03/starter/package.json
L3/L3-P03/starter/src/app.js
L3/L3-P03/starter/src/db/associations.js
L3/L3-P03/starter/src/db/connection.js
L3/L3-P03/starter/src/db/index.js
L3/L3-P03/starter/src/db/models/club.js
L3/L3-P03/starter/src/db/models/event.js
L3/L3-P03/starter/src/db/models/member.js
L3/L3-P03/starter/src/db/models/registration.js
L3/L3-P03/starter/src/db/seed.js
L3/L3-P03/starter/src/db/services/enroll.js
L3/L3-P03/starter/src/server.js
L3/L3-P03/starter/tests/config.json
L3/L3-P03/starter/tests/jest.test.mjs
L3/L3-P03/starter/tests/vitest.test.ts
L3/L3-P03/starter/vitest.config.ts
L3/L3-P04/solution/README.md
L3/L3-P04/solution/jest.config.cjs
L3/L3-P04/solution/package.json
L3/L3-P04/solution/src/app.js
L3/L3-P04/solution/src/db/associations.js
L3/L3-P04/solution/src/db/connection.js
L3/L3-P04/solution/src/db/index.js
L3/L3-P04/solution/src/db/models/club.js
L3/L3-P04/solution/src/db/models/event.js
L3/L3-P04/solution/src/db/models/member.js
L3/L3-P04/solution/src/db/models/registration.js
L3/L3-P04/solution/src/db/seed.js
L3/L3-P04/solution/src/db/services/enroll.js
L3/L3-P04/solution/src/server.js
L3/L3-P04/solution/tests/config.json
L3/L3-P04/solution/tests/jest.test.mjs
L3/L3-P04/solution/tests/vitest.test.ts
L3/L3-P04/solution/vitest.config.ts
L3/L3-P04/starter/README.md
L3/L3-P04/starter/jest.config.cjs
L3/L3-P04/starter/package.json
L3/L3-P04/starter/src/app.js
L3/L3-P04/starter/src/db/associations.js
L3/L3-P04/starter/src/db/connection.js
L3/L3-P04/starter/src/db/index.js
L3/L3-P04/starter/src/db/models/club.js
L3/L3-P04/starter/src/db/models/event.js
L3/L3-P04/starter/src/db/models/member.js
L3/L3-P04/starter/src/db/models/registration.js
L3/L3-P04/starter/src/db/seed.js
L3/L3-P04/starter/src/db/services/enroll.js
L3/L3-P04/starter/src/server.js
L3/L3-P04/starter/tests/config.json
L3/L3-P04/starter/tests/jest.test.mjs
L3/L3-P04/starter/tests/vitest.test.ts
L3/L3-P04/starter/vitest.config.ts
L3/L3-P05/solution/README.md
L3/L3-P05/solution/jest.config.cjs
L3/L3-P05/solution/package.json
L3/L3-P05/solution/src/app.js
L3/L3-P05/solution/src/db/associations.js
L3/L3-P05/solution/src/db/connection.js
L3/L3-P05/solution/src/db/index.js
L3/L3-P05/solution/src/db/models/club.js
L3/L3-P05/solution/src/db/models/event.js
L3/L3-P05/solution/src/db/models/member.js
L3/L3-P05/solution/src/db/models/registration.js
L3/L3-P05/solution/src/db/seed.js
L3/L3-P05/solution/src/db/services/enroll.js
L3/L3-P05/solution/src/server.js
L3/L3-P05/solution/tests/config.json
L3/L3-P05/solution/tests/jest.test.mjs
L3/L3-P05/solution/tests/vitest.test.ts
L3/L3-P05/solution/vitest.config.ts
L3/L3-P05/starter/README.md
L3/L3-P05/starter/jest.config.cjs
L3/L3-P05/starter/package.json
L3/L3-P05/starter/src/app.js
L3/L3-P05/starter/src/db/associations.js
L3/L3-P05/starter/src/db/connection.js
L3/L3-P05/starter/src/db/index.js
L3/L3-P05/starter/src/db/models/club.js
L3/L3-P05/starter/src/db/models/event.js
L3/L3-P05/starter/src/db/models/member.js
L3/L3-P05/starter/src/db/models/registration.js
L3/L3-P05/starter/src/db/seed.js
L3/L3-P05/starter/src/db/services/enroll.js
L3/L3-P05/starter/src/server.js
L3/L3-P05/starter/tests/config.json
L3/L3-P05/starter/tests/jest.test.mjs
L3/L3-P05/starter/tests/vitest.test.ts
L3/L3-P05/starter/vitest.config.ts
L3/L3-P06/solution/README.md
L3/L3-P06/solution/jest.config.cjs
L3/L3-P06/solution/package.json
L3/L3-P06/solution/src/app.js
L3/L3-P06/solution/src/db/associations.js
L3/L3-P06/solution/src/db/connection.js
L3/L3-P06/solution/src/db/index.js
L3/L3-P06/solution/src/db/models/club.js
L3/L3-P06/solution/src/db/models/event.js
L3/L3-P06/solution/src/db/models/member.js
L3/L3-P06/solution/src/db/models/registration.js
L3/L3-P06/solution/src/db/seed.js
L3/L3-P06/solution/src/db/services/enroll.js
L3/L3-P06/solution/src/server.js
L3/L3-P06/solution/tests/config.json
L3/L3-P06/solution/tests/jest.test.mjs
L3/L3-P06/solution/tests/vitest.test.ts
L3/L3-P06/solution/vitest.config.ts
L3/L3-P06/starter/README.md
L3/L3-P06/starter/jest.config.cjs
L3/L3-P06/starter/package.json
L3/L3-P06/starter/src/app.js
L3/L3-P06/starter/src/db/associations.js
L3/L3-P06/starter/src/db/connection.js
L3/L3-P06/starter/src/db/index.js
L3/L3-P06/starter/src/db/models/club.js
L3/L3-P06/starter/src/db/models/event.js
L3/L3-P06/starter/src/db/models/member.js
L3/L3-P06/starter/src/db/models/registration.js
L3/L3-P06/starter/src/db/seed.js
L3/L3-P06/starter/src/db/services/enroll.js
L3/L3-P06/starter/src/server.js
L3/L3-P06/starter/tests/config.json
L3/L3-P06/starter/tests/jest.test.mjs
L3/L3-P06/starter/tests/vitest.test.ts
L3/L3-P06/starter/vitest.config.ts
L3/L3-P07/solution/README.md
L3/L3-P07/solution/jest.config.cjs
L3/L3-P07/solution/package.json
L3/L3-P07/solution/src/app.js
L3/L3-P07/solution/src/db/associations.js
L3/L3-P07/solution/src/db/connection.js
L3/L3-P07/solution/src/db/index.js
L3/L3-P07/solution/src/db/models/club.js
L3/L3-P07/solution/src/db/models/event.js
L3/L3-P07/solution/src/db/models/member.js
L3/L3-P07/solution/src/db/models/registration.js
L3/L3-P07/solution/src/db/seed.js
L3/L3-P07/solution/src/db/services/enroll.js
L3/L3-P07/solution/src/server.js
L3/L3-P07/solution/tests/config.json
L3/L3-P07/solution/tests/jest.test.mjs
L3/L3-P07/solution/tests/vitest.test.ts
L3/L3-P07/solution/vitest.config.ts
L3/L3-P07/starter/README.md
L3/L3-P07/starter/jest.config.cjs
L3/L3-P07/starter/package.json
L3/L3-P07/starter/src/app.js
L3/L3-P07/starter/src/db/associations.js
L3/L3-P07/starter/src/db/connection.js
L3/L3-P07/starter/src/db/index.js
L3/L3-P07/starter/src/db/models/club.js
L3/L3-P07/starter/src/db/models/event.js
L3/L3-P07/starter/src/db/models/member.js
L3/L3-P07/starter/src/db/models/registration.js
L3/L3-P07/starter/src/db/seed.js
L3/L3-P07/starter/src/db/services/enroll.js
L3/L3-P07/starter/src/server.js
L3/L3-P07/starter/tests/config.json
L3/L3-P07/starter/tests/jest.test.mjs
L3/L3-P07/starter/tests/vitest.test.ts
L3/L3-P07/starter/vitest.config.ts
L3/L3-P08/solution/README.md
L3/L3-P08/solution/jest.config.cjs
L3/L3-P08/solution/package.json
L3/L3-P08/solution/src/app.js
L3/L3-P08/solution/src/db/associations.js
L3/L3-P08/solution/src/db/connection.js
L3/L3-P08/solution/src/db/index.js
L3/L3-P08/solution/src/db/models/club.js
L3/L3-P08/solution/src/db/models/event.js
L3/L3-P08/solution/src/db/models/member.js
L3/L3-P08/solution/src/db/models/registration.js
L3/L3-P08/solution/src/db/seed.js
L3/L3-P08/solution/src/db/services/enroll.js
L3/L3-P08/solution/src/server.js
L3/L3-P08/solution/tests/config.json
L3/L3-P08/solution/tests/jest.test.mjs
L3/L3-P08/solution/tests/vitest.test.ts
L3/L3-P08/solution/vitest.config.ts
L3/L3-P08/starter/README.md
L3/L3-P08/starter/jest.config.cjs
L3/L3-P08/starter/package.json
L3/L3-P08/starter/src/app.js
L3/L3-P08/starter/src/db/associations.js
L3/L3-P08/starter/src/db/connection.js
L3/L3-P08/starter/src/db/index.js
L3/L3-P08/starter/src/db/models/club.js
L3/L3-P08/starter/src/db/models/event.js
L3/L3-P08/starter/src/db/models/member.js
L3/L3-P08/starter/src/db/models/registration.js
L3/L3-P08/starter/src/db/seed.js
L3/L3-P08/starter/src/db/services/enroll.js
L3/L3-P08/starter/src/server.js
L3/L3-P08/starter/tests/config.json
L3/L3-P08/starter/tests/jest.test.mjs
L3/L3-P08/starter/tests/vitest.test.ts
L3/L3-P08/starter/vitest.config.ts
L3/L3-P09/solution/README.md
L3/L3-P09/solution/jest.config.cjs
L3/L3-P09/solution/package.json
L3/L3-P09/solution/src/app.js
L3/L3-P09/solution/src/db/associations.js
L3/L3-P09/solution/src/db/connection.js
L3/L3-P09/solution/src/db/index.js
L3/L3-P09/solution/src/db/models/club.js
L3/L3-P09/solution/src/db/models/event.js
L3/L3-P09/solution/src/db/models/member.js
L3/L3-P09/solution/src/db/models/registration.js
L3/L3-P09/solution/src/db/seed.js
L3/L3-P09/solution/src/db/services/enroll.js
L3/L3-P09/solution/src/server.js
L3/L3-P09/solution/tests/config.json
L3/L3-P09/solution/tests/jest.test.mjs
L3/L3-P09/solution/tests/vitest.test.ts
L3/L3-P09/solution/vitest.config.ts
L3/L3-P09/starter/README.md
L3/L3-P09/starter/jest.config.cjs
L3/L3-P09/starter/package.json
L3/L3-P09/starter/src/app.js
L3/L3-P09/starter/src/db/associations.js
L3/L3-P09/starter/src/db/connection.js
L3/L3-P09/starter/src/db/index.js
L3/L3-P09/starter/src/db/models/club.js
L3/L3-P09/starter/src/db/models/event.js
L3/L3-P09/starter/src/db/models/member.js
L3/L3-P09/starter/src/db/models/registration.js
L3/L3-P09/starter/src/db/seed.js
L3/L3-P09/starter/src/db/services/enroll.js
L3/L3-P09/starter/src/server.js
L3/L3-P09/starter/tests/config.json
L3/L3-P09/starter/tests/jest.test.mjs
L3/L3-P09/starter/tests/vitest.test.ts
L3/L3-P09/starter/vitest.config.ts
L3/L3-P10/solution/README.md
L3/L3-P10/solution/jest.config.cjs
L3/L3-P10/solution/package.json
L3/L3-P10/solution/src/app.js
L3/L3-P10/solution/src/db/associations.js
L3/L3-P10/solution/src/db/connection.js
L3/L3-P10/solution/src/db/index.js
L3/L3-P10/solution/src/db/models/club.js
L3/L3-P10/solution/src/db/models/event.js
L3/L3-P10/solution/src/db/models/member.js
L3/L3-P10/solution/src/db/models/registration.js
L3/L3-P10/solution/src/db/seed.js
L3/L3-P10/solution/src/db/services/enroll.js
L3/L3-P10/solution/src/server.js
L3/L3-P10/solution/tests/config.json
L3/L3-P10/solution/tests/jest.test.mjs
L3/L3-P10/solution/tests/vitest.test.ts
L3/L3-P10/solution/vitest.config.ts
L3/L3-P10/starter/README.md
L3/L3-P10/starter/jest.config.cjs
L3/L3-P10/starter/package.json
L3/L3-P10/starter/src/app.js
L3/L3-P10/starter/src/db/associations.js
L3/L3-P10/starter/src/db/connection.js
L3/L3-P10/starter/src/db/index.js
L3/L3-P10/starter/src/db/models/club.js
L3/L3-P10/starter/src/db/models/event.js
L3/L3-P10/starter/src/db/models/member.js
L3/L3-P10/starter/src/db/models/registration.js
L3/L3-P10/starter/src/db/seed.js
L3/L3-P10/starter/src/db/services/enroll.js
L3/L3-P10/starter/src/server.js
L3/L3-P10/starter/tests/config.json
L3/L3-P10/starter/tests/jest.test.mjs
L3/L3-P10/starter/tests/vitest.test.ts
L3/L3-P10/starter/vitest.config.ts
L3/L3-P11/solution/README.md
L3/L3-P11/solution/jest.config.cjs
L3/L3-P11/solution/package.json
L3/L3-P11/solution/src/app.js
L3/L3-P11/solution/src/db/associations.js
L3/L3-P11/solution/src/db/connection.js
L3/L3-P11/solution/src/db/index.js
L3/L3-P11/solution/src/db/models/club.js
L3/L3-P11/solution/src/db/models/event.js
L3/L3-P11/solution/src/db/models/member.js
L3/L3-P11/solution/src/db/models/registration.js
L3/L3-P11/solution/src/db/seed.js
L3/L3-P11/solution/src/db/services/enroll.js
L3/L3-P11/solution/src/server.js
L3/L3-P11/solution/tests/config.json
L3/L3-P11/solution/tests/jest.test.mjs
L3/L3-P11/solution/tests/vitest.test.ts
L3/L3-P11/solution/vitest.config.ts
L3/L3-P11/starter/README.md
L3/L3-P11/starter/jest.config.cjs
L3/L3-P11/starter/package.json
L3/L3-P11/starter/src/app.js
L3/L3-P11/starter/src/db/associations.js
L3/L3-P11/starter/src/db/connection.js
L3/L3-P11/starter/src/db/index.js
L3/L3-P11/starter/src/db/models/club.js
L3/L3-P11/starter/src/db/models/event.js
L3/L3-P11/starter/src/db/models/member.js
L3/L3-P11/starter/src/db/models/registration.js
L3/L3-P11/starter/src/db/seed.js
L3/L3-P11/starter/src/db/services/enroll.js
L3/L3-P11/starter/src/server.js
L3/L3-P11/starter/tests/config.json
L3/L3-P11/starter/tests/jest.test.mjs
L3/L3-P11/starter/tests/vitest.test.ts
L3/L3-P11/starter/vitest.config.ts
L3/L3-P12/solution/README.md
L3/L3-P12/solution/jest.config.cjs
L3/L3-P12/solution/package.json
L3/L3-P12/solution/src/app.js
L3/L3-P12/solution/src/db/associations.js
L3/L3-P12/solution/src/db/connection.js
L3/L3-P12/solution/src/db/index.js
L3/L3-P12/solution/src/db/models/club.js
L3/L3-P12/solution/src/db/models/event.js
L3/L3-P12/solution/src/db/models/member.js
L3/L3-P12/solution/src/db/models/registration.js
L3/L3-P12/solution/src/db/seed.js
L3/L3-P12/solution/src/db/services/enroll.js
L3/L3-P12/solution/src/server.js
L3/L3-P12/solution/tests/config.json
L3/L3-P12/solution/tests/jest.test.mjs
L3/L3-P12/solution/tests/vitest.test.ts
L3/L3-P12/solution/vitest.config.ts
L3/L3-P12/starter/README.md
L3/L3-P12/starter/jest.config.cjs
L3/L3-P12/starter/package.json
L3/L3-P12/starter/src/app.js
L3/L3-P12/starter/src/db/associations.js
L3/L3-P12/starter/src/db/connection.js
L3/L3-P12/starter/src/db/index.js
L3/L3-P12/starter/src/db/models/club.js
L3/L3-P12/starter/src/db/models/event.js
L3/L3-P12/starter/src/db/models/member.js
L3/L3-P12/starter/src/db/models/registration.js
L3/L3-P12/starter/src/db/seed.js
L3/L3-P12/starter/src/db/services/enroll.js
L3/L3-P12/starter/src/server.js
L3/L3-P12/starter/tests/config.json
L3/L3-P12/starter/tests/jest.test.mjs
L3/L3-P12/starter/tests/vitest.test.ts
L3/L3-P12/starter/vitest.config.ts
L3/L3-P13/solution/README.md
L3/L3-P13/solution/jest.config.cjs
L3/L3-P13/solution/package.json
L3/L3-P13/solution/src/app.js
L3/L3-P13/solution/src/db/associations.js
L3/L3-P13/solution/src/db/connection.js
L3/L3-P13/solution/src/db/index.js
L3/L3-P13/solution/src/db/models/club.js
L3/L3-P13/solution/src/db/models/event.js
L3/L3-P13/solution/src/db/models/member.js
L3/L3-P13/solution/src/db/models/registration.js
L3/L3-P13/solution/src/db/seed.js
L3/L3-P13/solution/src/db/services/enroll.js
L3/L3-P13/solution/src/server.js
L3/L3-P13/solution/tests/config.json
L3/L3-P13/solution/tests/jest.test.mjs
L3/L3-P13/solution/tests/vitest.test.ts
L3/L3-P13/solution/vitest.config.ts
L3/L3-P13/starter/README.md
L3/L3-P13/starter/jest.config.cjs
L3/L3-P13/starter/package.json
L3/L3-P13/starter/src/app.js
L3/L3-P13/starter/src/db/associations.js
L3/L3-P13/starter/src/db/connection.js
L3/L3-P13/starter/src/db/index.js
L3/L3-P13/starter/src/db/models/club.js
L3/L3-P13/starter/src/db/models/event.js
L3/L3-P13/starter/src/db/models/member.js
L3/L3-P13/starter/src/db/models/registration.js
L3/L3-P13/starter/src/db/seed.js
L3/L3-P13/starter/src/db/services/enroll.js
L3/L3-P13/starter/src/server.js
L3/L3-P13/starter/tests/config.json
L3/L3-P13/starter/tests/jest.test.mjs
L3/L3-P13/starter/tests/vitest.test.ts
L3/L3-P13/starter/vitest.config.ts
L3/L3-P14/solution/README.md
L3/L3-P14/solution/jest.config.cjs
L3/L3-P14/solution/package.json
L3/L3-P14/solution/src/app.js
L3/L3-P14/solution/src/db/associations.js
L3/L3-P14/solution/src/db/connection.js
L3/L3-P14/solution/src/db/index.js
L3/L3-P14/solution/src/db/models/club.js
L3/L3-P14/solution/src/db/models/event.js
L3/L3-P14/solution/src/db/models/member.js
L3/L3-P14/solution/src/db/models/registration.js
L3/L3-P14/solution/src/db/seed.js
L3/L3-P14/solution/src/db/services/enroll.js
L3/L3-P14/solution/src/server.js
L3/L3-P14/solution/tests/config.json
L3/L3-P14/solution/tests/jest.test.mjs
L3/L3-P14/solution/tests/vitest.test.ts
L3/L3-P14/solution/vitest.config.ts
L3/L3-P14/starter/README.md
L3/L3-P14/starter/jest.config.cjs
L3/L3-P14/starter/package.json
L3/L3-P14/starter/src/app.js
L3/L3-P14/starter/src/db/associations.js
L3/L3-P14/starter/src/db/connection.js
L3/L3-P14/starter/src/db/index.js
L3/L3-P14/starter/src/db/models/club.js
L3/L3-P14/starter/src/db/models/event.js
L3/L3-P14/starter/src/db/models/member.js
L3/L3-P14/starter/src/db/models/registration.js
L3/L3-P14/starter/src/db/seed.js
L3/L3-P14/starter/src/db/services/enroll.js
L3/L3-P14/starter/src/server.js
L3/L3-P14/starter/tests/config.json
L3/L3-P14/starter/tests/jest.test.mjs
L3/L3-P14/starter/tests/vitest.test.ts
L3/L3-P14/starter/vitest.config.ts
L3/L3-P15/solution/README.md
L3/L3-P15/solution/jest.config.cjs
L3/L3-P15/solution/package.json
L3/L3-P15/solution/src/app.js
L3/L3-P15/solution/src/db/associations.js
L3/L3-P15/solution/src/db/connection.js
L3/L3-P15/solution/src/db/index.js
L3/L3-P15/solution/src/db/models/club.js
L3/L3-P15/solution/src/db/models/event.js
L3/L3-P15/solution/src/db/models/member.js
L3/L3-P15/solution/src/db/models/registration.js
L3/L3-P15/solution/src/db/seed.js
L3/L3-P15/solution/src/db/services/enroll.js
L3/L3-P15/solution/src/server.js
L3/L3-P15/solution/tests/config.json
L3/L3-P15/solution/tests/jest.test.mjs
L3/L3-P15/solution/tests/vitest.test.ts
L3/L3-P15/solution/vitest.config.ts
L3/L3-P15/starter/README.md
L3/L3-P15/starter/jest.config.cjs
L3/L3-P15/starter/package.json
L3/L3-P15/starter/src/app.js
L3/L3-P15/starter/src/db/associations.js
L3/L3-P15/starter/src/db/connection.js
L3/L3-P15/starter/src/db/index.js
L3/L3-P15/starter/src/db/models/club.js
L3/L3-P15/starter/src/db/models/event.js
L3/L3-P15/starter/src/db/models/member.js
L3/L3-P15/starter/src/db/models/registration.js
L3/L3-P15/starter/src/db/seed.js
L3/L3-P15/starter/src/db/services/enroll.js
L3/L3-P15/starter/src/server.js
L3/L3-P15/starter/tests/config.json
L3/L3-P15/starter/tests/jest.test.mjs
L3/L3-P15/starter/tests/vitest.test.ts
L3/L3-P15/starter/vitest.config.ts
```

**Variante detectate:** solution: 810, starter: 810.

**Categorii de fișiere:** config: 270, docs: 90, code: 990, tests: 270.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `L1/L1-P01/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P01/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P02/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P02/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P03/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P03/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P04/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P04/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P05/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P05/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P06/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P06/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P07/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P07/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P08/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P08/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P09/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P09/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P10/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P10/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P11/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P11/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P12/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P12/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P13/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P13/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P14/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P14/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P15/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L1/L1-P15/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P01/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P01/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P02/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P02/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P03/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P03/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P04/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P04/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P05/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P05/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P06/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P06/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P07/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P07/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P08/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P08/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P09/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P09/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P10/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P10/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P11/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P11/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P12/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P12/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P13/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P13/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P14/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P14/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P15/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L2/L2-P15/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P01/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P01/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P02/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P02/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P03/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P03/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P04/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P04/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P05/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P05/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P06/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P06/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P07/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P07/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P08/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P08/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P09/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P09/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P10/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P10/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P11/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P11/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P12/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P12/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P13/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P13/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P14/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P14/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P15/starter/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest
- `L3/L3-P15/solution/package.json`: name=`s9p3-project` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/server.js`
  - `start` → `node src/server.js`
  - `test:vitest` → `vitest run`
  - `test:jest` → `NODE_OPTIONS=--experimental-vm-modules jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** cors, express, sequelize, sqlite3
  - **DevDeps:** jest, nodemon, supertest, vitest

### Seminar9_Partea3_p3-READMEs.zip

```
L1-P01.README.md
L1-P02.README.md
L1-P03.README.md
L1-P04.README.md
L1-P05.README.md
L1-P06.README.md
L1-P07.README.md
L1-P08.README.md
L1-P09.README.md
L1-P10.README.md
L1-P11.README.md
L1-P12.README.md
L1-P13.README.md
L1-P14.README.md
L1-P15.README.md
L2-P01.README.md
L2-P02.README.md
L2-P03.README.md
L2-P04.README.md
L2-P05.README.md
L2-P06.README.md
L2-P07.README.md
L2-P08.README.md
L2-P09.README.md
L2-P10.README.md
L2-P11.README.md
L2-P12.README.md
L2-P13.README.md
L2-P14.README.md
L2-P15.README.md
L3-P01.README.md
L3-P02.README.md
L3-P03.README.md
L3-P04.README.md
L3-P05.README.md
L3-P06.README.md
L3-P07.README.md
L3-P08.README.md
L3-P09.README.md
L3-P10.README.md
L3-P11.README.md
L3-P12.README.md
L3-P13.README.md
L3-P14.README.md
L3-P15.README.md
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** docs: 45.

## 2. Sinteza documentelor DOCX (teorie ↔ laborator ↔ proiecte)

### Seminar9_Partea1_Teorie.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 9 — Persistență SQLite/Sequelize — Partea 1 (Teorie)
- HOOK: De la fișiere JSON și foi de calcul la o bază relațională cu SQLite + Sequelize

### Seminar9_Partea2_Laborator.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 9 — Persistență SQLite/Sequelize — Partea 2 (Laborator extins)
- Context și obiectiv general
---------------------------
Această parte a seminarului transformă teoria din Partea 1 într‑un laborator aplicat, integral executabil, organizat pe etape progresive. Vei porni de la un proiect Node.js + Express + Sequelize configurat pentru SQLite (fișier în modul development și „sqlite::memory:” în test), vei defini modele și asocieri, vei crea și verifica tranzacții, vei testa integritatea referențială (FK) și vei compara încărcarea „lazy” cu „eager” (anti‑N+1). Laboratorul include un „worksheet” (cerință + checklist) pentru fiecare etapă, „starter code” pregătit și **teste automate** în **Vitest** și **Jest** rulate side‑by‑side.
- Principiul de lucru este **VSL (Very Short Loop)**: implementezi un pas mic, rulezi testele, verifici feedback‑ul, ajustezi. Orice bloc de cod sau comandă CLI este prezentat în blocuri separate, precedate și urmate de explicații. În plus, ofer prompturi concrete pentru **GitHub Copilot** (sau alt LLM) în dreptul activităților repetitive sau pretabile la completare automată (modele, migrații, teste).

### Seminar9_Partea3_Arhive_Ghid.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhive Partea 3 (Seminarul 9)
- Ce conțin arhivele
- • **s9p3-standalone.zip** — 45 proiecte, fiecare cu `starter/` și `solution/`, teste Vitest & Jest, README per proiect.

### Seminar9_Partea3_Proiecte_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 9 — Partea 3: Proiecte/teme (45 proiecte)
- Această parte reunește **45 de proiecte** împărțite pe **L1/L2/L3** (fundamentale/intermediare/avansate) în jurul aceluiași domeniu didactic — *Student Clubs* — și al aceluiași toolchain: **Node/Express + SQLite + Sequelize** cu **Vitest** și **Jest** rulate **side‑by‑side**. Fiecare proiect include:
• **Specificație**, **criterii de acceptare** și **sugestii de testare**,
• **Starter code** + **Solution** (aplicație completă),
• **Teste automate** (activabile via `tests/config.json`),
• **AI‑assist (VSL)** — prompturi scurte, verificabile.
- Cum sunt organizate proiectele

## 3. Monorepo vs. standalone — analiză comparativă


**Manageri de pachete & workspaces.** Monorepo (PNPM) declară `packages/*` în `pnpm-workspace.yaml` și/sau `workspaces` în `package.json`, cu instalare la rădăcină (`pnpm i -w`). Standalone instalează local (`npm i`).

**Comenzi de instalare/testare.** Monorepo: `pnpm -w run test` sau `pnpm --filter <pkg> run test`. Standalone: `npm test`. Testare duală (Vitest & Jest) conform laboratorului. 

**Integrare CI.** Monorepo agregă pipelines (lint, unit, e2e) în `.github/workflows/*` ; standalone tinde să le aibă per proiect. 

**Avantaje/Dezavantaje.** Standalone — simplitate pentru începători; Monorepo — scalare pentru colecții mari (ex. 45 proiecte L1–L3), partajare de configuri și execuții rapide în CI; costul este înțelegerea filtrării PNPM și a dependențelor partajate.
## 4. Rolul fișierelor cheie (config, cod, teste, extra)

| Fișier / tip | Rol |
|---|---|
| `package.json` | Manifestul proiectului: metadate, dependențe, scripturi; definește `type:"module"` pentru ESM. |
| `vitest.config.ts` | Configurarea Vitest (Node/JSDOM, reporters, setup). |
| `jest.config.cjs` | Configurarea Jest (Node/JSDOM, transform ESM cu `--experimental-vm-modules` sau `babel-jest`). |
| `pnpm-workspace.yaml` | Declară pachetele din monorepo pentru PNPM. |
| `src/db/index.js` | Inițializarea Sequelize, definirea modelelor, asocierilor și `sync()` (dev/test). |
| `src/db/associations.js` | Declarații 1‑N și M‑N (`belongsToMany` prin `Registration`). |
| `src/app.js` | Server Express minimal (`/health`), util pentru verificări manuale. |

## 5. Corelații cod ↔ configurări ↔ teste


- **Rutele de API & health** (`/health`) din `src/app.js` validează conectivitatea și `PRAGMA foreign_keys` — sunt verificate în suite **Vitest** și **Jest** cu `supertest`.  
- **`.env.example`**: parametrizarea `SQLITE_STORAGE` (fișier dev) și modul `sqlite::memory:` pentru teste; legătură cu inițializarea din `src/db/index.js`.  
- **ESLint + CI**: workflow‑urile rulează `lint` și `test`, blocând PR‑uri cu erori; pentru L3, pot apărea teste e2e sau generare PWA (Workbox).  
- **Anti‑N+1 & tranzacții**: testele verifică `include` vs. încărcare lazy (număr de interogări), respectiv atomicitatea `enrollMember`.  
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S9 trece de la persistență ad‑hoc (fișiere JSON/spreadsheets) la **model relațional** cu **SQLite**, folosind **Sequelize** ca ORM pentru modelare, asocieri și tranzacții ACID. Structurile din arhive respectă un **toolchain test‑first** cu **Vitest** și **Jest** rulate side‑by‑side, plus server Express minimal pentru verificări manuale. ### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; rădăcină + `packages/*` |
| Instalare | `npm i` | `pnpm i -w` |
| Testare | `npm test` (Vitest & Jest) | `pnpm -w run test` sau `--filter` |
| CI | Workflows simple per proiect | Workflows agregate, matrice pe pachete |
| Scalare (45 proiecte) | multiplicare directoare | pachete dedicate în `packages/*` |
| Public țintă | începători | echipe/colecții avansate |
### Inventar pe arhivă (roluri)

- **Seminar9_Partea2_p2-standalone.zip** — config=3, docs=1, code=10, tests=4.
- **Seminar9_Partea3_p3-monorepo.zip** — config=137, docs=45, code=495, tests=135.
- **Seminar9_Partea3_p3-standalone.zip** — config=270, docs=90, code=990, tests=270.
- **Seminar9_Partea3_p3-READMEs.zip** — docs=45.
### Explicații fișier-cu-fișier

Consultați tabelul din §4; pentru detalii referitoare la modele/asocieri, vedeți `src/db/models/*` și `src/db/associations.js` (dacă lipsesc în anumite arhive, sunt marcate în această documentație ca **„lipsă (re-upload necesar)”**).
### Corelații între fișiere


- `src/db/index.js` ↔ `tests/*`: inițializare DB (sqlite::memory: în test), FK ON, eager vs. lazy.  
- `src/db/services/enroll.js` ↔ `tests/*`: tranzacții (commit/rollback) și invarianta `memberCount`.  
- `.github/workflows/*` ↔ `lint`/`test`: pipeline determinist pentru PR‑uri.  
### Recomandări pentru studenți


1) **Începeți în standalone**, apoi scalați în monorepo pentru colecții mari.  
2) **Modelați explicit relațiile** (1‑N, M‑N) și activați **FK ON** la inițializare.  
3) **Evitați N+1** prin `include` și **proiecții selective** (`attributes`).  
4) **Testați dublu** (Vitest & Jest) pe `sqlite::memory:`; separați unit/integration.  
5) **Tranzacții** pentru operații atomice; tratați erorile cu rollback.  
6) **Documentați contractele** și păstrați „bucle scurte” (VSL) în dezvoltare.  
### Instrucțiuni „Quick start” per arhivă


**Partea 2 — standalone:**
```bash
unzip "Seminar9_Partea2_p2-standalone.zip" -d s9p2-standalone
cd s9p2-standalone
npm i
npm test
npm run dev   # server Express opțional pe /health
```

**Partea 3 — monorepo (proiecte):**
```bash
unzip "Seminar9_Partea3_p3-monorepo.zip" -d s9p3-monorepo
cd s9p3-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter l1-p01-starter run dev
```

**Partea 3 — standalone (proiecte):**
```bash
unzip "Seminar9_Partea3_p3-standalone.zip" -d s9p3-standalone
cd s9p3-standalone/L1/L1-P01/starter
npm i
npm test
npm run dev
```
### Troubleshooting (erori frecvente)


- **FK inactive** → verificați `PRAGMA foreign_keys=ON` în `src/db/connection.js`/`index.js`.  
- **Eroare ESM în Jest** → folosiți scriptul `test:jest` cu `NODE_OPTIONS=--experimental-vm-modules` sau configurați `babel-jest`.  
- **N+1** → înlocuiți ciclurile `for` + `get*()` cu `include` și `attributes`.  
- **`sqlite3` build issues** → `npm rebuild sqlite3` sau folosiți imagini cu binare precompilate.  
- **PNPM filter** → verificați `pnpm-workspace.yaml` și `name` în `package.json`.  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** — model relațional, ACID, WAL, FK, normalizare; justifică alegeri precum `PRAGMA foreign_keys` și evitarea N+1.  
- **Partea 2 (Laborator)** — proiect Node/Express + SQLite/Sequelize, testare duală, tranzacții, eager vs. lazy.  
- **Partea 3 (Ghid Arhive)** — cum rulezi standalone/monorepo, comenzi PNPM și structură pe niveluri.  
- **Partea 3 (Proiecte)** — 45 proiecte L1–L3, fiecare cu **starter/solution** și suite de teste echivalente.  
### Prompt-șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S9** (standalone & monorepo) o aplicație Node/Express + Sequelize (SQLite) cu modele `Club/Member/Registration/Event`, `PRAGMA foreign_keys=ON`, tranzacție `enrollMember`, testare dublă **Vitest/Jest** (sqlite::memory:), CI, README cu Quick start & Troubleshooting, și variante **starter**/**solution**.”
