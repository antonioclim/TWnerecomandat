# Seminarul S1 — Introducere în JavaScript (sintaxă modernă, funcții, iterație, CLI) — Analiză integrată (standalone & monorepo)

*Generat la 2025-09-21 05:30.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar1_Partea2_p2-lab.zip

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
src/lib/filters.js
src/lib/format.js
src/lib/parse.js
src/lib/transform.js
tests/jest/cli.jest.test.js
tests/jest/parse.jest.test.js
tests/jest/transform.jest.test.js
tests/vitest/cli.test.js
tests/vitest/parse.test.js
tests/vitest/transform.test.js
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 6, docs: 1, other: 3, code: 5, tests: 6.

**package.json — sinteză: scripturi, workspaces, bin, dependențe (eșantion)**

- `package.json`: name=`s1p2-lab` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js

### Seminar1_Partea3_p3-monorepo.zip

```
.github/workflows/e2e-l3.yml
.github/workflows/lint.yml
.github/workflows/unit.yml
package.json
packages/l1-p01-starter/.gitignore
packages/l1-p01-starter/README.md
packages/l1-p01-starter/babel.config.cjs
packages/l1-p01-starter/bin/cli.js
packages/l1-p01-starter/data/sample.csv
packages/l1-p01-starter/data/sample.json
packages/l1-p01-starter/eslint.config.mjs
packages/l1-p01-starter/jest.config.cjs
packages/l1-p01-starter/package.json
packages/l1-p01-starter/src/cli-runner.js
packages/l1-p01-starter/src/lib/filters.js
packages/l1-p01-starter/src/lib/format.js
packages/l1-p01-starter/src/lib/parse.js
packages/l1-p01-starter/src/lib/transform.js
packages/l1-p01-starter/tests/jest/cli.jest.test.js
packages/l1-p01-starter/tests/jest/parse.jest.test.js
packages/l1-p01-starter/tests/jest/transform.jest.test.js
packages/l1-p01-starter/tests/vitest/cli.test.js
packages/l1-p01-starter/tests/vitest/parse.test.js
packages/l1-p01-starter/tests/vitest/transform.test.js
packages/l1-p01-starter/vitest.config.ts
packages/l1-p02-starter/.gitignore
packages/l1-p02-starter/README.md
packages/l1-p02-starter/babel.config.cjs
packages/l1-p02-starter/bin/cli.js
packages/l1-p02-starter/data/sample.csv
packages/l1-p02-starter/data/sample.json
packages/l1-p02-starter/eslint.config.mjs
packages/l1-p02-starter/jest.config.cjs
packages/l1-p02-starter/package.json
packages/l1-p02-starter/src/cli-runner.js
packages/l1-p02-starter/src/lib/filters.js
packages/l1-p02-starter/src/lib/format.js
packages/l1-p02-starter/src/lib/parse.js
packages/l1-p02-starter/src/lib/transform.js
packages/l1-p02-starter/tests/jest/cli.jest.test.js
packages/l1-p02-starter/tests/jest/parse.jest.test.js
packages/l1-p02-starter/tests/jest/transform.jest.test.js
packages/l1-p02-starter/tests/vitest/cli.test.js
packages/l1-p02-starter/tests/vitest/parse.test.js
packages/l1-p02-starter/tests/vitest/transform.test.js
packages/l1-p02-starter/vitest.config.ts
packages/l1-p03-starter/.gitignore
packages/l1-p03-starter/README.md
packages/l1-p03-starter/babel.config.cjs
packages/l1-p03-starter/bin/cli.js
packages/l1-p03-starter/data/sample.csv
packages/l1-p03-starter/data/sample.json
packages/l1-p03-starter/eslint.config.mjs
packages/l1-p03-starter/jest.config.cjs
packages/l1-p03-starter/package.json
packages/l1-p03-starter/src/cli-runner.js
packages/l1-p03-starter/src/lib/filters.js
packages/l1-p03-starter/src/lib/format.js
packages/l1-p03-starter/src/lib/parse.js
packages/l1-p03-starter/src/lib/transform.js
packages/l1-p03-starter/tests/jest/cli.jest.test.js
packages/l1-p03-starter/tests/jest/parse.jest.test.js
packages/l1-p03-starter/tests/jest/transform.jest.test.js
packages/l1-p03-starter/tests/vitest/cli.test.js
packages/l1-p03-starter/tests/vitest/parse.test.js
packages/l1-p03-starter/tests/vitest/transform.test.js
packages/l1-p03-starter/vitest.config.ts
packages/l1-p04-starter/.gitignore
packages/l1-p04-starter/README.md
packages/l1-p04-starter/babel.config.cjs
packages/l1-p04-starter/bin/cli.js
packages/l1-p04-starter/data/sample.csv
packages/l1-p04-starter/data/sample.json
packages/l1-p04-starter/eslint.config.mjs
packages/l1-p04-starter/jest.config.cjs
packages/l1-p04-starter/package.json
packages/l1-p04-starter/src/cli-runner.js
packages/l1-p04-starter/src/lib/filters.js
packages/l1-p04-starter/src/lib/format.js
packages/l1-p04-starter/src/lib/parse.js
packages/l1-p04-starter/src/lib/transform.js
packages/l1-p04-starter/tests/jest/cli.jest.test.js
packages/l1-p04-starter/tests/jest/parse.jest.test.js
packages/l1-p04-starter/tests/jest/transform.jest.test.js
packages/l1-p04-starter/tests/vitest/cli.test.js
packages/l1-p04-starter/tests/vitest/parse.test.js
packages/l1-p04-starter/tests/vitest/transform.test.js
packages/l1-p04-starter/vitest.config.ts
packages/l1-p05-starter/.gitignore
packages/l1-p05-starter/README.md
packages/l1-p05-starter/babel.config.cjs
packages/l1-p05-starter/bin/cli.js
packages/l1-p05-starter/data/sample.csv
packages/l1-p05-starter/data/sample.json
packages/l1-p05-starter/eslint.config.mjs
packages/l1-p05-starter/jest.config.cjs
packages/l1-p05-starter/package.json
packages/l1-p05-starter/src/cli-runner.js
packages/l1-p05-starter/src/lib/filters.js
packages/l1-p05-starter/src/lib/format.js
packages/l1-p05-starter/src/lib/parse.js
packages/l1-p05-starter/src/lib/transform.js
packages/l1-p05-starter/tests/jest/cli.jest.test.js
packages/l1-p05-starter/tests/jest/parse.jest.test.js
packages/l1-p05-starter/tests/jest/transform.jest.test.js
packages/l1-p05-starter/tests/vitest/cli.test.js
packages/l1-p05-starter/tests/vitest/parse.test.js
packages/l1-p05-starter/tests/vitest/transform.test.js
packages/l1-p05-starter/vitest.config.ts
packages/l1-p06-starter/.gitignore
packages/l1-p06-starter/README.md
packages/l1-p06-starter/babel.config.cjs
packages/l1-p06-starter/bin/cli.js
packages/l1-p06-starter/data/sample.csv
packages/l1-p06-starter/data/sample.json
packages/l1-p06-starter/eslint.config.mjs
packages/l1-p06-starter/jest.config.cjs
packages/l1-p06-starter/package.json
packages/l1-p06-starter/src/cli-runner.js
packages/l1-p06-starter/src/lib/filters.js
packages/l1-p06-starter/src/lib/format.js
packages/l1-p06-starter/src/lib/parse.js
packages/l1-p06-starter/src/lib/transform.js
packages/l1-p06-starter/tests/jest/cli.jest.test.js
packages/l1-p06-starter/tests/jest/parse.jest.test.js
packages/l1-p06-starter/tests/jest/transform.jest.test.js
packages/l1-p06-starter/tests/vitest/cli.test.js
packages/l1-p06-starter/tests/vitest/parse.test.js
packages/l1-p06-starter/tests/vitest/transform.test.js
packages/l1-p06-starter/vitest.config.ts
packages/l1-p07-starter/.gitignore
packages/l1-p07-starter/README.md
packages/l1-p07-starter/babel.config.cjs
packages/l1-p07-starter/bin/cli.js
packages/l1-p07-starter/data/sample.csv
packages/l1-p07-starter/data/sample.json
packages/l1-p07-starter/eslint.config.mjs
packages/l1-p07-starter/jest.config.cjs
packages/l1-p07-starter/package.json
packages/l1-p07-starter/src/cli-runner.js
packages/l1-p07-starter/src/lib/filters.js
packages/l1-p07-starter/src/lib/format.js
packages/l1-p07-starter/src/lib/parse.js
packages/l1-p07-starter/src/lib/transform.js
packages/l1-p07-starter/tests/jest/cli.jest.test.js
packages/l1-p07-starter/tests/jest/parse.jest.test.js
packages/l1-p07-starter/tests/jest/transform.jest.test.js
packages/l1-p07-starter/tests/vitest/cli.test.js
packages/l1-p07-starter/tests/vitest/parse.test.js
packages/l1-p07-starter/tests/vitest/transform.test.js
packages/l1-p07-starter/vitest.config.ts
packages/l1-p08-starter/.gitignore
packages/l1-p08-starter/README.md
packages/l1-p08-starter/babel.config.cjs
packages/l1-p08-starter/bin/cli.js
packages/l1-p08-starter/data/sample.csv
packages/l1-p08-starter/data/sample.json
packages/l1-p08-starter/eslint.config.mjs
packages/l1-p08-starter/jest.config.cjs
packages/l1-p08-starter/package.json
packages/l1-p08-starter/src/cli-runner.js
packages/l1-p08-starter/src/lib/filters.js
packages/l1-p08-starter/src/lib/format.js
packages/l1-p08-starter/src/lib/parse.js
packages/l1-p08-starter/src/lib/transform.js
packages/l1-p08-starter/tests/jest/cli.jest.test.js
packages/l1-p08-starter/tests/jest/parse.jest.test.js
packages/l1-p08-starter/tests/jest/transform.jest.test.js
packages/l1-p08-starter/tests/vitest/cli.test.js
packages/l1-p08-starter/tests/vitest/parse.test.js
packages/l1-p08-starter/tests/vitest/transform.test.js
packages/l1-p08-starter/vitest.config.ts
packages/l1-p09-starter/.gitignore
packages/l1-p09-starter/README.md
packages/l1-p09-starter/babel.config.cjs
packages/l1-p09-starter/bin/cli.js
packages/l1-p09-starter/data/sample.csv
packages/l1-p09-starter/data/sample.json
packages/l1-p09-starter/eslint.config.mjs
packages/l1-p09-starter/jest.config.cjs
packages/l1-p09-starter/package.json
packages/l1-p09-starter/src/cli-runner.js
packages/l1-p09-starter/src/lib/filters.js
packages/l1-p09-starter/src/lib/format.js
packages/l1-p09-starter/src/lib/parse.js
packages/l1-p09-starter/src/lib/transform.js
packages/l1-p09-starter/tests/jest/cli.jest.test.js
packages/l1-p09-starter/tests/jest/parse.jest.test.js
packages/l1-p09-starter/tests/jest/transform.jest.test.js
packages/l1-p09-starter/tests/vitest/cli.test.js
packages/l1-p09-starter/tests/vitest/parse.test.js
packages/l1-p09-starter/tests/vitest/transform.test.js
packages/l1-p09-starter/vitest.config.ts
packages/l1-p10-starter/.gitignore
packages/l1-p10-starter/README.md
packages/l1-p10-starter/babel.config.cjs
packages/l1-p10-starter/bin/cli.js
packages/l1-p10-starter/data/sample.csv
packages/l1-p10-starter/data/sample.json
packages/l1-p10-starter/eslint.config.mjs
packages/l1-p10-starter/jest.config.cjs
packages/l1-p10-starter/package.json
packages/l1-p10-starter/src/cli-runner.js
packages/l1-p10-starter/src/lib/filters.js
packages/l1-p10-starter/src/lib/format.js
packages/l1-p10-starter/src/lib/parse.js
packages/l1-p10-starter/src/lib/transform.js
packages/l1-p10-starter/tests/jest/cli.jest.test.js
packages/l1-p10-starter/tests/jest/parse.jest.test.js
packages/l1-p10-starter/tests/jest/transform.jest.test.js
packages/l1-p10-starter/tests/vitest/cli.test.js
packages/l1-p10-starter/tests/vitest/parse.test.js
packages/l1-p10-starter/tests/vitest/transform.test.js
packages/l1-p10-starter/vitest.config.ts
packages/l1-p11-starter/.gitignore
packages/l1-p11-starter/README.md
packages/l1-p11-starter/babel.config.cjs
packages/l1-p11-starter/bin/cli.js
packages/l1-p11-starter/data/sample.csv
packages/l1-p11-starter/data/sample.json
packages/l1-p11-starter/eslint.config.mjs
packages/l1-p11-starter/jest.config.cjs
packages/l1-p11-starter/package.json
packages/l1-p11-starter/src/cli-runner.js
packages/l1-p11-starter/src/lib/filters.js
packages/l1-p11-starter/src/lib/format.js
packages/l1-p11-starter/src/lib/parse.js
packages/l1-p11-starter/src/lib/transform.js
packages/l1-p11-starter/tests/jest/cli.jest.test.js
packages/l1-p11-starter/tests/jest/parse.jest.test.js
packages/l1-p11-starter/tests/jest/transform.jest.test.js
packages/l1-p11-starter/tests/vitest/cli.test.js
packages/l1-p11-starter/tests/vitest/parse.test.js
packages/l1-p11-starter/tests/vitest/transform.test.js
packages/l1-p11-starter/vitest.config.ts
packages/l1-p12-starter/.gitignore
packages/l1-p12-starter/README.md
packages/l1-p12-starter/babel.config.cjs
packages/l1-p12-starter/bin/cli.js
packages/l1-p12-starter/data/sample.csv
packages/l1-p12-starter/data/sample.json
packages/l1-p12-starter/eslint.config.mjs
packages/l1-p12-starter/jest.config.cjs
packages/l1-p12-starter/package.json
packages/l1-p12-starter/src/cli-runner.js
packages/l1-p12-starter/src/lib/filters.js
packages/l1-p12-starter/src/lib/format.js
packages/l1-p12-starter/src/lib/parse.js
packages/l1-p12-starter/src/lib/transform.js
packages/l1-p12-starter/tests/jest/cli.jest.test.js
packages/l1-p12-starter/tests/jest/parse.jest.test.js
packages/l1-p12-starter/tests/jest/transform.jest.test.js
packages/l1-p12-starter/tests/vitest/cli.test.js
packages/l1-p12-starter/tests/vitest/parse.test.js
packages/l1-p12-starter/tests/vitest/transform.test.js
packages/l1-p12-starter/vitest.config.ts
packages/l1-p13-starter/.gitignore
packages/l1-p13-starter/README.md
packages/l1-p13-starter/babel.config.cjs
packages/l1-p13-starter/bin/cli.js
packages/l1-p13-starter/data/sample.csv
packages/l1-p13-starter/data/sample.json
packages/l1-p13-starter/eslint.config.mjs
packages/l1-p13-starter/jest.config.cjs
packages/l1-p13-starter/package.json
packages/l1-p13-starter/src/cli-runner.js
packages/l1-p13-starter/src/lib/filters.js
packages/l1-p13-starter/src/lib/format.js
packages/l1-p13-starter/src/lib/parse.js
packages/l1-p13-starter/src/lib/transform.js
packages/l1-p13-starter/tests/jest/cli.jest.test.js
packages/l1-p13-starter/tests/jest/parse.jest.test.js
packages/l1-p13-starter/tests/jest/transform.jest.test.js
packages/l1-p13-starter/tests/vitest/cli.test.js
packages/l1-p13-starter/tests/vitest/parse.test.js
packages/l1-p13-starter/tests/vitest/transform.test.js
packages/l1-p13-starter/vitest.config.ts
packages/l1-p14-starter/.gitignore
packages/l1-p14-starter/README.md
packages/l1-p14-starter/babel.config.cjs
packages/l1-p14-starter/bin/cli.js
packages/l1-p14-starter/data/sample.csv
packages/l1-p14-starter/data/sample.json
packages/l1-p14-starter/eslint.config.mjs
packages/l1-p14-starter/jest.config.cjs
packages/l1-p14-starter/package.json
packages/l1-p14-starter/src/cli-runner.js
packages/l1-p14-starter/src/lib/filters.js
packages/l1-p14-starter/src/lib/format.js
packages/l1-p14-starter/src/lib/parse.js
packages/l1-p14-starter/src/lib/transform.js
packages/l1-p14-starter/tests/jest/cli.jest.test.js
packages/l1-p14-starter/tests/jest/parse.jest.test.js
packages/l1-p14-starter/tests/jest/transform.jest.test.js
packages/l1-p14-starter/tests/vitest/cli.test.js
packages/l1-p14-starter/tests/vitest/parse.test.js
packages/l1-p14-starter/tests/vitest/transform.test.js
packages/l1-p14-starter/vitest.config.ts
packages/l1-p15-starter/.gitignore
packages/l1-p15-starter/README.md
packages/l1-p15-starter/babel.config.cjs
packages/l1-p15-starter/bin/cli.js
packages/l1-p15-starter/data/sample.csv
packages/l1-p15-starter/data/sample.json
packages/l1-p15-starter/eslint.config.mjs
packages/l1-p15-starter/jest.config.cjs
packages/l1-p15-starter/package.json
packages/l1-p15-starter/src/cli-runner.js
packages/l1-p15-starter/src/lib/filters.js
packages/l1-p15-starter/src/lib/format.js
packages/l1-p15-starter/src/lib/parse.js
packages/l1-p15-starter/src/lib/transform.js
packages/l1-p15-starter/tests/jest/cli.jest.test.js
packages/l1-p15-starter/tests/jest/parse.jest.test.js
packages/l1-p15-starter/tests/jest/transform.jest.test.js
packages/l1-p15-starter/tests/vitest/cli.test.js
packages/l1-p15-starter/tests/vitest/parse.test.js
packages/l1-p15-starter/tests/vitest/transform.test.js
packages/l1-p15-starter/vitest.config.ts
packages/l2-p01-starter/.gitignore
packages/l2-p01-starter/README.md
packages/l2-p01-starter/babel.config.cjs
packages/l2-p01-starter/bin/cli.js
packages/l2-p01-starter/data/sample.csv
packages/l2-p01-starter/data/sample.json
packages/l2-p01-starter/eslint.config.mjs
packages/l2-p01-starter/jest.config.cjs
packages/l2-p01-starter/package.json
packages/l2-p01-starter/src/cli-runner.js
packages/l2-p01-starter/src/lib/filters.js
packages/l2-p01-starter/src/lib/format.js
packages/l2-p01-starter/src/lib/parse.js
packages/l2-p01-starter/src/lib/transform.js
packages/l2-p01-starter/tests/jest/cli.jest.test.js
packages/l2-p01-starter/tests/jest/parse.jest.test.js
packages/l2-p01-starter/tests/jest/transform.jest.test.js
packages/l2-p01-starter/tests/vitest/cli.test.js
packages/l2-p01-starter/tests/vitest/parse.test.js
packages/l2-p01-starter/tests/vitest/transform.test.js
packages/l2-p01-starter/vitest.config.ts
packages/l2-p02-starter/.gitignore
packages/l2-p02-starter/README.md
packages/l2-p02-starter/babel.config.cjs
packages/l2-p02-starter/bin/cli.js
packages/l2-p02-starter/data/sample.csv
packages/l2-p02-starter/data/sample.json
packages/l2-p02-starter/eslint.config.mjs
packages/l2-p02-starter/jest.config.cjs
packages/l2-p02-starter/package.json
packages/l2-p02-starter/src/cli-runner.js
packages/l2-p02-starter/src/lib/filters.js
packages/l2-p02-starter/src/lib/format.js
packages/l2-p02-starter/src/lib/parse.js
packages/l2-p02-starter/src/lib/transform.js
packages/l2-p02-starter/tests/jest/cli.jest.test.js
packages/l2-p02-starter/tests/jest/parse.jest.test.js
packages/l2-p02-starter/tests/jest/transform.jest.test.js
packages/l2-p02-starter/tests/vitest/cli.test.js
packages/l2-p02-starter/tests/vitest/parse.test.js
packages/l2-p02-starter/tests/vitest/transform.test.js
packages/l2-p02-starter/vitest.config.ts
packages/l2-p03-starter/.gitignore
packages/l2-p03-starter/README.md
packages/l2-p03-starter/babel.config.cjs
packages/l2-p03-starter/bin/cli.js
packages/l2-p03-starter/data/sample.csv
packages/l2-p03-starter/data/sample.json
packages/l2-p03-starter/eslint.config.mjs
packages/l2-p03-starter/jest.config.cjs
packages/l2-p03-starter/package.json
packages/l2-p03-starter/src/cli-runner.js
packages/l2-p03-starter/src/lib/filters.js
packages/l2-p03-starter/src/lib/format.js
packages/l2-p03-starter/src/lib/parse.js
packages/l2-p03-starter/src/lib/transform.js
packages/l2-p03-starter/tests/jest/cli.jest.test.js
packages/l2-p03-starter/tests/jest/parse.jest.test.js
packages/l2-p03-starter/tests/jest/transform.jest.test.js
packages/l2-p03-starter/tests/vitest/cli.test.js
packages/l2-p03-starter/tests/vitest/parse.test.js
packages/l2-p03-starter/tests/vitest/transform.test.js
packages/l2-p03-starter/vitest.config.ts
packages/l2-p04-starter/.gitignore
packages/l2-p04-starter/README.md
packages/l2-p04-starter/babel.config.cjs
packages/l2-p04-starter/bin/cli.js
packages/l2-p04-starter/data/sample.csv
packages/l2-p04-starter/data/sample.json
packages/l2-p04-starter/eslint.config.mjs
packages/l2-p04-starter/jest.config.cjs
packages/l2-p04-starter/package.json
packages/l2-p04-starter/src/cli-runner.js
packages/l2-p04-starter/src/lib/filters.js
packages/l2-p04-starter/src/lib/format.js
packages/l2-p04-starter/src/lib/parse.js
packages/l2-p04-starter/src/lib/transform.js
packages/l2-p04-starter/tests/jest/cli.jest.test.js
packages/l2-p04-starter/tests/jest/parse.jest.test.js
packages/l2-p04-starter/tests/jest/transform.jest.test.js
packages/l2-p04-starter/tests/vitest/cli.test.js
packages/l2-p04-starter/tests/vitest/parse.test.js
packages/l2-p04-starter/tests/vitest/transform.test.js
packages/l2-p04-starter/vitest.config.ts
packages/l2-p05-starter/.gitignore
packages/l2-p05-starter/README.md
packages/l2-p05-starter/babel.config.cjs
packages/l2-p05-starter/bin/cli.js
packages/l2-p05-starter/data/sample.csv
packages/l2-p05-starter/data/sample.json
packages/l2-p05-starter/eslint.config.mjs
packages/l2-p05-starter/jest.config.cjs
packages/l2-p05-starter/package.json
packages/l2-p05-starter/src/cli-runner.js
packages/l2-p05-starter/src/lib/filters.js
packages/l2-p05-starter/src/lib/format.js
packages/l2-p05-starter/src/lib/parse.js
packages/l2-p05-starter/src/lib/transform.js
packages/l2-p05-starter/tests/jest/cli.jest.test.js
packages/l2-p05-starter/tests/jest/parse.jest.test.js
packages/l2-p05-starter/tests/jest/transform.jest.test.js
packages/l2-p05-starter/tests/vitest/cli.test.js
packages/l2-p05-starter/tests/vitest/parse.test.js
packages/l2-p05-starter/tests/vitest/transform.test.js
packages/l2-p05-starter/vitest.config.ts
packages/l2-p06-starter/.gitignore
packages/l2-p06-starter/README.md
packages/l2-p06-starter/babel.config.cjs
packages/l2-p06-starter/bin/cli.js
packages/l2-p06-starter/data/sample.csv
packages/l2-p06-starter/data/sample.json
packages/l2-p06-starter/eslint.config.mjs
packages/l2-p06-starter/jest.config.cjs
packages/l2-p06-starter/package.json
packages/l2-p06-starter/src/cli-runner.js
packages/l2-p06-starter/src/lib/filters.js
packages/l2-p06-starter/src/lib/format.js
packages/l2-p06-starter/src/lib/parse.js
packages/l2-p06-starter/src/lib/transform.js
packages/l2-p06-starter/tests/jest/cli.jest.test.js
packages/l2-p06-starter/tests/jest/parse.jest.test.js
packages/l2-p06-starter/tests/jest/transform.jest.test.js
packages/l2-p06-starter/tests/vitest/cli.test.js
packages/l2-p06-starter/tests/vitest/parse.test.js
packages/l2-p06-starter/tests/vitest/transform.test.js
packages/l2-p06-starter/vitest.config.ts
packages/l2-p07-starter/.gitignore
packages/l2-p07-starter/README.md
packages/l2-p07-starter/babel.config.cjs
packages/l2-p07-starter/bin/cli.js
packages/l2-p07-starter/data/sample.csv
packages/l2-p07-starter/data/sample.json
packages/l2-p07-starter/eslint.config.mjs
packages/l2-p07-starter/jest.config.cjs
packages/l2-p07-starter/package.json
packages/l2-p07-starter/src/cli-runner.js
packages/l2-p07-starter/src/lib/filters.js
packages/l2-p07-starter/src/lib/format.js
packages/l2-p07-starter/src/lib/parse.js
packages/l2-p07-starter/src/lib/transform.js
packages/l2-p07-starter/tests/jest/cli.jest.test.js
packages/l2-p07-starter/tests/jest/parse.jest.test.js
packages/l2-p07-starter/tests/jest/transform.jest.test.js
packages/l2-p07-starter/tests/vitest/cli.test.js
packages/l2-p07-starter/tests/vitest/parse.test.js
packages/l2-p07-starter/tests/vitest/transform.test.js
packages/l2-p07-starter/vitest.config.ts
packages/l2-p08-starter/.gitignore
packages/l2-p08-starter/README.md
packages/l2-p08-starter/babel.config.cjs
packages/l2-p08-starter/bin/cli.js
packages/l2-p08-starter/data/sample.csv
packages/l2-p08-starter/data/sample.json
packages/l2-p08-starter/eslint.config.mjs
packages/l2-p08-starter/jest.config.cjs
packages/l2-p08-starter/package.json
packages/l2-p08-starter/src/cli-runner.js
packages/l2-p08-starter/src/lib/filters.js
packages/l2-p08-starter/src/lib/format.js
packages/l2-p08-starter/src/lib/parse.js
packages/l2-p08-starter/src/lib/transform.js
packages/l2-p08-starter/tests/jest/cli.jest.test.js
packages/l2-p08-starter/tests/jest/parse.jest.test.js
packages/l2-p08-starter/tests/jest/transform.jest.test.js
packages/l2-p08-starter/tests/vitest/cli.test.js
packages/l2-p08-starter/tests/vitest/parse.test.js
packages/l2-p08-starter/tests/vitest/transform.test.js
packages/l2-p08-starter/vitest.config.ts
packages/l2-p09-starter/.gitignore
packages/l2-p09-starter/README.md
packages/l2-p09-starter/babel.config.cjs
packages/l2-p09-starter/bin/cli.js
packages/l2-p09-starter/data/sample.csv
packages/l2-p09-starter/data/sample.json
packages/l2-p09-starter/eslint.config.mjs
packages/l2-p09-starter/jest.config.cjs
packages/l2-p09-starter/package.json
packages/l2-p09-starter/src/cli-runner.js
packages/l2-p09-starter/src/lib/filters.js
packages/l2-p09-starter/src/lib/format.js
packages/l2-p09-starter/src/lib/parse.js
packages/l2-p09-starter/src/lib/transform.js
packages/l2-p09-starter/tests/jest/cli.jest.test.js
packages/l2-p09-starter/tests/jest/parse.jest.test.js
packages/l2-p09-starter/tests/jest/transform.jest.test.js
packages/l2-p09-starter/tests/vitest/cli.test.js
packages/l2-p09-starter/tests/vitest/parse.test.js
packages/l2-p09-starter/tests/vitest/transform.test.js
packages/l2-p09-starter/vitest.config.ts
packages/l2-p10-starter/.gitignore
packages/l2-p10-starter/README.md
packages/l2-p10-starter/babel.config.cjs
packages/l2-p10-starter/bin/cli.js
packages/l2-p10-starter/data/sample.csv
packages/l2-p10-starter/data/sample.json
packages/l2-p10-starter/eslint.config.mjs
packages/l2-p10-starter/jest.config.cjs
packages/l2-p10-starter/package.json
packages/l2-p10-starter/src/cli-runner.js
packages/l2-p10-starter/src/lib/filters.js
packages/l2-p10-starter/src/lib/format.js
packages/l2-p10-starter/src/lib/parse.js
packages/l2-p10-starter/src/lib/transform.js
packages/l2-p10-starter/tests/jest/cli.jest.test.js
packages/l2-p10-starter/tests/jest/parse.jest.test.js
packages/l2-p10-starter/tests/jest/transform.jest.test.js
packages/l2-p10-starter/tests/vitest/cli.test.js
packages/l2-p10-starter/tests/vitest/parse.test.js
packages/l2-p10-starter/tests/vitest/transform.test.js
packages/l2-p10-starter/vitest.config.ts
packages/l2-p11-starter/.gitignore
packages/l2-p11-starter/README.md
packages/l2-p11-starter/babel.config.cjs
packages/l2-p11-starter/bin/cli.js
packages/l2-p11-starter/data/sample.csv
packages/l2-p11-starter/data/sample.json
packages/l2-p11-starter/eslint.config.mjs
packages/l2-p11-starter/jest.config.cjs
packages/l2-p11-starter/package.json
packages/l2-p11-starter/src/cli-runner.js
packages/l2-p11-starter/src/lib/filters.js
packages/l2-p11-starter/src/lib/format.js
packages/l2-p11-starter/src/lib/parse.js
packages/l2-p11-starter/src/lib/transform.js
packages/l2-p11-starter/tests/jest/cli.jest.test.js
packages/l2-p11-starter/tests/jest/parse.jest.test.js
packages/l2-p11-starter/tests/jest/transform.jest.test.js
packages/l2-p11-starter/tests/vitest/cli.test.js
packages/l2-p11-starter/tests/vitest/parse.test.js
packages/l2-p11-starter/tests/vitest/transform.test.js
packages/l2-p11-starter/vitest.config.ts
packages/l2-p12-starter/.gitignore
packages/l2-p12-starter/README.md
packages/l2-p12-starter/babel.config.cjs
packages/l2-p12-starter/bin/cli.js
packages/l2-p12-starter/data/sample.csv
packages/l2-p12-starter/data/sample.json
packages/l2-p12-starter/eslint.config.mjs
packages/l2-p12-starter/jest.config.cjs
packages/l2-p12-starter/package.json
packages/l2-p12-starter/src/cli-runner.js
packages/l2-p12-starter/src/lib/filters.js
packages/l2-p12-starter/src/lib/format.js
packages/l2-p12-starter/src/lib/parse.js
packages/l2-p12-starter/src/lib/transform.js
packages/l2-p12-starter/tests/jest/cli.jest.test.js
packages/l2-p12-starter/tests/jest/parse.jest.test.js
packages/l2-p12-starter/tests/jest/transform.jest.test.js
packages/l2-p12-starter/tests/vitest/cli.test.js
packages/l2-p12-starter/tests/vitest/parse.test.js
packages/l2-p12-starter/tests/vitest/transform.test.js
packages/l2-p12-starter/vitest.config.ts
packages/l2-p13-starter/.gitignore
packages/l2-p13-starter/README.md
packages/l2-p13-starter/babel.config.cjs
packages/l2-p13-starter/bin/cli.js
packages/l2-p13-starter/data/sample.csv
packages/l2-p13-starter/data/sample.json
packages/l2-p13-starter/eslint.config.mjs
packages/l2-p13-starter/jest.config.cjs
packages/l2-p13-starter/package.json
packages/l2-p13-starter/src/cli-runner.js
packages/l2-p13-starter/src/lib/filters.js
packages/l2-p13-starter/src/lib/format.js
packages/l2-p13-starter/src/lib/parse.js
packages/l2-p13-starter/src/lib/transform.js
packages/l2-p13-starter/tests/jest/cli.jest.test.js
packages/l2-p13-starter/tests/jest/parse.jest.test.js
packages/l2-p13-starter/tests/jest/transform.jest.test.js
packages/l2-p13-starter/tests/vitest/cli.test.js
packages/l2-p13-starter/tests/vitest/parse.test.js
packages/l2-p13-starter/tests/vitest/transform.test.js
packages/l2-p13-starter/vitest.config.ts
packages/l2-p14-starter/.gitignore
packages/l2-p14-starter/README.md
packages/l2-p14-starter/babel.config.cjs
packages/l2-p14-starter/bin/cli.js
packages/l2-p14-starter/data/sample.csv
packages/l2-p14-starter/data/sample.json
packages/l2-p14-starter/eslint.config.mjs
packages/l2-p14-starter/jest.config.cjs
packages/l2-p14-starter/package.json
packages/l2-p14-starter/src/cli-runner.js
packages/l2-p14-starter/src/lib/filters.js
packages/l2-p14-starter/src/lib/format.js
packages/l2-p14-starter/src/lib/parse.js
packages/l2-p14-starter/src/lib/transform.js
packages/l2-p14-starter/tests/jest/cli.jest.test.js
packages/l2-p14-starter/tests/jest/parse.jest.test.js
packages/l2-p14-starter/tests/jest/transform.jest.test.js
packages/l2-p14-starter/tests/vitest/cli.test.js
packages/l2-p14-starter/tests/vitest/parse.test.js
packages/l2-p14-starter/tests/vitest/transform.test.js
packages/l2-p14-starter/vitest.config.ts
packages/l2-p15-starter/.gitignore
packages/l2-p15-starter/README.md
packages/l2-p15-starter/babel.config.cjs
packages/l2-p15-starter/bin/cli.js
packages/l2-p15-starter/data/sample.csv
packages/l2-p15-starter/data/sample.json
packages/l2-p15-starter/eslint.config.mjs
packages/l2-p15-starter/jest.config.cjs
packages/l2-p15-starter/package.json
packages/l2-p15-starter/src/cli-runner.js
packages/l2-p15-starter/src/lib/filters.js
packages/l2-p15-starter/src/lib/format.js
packages/l2-p15-starter/src/lib/parse.js
packages/l2-p15-starter/src/lib/transform.js
packages/l2-p15-starter/tests/jest/cli.jest.test.js
packages/l2-p15-starter/tests/jest/parse.jest.test.js
packages/l2-p15-starter/tests/jest/transform.jest.test.js
packages/l2-p15-starter/tests/vitest/cli.test.js
packages/l2-p15-starter/tests/vitest/parse.test.js
packages/l2-p15-starter/tests/vitest/transform.test.js
packages/l2-p15-starter/vitest.config.ts
packages/l3-p01-starter/.gitignore
packages/l3-p01-starter/README.md
packages/l3-p01-starter/babel.config.cjs
packages/l3-p01-starter/bin/cli.js
packages/l3-p01-starter/data/sample.csv
packages/l3-p01-starter/data/sample.json
packages/l3-p01-starter/e2e/example.spec.ts
packages/l3-p01-starter/eslint.config.mjs
packages/l3-p01-starter/jest.config.cjs
packages/l3-p01-starter/package.json
packages/l3-p01-starter/playwright.config.ts
packages/l3-p01-starter/public/index.html
packages/l3-p01-starter/public/manifest.webmanifest
packages/l3-p01-starter/scripts/build-sw.mjs
packages/l3-p01-starter/server.mjs
packages/l3-p01-starter/src/cli-runner.js
packages/l3-p01-starter/src/lib/filters.js
packages/l3-p01-starter/src/lib/format.js
packages/l3-p01-starter/src/lib/parse.js
packages/l3-p01-starter/src/lib/transform.js
packages/l3-p01-starter/tests/jest/cli.jest.test.js
packages/l3-p01-starter/tests/jest/parse.jest.test.js
packages/l3-p01-starter/tests/jest/transform.jest.test.js
packages/l3-p01-starter/tests/vitest/cli.test.js
packages/l3-p01-starter/tests/vitest/parse.test.js
packages/l3-p01-starter/tests/vitest/transform.test.js
packages/l3-p01-starter/vitest.config.ts
packages/l3-p02-starter/.gitignore
packages/l3-p02-starter/README.md
packages/l3-p02-starter/babel.config.cjs
packages/l3-p02-starter/bin/cli.js
packages/l3-p02-starter/data/sample.csv
packages/l3-p02-starter/data/sample.json
packages/l3-p02-starter/e2e/example.spec.ts
packages/l3-p02-starter/eslint.config.mjs
packages/l3-p02-starter/jest.config.cjs
packages/l3-p02-starter/package.json
packages/l3-p02-starter/playwright.config.ts
packages/l3-p02-starter/public/index.html
packages/l3-p02-starter/public/manifest.webmanifest
packages/l3-p02-starter/scripts/build-sw.mjs
packages/l3-p02-starter/server.mjs
packages/l3-p02-starter/src/cli-runner.js
packages/l3-p02-starter/src/lib/filters.js
packages/l3-p02-starter/src/lib/format.js
packages/l3-p02-starter/src/lib/parse.js
packages/l3-p02-starter/src/lib/transform.js
packages/l3-p02-starter/tests/jest/cli.jest.test.js
packages/l3-p02-starter/tests/jest/parse.jest.test.js
packages/l3-p02-starter/tests/jest/transform.jest.test.js
packages/l3-p02-starter/tests/vitest/cli.test.js
packages/l3-p02-starter/tests/vitest/parse.test.js
packages/l3-p02-starter/tests/vitest/transform.test.js
packages/l3-p02-starter/vitest.config.ts
packages/l3-p03-starter/.gitignore
packages/l3-p03-starter/README.md
packages/l3-p03-starter/babel.config.cjs
packages/l3-p03-starter/bin/cli.js
packages/l3-p03-starter/data/sample.csv
packages/l3-p03-starter/data/sample.json
packages/l3-p03-starter/e2e/example.spec.ts
packages/l3-p03-starter/eslint.config.mjs
packages/l3-p03-starter/jest.config.cjs
packages/l3-p03-starter/package.json
packages/l3-p03-starter/playwright.config.ts
packages/l3-p03-starter/public/index.html
packages/l3-p03-starter/public/manifest.webmanifest
packages/l3-p03-starter/scripts/build-sw.mjs
packages/l3-p03-starter/server.mjs
packages/l3-p03-starter/src/cli-runner.js
packages/l3-p03-starter/src/lib/filters.js
packages/l3-p03-starter/src/lib/format.js
packages/l3-p03-starter/src/lib/parse.js
packages/l3-p03-starter/src/lib/transform.js
packages/l3-p03-starter/tests/jest/cli.jest.test.js
packages/l3-p03-starter/tests/jest/parse.jest.test.js
packages/l3-p03-starter/tests/jest/transform.jest.test.js
packages/l3-p03-starter/tests/vitest/cli.test.js
packages/l3-p03-starter/tests/vitest/parse.test.js
packages/l3-p03-starter/tests/vitest/transform.test.js
packages/l3-p03-starter/vitest.config.ts
packages/l3-p04-starter/.gitignore
packages/l3-p04-starter/README.md
packages/l3-p04-starter/babel.config.cjs
packages/l3-p04-starter/bin/cli.js
packages/l3-p04-starter/data/sample.csv
packages/l3-p04-starter/data/sample.json
packages/l3-p04-starter/e2e/example.spec.ts
packages/l3-p04-starter/eslint.config.mjs
packages/l3-p04-starter/jest.config.cjs
packages/l3-p04-starter/package.json
packages/l3-p04-starter/playwright.config.ts
packages/l3-p04-starter/public/index.html
packages/l3-p04-starter/public/manifest.webmanifest
packages/l3-p04-starter/scripts/build-sw.mjs
packages/l3-p04-starter/server.mjs
packages/l3-p04-starter/src/cli-runner.js
packages/l3-p04-starter/src/lib/filters.js
packages/l3-p04-starter/src/lib/format.js
packages/l3-p04-starter/src/lib/parse.js
packages/l3-p04-starter/src/lib/transform.js
packages/l3-p04-starter/tests/jest/cli.jest.test.js
packages/l3-p04-starter/tests/jest/parse.jest.test.js
packages/l3-p04-starter/tests/jest/transform.jest.test.js
packages/l3-p04-starter/tests/vitest/cli.test.js
packages/l3-p04-starter/tests/vitest/parse.test.js
packages/l3-p04-starter/tests/vitest/transform.test.js
packages/l3-p04-starter/vitest.config.ts
packages/l3-p05-starter/.gitignore
packages/l3-p05-starter/README.md
packages/l3-p05-starter/babel.config.cjs
packages/l3-p05-starter/bin/cli.js
packages/l3-p05-starter/data/sample.csv
packages/l3-p05-starter/data/sample.json
packages/l3-p05-starter/e2e/example.spec.ts
packages/l3-p05-starter/eslint.config.mjs
packages/l3-p05-starter/jest.config.cjs
packages/l3-p05-starter/package.json
packages/l3-p05-starter/playwright.config.ts
packages/l3-p05-starter/public/index.html
packages/l3-p05-starter/public/manifest.webmanifest
packages/l3-p05-starter/scripts/build-sw.mjs
packages/l3-p05-starter/server.mjs
packages/l3-p05-starter/src/cli-runner.js
packages/l3-p05-starter/src/lib/filters.js
packages/l3-p05-starter/src/lib/format.js
packages/l3-p05-starter/src/lib/parse.js
packages/l3-p05-starter/src/lib/transform.js
packages/l3-p05-starter/tests/jest/cli.jest.test.js
packages/l3-p05-starter/tests/jest/parse.jest.test.js
packages/l3-p05-starter/tests/jest/transform.jest.test.js
packages/l3-p05-starter/tests/vitest/cli.test.js
packages/l3-p05-starter/tests/vitest/parse.test.js
packages/l3-p05-starter/tests/vitest/transform.test.js
packages/l3-p05-starter/vitest.config.ts
packages/l3-p06-starter/.gitignore
packages/l3-p06-starter/README.md
packages/l3-p06-starter/babel.config.cjs
packages/l3-p06-starter/bin/cli.js
packages/l3-p06-starter/data/sample.csv
packages/l3-p06-starter/data/sample.json
packages/l3-p06-starter/e2e/example.spec.ts
packages/l3-p06-starter/eslint.config.mjs
packages/l3-p06-starter/jest.config.cjs
packages/l3-p06-starter/package.json
packages/l3-p06-starter/playwright.config.ts
packages/l3-p06-starter/public/index.html
packages/l3-p06-starter/public/manifest.webmanifest
packages/l3-p06-starter/scripts/build-sw.mjs
packages/l3-p06-starter/server.mjs
packages/l3-p06-starter/src/cli-runner.js
packages/l3-p06-starter/src/lib/filters.js
packages/l3-p06-starter/src/lib/format.js
packages/l3-p06-starter/src/lib/parse.js
packages/l3-p06-starter/src/lib/transform.js
packages/l3-p06-starter/tests/jest/cli.jest.test.js
packages/l3-p06-starter/tests/jest/parse.jest.test.js
packages/l3-p06-starter/tests/jest/transform.jest.test.js
packages/l3-p06-starter/tests/vitest/cli.test.js
packages/l3-p06-starter/tests/vitest/parse.test.js
packages/l3-p06-starter/tests/vitest/transform.test.js
packages/l3-p06-starter/vitest.config.ts
packages/l3-p07-starter/.gitignore
packages/l3-p07-starter/README.md
packages/l3-p07-starter/babel.config.cjs
packages/l3-p07-starter/bin/cli.js
packages/l3-p07-starter/data/sample.csv
packages/l3-p07-starter/data/sample.json
packages/l3-p07-starter/e2e/example.spec.ts
packages/l3-p07-starter/eslint.config.mjs
packages/l3-p07-starter/jest.config.cjs
packages/l3-p07-starter/package.json
packages/l3-p07-starter/playwright.config.ts
packages/l3-p07-starter/public/index.html
packages/l3-p07-starter/public/manifest.webmanifest
packages/l3-p07-starter/scripts/build-sw.mjs
packages/l3-p07-starter/server.mjs
packages/l3-p07-starter/src/cli-runner.js
packages/l3-p07-starter/src/lib/filters.js
packages/l3-p07-starter/src/lib/format.js
packages/l3-p07-starter/src/lib/parse.js
packages/l3-p07-starter/src/lib/transform.js
packages/l3-p07-starter/tests/jest/cli.jest.test.js
packages/l3-p07-starter/tests/jest/parse.jest.test.js
packages/l3-p07-starter/tests/jest/transform.jest.test.js
packages/l3-p07-starter/tests/vitest/cli.test.js
packages/l3-p07-starter/tests/vitest/parse.test.js
packages/l3-p07-starter/tests/vitest/transform.test.js
packages/l3-p07-starter/vitest.config.ts
packages/l3-p08-starter/.gitignore
packages/l3-p08-starter/README.md
packages/l3-p08-starter/babel.config.cjs
packages/l3-p08-starter/bin/cli.js
packages/l3-p08-starter/data/sample.csv
packages/l3-p08-starter/data/sample.json
packages/l3-p08-starter/e2e/example.spec.ts
packages/l3-p08-starter/eslint.config.mjs
packages/l3-p08-starter/jest.config.cjs
packages/l3-p08-starter/package.json
packages/l3-p08-starter/playwright.config.ts
packages/l3-p08-starter/public/index.html
packages/l3-p08-starter/public/manifest.webmanifest
packages/l3-p08-starter/scripts/build-sw.mjs
packages/l3-p08-starter/server.mjs
packages/l3-p08-starter/src/cli-runner.js
packages/l3-p08-starter/src/lib/filters.js
packages/l3-p08-starter/src/lib/format.js
packages/l3-p08-starter/src/lib/parse.js
packages/l3-p08-starter/src/lib/transform.js
packages/l3-p08-starter/tests/jest/cli.jest.test.js
packages/l3-p08-starter/tests/jest/parse.jest.test.js
packages/l3-p08-starter/tests/jest/transform.jest.test.js
packages/l3-p08-starter/tests/vitest/cli.test.js
packages/l3-p08-starter/tests/vitest/parse.test.js
packages/l3-p08-starter/tests/vitest/transform.test.js
packages/l3-p08-starter/vitest.config.ts
packages/l3-p09-starter/.gitignore
packages/l3-p09-starter/README.md
packages/l3-p09-starter/babel.config.cjs
packages/l3-p09-starter/bin/cli.js
packages/l3-p09-starter/data/sample.csv
packages/l3-p09-starter/data/sample.json
packages/l3-p09-starter/e2e/example.spec.ts
packages/l3-p09-starter/eslint.config.mjs
packages/l3-p09-starter/jest.config.cjs
packages/l3-p09-starter/package.json
packages/l3-p09-starter/playwright.config.ts
packages/l3-p09-starter/public/index.html
packages/l3-p09-starter/public/manifest.webmanifest
packages/l3-p09-starter/scripts/build-sw.mjs
packages/l3-p09-starter/server.mjs
packages/l3-p09-starter/src/cli-runner.js
packages/l3-p09-starter/src/lib/filters.js
packages/l3-p09-starter/src/lib/format.js
packages/l3-p09-starter/src/lib/parse.js
packages/l3-p09-starter/src/lib/transform.js
packages/l3-p09-starter/tests/jest/cli.jest.test.js
packages/l3-p09-starter/tests/jest/parse.jest.test.js
packages/l3-p09-starter/tests/jest/transform.jest.test.js
packages/l3-p09-starter/tests/vitest/cli.test.js
packages/l3-p09-starter/tests/vitest/parse.test.js
packages/l3-p09-starter/tests/vitest/transform.test.js
packages/l3-p09-starter/vitest.config.ts
packages/l3-p10-starter/.gitignore
packages/l3-p10-starter/README.md
packages/l3-p10-starter/babel.config.cjs
packages/l3-p10-starter/bin/cli.js
packages/l3-p10-starter/data/sample.csv
packages/l3-p10-starter/data/sample.json
packages/l3-p10-starter/e2e/example.spec.ts
packages/l3-p10-starter/eslint.config.mjs
packages/l3-p10-starter/jest.config.cjs
packages/l3-p10-starter/package.json
packages/l3-p10-starter/playwright.config.ts
packages/l3-p10-starter/public/index.html
packages/l3-p10-starter/public/manifest.webmanifest
packages/l3-p10-starter/scripts/build-sw.mjs
packages/l3-p10-starter/server.mjs
packages/l3-p10-starter/src/cli-runner.js
packages/l3-p10-starter/src/lib/filters.js
packages/l3-p10-starter/src/lib/format.js
packages/l3-p10-starter/src/lib/parse.js
packages/l3-p10-starter/src/lib/transform.js
packages/l3-p10-starter/tests/jest/cli.jest.test.js
packages/l3-p10-starter/tests/jest/parse.jest.test.js
packages/l3-p10-starter/tests/jest/transform.jest.test.js
packages/l3-p10-starter/tests/vitest/cli.test.js
packages/l3-p10-starter/tests/vitest/parse.test.js
packages/l3-p10-starter/tests/vitest/transform.test.js
packages/l3-p10-starter/vitest.config.ts
packages/l3-p11-starter/.gitignore
packages/l3-p11-starter/README.md
packages/l3-p11-starter/babel.config.cjs
packages/l3-p11-starter/bin/cli.js
packages/l3-p11-starter/data/sample.csv
packages/l3-p11-starter/data/sample.json
packages/l3-p11-starter/e2e/example.spec.ts
packages/l3-p11-starter/eslint.config.mjs
packages/l3-p11-starter/jest.config.cjs
packages/l3-p11-starter/package.json
packages/l3-p11-starter/playwright.config.ts
packages/l3-p11-starter/public/index.html
packages/l3-p11-starter/public/manifest.webmanifest
packages/l3-p11-starter/scripts/build-sw.mjs
packages/l3-p11-starter/server.mjs
packages/l3-p11-starter/src/cli-runner.js
packages/l3-p11-starter/src/lib/filters.js
packages/l3-p11-starter/src/lib/format.js
packages/l3-p11-starter/src/lib/parse.js
packages/l3-p11-starter/src/lib/transform.js
packages/l3-p11-starter/tests/jest/cli.jest.test.js
packages/l3-p11-starter/tests/jest/parse.jest.test.js
packages/l3-p11-starter/tests/jest/transform.jest.test.js
packages/l3-p11-starter/tests/vitest/cli.test.js
packages/l3-p11-starter/tests/vitest/parse.test.js
packages/l3-p11-starter/tests/vitest/transform.test.js
packages/l3-p11-starter/vitest.config.ts
packages/l3-p12-starter/.gitignore
packages/l3-p12-starter/README.md
packages/l3-p12-starter/babel.config.cjs
packages/l3-p12-starter/bin/cli.js
packages/l3-p12-starter/data/sample.csv
packages/l3-p12-starter/data/sample.json
packages/l3-p12-starter/e2e/example.spec.ts
packages/l3-p12-starter/eslint.config.mjs
packages/l3-p12-starter/jest.config.cjs
packages/l3-p12-starter/package.json
packages/l3-p12-starter/playwright.config.ts
packages/l3-p12-starter/public/index.html
packages/l3-p12-starter/public/manifest.webmanifest
packages/l3-p12-starter/scripts/build-sw.mjs
packages/l3-p12-starter/server.mjs
packages/l3-p12-starter/src/cli-runner.js
packages/l3-p12-starter/src/lib/filters.js
packages/l3-p12-starter/src/lib/format.js
packages/l3-p12-starter/src/lib/parse.js
packages/l3-p12-starter/src/lib/transform.js
packages/l3-p12-starter/tests/jest/cli.jest.test.js
packages/l3-p12-starter/tests/jest/parse.jest.test.js
packages/l3-p12-starter/tests/jest/transform.jest.test.js
packages/l3-p12-starter/tests/vitest/cli.test.js
packages/l3-p12-starter/tests/vitest/parse.test.js
packages/l3-p12-starter/tests/vitest/transform.test.js
packages/l3-p12-starter/vitest.config.ts
packages/l3-p13-starter/.gitignore
packages/l3-p13-starter/README.md
packages/l3-p13-starter/babel.config.cjs
packages/l3-p13-starter/bin/cli.js
packages/l3-p13-starter/data/sample.csv
packages/l3-p13-starter/data/sample.json
packages/l3-p13-starter/e2e/example.spec.ts
packages/l3-p13-starter/eslint.config.mjs
packages/l3-p13-starter/jest.config.cjs
packages/l3-p13-starter/package.json
packages/l3-p13-starter/playwright.config.ts
packages/l3-p13-starter/public/index.html
packages/l3-p13-starter/public/manifest.webmanifest
packages/l3-p13-starter/scripts/build-sw.mjs
packages/l3-p13-starter/server.mjs
packages/l3-p13-starter/src/cli-runner.js
packages/l3-p13-starter/src/lib/filters.js
packages/l3-p13-starter/src/lib/format.js
packages/l3-p13-starter/src/lib/parse.js
packages/l3-p13-starter/src/lib/transform.js
packages/l3-p13-starter/tests/jest/cli.jest.test.js
packages/l3-p13-starter/tests/jest/parse.jest.test.js
packages/l3-p13-starter/tests/jest/transform.jest.test.js
packages/l3-p13-starter/tests/vitest/cli.test.js
packages/l3-p13-starter/tests/vitest/parse.test.js
packages/l3-p13-starter/tests/vitest/transform.test.js
packages/l3-p13-starter/vitest.config.ts
packages/l3-p14-starter/.gitignore
packages/l3-p14-starter/README.md
packages/l3-p14-starter/babel.config.cjs
packages/l3-p14-starter/bin/cli.js
packages/l3-p14-starter/data/sample.csv
packages/l3-p14-starter/data/sample.json
packages/l3-p14-starter/e2e/example.spec.ts
packages/l3-p14-starter/eslint.config.mjs
packages/l3-p14-starter/jest.config.cjs
packages/l3-p14-starter/package.json
packages/l3-p14-starter/playwright.config.ts
packages/l3-p14-starter/public/index.html
packages/l3-p14-starter/public/manifest.webmanifest
packages/l3-p14-starter/scripts/build-sw.mjs
packages/l3-p14-starter/server.mjs
packages/l3-p14-starter/src/cli-runner.js
packages/l3-p14-starter/src/lib/filters.js
packages/l3-p14-starter/src/lib/format.js
packages/l3-p14-starter/src/lib/parse.js
packages/l3-p14-starter/src/lib/transform.js
packages/l3-p14-starter/tests/jest/cli.jest.test.js
packages/l3-p14-starter/tests/jest/parse.jest.test.js
packages/l3-p14-starter/tests/jest/transform.jest.test.js
packages/l3-p14-starter/tests/vitest/cli.test.js
packages/l3-p14-starter/tests/vitest/parse.test.js
packages/l3-p14-starter/tests/vitest/transform.test.js
packages/l3-p14-starter/vitest.config.ts
packages/l3-p15-starter/.gitignore
packages/l3-p15-starter/README.md
packages/l3-p15-starter/babel.config.cjs
packages/l3-p15-starter/bin/cli.js
packages/l3-p15-starter/data/sample.csv
packages/l3-p15-starter/data/sample.json
packages/l3-p15-starter/e2e/example.spec.ts
packages/l3-p15-starter/eslint.config.mjs
packages/l3-p15-starter/jest.config.cjs
packages/l3-p15-starter/package.json
packages/l3-p15-starter/playwright.config.ts
packages/l3-p15-starter/public/index.html
packages/l3-p15-starter/public/manifest.webmanifest
packages/l3-p15-starter/scripts/build-sw.mjs
packages/l3-p15-starter/server.mjs
packages/l3-p15-starter/src/cli-runner.js
packages/l3-p15-starter/src/lib/filters.js
packages/l3-p15-starter/src/lib/format.js
packages/l3-p15-starter/src/lib/parse.js
packages/l3-p15-starter/src/lib/transform.js
packages/l3-p15-starter/tests/jest/cli.jest.test.js
packages/l3-p15-starter/tests/jest/parse.jest.test.js
packages/l3-p15-starter/tests/jest/transform.jest.test.js
packages/l3-p15-starter/tests/vitest/cli.test.js
packages/l3-p15-starter/tests/vitest/parse.test.js
packages/l3-p15-starter/tests/vitest/transform.test.js
packages/l3-p15-starter/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** starter: 1035.

**Categorii de fișiere:** config: 302, docs: 45, other: 180, code: 225, tests: 270, public: 15, ci: 3.

**package.json — sinteză: scripturi, workspaces, bin, dependențe (eșantion)**

- `package.json`: name=`s1p3-monorepo` type=`module` workspaces=True bin=False
- `packages/l1-p01-starter/package.json`: name=`l1-p01-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p02-starter/package.json`: name=`l1-p02-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p03-starter/package.json`: name=`l1-p03-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p04-starter/package.json`: name=`l1-p04-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p05-starter/package.json`: name=`l1-p05-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p06-starter/package.json`: name=`l1-p06-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p07-starter/package.json`: name=`l1-p07-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p08-starter/package.json`: name=`l1-p08-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p09-starter/package.json`: name=`l1-p09-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p10-starter/package.json`: name=`l1-p10-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p11-starter/package.json`: name=`l1-p11-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p12-starter/package.json`: name=`l1-p12-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p13-starter/package.json`: name=`l1-p13-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p14-starter/package.json`: name=`l1-p14-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l1-p15-starter/package.json`: name=`l1-p15-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p01-starter/package.json`: name=`l2-p01-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p02-starter/package.json`: name=`l2-p02-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p03-starter/package.json`: name=`l2-p03-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p04-starter/package.json`: name=`l2-p04-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p05-starter/package.json`: name=`l2-p05-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p06-starter/package.json`: name=`l2-p06-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p07-starter/package.json`: name=`l2-p07-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p08-starter/package.json`: name=`l2-p08-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p09-starter/package.json`: name=`l2-p09-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p10-starter/package.json`: name=`l2-p10-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p11-starter/package.json`: name=`l2-p11-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p12-starter/package.json`: name=`l2-p12-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p13-starter/package.json`: name=`l2-p13-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p14-starter/package.json`: name=`l2-p14-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l2-p15-starter/package.json`: name=`l2-p15-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `packages/l3-p01-starter/package.json`: name=`l3-p01-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p02-starter/package.json`: name=`l3-p02-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p03-starter/package.json`: name=`l3-p03-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p04-starter/package.json`: name=`l3-p04-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p05-starter/package.json`: name=`l3-p05-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p06-starter/package.json`: name=`l3-p06-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p07-starter/package.json`: name=`l3-p07-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p08-starter/package.json`: name=`l3-p08-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p09-starter/package.json`: name=`l3-p09-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p10-starter/package.json`: name=`l3-p10-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p11-starter/package.json`: name=`l3-p11-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p12-starter/package.json`: name=`l3-p12-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p13-starter/package.json`: name=`l3-p13-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p14-starter/package.json`: name=`l3-p14-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `packages/l3-p15-starter/package.json`: name=`l3-p15-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build

### Seminar1_Partea3_p3-standalone.zip

> Structura este mare; se afișează începutul și sfârșitul.

```
.github/workflows/e2e-l3.yml
.github/workflows/lint.yml
.github/workflows/unit-jest.yml
.github/workflows/unit-vitest.yml
.github/workflows/workbox-l3.yml
L1/L1-P01/solution/.gitignore
L1/L1-P01/solution/README.md
L1/L1-P01/solution/babel.config.cjs
L1/L1-P01/solution/bin/cli.js
L1/L1-P01/solution/data/sample.csv
L1/L1-P01/solution/data/sample.json
L1/L1-P01/solution/eslint.config.mjs
L1/L1-P01/solution/jest.config.cjs
L1/L1-P01/solution/package.json
L1/L1-P01/solution/src/cli-runner.js
L1/L1-P01/solution/src/lib/filters.js
L1/L1-P01/solution/src/lib/format.js
L1/L1-P01/solution/src/lib/parse.js
L1/L1-P01/solution/src/lib/transform.js
L1/L1-P01/solution/tests/jest/cli.jest.test.js
L1/L1-P01/solution/tests/jest/parse.jest.test.js
L1/L1-P01/solution/tests/jest/transform.jest.test.js
L1/L1-P01/solution/tests/vitest/cli.test.js
L1/L1-P01/solution/tests/vitest/parse.test.js
L1/L1-P01/solution/tests/vitest/transform.test.js
L1/L1-P01/solution/vitest.config.ts
L1/L1-P01/starter/.gitignore
L1/L1-P01/starter/README.md
L1/L1-P01/starter/babel.config.cjs
L1/L1-P01/starter/bin/cli.js
L1/L1-P01/starter/data/sample.csv
L1/L1-P01/starter/data/sample.json
L1/L1-P01/starter/eslint.config.mjs
L1/L1-P01/starter/jest.config.cjs
L1/L1-P01/starter/package.json
L1/L1-P01/starter/src/cli-runner.js
L1/L1-P01/starter/src/lib/filters.js
L1/L1-P01/starter/src/lib/format.js
L1/L1-P01/starter/src/lib/parse.js
L1/L1-P01/starter/src/lib/transform.js
L1/L1-P01/starter/tests/jest/cli.jest.test.js
L1/L1-P01/starter/tests/jest/parse.jest.test.js
L1/L1-P01/starter/tests/jest/transform.jest.test.js
L1/L1-P01/starter/tests/vitest/cli.test.js
L1/L1-P01/starter/tests/vitest/parse.test.js
L1/L1-P01/starter/tests/vitest/transform.test.js
L1/L1-P01/starter/vitest.config.ts
L1/L1-P02/solution/.gitignore
L1/L1-P02/solution/README.md
L1/L1-P02/solution/babel.config.cjs
L1/L1-P02/solution/bin/cli.js
L1/L1-P02/solution/data/sample.csv
L1/L1-P02/solution/data/sample.json
L1/L1-P02/solution/eslint.config.mjs
L1/L1-P02/solution/jest.config.cjs
L1/L1-P02/solution/package.json
L1/L1-P02/solution/src/cli-runner.js
L1/L1-P02/solution/src/lib/filters.js
L1/L1-P02/solution/src/lib/format.js
L1/L1-P02/solution/src/lib/parse.js
L1/L1-P02/solution/src/lib/transform.js
L1/L1-P02/solution/tests/jest/cli.jest.test.js
L1/L1-P02/solution/tests/jest/parse.jest.test.js
L1/L1-P02/solution/tests/jest/transform.jest.test.js
L1/L1-P02/solution/tests/vitest/cli.test.js
L1/L1-P02/solution/tests/vitest/parse.test.js
L1/L1-P02/solution/tests/vitest/transform.test.js
L1/L1-P02/solution/vitest.config.ts
L1/L1-P02/starter/.gitignore
L1/L1-P02/starter/README.md
L1/L1-P02/starter/babel.config.cjs
L1/L1-P02/starter/bin/cli.js
L1/L1-P02/starter/data/sample.csv
L1/L1-P02/starter/data/sample.json
L1/L1-P02/starter/eslint.config.mjs
L1/L1-P02/starter/jest.config.cjs
L1/L1-P02/starter/package.json
L1/L1-P02/starter/src/cli-runner.js
L1/L1-P02/starter/src/lib/filters.js
L1/L1-P02/starter/src/lib/format.js
L1/L1-P02/starter/src/lib/parse.js
L1/L1-P02/starter/src/lib/transform.js
L1/L1-P02/starter/tests/jest/cli.jest.test.js
L1/L1-P02/starter/tests/jest/parse.jest.test.js
L1/L1-P02/starter/tests/jest/transform.jest.test.js
L1/L1-P02/starter/tests/vitest/cli.test.js
L1/L1-P02/starter/tests/vitest/parse.test.js
L1/L1-P02/starter/tests/vitest/transform.test.js
L1/L1-P02/starter/vitest.config.ts
L1/L1-P03/solution/.gitignore
L1/L1-P03/solution/README.md
L1/L1-P03/solution/babel.config.cjs
L1/L1-P03/solution/bin/cli.js
L1/L1-P03/solution/data/sample.csv
L1/L1-P03/solution/data/sample.json
L1/L1-P03/solution/eslint.config.mjs
L1/L1-P03/solution/jest.config.cjs
L1/L1-P03/solution/package.json
L1/L1-P03/solution/src/cli-runner.js
L1/L1-P03/solution/src/lib/filters.js
L1/L1-P03/solution/src/lib/format.js
L1/L1-P03/solution/src/lib/parse.js
L1/L1-P03/solution/src/lib/transform.js
L1/L1-P03/solution/tests/jest/cli.jest.test.js
L1/L1-P03/solution/tests/jest/parse.jest.test.js
L1/L1-P03/solution/tests/jest/transform.jest.test.js
L1/L1-P03/solution/tests/vitest/cli.test.js
L1/L1-P03/solution/tests/vitest/parse.test.js
L1/L1-P03/solution/tests/vitest/transform.test.js
L1/L1-P03/solution/vitest.config.ts
L1/L1-P03/starter/.gitignore
L1/L1-P03/starter/README.md
L1/L1-P03/starter/babel.config.cjs
L1/L1-P03/starter/bin/cli.js
L1/L1-P03/starter/data/sample.csv
L1/L1-P03/starter/data/sample.json
L1/L1-P03/starter/eslint.config.mjs
L1/L1-P03/starter/jest.config.cjs
L1/L1-P03/starter/package.json
L1/L1-P03/starter/src/cli-runner.js
L1/L1-P03/starter/src/lib/filters.js
L1/L1-P03/starter/src/lib/format.js
L1/L1-P03/starter/src/lib/parse.js
L1/L1-P03/starter/src/lib/transform.js
L1/L1-P03/starter/tests/jest/cli.jest.test.js
L1/L1-P03/starter/tests/jest/parse.jest.test.js
L1/L1-P03/starter/tests/jest/transform.jest.test.js
L1/L1-P03/starter/tests/vitest/cli.test.js
L1/L1-P03/starter/tests/vitest/parse.test.js
L1/L1-P03/starter/tests/vitest/transform.test.js
L1/L1-P03/starter/vitest.config.ts
L1/L1-P04/solution/.gitignore
L1/L1-P04/solution/README.md
L1/L1-P04/solution/babel.config.cjs
L1/L1-P04/solution/bin/cli.js
L1/L1-P04/solution/data/sample.csv
L1/L1-P04/solution/data/sample.json
L1/L1-P04/solution/eslint.config.mjs
L1/L1-P04/solution/jest.config.cjs
L1/L1-P04/solution/package.json
L1/L1-P04/solution/src/cli-runner.js
L1/L1-P04/solution/src/lib/filters.js
L1/L1-P04/solution/src/lib/format.js
L1/L1-P04/solution/src/lib/parse.js
L1/L1-P04/solution/src/lib/transform.js
L1/L1-P04/solution/tests/jest/cli.jest.test.js
L1/L1-P04/solution/tests/jest/parse.jest.test.js
L1/L1-P04/solution/tests/jest/transform.jest.test.js
L1/L1-P04/solution/tests/vitest/cli.test.js
L1/L1-P04/solution/tests/vitest/parse.test.js
L1/L1-P04/solution/tests/vitest/transform.test.js
L1/L1-P04/solution/vitest.config.ts
L1/L1-P04/starter/.gitignore
L1/L1-P04/starter/README.md
L1/L1-P04/starter/babel.config.cjs
L1/L1-P04/starter/bin/cli.js
L1/L1-P04/starter/data/sample.csv
L1/L1-P04/starter/data/sample.json
L1/L1-P04/starter/eslint.config.mjs
L1/L1-P04/starter/jest.config.cjs
L1/L1-P04/starter/package.json
L1/L1-P04/starter/src/cli-runner.js
L1/L1-P04/starter/src/lib/filters.js
L1/L1-P04/starter/src/lib/format.js
L1/L1-P04/starter/src/lib/parse.js
L1/L1-P04/starter/src/lib/transform.js
L1/L1-P04/starter/tests/jest/cli.jest.test.js
L1/L1-P04/starter/tests/jest/parse.jest.test.js
L1/L1-P04/starter/tests/jest/transform.jest.test.js
L1/L1-P04/starter/tests/vitest/cli.test.js
L1/L1-P04/starter/tests/vitest/parse.test.js
L1/L1-P04/starter/tests/vitest/transform.test.js
L1/L1-P04/starter/vitest.config.ts
L1/L1-P05/solution/.gitignore
L1/L1-P05/solution/README.md
L1/L1-P05/solution/babel.config.cjs
L1/L1-P05/solution/bin/cli.js
L1/L1-P05/solution/data/sample.csv
L1/L1-P05/solution/data/sample.json
L1/L1-P05/solution/eslint.config.mjs
L1/L1-P05/solution/jest.config.cjs
L1/L1-P05/solution/package.json
L1/L1-P05/solution/src/cli-runner.js
L1/L1-P05/solution/src/lib/filters.js
L1/L1-P05/solution/src/lib/format.js
L1/L1-P05/solution/src/lib/parse.js
L1/L1-P05/solution/src/lib/transform.js
L1/L1-P05/solution/tests/jest/cli.jest.test.js
L1/L1-P05/solution/tests/jest/parse.jest.test.js
L1/L1-P05/solution/tests/jest/transform.jest.test.js
L1/L1-P05/solution/tests/vitest/cli.test.js
L1/L1-P05/solution/tests/vitest/parse.test.js
L1/L1-P05/solution/tests/vitest/transform.test.js
L1/L1-P05/solution/vitest.config.ts
L1/L1-P05/starter/.gitignore
L1/L1-P05/starter/README.md
L1/L1-P05/starter/babel.config.cjs
L1/L1-P05/starter/bin/cli.js
L1/L1-P05/starter/data/sample.csv
L1/L1-P05/starter/data/sample.json
L1/L1-P05/starter/eslint.config.mjs
L1/L1-P05/starter/jest.config.cjs
L1/L1-P05/starter/package.json
L1/L1-P05/starter/src/cli-runner.js
L1/L1-P05/starter/src/lib/filters.js
L1/L1-P05/starter/src/lib/format.js
L1/L1-P05/starter/src/lib/parse.js
L1/L1-P05/starter/src/lib/transform.js
L1/L1-P05/starter/tests/jest/cli.jest.test.js
L1/L1-P05/starter/tests/jest/parse.jest.test.js
L1/L1-P05/starter/tests/jest/transform.jest.test.js
L1/L1-P05/starter/tests/vitest/cli.test.js
L1/L1-P05/starter/tests/vitest/parse.test.js
L1/L1-P05/starter/tests/vitest/transform.test.js
L1/L1-P05/starter/vitest.config.ts
L1/L1-P06/solution/.gitignore
L1/L1-P06/solution/README.md
L1/L1-P06/solution/babel.config.cjs
L1/L1-P06/solution/bin/cli.js
L1/L1-P06/solution/data/sample.csv
L1/L1-P06/solution/data/sample.json
L1/L1-P06/solution/eslint.config.mjs
L1/L1-P06/solution/jest.config.cjs
L1/L1-P06/solution/package.json
L1/L1-P06/solution/src/cli-runner.js
L1/L1-P06/solution/src/lib/filters.js
L1/L1-P06/solution/src/lib/format.js
L1/L1-P06/solution/src/lib/parse.js
L1/L1-P06/solution/src/lib/transform.js
L1/L1-P06/solution/tests/jest/cli.jest.test.js
L1/L1-P06/solution/tests/jest/parse.jest.test.js
L1/L1-P06/solution/tests/jest/transform.jest.test.js
L1/L1-P06/solution/tests/vitest/cli.test.js
L1/L1-P06/solution/tests/vitest/parse.test.js
L1/L1-P06/solution/tests/vitest/transform.test.js
L1/L1-P06/solution/vitest.config.ts
L1/L1-P06/starter/.gitignore
L1/L1-P06/starter/README.md
L1/L1-P06/starter/babel.config.cjs
L1/L1-P06/starter/bin/cli.js
L1/L1-P06/starter/data/sample.csv
L1/L1-P06/starter/data/sample.json
L1/L1-P06/starter/eslint.config.mjs
L1/L1-P06/starter/jest.config.cjs
L1/L1-P06/starter/package.json
L1/L1-P06/starter/src/cli-runner.js
L1/L1-P06/starter/src/lib/filters.js
L1/L1-P06/starter/src/lib/format.js
L1/L1-P06/starter/src/lib/parse.js
L1/L1-P06/starter/src/lib/transform.js
L1/L1-P06/starter/tests/jest/cli.jest.test.js
L1/L1-P06/starter/tests/jest/parse.jest.test.js
L1/L1-P06/starter/tests/jest/transform.jest.test.js
L1/L1-P06/starter/tests/vitest/cli.test.js
L1/L1-P06/starter/tests/vitest/parse.test.js
L1/L1-P06/starter/tests/vitest/transform.test.js
L1/L1-P06/starter/vitest.config.ts
L1/L1-P07/solution/.gitignore
L1/L1-P07/solution/README.md
L1/L1-P07/solution/babel.config.cjs
L1/L1-P07/solution/bin/cli.js
L1/L1-P07/solution/data/sample.csv
L1/L1-P07/solution/data/sample.json
L1/L1-P07/solution/eslint.config.mjs
L1/L1-P07/solution/jest.config.cjs
L1/L1-P07/solution/package.json
L1/L1-P07/solution/src/cli-runner.js
L1/L1-P07/solution/src/lib/filters.js
L1/L1-P07/solution/src/lib/format.js
L1/L1-P07/solution/src/lib/parse.js
L1/L1-P07/solution/src/lib/transform.js
L1/L1-P07/solution/tests/jest/cli.jest.test.js
L1/L1-P07/solution/tests/jest/parse.jest.test.js
L1/L1-P07/solution/tests/jest/transform.jest.test.js
L1/L1-P07/solution/tests/vitest/cli.test.js
L1/L1-P07/solution/tests/vitest/parse.test.js
L1/L1-P07/solution/tests/vitest/transform.test.js
L1/L1-P07/solution/vitest.config.ts
L1/L1-P07/starter/.gitignore
L1/L1-P07/starter/README.md
L1/L1-P07/starter/babel.config.cjs
L1/L1-P07/starter/bin/cli.js
L1/L1-P07/starter/data/sample.csv
L1/L1-P07/starter/data/sample.json
L1/L1-P07/starter/eslint.config.mjs
L1/L1-P07/starter/jest.config.cjs
L1/L1-P07/starter/package.json
L1/L1-P07/starter/src/cli-runner.js
L1/L1-P07/starter/src/lib/filters.js
L1/L1-P07/starter/src/lib/format.js
L1/L1-P07/starter/src/lib/parse.js
L1/L1-P07/starter/src/lib/transform.js
L1/L1-P07/starter/tests/jest/cli.jest.test.js
L1/L1-P07/starter/tests/jest/parse.jest.test.js
L1/L1-P07/starter/tests/jest/transform.jest.test.js
L1/L1-P07/starter/tests/vitest/cli.test.js
L1/L1-P07/starter/tests/vitest/parse.test.js
L1/L1-P07/starter/tests/vitest/transform.test.js
L1/L1-P07/starter/vitest.config.ts
L1/L1-P08/solution/.gitignore
L1/L1-P08/solution/README.md
L1/L1-P08/solution/babel.config.cjs
L1/L1-P08/solution/bin/cli.js
L1/L1-P08/solution/data/sample.csv
L1/L1-P08/solution/data/sample.json
L1/L1-P08/solution/eslint.config.mjs
L1/L1-P08/solution/jest.config.cjs
L1/L1-P08/solution/package.json
L1/L1-P08/solution/src/cli-runner.js
L1/L1-P08/solution/src/lib/filters.js
L1/L1-P08/solution/src/lib/format.js
L1/L1-P08/solution/src/lib/parse.js
L1/L1-P08/solution/src/lib/transform.js
L1/L1-P08/solution/tests/jest/cli.jest.test.js
L1/L1-P08/solution/tests/jest/parse.jest.test.js
L1/L1-P08/solution/tests/jest/transform.jest.test.js
L1/L1-P08/solution/tests/vitest/cli.test.js
L1/L1-P08/solution/tests/vitest/parse.test.js
L1/L1-P08/solution/tests/vitest/transform.test.js
L1/L1-P08/solution/vitest.config.ts
L1/L1-P08/starter/.gitignore
L1/L1-P08/starter/README.md
L1/L1-P08/starter/babel.config.cjs
L1/L1-P08/starter/bin/cli.js
L1/L1-P08/starter/data/sample.csv
L1/L1-P08/starter/data/sample.json
L1/L1-P08/starter/eslint.config.mjs
L1/L1-P08/starter/jest.config.cjs
L1/L1-P08/starter/package.json
L1/L1-P08/starter/src/cli-runner.js
L1/L1-P08/starter/src/lib/filters.js
L1/L1-P08/starter/src/lib/format.js
L1/L1-P08/starter/src/lib/parse.js
L1/L1-P08/starter/src/lib/transform.js
L1/L1-P08/starter/tests/jest/cli.jest.test.js
L1/L1-P08/starter/tests/jest/parse.jest.test.js
L1/L1-P08/starter/tests/jest/transform.jest.test.js
L1/L1-P08/starter/tests/vitest/cli.test.js
L1/L1-P08/starter/tests/vitest/parse.test.js
L1/L1-P08/starter/tests/vitest/transform.test.js
L1/L1-P08/starter/vitest.config.ts
L1/L1-P09/solution/.gitignore
L1/L1-P09/solution/README.md
L1/L1-P09/solution/babel.config.cjs
L1/L1-P09/solution/bin/cli.js
L1/L1-P09/solution/data/sample.csv
L1/L1-P09/solution/data/sample.json
L1/L1-P09/solution/eslint.config.mjs
L1/L1-P09/solution/jest.config.cjs
L1/L1-P09/solution/package.json
L1/L1-P09/solution/src/cli-runner.js
L1/L1-P09/solution/src/lib/filters.js
L1/L1-P09/solution/src/lib/format.js
L1/L1-P09/solution/src/lib/parse.js
L1/L1-P09/solution/src/lib/transform.js
L1/L1-P09/solution/tests/jest/cli.jest.test.js
L1/L1-P09/solution/tests/jest/parse.jest.test.js
L1/L1-P09/solution/tests/jest/transform.jest.test.js
L1/L1-P09/solution/tests/vitest/cli.test.js
L1/L1-P09/solution/tests/vitest/parse.test.js
L1/L1-P09/solution/tests/vitest/transform.test.js
L1/L1-P09/solution/vitest.config.ts
L1/L1-P09/starter/.gitignore
L1/L1-P09/starter/README.md
L1/L1-P09/starter/babel.config.cjs
L1/L1-P09/starter/bin/cli.js
L1/L1-P09/starter/data/sample.csv
L1/L1-P09/starter/data/sample.json
L1/L1-P09/starter/eslint.config.mjs
L1/L1-P09/starter/jest.config.cjs
L1/L1-P09/starter/package.json
L1/L1-P09/starter/src/cli-runner.js
L1/L1-P09/starter/src/lib/filters.js
L1/L1-P09/starter/src/lib/format.js
L1/L1-P09/starter/src/lib/parse.js
L1/L1-P09/starter/src/lib/transform.js
L1/L1-P09/starter/tests/jest/cli.jest.test.js
L1/L1-P09/starter/tests/jest/parse.jest.test.js
L1/L1-P09/starter/tests/jest/transform.jest.test.js
L1/L1-P09/starter/tests/vitest/cli.test.js
L1/L1-P09/starter/tests/vitest/parse.test.js
L1/L1-P09/starter/tests/vitest/transform.test.js
L1/L1-P09/starter/vitest.config.ts
L1/L1-P10/solution/.gitignore
L1/L1-P10/solution/README.md
L1/L1-P10/solution/babel.config.cjs
L1/L1-P10/solution/bin/cli.js
L1/L1-P10/solution/data/sample.csv
L1/L1-P10/solution/data/sample.json
L1/L1-P10/solution/eslint.config.mjs
L1/L1-P10/solution/jest.config.cjs
L1/L1-P10/solution/package.json
L1/L1-P10/solution/src/cli-runner.js
L1/L1-P10/solution/src/lib/filters.js
L1/L1-P10/solution/src/lib/format.js
L1/L1-P10/solution/src/lib/parse.js
L1/L1-P10/solution/src/lib/transform.js
L1/L1-P10/solution/tests/jest/cli.jest.test.js
L1/L1-P10/solution/tests/jest/parse.jest.test.js
L1/L1-P10/solution/tests/jest/transform.jest.test.js
L1/L1-P10/solution/tests/vitest/cli.test.js
L1/L1-P10/solution/tests/vitest/parse.test.js
L1/L1-P10/solution/tests/vitest/transform.test.js
L1/L1-P10/solution/vitest.config.ts
L1/L1-P10/starter/.gitignore
L1/L1-P10/starter/README.md
L1/L1-P10/starter/babel.config.cjs
L1/L1-P10/starter/bin/cli.js
L1/L1-P10/starter/data/sample.csv
L1/L1-P10/starter/data/sample.json
L1/L1-P10/starter/eslint.config.mjs
L1/L1-P10/starter/jest.config.cjs
L1/L1-P10/starter/package.json
L1/L1-P10/starter/src/cli-runner.js
L1/L1-P10/starter/src/lib/filters.js
L1/L1-P10/starter/src/lib/format.js
L1/L1-P10/starter/src/lib/parse.js
L1/L1-P10/starter/src/lib/transform.js
L1/L1-P10/starter/tests/jest/cli.jest.test.js
L1/L1-P10/starter/tests/jest/parse.jest.test.js
L1/L1-P10/starter/tests/jest/transform.jest.test.js
L1/L1-P10/starter/tests/vitest/cli.test.js
L1/L1-P10/starter/tests/vitest/parse.test.js
L1/L1-P10/starter/tests/vitest/transform.test.js
L1/L1-P10/starter/vitest.config.ts
L1/L1-P11/solution/.gitignore
L1/L1-P11/solution/README.md
L1/L1-P11/solution/babel.config.cjs
L1/L1-P11/solution/bin/cli.js
L1/L1-P11/solution/data/sample.csv
L1/L1-P11/solution/data/sample.json
L1/L1-P11/solution/eslint.config.mjs
L1/L1-P11/solution/jest.config.cjs
L1/L1-P11/solution/package.json
L1/L1-P11/solution/src/cli-runner.js
L1/L1-P11/solution/src/lib/filters.js
L1/L1-P11/solution/src/lib/format.js
L1/L1-P11/solution/src/lib/parse.js
L1/L1-P11/solution/src/lib/transform.js
L1/L1-P11/solution/tests/jest/cli.jest.test.js
L1/L1-P11/solution/tests/jest/parse.jest.test.js
L1/L1-P11/solution/tests/jest/transform.jest.test.js
L1/L1-P11/solution/tests/vitest/cli.test.js
L1/L1-P11/solution/tests/vitest/parse.test.js
L1/L1-P11/solution/tests/vitest/transform.test.js
L1/L1-P11/solution/vitest.config.ts
L1/L1-P11/starter/.gitignore
L1/L1-P11/starter/README.md
L1/L1-P11/starter/babel.config.cjs
L1/L1-P11/starter/bin/cli.js
L1/L1-P11/starter/data/sample.csv
L1/L1-P11/starter/data/sample.json
L1/L1-P11/starter/eslint.config.mjs
L1/L1-P11/starter/jest.config.cjs
L1/L1-P11/starter/package.json
L1/L1-P11/starter/src/cli-runner.js
L1/L1-P11/starter/src/lib/filters.js
L1/L1-P11/starter/src/lib/format.js
L1/L1-P11/starter/src/lib/parse.js
L1/L1-P11/starter/src/lib/transform.js
L1/L1-P11/starter/tests/jest/cli.jest.test.js
L1/L1-P11/starter/tests/jest/parse.jest.test.js
L1/L1-P11/starter/tests/jest/transform.jest.test.js
L1/L1-P11/starter/tests/vitest/cli.test.js
L1/L1-P11/starter/tests/vitest/parse.test.js
L1/L1-P11/starter/tests/vitest/transform.test.js
L1/L1-P11/starter/vitest.config.ts
L1/L1-P12/solution/.gitignore
L1/L1-P12/solution/README.md
L1/L1-P12/solution/babel.config.cjs
L1/L1-P12/solution/bin/cli.js
L1/L1-P12/solution/data/sample.csv
L1/L1-P12/solution/data/sample.json
L1/L1-P12/solution/eslint.config.mjs
L1/L1-P12/solution/jest.config.cjs
L1/L1-P12/solution/package.json
L1/L1-P12/solution/src/cli-runner.js
L1/L1-P12/solution/src/lib/filters.js
L1/L1-P12/solution/src/lib/format.js
L1/L1-P12/solution/src/lib/parse.js
L1/L1-P12/solution/src/lib/transform.js
L1/L1-P12/solution/tests/jest/cli.jest.test.js
L1/L1-P12/solution/tests/jest/parse.jest.test.js
L1/L1-P12/solution/tests/jest/transform.jest.test.js
L1/L1-P12/solution/tests/vitest/cli.test.js
L1/L1-P12/solution/tests/vitest/parse.test.js
L1/L1-P12/solution/tests/vitest/transform.test.js
L1/L1-P12/solution/vitest.config.ts
L1/L1-P12/starter/.gitignore
L1/L1-P12/starter/README.md
L1/L1-P12/starter/babel.config.cjs
L1/L1-P12/starter/bin/cli.js
L1/L1-P12/starter/data/sample.csv
L1/L1-P12/starter/data/sample.json
L1/L1-P12/starter/eslint.config.mjs
L1/L1-P12/starter/jest.config.cjs
L1/L1-P12/starter/package.json
L1/L1-P12/starter/src/cli-runner.js
L1/L1-P12/starter/src/lib/filters.js
L1/L1-P12/starter/src/lib/format.js
L1/L1-P12/starter/src/lib/parse.js
L1/L1-P12/starter/src/lib/transform.js
L1/L1-P12/starter/tests/jest/cli.jest.test.js
L1/L1-P12/starter/tests/jest/parse.jest.test.js
L1/L1-P12/starter/tests/jest/transform.jest.test.js
L1/L1-P12/starter/tests/vitest/cli.test.js
L1/L1-P12/starter/tests/vitest/parse.test.js
L1/L1-P12/starter/tests/vitest/transform.test.js
L1/L1-P12/starter/vitest.config.ts
L1/L1-P13/solution/.gitignore
L1/L1-P13/solution/README.md
L1/L1-P13/solution/babel.config.cjs
L1/L1-P13/solution/bin/cli.js
L1/L1-P13/solution/data/sample.csv
L1/L1-P13/solution/data/sample.json
L1/L1-P13/solution/eslint.config.mjs
L1/L1-P13/solution/jest.config.cjs
L1/L1-P13/solution/package.json
L1/L1-P13/solution/src/cli-runner.js
L1/L1-P13/solution/src/lib/filters.js
L1/L1-P13/solution/src/lib/format.js
L1/L1-P13/solution/src/lib/parse.js
L1/L1-P13/solution/src/lib/transform.js
L1/L1-P13/solution/tests/jest/cli.jest.test.js
L1/L1-P13/solution/tests/jest/parse.jest.test.js
L1/L1-P13/solution/tests/jest/transform.jest.test.js
L1/L1-P13/solution/tests/vitest/cli.test.js
L1/L1-P13/solution/tests/vitest/parse.test.js
L1/L1-P13/solution/tests/vitest/transform.test.js
L1/L1-P13/solution/vitest.config.ts
L1/L1-P13/starter/.gitignore
L1/L1-P13/starter/README.md
L1/L1-P13/starter/babel.config.cjs
L1/L1-P13/starter/bin/cli.js
L1/L1-P13/starter/data/sample.csv
L1/L1-P13/starter/data/sample.json
L1/L1-P13/starter/eslint.config.mjs
L1/L1-P13/starter/jest.config.cjs
L1/L1-P13/starter/package.json
L1/L1-P13/starter/src/cli-runner.js
L1/L1-P13/starter/src/lib/filters.js
L1/L1-P13/starter/src/lib/format.js
L1/L1-P13/starter/src/lib/parse.js
L1/L1-P13/starter/src/lib/transform.js
L1/L1-P13/starter/tests/jest/cli.jest.test.js
L1/L1-P13/starter/tests/jest/parse.jest.test.js
L1/L1-P13/starter/tests/jest/transform.jest.test.js
L1/L1-P13/starter/tests/vitest/cli.test.js
L1/L1-P13/starter/tests/vitest/parse.test.js
L1/L1-P13/starter/tests/vitest/transform.test.js
L1/L1-P13/starter/vitest.config.ts
L1/L1-P14/solution/.gitignore
L1/L1-P14/solution/README.md
L1/L1-P14/solution/babel.config.cjs
L1/L1-P14/solution/bin/cli.js
L1/L1-P14/solution/data/sample.csv
L1/L1-P14/solution/data/sample.json
L1/L1-P14/solution/eslint.config.mjs
L1/L1-P14/solution/jest.config.cjs
L1/L1-P14/solution/package.json
L1/L1-P14/solution/src/cli-runner.js
L1/L1-P14/solution/src/lib/filters.js
L1/L1-P14/solution/src/lib/format.js
L1/L1-P14/solution/src/lib/parse.js
L1/L1-P14/solution/src/lib/transform.js
L1/L1-P14/solution/tests/jest/cli.jest.test.js
L1/L1-P14/solution/tests/jest/parse.jest.test.js
L1/L1-P14/solution/tests/jest/transform.jest.test.js
L1/L1-P14/solution/tests/vitest/cli.test.js
L1/L1-P14/solution/tests/vitest/parse.test.js
L1/L1-P14/solution/tests/vitest/transform.test.js
L1/L1-P14/solution/vitest.config.ts
L1/L1-P14/starter/.gitignore
L1/L1-P14/starter/README.md
L1/L1-P14/starter/babel.config.cjs
L1/L1-P14/starter/bin/cli.js
L1/L1-P14/starter/data/sample.csv
L1/L1-P14/starter/data/sample.json
L1/L1-P14/starter/eslint.config.mjs
L1/L1-P14/starter/jest.config.cjs
L1/L1-P14/starter/package.json
L1/L1-P14/starter/src/cli-runner.js
L1/L1-P14/starter/src/lib/filters.js
L1/L1-P14/starter/src/lib/format.js
L1/L1-P14/starter/src/lib/parse.js
L1/L1-P14/starter/src/lib/transform.js
L1/L1-P14/starter/tests/jest/cli.jest.test.js
L1/L1-P14/starter/tests/jest/parse.jest.test.js
L1/L1-P14/starter/tests/jest/transform.jest.test.js
L1/L1-P14/starter/tests/vitest/cli.test.js
L1/L1-P14/starter/tests/vitest/parse.test.js
L1/L1-P14/starter/tests/vitest/transform.test.js
L1/L1-P14/starter/vitest.config.ts
L1/L1-P15/solution/.gitignore
L1/L1-P15/solution/README.md
L1/L1-P15/solution/babel.config.cjs
L1/L1-P15/solution/bin/cli.js
L1/L1-P15/solution/data/sample.csv
L1/L1-P15/solution/data/sample.json
L1/L1-P15/solution/eslint.config.mjs
L1/L1-P15/solution/jest.config.cjs
L1/L1-P15/solution/package.json
L1/L1-P15/solution/src/cli-runner.js
L1/L1-P15/solution/src/lib/filters.js
L1/L1-P15/solution/src/lib/format.js
L1/L1-P15/solution/src/lib/parse.js
L1/L1-P15/solution/src/lib/transform.js
L1/L1-P15/solution/tests/jest/cli.jest.test.js
L1/L1-P15/solution/tests/jest/parse.jest.test.js
L1/L1-P15/solution/tests/jest/transform.jest.test.js
L1/L1-P15/solution/tests/vitest/cli.test.js
L1/L1-P15/solution/tests/vitest/parse.test.js
L1/L1-P15/solution/tests/vitest/transform.test.js
L1/L1-P15/solution/vitest.config.ts
L1/L1-P15/starter/.gitignore
L1/L1-P15/starter/README.md
L1/L1-P15/starter/babel.config.cjs
L1/L1-P15/starter/bin/cli.js
L1/L1-P15/starter/data/sample.csv
L1/L1-P15/starter/data/sample.json
L1/L1-P15/starter/eslint.config.mjs
L1/L1-P15/starter/jest.config.cjs
L1/L1-P15/starter/package.json
L1/L1-P15/starter/src/cli-runner.js
L1/L1-P15/starter/src/lib/filters.js
L1/L1-P15/starter/src/lib/format.js
L1/L1-P15/starter/src/lib/parse.js
L1/L1-P15/starter/src/lib/transform.js
L1/L1-P15/starter/tests/jest/cli.jest.test.js
L1/L1-P15/starter/tests/jest/parse.jest.test.js
L1/L1-P15/starter/tests/jest/transform.jest.test.js
L1/L1-P15/starter/tests/vitest/cli.test.js
L1/L1-P15/starter/tests/vitest/parse.test.js
L1/L1-P15/starter/tests/vitest/transform.test.js
L1/L1-P15/starter/vitest.config.ts
L2/L2-P01/solution/.gitignore
L2/L2-P01/solution/README.md
L2/L2-P01/solution/babel.config.cjs
L2/L2-P01/solution/bin/cli.js
L2/L2-P01/solution/data/sample.csv
L2/L2-P01/solution/data/sample.json
L2/L2-P01/solution/eslint.config.mjs
L2/L2-P01/solution/jest.config.cjs
L2/L2-P01/solution/package.json
L2/L2-P01/solution/src/cli-runner.js
L2/L2-P01/solution/src/lib/filters.js
L2/L2-P01/solution/src/lib/format.js
L2/L2-P01/solution/src/lib/parse.js
L2/L2-P01/solution/src/lib/transform.js
L2/L2-P01/solution/tests/jest/cli.jest.test.js
L2/L2-P01/solution/tests/jest/parse.jest.test.js
L2/L2-P01/solution/tests/jest/transform.jest.test.js
L2/L2-P01/solution/tests/vitest/cli.test.js
L2/L2-P01/solution/tests/vitest/parse.test.js
L2/L2-P01/solution/tests/vitest/transform.test.js
L2/L2-P01/solution/vitest.config.ts
L2/L2-P01/starter/.gitignore
L2/L2-P01/starter/README.md
L2/L2-P01/starter/babel.config.cjs
L2/L2-P01/starter/bin/cli.js
L2/L2-P01/starter/data/sample.csv
L2/L2-P01/starter/data/sample.json
L2/L2-P01/starter/eslint.config.mjs
L2/L2-P01/starter/jest.config.cjs
L2/L2-P01/starter/package.json
L2/L2-P01/starter/src/cli-runner.js
L2/L2-P01/starter/src/lib/filters.js
L2/L2-P01/starter/src/lib/format.js
L2/L2-P01/starter/src/lib/parse.js
L2/L2-P01/starter/src/lib/transform.js
L2/L2-P01/starter/tests/jest/cli.jest.test.js
L2/L2-P01/starter/tests/jest/parse.jest.test.js
L2/L2-P01/starter/tests/jest/transform.jest.test.js
L2/L2-P01/starter/tests/vitest/cli.test.js
L2/L2-P01/starter/tests/vitest/parse.test.js
L2/L2-P01/starter/tests/vitest/transform.test.js
L2/L2-P01/starter/vitest.config.ts
L2/L2-P02/solution/.gitignore
L2/L2-P02/solution/README.md
L2/L2-P02/solution/babel.config.cjs
L2/L2-P02/solution/bin/cli.js
L2/L2-P02/solution/data/sample.csv
L2/L2-P02/solution/data/sample.json
L2/L2-P02/solution/eslint.config.mjs
L2/L2-P02/solution/jest.config.cjs
L2/L2-P02/solution/package.json
L2/L2-P02/solution/src/cli-runner.js
L2/L2-P02/solution/src/lib/filters.js
L2/L2-P02/solution/src/lib/format.js
L2/L2-P02/solution/src/lib/parse.js
L2/L2-P02/solution/src/lib/transform.js
L2/L2-P02/solution/tests/jest/cli.jest.test.js
L2/L2-P02/solution/tests/jest/parse.jest.test.js
L2/L2-P02/solution/tests/jest/transform.jest.test.js
L2/L2-P02/solution/tests/vitest/cli.test.js
L2/L2-P02/solution/tests/vitest/parse.test.js
L2/L2-P02/solution/tests/vitest/transform.test.js
L2/L2-P02/solution/vitest.config.ts
L2/L2-P02/starter/.gitignore
L2/L2-P02/starter/README.md
L2/L2-P02/starter/babel.config.cjs
L2/L2-P02/starter/bin/cli.js
L2/L2-P02/starter/data/sample.csv
L2/L2-P02/starter/data/sample.json
L2/L2-P02/starter/eslint.config.mjs
L2/L2-P02/starter/jest.config.cjs
L2/L2-P02/starter/package.json
L2/L2-P02/starter/src/cli-runner.js
L2/L2-P02/starter/src/lib/filters.js
L2/L2-P02/starter/src/lib/format.js
L2/L2-P02/starter/src/lib/parse.js
L2/L2-P02/starter/src/lib/transform.js
L2/L2-P02/starter/tests/jest/cli.jest.test.js
L2/L2-P02/starter/tests/jest/parse.jest.test.js
L2/L2-P02/starter/tests/jest/transform.jest.test.js
L2/L2-P02/starter/tests/vitest/cli.test.js
L2/L2-P02/starter/tests/vitest/parse.test.js
L2/L2-P02/starter/tests/vitest/transform.test.js
L2/L2-P02/starter/vitest.config.ts
L2/L2-P03/solution/.gitignore
L2/L2-P03/solution/README.md
L2/L2-P03/solution/babel.config.cjs
L2/L2-P03/solution/bin/cli.js
L2/L2-P03/solution/data/sample.csv
L2/L2-P03/solution/data/sample.json
L2/L2-P03/solution/eslint.config.mjs
L2/L2-P03/solution/jest.config.cjs
L2/L2-P03/solution/package.json
L2/L2-P03/solution/src/cli-runner.js
L2/L2-P03/solution/src/lib/filters.js
L2/L2-P03/solution/src/lib/format.js
L2/L2-P03/solution/src/lib/parse.js
L2/L2-P03/solution/src/lib/transform.js
L2/L2-P03/solution/tests/jest/cli.jest.test.js
L2/L2-P03/solution/tests/jest/parse.jest.test.js
L2/L2-P03/solution/tests/jest/transform.jest.test.js
L2/L2-P03/solution/tests/vitest/cli.test.js
L2/L2-P03/solution/tests/vitest/parse.test.js
L2/L2-P03/solution/tests/vitest/transform.test.js
L2/L2-P03/solution/vitest.config.ts
L2/L2-P03/starter/.gitignore
L2/L2-P03/starter/README.md
L2/L2-P03/starter/babel.config.cjs
L2/L2-P03/starter/bin/cli.js
L2/L2-P03/starter/data/sample.csv
L2/L2-P03/starter/data/sample.json
L2/L2-P03/starter/eslint.config.mjs
L2/L2-P03/starter/jest.config.cjs
L2/L2-P03/starter/package.json
L2/L2-P03/starter/src/cli-runner.js
L2/L2-P03/starter/src/lib/filters.js
L2/L2-P03/starter/src/lib/format.js
L2/L2-P03/starter/src/lib/parse.js
L2/L2-P03/starter/src/lib/transform.js
L2/L2-P03/starter/tests/jest/cli.jest.test.js
L2/L2-P03/starter/tests/jest/parse.jest.test.js
L2/L2-P03/starter/tests/jest/transform.jest.test.js
L2/L2-P03/starter/tests/vitest/cli.test.js
L2/L2-P03/starter/tests/vitest/parse.test.js
L2/L2-P03/starter/tests/vitest/transform.test.js
L2/L2-P03/starter/vitest.config.ts
L2/L2-P04/solution/.gitignore
L2/L2-P04/solution/README.md
L2/L2-P04/solution/babel.config.cjs
L2/L2-P04/solution/bin/cli.js
L2/L2-P04/solution/data/sample.csv
L2/L2-P04/solution/data/sample.json
L2/L2-P04/solution/eslint.config.mjs
L2/L2-P04/solution/jest.config.cjs
L2/L2-P04/solution/package.json
L2/L2-P04/solution/src/cli-runner.js
L2/L2-P04/solution/src/lib/filters.js
L2/L2-P04/solution/src/lib/format.js
L2/L2-P04/solution/src/lib/parse.js
L2/L2-P04/solution/src/lib/transform.js
L2/L2-P04/solution/tests/jest/cli.jest.test.js
L2/L2-P04/solution/tests/jest/parse.jest.test.js
L2/L2-P04/solution/tests/jest/transform.jest.test.js
L2/L2-P04/solution/tests/vitest/cli.test.js
L2/L2-P04/solution/tests/vitest/parse.test.js
L2/L2-P04/solution/tests/vitest/transform.test.js
L2/L2-P04/solution/vitest.config.ts
L2/L2-P04/starter/.gitignore
L2/L2-P04/starter/README.md
L2/L2-P04/starter/babel.config.cjs
L2/L2-P04/starter/bin/cli.js
L2/L2-P04/starter/data/sample.csv
L2/L2-P04/starter/data/sample.json
L2/L2-P04/starter/eslint.config.mjs
L2/L2-P04/starter/jest.config.cjs
L2/L2-P04/starter/package.json
L2/L2-P04/starter/src/cli-runner.js
L2/L2-P04/starter/src/lib/filters.js
L2/L2-P04/starter/src/lib/format.js
L2/L2-P04/starter/src/lib/parse.js
L2/L2-P04/starter/src/lib/transform.js
L2/L2-P04/starter/tests/jest/cli.jest.test.js
L2/L2-P04/starter/tests/jest/parse.jest.test.js
L2/L2-P04/starter/tests/jest/transform.jest.test.js
L2/L2-P04/starter/tests/vitest/cli.test.js
…
L3/L3-P01/solution/playwright.config.ts
L3/L3-P01/solution/public/index.html
L3/L3-P01/solution/public/manifest.webmanifest
L3/L3-P01/solution/scripts/build-sw.mjs
L3/L3-P01/solution/server.mjs
L3/L3-P01/solution/src/cli-runner.js
L3/L3-P01/solution/src/lib/filters.js
L3/L3-P01/solution/src/lib/format.js
L3/L3-P01/solution/src/lib/parse.js
L3/L3-P01/solution/src/lib/transform.js
L3/L3-P01/solution/tests/jest/cli.jest.test.js
L3/L3-P01/solution/tests/jest/parse.jest.test.js
L3/L3-P01/solution/tests/jest/transform.jest.test.js
L3/L3-P01/solution/tests/vitest/cli.test.js
L3/L3-P01/solution/tests/vitest/parse.test.js
L3/L3-P01/solution/tests/vitest/transform.test.js
L3/L3-P01/solution/vitest.config.ts
L3/L3-P01/starter/.gitignore
L3/L3-P01/starter/README.md
L3/L3-P01/starter/babel.config.cjs
L3/L3-P01/starter/bin/cli.js
L3/L3-P01/starter/data/sample.csv
L3/L3-P01/starter/data/sample.json
L3/L3-P01/starter/e2e/example.spec.ts
L3/L3-P01/starter/eslint.config.mjs
L3/L3-P01/starter/jest.config.cjs
L3/L3-P01/starter/package.json
L3/L3-P01/starter/playwright.config.ts
L3/L3-P01/starter/public/index.html
L3/L3-P01/starter/public/manifest.webmanifest
L3/L3-P01/starter/scripts/build-sw.mjs
L3/L3-P01/starter/server.mjs
L3/L3-P01/starter/src/cli-runner.js
L3/L3-P01/starter/src/lib/filters.js
L3/L3-P01/starter/src/lib/format.js
L3/L3-P01/starter/src/lib/parse.js
L3/L3-P01/starter/src/lib/transform.js
L3/L3-P01/starter/tests/jest/cli.jest.test.js
L3/L3-P01/starter/tests/jest/parse.jest.test.js
L3/L3-P01/starter/tests/jest/transform.jest.test.js
L3/L3-P01/starter/tests/vitest/cli.test.js
L3/L3-P01/starter/tests/vitest/parse.test.js
L3/L3-P01/starter/tests/vitest/transform.test.js
L3/L3-P01/starter/vitest.config.ts
L3/L3-P02/solution/.gitignore
L3/L3-P02/solution/README.md
L3/L3-P02/solution/babel.config.cjs
L3/L3-P02/solution/bin/cli.js
L3/L3-P02/solution/data/sample.csv
L3/L3-P02/solution/data/sample.json
L3/L3-P02/solution/e2e/example.spec.ts
L3/L3-P02/solution/eslint.config.mjs
L3/L3-P02/solution/jest.config.cjs
L3/L3-P02/solution/package.json
L3/L3-P02/solution/playwright.config.ts
L3/L3-P02/solution/public/index.html
L3/L3-P02/solution/public/manifest.webmanifest
L3/L3-P02/solution/scripts/build-sw.mjs
L3/L3-P02/solution/server.mjs
L3/L3-P02/solution/src/cli-runner.js
L3/L3-P02/solution/src/lib/filters.js
L3/L3-P02/solution/src/lib/format.js
L3/L3-P02/solution/src/lib/parse.js
L3/L3-P02/solution/src/lib/transform.js
L3/L3-P02/solution/tests/jest/cli.jest.test.js
L3/L3-P02/solution/tests/jest/parse.jest.test.js
L3/L3-P02/solution/tests/jest/transform.jest.test.js
L3/L3-P02/solution/tests/vitest/cli.test.js
L3/L3-P02/solution/tests/vitest/parse.test.js
L3/L3-P02/solution/tests/vitest/transform.test.js
L3/L3-P02/solution/vitest.config.ts
L3/L3-P02/starter/.gitignore
L3/L3-P02/starter/README.md
L3/L3-P02/starter/babel.config.cjs
L3/L3-P02/starter/bin/cli.js
L3/L3-P02/starter/data/sample.csv
L3/L3-P02/starter/data/sample.json
L3/L3-P02/starter/e2e/example.spec.ts
L3/L3-P02/starter/eslint.config.mjs
L3/L3-P02/starter/jest.config.cjs
L3/L3-P02/starter/package.json
L3/L3-P02/starter/playwright.config.ts
L3/L3-P02/starter/public/index.html
L3/L3-P02/starter/public/manifest.webmanifest
L3/L3-P02/starter/scripts/build-sw.mjs
L3/L3-P02/starter/server.mjs
L3/L3-P02/starter/src/cli-runner.js
L3/L3-P02/starter/src/lib/filters.js
L3/L3-P02/starter/src/lib/format.js
L3/L3-P02/starter/src/lib/parse.js
L3/L3-P02/starter/src/lib/transform.js
L3/L3-P02/starter/tests/jest/cli.jest.test.js
L3/L3-P02/starter/tests/jest/parse.jest.test.js
L3/L3-P02/starter/tests/jest/transform.jest.test.js
L3/L3-P02/starter/tests/vitest/cli.test.js
L3/L3-P02/starter/tests/vitest/parse.test.js
L3/L3-P02/starter/tests/vitest/transform.test.js
L3/L3-P02/starter/vitest.config.ts
L3/L3-P03/solution/.gitignore
L3/L3-P03/solution/README.md
L3/L3-P03/solution/babel.config.cjs
L3/L3-P03/solution/bin/cli.js
L3/L3-P03/solution/data/sample.csv
L3/L3-P03/solution/data/sample.json
L3/L3-P03/solution/e2e/example.spec.ts
L3/L3-P03/solution/eslint.config.mjs
L3/L3-P03/solution/jest.config.cjs
L3/L3-P03/solution/package.json
L3/L3-P03/solution/playwright.config.ts
L3/L3-P03/solution/public/index.html
L3/L3-P03/solution/public/manifest.webmanifest
L3/L3-P03/solution/scripts/build-sw.mjs
L3/L3-P03/solution/server.mjs
L3/L3-P03/solution/src/cli-runner.js
L3/L3-P03/solution/src/lib/filters.js
L3/L3-P03/solution/src/lib/format.js
L3/L3-P03/solution/src/lib/parse.js
L3/L3-P03/solution/src/lib/transform.js
L3/L3-P03/solution/tests/jest/cli.jest.test.js
L3/L3-P03/solution/tests/jest/parse.jest.test.js
L3/L3-P03/solution/tests/jest/transform.jest.test.js
L3/L3-P03/solution/tests/vitest/cli.test.js
L3/L3-P03/solution/tests/vitest/parse.test.js
L3/L3-P03/solution/tests/vitest/transform.test.js
L3/L3-P03/solution/vitest.config.ts
L3/L3-P03/starter/.gitignore
L3/L3-P03/starter/README.md
L3/L3-P03/starter/babel.config.cjs
L3/L3-P03/starter/bin/cli.js
L3/L3-P03/starter/data/sample.csv
L3/L3-P03/starter/data/sample.json
L3/L3-P03/starter/e2e/example.spec.ts
L3/L3-P03/starter/eslint.config.mjs
L3/L3-P03/starter/jest.config.cjs
L3/L3-P03/starter/package.json
L3/L3-P03/starter/playwright.config.ts
L3/L3-P03/starter/public/index.html
L3/L3-P03/starter/public/manifest.webmanifest
L3/L3-P03/starter/scripts/build-sw.mjs
L3/L3-P03/starter/server.mjs
L3/L3-P03/starter/src/cli-runner.js
L3/L3-P03/starter/src/lib/filters.js
L3/L3-P03/starter/src/lib/format.js
L3/L3-P03/starter/src/lib/parse.js
L3/L3-P03/starter/src/lib/transform.js
L3/L3-P03/starter/tests/jest/cli.jest.test.js
L3/L3-P03/starter/tests/jest/parse.jest.test.js
L3/L3-P03/starter/tests/jest/transform.jest.test.js
L3/L3-P03/starter/tests/vitest/cli.test.js
L3/L3-P03/starter/tests/vitest/parse.test.js
L3/L3-P03/starter/tests/vitest/transform.test.js
L3/L3-P03/starter/vitest.config.ts
L3/L3-P04/solution/.gitignore
L3/L3-P04/solution/README.md
L3/L3-P04/solution/babel.config.cjs
L3/L3-P04/solution/bin/cli.js
L3/L3-P04/solution/data/sample.csv
L3/L3-P04/solution/data/sample.json
L3/L3-P04/solution/e2e/example.spec.ts
L3/L3-P04/solution/eslint.config.mjs
L3/L3-P04/solution/jest.config.cjs
L3/L3-P04/solution/package.json
L3/L3-P04/solution/playwright.config.ts
L3/L3-P04/solution/public/index.html
L3/L3-P04/solution/public/manifest.webmanifest
L3/L3-P04/solution/scripts/build-sw.mjs
L3/L3-P04/solution/server.mjs
L3/L3-P04/solution/src/cli-runner.js
L3/L3-P04/solution/src/lib/filters.js
L3/L3-P04/solution/src/lib/format.js
L3/L3-P04/solution/src/lib/parse.js
L3/L3-P04/solution/src/lib/transform.js
L3/L3-P04/solution/tests/jest/cli.jest.test.js
L3/L3-P04/solution/tests/jest/parse.jest.test.js
L3/L3-P04/solution/tests/jest/transform.jest.test.js
L3/L3-P04/solution/tests/vitest/cli.test.js
L3/L3-P04/solution/tests/vitest/parse.test.js
L3/L3-P04/solution/tests/vitest/transform.test.js
L3/L3-P04/solution/vitest.config.ts
L3/L3-P04/starter/.gitignore
L3/L3-P04/starter/README.md
L3/L3-P04/starter/babel.config.cjs
L3/L3-P04/starter/bin/cli.js
L3/L3-P04/starter/data/sample.csv
L3/L3-P04/starter/data/sample.json
L3/L3-P04/starter/e2e/example.spec.ts
L3/L3-P04/starter/eslint.config.mjs
L3/L3-P04/starter/jest.config.cjs
L3/L3-P04/starter/package.json
L3/L3-P04/starter/playwright.config.ts
L3/L3-P04/starter/public/index.html
L3/L3-P04/starter/public/manifest.webmanifest
L3/L3-P04/starter/scripts/build-sw.mjs
L3/L3-P04/starter/server.mjs
L3/L3-P04/starter/src/cli-runner.js
L3/L3-P04/starter/src/lib/filters.js
L3/L3-P04/starter/src/lib/format.js
L3/L3-P04/starter/src/lib/parse.js
L3/L3-P04/starter/src/lib/transform.js
L3/L3-P04/starter/tests/jest/cli.jest.test.js
L3/L3-P04/starter/tests/jest/parse.jest.test.js
L3/L3-P04/starter/tests/jest/transform.jest.test.js
L3/L3-P04/starter/tests/vitest/cli.test.js
L3/L3-P04/starter/tests/vitest/parse.test.js
L3/L3-P04/starter/tests/vitest/transform.test.js
L3/L3-P04/starter/vitest.config.ts
L3/L3-P05/solution/.gitignore
L3/L3-P05/solution/README.md
L3/L3-P05/solution/babel.config.cjs
L3/L3-P05/solution/bin/cli.js
L3/L3-P05/solution/data/sample.csv
L3/L3-P05/solution/data/sample.json
L3/L3-P05/solution/e2e/example.spec.ts
L3/L3-P05/solution/eslint.config.mjs
L3/L3-P05/solution/jest.config.cjs
L3/L3-P05/solution/package.json
L3/L3-P05/solution/playwright.config.ts
L3/L3-P05/solution/public/index.html
L3/L3-P05/solution/public/manifest.webmanifest
L3/L3-P05/solution/scripts/build-sw.mjs
L3/L3-P05/solution/server.mjs
L3/L3-P05/solution/src/cli-runner.js
L3/L3-P05/solution/src/lib/filters.js
L3/L3-P05/solution/src/lib/format.js
L3/L3-P05/solution/src/lib/parse.js
L3/L3-P05/solution/src/lib/transform.js
L3/L3-P05/solution/tests/jest/cli.jest.test.js
L3/L3-P05/solution/tests/jest/parse.jest.test.js
L3/L3-P05/solution/tests/jest/transform.jest.test.js
L3/L3-P05/solution/tests/vitest/cli.test.js
L3/L3-P05/solution/tests/vitest/parse.test.js
L3/L3-P05/solution/tests/vitest/transform.test.js
L3/L3-P05/solution/vitest.config.ts
L3/L3-P05/starter/.gitignore
L3/L3-P05/starter/README.md
L3/L3-P05/starter/babel.config.cjs
L3/L3-P05/starter/bin/cli.js
L3/L3-P05/starter/data/sample.csv
L3/L3-P05/starter/data/sample.json
L3/L3-P05/starter/e2e/example.spec.ts
L3/L3-P05/starter/eslint.config.mjs
L3/L3-P05/starter/jest.config.cjs
L3/L3-P05/starter/package.json
L3/L3-P05/starter/playwright.config.ts
L3/L3-P05/starter/public/index.html
L3/L3-P05/starter/public/manifest.webmanifest
L3/L3-P05/starter/scripts/build-sw.mjs
L3/L3-P05/starter/server.mjs
L3/L3-P05/starter/src/cli-runner.js
L3/L3-P05/starter/src/lib/filters.js
L3/L3-P05/starter/src/lib/format.js
L3/L3-P05/starter/src/lib/parse.js
L3/L3-P05/starter/src/lib/transform.js
L3/L3-P05/starter/tests/jest/cli.jest.test.js
L3/L3-P05/starter/tests/jest/parse.jest.test.js
L3/L3-P05/starter/tests/jest/transform.jest.test.js
L3/L3-P05/starter/tests/vitest/cli.test.js
L3/L3-P05/starter/tests/vitest/parse.test.js
L3/L3-P05/starter/tests/vitest/transform.test.js
L3/L3-P05/starter/vitest.config.ts
L3/L3-P06/solution/.gitignore
L3/L3-P06/solution/README.md
L3/L3-P06/solution/babel.config.cjs
L3/L3-P06/solution/bin/cli.js
L3/L3-P06/solution/data/sample.csv
L3/L3-P06/solution/data/sample.json
L3/L3-P06/solution/e2e/example.spec.ts
L3/L3-P06/solution/eslint.config.mjs
L3/L3-P06/solution/jest.config.cjs
L3/L3-P06/solution/package.json
L3/L3-P06/solution/playwright.config.ts
L3/L3-P06/solution/public/index.html
L3/L3-P06/solution/public/manifest.webmanifest
L3/L3-P06/solution/scripts/build-sw.mjs
L3/L3-P06/solution/server.mjs
L3/L3-P06/solution/src/cli-runner.js
L3/L3-P06/solution/src/lib/filters.js
L3/L3-P06/solution/src/lib/format.js
L3/L3-P06/solution/src/lib/parse.js
L3/L3-P06/solution/src/lib/transform.js
L3/L3-P06/solution/tests/jest/cli.jest.test.js
L3/L3-P06/solution/tests/jest/parse.jest.test.js
L3/L3-P06/solution/tests/jest/transform.jest.test.js
L3/L3-P06/solution/tests/vitest/cli.test.js
L3/L3-P06/solution/tests/vitest/parse.test.js
L3/L3-P06/solution/tests/vitest/transform.test.js
L3/L3-P06/solution/vitest.config.ts
L3/L3-P06/starter/.gitignore
L3/L3-P06/starter/README.md
L3/L3-P06/starter/babel.config.cjs
L3/L3-P06/starter/bin/cli.js
L3/L3-P06/starter/data/sample.csv
L3/L3-P06/starter/data/sample.json
L3/L3-P06/starter/e2e/example.spec.ts
L3/L3-P06/starter/eslint.config.mjs
L3/L3-P06/starter/jest.config.cjs
L3/L3-P06/starter/package.json
L3/L3-P06/starter/playwright.config.ts
L3/L3-P06/starter/public/index.html
L3/L3-P06/starter/public/manifest.webmanifest
L3/L3-P06/starter/scripts/build-sw.mjs
L3/L3-P06/starter/server.mjs
L3/L3-P06/starter/src/cli-runner.js
L3/L3-P06/starter/src/lib/filters.js
L3/L3-P06/starter/src/lib/format.js
L3/L3-P06/starter/src/lib/parse.js
L3/L3-P06/starter/src/lib/transform.js
L3/L3-P06/starter/tests/jest/cli.jest.test.js
L3/L3-P06/starter/tests/jest/parse.jest.test.js
L3/L3-P06/starter/tests/jest/transform.jest.test.js
L3/L3-P06/starter/tests/vitest/cli.test.js
L3/L3-P06/starter/tests/vitest/parse.test.js
L3/L3-P06/starter/tests/vitest/transform.test.js
L3/L3-P06/starter/vitest.config.ts
L3/L3-P07/solution/.gitignore
L3/L3-P07/solution/README.md
L3/L3-P07/solution/babel.config.cjs
L3/L3-P07/solution/bin/cli.js
L3/L3-P07/solution/data/sample.csv
L3/L3-P07/solution/data/sample.json
L3/L3-P07/solution/e2e/example.spec.ts
L3/L3-P07/solution/eslint.config.mjs
L3/L3-P07/solution/jest.config.cjs
L3/L3-P07/solution/package.json
L3/L3-P07/solution/playwright.config.ts
L3/L3-P07/solution/public/index.html
L3/L3-P07/solution/public/manifest.webmanifest
L3/L3-P07/solution/scripts/build-sw.mjs
L3/L3-P07/solution/server.mjs
L3/L3-P07/solution/src/cli-runner.js
L3/L3-P07/solution/src/lib/filters.js
L3/L3-P07/solution/src/lib/format.js
L3/L3-P07/solution/src/lib/parse.js
L3/L3-P07/solution/src/lib/transform.js
L3/L3-P07/solution/tests/jest/cli.jest.test.js
L3/L3-P07/solution/tests/jest/parse.jest.test.js
L3/L3-P07/solution/tests/jest/transform.jest.test.js
L3/L3-P07/solution/tests/vitest/cli.test.js
L3/L3-P07/solution/tests/vitest/parse.test.js
L3/L3-P07/solution/tests/vitest/transform.test.js
L3/L3-P07/solution/vitest.config.ts
L3/L3-P07/starter/.gitignore
L3/L3-P07/starter/README.md
L3/L3-P07/starter/babel.config.cjs
L3/L3-P07/starter/bin/cli.js
L3/L3-P07/starter/data/sample.csv
L3/L3-P07/starter/data/sample.json
L3/L3-P07/starter/e2e/example.spec.ts
L3/L3-P07/starter/eslint.config.mjs
L3/L3-P07/starter/jest.config.cjs
L3/L3-P07/starter/package.json
L3/L3-P07/starter/playwright.config.ts
L3/L3-P07/starter/public/index.html
L3/L3-P07/starter/public/manifest.webmanifest
L3/L3-P07/starter/scripts/build-sw.mjs
L3/L3-P07/starter/server.mjs
L3/L3-P07/starter/src/cli-runner.js
L3/L3-P07/starter/src/lib/filters.js
L3/L3-P07/starter/src/lib/format.js
L3/L3-P07/starter/src/lib/parse.js
L3/L3-P07/starter/src/lib/transform.js
L3/L3-P07/starter/tests/jest/cli.jest.test.js
L3/L3-P07/starter/tests/jest/parse.jest.test.js
L3/L3-P07/starter/tests/jest/transform.jest.test.js
L3/L3-P07/starter/tests/vitest/cli.test.js
L3/L3-P07/starter/tests/vitest/parse.test.js
L3/L3-P07/starter/tests/vitest/transform.test.js
L3/L3-P07/starter/vitest.config.ts
L3/L3-P08/solution/.gitignore
L3/L3-P08/solution/README.md
L3/L3-P08/solution/babel.config.cjs
L3/L3-P08/solution/bin/cli.js
L3/L3-P08/solution/data/sample.csv
L3/L3-P08/solution/data/sample.json
L3/L3-P08/solution/e2e/example.spec.ts
L3/L3-P08/solution/eslint.config.mjs
L3/L3-P08/solution/jest.config.cjs
L3/L3-P08/solution/package.json
L3/L3-P08/solution/playwright.config.ts
L3/L3-P08/solution/public/index.html
L3/L3-P08/solution/public/manifest.webmanifest
L3/L3-P08/solution/scripts/build-sw.mjs
L3/L3-P08/solution/server.mjs
L3/L3-P08/solution/src/cli-runner.js
L3/L3-P08/solution/src/lib/filters.js
L3/L3-P08/solution/src/lib/format.js
L3/L3-P08/solution/src/lib/parse.js
L3/L3-P08/solution/src/lib/transform.js
L3/L3-P08/solution/tests/jest/cli.jest.test.js
L3/L3-P08/solution/tests/jest/parse.jest.test.js
L3/L3-P08/solution/tests/jest/transform.jest.test.js
L3/L3-P08/solution/tests/vitest/cli.test.js
L3/L3-P08/solution/tests/vitest/parse.test.js
L3/L3-P08/solution/tests/vitest/transform.test.js
L3/L3-P08/solution/vitest.config.ts
L3/L3-P08/starter/.gitignore
L3/L3-P08/starter/README.md
L3/L3-P08/starter/babel.config.cjs
L3/L3-P08/starter/bin/cli.js
L3/L3-P08/starter/data/sample.csv
L3/L3-P08/starter/data/sample.json
L3/L3-P08/starter/e2e/example.spec.ts
L3/L3-P08/starter/eslint.config.mjs
L3/L3-P08/starter/jest.config.cjs
L3/L3-P08/starter/package.json
L3/L3-P08/starter/playwright.config.ts
L3/L3-P08/starter/public/index.html
L3/L3-P08/starter/public/manifest.webmanifest
L3/L3-P08/starter/scripts/build-sw.mjs
L3/L3-P08/starter/server.mjs
L3/L3-P08/starter/src/cli-runner.js
L3/L3-P08/starter/src/lib/filters.js
L3/L3-P08/starter/src/lib/format.js
L3/L3-P08/starter/src/lib/parse.js
L3/L3-P08/starter/src/lib/transform.js
L3/L3-P08/starter/tests/jest/cli.jest.test.js
L3/L3-P08/starter/tests/jest/parse.jest.test.js
L3/L3-P08/starter/tests/jest/transform.jest.test.js
L3/L3-P08/starter/tests/vitest/cli.test.js
L3/L3-P08/starter/tests/vitest/parse.test.js
L3/L3-P08/starter/tests/vitest/transform.test.js
L3/L3-P08/starter/vitest.config.ts
L3/L3-P09/solution/.gitignore
L3/L3-P09/solution/README.md
L3/L3-P09/solution/babel.config.cjs
L3/L3-P09/solution/bin/cli.js
L3/L3-P09/solution/data/sample.csv
L3/L3-P09/solution/data/sample.json
L3/L3-P09/solution/e2e/example.spec.ts
L3/L3-P09/solution/eslint.config.mjs
L3/L3-P09/solution/jest.config.cjs
L3/L3-P09/solution/package.json
L3/L3-P09/solution/playwright.config.ts
L3/L3-P09/solution/public/index.html
L3/L3-P09/solution/public/manifest.webmanifest
L3/L3-P09/solution/scripts/build-sw.mjs
L3/L3-P09/solution/server.mjs
L3/L3-P09/solution/src/cli-runner.js
L3/L3-P09/solution/src/lib/filters.js
L3/L3-P09/solution/src/lib/format.js
L3/L3-P09/solution/src/lib/parse.js
L3/L3-P09/solution/src/lib/transform.js
L3/L3-P09/solution/tests/jest/cli.jest.test.js
L3/L3-P09/solution/tests/jest/parse.jest.test.js
L3/L3-P09/solution/tests/jest/transform.jest.test.js
L3/L3-P09/solution/tests/vitest/cli.test.js
L3/L3-P09/solution/tests/vitest/parse.test.js
L3/L3-P09/solution/tests/vitest/transform.test.js
L3/L3-P09/solution/vitest.config.ts
L3/L3-P09/starter/.gitignore
L3/L3-P09/starter/README.md
L3/L3-P09/starter/babel.config.cjs
L3/L3-P09/starter/bin/cli.js
L3/L3-P09/starter/data/sample.csv
L3/L3-P09/starter/data/sample.json
L3/L3-P09/starter/e2e/example.spec.ts
L3/L3-P09/starter/eslint.config.mjs
L3/L3-P09/starter/jest.config.cjs
L3/L3-P09/starter/package.json
L3/L3-P09/starter/playwright.config.ts
L3/L3-P09/starter/public/index.html
L3/L3-P09/starter/public/manifest.webmanifest
L3/L3-P09/starter/scripts/build-sw.mjs
L3/L3-P09/starter/server.mjs
L3/L3-P09/starter/src/cli-runner.js
L3/L3-P09/starter/src/lib/filters.js
L3/L3-P09/starter/src/lib/format.js
L3/L3-P09/starter/src/lib/parse.js
L3/L3-P09/starter/src/lib/transform.js
L3/L3-P09/starter/tests/jest/cli.jest.test.js
L3/L3-P09/starter/tests/jest/parse.jest.test.js
L3/L3-P09/starter/tests/jest/transform.jest.test.js
L3/L3-P09/starter/tests/vitest/cli.test.js
L3/L3-P09/starter/tests/vitest/parse.test.js
L3/L3-P09/starter/tests/vitest/transform.test.js
L3/L3-P09/starter/vitest.config.ts
L3/L3-P10/solution/.gitignore
L3/L3-P10/solution/README.md
L3/L3-P10/solution/babel.config.cjs
L3/L3-P10/solution/bin/cli.js
L3/L3-P10/solution/data/sample.csv
L3/L3-P10/solution/data/sample.json
L3/L3-P10/solution/e2e/example.spec.ts
L3/L3-P10/solution/eslint.config.mjs
L3/L3-P10/solution/jest.config.cjs
L3/L3-P10/solution/package.json
L3/L3-P10/solution/playwright.config.ts
L3/L3-P10/solution/public/index.html
L3/L3-P10/solution/public/manifest.webmanifest
L3/L3-P10/solution/scripts/build-sw.mjs
L3/L3-P10/solution/server.mjs
L3/L3-P10/solution/src/cli-runner.js
L3/L3-P10/solution/src/lib/filters.js
L3/L3-P10/solution/src/lib/format.js
L3/L3-P10/solution/src/lib/parse.js
L3/L3-P10/solution/src/lib/transform.js
L3/L3-P10/solution/tests/jest/cli.jest.test.js
L3/L3-P10/solution/tests/jest/parse.jest.test.js
L3/L3-P10/solution/tests/jest/transform.jest.test.js
L3/L3-P10/solution/tests/vitest/cli.test.js
L3/L3-P10/solution/tests/vitest/parse.test.js
L3/L3-P10/solution/tests/vitest/transform.test.js
L3/L3-P10/solution/vitest.config.ts
L3/L3-P10/starter/.gitignore
L3/L3-P10/starter/README.md
L3/L3-P10/starter/babel.config.cjs
L3/L3-P10/starter/bin/cli.js
L3/L3-P10/starter/data/sample.csv
L3/L3-P10/starter/data/sample.json
L3/L3-P10/starter/e2e/example.spec.ts
L3/L3-P10/starter/eslint.config.mjs
L3/L3-P10/starter/jest.config.cjs
L3/L3-P10/starter/package.json
L3/L3-P10/starter/playwright.config.ts
L3/L3-P10/starter/public/index.html
L3/L3-P10/starter/public/manifest.webmanifest
L3/L3-P10/starter/scripts/build-sw.mjs
L3/L3-P10/starter/server.mjs
L3/L3-P10/starter/src/cli-runner.js
L3/L3-P10/starter/src/lib/filters.js
L3/L3-P10/starter/src/lib/format.js
L3/L3-P10/starter/src/lib/parse.js
L3/L3-P10/starter/src/lib/transform.js
L3/L3-P10/starter/tests/jest/cli.jest.test.js
L3/L3-P10/starter/tests/jest/parse.jest.test.js
L3/L3-P10/starter/tests/jest/transform.jest.test.js
L3/L3-P10/starter/tests/vitest/cli.test.js
L3/L3-P10/starter/tests/vitest/parse.test.js
L3/L3-P10/starter/tests/vitest/transform.test.js
L3/L3-P10/starter/vitest.config.ts
L3/L3-P11/solution/.gitignore
L3/L3-P11/solution/README.md
L3/L3-P11/solution/babel.config.cjs
L3/L3-P11/solution/bin/cli.js
L3/L3-P11/solution/data/sample.csv
L3/L3-P11/solution/data/sample.json
L3/L3-P11/solution/e2e/example.spec.ts
L3/L3-P11/solution/eslint.config.mjs
L3/L3-P11/solution/jest.config.cjs
L3/L3-P11/solution/package.json
L3/L3-P11/solution/playwright.config.ts
L3/L3-P11/solution/public/index.html
L3/L3-P11/solution/public/manifest.webmanifest
L3/L3-P11/solution/scripts/build-sw.mjs
L3/L3-P11/solution/server.mjs
L3/L3-P11/solution/src/cli-runner.js
L3/L3-P11/solution/src/lib/filters.js
L3/L3-P11/solution/src/lib/format.js
L3/L3-P11/solution/src/lib/parse.js
L3/L3-P11/solution/src/lib/transform.js
L3/L3-P11/solution/tests/jest/cli.jest.test.js
L3/L3-P11/solution/tests/jest/parse.jest.test.js
L3/L3-P11/solution/tests/jest/transform.jest.test.js
L3/L3-P11/solution/tests/vitest/cli.test.js
L3/L3-P11/solution/tests/vitest/parse.test.js
L3/L3-P11/solution/tests/vitest/transform.test.js
L3/L3-P11/solution/vitest.config.ts
L3/L3-P11/starter/.gitignore
L3/L3-P11/starter/README.md
L3/L3-P11/starter/babel.config.cjs
L3/L3-P11/starter/bin/cli.js
L3/L3-P11/starter/data/sample.csv
L3/L3-P11/starter/data/sample.json
L3/L3-P11/starter/e2e/example.spec.ts
L3/L3-P11/starter/eslint.config.mjs
L3/L3-P11/starter/jest.config.cjs
L3/L3-P11/starter/package.json
L3/L3-P11/starter/playwright.config.ts
L3/L3-P11/starter/public/index.html
L3/L3-P11/starter/public/manifest.webmanifest
L3/L3-P11/starter/scripts/build-sw.mjs
L3/L3-P11/starter/server.mjs
L3/L3-P11/starter/src/cli-runner.js
L3/L3-P11/starter/src/lib/filters.js
L3/L3-P11/starter/src/lib/format.js
L3/L3-P11/starter/src/lib/parse.js
L3/L3-P11/starter/src/lib/transform.js
L3/L3-P11/starter/tests/jest/cli.jest.test.js
L3/L3-P11/starter/tests/jest/parse.jest.test.js
L3/L3-P11/starter/tests/jest/transform.jest.test.js
L3/L3-P11/starter/tests/vitest/cli.test.js
L3/L3-P11/starter/tests/vitest/parse.test.js
L3/L3-P11/starter/tests/vitest/transform.test.js
L3/L3-P11/starter/vitest.config.ts
L3/L3-P12/solution/.gitignore
L3/L3-P12/solution/README.md
L3/L3-P12/solution/babel.config.cjs
L3/L3-P12/solution/bin/cli.js
L3/L3-P12/solution/data/sample.csv
L3/L3-P12/solution/data/sample.json
L3/L3-P12/solution/e2e/example.spec.ts
L3/L3-P12/solution/eslint.config.mjs
L3/L3-P12/solution/jest.config.cjs
L3/L3-P12/solution/package.json
L3/L3-P12/solution/playwright.config.ts
L3/L3-P12/solution/public/index.html
L3/L3-P12/solution/public/manifest.webmanifest
L3/L3-P12/solution/scripts/build-sw.mjs
L3/L3-P12/solution/server.mjs
L3/L3-P12/solution/src/cli-runner.js
L3/L3-P12/solution/src/lib/filters.js
L3/L3-P12/solution/src/lib/format.js
L3/L3-P12/solution/src/lib/parse.js
L3/L3-P12/solution/src/lib/transform.js
L3/L3-P12/solution/tests/jest/cli.jest.test.js
L3/L3-P12/solution/tests/jest/parse.jest.test.js
L3/L3-P12/solution/tests/jest/transform.jest.test.js
L3/L3-P12/solution/tests/vitest/cli.test.js
L3/L3-P12/solution/tests/vitest/parse.test.js
L3/L3-P12/solution/tests/vitest/transform.test.js
L3/L3-P12/solution/vitest.config.ts
L3/L3-P12/starter/.gitignore
L3/L3-P12/starter/README.md
L3/L3-P12/starter/babel.config.cjs
L3/L3-P12/starter/bin/cli.js
L3/L3-P12/starter/data/sample.csv
L3/L3-P12/starter/data/sample.json
L3/L3-P12/starter/e2e/example.spec.ts
L3/L3-P12/starter/eslint.config.mjs
L3/L3-P12/starter/jest.config.cjs
L3/L3-P12/starter/package.json
L3/L3-P12/starter/playwright.config.ts
L3/L3-P12/starter/public/index.html
L3/L3-P12/starter/public/manifest.webmanifest
L3/L3-P12/starter/scripts/build-sw.mjs
L3/L3-P12/starter/server.mjs
L3/L3-P12/starter/src/cli-runner.js
L3/L3-P12/starter/src/lib/filters.js
L3/L3-P12/starter/src/lib/format.js
L3/L3-P12/starter/src/lib/parse.js
L3/L3-P12/starter/src/lib/transform.js
L3/L3-P12/starter/tests/jest/cli.jest.test.js
L3/L3-P12/starter/tests/jest/parse.jest.test.js
L3/L3-P12/starter/tests/jest/transform.jest.test.js
L3/L3-P12/starter/tests/vitest/cli.test.js
L3/L3-P12/starter/tests/vitest/parse.test.js
L3/L3-P12/starter/tests/vitest/transform.test.js
L3/L3-P12/starter/vitest.config.ts
L3/L3-P13/solution/.gitignore
L3/L3-P13/solution/README.md
L3/L3-P13/solution/babel.config.cjs
L3/L3-P13/solution/bin/cli.js
L3/L3-P13/solution/data/sample.csv
L3/L3-P13/solution/data/sample.json
L3/L3-P13/solution/e2e/example.spec.ts
L3/L3-P13/solution/eslint.config.mjs
L3/L3-P13/solution/jest.config.cjs
L3/L3-P13/solution/package.json
L3/L3-P13/solution/playwright.config.ts
L3/L3-P13/solution/public/index.html
L3/L3-P13/solution/public/manifest.webmanifest
L3/L3-P13/solution/scripts/build-sw.mjs
L3/L3-P13/solution/server.mjs
L3/L3-P13/solution/src/cli-runner.js
L3/L3-P13/solution/src/lib/filters.js
L3/L3-P13/solution/src/lib/format.js
L3/L3-P13/solution/src/lib/parse.js
L3/L3-P13/solution/src/lib/transform.js
L3/L3-P13/solution/tests/jest/cli.jest.test.js
L3/L3-P13/solution/tests/jest/parse.jest.test.js
L3/L3-P13/solution/tests/jest/transform.jest.test.js
L3/L3-P13/solution/tests/vitest/cli.test.js
L3/L3-P13/solution/tests/vitest/parse.test.js
L3/L3-P13/solution/tests/vitest/transform.test.js
L3/L3-P13/solution/vitest.config.ts
L3/L3-P13/starter/.gitignore
L3/L3-P13/starter/README.md
L3/L3-P13/starter/babel.config.cjs
L3/L3-P13/starter/bin/cli.js
L3/L3-P13/starter/data/sample.csv
L3/L3-P13/starter/data/sample.json
L3/L3-P13/starter/e2e/example.spec.ts
L3/L3-P13/starter/eslint.config.mjs
L3/L3-P13/starter/jest.config.cjs
L3/L3-P13/starter/package.json
L3/L3-P13/starter/playwright.config.ts
L3/L3-P13/starter/public/index.html
L3/L3-P13/starter/public/manifest.webmanifest
L3/L3-P13/starter/scripts/build-sw.mjs
L3/L3-P13/starter/server.mjs
L3/L3-P13/starter/src/cli-runner.js
L3/L3-P13/starter/src/lib/filters.js
L3/L3-P13/starter/src/lib/format.js
L3/L3-P13/starter/src/lib/parse.js
L3/L3-P13/starter/src/lib/transform.js
L3/L3-P13/starter/tests/jest/cli.jest.test.js
L3/L3-P13/starter/tests/jest/parse.jest.test.js
L3/L3-P13/starter/tests/jest/transform.jest.test.js
L3/L3-P13/starter/tests/vitest/cli.test.js
L3/L3-P13/starter/tests/vitest/parse.test.js
L3/L3-P13/starter/tests/vitest/transform.test.js
L3/L3-P13/starter/vitest.config.ts
L3/L3-P14/solution/.gitignore
L3/L3-P14/solution/README.md
L3/L3-P14/solution/babel.config.cjs
L3/L3-P14/solution/bin/cli.js
L3/L3-P14/solution/data/sample.csv
L3/L3-P14/solution/data/sample.json
L3/L3-P14/solution/e2e/example.spec.ts
L3/L3-P14/solution/eslint.config.mjs
L3/L3-P14/solution/jest.config.cjs
L3/L3-P14/solution/package.json
L3/L3-P14/solution/playwright.config.ts
L3/L3-P14/solution/public/index.html
L3/L3-P14/solution/public/manifest.webmanifest
L3/L3-P14/solution/scripts/build-sw.mjs
L3/L3-P14/solution/server.mjs
L3/L3-P14/solution/src/cli-runner.js
L3/L3-P14/solution/src/lib/filters.js
L3/L3-P14/solution/src/lib/format.js
L3/L3-P14/solution/src/lib/parse.js
L3/L3-P14/solution/src/lib/transform.js
L3/L3-P14/solution/tests/jest/cli.jest.test.js
L3/L3-P14/solution/tests/jest/parse.jest.test.js
L3/L3-P14/solution/tests/jest/transform.jest.test.js
L3/L3-P14/solution/tests/vitest/cli.test.js
L3/L3-P14/solution/tests/vitest/parse.test.js
L3/L3-P14/solution/tests/vitest/transform.test.js
L3/L3-P14/solution/vitest.config.ts
L3/L3-P14/starter/.gitignore
L3/L3-P14/starter/README.md
L3/L3-P14/starter/babel.config.cjs
L3/L3-P14/starter/bin/cli.js
L3/L3-P14/starter/data/sample.csv
L3/L3-P14/starter/data/sample.json
L3/L3-P14/starter/e2e/example.spec.ts
L3/L3-P14/starter/eslint.config.mjs
L3/L3-P14/starter/jest.config.cjs
L3/L3-P14/starter/package.json
L3/L3-P14/starter/playwright.config.ts
L3/L3-P14/starter/public/index.html
L3/L3-P14/starter/public/manifest.webmanifest
L3/L3-P14/starter/scripts/build-sw.mjs
L3/L3-P14/starter/server.mjs
L3/L3-P14/starter/src/cli-runner.js
L3/L3-P14/starter/src/lib/filters.js
L3/L3-P14/starter/src/lib/format.js
L3/L3-P14/starter/src/lib/parse.js
L3/L3-P14/starter/src/lib/transform.js
L3/L3-P14/starter/tests/jest/cli.jest.test.js
L3/L3-P14/starter/tests/jest/parse.jest.test.js
L3/L3-P14/starter/tests/jest/transform.jest.test.js
L3/L3-P14/starter/tests/vitest/cli.test.js
L3/L3-P14/starter/tests/vitest/parse.test.js
L3/L3-P14/starter/tests/vitest/transform.test.js
L3/L3-P14/starter/vitest.config.ts
L3/L3-P15/solution/.gitignore
L3/L3-P15/solution/README.md
L3/L3-P15/solution/babel.config.cjs
L3/L3-P15/solution/bin/cli.js
L3/L3-P15/solution/data/sample.csv
L3/L3-P15/solution/data/sample.json
L3/L3-P15/solution/e2e/example.spec.ts
L3/L3-P15/solution/eslint.config.mjs
L3/L3-P15/solution/jest.config.cjs
L3/L3-P15/solution/package.json
L3/L3-P15/solution/playwright.config.ts
L3/L3-P15/solution/public/index.html
L3/L3-P15/solution/public/manifest.webmanifest
L3/L3-P15/solution/scripts/build-sw.mjs
L3/L3-P15/solution/server.mjs
L3/L3-P15/solution/src/cli-runner.js
L3/L3-P15/solution/src/lib/filters.js
L3/L3-P15/solution/src/lib/format.js
L3/L3-P15/solution/src/lib/parse.js
L3/L3-P15/solution/src/lib/transform.js
L3/L3-P15/solution/tests/jest/cli.jest.test.js
L3/L3-P15/solution/tests/jest/parse.jest.test.js
L3/L3-P15/solution/tests/jest/transform.jest.test.js
L3/L3-P15/solution/tests/vitest/cli.test.js
L3/L3-P15/solution/tests/vitest/parse.test.js
L3/L3-P15/solution/tests/vitest/transform.test.js
L3/L3-P15/solution/vitest.config.ts
L3/L3-P15/starter/.gitignore
L3/L3-P15/starter/README.md
L3/L3-P15/starter/babel.config.cjs
L3/L3-P15/starter/bin/cli.js
L3/L3-P15/starter/data/sample.csv
L3/L3-P15/starter/data/sample.json
L3/L3-P15/starter/e2e/example.spec.ts
L3/L3-P15/starter/eslint.config.mjs
L3/L3-P15/starter/jest.config.cjs
L3/L3-P15/starter/package.json
L3/L3-P15/starter/playwright.config.ts
L3/L3-P15/starter/public/index.html
L3/L3-P15/starter/public/manifest.webmanifest
L3/L3-P15/starter/scripts/build-sw.mjs
L3/L3-P15/starter/server.mjs
L3/L3-P15/starter/src/cli-runner.js
L3/L3-P15/starter/src/lib/filters.js
L3/L3-P15/starter/src/lib/format.js
L3/L3-P15/starter/src/lib/parse.js
L3/L3-P15/starter/src/lib/transform.js
L3/L3-P15/starter/tests/jest/cli.jest.test.js
L3/L3-P15/starter/tests/jest/parse.jest.test.js
L3/L3-P15/starter/tests/jest/transform.jest.test.js
L3/L3-P15/starter/tests/vitest/cli.test.js
L3/L3-P15/starter/tests/vitest/parse.test.js
L3/L3-P15/starter/tests/vitest/transform.test.js
L3/L3-P15/starter/vitest.config.ts
```

**Variante detectate:** solution: 1035, starter: 1035.

**Categorii de fișiere:** config: 600, docs: 90, other: 360, code: 450, tests: 540, public: 30, ci: 5.

**package.json — sinteză: scripturi, workspaces, bin, dependențe (eșantion)**

- `L1/L1-P01/starter/package.json`: name=`l1-p01-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P01/solution/package.json`: name=`l1-p01-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P02/starter/package.json`: name=`l1-p02-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P02/solution/package.json`: name=`l1-p02-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P03/starter/package.json`: name=`l1-p03-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P03/solution/package.json`: name=`l1-p03-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P04/starter/package.json`: name=`l1-p04-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P04/solution/package.json`: name=`l1-p04-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P05/starter/package.json`: name=`l1-p05-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P05/solution/package.json`: name=`l1-p05-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P06/starter/package.json`: name=`l1-p06-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P06/solution/package.json`: name=`l1-p06-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P07/starter/package.json`: name=`l1-p07-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P07/solution/package.json`: name=`l1-p07-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P08/starter/package.json`: name=`l1-p08-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P08/solution/package.json`: name=`l1-p08-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P09/starter/package.json`: name=`l1-p09-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P09/solution/package.json`: name=`l1-p09-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P10/starter/package.json`: name=`l1-p10-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P10/solution/package.json`: name=`l1-p10-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P11/starter/package.json`: name=`l1-p11-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P11/solution/package.json`: name=`l1-p11-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P12/starter/package.json`: name=`l1-p12-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P12/solution/package.json`: name=`l1-p12-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P13/starter/package.json`: name=`l1-p13-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P13/solution/package.json`: name=`l1-p13-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P14/starter/package.json`: name=`l1-p14-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P14/solution/package.json`: name=`l1-p14-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P15/starter/package.json`: name=`l1-p15-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L1/L1-P15/solution/package.json`: name=`l1-p15-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P01/starter/package.json`: name=`l2-p01-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P01/solution/package.json`: name=`l2-p01-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P02/starter/package.json`: name=`l2-p02-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P02/solution/package.json`: name=`l2-p02-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P03/starter/package.json`: name=`l2-p03-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P03/solution/package.json`: name=`l2-p03-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P04/starter/package.json`: name=`l2-p04-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P04/solution/package.json`: name=`l2-p04-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P05/starter/package.json`: name=`l2-p05-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P05/solution/package.json`: name=`l2-p05-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P06/starter/package.json`: name=`l2-p06-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P06/solution/package.json`: name=`l2-p06-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P07/starter/package.json`: name=`l2-p07-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P07/solution/package.json`: name=`l2-p07-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P08/starter/package.json`: name=`l2-p08-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P08/solution/package.json`: name=`l2-p08-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P09/starter/package.json`: name=`l2-p09-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P09/solution/package.json`: name=`l2-p09-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P10/starter/package.json`: name=`l2-p10-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P10/solution/package.json`: name=`l2-p10-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P11/starter/package.json`: name=`l2-p11-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P11/solution/package.json`: name=`l2-p11-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P12/starter/package.json`: name=`l2-p12-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P12/solution/package.json`: name=`l2-p12-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P13/starter/package.json`: name=`l2-p13-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P13/solution/package.json`: name=`l2-p13-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P14/starter/package.json`: name=`l2-p14-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P14/solution/package.json`: name=`l2-p14-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P15/starter/package.json`: name=`l2-p15-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L2/L2-P15/solution/package.json`: name=`l2-p15-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js
- `L3/L3-P01/starter/package.json`: name=`l3-p01-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P01/solution/package.json`: name=`l3-p01-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P02/starter/package.json`: name=`l3-p02-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P02/solution/package.json`: name=`l3-p02-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P03/starter/package.json`: name=`l3-p03-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P03/solution/package.json`: name=`l3-p03-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P04/starter/package.json`: name=`l3-p04-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P04/solution/package.json`: name=`l3-p04-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P05/starter/package.json`: name=`l3-p05-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P05/solution/package.json`: name=`l3-p05-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P06/starter/package.json`: name=`l3-p06-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P06/solution/package.json`: name=`l3-p06-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P07/starter/package.json`: name=`l3-p07-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P07/solution/package.json`: name=`l3-p07-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P08/starter/package.json`: name=`l3-p08-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P08/solution/package.json`: name=`l3-p08-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P09/starter/package.json`: name=`l3-p09-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P09/solution/package.json`: name=`l3-p09-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P10/starter/package.json`: name=`l3-p10-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P10/solution/package.json`: name=`l3-p10-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P11/starter/package.json`: name=`l3-p11-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P11/solution/package.json`: name=`l3-p11-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P12/starter/package.json`: name=`l3-p12-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P12/solution/package.json`: name=`l3-p12-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P13/starter/package.json`: name=`l3-p13-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P13/solution/package.json`: name=`l3-p13-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P14/starter/package.json`: name=`l3-p14-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P14/solution/package.json`: name=`l3-p14-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P15/starter/package.json`: name=`l3-p15-starter` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build
- `L3/L3-P15/solution/package.json`: name=`l3-p15-solution` type=`module` workspaces=False bin=True
  - **Scripturi:**
  - `dev` → `node bin/cli.js data/sample.csv --limit 5 --format table`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `lint` → `eslint . --ext js,mjs`
  - `e2e` → `playwright test`
  - `pw:install` → `playwright install --with-deps`
  - `build:sw` → `node scripts/build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, eslint, @eslint/js, @playwright/test, workbox-build

### Seminar1_Partea3_p3-READMEs.zip

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

**Categorii de fișiere:** docs: 90.

## 2. Sinteza documentelor DOCX (teorie ↔ laborator ↔ proiecte)

### Seminar1_Partea1_Teorie.docx

**Titluri/Heading‑uri (eșantion):**

- Seminarul 1 — Introducere în JavaScript: sintaxă modernă, funcții, iterație, CLI
(Partea 1 — Teorie, narativă, hook realist, exemple și subcapitole)
- **Hook realist: „Raport în 45 de minute”**

### Seminar1_Partea2_Laborator.docx

**Titluri/Heading‑uri (eșantion):**

- Seminarul 1 — Partea 2 (Laborator extins)
- Această **Partea 2 — Laborator** transformă conceptele din Partea 1 (sintaxă modernă, funcții, iterație, CLI) într‑un exercițiu cap‑la‑cap pe aceeași temă: generarea rapidă a unui **raport „StudentHub”** din date CSV/JSON. Structura e **progresivă**: începem cu micro‑exerciții pe funcții pure, continuăm cu integrarea într‑un **pipeline** map/filter/reduce, apoi ambalăm logica într‑un **CLI** testabil care produce rezultate în **format tabelar** sau **JSON**. Toate etapele vin cu **worksheet (cerință + checklist)**, **starter code**, și **teste** (Vitest & Jest în oglindă).
- ────────────────────────────────────────────────────────────────────────

### Seminar1_Partea2_Worksheet_Ghid.docx

**Titluri/Heading‑uri (eșantion):**

- Seminarul 1 — Partea 2 (Ghid arhivă + Worksheet)
- # Ghid de utilizare a arhivei „s1p2-lab.zip” & Worksheet detaliat
- ## 1. Ce conține arhiva
- `src/lib/*` — funcțiile pure ale laboratorului (parsare, transformare, filtrare, formatare).
- `src/cli-runner.js` — orchestrator CLI cu I/O injectabil pentru teste.
- `bin/cli.js` — intrarea CLI (se poate „linka” ca bin).
- `data/*` — fișiere exemplu.
- `tests/vitest/*` și `tests/jest/*` — suite paralele cu aceleași contracte.
- Config: `eslint.config.mjs`, `vitest.config.ts`, `jest.config.cjs`, `babel.config.cjs`, `.gitignore`.

### Seminar1_Partea3_Arhive_Ghid.docx

**Titluri/Heading‑uri (eșantion):**

- Ghid — Arhive (Seminarul 1, Partea 3)
- **Livrabile:** `s1p3-standalone.zip`, `s1p3-monorepo.zip`, `s1p3-readmes.zip`. Prima conține toate proiectele (starter+solution) cu workflows CI; a doua — doar starter-ele în PNPM workspaces; a treia — toate README-urile.
- **Rulare rapidă — standalone**

### Seminar1_Partea3_Proiecte_extins.docx

**Titluri/Heading‑uri (eșantion):**

- Seminarul 1 — Partea 3 (Proiecte/teme extinse)
- Această **Partea 3** propune **45 de proiecte** (15×L1, 15×L2, 15×L3) pe tema „Introducere în JavaScript — sintaxă modernă, funcții, iterație, CLI”. Fiecare proiect are o **specificație** (cerințe măsurabile) și o **soluție** (implementare‑etalon). În arhivele livrate, fiecare proiect are două variante: `starter/` (schelet + teste care pică) și `solution/` (implementare care trece toate testele). Pentru L3 am adăugat **Playwright e2e** și **Workbox PWA** pentru o mică interfață web statică de vizualizare a raportului.

**Metodă recomandată de lucru** (în toate proiectele):
1. Rulează `npm test` în `starter/` — observă testele care eșuează (definesc **contractul**).
2. Completează `src/lib/*` și `src/cli-runner.js` până când testele devin verzi.
3. Compară cu `solution/` și notează diferențele (decizii de design, edge‑cases).
4. Folosește **AI‑assist** (Copilot sub VSL / ChatGPT/Mistral/Claude) pentru a genera draft‑uri, dar **verifică** cu testele.

**Arborele** și **workflows** (lint/unit/e2e/workbox) sunt precablate atât în varianta **standalone**, cât și în **monorepo (PNPM)**.
- # L1 — Fundamental (15 proiecte)

## 3. Monorepo vs. standalone — analiză comparativă


**Manageri de pachete & workspaces.** Variantele monorepo folosesc `pnpm-workspace.yaml` și/sau `workspaces` în `package.json` pentru orchestrare; standalone izolează dependențele pe proiect.

**Comenzi de instalare/testare.** Monorepo: `pnpm i -w`, `pnpm --filter <pkg> run test` (sau `-w run test` pentru toate). Standalone: `npm i`, `npm test`. Suitele de teste sunt **oglindite** (Vitest & Jest), verificând aceleași **contracte** de funcții/CLI. 

**Integrare CI.** Monorepo agregă workflows (lint, unit Jest/Vitest, e2e & Workbox doar pentru L3), în timp ce standalone le definește per proiect.

**Avantaje/Dezavantaje.** Standalone — simplitate cognitivă (ideal începători). Monorepo — scalabil pentru seturi mari de proiecte (ex. 45 L1–L3), cu partajarea config‑urilor și execuții rapide în CI; costul este înțelegerea filtrării PNPM și a grafului de pachete.
## 4. Rolul fișierelor cheie (config, cod, teste, extra)

| Fișier / tip | Rol |
|---|---|
| `package.json` | Manifest proiect: metadate, dependențe, scripturi; poate expune `bin` pentru CLI. |
| `eslint.config.mjs` | Flat config ESLint; reguli minime pentru stil & erori comune. |
| `vitest.config.ts` | Configurare Vitest (environment `node`/`jsdom`, reporters, include). |
| `jest.config.cjs` | Configurare Jest (transform cu `babel-jest`, `extensionsToTreatAsEsm` la nevoie). |
| `babel.config.cjs` | Preseturi pentru Jest (`@babel/preset-env`). |
| `pnpm-workspace.yaml` | Workspace PNPM pentru monorepo; filtrează pachetele. |
| `src/lib/parse.js` | Funcții **pure** de parsare CSV/JSON (fără I/O). |
| `src/lib/transform.js` | Agregări pure: `groupBy`, `countBy`, `topK`. |
| `src/lib/filters.js` | Predicates: `filterNewMembers`, `byFaculty`. |
| `src/lib/format.js` | Formatări: tabel text și JSON serializat. |
| `src/cli-runner.js` | Orchestrator `run(argv, io)`; returnează cod de ieșire. |
| `bin/cli.js` | Intrare CLI; parsează `process.argv` și invocă runner‑ul. |

## 5. Corelații cod ↔ configurări ↔ teste


- **Funcțiile pure** din `src/lib/*` sunt testate în **ambele suite** (Vitest & Jest) pe **aceleași contracte** (parsare, agregări, filtrări, formatare).  
- **Runnerul CLI** (`src/cli-runner.js`) oferă I/O injectabil (`readFile`, `writeOut`, `writeErr`) pentru teste deterministe; `bin/cli.js` e doar un strat subțire.  
- **`.env.example`** (dacă este prezent) documentează variabilele folosite implicit de runner (ex.: `REPORT_LIMIT`); legat de opțiunile CLI.  
- **ESLint + CI**: workflows execută `lint` și `test` (Vitest & Jest) pe toate proiectele; în L3, se adaugă **Playwright** (e2e) și **Workbox** (PWA).  
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S1 pune bazele **JavaScript modern** (ESM, funcții, iterație declarativă) și demonstrează valoarea **programării funcționale** în prelucrarea de date, culminând cu un **utilitar CLI** care generează un raport „StudentHub”. Conținutul teoretic este mapat explicit pe laboratorul Partea 2 și pe proiectele Partea 3 (standalone & monorepo). fileciteturn9file0### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; rădăcină + `packages/*` |
| Instalare | `npm i` | `pnpm i -w` |
| Testare | `npm test` (Vitest & Jest) | `pnpm -w run test` sau `--filter` |
| CI | Workflows simple per proiect | Workflows agregate; matrice pe pachete |
| Scalare (45 proiecte) | multiplicare directoare | `packages/*` curate și refolosibile |
| Public țintă | începători | colecții/programe avansate |
### Inventar pe arhivă (roluri)

- **Seminar1_Partea2_p2-lab.zip** — config=6, docs=1, other=3, code=5, tests=6.
- **Seminar1_Partea3_p3-monorepo.zip** — config=302, docs=45, other=180, code=225, tests=270, public=15, ci=3.
- **Seminar1_Partea3_p3-standalone.zip** — config=600, docs=90, other=360, code=450, tests=540, public=30, ci=5.
- **Seminar1_Partea3_p3-READMEs.zip** — docs=90.
### Explicații fișier‑cu‑fișier

Consultați tabelul din §4. Maparea exactă a funcțiilor (`parse/transform/filters/format`) și a runner‑ului CLI pe cerința StudentHub este prezentată în **Laborator** și în **Ghidul arhivei** (Worksheet). fileciteturn9file1 fileciteturn9file2
### Corelații între fișiere


- `src/lib/parse.js` ↔ teste: conversii explicite, tratarea `interests` și `is_new`. fileciteturn9file1  
- `src/lib/transform.js` ↔ teste: `countBy`, `groupBy`, `topK` (K parametrizat). fileciteturn9file1  
- `src/lib/filters.js` ↔ teste: `filterNewMembers(refDate)` și `byFaculty(name)`. fileciteturn9file1  
- `src/cli-runner.js`/`bin/cli.js` ↔ teste: usage, coduri de ieșire, formate `table|json`. fileciteturn9file1 fileciteturn9file2  
- `.github/workflows/*` (în Partea 3) ↔ execuții lint/unit/e2e/workbox pe proiectele L1–L3. fileciteturn9file3  
### Recomandări pentru studenți


1) **Separă logica de I/O**: funcții pure în `src/lib/*`; runner/CLI doar „la margine”. fileciteturn9file1  
2) **Scrie testele o dată, rulează-le în două ecosisteme** (Vitest & Jest) — transfer de competență. fileciteturn9file1  
3) **Folosește conversii explicite** și `??` pentru valori lipsă; tratează `NaN` ca „contaminant”. fileciteturn9file0  
4) **Documentează usage** și codurile de ieșire (0/1); CLI bun = contract clar. fileciteturn9file1  
5) **Învață din `solution/`** după ce ai încercat singur; compară deciziile de design și edge‑cases. fileciteturn9file4  
### Instrucțiuni „Quick start” per arhivă


**Partea 2 — laborator (p2-lab.zip):**
```bash
unzip "Seminar1_Partea2_p2-lab.zip" -d s1p2-lab
cd s1p2-lab
npm i
npm test            # rulează Vitest & Jest (oglindă)
npm run dev         # raport tabelar pe data/sample.csv
node bin/cli.js data/sample.json --format json --limit 7
```
fileciteturn9file1 fileciteturn9file2

**Partea 3 — standalone (p3-standalone.zip):**
```bash
unzip "Seminar1_Partea3_p3-standalone.zip" -d s1p3-standalone
cd s1p3-standalone/L1/L1-P01/starter
npm i
npm test
npm run dev
```
fileciteturn9file3

**Partea 3 — monorepo (p3-monorepo.zip, PNPM):**
```bash
unzip "Seminar1_Partea3_p3-monorepo.zip" -d s1p3-monorepo
cd s1p3-monorepo
pnpm i -w
pnpm --filter l1-p01-starter run test
pnpm --filter l1-p01-starter run dev
```
fileciteturn9file3

**Partea 3 — README-uri agregate (p3-READMEs.zip):**
```bash
unzip "Seminar1_Partea3_p3-READMEs.zip" -d s1p3-readmes
ls s1p3-readmes | head -n 10
```
fileciteturn9file3
### Troubleshooting (erori frecvente)


- **ESM în Jest** → folosește `babel-jest` + `extensionsToTreatAsEsm`; vezi configurațiile din arhive. fileciteturn9file3  
- **CSV zgomotos** → normalizează separatoarele și newline‑urile; verifică antetul ca schemă. fileciteturn9file2  
- **Diferențe de output** (table vs. json) → separă strict `formatTable` de `toJSON`. fileciteturn9file1  
- **CI roșu pe e2e sau PWA** (doar L3) → rulează `npm run pw:install` și `npm run build:sw`. fileciteturn9file3  
- **Porturi ocupate** (în proiectele L3 cu server static) → schimbă `PORT` sau folosește un port liber. fileciteturn9file3  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** — limbaj JS modern, funcții/compoziție, iterație declarativă, CLI POSIX‑style; fixează vocabularul și contractele. fileciteturn9file0  
- **Partea 2 (Laborator + Worksheet)** — structură de proiect (lib/runner/bin), teste oglidă Vitest & Jest, opțiuni CLI; oferă checklist de acceptare. fileciteturn9file1 fileciteturn9file2  
- **Partea 3 (Ghid arhive + Proiecte)** — 45 proiecte L1–L3, variante starter/solution, CI, e2e, Workbox; recomandări de lucru și prompts AI. fileciteturn9file3 fileciteturn9file4  
### Prompt‑șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S1** (standalone & monorepo) un utilitar **Node/ESM** de raportare „StudentHub”: `src/lib/*` (funcții pure: parse/transform/filters/format), `src/cli-runner.js` (`run(argv, io)`), `bin/cli.js` (entry). Adaugă **teste oglidă** (Vitest & Jest), **README** cu Quick start & Troubleshooting, **CI** (lint/unit; e2e & Workbox doar la L3) și variante **starter**/**solution**. Contractele testelor definesc comportamentele așteptate (parsare, `topK`, filtrări, formate).”
