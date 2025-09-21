# Seminarul S12 — Tabele & Grafice (standalone & monorepo) — Analiză integrată a arhivelor și ghidurilor

*Generat la 2025-09-21 04:29.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar12_Partea2_p2-monorepo.zip

```
package.json
packages/lab/babel.config.cjs
packages/lab/docs/README.md
packages/lab/docs/WORKSHEET.md
packages/lab/index.html
packages/lab/jest.config.cjs
packages/lab/package.json
packages/lab/public/members.json
packages/lab/src/App.tsx
packages/lab/src/components/ChartPanel.tsx
packages/lab/src/components/DataTable.tsx
packages/lab/src/data/members.json
packages/lab/src/data/useMembersData.ts
packages/lab/src/main.tsx
packages/lab/src/selectors/analytics.ts
packages/lab/src/styles.css
packages/lab/tests/jest/chart.jest.test.tsx
packages/lab/tests/jest/selectors.jest.test.ts
packages/lab/tests/jest/table.jest.test.tsx
packages/lab/tests/setup.ts
packages/lab/tests/vitest/chart.test.tsx
packages/lab/tests/vitest/selectors.test.ts
packages/lab/tests/vitest/table.test.tsx
packages/lab/tsconfig.json
packages/lab/vite.config.ts
packages/lab/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 8, other: 1, code: 8, public: 1, tests: 7, docs: 2.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s12p2-monorepo` type=`module` workspaces=True
- `packages/lab/package.json`: name=`s12p2-tables-charts-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest

### Seminar12_Partea2_p2-standalone.zip

```
babel.config.cjs
docs/README.md
docs/WORKSHEET.md
index.html
jest.config.cjs
package.json
public/members.json
src/App.tsx
src/components/ChartPanel.tsx
src/components/DataTable.tsx
src/data/members.json
src/data/useMembersData.ts
src/main.tsx
src/selectors/analytics.ts
src/styles.css
tests/jest/chart.jest.test.tsx
tests/jest/selectors.jest.test.ts
tests/jest/table.jest.test.tsx
tests/setup.ts
tests/vitest/chart.test.tsx
tests/vitest/selectors.test.ts
tests/vitest/table.test.tsx
tsconfig.json
vite.config.ts
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 6, other: 1, code: 8, public: 1, tests: 7, docs: 2.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s12p2-tables-charts-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest

### Seminar12_Partea3_p3-monorepo.zip

```
package.json
packages/l1-p01-starter/README.md
packages/l1-p01-starter/babel.config.cjs
packages/l1-p01-starter/index.html
packages/l1-p01-starter/jest.config.cjs
packages/l1-p01-starter/package.json
packages/l1-p01-starter/src/App.tsx
packages/l1-p01-starter/src/components/ChartPanel.tsx
packages/l1-p01-starter/src/components/DataTable.tsx
packages/l1-p01-starter/src/data/members.json
packages/l1-p01-starter/src/lib/lib.ts
packages/l1-p01-starter/src/main.tsx
packages/l1-p01-starter/src/styles.css
packages/l1-p01-starter/tests/jest/spec.jest.test.ts
packages/l1-p01-starter/tests/setup.ts
packages/l1-p01-starter/tests/vitest/spec.test.ts
packages/l1-p01-starter/tsconfig.json
packages/l1-p01-starter/vite.config.ts
packages/l1-p01-starter/vitest.config.ts
packages/l1-p02-starter/README.md
packages/l1-p02-starter/babel.config.cjs
packages/l1-p02-starter/index.html
packages/l1-p02-starter/jest.config.cjs
packages/l1-p02-starter/package.json
packages/l1-p02-starter/src/App.tsx
packages/l1-p02-starter/src/components/ChartPanel.tsx
packages/l1-p02-starter/src/components/DataTable.tsx
packages/l1-p02-starter/src/data/members.json
packages/l1-p02-starter/src/lib/lib.ts
packages/l1-p02-starter/src/main.tsx
packages/l1-p02-starter/src/styles.css
packages/l1-p02-starter/tests/jest/spec.jest.test.ts
packages/l1-p02-starter/tests/setup.ts
packages/l1-p02-starter/tests/vitest/spec.test.ts
packages/l1-p02-starter/tsconfig.json
packages/l1-p02-starter/vite.config.ts
packages/l1-p02-starter/vitest.config.ts
packages/l1-p03-starter/README.md
packages/l1-p03-starter/babel.config.cjs
packages/l1-p03-starter/index.html
packages/l1-p03-starter/jest.config.cjs
packages/l1-p03-starter/package.json
packages/l1-p03-starter/src/App.tsx
packages/l1-p03-starter/src/components/ChartPanel.tsx
packages/l1-p03-starter/src/components/DataTable.tsx
packages/l1-p03-starter/src/data/members.json
packages/l1-p03-starter/src/lib/lib.ts
packages/l1-p03-starter/src/main.tsx
packages/l1-p03-starter/src/styles.css
packages/l1-p03-starter/tests/jest/spec.jest.test.ts
packages/l1-p03-starter/tests/setup.ts
packages/l1-p03-starter/tests/vitest/spec.test.ts
packages/l1-p03-starter/tsconfig.json
packages/l1-p03-starter/vite.config.ts
packages/l1-p03-starter/vitest.config.ts
packages/l1-p04-starter/README.md
packages/l1-p04-starter/babel.config.cjs
packages/l1-p04-starter/index.html
packages/l1-p04-starter/jest.config.cjs
packages/l1-p04-starter/package.json
packages/l1-p04-starter/src/App.tsx
packages/l1-p04-starter/src/components/ChartPanel.tsx
packages/l1-p04-starter/src/components/DataTable.tsx
packages/l1-p04-starter/src/data/members.json
packages/l1-p04-starter/src/lib/lib.ts
packages/l1-p04-starter/src/main.tsx
packages/l1-p04-starter/src/styles.css
packages/l1-p04-starter/tests/jest/spec.jest.test.ts
packages/l1-p04-starter/tests/setup.ts
packages/l1-p04-starter/tests/vitest/spec.test.ts
packages/l1-p04-starter/tsconfig.json
packages/l1-p04-starter/vite.config.ts
packages/l1-p04-starter/vitest.config.ts
packages/l1-p05-starter/README.md
packages/l1-p05-starter/babel.config.cjs
packages/l1-p05-starter/index.html
packages/l1-p05-starter/jest.config.cjs
packages/l1-p05-starter/package.json
packages/l1-p05-starter/src/App.tsx
packages/l1-p05-starter/src/components/ChartPanel.tsx
packages/l1-p05-starter/src/components/DataTable.tsx
packages/l1-p05-starter/src/data/members.json
packages/l1-p05-starter/src/lib/lib.ts
packages/l1-p05-starter/src/main.tsx
packages/l1-p05-starter/src/styles.css
packages/l1-p05-starter/tests/jest/spec.jest.test.ts
packages/l1-p05-starter/tests/setup.ts
packages/l1-p05-starter/tests/vitest/spec.test.ts
packages/l1-p05-starter/tsconfig.json
packages/l1-p05-starter/vite.config.ts
packages/l1-p05-starter/vitest.config.ts
packages/l1-p06-starter/README.md
packages/l1-p06-starter/babel.config.cjs
packages/l1-p06-starter/index.html
packages/l1-p06-starter/jest.config.cjs
packages/l1-p06-starter/package.json
packages/l1-p06-starter/src/App.tsx
packages/l1-p06-starter/src/components/ChartPanel.tsx
packages/l1-p06-starter/src/components/DataTable.tsx
packages/l1-p06-starter/src/data/members.json
packages/l1-p06-starter/src/lib/lib.ts
packages/l1-p06-starter/src/main.tsx
packages/l1-p06-starter/src/styles.css
packages/l1-p06-starter/tests/jest/spec.jest.test.ts
packages/l1-p06-starter/tests/setup.ts
packages/l1-p06-starter/tests/vitest/spec.test.ts
packages/l1-p06-starter/tsconfig.json
packages/l1-p06-starter/vite.config.ts
packages/l1-p06-starter/vitest.config.ts
packages/l1-p07-starter/README.md
packages/l1-p07-starter/babel.config.cjs
packages/l1-p07-starter/index.html
packages/l1-p07-starter/jest.config.cjs
packages/l1-p07-starter/package.json
packages/l1-p07-starter/src/App.tsx
packages/l1-p07-starter/src/components/ChartPanel.tsx
packages/l1-p07-starter/src/components/DataTable.tsx
packages/l1-p07-starter/src/data/members.json
packages/l1-p07-starter/src/lib/lib.ts
packages/l1-p07-starter/src/main.tsx
packages/l1-p07-starter/src/styles.css
packages/l1-p07-starter/tests/jest/spec.jest.test.ts
packages/l1-p07-starter/tests/setup.ts
packages/l1-p07-starter/tests/vitest/spec.test.ts
packages/l1-p07-starter/tsconfig.json
packages/l1-p07-starter/vite.config.ts
packages/l1-p07-starter/vitest.config.ts
packages/l1-p08-starter/README.md
packages/l1-p08-starter/babel.config.cjs
packages/l1-p08-starter/index.html
packages/l1-p08-starter/jest.config.cjs
packages/l1-p08-starter/package.json
packages/l1-p08-starter/src/App.tsx
packages/l1-p08-starter/src/components/ChartPanel.tsx
packages/l1-p08-starter/src/components/DataTable.tsx
packages/l1-p08-starter/src/data/members.json
packages/l1-p08-starter/src/lib/lib.ts
packages/l1-p08-starter/src/main.tsx
packages/l1-p08-starter/src/styles.css
packages/l1-p08-starter/tests/jest/spec.jest.test.ts
packages/l1-p08-starter/tests/setup.ts
packages/l1-p08-starter/tests/vitest/spec.test.ts
packages/l1-p08-starter/tsconfig.json
packages/l1-p08-starter/vite.config.ts
packages/l1-p08-starter/vitest.config.ts
packages/l1-p09-starter/README.md
packages/l1-p09-starter/babel.config.cjs
packages/l1-p09-starter/index.html
packages/l1-p09-starter/jest.config.cjs
packages/l1-p09-starter/package.json
packages/l1-p09-starter/src/App.tsx
packages/l1-p09-starter/src/components/ChartPanel.tsx
packages/l1-p09-starter/src/components/DataTable.tsx
packages/l1-p09-starter/src/data/members.json
packages/l1-p09-starter/src/lib/lib.ts
packages/l1-p09-starter/src/main.tsx
packages/l1-p09-starter/src/styles.css
packages/l1-p09-starter/tests/jest/spec.jest.test.ts
packages/l1-p09-starter/tests/setup.ts
packages/l1-p09-starter/tests/vitest/spec.test.ts
packages/l1-p09-starter/tsconfig.json
packages/l1-p09-starter/vite.config.ts
packages/l1-p09-starter/vitest.config.ts
packages/l1-p10-starter/README.md
packages/l1-p10-starter/babel.config.cjs
packages/l1-p10-starter/index.html
packages/l1-p10-starter/jest.config.cjs
packages/l1-p10-starter/package.json
packages/l1-p10-starter/src/App.tsx
packages/l1-p10-starter/src/components/ChartPanel.tsx
packages/l1-p10-starter/src/components/DataTable.tsx
packages/l1-p10-starter/src/data/members.json
packages/l1-p10-starter/src/lib/lib.ts
packages/l1-p10-starter/src/main.tsx
packages/l1-p10-starter/src/styles.css
packages/l1-p10-starter/tests/jest/spec.jest.test.ts
packages/l1-p10-starter/tests/setup.ts
packages/l1-p10-starter/tests/vitest/spec.test.ts
packages/l1-p10-starter/tsconfig.json
packages/l1-p10-starter/vite.config.ts
packages/l1-p10-starter/vitest.config.ts
packages/l1-p11-starter/README.md
packages/l1-p11-starter/babel.config.cjs
packages/l1-p11-starter/index.html
packages/l1-p11-starter/jest.config.cjs
packages/l1-p11-starter/package.json
packages/l1-p11-starter/src/App.tsx
packages/l1-p11-starter/src/components/ChartPanel.tsx
packages/l1-p11-starter/src/components/DataTable.tsx
packages/l1-p11-starter/src/data/members.json
packages/l1-p11-starter/src/lib/lib.ts
packages/l1-p11-starter/src/main.tsx
packages/l1-p11-starter/src/styles.css
packages/l1-p11-starter/tests/jest/spec.jest.test.ts
packages/l1-p11-starter/tests/setup.ts
packages/l1-p11-starter/tests/vitest/spec.test.ts
packages/l1-p11-starter/tsconfig.json
packages/l1-p11-starter/vite.config.ts
packages/l1-p11-starter/vitest.config.ts
packages/l1-p12-starter/README.md
packages/l1-p12-starter/babel.config.cjs
packages/l1-p12-starter/index.html
packages/l1-p12-starter/jest.config.cjs
packages/l1-p12-starter/package.json
packages/l1-p12-starter/src/App.tsx
packages/l1-p12-starter/src/components/ChartPanel.tsx
packages/l1-p12-starter/src/components/DataTable.tsx
packages/l1-p12-starter/src/data/members.json
packages/l1-p12-starter/src/lib/lib.ts
packages/l1-p12-starter/src/main.tsx
packages/l1-p12-starter/src/styles.css
packages/l1-p12-starter/tests/jest/spec.jest.test.ts
packages/l1-p12-starter/tests/setup.ts
packages/l1-p12-starter/tests/vitest/spec.test.ts
packages/l1-p12-starter/tsconfig.json
packages/l1-p12-starter/vite.config.ts
packages/l1-p12-starter/vitest.config.ts
packages/l1-p13-starter/README.md
packages/l1-p13-starter/babel.config.cjs
packages/l1-p13-starter/index.html
packages/l1-p13-starter/jest.config.cjs
packages/l1-p13-starter/package.json
packages/l1-p13-starter/src/App.tsx
packages/l1-p13-starter/src/components/ChartPanel.tsx
packages/l1-p13-starter/src/components/DataTable.tsx
packages/l1-p13-starter/src/data/members.json
packages/l1-p13-starter/src/lib/lib.ts
packages/l1-p13-starter/src/main.tsx
packages/l1-p13-starter/src/styles.css
packages/l1-p13-starter/tests/jest/spec.jest.test.ts
packages/l1-p13-starter/tests/setup.ts
packages/l1-p13-starter/tests/vitest/spec.test.ts
packages/l1-p13-starter/tsconfig.json
packages/l1-p13-starter/vite.config.ts
packages/l1-p13-starter/vitest.config.ts
packages/l1-p14-starter/README.md
packages/l1-p14-starter/babel.config.cjs
packages/l1-p14-starter/index.html
packages/l1-p14-starter/jest.config.cjs
packages/l1-p14-starter/package.json
packages/l1-p14-starter/src/App.tsx
packages/l1-p14-starter/src/components/ChartPanel.tsx
packages/l1-p14-starter/src/components/DataTable.tsx
packages/l1-p14-starter/src/data/members.json
packages/l1-p14-starter/src/lib/lib.ts
packages/l1-p14-starter/src/main.tsx
packages/l1-p14-starter/src/styles.css
packages/l1-p14-starter/tests/jest/spec.jest.test.ts
packages/l1-p14-starter/tests/setup.ts
packages/l1-p14-starter/tests/vitest/spec.test.ts
packages/l1-p14-starter/tsconfig.json
packages/l1-p14-starter/vite.config.ts
packages/l1-p14-starter/vitest.config.ts
packages/l1-p15-starter/README.md
packages/l1-p15-starter/babel.config.cjs
packages/l1-p15-starter/index.html
packages/l1-p15-starter/jest.config.cjs
packages/l1-p15-starter/package.json
packages/l1-p15-starter/src/App.tsx
packages/l1-p15-starter/src/components/ChartPanel.tsx
packages/l1-p15-starter/src/components/DataTable.tsx
packages/l1-p15-starter/src/data/members.json
packages/l1-p15-starter/src/lib/lib.ts
packages/l1-p15-starter/src/main.tsx
packages/l1-p15-starter/src/styles.css
packages/l1-p15-starter/tests/jest/spec.jest.test.ts
packages/l1-p15-starter/tests/setup.ts
packages/l1-p15-starter/tests/vitest/spec.test.ts
packages/l1-p15-starter/tsconfig.json
packages/l1-p15-starter/vite.config.ts
packages/l1-p15-starter/vitest.config.ts
packages/l2-p01-starter/README.md
packages/l2-p01-starter/babel.config.cjs
packages/l2-p01-starter/index.html
packages/l2-p01-starter/jest.config.cjs
packages/l2-p01-starter/package.json
packages/l2-p01-starter/src/App.tsx
packages/l2-p01-starter/src/components/ChartPanel.tsx
packages/l2-p01-starter/src/components/DataTable.tsx
packages/l2-p01-starter/src/data/members.json
packages/l2-p01-starter/src/lib/lib.ts
packages/l2-p01-starter/src/main.tsx
packages/l2-p01-starter/src/styles.css
packages/l2-p01-starter/tests/jest/spec.jest.test.ts
packages/l2-p01-starter/tests/setup.ts
packages/l2-p01-starter/tests/vitest/spec.test.ts
packages/l2-p01-starter/tsconfig.json
packages/l2-p01-starter/vite.config.ts
packages/l2-p01-starter/vitest.config.ts
packages/l2-p02-starter/README.md
packages/l2-p02-starter/babel.config.cjs
packages/l2-p02-starter/index.html
packages/l2-p02-starter/jest.config.cjs
packages/l2-p02-starter/package.json
packages/l2-p02-starter/src/App.tsx
packages/l2-p02-starter/src/components/ChartPanel.tsx
packages/l2-p02-starter/src/components/DataTable.tsx
packages/l2-p02-starter/src/data/members.json
packages/l2-p02-starter/src/lib/lib.ts
packages/l2-p02-starter/src/main.tsx
packages/l2-p02-starter/src/styles.css
packages/l2-p02-starter/tests/jest/spec.jest.test.ts
packages/l2-p02-starter/tests/setup.ts
packages/l2-p02-starter/tests/vitest/spec.test.ts
packages/l2-p02-starter/tsconfig.json
packages/l2-p02-starter/vite.config.ts
packages/l2-p02-starter/vitest.config.ts
packages/l2-p03-starter/README.md
packages/l2-p03-starter/babel.config.cjs
packages/l2-p03-starter/index.html
packages/l2-p03-starter/jest.config.cjs
packages/l2-p03-starter/package.json
packages/l2-p03-starter/src/App.tsx
packages/l2-p03-starter/src/components/ChartPanel.tsx
packages/l2-p03-starter/src/components/DataTable.tsx
packages/l2-p03-starter/src/data/members.json
packages/l2-p03-starter/src/lib/lib.ts
packages/l2-p03-starter/src/main.tsx
packages/l2-p03-starter/src/styles.css
packages/l2-p03-starter/tests/jest/spec.jest.test.ts
packages/l2-p03-starter/tests/setup.ts
packages/l2-p03-starter/tests/vitest/spec.test.ts
packages/l2-p03-starter/tsconfig.json
packages/l2-p03-starter/vite.config.ts
packages/l2-p03-starter/vitest.config.ts
packages/l2-p04-starter/README.md
packages/l2-p04-starter/babel.config.cjs
packages/l2-p04-starter/index.html
packages/l2-p04-starter/jest.config.cjs
packages/l2-p04-starter/package.json
packages/l2-p04-starter/src/App.tsx
packages/l2-p04-starter/src/components/ChartPanel.tsx
packages/l2-p04-starter/src/components/DataTable.tsx
packages/l2-p04-starter/src/data/members.json
packages/l2-p04-starter/src/lib/lib.ts
packages/l2-p04-starter/src/main.tsx
packages/l2-p04-starter/src/styles.css
packages/l2-p04-starter/tests/jest/spec.jest.test.ts
packages/l2-p04-starter/tests/setup.ts
packages/l2-p04-starter/tests/vitest/spec.test.ts
packages/l2-p04-starter/tsconfig.json
packages/l2-p04-starter/vite.config.ts
packages/l2-p04-starter/vitest.config.ts
packages/l2-p05-starter/README.md
packages/l2-p05-starter/babel.config.cjs
packages/l2-p05-starter/index.html
packages/l2-p05-starter/jest.config.cjs
packages/l2-p05-starter/package.json
packages/l2-p05-starter/src/App.tsx
packages/l2-p05-starter/src/components/ChartPanel.tsx
packages/l2-p05-starter/src/components/DataTable.tsx
packages/l2-p05-starter/src/data/members.json
packages/l2-p05-starter/src/lib/lib.ts
packages/l2-p05-starter/src/main.tsx
packages/l2-p05-starter/src/styles.css
packages/l2-p05-starter/tests/jest/spec.jest.test.ts
packages/l2-p05-starter/tests/setup.ts
packages/l2-p05-starter/tests/vitest/spec.test.ts
packages/l2-p05-starter/tsconfig.json
packages/l2-p05-starter/vite.config.ts
packages/l2-p05-starter/vitest.config.ts
packages/l2-p06-starter/README.md
packages/l2-p06-starter/babel.config.cjs
packages/l2-p06-starter/index.html
packages/l2-p06-starter/jest.config.cjs
packages/l2-p06-starter/package.json
packages/l2-p06-starter/src/App.tsx
packages/l2-p06-starter/src/components/ChartPanel.tsx
packages/l2-p06-starter/src/components/DataTable.tsx
packages/l2-p06-starter/src/data/members.json
packages/l2-p06-starter/src/lib/lib.ts
packages/l2-p06-starter/src/main.tsx
packages/l2-p06-starter/src/styles.css
packages/l2-p06-starter/tests/jest/spec.jest.test.ts
packages/l2-p06-starter/tests/setup.ts
packages/l2-p06-starter/tests/vitest/spec.test.ts
packages/l2-p06-starter/tsconfig.json
packages/l2-p06-starter/vite.config.ts
packages/l2-p06-starter/vitest.config.ts
packages/l2-p07-starter/README.md
packages/l2-p07-starter/babel.config.cjs
packages/l2-p07-starter/index.html
packages/l2-p07-starter/jest.config.cjs
packages/l2-p07-starter/package.json
packages/l2-p07-starter/src/App.tsx
packages/l2-p07-starter/src/components/ChartPanel.tsx
packages/l2-p07-starter/src/components/DataTable.tsx
packages/l2-p07-starter/src/data/members.json
packages/l2-p07-starter/src/lib/lib.ts
packages/l2-p07-starter/src/main.tsx
packages/l2-p07-starter/src/styles.css
packages/l2-p07-starter/tests/jest/spec.jest.test.ts
packages/l2-p07-starter/tests/setup.ts
packages/l2-p07-starter/tests/vitest/spec.test.ts
packages/l2-p07-starter/tsconfig.json
packages/l2-p07-starter/vite.config.ts
packages/l2-p07-starter/vitest.config.ts
packages/l2-p08-starter/README.md
packages/l2-p08-starter/babel.config.cjs
packages/l2-p08-starter/index.html
packages/l2-p08-starter/jest.config.cjs
packages/l2-p08-starter/package.json
packages/l2-p08-starter/src/App.tsx
packages/l2-p08-starter/src/components/ChartPanel.tsx
packages/l2-p08-starter/src/components/DataTable.tsx
packages/l2-p08-starter/src/data/members.json
packages/l2-p08-starter/src/lib/lib.ts
packages/l2-p08-starter/src/main.tsx
packages/l2-p08-starter/src/styles.css
packages/l2-p08-starter/tests/jest/spec.jest.test.ts
packages/l2-p08-starter/tests/setup.ts
packages/l2-p08-starter/tests/vitest/spec.test.ts
packages/l2-p08-starter/tsconfig.json
packages/l2-p08-starter/vite.config.ts
packages/l2-p08-starter/vitest.config.ts
packages/l2-p09-starter/README.md
packages/l2-p09-starter/babel.config.cjs
packages/l2-p09-starter/index.html
packages/l2-p09-starter/jest.config.cjs
packages/l2-p09-starter/package.json
packages/l2-p09-starter/src/App.tsx
packages/l2-p09-starter/src/components/ChartPanel.tsx
packages/l2-p09-starter/src/components/DataTable.tsx
packages/l2-p09-starter/src/data/members.json
packages/l2-p09-starter/src/lib/lib.ts
packages/l2-p09-starter/src/main.tsx
packages/l2-p09-starter/src/styles.css
packages/l2-p09-starter/tests/jest/spec.jest.test.ts
packages/l2-p09-starter/tests/setup.ts
packages/l2-p09-starter/tests/vitest/spec.test.ts
packages/l2-p09-starter/tsconfig.json
packages/l2-p09-starter/vite.config.ts
packages/l2-p09-starter/vitest.config.ts
packages/l2-p10-starter/README.md
packages/l2-p10-starter/babel.config.cjs
packages/l2-p10-starter/index.html
packages/l2-p10-starter/jest.config.cjs
packages/l2-p10-starter/package.json
packages/l2-p10-starter/src/App.tsx
packages/l2-p10-starter/src/components/ChartPanel.tsx
packages/l2-p10-starter/src/components/DataTable.tsx
packages/l2-p10-starter/src/data/members.json
packages/l2-p10-starter/src/lib/lib.ts
packages/l2-p10-starter/src/main.tsx
packages/l2-p10-starter/src/styles.css
packages/l2-p10-starter/tests/jest/spec.jest.test.ts
packages/l2-p10-starter/tests/setup.ts
packages/l2-p10-starter/tests/vitest/spec.test.ts
packages/l2-p10-starter/tsconfig.json
packages/l2-p10-starter/vite.config.ts
packages/l2-p10-starter/vitest.config.ts
packages/l2-p11-starter/README.md
packages/l2-p11-starter/babel.config.cjs
packages/l2-p11-starter/index.html
packages/l2-p11-starter/jest.config.cjs
packages/l2-p11-starter/package.json
packages/l2-p11-starter/src/App.tsx
packages/l2-p11-starter/src/components/ChartPanel.tsx
packages/l2-p11-starter/src/components/DataTable.tsx
packages/l2-p11-starter/src/data/members.json
packages/l2-p11-starter/src/lib/lib.ts
packages/l2-p11-starter/src/main.tsx
packages/l2-p11-starter/src/styles.css
packages/l2-p11-starter/tests/jest/spec.jest.test.ts
packages/l2-p11-starter/tests/setup.ts
packages/l2-p11-starter/tests/vitest/spec.test.ts
packages/l2-p11-starter/tsconfig.json
packages/l2-p11-starter/vite.config.ts
packages/l2-p11-starter/vitest.config.ts
packages/l2-p12-starter/README.md
packages/l2-p12-starter/babel.config.cjs
packages/l2-p12-starter/index.html
packages/l2-p12-starter/jest.config.cjs
packages/l2-p12-starter/package.json
packages/l2-p12-starter/src/App.tsx
packages/l2-p12-starter/src/components/ChartPanel.tsx
packages/l2-p12-starter/src/components/DataTable.tsx
packages/l2-p12-starter/src/data/members.json
packages/l2-p12-starter/src/lib/lib.ts
packages/l2-p12-starter/src/main.tsx
packages/l2-p12-starter/src/styles.css
packages/l2-p12-starter/tests/jest/spec.jest.test.ts
packages/l2-p12-starter/tests/setup.ts
packages/l2-p12-starter/tests/vitest/spec.test.ts
packages/l2-p12-starter/tsconfig.json
packages/l2-p12-starter/vite.config.ts
packages/l2-p12-starter/vitest.config.ts
packages/l2-p13-starter/README.md
packages/l2-p13-starter/babel.config.cjs
packages/l2-p13-starter/index.html
packages/l2-p13-starter/jest.config.cjs
packages/l2-p13-starter/package.json
packages/l2-p13-starter/src/App.tsx
packages/l2-p13-starter/src/components/ChartPanel.tsx
packages/l2-p13-starter/src/components/DataTable.tsx
packages/l2-p13-starter/src/data/members.json
packages/l2-p13-starter/src/lib/lib.ts
packages/l2-p13-starter/src/main.tsx
packages/l2-p13-starter/src/styles.css
packages/l2-p13-starter/tests/jest/spec.jest.test.ts
packages/l2-p13-starter/tests/setup.ts
packages/l2-p13-starter/tests/vitest/spec.test.ts
packages/l2-p13-starter/tsconfig.json
packages/l2-p13-starter/vite.config.ts
packages/l2-p13-starter/vitest.config.ts
packages/l2-p14-starter/README.md
packages/l2-p14-starter/babel.config.cjs
packages/l2-p14-starter/index.html
packages/l2-p14-starter/jest.config.cjs
packages/l2-p14-starter/package.json
packages/l2-p14-starter/src/App.tsx
packages/l2-p14-starter/src/components/ChartPanel.tsx
packages/l2-p14-starter/src/components/DataTable.tsx
packages/l2-p14-starter/src/data/members.json
packages/l2-p14-starter/src/lib/lib.ts
packages/l2-p14-starter/src/main.tsx
packages/l2-p14-starter/src/styles.css
packages/l2-p14-starter/tests/jest/spec.jest.test.ts
packages/l2-p14-starter/tests/setup.ts
packages/l2-p14-starter/tests/vitest/spec.test.ts
packages/l2-p14-starter/tsconfig.json
packages/l2-p14-starter/vite.config.ts
packages/l2-p14-starter/vitest.config.ts
packages/l2-p15-starter/README.md
packages/l2-p15-starter/babel.config.cjs
packages/l2-p15-starter/index.html
packages/l2-p15-starter/jest.config.cjs
packages/l2-p15-starter/package.json
packages/l2-p15-starter/src/App.tsx
packages/l2-p15-starter/src/components/ChartPanel.tsx
packages/l2-p15-starter/src/components/DataTable.tsx
packages/l2-p15-starter/src/data/members.json
packages/l2-p15-starter/src/lib/lib.ts
packages/l2-p15-starter/src/main.tsx
packages/l2-p15-starter/src/styles.css
packages/l2-p15-starter/tests/jest/spec.jest.test.ts
packages/l2-p15-starter/tests/setup.ts
packages/l2-p15-starter/tests/vitest/spec.test.ts
packages/l2-p15-starter/tsconfig.json
packages/l2-p15-starter/vite.config.ts
packages/l2-p15-starter/vitest.config.ts
packages/l3-p01-starter/README.md
packages/l3-p01-starter/babel.config.cjs
packages/l3-p01-starter/index.html
packages/l3-p01-starter/jest.config.cjs
packages/l3-p01-starter/package.json
packages/l3-p01-starter/src/App.tsx
packages/l3-p01-starter/src/components/ChartPanel.tsx
packages/l3-p01-starter/src/components/DataTable.tsx
packages/l3-p01-starter/src/data/members.json
packages/l3-p01-starter/src/lib/lib.ts
packages/l3-p01-starter/src/main.tsx
packages/l3-p01-starter/src/styles.css
packages/l3-p01-starter/tests/jest/spec.jest.test.ts
packages/l3-p01-starter/tests/setup.ts
packages/l3-p01-starter/tests/vitest/spec.test.ts
packages/l3-p01-starter/tsconfig.json
packages/l3-p01-starter/vite.config.ts
packages/l3-p01-starter/vitest.config.ts
packages/l3-p02-starter/README.md
packages/l3-p02-starter/babel.config.cjs
packages/l3-p02-starter/index.html
packages/l3-p02-starter/jest.config.cjs
packages/l3-p02-starter/package.json
packages/l3-p02-starter/src/App.tsx
packages/l3-p02-starter/src/components/ChartPanel.tsx
packages/l3-p02-starter/src/components/DataTable.tsx
packages/l3-p02-starter/src/data/members.json
packages/l3-p02-starter/src/lib/lib.ts
packages/l3-p02-starter/src/main.tsx
packages/l3-p02-starter/src/styles.css
packages/l3-p02-starter/tests/jest/spec.jest.test.ts
packages/l3-p02-starter/tests/setup.ts
packages/l3-p02-starter/tests/vitest/spec.test.ts
packages/l3-p02-starter/tsconfig.json
packages/l3-p02-starter/vite.config.ts
packages/l3-p02-starter/vitest.config.ts
packages/l3-p03-starter/README.md
packages/l3-p03-starter/babel.config.cjs
packages/l3-p03-starter/index.html
packages/l3-p03-starter/jest.config.cjs
packages/l3-p03-starter/package.json
packages/l3-p03-starter/src/App.tsx
packages/l3-p03-starter/src/components/ChartPanel.tsx
packages/l3-p03-starter/src/components/DataTable.tsx
packages/l3-p03-starter/src/data/members.json
packages/l3-p03-starter/src/lib/lib.ts
packages/l3-p03-starter/src/main.tsx
packages/l3-p03-starter/src/styles.css
packages/l3-p03-starter/tests/jest/spec.jest.test.ts
packages/l3-p03-starter/tests/setup.ts
packages/l3-p03-starter/tests/vitest/spec.test.ts
packages/l3-p03-starter/tsconfig.json
packages/l3-p03-starter/vite.config.ts
packages/l3-p03-starter/vitest.config.ts
packages/l3-p04-starter/README.md
packages/l3-p04-starter/babel.config.cjs
packages/l3-p04-starter/index.html
packages/l3-p04-starter/jest.config.cjs
packages/l3-p04-starter/package.json
packages/l3-p04-starter/src/App.tsx
packages/l3-p04-starter/src/components/ChartPanel.tsx
packages/l3-p04-starter/src/components/DataTable.tsx
packages/l3-p04-starter/src/data/members.json
packages/l3-p04-starter/src/lib/lib.ts
packages/l3-p04-starter/src/main.tsx
packages/l3-p04-starter/src/styles.css
packages/l3-p04-starter/tests/jest/spec.jest.test.ts
packages/l3-p04-starter/tests/setup.ts
packages/l3-p04-starter/tests/vitest/spec.test.ts
packages/l3-p04-starter/tsconfig.json
packages/l3-p04-starter/vite.config.ts
packages/l3-p04-starter/vitest.config.ts
packages/l3-p05-starter/README.md
packages/l3-p05-starter/babel.config.cjs
packages/l3-p05-starter/index.html
packages/l3-p05-starter/jest.config.cjs
packages/l3-p05-starter/package.json
packages/l3-p05-starter/src/App.tsx
packages/l3-p05-starter/src/components/ChartPanel.tsx
packages/l3-p05-starter/src/components/DataTable.tsx
packages/l3-p05-starter/src/data/members.json
packages/l3-p05-starter/src/lib/lib.ts
packages/l3-p05-starter/src/main.tsx
packages/l3-p05-starter/src/styles.css
packages/l3-p05-starter/tests/jest/spec.jest.test.ts
packages/l3-p05-starter/tests/setup.ts
packages/l3-p05-starter/tests/vitest/spec.test.ts
packages/l3-p05-starter/tsconfig.json
packages/l3-p05-starter/vite.config.ts
packages/l3-p05-starter/vitest.config.ts
packages/l3-p06-starter/README.md
packages/l3-p06-starter/babel.config.cjs
packages/l3-p06-starter/index.html
packages/l3-p06-starter/jest.config.cjs
packages/l3-p06-starter/package.json
packages/l3-p06-starter/src/App.tsx
packages/l3-p06-starter/src/components/ChartPanel.tsx
packages/l3-p06-starter/src/components/DataTable.tsx
packages/l3-p06-starter/src/data/members.json
packages/l3-p06-starter/src/lib/lib.ts
packages/l3-p06-starter/src/main.tsx
packages/l3-p06-starter/src/styles.css
packages/l3-p06-starter/tests/jest/spec.jest.test.ts
packages/l3-p06-starter/tests/setup.ts
packages/l3-p06-starter/tests/vitest/spec.test.ts
packages/l3-p06-starter/tsconfig.json
packages/l3-p06-starter/vite.config.ts
packages/l3-p06-starter/vitest.config.ts
packages/l3-p07-starter/README.md
packages/l3-p07-starter/babel.config.cjs
packages/l3-p07-starter/index.html
packages/l3-p07-starter/jest.config.cjs
packages/l3-p07-starter/package.json
packages/l3-p07-starter/src/App.tsx
packages/l3-p07-starter/src/components/ChartPanel.tsx
packages/l3-p07-starter/src/components/DataTable.tsx
packages/l3-p07-starter/src/data/members.json
packages/l3-p07-starter/src/lib/lib.ts
packages/l3-p07-starter/src/main.tsx
packages/l3-p07-starter/src/styles.css
packages/l3-p07-starter/tests/jest/spec.jest.test.ts
packages/l3-p07-starter/tests/setup.ts
packages/l3-p07-starter/tests/vitest/spec.test.ts
packages/l3-p07-starter/tsconfig.json
packages/l3-p07-starter/vite.config.ts
packages/l3-p07-starter/vitest.config.ts
packages/l3-p08-starter/README.md
packages/l3-p08-starter/babel.config.cjs
packages/l3-p08-starter/index.html
packages/l3-p08-starter/jest.config.cjs
packages/l3-p08-starter/package.json
packages/l3-p08-starter/src/App.tsx
packages/l3-p08-starter/src/components/ChartPanel.tsx
packages/l3-p08-starter/src/components/DataTable.tsx
packages/l3-p08-starter/src/data/members.json
packages/l3-p08-starter/src/lib/lib.ts
packages/l3-p08-starter/src/main.tsx
packages/l3-p08-starter/src/styles.css
packages/l3-p08-starter/tests/jest/spec.jest.test.ts
packages/l3-p08-starter/tests/setup.ts
packages/l3-p08-starter/tests/vitest/spec.test.ts
packages/l3-p08-starter/tsconfig.json
packages/l3-p08-starter/vite.config.ts
packages/l3-p08-starter/vitest.config.ts
packages/l3-p09-starter/README.md
packages/l3-p09-starter/babel.config.cjs
packages/l3-p09-starter/index.html
packages/l3-p09-starter/jest.config.cjs
packages/l3-p09-starter/package.json
packages/l3-p09-starter/src/App.tsx
packages/l3-p09-starter/src/components/ChartPanel.tsx
packages/l3-p09-starter/src/components/DataTable.tsx
packages/l3-p09-starter/src/data/members.json
packages/l3-p09-starter/src/lib/lib.ts
packages/l3-p09-starter/src/main.tsx
packages/l3-p09-starter/src/styles.css
packages/l3-p09-starter/tests/jest/spec.jest.test.ts
packages/l3-p09-starter/tests/setup.ts
packages/l3-p09-starter/tests/vitest/spec.test.ts
packages/l3-p09-starter/tsconfig.json
packages/l3-p09-starter/vite.config.ts
packages/l3-p09-starter/vitest.config.ts
packages/l3-p10-starter/README.md
packages/l3-p10-starter/babel.config.cjs
packages/l3-p10-starter/index.html
packages/l3-p10-starter/jest.config.cjs
packages/l3-p10-starter/package.json
packages/l3-p10-starter/src/App.tsx
packages/l3-p10-starter/src/components/ChartPanel.tsx
packages/l3-p10-starter/src/components/DataTable.tsx
packages/l3-p10-starter/src/data/members.json
packages/l3-p10-starter/src/lib/lib.ts
packages/l3-p10-starter/src/main.tsx
packages/l3-p10-starter/src/styles.css
packages/l3-p10-starter/tests/jest/spec.jest.test.ts
packages/l3-p10-starter/tests/setup.ts
packages/l3-p10-starter/tests/vitest/spec.test.ts
packages/l3-p10-starter/tsconfig.json
packages/l3-p10-starter/vite.config.ts
packages/l3-p10-starter/vitest.config.ts
packages/l3-p11-starter/README.md
packages/l3-p11-starter/babel.config.cjs
packages/l3-p11-starter/index.html
packages/l3-p11-starter/jest.config.cjs
packages/l3-p11-starter/package.json
packages/l3-p11-starter/src/App.tsx
packages/l3-p11-starter/src/components/ChartPanel.tsx
packages/l3-p11-starter/src/components/DataTable.tsx
packages/l3-p11-starter/src/data/members.json
packages/l3-p11-starter/src/lib/lib.ts
packages/l3-p11-starter/src/main.tsx
packages/l3-p11-starter/src/styles.css
packages/l3-p11-starter/tests/jest/spec.jest.test.ts
packages/l3-p11-starter/tests/setup.ts
packages/l3-p11-starter/tests/vitest/spec.test.ts
packages/l3-p11-starter/tsconfig.json
packages/l3-p11-starter/vite.config.ts
packages/l3-p11-starter/vitest.config.ts
packages/l3-p12-starter/README.md
packages/l3-p12-starter/babel.config.cjs
packages/l3-p12-starter/index.html
packages/l3-p12-starter/jest.config.cjs
packages/l3-p12-starter/package.json
packages/l3-p12-starter/src/App.tsx
packages/l3-p12-starter/src/components/ChartPanel.tsx
packages/l3-p12-starter/src/components/DataTable.tsx
packages/l3-p12-starter/src/data/members.json
packages/l3-p12-starter/src/lib/lib.ts
packages/l3-p12-starter/src/main.tsx
packages/l3-p12-starter/src/styles.css
packages/l3-p12-starter/tests/jest/spec.jest.test.ts
packages/l3-p12-starter/tests/setup.ts
packages/l3-p12-starter/tests/vitest/spec.test.ts
packages/l3-p12-starter/tsconfig.json
packages/l3-p12-starter/vite.config.ts
packages/l3-p12-starter/vitest.config.ts
packages/l3-p13-starter/README.md
packages/l3-p13-starter/babel.config.cjs
packages/l3-p13-starter/index.html
packages/l3-p13-starter/jest.config.cjs
packages/l3-p13-starter/package.json
packages/l3-p13-starter/src/App.tsx
packages/l3-p13-starter/src/components/ChartPanel.tsx
packages/l3-p13-starter/src/components/DataTable.tsx
packages/l3-p13-starter/src/data/members.json
packages/l3-p13-starter/src/lib/lib.ts
packages/l3-p13-starter/src/main.tsx
packages/l3-p13-starter/src/styles.css
packages/l3-p13-starter/tests/jest/spec.jest.test.ts
packages/l3-p13-starter/tests/setup.ts
packages/l3-p13-starter/tests/vitest/spec.test.ts
packages/l3-p13-starter/tsconfig.json
packages/l3-p13-starter/vite.config.ts
packages/l3-p13-starter/vitest.config.ts
packages/l3-p14-starter/README.md
packages/l3-p14-starter/babel.config.cjs
packages/l3-p14-starter/index.html
packages/l3-p14-starter/jest.config.cjs
packages/l3-p14-starter/package.json
packages/l3-p14-starter/src/App.tsx
packages/l3-p14-starter/src/components/ChartPanel.tsx
packages/l3-p14-starter/src/components/DataTable.tsx
packages/l3-p14-starter/src/data/members.json
packages/l3-p14-starter/src/lib/lib.ts
packages/l3-p14-starter/src/main.tsx
packages/l3-p14-starter/src/styles.css
packages/l3-p14-starter/tests/jest/spec.jest.test.ts
packages/l3-p14-starter/tests/setup.ts
packages/l3-p14-starter/tests/vitest/spec.test.ts
packages/l3-p14-starter/tsconfig.json
packages/l3-p14-starter/vite.config.ts
packages/l3-p14-starter/vitest.config.ts
packages/l3-p15-starter/README.md
packages/l3-p15-starter/babel.config.cjs
packages/l3-p15-starter/index.html
packages/l3-p15-starter/jest.config.cjs
packages/l3-p15-starter/package.json
packages/l3-p15-starter/src/App.tsx
packages/l3-p15-starter/src/components/ChartPanel.tsx
packages/l3-p15-starter/src/components/DataTable.tsx
packages/l3-p15-starter/src/data/members.json
packages/l3-p15-starter/src/lib/lib.ts
packages/l3-p15-starter/src/main.tsx
packages/l3-p15-starter/src/styles.css
packages/l3-p15-starter/tests/jest/spec.jest.test.ts
packages/l3-p15-starter/tests/setup.ts
packages/l3-p15-starter/tests/vitest/spec.test.ts
packages/l3-p15-starter/tsconfig.json
packages/l3-p15-starter/vite.config.ts
packages/l3-p15-starter/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** starter: 810.

**Categorii de fișiere:** config: 272, other: 45, docs: 45, code: 315, tests: 135.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s12p3-monorepo` type=`module` workspaces=True
- `packages/l1-p01-starter/package.json`: name=`l1-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p02-starter/package.json`: name=`l1-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p03-starter/package.json`: name=`l1-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p04-starter/package.json`: name=`l1-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p05-starter/package.json`: name=`l1-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p06-starter/package.json`: name=`l1-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p07-starter/package.json`: name=`l1-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p08-starter/package.json`: name=`l1-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p09-starter/package.json`: name=`l1-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p10-starter/package.json`: name=`l1-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p11-starter/package.json`: name=`l1-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p12-starter/package.json`: name=`l1-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p13-starter/package.json`: name=`l1-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p14-starter/package.json`: name=`l1-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p15-starter/package.json`: name=`l1-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p01-starter/package.json`: name=`l2-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p02-starter/package.json`: name=`l2-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p03-starter/package.json`: name=`l2-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p04-starter/package.json`: name=`l2-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p05-starter/package.json`: name=`l2-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p06-starter/package.json`: name=`l2-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p07-starter/package.json`: name=`l2-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p08-starter/package.json`: name=`l2-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p09-starter/package.json`: name=`l2-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p10-starter/package.json`: name=`l2-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p11-starter/package.json`: name=`l2-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p12-starter/package.json`: name=`l2-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p13-starter/package.json`: name=`l2-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p14-starter/package.json`: name=`l2-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p15-starter/package.json`: name=`l2-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p01-starter/package.json`: name=`l3-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p02-starter/package.json`: name=`l3-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p03-starter/package.json`: name=`l3-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p04-starter/package.json`: name=`l3-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p05-starter/package.json`: name=`l3-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p06-starter/package.json`: name=`l3-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p07-starter/package.json`: name=`l3-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p08-starter/package.json`: name=`l3-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p09-starter/package.json`: name=`l3-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p10-starter/package.json`: name=`l3-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p11-starter/package.json`: name=`l3-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p12-starter/package.json`: name=`l3-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p13-starter/package.json`: name=`l3-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p14-starter/package.json`: name=`l3-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p15-starter/package.json`: name=`l3-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest

### Seminar12_Partea3_p3-standalone.zip

> Structura este mare; se afișează începutul și sfârșitul.

```
L1/L1-P01/solution/README.md
L1/L1-P01/solution/babel.config.cjs
L1/L1-P01/solution/index.html
L1/L1-P01/solution/jest.config.cjs
L1/L1-P01/solution/package.json
L1/L1-P01/solution/src/App.tsx
L1/L1-P01/solution/src/components/ChartPanel.tsx
L1/L1-P01/solution/src/components/DataTable.tsx
L1/L1-P01/solution/src/data/members.json
L1/L1-P01/solution/src/lib/lib.ts
L1/L1-P01/solution/src/main.tsx
L1/L1-P01/solution/src/styles.css
L1/L1-P01/solution/tests/jest/spec.jest.test.ts
L1/L1-P01/solution/tests/setup.ts
L1/L1-P01/solution/tests/vitest/spec.test.ts
L1/L1-P01/solution/tsconfig.json
L1/L1-P01/solution/vite.config.ts
L1/L1-P01/solution/vitest.config.ts
L1/L1-P01/starter/README.md
L1/L1-P01/starter/babel.config.cjs
L1/L1-P01/starter/index.html
L1/L1-P01/starter/jest.config.cjs
L1/L1-P01/starter/package.json
L1/L1-P01/starter/src/App.tsx
L1/L1-P01/starter/src/components/ChartPanel.tsx
L1/L1-P01/starter/src/components/DataTable.tsx
L1/L1-P01/starter/src/data/members.json
L1/L1-P01/starter/src/lib/lib.ts
L1/L1-P01/starter/src/main.tsx
L1/L1-P01/starter/src/styles.css
L1/L1-P01/starter/tests/jest/spec.jest.test.ts
L1/L1-P01/starter/tests/setup.ts
L1/L1-P01/starter/tests/vitest/spec.test.ts
L1/L1-P01/starter/tsconfig.json
L1/L1-P01/starter/vite.config.ts
L1/L1-P01/starter/vitest.config.ts
L1/L1-P02/solution/README.md
L1/L1-P02/solution/babel.config.cjs
L1/L1-P02/solution/index.html
L1/L1-P02/solution/jest.config.cjs
L1/L1-P02/solution/package.json
L1/L1-P02/solution/src/App.tsx
L1/L1-P02/solution/src/components/ChartPanel.tsx
L1/L1-P02/solution/src/components/DataTable.tsx
L1/L1-P02/solution/src/data/members.json
L1/L1-P02/solution/src/lib/lib.ts
L1/L1-P02/solution/src/main.tsx
L1/L1-P02/solution/src/styles.css
L1/L1-P02/solution/tests/jest/spec.jest.test.ts
L1/L1-P02/solution/tests/setup.ts
L1/L1-P02/solution/tests/vitest/spec.test.ts
L1/L1-P02/solution/tsconfig.json
L1/L1-P02/solution/vite.config.ts
L1/L1-P02/solution/vitest.config.ts
L1/L1-P02/starter/README.md
L1/L1-P02/starter/babel.config.cjs
L1/L1-P02/starter/index.html
L1/L1-P02/starter/jest.config.cjs
L1/L1-P02/starter/package.json
L1/L1-P02/starter/src/App.tsx
L1/L1-P02/starter/src/components/ChartPanel.tsx
L1/L1-P02/starter/src/components/DataTable.tsx
L1/L1-P02/starter/src/data/members.json
L1/L1-P02/starter/src/lib/lib.ts
L1/L1-P02/starter/src/main.tsx
L1/L1-P02/starter/src/styles.css
L1/L1-P02/starter/tests/jest/spec.jest.test.ts
L1/L1-P02/starter/tests/setup.ts
L1/L1-P02/starter/tests/vitest/spec.test.ts
L1/L1-P02/starter/tsconfig.json
L1/L1-P02/starter/vite.config.ts
L1/L1-P02/starter/vitest.config.ts
L1/L1-P03/solution/README.md
L1/L1-P03/solution/babel.config.cjs
L1/L1-P03/solution/index.html
L1/L1-P03/solution/jest.config.cjs
L1/L1-P03/solution/package.json
L1/L1-P03/solution/src/App.tsx
L1/L1-P03/solution/src/components/ChartPanel.tsx
L1/L1-P03/solution/src/components/DataTable.tsx
L1/L1-P03/solution/src/data/members.json
L1/L1-P03/solution/src/lib/lib.ts
L1/L1-P03/solution/src/main.tsx
L1/L1-P03/solution/src/styles.css
L1/L1-P03/solution/tests/jest/spec.jest.test.ts
L1/L1-P03/solution/tests/setup.ts
L1/L1-P03/solution/tests/vitest/spec.test.ts
L1/L1-P03/solution/tsconfig.json
L1/L1-P03/solution/vite.config.ts
L1/L1-P03/solution/vitest.config.ts
L1/L1-P03/starter/README.md
L1/L1-P03/starter/babel.config.cjs
L1/L1-P03/starter/index.html
L1/L1-P03/starter/jest.config.cjs
L1/L1-P03/starter/package.json
L1/L1-P03/starter/src/App.tsx
L1/L1-P03/starter/src/components/ChartPanel.tsx
L1/L1-P03/starter/src/components/DataTable.tsx
L1/L1-P03/starter/src/data/members.json
L1/L1-P03/starter/src/lib/lib.ts
L1/L1-P03/starter/src/main.tsx
L1/L1-P03/starter/src/styles.css
L1/L1-P03/starter/tests/jest/spec.jest.test.ts
L1/L1-P03/starter/tests/setup.ts
L1/L1-P03/starter/tests/vitest/spec.test.ts
L1/L1-P03/starter/tsconfig.json
L1/L1-P03/starter/vite.config.ts
L1/L1-P03/starter/vitest.config.ts
L1/L1-P04/solution/README.md
L1/L1-P04/solution/babel.config.cjs
L1/L1-P04/solution/index.html
L1/L1-P04/solution/jest.config.cjs
L1/L1-P04/solution/package.json
L1/L1-P04/solution/src/App.tsx
L1/L1-P04/solution/src/components/ChartPanel.tsx
L1/L1-P04/solution/src/components/DataTable.tsx
L1/L1-P04/solution/src/data/members.json
L1/L1-P04/solution/src/lib/lib.ts
L1/L1-P04/solution/src/main.tsx
L1/L1-P04/solution/src/styles.css
L1/L1-P04/solution/tests/jest/spec.jest.test.ts
L1/L1-P04/solution/tests/setup.ts
L1/L1-P04/solution/tests/vitest/spec.test.ts
L1/L1-P04/solution/tsconfig.json
L1/L1-P04/solution/vite.config.ts
L1/L1-P04/solution/vitest.config.ts
L1/L1-P04/starter/README.md
L1/L1-P04/starter/babel.config.cjs
L1/L1-P04/starter/index.html
L1/L1-P04/starter/jest.config.cjs
L1/L1-P04/starter/package.json
L1/L1-P04/starter/src/App.tsx
L1/L1-P04/starter/src/components/ChartPanel.tsx
L1/L1-P04/starter/src/components/DataTable.tsx
L1/L1-P04/starter/src/data/members.json
L1/L1-P04/starter/src/lib/lib.ts
L1/L1-P04/starter/src/main.tsx
L1/L1-P04/starter/src/styles.css
L1/L1-P04/starter/tests/jest/spec.jest.test.ts
L1/L1-P04/starter/tests/setup.ts
L1/L1-P04/starter/tests/vitest/spec.test.ts
L1/L1-P04/starter/tsconfig.json
L1/L1-P04/starter/vite.config.ts
L1/L1-P04/starter/vitest.config.ts
L1/L1-P05/solution/README.md
L1/L1-P05/solution/babel.config.cjs
L1/L1-P05/solution/index.html
L1/L1-P05/solution/jest.config.cjs
L1/L1-P05/solution/package.json
L1/L1-P05/solution/src/App.tsx
L1/L1-P05/solution/src/components/ChartPanel.tsx
L1/L1-P05/solution/src/components/DataTable.tsx
L1/L1-P05/solution/src/data/members.json
L1/L1-P05/solution/src/lib/lib.ts
L1/L1-P05/solution/src/main.tsx
L1/L1-P05/solution/src/styles.css
L1/L1-P05/solution/tests/jest/spec.jest.test.ts
L1/L1-P05/solution/tests/setup.ts
L1/L1-P05/solution/tests/vitest/spec.test.ts
L1/L1-P05/solution/tsconfig.json
L1/L1-P05/solution/vite.config.ts
L1/L1-P05/solution/vitest.config.ts
L1/L1-P05/starter/README.md
L1/L1-P05/starter/babel.config.cjs
L1/L1-P05/starter/index.html
L1/L1-P05/starter/jest.config.cjs
L1/L1-P05/starter/package.json
L1/L1-P05/starter/src/App.tsx
L1/L1-P05/starter/src/components/ChartPanel.tsx
L1/L1-P05/starter/src/components/DataTable.tsx
L1/L1-P05/starter/src/data/members.json
L1/L1-P05/starter/src/lib/lib.ts
L1/L1-P05/starter/src/main.tsx
L1/L1-P05/starter/src/styles.css
L1/L1-P05/starter/tests/jest/spec.jest.test.ts
L1/L1-P05/starter/tests/setup.ts
L1/L1-P05/starter/tests/vitest/spec.test.ts
L1/L1-P05/starter/tsconfig.json
L1/L1-P05/starter/vite.config.ts
L1/L1-P05/starter/vitest.config.ts
L1/L1-P06/solution/README.md
L1/L1-P06/solution/babel.config.cjs
L1/L1-P06/solution/index.html
L1/L1-P06/solution/jest.config.cjs
L1/L1-P06/solution/package.json
L1/L1-P06/solution/src/App.tsx
L1/L1-P06/solution/src/components/ChartPanel.tsx
L1/L1-P06/solution/src/components/DataTable.tsx
L1/L1-P06/solution/src/data/members.json
L1/L1-P06/solution/src/lib/lib.ts
L1/L1-P06/solution/src/main.tsx
L1/L1-P06/solution/src/styles.css
L1/L1-P06/solution/tests/jest/spec.jest.test.ts
L1/L1-P06/solution/tests/setup.ts
L1/L1-P06/solution/tests/vitest/spec.test.ts
L1/L1-P06/solution/tsconfig.json
L1/L1-P06/solution/vite.config.ts
L1/L1-P06/solution/vitest.config.ts
L1/L1-P06/starter/README.md
L1/L1-P06/starter/babel.config.cjs
L1/L1-P06/starter/index.html
L1/L1-P06/starter/jest.config.cjs
L1/L1-P06/starter/package.json
L1/L1-P06/starter/src/App.tsx
L1/L1-P06/starter/src/components/ChartPanel.tsx
L1/L1-P06/starter/src/components/DataTable.tsx
L1/L1-P06/starter/src/data/members.json
L1/L1-P06/starter/src/lib/lib.ts
L1/L1-P06/starter/src/main.tsx
L1/L1-P06/starter/src/styles.css
L1/L1-P06/starter/tests/jest/spec.jest.test.ts
L1/L1-P06/starter/tests/setup.ts
L1/L1-P06/starter/tests/vitest/spec.test.ts
L1/L1-P06/starter/tsconfig.json
L1/L1-P06/starter/vite.config.ts
L1/L1-P06/starter/vitest.config.ts
L1/L1-P07/solution/README.md
L1/L1-P07/solution/babel.config.cjs
L1/L1-P07/solution/index.html
L1/L1-P07/solution/jest.config.cjs
L1/L1-P07/solution/package.json
L1/L1-P07/solution/src/App.tsx
L1/L1-P07/solution/src/components/ChartPanel.tsx
L1/L1-P07/solution/src/components/DataTable.tsx
L1/L1-P07/solution/src/data/members.json
L1/L1-P07/solution/src/lib/lib.ts
L1/L1-P07/solution/src/main.tsx
L1/L1-P07/solution/src/styles.css
L1/L1-P07/solution/tests/jest/spec.jest.test.ts
L1/L1-P07/solution/tests/setup.ts
L1/L1-P07/solution/tests/vitest/spec.test.ts
L1/L1-P07/solution/tsconfig.json
L1/L1-P07/solution/vite.config.ts
L1/L1-P07/solution/vitest.config.ts
L1/L1-P07/starter/README.md
L1/L1-P07/starter/babel.config.cjs
L1/L1-P07/starter/index.html
L1/L1-P07/starter/jest.config.cjs
L1/L1-P07/starter/package.json
L1/L1-P07/starter/src/App.tsx
L1/L1-P07/starter/src/components/ChartPanel.tsx
L1/L1-P07/starter/src/components/DataTable.tsx
L1/L1-P07/starter/src/data/members.json
L1/L1-P07/starter/src/lib/lib.ts
L1/L1-P07/starter/src/main.tsx
L1/L1-P07/starter/src/styles.css
L1/L1-P07/starter/tests/jest/spec.jest.test.ts
L1/L1-P07/starter/tests/setup.ts
L1/L1-P07/starter/tests/vitest/spec.test.ts
L1/L1-P07/starter/tsconfig.json
L1/L1-P07/starter/vite.config.ts
L1/L1-P07/starter/vitest.config.ts
L1/L1-P08/solution/README.md
L1/L1-P08/solution/babel.config.cjs
L1/L1-P08/solution/index.html
L1/L1-P08/solution/jest.config.cjs
L1/L1-P08/solution/package.json
L1/L1-P08/solution/src/App.tsx
L1/L1-P08/solution/src/components/ChartPanel.tsx
L1/L1-P08/solution/src/components/DataTable.tsx
L1/L1-P08/solution/src/data/members.json
L1/L1-P08/solution/src/lib/lib.ts
L1/L1-P08/solution/src/main.tsx
L1/L1-P08/solution/src/styles.css
L1/L1-P08/solution/tests/jest/spec.jest.test.ts
L1/L1-P08/solution/tests/setup.ts
L1/L1-P08/solution/tests/vitest/spec.test.ts
L1/L1-P08/solution/tsconfig.json
L1/L1-P08/solution/vite.config.ts
L1/L1-P08/solution/vitest.config.ts
L1/L1-P08/starter/README.md
L1/L1-P08/starter/babel.config.cjs
L1/L1-P08/starter/index.html
L1/L1-P08/starter/jest.config.cjs
L1/L1-P08/starter/package.json
L1/L1-P08/starter/src/App.tsx
L1/L1-P08/starter/src/components/ChartPanel.tsx
L1/L1-P08/starter/src/components/DataTable.tsx
L1/L1-P08/starter/src/data/members.json
L1/L1-P08/starter/src/lib/lib.ts
L1/L1-P08/starter/src/main.tsx
L1/L1-P08/starter/src/styles.css
L1/L1-P08/starter/tests/jest/spec.jest.test.ts
L1/L1-P08/starter/tests/setup.ts
L1/L1-P08/starter/tests/vitest/spec.test.ts
L1/L1-P08/starter/tsconfig.json
L1/L1-P08/starter/vite.config.ts
L1/L1-P08/starter/vitest.config.ts
L1/L1-P09/solution/README.md
L1/L1-P09/solution/babel.config.cjs
L1/L1-P09/solution/index.html
L1/L1-P09/solution/jest.config.cjs
L1/L1-P09/solution/package.json
L1/L1-P09/solution/src/App.tsx
L1/L1-P09/solution/src/components/ChartPanel.tsx
L1/L1-P09/solution/src/components/DataTable.tsx
L1/L1-P09/solution/src/data/members.json
L1/L1-P09/solution/src/lib/lib.ts
L1/L1-P09/solution/src/main.tsx
L1/L1-P09/solution/src/styles.css
L1/L1-P09/solution/tests/jest/spec.jest.test.ts
L1/L1-P09/solution/tests/setup.ts
L1/L1-P09/solution/tests/vitest/spec.test.ts
L1/L1-P09/solution/tsconfig.json
L1/L1-P09/solution/vite.config.ts
L1/L1-P09/solution/vitest.config.ts
L1/L1-P09/starter/README.md
L1/L1-P09/starter/babel.config.cjs
L1/L1-P09/starter/index.html
L1/L1-P09/starter/jest.config.cjs
L1/L1-P09/starter/package.json
L1/L1-P09/starter/src/App.tsx
L1/L1-P09/starter/src/components/ChartPanel.tsx
L1/L1-P09/starter/src/components/DataTable.tsx
L1/L1-P09/starter/src/data/members.json
L1/L1-P09/starter/src/lib/lib.ts
L1/L1-P09/starter/src/main.tsx
L1/L1-P09/starter/src/styles.css
L1/L1-P09/starter/tests/jest/spec.jest.test.ts
L1/L1-P09/starter/tests/setup.ts
L1/L1-P09/starter/tests/vitest/spec.test.ts
L1/L1-P09/starter/tsconfig.json
L1/L1-P09/starter/vite.config.ts
L1/L1-P09/starter/vitest.config.ts
L1/L1-P10/solution/README.md
L1/L1-P10/solution/babel.config.cjs
L1/L1-P10/solution/index.html
L1/L1-P10/solution/jest.config.cjs
L1/L1-P10/solution/package.json
L1/L1-P10/solution/src/App.tsx
L1/L1-P10/solution/src/components/ChartPanel.tsx
L1/L1-P10/solution/src/components/DataTable.tsx
L1/L1-P10/solution/src/data/members.json
L1/L1-P10/solution/src/lib/lib.ts
L1/L1-P10/solution/src/main.tsx
L1/L1-P10/solution/src/styles.css
L1/L1-P10/solution/tests/jest/spec.jest.test.ts
L1/L1-P10/solution/tests/setup.ts
L1/L1-P10/solution/tests/vitest/spec.test.ts
L1/L1-P10/solution/tsconfig.json
L1/L1-P10/solution/vite.config.ts
L1/L1-P10/solution/vitest.config.ts
L1/L1-P10/starter/README.md
L1/L1-P10/starter/babel.config.cjs
L1/L1-P10/starter/index.html
L1/L1-P10/starter/jest.config.cjs
L1/L1-P10/starter/package.json
L1/L1-P10/starter/src/App.tsx
L1/L1-P10/starter/src/components/ChartPanel.tsx
L1/L1-P10/starter/src/components/DataTable.tsx
L1/L1-P10/starter/src/data/members.json
L1/L1-P10/starter/src/lib/lib.ts
L1/L1-P10/starter/src/main.tsx
L1/L1-P10/starter/src/styles.css
L1/L1-P10/starter/tests/jest/spec.jest.test.ts
L1/L1-P10/starter/tests/setup.ts
L1/L1-P10/starter/tests/vitest/spec.test.ts
L1/L1-P10/starter/tsconfig.json
L1/L1-P10/starter/vite.config.ts
L1/L1-P10/starter/vitest.config.ts
L1/L1-P11/solution/README.md
L1/L1-P11/solution/babel.config.cjs
L1/L1-P11/solution/index.html
L1/L1-P11/solution/jest.config.cjs
L1/L1-P11/solution/package.json
L1/L1-P11/solution/src/App.tsx
L1/L1-P11/solution/src/components/ChartPanel.tsx
L1/L1-P11/solution/src/components/DataTable.tsx
L1/L1-P11/solution/src/data/members.json
L1/L1-P11/solution/src/lib/lib.ts
L1/L1-P11/solution/src/main.tsx
L1/L1-P11/solution/src/styles.css
L1/L1-P11/solution/tests/jest/spec.jest.test.ts
L1/L1-P11/solution/tests/setup.ts
L1/L1-P11/solution/tests/vitest/spec.test.ts
L1/L1-P11/solution/tsconfig.json
L1/L1-P11/solution/vite.config.ts
L1/L1-P11/solution/vitest.config.ts
L1/L1-P11/starter/README.md
L1/L1-P11/starter/babel.config.cjs
L1/L1-P11/starter/index.html
L1/L1-P11/starter/jest.config.cjs
L1/L1-P11/starter/package.json
L1/L1-P11/starter/src/App.tsx
L1/L1-P11/starter/src/components/ChartPanel.tsx
L1/L1-P11/starter/src/components/DataTable.tsx
L1/L1-P11/starter/src/data/members.json
L1/L1-P11/starter/src/lib/lib.ts
L1/L1-P11/starter/src/main.tsx
L1/L1-P11/starter/src/styles.css
L1/L1-P11/starter/tests/jest/spec.jest.test.ts
L1/L1-P11/starter/tests/setup.ts
L1/L1-P11/starter/tests/vitest/spec.test.ts
L1/L1-P11/starter/tsconfig.json
L1/L1-P11/starter/vite.config.ts
L1/L1-P11/starter/vitest.config.ts
L1/L1-P12/solution/README.md
L1/L1-P12/solution/babel.config.cjs
L1/L1-P12/solution/index.html
L1/L1-P12/solution/jest.config.cjs
L1/L1-P12/solution/package.json
L1/L1-P12/solution/src/App.tsx
L1/L1-P12/solution/src/components/ChartPanel.tsx
L1/L1-P12/solution/src/components/DataTable.tsx
L1/L1-P12/solution/src/data/members.json
L1/L1-P12/solution/src/lib/lib.ts
L1/L1-P12/solution/src/main.tsx
L1/L1-P12/solution/src/styles.css
L1/L1-P12/solution/tests/jest/spec.jest.test.ts
L1/L1-P12/solution/tests/setup.ts
L1/L1-P12/solution/tests/vitest/spec.test.ts
L1/L1-P12/solution/tsconfig.json
L1/L1-P12/solution/vite.config.ts
L1/L1-P12/solution/vitest.config.ts
L1/L1-P12/starter/README.md
L1/L1-P12/starter/babel.config.cjs
L1/L1-P12/starter/index.html
L1/L1-P12/starter/jest.config.cjs
L1/L1-P12/starter/package.json
L1/L1-P12/starter/src/App.tsx
L1/L1-P12/starter/src/components/ChartPanel.tsx
L1/L1-P12/starter/src/components/DataTable.tsx
L1/L1-P12/starter/src/data/members.json
L1/L1-P12/starter/src/lib/lib.ts
L1/L1-P12/starter/src/main.tsx
L1/L1-P12/starter/src/styles.css
L1/L1-P12/starter/tests/jest/spec.jest.test.ts
L1/L1-P12/starter/tests/setup.ts
L1/L1-P12/starter/tests/vitest/spec.test.ts
L1/L1-P12/starter/tsconfig.json
L1/L1-P12/starter/vite.config.ts
L1/L1-P12/starter/vitest.config.ts
L1/L1-P13/solution/README.md
L1/L1-P13/solution/babel.config.cjs
L1/L1-P13/solution/index.html
L1/L1-P13/solution/jest.config.cjs
L1/L1-P13/solution/package.json
L1/L1-P13/solution/src/App.tsx
L1/L1-P13/solution/src/components/ChartPanel.tsx
L1/L1-P13/solution/src/components/DataTable.tsx
L1/L1-P13/solution/src/data/members.json
L1/L1-P13/solution/src/lib/lib.ts
L1/L1-P13/solution/src/main.tsx
L1/L1-P13/solution/src/styles.css
L1/L1-P13/solution/tests/jest/spec.jest.test.ts
L1/L1-P13/solution/tests/setup.ts
L1/L1-P13/solution/tests/vitest/spec.test.ts
L1/L1-P13/solution/tsconfig.json
L1/L1-P13/solution/vite.config.ts
L1/L1-P13/solution/vitest.config.ts
L1/L1-P13/starter/README.md
L1/L1-P13/starter/babel.config.cjs
L1/L1-P13/starter/index.html
L1/L1-P13/starter/jest.config.cjs
L1/L1-P13/starter/package.json
L1/L1-P13/starter/src/App.tsx
L1/L1-P13/starter/src/components/ChartPanel.tsx
L1/L1-P13/starter/src/components/DataTable.tsx
L1/L1-P13/starter/src/data/members.json
L1/L1-P13/starter/src/lib/lib.ts
L1/L1-P13/starter/src/main.tsx
L1/L1-P13/starter/src/styles.css
L1/L1-P13/starter/tests/jest/spec.jest.test.ts
L1/L1-P13/starter/tests/setup.ts
L1/L1-P13/starter/tests/vitest/spec.test.ts
L1/L1-P13/starter/tsconfig.json
L1/L1-P13/starter/vite.config.ts
L1/L1-P13/starter/vitest.config.ts
L1/L1-P14/solution/README.md
L1/L1-P14/solution/babel.config.cjs
L1/L1-P14/solution/index.html
L1/L1-P14/solution/jest.config.cjs
L1/L1-P14/solution/package.json
L1/L1-P14/solution/src/App.tsx
L1/L1-P14/solution/src/components/ChartPanel.tsx
L1/L1-P14/solution/src/components/DataTable.tsx
L1/L1-P14/solution/src/data/members.json
L1/L1-P14/solution/src/lib/lib.ts
L1/L1-P14/solution/src/main.tsx
L1/L1-P14/solution/src/styles.css
L1/L1-P14/solution/tests/jest/spec.jest.test.ts
L1/L1-P14/solution/tests/setup.ts
L1/L1-P14/solution/tests/vitest/spec.test.ts
L1/L1-P14/solution/tsconfig.json
L1/L1-P14/solution/vite.config.ts
L1/L1-P14/solution/vitest.config.ts
L1/L1-P14/starter/README.md
L1/L1-P14/starter/babel.config.cjs
L1/L1-P14/starter/index.html
L1/L1-P14/starter/jest.config.cjs
L1/L1-P14/starter/package.json
L1/L1-P14/starter/src/App.tsx
L1/L1-P14/starter/src/components/ChartPanel.tsx
L1/L1-P14/starter/src/components/DataTable.tsx
L1/L1-P14/starter/src/data/members.json
L1/L1-P14/starter/src/lib/lib.ts
L1/L1-P14/starter/src/main.tsx
L1/L1-P14/starter/src/styles.css
L1/L1-P14/starter/tests/jest/spec.jest.test.ts
L1/L1-P14/starter/tests/setup.ts
…
L3/L3-P02/solution/package.json
L3/L3-P02/solution/src/App.tsx
L3/L3-P02/solution/src/components/ChartPanel.tsx
L3/L3-P02/solution/src/components/DataTable.tsx
L3/L3-P02/solution/src/data/members.json
L3/L3-P02/solution/src/lib/lib.ts
L3/L3-P02/solution/src/main.tsx
L3/L3-P02/solution/src/styles.css
L3/L3-P02/solution/tests/jest/spec.jest.test.ts
L3/L3-P02/solution/tests/setup.ts
L3/L3-P02/solution/tests/vitest/spec.test.ts
L3/L3-P02/solution/tsconfig.json
L3/L3-P02/solution/vite.config.ts
L3/L3-P02/solution/vitest.config.ts
L3/L3-P02/starter/README.md
L3/L3-P02/starter/babel.config.cjs
L3/L3-P02/starter/index.html
L3/L3-P02/starter/jest.config.cjs
L3/L3-P02/starter/package.json
L3/L3-P02/starter/src/App.tsx
L3/L3-P02/starter/src/components/ChartPanel.tsx
L3/L3-P02/starter/src/components/DataTable.tsx
L3/L3-P02/starter/src/data/members.json
L3/L3-P02/starter/src/lib/lib.ts
L3/L3-P02/starter/src/main.tsx
L3/L3-P02/starter/src/styles.css
L3/L3-P02/starter/tests/jest/spec.jest.test.ts
L3/L3-P02/starter/tests/setup.ts
L3/L3-P02/starter/tests/vitest/spec.test.ts
L3/L3-P02/starter/tsconfig.json
L3/L3-P02/starter/vite.config.ts
L3/L3-P02/starter/vitest.config.ts
L3/L3-P03/solution/README.md
L3/L3-P03/solution/babel.config.cjs
L3/L3-P03/solution/index.html
L3/L3-P03/solution/jest.config.cjs
L3/L3-P03/solution/package.json
L3/L3-P03/solution/src/App.tsx
L3/L3-P03/solution/src/components/ChartPanel.tsx
L3/L3-P03/solution/src/components/DataTable.tsx
L3/L3-P03/solution/src/data/members.json
L3/L3-P03/solution/src/lib/lib.ts
L3/L3-P03/solution/src/main.tsx
L3/L3-P03/solution/src/styles.css
L3/L3-P03/solution/tests/jest/spec.jest.test.ts
L3/L3-P03/solution/tests/setup.ts
L3/L3-P03/solution/tests/vitest/spec.test.ts
L3/L3-P03/solution/tsconfig.json
L3/L3-P03/solution/vite.config.ts
L3/L3-P03/solution/vitest.config.ts
L3/L3-P03/starter/README.md
L3/L3-P03/starter/babel.config.cjs
L3/L3-P03/starter/index.html
L3/L3-P03/starter/jest.config.cjs
L3/L3-P03/starter/package.json
L3/L3-P03/starter/src/App.tsx
L3/L3-P03/starter/src/components/ChartPanel.tsx
L3/L3-P03/starter/src/components/DataTable.tsx
L3/L3-P03/starter/src/data/members.json
L3/L3-P03/starter/src/lib/lib.ts
L3/L3-P03/starter/src/main.tsx
L3/L3-P03/starter/src/styles.css
L3/L3-P03/starter/tests/jest/spec.jest.test.ts
L3/L3-P03/starter/tests/setup.ts
L3/L3-P03/starter/tests/vitest/spec.test.ts
L3/L3-P03/starter/tsconfig.json
L3/L3-P03/starter/vite.config.ts
L3/L3-P03/starter/vitest.config.ts
L3/L3-P04/solution/README.md
L3/L3-P04/solution/babel.config.cjs
L3/L3-P04/solution/index.html
L3/L3-P04/solution/jest.config.cjs
L3/L3-P04/solution/package.json
L3/L3-P04/solution/src/App.tsx
L3/L3-P04/solution/src/components/ChartPanel.tsx
L3/L3-P04/solution/src/components/DataTable.tsx
L3/L3-P04/solution/src/data/members.json
L3/L3-P04/solution/src/lib/lib.ts
L3/L3-P04/solution/src/main.tsx
L3/L3-P04/solution/src/styles.css
L3/L3-P04/solution/tests/jest/spec.jest.test.ts
L3/L3-P04/solution/tests/setup.ts
L3/L3-P04/solution/tests/vitest/spec.test.ts
L3/L3-P04/solution/tsconfig.json
L3/L3-P04/solution/vite.config.ts
L3/L3-P04/solution/vitest.config.ts
L3/L3-P04/starter/README.md
L3/L3-P04/starter/babel.config.cjs
L3/L3-P04/starter/index.html
L3/L3-P04/starter/jest.config.cjs
L3/L3-P04/starter/package.json
L3/L3-P04/starter/src/App.tsx
L3/L3-P04/starter/src/components/ChartPanel.tsx
L3/L3-P04/starter/src/components/DataTable.tsx
L3/L3-P04/starter/src/data/members.json
L3/L3-P04/starter/src/lib/lib.ts
L3/L3-P04/starter/src/main.tsx
L3/L3-P04/starter/src/styles.css
L3/L3-P04/starter/tests/jest/spec.jest.test.ts
L3/L3-P04/starter/tests/setup.ts
L3/L3-P04/starter/tests/vitest/spec.test.ts
L3/L3-P04/starter/tsconfig.json
L3/L3-P04/starter/vite.config.ts
L3/L3-P04/starter/vitest.config.ts
L3/L3-P05/solution/README.md
L3/L3-P05/solution/babel.config.cjs
L3/L3-P05/solution/index.html
L3/L3-P05/solution/jest.config.cjs
L3/L3-P05/solution/package.json
L3/L3-P05/solution/src/App.tsx
L3/L3-P05/solution/src/components/ChartPanel.tsx
L3/L3-P05/solution/src/components/DataTable.tsx
L3/L3-P05/solution/src/data/members.json
L3/L3-P05/solution/src/lib/lib.ts
L3/L3-P05/solution/src/main.tsx
L3/L3-P05/solution/src/styles.css
L3/L3-P05/solution/tests/jest/spec.jest.test.ts
L3/L3-P05/solution/tests/setup.ts
L3/L3-P05/solution/tests/vitest/spec.test.ts
L3/L3-P05/solution/tsconfig.json
L3/L3-P05/solution/vite.config.ts
L3/L3-P05/solution/vitest.config.ts
L3/L3-P05/starter/README.md
L3/L3-P05/starter/babel.config.cjs
L3/L3-P05/starter/index.html
L3/L3-P05/starter/jest.config.cjs
L3/L3-P05/starter/package.json
L3/L3-P05/starter/src/App.tsx
L3/L3-P05/starter/src/components/ChartPanel.tsx
L3/L3-P05/starter/src/components/DataTable.tsx
L3/L3-P05/starter/src/data/members.json
L3/L3-P05/starter/src/lib/lib.ts
L3/L3-P05/starter/src/main.tsx
L3/L3-P05/starter/src/styles.css
L3/L3-P05/starter/tests/jest/spec.jest.test.ts
L3/L3-P05/starter/tests/setup.ts
L3/L3-P05/starter/tests/vitest/spec.test.ts
L3/L3-P05/starter/tsconfig.json
L3/L3-P05/starter/vite.config.ts
L3/L3-P05/starter/vitest.config.ts
L3/L3-P06/solution/README.md
L3/L3-P06/solution/babel.config.cjs
L3/L3-P06/solution/index.html
L3/L3-P06/solution/jest.config.cjs
L3/L3-P06/solution/package.json
L3/L3-P06/solution/src/App.tsx
L3/L3-P06/solution/src/components/ChartPanel.tsx
L3/L3-P06/solution/src/components/DataTable.tsx
L3/L3-P06/solution/src/data/members.json
L3/L3-P06/solution/src/lib/lib.ts
L3/L3-P06/solution/src/main.tsx
L3/L3-P06/solution/src/styles.css
L3/L3-P06/solution/tests/jest/spec.jest.test.ts
L3/L3-P06/solution/tests/setup.ts
L3/L3-P06/solution/tests/vitest/spec.test.ts
L3/L3-P06/solution/tsconfig.json
L3/L3-P06/solution/vite.config.ts
L3/L3-P06/solution/vitest.config.ts
L3/L3-P06/starter/README.md
L3/L3-P06/starter/babel.config.cjs
L3/L3-P06/starter/index.html
L3/L3-P06/starter/jest.config.cjs
L3/L3-P06/starter/package.json
L3/L3-P06/starter/src/App.tsx
L3/L3-P06/starter/src/components/ChartPanel.tsx
L3/L3-P06/starter/src/components/DataTable.tsx
L3/L3-P06/starter/src/data/members.json
L3/L3-P06/starter/src/lib/lib.ts
L3/L3-P06/starter/src/main.tsx
L3/L3-P06/starter/src/styles.css
L3/L3-P06/starter/tests/jest/spec.jest.test.ts
L3/L3-P06/starter/tests/setup.ts
L3/L3-P06/starter/tests/vitest/spec.test.ts
L3/L3-P06/starter/tsconfig.json
L3/L3-P06/starter/vite.config.ts
L3/L3-P06/starter/vitest.config.ts
L3/L3-P07/solution/README.md
L3/L3-P07/solution/babel.config.cjs
L3/L3-P07/solution/index.html
L3/L3-P07/solution/jest.config.cjs
L3/L3-P07/solution/package.json
L3/L3-P07/solution/src/App.tsx
L3/L3-P07/solution/src/components/ChartPanel.tsx
L3/L3-P07/solution/src/components/DataTable.tsx
L3/L3-P07/solution/src/data/members.json
L3/L3-P07/solution/src/lib/lib.ts
L3/L3-P07/solution/src/main.tsx
L3/L3-P07/solution/src/styles.css
L3/L3-P07/solution/tests/jest/spec.jest.test.ts
L3/L3-P07/solution/tests/setup.ts
L3/L3-P07/solution/tests/vitest/spec.test.ts
L3/L3-P07/solution/tsconfig.json
L3/L3-P07/solution/vite.config.ts
L3/L3-P07/solution/vitest.config.ts
L3/L3-P07/starter/README.md
L3/L3-P07/starter/babel.config.cjs
L3/L3-P07/starter/index.html
L3/L3-P07/starter/jest.config.cjs
L3/L3-P07/starter/package.json
L3/L3-P07/starter/src/App.tsx
L3/L3-P07/starter/src/components/ChartPanel.tsx
L3/L3-P07/starter/src/components/DataTable.tsx
L3/L3-P07/starter/src/data/members.json
L3/L3-P07/starter/src/lib/lib.ts
L3/L3-P07/starter/src/main.tsx
L3/L3-P07/starter/src/styles.css
L3/L3-P07/starter/tests/jest/spec.jest.test.ts
L3/L3-P07/starter/tests/setup.ts
L3/L3-P07/starter/tests/vitest/spec.test.ts
L3/L3-P07/starter/tsconfig.json
L3/L3-P07/starter/vite.config.ts
L3/L3-P07/starter/vitest.config.ts
L3/L3-P08/solution/README.md
L3/L3-P08/solution/babel.config.cjs
L3/L3-P08/solution/index.html
L3/L3-P08/solution/jest.config.cjs
L3/L3-P08/solution/package.json
L3/L3-P08/solution/src/App.tsx
L3/L3-P08/solution/src/components/ChartPanel.tsx
L3/L3-P08/solution/src/components/DataTable.tsx
L3/L3-P08/solution/src/data/members.json
L3/L3-P08/solution/src/lib/lib.ts
L3/L3-P08/solution/src/main.tsx
L3/L3-P08/solution/src/styles.css
L3/L3-P08/solution/tests/jest/spec.jest.test.ts
L3/L3-P08/solution/tests/setup.ts
L3/L3-P08/solution/tests/vitest/spec.test.ts
L3/L3-P08/solution/tsconfig.json
L3/L3-P08/solution/vite.config.ts
L3/L3-P08/solution/vitest.config.ts
L3/L3-P08/starter/README.md
L3/L3-P08/starter/babel.config.cjs
L3/L3-P08/starter/index.html
L3/L3-P08/starter/jest.config.cjs
L3/L3-P08/starter/package.json
L3/L3-P08/starter/src/App.tsx
L3/L3-P08/starter/src/components/ChartPanel.tsx
L3/L3-P08/starter/src/components/DataTable.tsx
L3/L3-P08/starter/src/data/members.json
L3/L3-P08/starter/src/lib/lib.ts
L3/L3-P08/starter/src/main.tsx
L3/L3-P08/starter/src/styles.css
L3/L3-P08/starter/tests/jest/spec.jest.test.ts
L3/L3-P08/starter/tests/setup.ts
L3/L3-P08/starter/tests/vitest/spec.test.ts
L3/L3-P08/starter/tsconfig.json
L3/L3-P08/starter/vite.config.ts
L3/L3-P08/starter/vitest.config.ts
L3/L3-P09/solution/README.md
L3/L3-P09/solution/babel.config.cjs
L3/L3-P09/solution/index.html
L3/L3-P09/solution/jest.config.cjs
L3/L3-P09/solution/package.json
L3/L3-P09/solution/src/App.tsx
L3/L3-P09/solution/src/components/ChartPanel.tsx
L3/L3-P09/solution/src/components/DataTable.tsx
L3/L3-P09/solution/src/data/members.json
L3/L3-P09/solution/src/lib/lib.ts
L3/L3-P09/solution/src/main.tsx
L3/L3-P09/solution/src/styles.css
L3/L3-P09/solution/tests/jest/spec.jest.test.ts
L3/L3-P09/solution/tests/setup.ts
L3/L3-P09/solution/tests/vitest/spec.test.ts
L3/L3-P09/solution/tsconfig.json
L3/L3-P09/solution/vite.config.ts
L3/L3-P09/solution/vitest.config.ts
L3/L3-P09/starter/README.md
L3/L3-P09/starter/babel.config.cjs
L3/L3-P09/starter/index.html
L3/L3-P09/starter/jest.config.cjs
L3/L3-P09/starter/package.json
L3/L3-P09/starter/src/App.tsx
L3/L3-P09/starter/src/components/ChartPanel.tsx
L3/L3-P09/starter/src/components/DataTable.tsx
L3/L3-P09/starter/src/data/members.json
L3/L3-P09/starter/src/lib/lib.ts
L3/L3-P09/starter/src/main.tsx
L3/L3-P09/starter/src/styles.css
L3/L3-P09/starter/tests/jest/spec.jest.test.ts
L3/L3-P09/starter/tests/setup.ts
L3/L3-P09/starter/tests/vitest/spec.test.ts
L3/L3-P09/starter/tsconfig.json
L3/L3-P09/starter/vite.config.ts
L3/L3-P09/starter/vitest.config.ts
L3/L3-P10/solution/README.md
L3/L3-P10/solution/babel.config.cjs
L3/L3-P10/solution/index.html
L3/L3-P10/solution/jest.config.cjs
L3/L3-P10/solution/package.json
L3/L3-P10/solution/src/App.tsx
L3/L3-P10/solution/src/components/ChartPanel.tsx
L3/L3-P10/solution/src/components/DataTable.tsx
L3/L3-P10/solution/src/data/members.json
L3/L3-P10/solution/src/lib/lib.ts
L3/L3-P10/solution/src/main.tsx
L3/L3-P10/solution/src/styles.css
L3/L3-P10/solution/tests/jest/spec.jest.test.ts
L3/L3-P10/solution/tests/setup.ts
L3/L3-P10/solution/tests/vitest/spec.test.ts
L3/L3-P10/solution/tsconfig.json
L3/L3-P10/solution/vite.config.ts
L3/L3-P10/solution/vitest.config.ts
L3/L3-P10/starter/README.md
L3/L3-P10/starter/babel.config.cjs
L3/L3-P10/starter/index.html
L3/L3-P10/starter/jest.config.cjs
L3/L3-P10/starter/package.json
L3/L3-P10/starter/src/App.tsx
L3/L3-P10/starter/src/components/ChartPanel.tsx
L3/L3-P10/starter/src/components/DataTable.tsx
L3/L3-P10/starter/src/data/members.json
L3/L3-P10/starter/src/lib/lib.ts
L3/L3-P10/starter/src/main.tsx
L3/L3-P10/starter/src/styles.css
L3/L3-P10/starter/tests/jest/spec.jest.test.ts
L3/L3-P10/starter/tests/setup.ts
L3/L3-P10/starter/tests/vitest/spec.test.ts
L3/L3-P10/starter/tsconfig.json
L3/L3-P10/starter/vite.config.ts
L3/L3-P10/starter/vitest.config.ts
L3/L3-P11/solution/README.md
L3/L3-P11/solution/babel.config.cjs
L3/L3-P11/solution/index.html
L3/L3-P11/solution/jest.config.cjs
L3/L3-P11/solution/package.json
L3/L3-P11/solution/src/App.tsx
L3/L3-P11/solution/src/components/ChartPanel.tsx
L3/L3-P11/solution/src/components/DataTable.tsx
L3/L3-P11/solution/src/data/members.json
L3/L3-P11/solution/src/lib/lib.ts
L3/L3-P11/solution/src/main.tsx
L3/L3-P11/solution/src/styles.css
L3/L3-P11/solution/tests/jest/spec.jest.test.ts
L3/L3-P11/solution/tests/setup.ts
L3/L3-P11/solution/tests/vitest/spec.test.ts
L3/L3-P11/solution/tsconfig.json
L3/L3-P11/solution/vite.config.ts
L3/L3-P11/solution/vitest.config.ts
L3/L3-P11/starter/README.md
L3/L3-P11/starter/babel.config.cjs
L3/L3-P11/starter/index.html
L3/L3-P11/starter/jest.config.cjs
L3/L3-P11/starter/package.json
L3/L3-P11/starter/src/App.tsx
L3/L3-P11/starter/src/components/ChartPanel.tsx
L3/L3-P11/starter/src/components/DataTable.tsx
L3/L3-P11/starter/src/data/members.json
L3/L3-P11/starter/src/lib/lib.ts
L3/L3-P11/starter/src/main.tsx
L3/L3-P11/starter/src/styles.css
L3/L3-P11/starter/tests/jest/spec.jest.test.ts
L3/L3-P11/starter/tests/setup.ts
L3/L3-P11/starter/tests/vitest/spec.test.ts
L3/L3-P11/starter/tsconfig.json
L3/L3-P11/starter/vite.config.ts
L3/L3-P11/starter/vitest.config.ts
L3/L3-P12/solution/README.md
L3/L3-P12/solution/babel.config.cjs
L3/L3-P12/solution/index.html
L3/L3-P12/solution/jest.config.cjs
L3/L3-P12/solution/package.json
L3/L3-P12/solution/src/App.tsx
L3/L3-P12/solution/src/components/ChartPanel.tsx
L3/L3-P12/solution/src/components/DataTable.tsx
L3/L3-P12/solution/src/data/members.json
L3/L3-P12/solution/src/lib/lib.ts
L3/L3-P12/solution/src/main.tsx
L3/L3-P12/solution/src/styles.css
L3/L3-P12/solution/tests/jest/spec.jest.test.ts
L3/L3-P12/solution/tests/setup.ts
L3/L3-P12/solution/tests/vitest/spec.test.ts
L3/L3-P12/solution/tsconfig.json
L3/L3-P12/solution/vite.config.ts
L3/L3-P12/solution/vitest.config.ts
L3/L3-P12/starter/README.md
L3/L3-P12/starter/babel.config.cjs
L3/L3-P12/starter/index.html
L3/L3-P12/starter/jest.config.cjs
L3/L3-P12/starter/package.json
L3/L3-P12/starter/src/App.tsx
L3/L3-P12/starter/src/components/ChartPanel.tsx
L3/L3-P12/starter/src/components/DataTable.tsx
L3/L3-P12/starter/src/data/members.json
L3/L3-P12/starter/src/lib/lib.ts
L3/L3-P12/starter/src/main.tsx
L3/L3-P12/starter/src/styles.css
L3/L3-P12/starter/tests/jest/spec.jest.test.ts
L3/L3-P12/starter/tests/setup.ts
L3/L3-P12/starter/tests/vitest/spec.test.ts
L3/L3-P12/starter/tsconfig.json
L3/L3-P12/starter/vite.config.ts
L3/L3-P12/starter/vitest.config.ts
L3/L3-P13/solution/README.md
L3/L3-P13/solution/babel.config.cjs
L3/L3-P13/solution/index.html
L3/L3-P13/solution/jest.config.cjs
L3/L3-P13/solution/package.json
L3/L3-P13/solution/src/App.tsx
L3/L3-P13/solution/src/components/ChartPanel.tsx
L3/L3-P13/solution/src/components/DataTable.tsx
L3/L3-P13/solution/src/data/members.json
L3/L3-P13/solution/src/lib/lib.ts
L3/L3-P13/solution/src/main.tsx
L3/L3-P13/solution/src/styles.css
L3/L3-P13/solution/tests/jest/spec.jest.test.ts
L3/L3-P13/solution/tests/setup.ts
L3/L3-P13/solution/tests/vitest/spec.test.ts
L3/L3-P13/solution/tsconfig.json
L3/L3-P13/solution/vite.config.ts
L3/L3-P13/solution/vitest.config.ts
L3/L3-P13/starter/README.md
L3/L3-P13/starter/babel.config.cjs
L3/L3-P13/starter/index.html
L3/L3-P13/starter/jest.config.cjs
L3/L3-P13/starter/package.json
L3/L3-P13/starter/src/App.tsx
L3/L3-P13/starter/src/components/ChartPanel.tsx
L3/L3-P13/starter/src/components/DataTable.tsx
L3/L3-P13/starter/src/data/members.json
L3/L3-P13/starter/src/lib/lib.ts
L3/L3-P13/starter/src/main.tsx
L3/L3-P13/starter/src/styles.css
L3/L3-P13/starter/tests/jest/spec.jest.test.ts
L3/L3-P13/starter/tests/setup.ts
L3/L3-P13/starter/tests/vitest/spec.test.ts
L3/L3-P13/starter/tsconfig.json
L3/L3-P13/starter/vite.config.ts
L3/L3-P13/starter/vitest.config.ts
L3/L3-P14/solution/README.md
L3/L3-P14/solution/babel.config.cjs
L3/L3-P14/solution/index.html
L3/L3-P14/solution/jest.config.cjs
L3/L3-P14/solution/package.json
L3/L3-P14/solution/src/App.tsx
L3/L3-P14/solution/src/components/ChartPanel.tsx
L3/L3-P14/solution/src/components/DataTable.tsx
L3/L3-P14/solution/src/data/members.json
L3/L3-P14/solution/src/lib/lib.ts
L3/L3-P14/solution/src/main.tsx
L3/L3-P14/solution/src/styles.css
L3/L3-P14/solution/tests/jest/spec.jest.test.ts
L3/L3-P14/solution/tests/setup.ts
L3/L3-P14/solution/tests/vitest/spec.test.ts
L3/L3-P14/solution/tsconfig.json
L3/L3-P14/solution/vite.config.ts
L3/L3-P14/solution/vitest.config.ts
L3/L3-P14/starter/README.md
L3/L3-P14/starter/babel.config.cjs
L3/L3-P14/starter/index.html
L3/L3-P14/starter/jest.config.cjs
L3/L3-P14/starter/package.json
L3/L3-P14/starter/src/App.tsx
L3/L3-P14/starter/src/components/ChartPanel.tsx
L3/L3-P14/starter/src/components/DataTable.tsx
L3/L3-P14/starter/src/data/members.json
L3/L3-P14/starter/src/lib/lib.ts
L3/L3-P14/starter/src/main.tsx
L3/L3-P14/starter/src/styles.css
L3/L3-P14/starter/tests/jest/spec.jest.test.ts
L3/L3-P14/starter/tests/setup.ts
L3/L3-P14/starter/tests/vitest/spec.test.ts
L3/L3-P14/starter/tsconfig.json
L3/L3-P14/starter/vite.config.ts
L3/L3-P14/starter/vitest.config.ts
L3/L3-P15/solution/README.md
L3/L3-P15/solution/babel.config.cjs
L3/L3-P15/solution/index.html
L3/L3-P15/solution/jest.config.cjs
L3/L3-P15/solution/package.json
L3/L3-P15/solution/src/App.tsx
L3/L3-P15/solution/src/components/ChartPanel.tsx
L3/L3-P15/solution/src/components/DataTable.tsx
L3/L3-P15/solution/src/data/members.json
L3/L3-P15/solution/src/lib/lib.ts
L3/L3-P15/solution/src/main.tsx
L3/L3-P15/solution/src/styles.css
L3/L3-P15/solution/tests/jest/spec.jest.test.ts
L3/L3-P15/solution/tests/setup.ts
L3/L3-P15/solution/tests/vitest/spec.test.ts
L3/L3-P15/solution/tsconfig.json
L3/L3-P15/solution/vite.config.ts
L3/L3-P15/solution/vitest.config.ts
L3/L3-P15/starter/README.md
L3/L3-P15/starter/babel.config.cjs
L3/L3-P15/starter/index.html
L3/L3-P15/starter/jest.config.cjs
L3/L3-P15/starter/package.json
L3/L3-P15/starter/src/App.tsx
L3/L3-P15/starter/src/components/ChartPanel.tsx
L3/L3-P15/starter/src/components/DataTable.tsx
L3/L3-P15/starter/src/data/members.json
L3/L3-P15/starter/src/lib/lib.ts
L3/L3-P15/starter/src/main.tsx
L3/L3-P15/starter/src/styles.css
L3/L3-P15/starter/tests/jest/spec.jest.test.ts
L3/L3-P15/starter/tests/setup.ts
L3/L3-P15/starter/tests/vitest/spec.test.ts
L3/L3-P15/starter/tsconfig.json
L3/L3-P15/starter/vite.config.ts
L3/L3-P15/starter/vitest.config.ts
```

**Variante detectate:** solution: 810, starter: 810.

**Categorii de fișiere:** config: 540, other: 90, docs: 90, code: 630, tests: 270.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `L1/L1-P01/starter/package.json`: name=`l1-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P01/solution/package.json`: name=`l1-p01-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P02/starter/package.json`: name=`l1-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P02/solution/package.json`: name=`l1-p02-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P03/starter/package.json`: name=`l1-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P03/solution/package.json`: name=`l1-p03-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P04/starter/package.json`: name=`l1-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P04/solution/package.json`: name=`l1-p04-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P05/starter/package.json`: name=`l1-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P05/solution/package.json`: name=`l1-p05-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P06/starter/package.json`: name=`l1-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P06/solution/package.json`: name=`l1-p06-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P07/starter/package.json`: name=`l1-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P07/solution/package.json`: name=`l1-p07-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P08/starter/package.json`: name=`l1-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P08/solution/package.json`: name=`l1-p08-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P09/starter/package.json`: name=`l1-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P09/solution/package.json`: name=`l1-p09-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P10/starter/package.json`: name=`l1-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P10/solution/package.json`: name=`l1-p10-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P11/starter/package.json`: name=`l1-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P11/solution/package.json`: name=`l1-p11-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P12/starter/package.json`: name=`l1-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P12/solution/package.json`: name=`l1-p12-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P13/starter/package.json`: name=`l1-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P13/solution/package.json`: name=`l1-p13-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P14/starter/package.json`: name=`l1-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P14/solution/package.json`: name=`l1-p14-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P15/starter/package.json`: name=`l1-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P15/solution/package.json`: name=`l1-p15-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P01/starter/package.json`: name=`l2-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P01/solution/package.json`: name=`l2-p01-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P02/starter/package.json`: name=`l2-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P02/solution/package.json`: name=`l2-p02-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P03/starter/package.json`: name=`l2-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P03/solution/package.json`: name=`l2-p03-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P04/starter/package.json`: name=`l2-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P04/solution/package.json`: name=`l2-p04-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P05/starter/package.json`: name=`l2-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P05/solution/package.json`: name=`l2-p05-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P06/starter/package.json`: name=`l2-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P06/solution/package.json`: name=`l2-p06-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P07/starter/package.json`: name=`l2-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P07/solution/package.json`: name=`l2-p07-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P08/starter/package.json`: name=`l2-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P08/solution/package.json`: name=`l2-p08-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P09/starter/package.json`: name=`l2-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P09/solution/package.json`: name=`l2-p09-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P10/starter/package.json`: name=`l2-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P10/solution/package.json`: name=`l2-p10-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P11/starter/package.json`: name=`l2-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P11/solution/package.json`: name=`l2-p11-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P12/starter/package.json`: name=`l2-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P12/solution/package.json`: name=`l2-p12-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P13/starter/package.json`: name=`l2-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P13/solution/package.json`: name=`l2-p13-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P14/starter/package.json`: name=`l2-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P14/solution/package.json`: name=`l2-p14-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P15/starter/package.json`: name=`l2-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P15/solution/package.json`: name=`l2-p15-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P01/starter/package.json`: name=`l3-p01-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P01/solution/package.json`: name=`l3-p01-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P02/starter/package.json`: name=`l3-p02-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P02/solution/package.json`: name=`l3-p02-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P03/starter/package.json`: name=`l3-p03-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P03/solution/package.json`: name=`l3-p03-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P04/starter/package.json`: name=`l3-p04-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P04/solution/package.json`: name=`l3-p04-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P05/starter/package.json`: name=`l3-p05-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P05/solution/package.json`: name=`l3-p05-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P06/starter/package.json`: name=`l3-p06-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P06/solution/package.json`: name=`l3-p06-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P07/starter/package.json`: name=`l3-p07-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P07/solution/package.json`: name=`l3-p07-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P08/starter/package.json`: name=`l3-p08-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P08/solution/package.json`: name=`l3-p08-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P09/starter/package.json`: name=`l3-p09-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P09/solution/package.json`: name=`l3-p09-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P10/starter/package.json`: name=`l3-p10-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P10/solution/package.json`: name=`l3-p10-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P11/starter/package.json`: name=`l3-p11-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P11/solution/package.json`: name=`l3-p11-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P12/starter/package.json`: name=`l3-p12-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P12/solution/package.json`: name=`l3-p12-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P13/starter/package.json`: name=`l3-p13-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P13/solution/package.json`: name=`l3-p13-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P14/starter/package.json`: name=`l3-p14-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P14/solution/package.json`: name=`l3-p14-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P15/starter/package.json`: name=`l3-p15-starter` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P15/solution/package.json`: name=`l3-p15-solution` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom, @tanstack/react-table, chart.js
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest

### Seminar12_Partea3_p3-READMEs.zip

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

### Seminar12_Partea1_Teorie_Tabele_si_Grafice_extins.docx

**Titluri/Heading-uri:**

- Seminarul 12 — Componente externe: tabele și grafice
Partea 1 — Teorie extinsă (narativ + exemple)
- HOOK (poveste realistă): „ClubHub+ Analytics”. După ce ați construit coloana vertebrală a aplicației (S10 React/JSX și S11 Redux Toolkit), asociația studențească vă cere acum un dashboard real de analiză: tabele cu mii de înregistrări (membri, cluburi, evenimente), grafice care sintetizează evoluții (înrolări noi pe săptămână, participare pe club, distribuția rolurilor), filtre legate între ele și export pentru raportare. În demo‑urile inițiale totul merge, dar în producție apar provocări: filtrele aplicate în tabel nu se reflectă corect în grafic, scroll‑ul se blochează pe dataset‑uri mari, formatele de dată și număr nu respectă locale‑ul utilizatorului, temele „light/dark” modifică lizibilitatea și accesibilitatea culorilor, iar echipa QA cere teste fiabile pentru piese care, aparent, „nu pot fi testate” (grafice). Acest seminar fixează o hartă riguroasă: cum alegem biblioteca de tabele și cea de grafice, cum proiectăm datele și starea (state) pentru a evita dublări și inconsistențe, cum asigurăm performanță și a11y, cum testăm (unit și de integrare) și cum folosim AI‑assist (VSL) pentru a accelera fără a compromite rigurozitatea.
- 1) De ce „componente externe” și de ce acum
Comunitatea React oferă „componente externe” pentru două zone notoriu costisitoare: tabele și grafice. Ambele sunt, de fapt, „mini‑motoare” de interacțiune cu date: tabelele rezolvă căutare, sortare, filtrare, paginare, selecții, editare; graficele rezolvă agregare, cartografiere vizuală (encoding), animații și interacțiuni (tooltip, legend, zoom/brush). A le „scrie de la zero” este rar justificat în proiecte aplicate. În schimb, deciziile bune sunt: (a) separarea clară a straturilor (server cache vs app state vs view state), (b) modelarea datelor și a derivatelor prin selectori memoizați, (c) contracte explicite între store și componente (tabel/grafic) și (d) politici de testare care verifică ceea ce contează (contractul de config și efectele observabile în DOM), nu detalii de implementare internă.

### Seminar12_Partea2_Ghid_Arhive.docx

**Titluri/Heading-uri:**

- Ghid de utilizare — Arhive (Seminarul 12, Partea 2)
- Acest ghid explică **ce conțin** arhivele și **cum se folosesc**.
- ## Arhive livrate
1) **s12p2-standalone.zip** — proiect Vite + React + TS + TanStack Table + Chart.js; Vitest & Jest (JSDOM).
2) **s12p2-monorepo.zip** — PNPM workspaces; pachet `packages/lab` conține aceeași aplicație (util pentru CI agregat).

### Seminar12_Partea2_TabeleGrafice_Laborator_extins.docx

**Titluri/Heading-uri:**

- Seminarul 12 — Tabele & Grafice — Partea 2 (Laborator extins)
- **Obiectivul Părții 2** este să construim un **dashboard** didactic „**ClubHub+ Analytics**” folosind **TanStack Table** (tabel interactiv) și **Chart.js** (grafic bar) peste un **pipeline curat de date** (selectors puri), astfel încât tabelele și graficele să fie **sincronizate** printr‑o **sursă unică a adevărului**. Vei implementa controlul căutării (search) și al filtrării pe club, vei exersa **sortarea accesibilă** (`aria-sort`) și vei genera un **config determinist** pentru chart (fără animații) ca să fie **testabil** în **Vitest** și **Jest**. Toate explicațiile sunt pas cu pas; la final ai un **worksheet** cu **checklist** și un **starter** complet cu testele aferente.
- ---

### Seminar12_Partea3_Arhive_Ghid.docx

**Titluri/Heading-uri:**

- Ghid de utilizare — Arhive (Seminarul 12, Partea 3)
- ## Arhive livrate
1) **s12p3-standalone.zip** — 45 proiecte (L1/L2/L3), fiecare cu `starter/` + `solution/`, teste Vitest/Jest, README.md.
2) **s12p3-monorepo.zip** — PNPM workspaces (toate `starter/` în `packages/*`).
3) **s12p3-readmes.zip** — toate README‑urile (starter+solution) pentru consultare rapidă.

## Cum aleg proiectele
- Parcurge L1 în ordine; apoi L2; finalizează cu L3.
- Evită sări în L3 fără bazele din L1/L2: contractele devin mai abstracte (spec‑uri declarative, crossfilter).

## Rulare (standalone)
```bash
unzip s12p3-standalone.zip
cd s12p3-standalone/L1/L1-P01/starter
npm i
npm test
npm run dev
```

## Rulare (monorepo)
```bash
unzip s12p3-monorepo.zip
cd s12p3-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter l1-p01-starter run dev
```

## Troubleshooting
- **Jest TSX** — asigurați `babel-jest` + preseturi (incluse).
- **Vitest JSDOM** — `environment:'jsdom'` + `setupFiles` (incluse).
- **Chart.js** — folosiți `chart.js/auto`; pentru teste, limitați-vă la contract (mock).
- **Locale** — dacă rezultatele `Intl.*` diferă, verificați locale‑ul Node/OS.
- **Performanță** — dacă datele cresc, folosiți `downsample`/`rollups`/virtualizare (L2/L3).

### Seminar12_Partea3_Proiecte_extins.docx

**Titluri/Heading-uri:**

- Seminarul 12 — Partea 3 (Proiecte/teme extinse)
- Partea 3 din Seminarul 12 oferă un set coerent de **45 de proiecte** împărțite pe trei niveluri (L1, L2, L3) care îmbină **tabele** (TanStack Table), **grafice** (Chart.js) și **funcții pure** pentru prelucrarea datelor. Scopul este consolidarea competențelor prin sarcini atomice, verificabile automat (**Vitest** & **Jest**), dar și prin extensii realiste (export, i18n, theming, sincronizări bidirecționale, specificații declarative pentru grafice, crossfilter, ferestre virtualizate, fluxuri în timp real).
    
**Metodologie didactică.** Fiecare proiect este structurat identic: (1) **Obiectiv educațional** (ce deprindere vizați), (2) **Specificații** (cerințe măsurabile), (3) **Contracte de test** (ce verifică testele, în termeni observabili), (4) **Soluție minimă** (principii algoritmice, nu neapărat cod complet aici), (5) **Erori tipice** (antipatters), (6) **AI‑assist (VSL)**—prompturi utile pentru GitHub Copilot sau un LLM (ChatGPT, Claude, Mistral). Abordarea privilegiază **funcțiile pure** pentru că acestea sunt: (a) deterministe (ușor de testat), (b) ușor de compus, (c) independente de UI.
    
**Principii transversale.**
- **Single source of truth.** Datele „raw” sunt unice; derivele (filtrare, agregare, paginate) se calculează „la cerere” prin **selectori** (funcții pure).
- **Contract over pixels.** Testele privesc contractele: forme de obiect (e.g., `{ labels, datasets }`), efecte observabile (aria‑sort, lungimi, secvențe), nu detalii fragile de implementare (DOM intern al graficului).
- **Accesibilitate (a11y).** Tabele semantice, `aria-sort`, butoane de sortare, `caption`, focus și tastatură; grafice deterministe, culori lizibile (palete contrastante), alternative textuale (sumare de date).
- **i18n/Theming.** Formatarea numerelor și datelor prin `Intl.*`; palete dependente de temă și testate pe canale (sequential/diverging); nu codificați doar cu culoarea.
- **Performanță.** Debounce/throttle pentru filtre; virtualizare; bugete măsurabile; funcții `downsample`/`rollups` pentru volum mare de date.
- **Reproducibilitate.** Configurări declarative, *snapshots* ale specificațiilor, serializare stabilă (`serializeConfig`), opțiuni pentru export (CSV/PNG).
- **Siguranță.** `sanitizeCsv` pentru export, evitarea injecțiilor (e.g., formula injection).
    
**Flux de lucru recomandat.** Alegeți un proiect, rulați `npm test` în `starter/`, completați TODO‑urile din `src/lib/lib.ts` până testele devin verzi, apoi inspectați `solution/` pentru a compara abordarea. Documentația din README indică *learning goals* și prompturi de AI. Testele sunt identice (logic) în **Vitest** și **Jest** pentru a vă antrena în ambele ecosisteme.
- # L1 — Fundamental

## 3. Monorepo vs. standalone — analiză comparativă


**Manageri de pachete & workspaces.** Variantele monorepo folosesc `pnpm-workspace.yaml` și/sau câmpul `workspaces` în `package.json` pentru a orchestra pachete (ex.: `packages/lab`, `packages/*`). Standalone izolează setul de dependențe pe directorul proiectului.

**Comenzi de instalare/testare.** Monorepo: `pnpm i -w`, `pnpm --filter <pkg> run test` (sau `-w run test` pentru toate). Standalone: `npm i`, `npm test`. Ambele folosesc testare dublă (Vitest/Jest) conform ghidurilor laboratorului.

**Integrare CI.** Monorepo agregă workflows unificate la rădăcină (`.github/workflows/*.yml`), cu matrice pe pachete; standalone tinde să aibă workflows per proiect, simplificate.

**Avantaje/Dezavantaje.** Începătorii beneficiază de standalone (model mental redus). Monorepo devine preferabil pentru colecții mari (ex.: 45 proiecte L1–L3) și pentru partajarea config‑urilor; costul este înțelegerea filtrării PNPM și a grafului de pachete.
## 4. Rolul fișierelor cheie (config, cod, teste, extra)

| Fișier / tip | Rol |
|---|---|
| `package.json` | Manifestul proiectului: metadate, dependențe, scripturi. Activează ESM prin `type: "module"`. |
| `pnpm-workspace.yaml` | Declară pachetele din monorepo pentru PNPM. |
| `tsconfig.json` | Parametri TypeScript (strictness, paths). |
| `vite.config.ts` | Configurare Vite pentru dev/build (React plugin). |
| `vitest.config.ts` | Configurare Vitest (environment JSDOM, reporters). |
| `jest.config.cjs` | Configurare Jest pentru TSX/JSX (JSDOM, transform cu `babel-jest`). |
| `babel.config.cjs` | Preseturi Babel pentru Jest (`@babel/preset-env`, `@babel/preset-react`, `@babel/preset-typescript`). |
| `src/App.tsx` | Compoziția UI (controale, tabel, grafic). |
| `src/components/DataTable.tsx` | Tabelul TanStack (sortare accesibilă, aria-sort). |
| `src/components/ChartPanel.tsx` | Wrapper determinist pentru Chart.js (fără animații). |
| `src/selectors/analytics.ts` | Funcții pure (filtrare, agregări) — „contract over pixels”. |
| `public/index.html` | Șablonul HTML servit de Vite (root). |

## 5. Corelații cod ↔ configurări ↔ teste


- **Selectori (funcții pure)** din `src/selectors/analytics.ts` derivă **configul graficului** și **rândurile vizibile** din aceeași sursă de date; **Vitest** și **Jest** verifică aceleași contracte (forme de obiect, aria‑sort, ordini), nu pixeli. 
- **`.env.example`** documentează variabilele **Vite/Node**; `VITE_*` sunt injectate în build, iar restul se citesc în scripturi/CI. 
- **ESLint + CI**: `npm run lint`/workflow‑urile blochează regresiile stilistice; `test` rulează Vitest **și** Jest; pentru L3, **Playwright** completează cu e2e, iar **Workbox** (dacă prezent) asigură PWA.
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S12 fixează integrarea **tabelelor** (TanStack Table) și **graficelor** (Chart.js/ECharts) într‑un **dashboard sincronizat** prin „single source of truth”, cu testare dublă (Vitest & Jest) și extensii (i18n, theming, export, virtualizare). Mappingul dintre teorie, laborator și proiecte este explicit și reproductibil (contracte de test).### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; rădăcină + pachete |
| Instalare | `npm i` în directorul proiectului | `pnpm i -w` la rădăcină |
| Rulare teste | `npm test` | `pnpm -w run test` sau `--filter` |
| CI | Workflows simple per proiect | Workflows agregate, matrice pe pachete |
| Scalare (45 proiecte) | multiplicare directoare | pachete dedicate în `packages/*` |
| Public țintă | începători | echipe/colecții avansate |
### Inventar pe arhivă (roluri)

- **Seminar12_Partea2_p2-monorepo.zip** — config=8, other=1, code=8, public=1, tests=7, docs=2.
- **Seminar12_Partea2_p2-standalone.zip** — config=6, other=1, code=8, public=1, tests=7, docs=2.
- **Seminar12_Partea3_p3-monorepo.zip** — config=272, other=45, docs=45, code=315, tests=135.
- **Seminar12_Partea3_p3-standalone.zip** — config=540, other=90, docs=90, code=630, tests=270.
- **Seminar12_Partea3_p3-READMEs.zip** — docs=90.
### Explicații fișier‑cu‑fișier

Consultați tabelul din §4 și detaliile din `package.json`/configuri, plus testele din `tests/` pentru fiecare proiect.
### Corelații între fișiere


- `src/selectors/analytics.ts` ↔ `tests/*`: testele asertă structurile `{ labels, datasets }` și subseturile vizibile.  
- `src/components/DataTable.tsx` ↔ a11y: `aria-sort`, `caption`, navigare cu tastatura; acoperite de teste RTL.  
- `ChartPanel.tsx` ↔ mock Chart.js: constructorul e mock‑uit în teste pentru determinism.  
- `.github/workflows/*` ↔ `lint`/`test`: pipeline determinist pentru PR‑uri.  
### Recomandări pentru studenți


1) **Începeți în varianta standalone** (curba mai lină).  
2) **Scrieți întâi selectorii** (funcții pure), abia apoi UI.  
3) **Testați în paralel** cu Vitest și Jest pentru robustețe.  
4) **Separați datele „raw” de formatare** (Intl.* doar în view).  
5) **Mențineți accesibilitatea** (tabele semantice; contrast; focus).  
6) **Documentați contractele** (forme de config/grafic) — vor ghida proiectele L2/L3.  
### Instrucțiuni „Quick start” per arhivă


**Partea 2 — standalone:**
```bash
unzip Seminar12_Partea2_p2-standalone.zip -d s12p2-standalone
cd s12p2-standalone
npm i
npm test
npm run dev
```

**Partea 2 — monorepo:**
```bash
unzip Seminar12_Partea2_p2-monorepo.zip -d s12p2-monorepo
cd s12p2-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter lab run dev
```

**Partea 3 — standalone (proiecte):**
```bash
unzip Seminar12_Partea3_p3-standalone.zip -d s12p3-standalone
cd s12p3-standalone/L1/L1-P01/starter
npm i
npm test
npm run dev
```

**Partea 3 — monorepo (proiecte):**
```bash
unzip Seminar12_Partea3_p3-monorepo.zip -d s12p3-monorepo
cd s12p3-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter l1-p01-starter run dev
```
### Troubleshooting (erori frecvente)


- **TSX în Jest** → `babel-jest` + preseturi; verificați `jest.config.cjs`.  
- **JSDOM** → setați `testEnvironment`/`environment` adecvat (Jest/Vitest).  
- **Chart.js în teste** → mock constructorul din `chart.js/auto`; asertați contractul, nu pixelii.  
- **Intl locale** → verificați `ro-RO` vs `en-GB` la formatare (Node/OS).  
- **Performanță** → dataset mare: virtualizare, debouncing, roll‑ups; pentru L3, paginare la sursă.  
- **PNPM filter** → dacă un pachet nu este găsit, verificați `pnpm-workspace.yaml` și `name` în `package.json`.  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** — principii de percepție vizuală, modelarea datelor și a stării, a11y, performanță, testabilitate deterministă (→ reflectate în selectori și în wrapperul Chart.js).  
- **Partea 2 (Laborator)** — „ClubHub+ Analytics”: pipeline curat, tabel sortabil accesibil, sincronizare tabel→grafic, testare dublă (→ oglindite în structura arhivelor).  
- **Partea 3 (Proiecte)** — 45 proiecte L1–L3 cu extensii (crossfilter, virtualizare, spec declarative) și rubrică de evaluare (→ mapate în folderele starter/solution).  
### Prompt‑șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S12** (standalone & monorepo) un dashboard React/TS cu TanStack Table + Chart.js, *single source of truth* prin selecții/filtre în selectori, testare dublă **Vitest/Jest**, plus CI și extensii (i18n, theming, export). Produce **starter** și **solution**, README cu Quick start și Troubleshooting.”
