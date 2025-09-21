# Seminarul S0 — Analiză integrată a arhivelor și ghidurilor (standalone & monorepo)

*Generat la 2025-09-21 04:11.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar0_Partea2_lab-monorepo.zip

```
package.json
packages/app/.env.example
packages/app/.gitignore
packages/app/README.md
packages/app/babel.config.cjs
packages/app/jest.config.cjs
packages/app/package.json
packages/app/public/index.html
packages/app/src/app.js
packages/app/src/index.js
packages/app/tests/jest/app.jest.test.js
packages/app/tests/vitest/app.test.js
packages/app/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 8, other: 1, public: 1, code: 2, tests: 2.

**package.json — sinteză scripturi & workspaces**

- `package.json`: name=`s0-lab-monorepo` type=`module` workspaces=True
  - **Scripturi:**
  - `test` → `npm -w run test`
- `packages/app/package.json`: name=`tw-seminar-0-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `echo "(placeholder) add ESLint flat config"`
  - `format` → `echo "(placeholder) add Prettier config"`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest

### Seminar0_Partea2_lab-standalone.zip

```
.env.example
.gitignore
README.md
babel.config.cjs
jest.config.cjs
package.json
public/index.html
src/app.js
src/index.js
tests/jest/app.jest.test.js
tests/vitest/app.test.js
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 6, other: 1, public: 1, code: 2, tests: 2.

**package.json — sinteză scripturi & workspaces**

- `package.json`: name=`tw-seminar-0-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `echo "(placeholder) add ESLint flat config"`
  - `format` → `echo "(placeholder) add Prettier config"`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest

### Seminar0_Partea3_p3-monorepo_v2.zip

```
.github/workflows/e2e-l3.yml
.github/workflows/lint.yml
.github/workflows/unit.yml
package.json
packages/l1-p01-starter/.env.example
packages/l1-p01-starter/.gitignore
packages/l1-p01-starter/README.md
packages/l1-p01-starter/babel.config.cjs
packages/l1-p01-starter/eslint.config.mjs
packages/l1-p01-starter/jest.config.cjs
packages/l1-p01-starter/package.json
packages/l1-p01-starter/public/index.html
packages/l1-p01-starter/src/app.js
packages/l1-p01-starter/src/index.js
packages/l1-p01-starter/tests/jest/spec.jest.test.js
packages/l1-p01-starter/tests/vitest/spec.test.js
packages/l1-p01-starter/vitest.config.ts
packages/l1-p02-starter/.env.example
packages/l1-p02-starter/.gitignore
packages/l1-p02-starter/README.md
packages/l1-p02-starter/babel.config.cjs
packages/l1-p02-starter/eslint.config.mjs
packages/l1-p02-starter/jest.config.cjs
packages/l1-p02-starter/package.json
packages/l1-p02-starter/public/index.html
packages/l1-p02-starter/src/app.js
packages/l1-p02-starter/src/index.js
packages/l1-p02-starter/tests/jest/spec.jest.test.js
packages/l1-p02-starter/tests/vitest/spec.test.js
packages/l1-p02-starter/vitest.config.ts
packages/l1-p03-starter/.env.example
packages/l1-p03-starter/.gitignore
packages/l1-p03-starter/README.md
packages/l1-p03-starter/babel.config.cjs
packages/l1-p03-starter/eslint.config.mjs
packages/l1-p03-starter/jest.config.cjs
packages/l1-p03-starter/package.json
packages/l1-p03-starter/public/index.html
packages/l1-p03-starter/src/app.js
packages/l1-p03-starter/src/index.js
packages/l1-p03-starter/tests/jest/spec.jest.test.js
packages/l1-p03-starter/tests/vitest/spec.test.js
packages/l1-p03-starter/vitest.config.ts
packages/l1-p04-starter/.env.example
packages/l1-p04-starter/.gitignore
packages/l1-p04-starter/README.md
packages/l1-p04-starter/babel.config.cjs
packages/l1-p04-starter/eslint.config.mjs
packages/l1-p04-starter/jest.config.cjs
packages/l1-p04-starter/package.json
packages/l1-p04-starter/public/index.html
packages/l1-p04-starter/src/app.js
packages/l1-p04-starter/src/index.js
packages/l1-p04-starter/tests/jest/spec.jest.test.js
packages/l1-p04-starter/tests/vitest/spec.test.js
packages/l1-p04-starter/vitest.config.ts
packages/l1-p05-starter/.env.example
packages/l1-p05-starter/.gitignore
packages/l1-p05-starter/README.md
packages/l1-p05-starter/babel.config.cjs
packages/l1-p05-starter/eslint.config.mjs
packages/l1-p05-starter/jest.config.cjs
packages/l1-p05-starter/package.json
packages/l1-p05-starter/public/index.html
packages/l1-p05-starter/src/app.js
packages/l1-p05-starter/src/index.js
packages/l1-p05-starter/tests/jest/spec.jest.test.js
packages/l1-p05-starter/tests/vitest/spec.test.js
packages/l1-p05-starter/vitest.config.ts
packages/l1-p06-starter/.env.example
packages/l1-p06-starter/.gitignore
packages/l1-p06-starter/README.md
packages/l1-p06-starter/babel.config.cjs
packages/l1-p06-starter/eslint.config.mjs
packages/l1-p06-starter/jest.config.cjs
packages/l1-p06-starter/package.json
packages/l1-p06-starter/public/index.html
packages/l1-p06-starter/src/app.js
packages/l1-p06-starter/src/index.js
packages/l1-p06-starter/tests/jest/spec.jest.test.js
packages/l1-p06-starter/tests/vitest/spec.test.js
packages/l1-p06-starter/vitest.config.ts
packages/l1-p07-starter/.env.example
packages/l1-p07-starter/.gitignore
packages/l1-p07-starter/README.md
packages/l1-p07-starter/babel.config.cjs
packages/l1-p07-starter/eslint.config.mjs
packages/l1-p07-starter/jest.config.cjs
packages/l1-p07-starter/package.json
packages/l1-p07-starter/public/index.html
packages/l1-p07-starter/src/app.js
packages/l1-p07-starter/src/index.js
packages/l1-p07-starter/tests/jest/spec.jest.test.js
packages/l1-p07-starter/tests/vitest/spec.test.js
packages/l1-p07-starter/vitest.config.ts
packages/l1-p08-starter/.env.example
packages/l1-p08-starter/.gitignore
packages/l1-p08-starter/README.md
packages/l1-p08-starter/babel.config.cjs
packages/l1-p08-starter/eslint.config.mjs
packages/l1-p08-starter/jest.config.cjs
packages/l1-p08-starter/package.json
packages/l1-p08-starter/public/index.html
packages/l1-p08-starter/src/app.js
packages/l1-p08-starter/src/index.js
packages/l1-p08-starter/tests/jest/spec.jest.test.js
packages/l1-p08-starter/tests/vitest/spec.test.js
packages/l1-p08-starter/vitest.config.ts
packages/l1-p09-starter/.env.example
packages/l1-p09-starter/.gitignore
packages/l1-p09-starter/README.md
packages/l1-p09-starter/babel.config.cjs
packages/l1-p09-starter/eslint.config.mjs
packages/l1-p09-starter/jest.config.cjs
packages/l1-p09-starter/package.json
packages/l1-p09-starter/public/index.html
packages/l1-p09-starter/src/app.js
packages/l1-p09-starter/src/index.js
packages/l1-p09-starter/tests/jest/spec.jest.test.js
packages/l1-p09-starter/tests/vitest/spec.test.js
packages/l1-p09-starter/vitest.config.ts
packages/l1-p10-starter/.env.example
packages/l1-p10-starter/.gitignore
packages/l1-p10-starter/README.md
packages/l1-p10-starter/babel.config.cjs
packages/l1-p10-starter/eslint.config.mjs
packages/l1-p10-starter/jest.config.cjs
packages/l1-p10-starter/package.json
packages/l1-p10-starter/public/index.html
packages/l1-p10-starter/src/app.js
packages/l1-p10-starter/src/index.js
packages/l1-p10-starter/tests/jest/spec.jest.test.js
packages/l1-p10-starter/tests/vitest/spec.test.js
packages/l1-p10-starter/vitest.config.ts
packages/l1-p11-starter/.env.example
packages/l1-p11-starter/.gitignore
packages/l1-p11-starter/README.md
packages/l1-p11-starter/babel.config.cjs
packages/l1-p11-starter/eslint.config.mjs
packages/l1-p11-starter/jest.config.cjs
packages/l1-p11-starter/package.json
packages/l1-p11-starter/public/index.html
packages/l1-p11-starter/src/app.js
packages/l1-p11-starter/src/index.js
packages/l1-p11-starter/tests/jest/spec.jest.test.js
packages/l1-p11-starter/tests/vitest/spec.test.js
packages/l1-p11-starter/vitest.config.ts
packages/l1-p12-starter/.env.example
packages/l1-p12-starter/.gitignore
packages/l1-p12-starter/README.md
packages/l1-p12-starter/babel.config.cjs
packages/l1-p12-starter/eslint.config.mjs
packages/l1-p12-starter/jest.config.cjs
packages/l1-p12-starter/package.json
packages/l1-p12-starter/public/index.html
packages/l1-p12-starter/src/app.js
packages/l1-p12-starter/src/index.js
packages/l1-p12-starter/tests/jest/spec.jest.test.js
packages/l1-p12-starter/tests/vitest/spec.test.js
packages/l1-p12-starter/vitest.config.ts
packages/l1-p13-starter/.env.example
packages/l1-p13-starter/.gitignore
packages/l1-p13-starter/README.md
packages/l1-p13-starter/babel.config.cjs
packages/l1-p13-starter/eslint.config.mjs
packages/l1-p13-starter/jest.config.cjs
packages/l1-p13-starter/package.json
packages/l1-p13-starter/public/index.html
packages/l1-p13-starter/src/app.js
packages/l1-p13-starter/src/index.js
packages/l1-p13-starter/tests/jest/spec.jest.test.js
packages/l1-p13-starter/tests/vitest/spec.test.js
packages/l1-p13-starter/vitest.config.ts
packages/l1-p14-starter/.env.example
packages/l1-p14-starter/.gitignore
packages/l1-p14-starter/README.md
packages/l1-p14-starter/babel.config.cjs
packages/l1-p14-starter/eslint.config.mjs
packages/l1-p14-starter/jest.config.cjs
packages/l1-p14-starter/package.json
packages/l1-p14-starter/public/index.html
packages/l1-p14-starter/src/app.js
packages/l1-p14-starter/src/index.js
packages/l1-p14-starter/tests/jest/spec.jest.test.js
packages/l1-p14-starter/tests/vitest/spec.test.js
packages/l1-p14-starter/vitest.config.ts
packages/l1-p15-starter/.env.example
packages/l1-p15-starter/.gitignore
packages/l1-p15-starter/README.md
packages/l1-p15-starter/babel.config.cjs
packages/l1-p15-starter/eslint.config.mjs
packages/l1-p15-starter/jest.config.cjs
packages/l1-p15-starter/package.json
packages/l1-p15-starter/public/index.html
packages/l1-p15-starter/src/app.js
packages/l1-p15-starter/src/index.js
packages/l1-p15-starter/tests/jest/spec.jest.test.js
packages/l1-p15-starter/tests/vitest/spec.test.js
packages/l1-p15-starter/vitest.config.ts
packages/l2-p01-starter/.env.example
packages/l2-p01-starter/.gitignore
packages/l2-p01-starter/README.md
packages/l2-p01-starter/babel.config.cjs
packages/l2-p01-starter/eslint.config.mjs
packages/l2-p01-starter/jest.config.cjs
packages/l2-p01-starter/package.json
packages/l2-p01-starter/public/index.html
packages/l2-p01-starter/src/app.js
packages/l2-p01-starter/src/index.js
packages/l2-p01-starter/tests/jest/spec.jest.test.js
packages/l2-p01-starter/tests/vitest/spec.test.js
packages/l2-p01-starter/vitest.config.ts
packages/l2-p02-starter/.env.example
packages/l2-p02-starter/.gitignore
packages/l2-p02-starter/README.md
packages/l2-p02-starter/babel.config.cjs
packages/l2-p02-starter/eslint.config.mjs
packages/l2-p02-starter/jest.config.cjs
packages/l2-p02-starter/package.json
packages/l2-p02-starter/public/index.html
packages/l2-p02-starter/src/app.js
packages/l2-p02-starter/src/index.js
packages/l2-p02-starter/tests/jest/spec.jest.test.js
packages/l2-p02-starter/tests/vitest/spec.test.js
packages/l2-p02-starter/vitest.config.ts
packages/l2-p03-starter/.env.example
packages/l2-p03-starter/.gitignore
packages/l2-p03-starter/README.md
packages/l2-p03-starter/babel.config.cjs
packages/l2-p03-starter/eslint.config.mjs
packages/l2-p03-starter/jest.config.cjs
packages/l2-p03-starter/package.json
packages/l2-p03-starter/public/index.html
packages/l2-p03-starter/src/app.js
packages/l2-p03-starter/src/index.js
packages/l2-p03-starter/tests/jest/spec.jest.test.js
packages/l2-p03-starter/tests/vitest/spec.test.js
packages/l2-p03-starter/vitest.config.ts
packages/l2-p04-starter/.env.example
packages/l2-p04-starter/.gitignore
packages/l2-p04-starter/README.md
packages/l2-p04-starter/babel.config.cjs
packages/l2-p04-starter/eslint.config.mjs
packages/l2-p04-starter/jest.config.cjs
packages/l2-p04-starter/package.json
packages/l2-p04-starter/public/index.html
packages/l2-p04-starter/src/app.js
packages/l2-p04-starter/src/index.js
packages/l2-p04-starter/tests/jest/spec.jest.test.js
packages/l2-p04-starter/tests/vitest/spec.test.js
packages/l2-p04-starter/vitest.config.ts
packages/l2-p05-starter/.env.example
packages/l2-p05-starter/.gitignore
packages/l2-p05-starter/README.md
packages/l2-p05-starter/babel.config.cjs
packages/l2-p05-starter/eslint.config.mjs
packages/l2-p05-starter/jest.config.cjs
packages/l2-p05-starter/package.json
packages/l2-p05-starter/public/index.html
packages/l2-p05-starter/src/app.js
packages/l2-p05-starter/src/index.js
packages/l2-p05-starter/tests/jest/spec.jest.test.js
packages/l2-p05-starter/tests/vitest/spec.test.js
packages/l2-p05-starter/vitest.config.ts
packages/l2-p06-starter/.env.example
packages/l2-p06-starter/.gitignore
packages/l2-p06-starter/README.md
packages/l2-p06-starter/babel.config.cjs
packages/l2-p06-starter/eslint.config.mjs
packages/l2-p06-starter/jest.config.cjs
packages/l2-p06-starter/package.json
packages/l2-p06-starter/public/index.html
packages/l2-p06-starter/src/app.js
packages/l2-p06-starter/src/index.js
packages/l2-p06-starter/tests/jest/spec.jest.test.js
packages/l2-p06-starter/tests/vitest/spec.test.js
packages/l2-p06-starter/vitest.config.ts
packages/l2-p07-starter/.env.example
packages/l2-p07-starter/.gitignore
packages/l2-p07-starter/README.md
packages/l2-p07-starter/babel.config.cjs
packages/l2-p07-starter/eslint.config.mjs
packages/l2-p07-starter/jest.config.cjs
packages/l2-p07-starter/package.json
packages/l2-p07-starter/public/index.html
packages/l2-p07-starter/src/app.js
packages/l2-p07-starter/src/index.js
packages/l2-p07-starter/tests/jest/spec.jest.test.js
packages/l2-p07-starter/tests/vitest/spec.test.js
packages/l2-p07-starter/vitest.config.ts
packages/l2-p08-starter/.env.example
packages/l2-p08-starter/.gitignore
packages/l2-p08-starter/README.md
packages/l2-p08-starter/babel.config.cjs
packages/l2-p08-starter/eslint.config.mjs
packages/l2-p08-starter/jest.config.cjs
packages/l2-p08-starter/package.json
packages/l2-p08-starter/public/index.html
packages/l2-p08-starter/src/app.js
packages/l2-p08-starter/src/index.js
packages/l2-p08-starter/tests/jest/spec.jest.test.js
packages/l2-p08-starter/tests/vitest/spec.test.js
packages/l2-p08-starter/vitest.config.ts
packages/l2-p09-starter/.env.example
packages/l2-p09-starter/.gitignore
packages/l2-p09-starter/README.md
packages/l2-p09-starter/babel.config.cjs
packages/l2-p09-starter/eslint.config.mjs
packages/l2-p09-starter/jest.config.cjs
packages/l2-p09-starter/package.json
packages/l2-p09-starter/public/index.html
packages/l2-p09-starter/src/app.js
packages/l2-p09-starter/src/index.js
packages/l2-p09-starter/tests/jest/spec.jest.test.js
packages/l2-p09-starter/tests/vitest/spec.test.js
packages/l2-p09-starter/vitest.config.ts
packages/l2-p10-starter/.env.example
packages/l2-p10-starter/.gitignore
packages/l2-p10-starter/README.md
packages/l2-p10-starter/babel.config.cjs
packages/l2-p10-starter/eslint.config.mjs
packages/l2-p10-starter/jest.config.cjs
packages/l2-p10-starter/package.json
packages/l2-p10-starter/public/index.html
packages/l2-p10-starter/src/app.js
packages/l2-p10-starter/src/index.js
packages/l2-p10-starter/tests/jest/spec.jest.test.js
packages/l2-p10-starter/tests/vitest/spec.test.js
packages/l2-p10-starter/vitest.config.ts
packages/l2-p11-starter/.env.example
packages/l2-p11-starter/.gitignore
packages/l2-p11-starter/README.md
packages/l2-p11-starter/babel.config.cjs
packages/l2-p11-starter/eslint.config.mjs
packages/l2-p11-starter/jest.config.cjs
packages/l2-p11-starter/package.json
packages/l2-p11-starter/public/index.html
packages/l2-p11-starter/src/app.js
packages/l2-p11-starter/src/index.js
packages/l2-p11-starter/tests/jest/spec.jest.test.js
packages/l2-p11-starter/tests/vitest/spec.test.js
packages/l2-p11-starter/vitest.config.ts
packages/l2-p12-starter/.env.example
packages/l2-p12-starter/.gitignore
packages/l2-p12-starter/README.md
packages/l2-p12-starter/babel.config.cjs
packages/l2-p12-starter/eslint.config.mjs
packages/l2-p12-starter/jest.config.cjs
packages/l2-p12-starter/package.json
packages/l2-p12-starter/public/index.html
packages/l2-p12-starter/src/app.js
packages/l2-p12-starter/src/index.js
packages/l2-p12-starter/tests/jest/spec.jest.test.js
packages/l2-p12-starter/tests/vitest/spec.test.js
packages/l2-p12-starter/vitest.config.ts
packages/l2-p13-starter/.env.example
packages/l2-p13-starter/.gitignore
packages/l2-p13-starter/README.md
packages/l2-p13-starter/babel.config.cjs
packages/l2-p13-starter/eslint.config.mjs
packages/l2-p13-starter/jest.config.cjs
packages/l2-p13-starter/package.json
packages/l2-p13-starter/public/index.html
packages/l2-p13-starter/src/app.js
packages/l2-p13-starter/src/index.js
packages/l2-p13-starter/tests/jest/spec.jest.test.js
packages/l2-p13-starter/tests/vitest/spec.test.js
packages/l2-p13-starter/vitest.config.ts
packages/l2-p14-starter/.env.example
packages/l2-p14-starter/.gitignore
packages/l2-p14-starter/README.md
packages/l2-p14-starter/babel.config.cjs
packages/l2-p14-starter/eslint.config.mjs
packages/l2-p14-starter/jest.config.cjs
packages/l2-p14-starter/package.json
packages/l2-p14-starter/public/index.html
packages/l2-p14-starter/src/app.js
packages/l2-p14-starter/src/index.js
packages/l2-p14-starter/tests/jest/spec.jest.test.js
packages/l2-p14-starter/tests/vitest/spec.test.js
packages/l2-p14-starter/vitest.config.ts
packages/l2-p15-starter/.env.example
packages/l2-p15-starter/.gitignore
packages/l2-p15-starter/README.md
packages/l2-p15-starter/babel.config.cjs
packages/l2-p15-starter/eslint.config.mjs
packages/l2-p15-starter/jest.config.cjs
packages/l2-p15-starter/package.json
packages/l2-p15-starter/public/index.html
packages/l2-p15-starter/src/app.js
packages/l2-p15-starter/src/index.js
packages/l2-p15-starter/tests/jest/spec.jest.test.js
packages/l2-p15-starter/tests/vitest/spec.test.js
packages/l2-p15-starter/vitest.config.ts
packages/l3-p01-starter/.env.example
packages/l3-p01-starter/.gitignore
packages/l3-p01-starter/README.md
packages/l3-p01-starter/babel.config.cjs
packages/l3-p01-starter/e2e/example.spec.ts
packages/l3-p01-starter/eslint.config.mjs
packages/l3-p01-starter/jest.config.cjs
packages/l3-p01-starter/package.json
packages/l3-p01-starter/playwright.config.ts
packages/l3-p01-starter/public/index.html
packages/l3-p01-starter/public/manifest.webmanifest
packages/l3-p01-starter/public/register-sw.js
packages/l3-p01-starter/scripts/build-sw.mjs
packages/l3-p01-starter/src/app.js
packages/l3-p01-starter/src/index.js
packages/l3-p01-starter/tests/jest/spec.jest.test.js
packages/l3-p01-starter/tests/vitest/spec.test.js
packages/l3-p01-starter/vitest.config.ts
packages/l3-p02-starter/.env.example
packages/l3-p02-starter/.gitignore
packages/l3-p02-starter/README.md
packages/l3-p02-starter/babel.config.cjs
packages/l3-p02-starter/e2e/example.spec.ts
packages/l3-p02-starter/eslint.config.mjs
packages/l3-p02-starter/jest.config.cjs
packages/l3-p02-starter/package.json
packages/l3-p02-starter/playwright.config.ts
packages/l3-p02-starter/public/index.html
packages/l3-p02-starter/public/manifest.webmanifest
packages/l3-p02-starter/public/register-sw.js
packages/l3-p02-starter/scripts/build-sw.mjs
packages/l3-p02-starter/src/app.js
packages/l3-p02-starter/src/index.js
packages/l3-p02-starter/tests/jest/spec.jest.test.js
packages/l3-p02-starter/tests/vitest/spec.test.js
packages/l3-p02-starter/vitest.config.ts
packages/l3-p03-starter/.env.example
packages/l3-p03-starter/.gitignore
packages/l3-p03-starter/README.md
packages/l3-p03-starter/babel.config.cjs
packages/l3-p03-starter/e2e/example.spec.ts
packages/l3-p03-starter/eslint.config.mjs
packages/l3-p03-starter/jest.config.cjs
packages/l3-p03-starter/package.json
packages/l3-p03-starter/playwright.config.ts
packages/l3-p03-starter/public/index.html
packages/l3-p03-starter/public/manifest.webmanifest
packages/l3-p03-starter/public/register-sw.js
packages/l3-p03-starter/scripts/build-sw.mjs
packages/l3-p03-starter/src/app.js
packages/l3-p03-starter/src/index.js
packages/l3-p03-starter/tests/jest/spec.jest.test.js
packages/l3-p03-starter/tests/vitest/spec.test.js
packages/l3-p03-starter/vitest.config.ts
packages/l3-p04-starter/.env.example
packages/l3-p04-starter/.gitignore
packages/l3-p04-starter/README.md
packages/l3-p04-starter/babel.config.cjs
packages/l3-p04-starter/e2e/example.spec.ts
packages/l3-p04-starter/eslint.config.mjs
packages/l3-p04-starter/jest.config.cjs
packages/l3-p04-starter/package.json
packages/l3-p04-starter/playwright.config.ts
packages/l3-p04-starter/public/index.html
packages/l3-p04-starter/public/manifest.webmanifest
packages/l3-p04-starter/public/register-sw.js
packages/l3-p04-starter/scripts/build-sw.mjs
packages/l3-p04-starter/src/app.js
packages/l3-p04-starter/src/index.js
packages/l3-p04-starter/tests/jest/spec.jest.test.js
packages/l3-p04-starter/tests/vitest/spec.test.js
packages/l3-p04-starter/vitest.config.ts
packages/l3-p05-starter/.env.example
packages/l3-p05-starter/.gitignore
packages/l3-p05-starter/README.md
packages/l3-p05-starter/babel.config.cjs
packages/l3-p05-starter/e2e/example.spec.ts
packages/l3-p05-starter/eslint.config.mjs
packages/l3-p05-starter/jest.config.cjs
packages/l3-p05-starter/package.json
packages/l3-p05-starter/playwright.config.ts
packages/l3-p05-starter/public/index.html
packages/l3-p05-starter/public/manifest.webmanifest
packages/l3-p05-starter/public/register-sw.js
packages/l3-p05-starter/scripts/build-sw.mjs
packages/l3-p05-starter/src/app.js
packages/l3-p05-starter/src/index.js
packages/l3-p05-starter/tests/jest/spec.jest.test.js
packages/l3-p05-starter/tests/vitest/spec.test.js
packages/l3-p05-starter/vitest.config.ts
packages/l3-p06-starter/.env.example
packages/l3-p06-starter/.gitignore
packages/l3-p06-starter/README.md
packages/l3-p06-starter/babel.config.cjs
packages/l3-p06-starter/e2e/example.spec.ts
packages/l3-p06-starter/eslint.config.mjs
packages/l3-p06-starter/jest.config.cjs
packages/l3-p06-starter/package.json
packages/l3-p06-starter/playwright.config.ts
packages/l3-p06-starter/public/index.html
packages/l3-p06-starter/public/manifest.webmanifest
packages/l3-p06-starter/public/register-sw.js
packages/l3-p06-starter/scripts/build-sw.mjs
packages/l3-p06-starter/src/app.js
packages/l3-p06-starter/src/index.js
packages/l3-p06-starter/tests/jest/spec.jest.test.js
packages/l3-p06-starter/tests/vitest/spec.test.js
packages/l3-p06-starter/vitest.config.ts
packages/l3-p07-starter/.env.example
packages/l3-p07-starter/.gitignore
packages/l3-p07-starter/README.md
packages/l3-p07-starter/babel.config.cjs
packages/l3-p07-starter/e2e/example.spec.ts
packages/l3-p07-starter/eslint.config.mjs
packages/l3-p07-starter/jest.config.cjs
packages/l3-p07-starter/package.json
packages/l3-p07-starter/playwright.config.ts
packages/l3-p07-starter/public/index.html
packages/l3-p07-starter/public/manifest.webmanifest
packages/l3-p07-starter/public/register-sw.js
packages/l3-p07-starter/scripts/build-sw.mjs
packages/l3-p07-starter/src/app.js
packages/l3-p07-starter/src/index.js
packages/l3-p07-starter/tests/jest/spec.jest.test.js
packages/l3-p07-starter/tests/vitest/spec.test.js
packages/l3-p07-starter/vitest.config.ts
packages/l3-p08-starter/.env.example
packages/l3-p08-starter/.gitignore
packages/l3-p08-starter/README.md
packages/l3-p08-starter/babel.config.cjs
packages/l3-p08-starter/e2e/example.spec.ts
packages/l3-p08-starter/eslint.config.mjs
packages/l3-p08-starter/jest.config.cjs
packages/l3-p08-starter/package.json
packages/l3-p08-starter/playwright.config.ts
packages/l3-p08-starter/public/index.html
packages/l3-p08-starter/public/manifest.webmanifest
packages/l3-p08-starter/public/register-sw.js
packages/l3-p08-starter/scripts/build-sw.mjs
packages/l3-p08-starter/src/app.js
packages/l3-p08-starter/src/index.js
packages/l3-p08-starter/tests/jest/spec.jest.test.js
packages/l3-p08-starter/tests/vitest/spec.test.js
packages/l3-p08-starter/vitest.config.ts
packages/l3-p09-starter/.env.example
packages/l3-p09-starter/.gitignore
packages/l3-p09-starter/README.md
packages/l3-p09-starter/babel.config.cjs
packages/l3-p09-starter/e2e/example.spec.ts
packages/l3-p09-starter/eslint.config.mjs
packages/l3-p09-starter/jest.config.cjs
packages/l3-p09-starter/package.json
packages/l3-p09-starter/playwright.config.ts
packages/l3-p09-starter/public/index.html
packages/l3-p09-starter/public/manifest.webmanifest
packages/l3-p09-starter/public/register-sw.js
packages/l3-p09-starter/scripts/build-sw.mjs
packages/l3-p09-starter/src/app.js
packages/l3-p09-starter/src/index.js
packages/l3-p09-starter/tests/jest/spec.jest.test.js
packages/l3-p09-starter/tests/vitest/spec.test.js
packages/l3-p09-starter/vitest.config.ts
packages/l3-p10-starter/.env.example
packages/l3-p10-starter/.gitignore
packages/l3-p10-starter/README.md
packages/l3-p10-starter/babel.config.cjs
packages/l3-p10-starter/e2e/example.spec.ts
packages/l3-p10-starter/eslint.config.mjs
packages/l3-p10-starter/jest.config.cjs
packages/l3-p10-starter/package.json
packages/l3-p10-starter/playwright.config.ts
packages/l3-p10-starter/public/index.html
packages/l3-p10-starter/public/manifest.webmanifest
packages/l3-p10-starter/public/register-sw.js
packages/l3-p10-starter/scripts/build-sw.mjs
packages/l3-p10-starter/src/app.js
packages/l3-p10-starter/src/index.js
packages/l3-p10-starter/tests/jest/spec.jest.test.js
packages/l3-p10-starter/tests/vitest/spec.test.js
packages/l3-p10-starter/vitest.config.ts
packages/l3-p11-starter/.env.example
packages/l3-p11-starter/.gitignore
packages/l3-p11-starter/README.md
packages/l3-p11-starter/babel.config.cjs
packages/l3-p11-starter/e2e/example.spec.ts
packages/l3-p11-starter/eslint.config.mjs
packages/l3-p11-starter/jest.config.cjs
packages/l3-p11-starter/package.json
packages/l3-p11-starter/playwright.config.ts
packages/l3-p11-starter/public/index.html
packages/l3-p11-starter/public/manifest.webmanifest
packages/l3-p11-starter/public/register-sw.js
packages/l3-p11-starter/scripts/build-sw.mjs
packages/l3-p11-starter/src/app.js
packages/l3-p11-starter/src/index.js
packages/l3-p11-starter/tests/jest/spec.jest.test.js
packages/l3-p11-starter/tests/vitest/spec.test.js
packages/l3-p11-starter/vitest.config.ts
packages/l3-p12-starter/.env.example
packages/l3-p12-starter/.gitignore
packages/l3-p12-starter/README.md
packages/l3-p12-starter/babel.config.cjs
packages/l3-p12-starter/e2e/example.spec.ts
packages/l3-p12-starter/eslint.config.mjs
packages/l3-p12-starter/jest.config.cjs
packages/l3-p12-starter/package.json
packages/l3-p12-starter/playwright.config.ts
packages/l3-p12-starter/public/index.html
packages/l3-p12-starter/public/manifest.webmanifest
packages/l3-p12-starter/public/register-sw.js
packages/l3-p12-starter/scripts/build-sw.mjs
packages/l3-p12-starter/src/app.js
packages/l3-p12-starter/src/index.js
packages/l3-p12-starter/tests/jest/spec.jest.test.js
packages/l3-p12-starter/tests/vitest/spec.test.js
packages/l3-p12-starter/vitest.config.ts
packages/l3-p13-starter/.env.example
packages/l3-p13-starter/.gitignore
packages/l3-p13-starter/README.md
packages/l3-p13-starter/babel.config.cjs
packages/l3-p13-starter/e2e/example.spec.ts
packages/l3-p13-starter/eslint.config.mjs
packages/l3-p13-starter/jest.config.cjs
packages/l3-p13-starter/package.json
packages/l3-p13-starter/playwright.config.ts
packages/l3-p13-starter/public/index.html
packages/l3-p13-starter/public/manifest.webmanifest
packages/l3-p13-starter/public/register-sw.js
packages/l3-p13-starter/scripts/build-sw.mjs
packages/l3-p13-starter/src/app.js
packages/l3-p13-starter/src/index.js
packages/l3-p13-starter/tests/jest/spec.jest.test.js
packages/l3-p13-starter/tests/vitest/spec.test.js
packages/l3-p13-starter/vitest.config.ts
packages/l3-p14-starter/.env.example
packages/l3-p14-starter/.gitignore
packages/l3-p14-starter/README.md
packages/l3-p14-starter/babel.config.cjs
packages/l3-p14-starter/e2e/example.spec.ts
packages/l3-p14-starter/eslint.config.mjs
packages/l3-p14-starter/jest.config.cjs
packages/l3-p14-starter/package.json
packages/l3-p14-starter/playwright.config.ts
packages/l3-p14-starter/public/index.html
packages/l3-p14-starter/public/manifest.webmanifest
packages/l3-p14-starter/public/register-sw.js
packages/l3-p14-starter/scripts/build-sw.mjs
packages/l3-p14-starter/src/app.js
packages/l3-p14-starter/src/index.js
packages/l3-p14-starter/tests/jest/spec.jest.test.js
packages/l3-p14-starter/tests/vitest/spec.test.js
packages/l3-p14-starter/vitest.config.ts
packages/l3-p15-starter/.env.example
packages/l3-p15-starter/.gitignore
packages/l3-p15-starter/README.md
packages/l3-p15-starter/babel.config.cjs
packages/l3-p15-starter/e2e/example.spec.ts
packages/l3-p15-starter/eslint.config.mjs
packages/l3-p15-starter/jest.config.cjs
packages/l3-p15-starter/package.json
packages/l3-p15-starter/playwright.config.ts
packages/l3-p15-starter/public/index.html
packages/l3-p15-starter/public/manifest.webmanifest
packages/l3-p15-starter/public/register-sw.js
packages/l3-p15-starter/scripts/build-sw.mjs
packages/l3-p15-starter/src/app.js
packages/l3-p15-starter/src/index.js
packages/l3-p15-starter/tests/jest/spec.jest.test.js
packages/l3-p15-starter/tests/vitest/spec.test.js
packages/l3-p15-starter/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** starter: 660.

**Categorii de fișiere:** config: 332, other: 75, public: 75, code: 90, tests: 90, ci: 3.

**package.json — sinteză scripturi & workspaces**

- `package.json`: name=`s0p3-monorepo_v2` type=`module` workspaces=True
- `packages/l1-p01-starter/package.json`: name=`l1-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p02-starter/package.json`: name=`l1-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p03-starter/package.json`: name=`l1-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p04-starter/package.json`: name=`l1-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p05-starter/package.json`: name=`l1-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p06-starter/package.json`: name=`l1-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p07-starter/package.json`: name=`l1-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p08-starter/package.json`: name=`l1-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p09-starter/package.json`: name=`l1-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p10-starter/package.json`: name=`l1-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p11-starter/package.json`: name=`l1-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p12-starter/package.json`: name=`l1-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p13-starter/package.json`: name=`l1-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p14-starter/package.json`: name=`l1-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l1-p15-starter/package.json`: name=`l1-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p01-starter/package.json`: name=`l2-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p02-starter/package.json`: name=`l2-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p03-starter/package.json`: name=`l2-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p04-starter/package.json`: name=`l2-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p05-starter/package.json`: name=`l2-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p06-starter/package.json`: name=`l2-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p07-starter/package.json`: name=`l2-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p08-starter/package.json`: name=`l2-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p09-starter/package.json`: name=`l2-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p10-starter/package.json`: name=`l2-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p11-starter/package.json`: name=`l2-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p12-starter/package.json`: name=`l2-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p13-starter/package.json`: name=`l2-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p14-starter/package.json`: name=`l2-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l2-p15-starter/package.json`: name=`l2-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `packages/l3-p01-starter/package.json`: name=`l3-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p02-starter/package.json`: name=`l3-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p03-starter/package.json`: name=`l3-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p04-starter/package.json`: name=`l3-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p05-starter/package.json`: name=`l3-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p06-starter/package.json`: name=`l3-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p07-starter/package.json`: name=`l3-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p08-starter/package.json`: name=`l3-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p09-starter/package.json`: name=`l3-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p10-starter/package.json`: name=`l3-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p11-starter/package.json`: name=`l3-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p12-starter/package.json`: name=`l3-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p13-starter/package.json`: name=`l3-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p14-starter/package.json`: name=`l3-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p15-starter/package.json`: name=`l3-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build

### Seminar0_Partea3_p3-standalone_v2.zip

> Structura este mare; se afișează începutul și sfârșitul.

```
.github/workflows/e2e-l3.yml
.github/workflows/lint.yml
.github/workflows/unit-jest.yml
.github/workflows/unit-vitest.yml
.github/workflows/workbox-l3.yml
L1/L1-P01/solution/.env.example
L1/L1-P01/solution/.gitignore
L1/L1-P01/solution/README.md
L1/L1-P01/solution/babel.config.cjs
L1/L1-P01/solution/eslint.config.mjs
L1/L1-P01/solution/jest.config.cjs
L1/L1-P01/solution/package.json
L1/L1-P01/solution/public/index.html
L1/L1-P01/solution/src/app.js
L1/L1-P01/solution/src/index.js
L1/L1-P01/solution/tests/jest/spec.jest.test.js
L1/L1-P01/solution/tests/vitest/spec.test.js
L1/L1-P01/solution/vitest.config.ts
L1/L1-P01/starter/.env.example
L1/L1-P01/starter/.gitignore
L1/L1-P01/starter/README.md
L1/L1-P01/starter/babel.config.cjs
L1/L1-P01/starter/eslint.config.mjs
L1/L1-P01/starter/jest.config.cjs
L1/L1-P01/starter/package.json
L1/L1-P01/starter/public/index.html
L1/L1-P01/starter/src/app.js
L1/L1-P01/starter/src/index.js
L1/L1-P01/starter/tests/jest/spec.jest.test.js
L1/L1-P01/starter/tests/vitest/spec.test.js
L1/L1-P01/starter/vitest.config.ts
L1/L1-P02/solution/.env.example
L1/L1-P02/solution/.gitignore
L1/L1-P02/solution/README.md
L1/L1-P02/solution/babel.config.cjs
L1/L1-P02/solution/eslint.config.mjs
L1/L1-P02/solution/jest.config.cjs
L1/L1-P02/solution/package.json
L1/L1-P02/solution/public/index.html
L1/L1-P02/solution/src/app.js
L1/L1-P02/solution/src/index.js
L1/L1-P02/solution/tests/jest/spec.jest.test.js
L1/L1-P02/solution/tests/vitest/spec.test.js
L1/L1-P02/solution/vitest.config.ts
L1/L1-P02/starter/.env.example
L1/L1-P02/starter/.gitignore
L1/L1-P02/starter/README.md
L1/L1-P02/starter/babel.config.cjs
L1/L1-P02/starter/eslint.config.mjs
L1/L1-P02/starter/jest.config.cjs
L1/L1-P02/starter/package.json
L1/L1-P02/starter/public/index.html
L1/L1-P02/starter/src/app.js
L1/L1-P02/starter/src/index.js
L1/L1-P02/starter/tests/jest/spec.jest.test.js
L1/L1-P02/starter/tests/vitest/spec.test.js
L1/L1-P02/starter/vitest.config.ts
L1/L1-P03/solution/.env.example
L1/L1-P03/solution/.gitignore
L1/L1-P03/solution/README.md
L1/L1-P03/solution/babel.config.cjs
L1/L1-P03/solution/eslint.config.mjs
L1/L1-P03/solution/jest.config.cjs
L1/L1-P03/solution/package.json
L1/L1-P03/solution/public/index.html
L1/L1-P03/solution/src/app.js
L1/L1-P03/solution/src/index.js
L1/L1-P03/solution/tests/jest/spec.jest.test.js
L1/L1-P03/solution/tests/vitest/spec.test.js
L1/L1-P03/solution/vitest.config.ts
L1/L1-P03/starter/.env.example
L1/L1-P03/starter/.gitignore
L1/L1-P03/starter/README.md
L1/L1-P03/starter/babel.config.cjs
L1/L1-P03/starter/eslint.config.mjs
L1/L1-P03/starter/jest.config.cjs
L1/L1-P03/starter/package.json
L1/L1-P03/starter/public/index.html
L1/L1-P03/starter/src/app.js
L1/L1-P03/starter/src/index.js
L1/L1-P03/starter/tests/jest/spec.jest.test.js
L1/L1-P03/starter/tests/vitest/spec.test.js
L1/L1-P03/starter/vitest.config.ts
L1/L1-P04/solution/.env.example
L1/L1-P04/solution/.gitignore
L1/L1-P04/solution/README.md
L1/L1-P04/solution/babel.config.cjs
L1/L1-P04/solution/eslint.config.mjs
L1/L1-P04/solution/jest.config.cjs
L1/L1-P04/solution/package.json
L1/L1-P04/solution/public/index.html
L1/L1-P04/solution/src/app.js
L1/L1-P04/solution/src/index.js
L1/L1-P04/solution/tests/jest/spec.jest.test.js
L1/L1-P04/solution/tests/vitest/spec.test.js
L1/L1-P04/solution/vitest.config.ts
L1/L1-P04/starter/.env.example
L1/L1-P04/starter/.gitignore
L1/L1-P04/starter/README.md
L1/L1-P04/starter/babel.config.cjs
L1/L1-P04/starter/eslint.config.mjs
L1/L1-P04/starter/jest.config.cjs
L1/L1-P04/starter/package.json
L1/L1-P04/starter/public/index.html
L1/L1-P04/starter/src/app.js
L1/L1-P04/starter/src/index.js
L1/L1-P04/starter/tests/jest/spec.jest.test.js
L1/L1-P04/starter/tests/vitest/spec.test.js
L1/L1-P04/starter/vitest.config.ts
L1/L1-P05/solution/.env.example
L1/L1-P05/solution/.gitignore
L1/L1-P05/solution/README.md
L1/L1-P05/solution/babel.config.cjs
L1/L1-P05/solution/eslint.config.mjs
L1/L1-P05/solution/jest.config.cjs
L1/L1-P05/solution/package.json
L1/L1-P05/solution/public/index.html
L1/L1-P05/solution/src/app.js
L1/L1-P05/solution/src/index.js
L1/L1-P05/solution/tests/jest/spec.jest.test.js
L1/L1-P05/solution/tests/vitest/spec.test.js
L1/L1-P05/solution/vitest.config.ts
L1/L1-P05/starter/.env.example
L1/L1-P05/starter/.gitignore
L1/L1-P05/starter/README.md
L1/L1-P05/starter/babel.config.cjs
L1/L1-P05/starter/eslint.config.mjs
L1/L1-P05/starter/jest.config.cjs
L1/L1-P05/starter/package.json
L1/L1-P05/starter/public/index.html
L1/L1-P05/starter/src/app.js
L1/L1-P05/starter/src/index.js
L1/L1-P05/starter/tests/jest/spec.jest.test.js
L1/L1-P05/starter/tests/vitest/spec.test.js
L1/L1-P05/starter/vitest.config.ts
L1/L1-P06/solution/.env.example
L1/L1-P06/solution/.gitignore
L1/L1-P06/solution/README.md
L1/L1-P06/solution/babel.config.cjs
L1/L1-P06/solution/eslint.config.mjs
L1/L1-P06/solution/jest.config.cjs
L1/L1-P06/solution/package.json
L1/L1-P06/solution/public/index.html
L1/L1-P06/solution/src/app.js
L1/L1-P06/solution/src/index.js
L1/L1-P06/solution/tests/jest/spec.jest.test.js
L1/L1-P06/solution/tests/vitest/spec.test.js
L1/L1-P06/solution/vitest.config.ts
L1/L1-P06/starter/.env.example
L1/L1-P06/starter/.gitignore
L1/L1-P06/starter/README.md
L1/L1-P06/starter/babel.config.cjs
L1/L1-P06/starter/eslint.config.mjs
L1/L1-P06/starter/jest.config.cjs
L1/L1-P06/starter/package.json
L1/L1-P06/starter/public/index.html
L1/L1-P06/starter/src/app.js
L1/L1-P06/starter/src/index.js
L1/L1-P06/starter/tests/jest/spec.jest.test.js
L1/L1-P06/starter/tests/vitest/spec.test.js
L1/L1-P06/starter/vitest.config.ts
L1/L1-P07/solution/.env.example
L1/L1-P07/solution/.gitignore
L1/L1-P07/solution/README.md
L1/L1-P07/solution/babel.config.cjs
L1/L1-P07/solution/eslint.config.mjs
L1/L1-P07/solution/jest.config.cjs
L1/L1-P07/solution/package.json
L1/L1-P07/solution/public/index.html
L1/L1-P07/solution/src/app.js
L1/L1-P07/solution/src/index.js
L1/L1-P07/solution/tests/jest/spec.jest.test.js
L1/L1-P07/solution/tests/vitest/spec.test.js
L1/L1-P07/solution/vitest.config.ts
L1/L1-P07/starter/.env.example
L1/L1-P07/starter/.gitignore
L1/L1-P07/starter/README.md
L1/L1-P07/starter/babel.config.cjs
L1/L1-P07/starter/eslint.config.mjs
L1/L1-P07/starter/jest.config.cjs
L1/L1-P07/starter/package.json
L1/L1-P07/starter/public/index.html
L1/L1-P07/starter/src/app.js
L1/L1-P07/starter/src/index.js
L1/L1-P07/starter/tests/jest/spec.jest.test.js
L1/L1-P07/starter/tests/vitest/spec.test.js
L1/L1-P07/starter/vitest.config.ts
L1/L1-P08/solution/.env.example
L1/L1-P08/solution/.gitignore
L1/L1-P08/solution/README.md
L1/L1-P08/solution/babel.config.cjs
L1/L1-P08/solution/eslint.config.mjs
L1/L1-P08/solution/jest.config.cjs
L1/L1-P08/solution/package.json
L1/L1-P08/solution/public/index.html
L1/L1-P08/solution/src/app.js
L1/L1-P08/solution/src/index.js
L1/L1-P08/solution/tests/jest/spec.jest.test.js
L1/L1-P08/solution/tests/vitest/spec.test.js
L1/L1-P08/solution/vitest.config.ts
L1/L1-P08/starter/.env.example
L1/L1-P08/starter/.gitignore
L1/L1-P08/starter/README.md
L1/L1-P08/starter/babel.config.cjs
L1/L1-P08/starter/eslint.config.mjs
L1/L1-P08/starter/jest.config.cjs
L1/L1-P08/starter/package.json
L1/L1-P08/starter/public/index.html
L1/L1-P08/starter/src/app.js
L1/L1-P08/starter/src/index.js
L1/L1-P08/starter/tests/jest/spec.jest.test.js
L1/L1-P08/starter/tests/vitest/spec.test.js
L1/L1-P08/starter/vitest.config.ts
L1/L1-P09/solution/.env.example
L1/L1-P09/solution/.gitignore
L1/L1-P09/solution/README.md
L1/L1-P09/solution/babel.config.cjs
L1/L1-P09/solution/eslint.config.mjs
L1/L1-P09/solution/jest.config.cjs
L1/L1-P09/solution/package.json
L1/L1-P09/solution/public/index.html
L1/L1-P09/solution/src/app.js
L1/L1-P09/solution/src/index.js
L1/L1-P09/solution/tests/jest/spec.jest.test.js
L1/L1-P09/solution/tests/vitest/spec.test.js
L1/L1-P09/solution/vitest.config.ts
L1/L1-P09/starter/.env.example
L1/L1-P09/starter/.gitignore
L1/L1-P09/starter/README.md
L1/L1-P09/starter/babel.config.cjs
L1/L1-P09/starter/eslint.config.mjs
L1/L1-P09/starter/jest.config.cjs
L1/L1-P09/starter/package.json
L1/L1-P09/starter/public/index.html
L1/L1-P09/starter/src/app.js
L1/L1-P09/starter/src/index.js
L1/L1-P09/starter/tests/jest/spec.jest.test.js
L1/L1-P09/starter/tests/vitest/spec.test.js
L1/L1-P09/starter/vitest.config.ts
L1/L1-P10/solution/.env.example
L1/L1-P10/solution/.gitignore
L1/L1-P10/solution/README.md
L1/L1-P10/solution/babel.config.cjs
L1/L1-P10/solution/eslint.config.mjs
L1/L1-P10/solution/jest.config.cjs
L1/L1-P10/solution/package.json
L1/L1-P10/solution/public/index.html
L1/L1-P10/solution/src/app.js
L1/L1-P10/solution/src/index.js
L1/L1-P10/solution/tests/jest/spec.jest.test.js
L1/L1-P10/solution/tests/vitest/spec.test.js
L1/L1-P10/solution/vitest.config.ts
L1/L1-P10/starter/.env.example
L1/L1-P10/starter/.gitignore
L1/L1-P10/starter/README.md
L1/L1-P10/starter/babel.config.cjs
L1/L1-P10/starter/eslint.config.mjs
L1/L1-P10/starter/jest.config.cjs
L1/L1-P10/starter/package.json
L1/L1-P10/starter/public/index.html
L1/L1-P10/starter/src/app.js
L1/L1-P10/starter/src/index.js
L1/L1-P10/starter/tests/jest/spec.jest.test.js
L1/L1-P10/starter/tests/vitest/spec.test.js
L1/L1-P10/starter/vitest.config.ts
L1/L1-P11/solution/.env.example
L1/L1-P11/solution/.gitignore
L1/L1-P11/solution/README.md
L1/L1-P11/solution/babel.config.cjs
L1/L1-P11/solution/eslint.config.mjs
L1/L1-P11/solution/jest.config.cjs
L1/L1-P11/solution/package.json
L1/L1-P11/solution/public/index.html
L1/L1-P11/solution/src/app.js
L1/L1-P11/solution/src/index.js
L1/L1-P11/solution/tests/jest/spec.jest.test.js
L1/L1-P11/solution/tests/vitest/spec.test.js
L1/L1-P11/solution/vitest.config.ts
L1/L1-P11/starter/.env.example
L1/L1-P11/starter/.gitignore
L1/L1-P11/starter/README.md
L1/L1-P11/starter/babel.config.cjs
L1/L1-P11/starter/eslint.config.mjs
L1/L1-P11/starter/jest.config.cjs
L1/L1-P11/starter/package.json
L1/L1-P11/starter/public/index.html
L1/L1-P11/starter/src/app.js
L1/L1-P11/starter/src/index.js
L1/L1-P11/starter/tests/jest/spec.jest.test.js
L1/L1-P11/starter/tests/vitest/spec.test.js
L1/L1-P11/starter/vitest.config.ts
L1/L1-P12/solution/.env.example
L1/L1-P12/solution/.gitignore
L1/L1-P12/solution/README.md
L1/L1-P12/solution/babel.config.cjs
L1/L1-P12/solution/eslint.config.mjs
L1/L1-P12/solution/jest.config.cjs
L1/L1-P12/solution/package.json
L1/L1-P12/solution/public/index.html
L1/L1-P12/solution/src/app.js
L1/L1-P12/solution/src/index.js
L1/L1-P12/solution/tests/jest/spec.jest.test.js
L1/L1-P12/solution/tests/vitest/spec.test.js
L1/L1-P12/solution/vitest.config.ts
L1/L1-P12/starter/.env.example
L1/L1-P12/starter/.gitignore
L1/L1-P12/starter/README.md
L1/L1-P12/starter/babel.config.cjs
L1/L1-P12/starter/eslint.config.mjs
L1/L1-P12/starter/jest.config.cjs
L1/L1-P12/starter/package.json
L1/L1-P12/starter/public/index.html
L1/L1-P12/starter/src/app.js
L1/L1-P12/starter/src/index.js
L1/L1-P12/starter/tests/jest/spec.jest.test.js
L1/L1-P12/starter/tests/vitest/spec.test.js
L1/L1-P12/starter/vitest.config.ts
L1/L1-P13/solution/.env.example
L1/L1-P13/solution/.gitignore
L1/L1-P13/solution/README.md
L1/L1-P13/solution/babel.config.cjs
L1/L1-P13/solution/eslint.config.mjs
L1/L1-P13/solution/jest.config.cjs
L1/L1-P13/solution/package.json
L1/L1-P13/solution/public/index.html
L1/L1-P13/solution/src/app.js
L1/L1-P13/solution/src/index.js
L1/L1-P13/solution/tests/jest/spec.jest.test.js
L1/L1-P13/solution/tests/vitest/spec.test.js
L1/L1-P13/solution/vitest.config.ts
L1/L1-P13/starter/.env.example
L1/L1-P13/starter/.gitignore
L1/L1-P13/starter/README.md
L1/L1-P13/starter/babel.config.cjs
L1/L1-P13/starter/eslint.config.mjs
L1/L1-P13/starter/jest.config.cjs
L1/L1-P13/starter/package.json
L1/L1-P13/starter/public/index.html
L1/L1-P13/starter/src/app.js
L1/L1-P13/starter/src/index.js
L1/L1-P13/starter/tests/jest/spec.jest.test.js
L1/L1-P13/starter/tests/vitest/spec.test.js
L1/L1-P13/starter/vitest.config.ts
L1/L1-P14/solution/.env.example
L1/L1-P14/solution/.gitignore
L1/L1-P14/solution/README.md
L1/L1-P14/solution/babel.config.cjs
L1/L1-P14/solution/eslint.config.mjs
L1/L1-P14/solution/jest.config.cjs
L1/L1-P14/solution/package.json
L1/L1-P14/solution/public/index.html
L1/L1-P14/solution/src/app.js
L1/L1-P14/solution/src/index.js
L1/L1-P14/solution/tests/jest/spec.jest.test.js
L1/L1-P14/solution/tests/vitest/spec.test.js
L1/L1-P14/solution/vitest.config.ts
L1/L1-P14/starter/.env.example
L1/L1-P14/starter/.gitignore
L1/L1-P14/starter/README.md
L1/L1-P14/starter/babel.config.cjs
L1/L1-P14/starter/eslint.config.mjs
L1/L1-P14/starter/jest.config.cjs
L1/L1-P14/starter/package.json
L1/L1-P14/starter/public/index.html
L1/L1-P14/starter/src/app.js
L1/L1-P14/starter/src/index.js
L1/L1-P14/starter/tests/jest/spec.jest.test.js
L1/L1-P14/starter/tests/vitest/spec.test.js
L1/L1-P14/starter/vitest.config.ts
L1/L1-P15/solution/.env.example
L1/L1-P15/solution/.gitignore
L1/L1-P15/solution/README.md
L1/L1-P15/solution/babel.config.cjs
L1/L1-P15/solution/eslint.config.mjs
L1/L1-P15/solution/jest.config.cjs
L1/L1-P15/solution/package.json
L1/L1-P15/solution/public/index.html
L1/L1-P15/solution/src/app.js
L1/L1-P15/solution/src/index.js
L1/L1-P15/solution/tests/jest/spec.jest.test.js
L1/L1-P15/solution/tests/vitest/spec.test.js
L1/L1-P15/solution/vitest.config.ts
L1/L1-P15/starter/.env.example
L1/L1-P15/starter/.gitignore
L1/L1-P15/starter/README.md
L1/L1-P15/starter/babel.config.cjs
L1/L1-P15/starter/eslint.config.mjs
L1/L1-P15/starter/jest.config.cjs
L1/L1-P15/starter/package.json
L1/L1-P15/starter/public/index.html
L1/L1-P15/starter/src/app.js
L1/L1-P15/starter/src/index.js
L1/L1-P15/starter/tests/jest/spec.jest.test.js
L1/L1-P15/starter/tests/vitest/spec.test.js
L1/L1-P15/starter/vitest.config.ts
L2/L2-P01/solution/.env.example
L2/L2-P01/solution/.gitignore
L2/L2-P01/solution/README.md
L2/L2-P01/solution/babel.config.cjs
L2/L2-P01/solution/eslint.config.mjs
…
L3/L3-P04/starter/src/index.js
L3/L3-P04/starter/tests/jest/spec.jest.test.js
L3/L3-P04/starter/tests/vitest/spec.test.js
L3/L3-P04/starter/vitest.config.ts
L3/L3-P05/solution/.env.example
L3/L3-P05/solution/.gitignore
L3/L3-P05/solution/README.md
L3/L3-P05/solution/babel.config.cjs
L3/L3-P05/solution/e2e/example.spec.ts
L3/L3-P05/solution/eslint.config.mjs
L3/L3-P05/solution/jest.config.cjs
L3/L3-P05/solution/package.json
L3/L3-P05/solution/playwright.config.ts
L3/L3-P05/solution/public/index.html
L3/L3-P05/solution/public/manifest.webmanifest
L3/L3-P05/solution/public/register-sw.js
L3/L3-P05/solution/scripts/build-sw.mjs
L3/L3-P05/solution/src/app.js
L3/L3-P05/solution/src/index.js
L3/L3-P05/solution/tests/jest/spec.jest.test.js
L3/L3-P05/solution/tests/vitest/spec.test.js
L3/L3-P05/solution/vitest.config.ts
L3/L3-P05/starter/.env.example
L3/L3-P05/starter/.gitignore
L3/L3-P05/starter/README.md
L3/L3-P05/starter/babel.config.cjs
L3/L3-P05/starter/e2e/example.spec.ts
L3/L3-P05/starter/eslint.config.mjs
L3/L3-P05/starter/jest.config.cjs
L3/L3-P05/starter/package.json
L3/L3-P05/starter/playwright.config.ts
L3/L3-P05/starter/public/index.html
L3/L3-P05/starter/public/manifest.webmanifest
L3/L3-P05/starter/public/register-sw.js
L3/L3-P05/starter/scripts/build-sw.mjs
L3/L3-P05/starter/src/app.js
L3/L3-P05/starter/src/index.js
L3/L3-P05/starter/tests/jest/spec.jest.test.js
L3/L3-P05/starter/tests/vitest/spec.test.js
L3/L3-P05/starter/vitest.config.ts
L3/L3-P06/solution/.env.example
L3/L3-P06/solution/.gitignore
L3/L3-P06/solution/README.md
L3/L3-P06/solution/babel.config.cjs
L3/L3-P06/solution/e2e/example.spec.ts
L3/L3-P06/solution/eslint.config.mjs
L3/L3-P06/solution/jest.config.cjs
L3/L3-P06/solution/package.json
L3/L3-P06/solution/playwright.config.ts
L3/L3-P06/solution/public/index.html
L3/L3-P06/solution/public/manifest.webmanifest
L3/L3-P06/solution/public/register-sw.js
L3/L3-P06/solution/scripts/build-sw.mjs
L3/L3-P06/solution/src/app.js
L3/L3-P06/solution/src/index.js
L3/L3-P06/solution/tests/jest/spec.jest.test.js
L3/L3-P06/solution/tests/vitest/spec.test.js
L3/L3-P06/solution/vitest.config.ts
L3/L3-P06/starter/.env.example
L3/L3-P06/starter/.gitignore
L3/L3-P06/starter/README.md
L3/L3-P06/starter/babel.config.cjs
L3/L3-P06/starter/e2e/example.spec.ts
L3/L3-P06/starter/eslint.config.mjs
L3/L3-P06/starter/jest.config.cjs
L3/L3-P06/starter/package.json
L3/L3-P06/starter/playwright.config.ts
L3/L3-P06/starter/public/index.html
L3/L3-P06/starter/public/manifest.webmanifest
L3/L3-P06/starter/public/register-sw.js
L3/L3-P06/starter/scripts/build-sw.mjs
L3/L3-P06/starter/src/app.js
L3/L3-P06/starter/src/index.js
L3/L3-P06/starter/tests/jest/spec.jest.test.js
L3/L3-P06/starter/tests/vitest/spec.test.js
L3/L3-P06/starter/vitest.config.ts
L3/L3-P07/solution/.env.example
L3/L3-P07/solution/.gitignore
L3/L3-P07/solution/README.md
L3/L3-P07/solution/babel.config.cjs
L3/L3-P07/solution/e2e/example.spec.ts
L3/L3-P07/solution/eslint.config.mjs
L3/L3-P07/solution/jest.config.cjs
L3/L3-P07/solution/package.json
L3/L3-P07/solution/playwright.config.ts
L3/L3-P07/solution/public/index.html
L3/L3-P07/solution/public/manifest.webmanifest
L3/L3-P07/solution/public/register-sw.js
L3/L3-P07/solution/scripts/build-sw.mjs
L3/L3-P07/solution/src/app.js
L3/L3-P07/solution/src/index.js
L3/L3-P07/solution/tests/jest/spec.jest.test.js
L3/L3-P07/solution/tests/vitest/spec.test.js
L3/L3-P07/solution/vitest.config.ts
L3/L3-P07/starter/.env.example
L3/L3-P07/starter/.gitignore
L3/L3-P07/starter/README.md
L3/L3-P07/starter/babel.config.cjs
L3/L3-P07/starter/e2e/example.spec.ts
L3/L3-P07/starter/eslint.config.mjs
L3/L3-P07/starter/jest.config.cjs
L3/L3-P07/starter/package.json
L3/L3-P07/starter/playwright.config.ts
L3/L3-P07/starter/public/index.html
L3/L3-P07/starter/public/manifest.webmanifest
L3/L3-P07/starter/public/register-sw.js
L3/L3-P07/starter/scripts/build-sw.mjs
L3/L3-P07/starter/src/app.js
L3/L3-P07/starter/src/index.js
L3/L3-P07/starter/tests/jest/spec.jest.test.js
L3/L3-P07/starter/tests/vitest/spec.test.js
L3/L3-P07/starter/vitest.config.ts
L3/L3-P08/solution/.env.example
L3/L3-P08/solution/.gitignore
L3/L3-P08/solution/README.md
L3/L3-P08/solution/babel.config.cjs
L3/L3-P08/solution/e2e/example.spec.ts
L3/L3-P08/solution/eslint.config.mjs
L3/L3-P08/solution/jest.config.cjs
L3/L3-P08/solution/package.json
L3/L3-P08/solution/playwright.config.ts
L3/L3-P08/solution/public/index.html
L3/L3-P08/solution/public/manifest.webmanifest
L3/L3-P08/solution/public/register-sw.js
L3/L3-P08/solution/scripts/build-sw.mjs
L3/L3-P08/solution/src/app.js
L3/L3-P08/solution/src/index.js
L3/L3-P08/solution/tests/jest/spec.jest.test.js
L3/L3-P08/solution/tests/vitest/spec.test.js
L3/L3-P08/solution/vitest.config.ts
L3/L3-P08/starter/.env.example
L3/L3-P08/starter/.gitignore
L3/L3-P08/starter/README.md
L3/L3-P08/starter/babel.config.cjs
L3/L3-P08/starter/e2e/example.spec.ts
L3/L3-P08/starter/eslint.config.mjs
L3/L3-P08/starter/jest.config.cjs
L3/L3-P08/starter/package.json
L3/L3-P08/starter/playwright.config.ts
L3/L3-P08/starter/public/index.html
L3/L3-P08/starter/public/manifest.webmanifest
L3/L3-P08/starter/public/register-sw.js
L3/L3-P08/starter/scripts/build-sw.mjs
L3/L3-P08/starter/src/app.js
L3/L3-P08/starter/src/index.js
L3/L3-P08/starter/tests/jest/spec.jest.test.js
L3/L3-P08/starter/tests/vitest/spec.test.js
L3/L3-P08/starter/vitest.config.ts
L3/L3-P09/solution/.env.example
L3/L3-P09/solution/.gitignore
L3/L3-P09/solution/README.md
L3/L3-P09/solution/babel.config.cjs
L3/L3-P09/solution/e2e/example.spec.ts
L3/L3-P09/solution/eslint.config.mjs
L3/L3-P09/solution/jest.config.cjs
L3/L3-P09/solution/package.json
L3/L3-P09/solution/playwright.config.ts
L3/L3-P09/solution/public/index.html
L3/L3-P09/solution/public/manifest.webmanifest
L3/L3-P09/solution/public/register-sw.js
L3/L3-P09/solution/scripts/build-sw.mjs
L3/L3-P09/solution/src/app.js
L3/L3-P09/solution/src/index.js
L3/L3-P09/solution/tests/jest/spec.jest.test.js
L3/L3-P09/solution/tests/vitest/spec.test.js
L3/L3-P09/solution/vitest.config.ts
L3/L3-P09/starter/.env.example
L3/L3-P09/starter/.gitignore
L3/L3-P09/starter/README.md
L3/L3-P09/starter/babel.config.cjs
L3/L3-P09/starter/e2e/example.spec.ts
L3/L3-P09/starter/eslint.config.mjs
L3/L3-P09/starter/jest.config.cjs
L3/L3-P09/starter/package.json
L3/L3-P09/starter/playwright.config.ts
L3/L3-P09/starter/public/index.html
L3/L3-P09/starter/public/manifest.webmanifest
L3/L3-P09/starter/public/register-sw.js
L3/L3-P09/starter/scripts/build-sw.mjs
L3/L3-P09/starter/src/app.js
L3/L3-P09/starter/src/index.js
L3/L3-P09/starter/tests/jest/spec.jest.test.js
L3/L3-P09/starter/tests/vitest/spec.test.js
L3/L3-P09/starter/vitest.config.ts
L3/L3-P10/solution/.env.example
L3/L3-P10/solution/.gitignore
L3/L3-P10/solution/README.md
L3/L3-P10/solution/babel.config.cjs
L3/L3-P10/solution/e2e/example.spec.ts
L3/L3-P10/solution/eslint.config.mjs
L3/L3-P10/solution/jest.config.cjs
L3/L3-P10/solution/package.json
L3/L3-P10/solution/playwright.config.ts
L3/L3-P10/solution/public/index.html
L3/L3-P10/solution/public/manifest.webmanifest
L3/L3-P10/solution/public/register-sw.js
L3/L3-P10/solution/scripts/build-sw.mjs
L3/L3-P10/solution/src/app.js
L3/L3-P10/solution/src/index.js
L3/L3-P10/solution/tests/jest/spec.jest.test.js
L3/L3-P10/solution/tests/vitest/spec.test.js
L3/L3-P10/solution/vitest.config.ts
L3/L3-P10/starter/.env.example
L3/L3-P10/starter/.gitignore
L3/L3-P10/starter/README.md
L3/L3-P10/starter/babel.config.cjs
L3/L3-P10/starter/e2e/example.spec.ts
L3/L3-P10/starter/eslint.config.mjs
L3/L3-P10/starter/jest.config.cjs
L3/L3-P10/starter/package.json
L3/L3-P10/starter/playwright.config.ts
L3/L3-P10/starter/public/index.html
L3/L3-P10/starter/public/manifest.webmanifest
L3/L3-P10/starter/public/register-sw.js
L3/L3-P10/starter/scripts/build-sw.mjs
L3/L3-P10/starter/src/app.js
L3/L3-P10/starter/src/index.js
L3/L3-P10/starter/tests/jest/spec.jest.test.js
L3/L3-P10/starter/tests/vitest/spec.test.js
L3/L3-P10/starter/vitest.config.ts
L3/L3-P11/solution/.env.example
L3/L3-P11/solution/.gitignore
L3/L3-P11/solution/README.md
L3/L3-P11/solution/babel.config.cjs
L3/L3-P11/solution/e2e/example.spec.ts
L3/L3-P11/solution/eslint.config.mjs
L3/L3-P11/solution/jest.config.cjs
L3/L3-P11/solution/package.json
L3/L3-P11/solution/playwright.config.ts
L3/L3-P11/solution/public/index.html
L3/L3-P11/solution/public/manifest.webmanifest
L3/L3-P11/solution/public/register-sw.js
L3/L3-P11/solution/scripts/build-sw.mjs
L3/L3-P11/solution/src/app.js
L3/L3-P11/solution/src/index.js
L3/L3-P11/solution/tests/jest/spec.jest.test.js
L3/L3-P11/solution/tests/vitest/spec.test.js
L3/L3-P11/solution/vitest.config.ts
L3/L3-P11/starter/.env.example
L3/L3-P11/starter/.gitignore
L3/L3-P11/starter/README.md
L3/L3-P11/starter/babel.config.cjs
L3/L3-P11/starter/e2e/example.spec.ts
L3/L3-P11/starter/eslint.config.mjs
L3/L3-P11/starter/jest.config.cjs
L3/L3-P11/starter/package.json
L3/L3-P11/starter/playwright.config.ts
L3/L3-P11/starter/public/index.html
L3/L3-P11/starter/public/manifest.webmanifest
L3/L3-P11/starter/public/register-sw.js
L3/L3-P11/starter/scripts/build-sw.mjs
L3/L3-P11/starter/src/app.js
L3/L3-P11/starter/src/index.js
L3/L3-P11/starter/tests/jest/spec.jest.test.js
L3/L3-P11/starter/tests/vitest/spec.test.js
L3/L3-P11/starter/vitest.config.ts
L3/L3-P12/solution/.env.example
L3/L3-P12/solution/.gitignore
L3/L3-P12/solution/README.md
L3/L3-P12/solution/babel.config.cjs
L3/L3-P12/solution/e2e/example.spec.ts
L3/L3-P12/solution/eslint.config.mjs
L3/L3-P12/solution/jest.config.cjs
L3/L3-P12/solution/package.json
L3/L3-P12/solution/playwright.config.ts
L3/L3-P12/solution/public/index.html
L3/L3-P12/solution/public/manifest.webmanifest
L3/L3-P12/solution/public/register-sw.js
L3/L3-P12/solution/scripts/build-sw.mjs
L3/L3-P12/solution/src/app.js
L3/L3-P12/solution/src/index.js
L3/L3-P12/solution/tests/jest/spec.jest.test.js
L3/L3-P12/solution/tests/vitest/spec.test.js
L3/L3-P12/solution/vitest.config.ts
L3/L3-P12/starter/.env.example
L3/L3-P12/starter/.gitignore
L3/L3-P12/starter/README.md
L3/L3-P12/starter/babel.config.cjs
L3/L3-P12/starter/e2e/example.spec.ts
L3/L3-P12/starter/eslint.config.mjs
L3/L3-P12/starter/jest.config.cjs
L3/L3-P12/starter/package.json
L3/L3-P12/starter/playwright.config.ts
L3/L3-P12/starter/public/index.html
L3/L3-P12/starter/public/manifest.webmanifest
L3/L3-P12/starter/public/register-sw.js
L3/L3-P12/starter/scripts/build-sw.mjs
L3/L3-P12/starter/src/app.js
L3/L3-P12/starter/src/index.js
L3/L3-P12/starter/tests/jest/spec.jest.test.js
L3/L3-P12/starter/tests/vitest/spec.test.js
L3/L3-P12/starter/vitest.config.ts
L3/L3-P13/solution/.env.example
L3/L3-P13/solution/.gitignore
L3/L3-P13/solution/README.md
L3/L3-P13/solution/babel.config.cjs
L3/L3-P13/solution/e2e/example.spec.ts
L3/L3-P13/solution/eslint.config.mjs
L3/L3-P13/solution/jest.config.cjs
L3/L3-P13/solution/package.json
L3/L3-P13/solution/playwright.config.ts
L3/L3-P13/solution/public/index.html
L3/L3-P13/solution/public/manifest.webmanifest
L3/L3-P13/solution/public/register-sw.js
L3/L3-P13/solution/scripts/build-sw.mjs
L3/L3-P13/solution/src/app.js
L3/L3-P13/solution/src/index.js
L3/L3-P13/solution/tests/jest/spec.jest.test.js
L3/L3-P13/solution/tests/vitest/spec.test.js
L3/L3-P13/solution/vitest.config.ts
L3/L3-P13/starter/.env.example
L3/L3-P13/starter/.gitignore
L3/L3-P13/starter/README.md
L3/L3-P13/starter/babel.config.cjs
L3/L3-P13/starter/e2e/example.spec.ts
L3/L3-P13/starter/eslint.config.mjs
L3/L3-P13/starter/jest.config.cjs
L3/L3-P13/starter/package.json
L3/L3-P13/starter/playwright.config.ts
L3/L3-P13/starter/public/index.html
L3/L3-P13/starter/public/manifest.webmanifest
L3/L3-P13/starter/public/register-sw.js
L3/L3-P13/starter/scripts/build-sw.mjs
L3/L3-P13/starter/src/app.js
L3/L3-P13/starter/src/index.js
L3/L3-P13/starter/tests/jest/spec.jest.test.js
L3/L3-P13/starter/tests/vitest/spec.test.js
L3/L3-P13/starter/vitest.config.ts
L3/L3-P14/solution/.env.example
L3/L3-P14/solution/.gitignore
L3/L3-P14/solution/README.md
L3/L3-P14/solution/babel.config.cjs
L3/L3-P14/solution/e2e/example.spec.ts
L3/L3-P14/solution/eslint.config.mjs
L3/L3-P14/solution/jest.config.cjs
L3/L3-P14/solution/package.json
L3/L3-P14/solution/playwright.config.ts
L3/L3-P14/solution/public/index.html
L3/L3-P14/solution/public/manifest.webmanifest
L3/L3-P14/solution/public/register-sw.js
L3/L3-P14/solution/scripts/build-sw.mjs
L3/L3-P14/solution/src/app.js
L3/L3-P14/solution/src/index.js
L3/L3-P14/solution/tests/jest/spec.jest.test.js
L3/L3-P14/solution/tests/vitest/spec.test.js
L3/L3-P14/solution/vitest.config.ts
L3/L3-P14/starter/.env.example
L3/L3-P14/starter/.gitignore
L3/L3-P14/starter/README.md
L3/L3-P14/starter/babel.config.cjs
L3/L3-P14/starter/e2e/example.spec.ts
L3/L3-P14/starter/eslint.config.mjs
L3/L3-P14/starter/jest.config.cjs
L3/L3-P14/starter/package.json
L3/L3-P14/starter/playwright.config.ts
L3/L3-P14/starter/public/index.html
L3/L3-P14/starter/public/manifest.webmanifest
L3/L3-P14/starter/public/register-sw.js
L3/L3-P14/starter/scripts/build-sw.mjs
L3/L3-P14/starter/src/app.js
L3/L3-P14/starter/src/index.js
L3/L3-P14/starter/tests/jest/spec.jest.test.js
L3/L3-P14/starter/tests/vitest/spec.test.js
L3/L3-P14/starter/vitest.config.ts
L3/L3-P15/solution/.env.example
L3/L3-P15/solution/.gitignore
L3/L3-P15/solution/README.md
L3/L3-P15/solution/babel.config.cjs
L3/L3-P15/solution/e2e/example.spec.ts
L3/L3-P15/solution/eslint.config.mjs
L3/L3-P15/solution/jest.config.cjs
L3/L3-P15/solution/package.json
L3/L3-P15/solution/playwright.config.ts
L3/L3-P15/solution/public/index.html
L3/L3-P15/solution/public/manifest.webmanifest
L3/L3-P15/solution/public/register-sw.js
L3/L3-P15/solution/scripts/build-sw.mjs
L3/L3-P15/solution/src/app.js
L3/L3-P15/solution/src/index.js
L3/L3-P15/solution/tests/jest/spec.jest.test.js
L3/L3-P15/solution/tests/vitest/spec.test.js
L3/L3-P15/solution/vitest.config.ts
L3/L3-P15/starter/.env.example
L3/L3-P15/starter/.gitignore
L3/L3-P15/starter/README.md
L3/L3-P15/starter/babel.config.cjs
L3/L3-P15/starter/e2e/example.spec.ts
L3/L3-P15/starter/eslint.config.mjs
L3/L3-P15/starter/jest.config.cjs
L3/L3-P15/starter/package.json
L3/L3-P15/starter/playwright.config.ts
L3/L3-P15/starter/public/index.html
L3/L3-P15/starter/public/manifest.webmanifest
L3/L3-P15/starter/public/register-sw.js
L3/L3-P15/starter/scripts/build-sw.mjs
L3/L3-P15/starter/src/app.js
L3/L3-P15/starter/src/index.js
L3/L3-P15/starter/tests/jest/spec.jest.test.js
L3/L3-P15/starter/tests/vitest/spec.test.js
L3/L3-P15/starter/vitest.config.ts
```

**Variante detectate:** solution: 660, starter: 660.

**Categorii de fișiere:** config: 660, other: 150, public: 150, code: 180, tests: 180, ci: 5.

**package.json — sinteză scripturi & workspaces**

- `L1/L1-P01/starter/package.json`: name=`l1-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P01/solution/package.json`: name=`l1-p01-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P02/starter/package.json`: name=`l1-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P02/solution/package.json`: name=`l1-p02-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P03/starter/package.json`: name=`l1-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P03/solution/package.json`: name=`l1-p03-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P04/starter/package.json`: name=`l1-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P04/solution/package.json`: name=`l1-p04-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P05/starter/package.json`: name=`l1-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P05/solution/package.json`: name=`l1-p05-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P06/starter/package.json`: name=`l1-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P06/solution/package.json`: name=`l1-p06-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P07/starter/package.json`: name=`l1-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P07/solution/package.json`: name=`l1-p07-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P08/starter/package.json`: name=`l1-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P08/solution/package.json`: name=`l1-p08-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P09/starter/package.json`: name=`l1-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P09/solution/package.json`: name=`l1-p09-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P10/starter/package.json`: name=`l1-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P10/solution/package.json`: name=`l1-p10-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P11/starter/package.json`: name=`l1-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P11/solution/package.json`: name=`l1-p11-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P12/starter/package.json`: name=`l1-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P12/solution/package.json`: name=`l1-p12-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P13/starter/package.json`: name=`l1-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P13/solution/package.json`: name=`l1-p13-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P14/starter/package.json`: name=`l1-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P14/solution/package.json`: name=`l1-p14-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P15/starter/package.json`: name=`l1-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L1/L1-P15/solution/package.json`: name=`l1-p15-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P01/starter/package.json`: name=`l2-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P01/solution/package.json`: name=`l2-p01-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P02/starter/package.json`: name=`l2-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P02/solution/package.json`: name=`l2-p02-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P03/starter/package.json`: name=`l2-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P03/solution/package.json`: name=`l2-p03-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P04/starter/package.json`: name=`l2-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P04/solution/package.json`: name=`l2-p04-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P05/starter/package.json`: name=`l2-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P05/solution/package.json`: name=`l2-p05-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P06/starter/package.json`: name=`l2-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P06/solution/package.json`: name=`l2-p06-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P07/starter/package.json`: name=`l2-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P07/solution/package.json`: name=`l2-p07-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P08/starter/package.json`: name=`l2-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P08/solution/package.json`: name=`l2-p08-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P09/starter/package.json`: name=`l2-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P09/solution/package.json`: name=`l2-p09-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P10/starter/package.json`: name=`l2-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P10/solution/package.json`: name=`l2-p10-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P11/starter/package.json`: name=`l2-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P11/solution/package.json`: name=`l2-p11-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P12/starter/package.json`: name=`l2-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P12/solution/package.json`: name=`l2-p12-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P13/starter/package.json`: name=`l2-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P13/solution/package.json`: name=`l2-p13-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P14/starter/package.json`: name=`l2-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P14/solution/package.json`: name=`l2-p14-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P15/starter/package.json`: name=`l2-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L2/L2-P15/solution/package.json`: name=`l2-p15-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js
- `L3/L3-P01/starter/package.json`: name=`l3-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P01/solution/package.json`: name=`l3-p01-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P02/starter/package.json`: name=`l3-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P02/solution/package.json`: name=`l3-p02-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P03/starter/package.json`: name=`l3-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P03/solution/package.json`: name=`l3-p03-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P04/starter/package.json`: name=`l3-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P04/solution/package.json`: name=`l3-p04-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P05/starter/package.json`: name=`l3-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P05/solution/package.json`: name=`l3-p05-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P06/starter/package.json`: name=`l3-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P06/solution/package.json`: name=`l3-p06-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P07/starter/package.json`: name=`l3-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P07/solution/package.json`: name=`l3-p07-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P08/starter/package.json`: name=`l3-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P08/solution/package.json`: name=`l3-p08-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P09/starter/package.json`: name=`l3-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P09/solution/package.json`: name=`l3-p09-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P10/starter/package.json`: name=`l3-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P10/solution/package.json`: name=`l3-p10-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P11/starter/package.json`: name=`l3-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P11/solution/package.json`: name=`l3-p11-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P12/starter/package.json`: name=`l3-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P12/solution/package.json`: name=`l3-p12-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P13/starter/package.json`: name=`l3-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P13/solution/package.json`: name=`l3-p13-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P14/starter/package.json`: name=`l3-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P14/solution/package.json`: name=`l3-p14-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P15/starter/package.json`: name=`l3-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P15/solution/package.json`: name=`l3-p15-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `nodemon src/index.js`
  - `start` → `node src/index.js`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** express, dotenv
  - **DevDeps:** nodemon, vitest, jest, babel-jest, @babel/preset-env, supertest, eslint, @eslint/js, @playwright/test, workbox-build

### Seminar0_Partea3_p3-READMEs_v2.zip

```
L1/L1-P01/solution-README.md
L1/L1-P01/starter-README.md
L1/L1-P02/solution-README.md
L1/L1-P02/starter-README.md
L1/L1-P03/solution-README.md
L1/L1-P03/starter-README.md
L1/L1-P04/solution-README.md
L1/L1-P04/starter-README.md
L1/L1-P05/solution-README.md
L1/L1-P05/starter-README.md
L1/L1-P06/solution-README.md
L1/L1-P06/starter-README.md
L1/L1-P07/solution-README.md
L1/L1-P07/starter-README.md
L1/L1-P08/solution-README.md
L1/L1-P08/starter-README.md
L1/L1-P09/solution-README.md
L1/L1-P09/starter-README.md
L1/L1-P10/solution-README.md
L1/L1-P10/starter-README.md
L1/L1-P11/solution-README.md
L1/L1-P11/starter-README.md
L1/L1-P12/solution-README.md
L1/L1-P12/starter-README.md
L1/L1-P13/solution-README.md
L1/L1-P13/starter-README.md
L1/L1-P14/solution-README.md
L1/L1-P14/starter-README.md
L1/L1-P15/solution-README.md
L1/L1-P15/starter-README.md
L2/L2-P01/solution-README.md
L2/L2-P01/starter-README.md
L2/L2-P02/solution-README.md
L2/L2-P02/starter-README.md
L2/L2-P03/solution-README.md
L2/L2-P03/starter-README.md
L2/L2-P04/solution-README.md
L2/L2-P04/starter-README.md
L2/L2-P05/solution-README.md
L2/L2-P05/starter-README.md
L2/L2-P06/solution-README.md
L2/L2-P06/starter-README.md
L2/L2-P07/solution-README.md
L2/L2-P07/starter-README.md
L2/L2-P08/solution-README.md
L2/L2-P08/starter-README.md
L2/L2-P09/solution-README.md
L2/L2-P09/starter-README.md
L2/L2-P10/solution-README.md
L2/L2-P10/starter-README.md
L2/L2-P11/solution-README.md
L2/L2-P11/starter-README.md
L2/L2-P12/solution-README.md
L2/L2-P12/starter-README.md
L2/L2-P13/solution-README.md
L2/L2-P13/starter-README.md
L2/L2-P14/solution-README.md
L2/L2-P14/starter-README.md
L2/L2-P15/solution-README.md
L2/L2-P15/starter-README.md
L3/L3-P01/solution-README.md
L3/L3-P01/starter-README.md
L3/L3-P02/solution-README.md
L3/L3-P02/starter-README.md
L3/L3-P03/solution-README.md
L3/L3-P03/starter-README.md
L3/L3-P04/solution-README.md
L3/L3-P04/starter-README.md
L3/L3-P05/solution-README.md
L3/L3-P05/starter-README.md
L3/L3-P06/solution-README.md
L3/L3-P06/starter-README.md
L3/L3-P07/solution-README.md
L3/L3-P07/starter-README.md
L3/L3-P08/solution-README.md
L3/L3-P08/starter-README.md
L3/L3-P09/solution-README.md
L3/L3-P09/starter-README.md
L3/L3-P10/solution-README.md
L3/L3-P10/starter-README.md
L3/L3-P11/solution-README.md
L3/L3-P11/starter-README.md
L3/L3-P12/solution-README.md
L3/L3-P12/starter-README.md
L3/L3-P13/solution-README.md
L3/L3-P13/starter-README.md
L3/L3-P14/solution-README.md
L3/L3-P14/starter-README.md
L3/L3-P15/solution-README.md
L3/L3-P15/starter-README.md
```

**Variante detectate:** solution: 45, starter: 45.

**Categorii de fișiere:** other: 90.

## 2. Sinteza documentelor DOCX (teorie ↔ laborator ↔ proiecte)

### Seminar0_Partea1_Teorie_extins.docx

**Titluri/Heading‑uri:**

- Seminarul 0 — Partea 1 (Teorie, extins)
- Hook realist: De ce un „toolchain” bun îți salvează timpul și proiectul
- Imaginează‑ți un atelier mecanic. Ai pe masă scule fără etichete, lipsesc cheile potrivite, nu știi unde este manualul
și fiecare rotiță se potrivește doar dacă o lovești insistent. În programare, un „atelier” prost organizat înseamnă
timp pierdut în depanare, bug‑uri greu de reprodus, diferențe între mediul tău și al colegilor, versiuni de biblioteci
incompatibile și, în final, o arhitectură fragilă. Seminarul introductiv este exact acel moment în care deschidem cutia cu scule,
ordonăm uneltele, stabilim regulile de lucru și lipim etichete clare.

### Seminar0_Partea2_Ghid_Arhive.docx

**Titluri/Heading‑uri:**

- Ghid — Arhive Seminarul 0 (Laborator)
- Acest ghid descrie conținutul arhivelor livrate și pașii de utilizare.
- ## Arhive livrate

### Seminar0_Partea2_Laborator_extins.docx

**Titluri/Heading‑uri:**

- Seminarul 0 — Partea 2 (Laborator extins)
- Scopul laboratorului și logica progresivă
- Acest laborator transformă conceptele din Partea 1 într‑un proiect funcțional, testabil și reproductibil.
Veți porni de la un repository gol, veți inițializa un proiect Node (ESM), veți ridica un server Express minimal care servește
fișiere statice și expune rute simple (`/ping`, `/api/time`), apoi veți scrie **teste unitare** și **de contract** în **Vitest** și **Jest**,
în oglindă. Lucrarea este însoțită de un **worksheet** (cerință + checklist) și de un **starter** gata de rulat (în arhivele ZIP).

### Seminar0_Partea3_Arhive_Ghid_v2.docx

**Titluri/Heading‑uri:**

- Ghid — Arhive (Seminarul 0, Partea 3 — v2)
- Livrabile _v2: `s0p3-standalone_v2.zip`, `s0p3-monorepo_v2.zip`, `s0p3-readmes_v2.zip`. Prima include toate proiectele (starter+solution) cu workflows CI; a doua — doar starter-ele în PNPM workspaces; a treia — toate README-urile.
- ### Rulare rapidă — standalone
cd s0p3-standalone_v2/L1/L1-P01/starter
npm i
npm test
npm run dev

### Seminar0_Partea3_Proiecte_extins_v2.docx

**Titluri/Heading‑uri:**

- Seminarul 0 — Partea 3 (Proiecte/teme extinse — v2)
- Această versiune reface integral livrabilele pentru Partea 3: 45 proiecte (L1-L3) cu variante `starter/` și `solution/`, testare dublă (Vitest & Jest), iar pentru L3 — Playwright e2e + Workbox PWA. Arhivele ZIP (_v2) și ghidul asociat sunt incluse separat.
- # L1 — Fundamental

## 3. Monorepo vs. standalone — analiză comparativă


**Manageri de pachete & workspaces.** Variantele monorepo folosesc `pnpm-workspace.yaml` și/sau `workspaces` în `package.json`, permițând instalarea pe rădăcină (`pnpm i -w`) și rularea țintită (`pnpm --filter`). Standalone folosește `npm` local, izolând dependențele per proiect.

**Comenzi de instalare/testare.** Monorepo: `pnpm i -w`, `pnpm --filter <pkg> run test`. Standalone: `npm i`, `npm test`. În ambele cazuri, scripturile includ de regulă `test:vitest` și `test:jest`, agregate în `test`.

**Integrare CI.** Monorepo tinde spre workflows unificate („unit.yml” pe `packages/*`), în timp ce standalone are workflows per proiect (ex. `unit-vitest.yml`, `unit-jest.yml`, `lint.yml`, `e2e-l3.yml`).

**Avantaje/Dezavantaje.** Pentru începători, standalone reduce complexitatea cognitivă (un singur `package.json`, o singură cale). Monorepo devine preferabil când există multe proiecte/variante (starter/solution, L1–L3) și când CI trebuie orchestrat pe matrice. Dezavantajul monorepo este înțelegerea corectă a frontierelor pachetelor și a comenzii `--filter` (și a cache‑ului PNPM). 
## 4. Rolul fișierelor cheie (config, cod, teste, extra)

| Fișier / tip | Rol |
|---|---|
| `package.json` | Manifestul proiectului: metadate, dependențe, scripturi. Activează ESM prin `type: "module"`. |
| `pnpm-workspace.yaml` | Declară pachetele din monorepo și domeniul instalării la rădăcină. |
| `vitest.config.ts` | Configurarea Vitest (mediul `node`, reporters). |
| `jest.config.cjs` | Configurare Jest (ESM via `babel-jest`, `extensionsToTreatAsEsm`). |
| `babel.config.cjs` | Transformări Babel pentru Jest (`@babel/preset-env`). |
| `.gitignore` | Exclude fișiere/foldere (ex. `node_modules/`, `.env`). |
| `.env.example` | Sablon variabile mediu (ex. `PORT=`); nu se comite `.env` real. |
| `src/app.js` | „Fabrica” Express `createApp()`: middleware JSON/static, rute, handlere 404/500. |
| `src/index.js` | Entrypoint: citește `.env` (prin `dotenv`), pornește serverul pe `PORT`. |
| `public/index.html` | Activ static; dovada servării corecte, verificat în teste și e2e. |

## 5. Corelații cod ↔ configurări ↔ teste


- **Rutele din `src/app.js`** (`/ping`, `/api/time`, eventual `/` static) sunt verificate prin suite **Vitest** și **Jest** (aceleași aserții, două motoare), utilizând `supertest` pentru a simula request‑uri fără a deschide porturi. 
- **`.env.example`** documentează variabilele (e.g., `PORT`), citite în **`src/index.js`** cu `dotenv.config()`. Această decuplare permite suprascrierea portului în CI/e2e.
- **ESLint + CI**: reguli statice (flat config) executate local (`npm run lint`) și în workflows (`lint.yml`), blocând PR‑uri care introduc anti‑pattern‑uri (e.g., variabile nefolosite). Suitelor unitare li se alătură **Playwright** pentru testare e2e (L3) și **Workbox** pentru generarea `sw.js` (PWA), ambele orchestrate din `.github/workflows/*`.
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Acest pachet reunește variante **standalone** și **monorepo** pentru Seminarul 0, aliniind teoria (toolchain, ESM, Express) cu laboratorul (server minimal, rute, teste duble Vitest/Jest) și cu proiectele (L1–L3, inclusiv e2e și PWA). Scopul este un demaraj reproductibil și o rutină profesională (test‑first, CI, calitate). Referințele detaliate din ghidurile DOCX se mapază pe structurile arhivelor ZIP prin convenții consistente (nume de directoare, scripturi, workflows).### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM/Yarn workspaces) |
|---|---|---|
| Complexitate cognitivă | Redusă; un singur `package.json` | Mai ridicată; rădăcină + pachete |
| Instalare | `npm i` în proiect | `pnpm i -w` la rădăcină |
| Rulare teste | `npm test` | `pnpm --filter <pkg> run test` |
| CI | Workflows per proiect | Workflows unificate pe `packages/*` |
| Scalare (L1–L3, starter/solution) | Multiplicare fișiere | Organizare în pachete |
| Începători vs. avansați | Recomandat pentru start | Recomandat pentru colecții mari & CI complex |
### Inventar pe arhivă (roluri)

- **Seminar0_Partea2_lab-monorepo.zip** — conține: config=8, other=1, public=1, code=2, tests=2.
- **Seminar0_Partea2_lab-standalone.zip** — conține: config=6, other=1, public=1, code=2, tests=2.
- **Seminar0_Partea3_p3-monorepo_v2.zip** — conține: config=332, other=75, public=75, code=90, tests=90, ci=3.
- **Seminar0_Partea3_p3-standalone_v2.zip** — conține: config=660, other=150, public=150, code=180, tests=180, ci=5.
- **Seminar0_Partea3_p3-READMEs_v2.zip** — conține: other=90.
### Explicații fișier‑cu‑fișier

Consultați tabelul din §4; în plus, pentru fișiere specifice L3:

- `playwright.config.*` — definirea proiectelor e2e (browsere, timeouturi, retries).
- `public/manifest.webmanifest` (dacă prezent) — metadate PWA; corelat cu `sw.js`.
- `.github/workflows/e2e-l3.yml` — secvență e2e (instalare deps, build, server ephemeral, Playwright).
### Corelații între fișiere


- `src/app.js` ↔ `tests/*` (Vitest/Jest): contracte pentru rute & headere.
- `src/index.js` ↔ `.env.example`: parametrizare `PORT` și moduri `NODE_ENV`.
- `.github/workflows/*` ↔ `eslint.config.js`/`jest.config.cjs`/`vitest.config.ts`: pipeline validat cap‑la‑cap.
- `public/*` ↔ `workbox-config.js`/`sw.js`: precache și offline pentru L3.
### Recomandări pentru studenți


1) **Începeți în standalone.** După înțelegerea fluxului, migrați spre monorepo pentru proiecte multiple.  
2) **Test‑first.** Scrieți/rulați testele la fiecare pas; mențineți suitele Vitest/Jest sincronizate.  
3) **ESM disciplinat.** Importuri cu extensii `.js`; separați `createApp()` de `listen()`.  
4) **Calitate.** Activați ESLint/Prettier; rulați `npm run lint` local înainte de commit.  
5) **CI ca gardian.** Păstrați workflows simple și deterministe; folosiți matrice doar când adaugă valoare.  
6) **Versionare.** Mesaje de commit clare (Conventional Commits), ramuri feature și PR-uri cu review.  
### Instrucțiuni „Quick start”


**Standalone (laborator Partea 2):**
```bash
cd s0-lab-standalone
npm i
npm test
npm run dev    # sau: npm start
```

**Monorepo (laborator Partea 2):**
```bash
cd s0-lab-monorepo
pnpm i -w
pnpm --filter app run test
pnpm --filter app run dev
```

**Proiecte v2 — standalone (Partea 3):**
```bash
cd s0p3-standalone_v2/L1/L1-P01/starter
npm i
npm test
npm run dev
```

**Proiecte v2 — monorepo (Partea 3):**
```bash
cd s0p3-monorepo_v2
pnpm i -w
pnpm --filter l1-p01-starter run test
pnpm --filter l1-p01-starter run dev
```
### Troubleshooting (erori frecvente)


- `EADDRINUSE: 3000` → setați `PORT` în `.env` (consultați `.env.example`), reporniți.  
- `ERR_MODULE_NOT_FOUND` (ESM) → adăugați extensiile `.js` în importuri; păstrați `"type": "module"`.  
- `SyntaxError: Cannot use import statement outside a module` (Jest) → asigurați `babel-jest` + `extensionsToTreatAsEsm`.  
- 404 la `/` → verificați `express.static('public')` și existența `public/index.html`.  
- Playwright nu lansează browserul → rulați `npx playwright install` sau un script `pw:install`.  
- `pnpm --filter` nu găsește pachetul → verificați `pnpm-workspace.yaml` și `name` în `packages/*/package.json`.  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** fundamentează alegerea ESM, separația `createApp()`/`listen()`, și rolul `.env` (→ implementate în arhive).  
- **Partea 2 (Laborator)** detaliază checklist‑ul și testele în oglindă Vitest/Jest (→ regăsite în `tests/` și în scripturile `test:*`).  
- **Partea 3 (Proiecte)** escaladează către e2e (Playwright) și PWA (Workbox) cu workflows CI dedicate (→ `.github/workflows/*`).  
### Prompt‑șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul Sx** (standalone & monorepo) un proiect Node/Express (ESM) cu `createApp()`, rutele `/ping`, `/api/time`, servire `public/index.html`, testare dublă **Vitest**/**Jest** cu `supertest`, plus CI (lint, unit, e2e pentru L3) și, opțional, Workbox pentru PWA. Produce **starter** și **solution**, README cu Quick start și Troubleshooting.”
