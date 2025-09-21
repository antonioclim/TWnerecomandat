# Seminarul S10 — React: componente & JSX (standalone & monorepo) — Analiză integrată a arhivelor și ghidurilor

*Generat la 2025-09-21 04:46.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar10_Partea2_p2-monorepo.zip

```
package.json
packages/lab/babel.config.cjs
packages/lab/docs/README.md
packages/lab/docs/WORKSHEET.md
packages/lab/index.html
packages/lab/jest.config.cjs
packages/lab/package.json
packages/lab/src/App.tsx
packages/lab/src/components/AddClubForm.tsx
packages/lab/src/components/ClubCard.tsx
packages/lab/src/components/ClubList.tsx
packages/lab/src/components/Footer.tsx
packages/lab/src/components/Header.tsx
packages/lab/src/components/SearchBox.tsx
packages/lab/src/hooks/useFilteredClubs.ts
packages/lab/src/main.tsx
packages/lab/src/styles.css
packages/lab/src/types.ts
packages/lab/tests/jest/AddClubForm.jest.test.tsx
packages/lab/tests/jest/App.jest.test.tsx
packages/lab/tests/jest/ClubCard.jest.test.tsx
packages/lab/tests/jest/SearchBox.jest.test.tsx
packages/lab/tests/setup.ts
packages/lab/tests/vitest/AddClubForm.test.tsx
packages/lab/tests/vitest/App.test.tsx
packages/lab/tests/vitest/ClubCard.test.tsx
packages/lab/tests/vitest/SearchBox.test.tsx
packages/lab/tsconfig.json
packages/lab/vite.config.ts
packages/lab/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 8, public: 1, code: 11, tests: 9, docs: 2.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s10p2-monorepo` type=`module` workspaces=True
- `packages/lab/package.json`: name=`s10p2-react-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest

### Seminar10_Partea2_p2-standalone.zip

```
babel.config.cjs
docs/README.md
docs/WORKSHEET.md
index.html
jest.config.cjs
package.json
src/App.tsx
src/components/AddClubForm.tsx
src/components/ClubCard.tsx
src/components/ClubList.tsx
src/components/Footer.tsx
src/components/Header.tsx
src/components/SearchBox.tsx
src/hooks/useFilteredClubs.ts
src/main.tsx
src/styles.css
src/types.ts
tests/jest/AddClubForm.jest.test.tsx
tests/jest/App.jest.test.tsx
tests/jest/ClubCard.jest.test.tsx
tests/jest/SearchBox.jest.test.tsx
tests/setup.ts
tests/vitest/AddClubForm.test.tsx
tests/vitest/App.test.tsx
tests/vitest/ClubCard.test.tsx
tests/vitest/SearchBox.test.tsx
tsconfig.json
vite.config.ts
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 6, public: 1, code: 11, tests: 9, docs: 2.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s10p2-react-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest

### Seminar10_Partea3_p3-monorepo.zip

```
package.json
packages/l1-p01-starter/README.md
packages/l1-p01-starter/babel.config.cjs
packages/l1-p01-starter/index.html
packages/l1-p01-starter/jest.config.cjs
packages/l1-p01-starter/package.json
packages/l1-p01-starter/src/App.tsx
packages/l1-p01-starter/src/main.tsx
packages/l1-p01-starter/src/styles.css
packages/l1-p01-starter/tests/jest/App.jest.test.tsx
packages/l1-p01-starter/tests/setup.ts
packages/l1-p01-starter/tests/vitest/App.test.tsx
packages/l1-p01-starter/tsconfig.json
packages/l1-p01-starter/vite.config.ts
packages/l1-p01-starter/vitest.config.ts
packages/l1-p02-starter/README.md
packages/l1-p02-starter/babel.config.cjs
packages/l1-p02-starter/index.html
packages/l1-p02-starter/jest.config.cjs
packages/l1-p02-starter/package.json
packages/l1-p02-starter/src/App.tsx
packages/l1-p02-starter/src/main.tsx
packages/l1-p02-starter/src/styles.css
packages/l1-p02-starter/tests/jest/App.jest.test.tsx
packages/l1-p02-starter/tests/setup.ts
packages/l1-p02-starter/tests/vitest/App.test.tsx
packages/l1-p02-starter/tsconfig.json
packages/l1-p02-starter/vite.config.ts
packages/l1-p02-starter/vitest.config.ts
packages/l1-p03-starter/README.md
packages/l1-p03-starter/babel.config.cjs
packages/l1-p03-starter/index.html
packages/l1-p03-starter/jest.config.cjs
packages/l1-p03-starter/package.json
packages/l1-p03-starter/src/App.tsx
packages/l1-p03-starter/src/main.tsx
packages/l1-p03-starter/src/styles.css
packages/l1-p03-starter/tests/jest/App.jest.test.tsx
packages/l1-p03-starter/tests/setup.ts
packages/l1-p03-starter/tests/vitest/App.test.tsx
packages/l1-p03-starter/tsconfig.json
packages/l1-p03-starter/vite.config.ts
packages/l1-p03-starter/vitest.config.ts
packages/l1-p04-starter/README.md
packages/l1-p04-starter/babel.config.cjs
packages/l1-p04-starter/index.html
packages/l1-p04-starter/jest.config.cjs
packages/l1-p04-starter/package.json
packages/l1-p04-starter/src/App.tsx
packages/l1-p04-starter/src/main.tsx
packages/l1-p04-starter/src/styles.css
packages/l1-p04-starter/tests/jest/App.jest.test.tsx
packages/l1-p04-starter/tests/setup.ts
packages/l1-p04-starter/tests/vitest/App.test.tsx
packages/l1-p04-starter/tsconfig.json
packages/l1-p04-starter/vite.config.ts
packages/l1-p04-starter/vitest.config.ts
packages/l1-p05-starter/README.md
packages/l1-p05-starter/babel.config.cjs
packages/l1-p05-starter/index.html
packages/l1-p05-starter/jest.config.cjs
packages/l1-p05-starter/package.json
packages/l1-p05-starter/src/App.tsx
packages/l1-p05-starter/src/main.tsx
packages/l1-p05-starter/src/styles.css
packages/l1-p05-starter/tests/jest/App.jest.test.tsx
packages/l1-p05-starter/tests/setup.ts
packages/l1-p05-starter/tests/vitest/App.test.tsx
packages/l1-p05-starter/tsconfig.json
packages/l1-p05-starter/vite.config.ts
packages/l1-p05-starter/vitest.config.ts
packages/l1-p06-starter/README.md
packages/l1-p06-starter/babel.config.cjs
packages/l1-p06-starter/index.html
packages/l1-p06-starter/jest.config.cjs
packages/l1-p06-starter/package.json
packages/l1-p06-starter/src/App.tsx
packages/l1-p06-starter/src/main.tsx
packages/l1-p06-starter/src/styles.css
packages/l1-p06-starter/tests/jest/App.jest.test.tsx
packages/l1-p06-starter/tests/setup.ts
packages/l1-p06-starter/tests/vitest/App.test.tsx
packages/l1-p06-starter/tsconfig.json
packages/l1-p06-starter/vite.config.ts
packages/l1-p06-starter/vitest.config.ts
packages/l1-p07-starter/README.md
packages/l1-p07-starter/babel.config.cjs
packages/l1-p07-starter/index.html
packages/l1-p07-starter/jest.config.cjs
packages/l1-p07-starter/package.json
packages/l1-p07-starter/src/App.tsx
packages/l1-p07-starter/src/main.tsx
packages/l1-p07-starter/src/styles.css
packages/l1-p07-starter/tests/jest/App.jest.test.tsx
packages/l1-p07-starter/tests/setup.ts
packages/l1-p07-starter/tests/vitest/App.test.tsx
packages/l1-p07-starter/tsconfig.json
packages/l1-p07-starter/vite.config.ts
packages/l1-p07-starter/vitest.config.ts
packages/l1-p08-starter/README.md
packages/l1-p08-starter/babel.config.cjs
packages/l1-p08-starter/index.html
packages/l1-p08-starter/jest.config.cjs
packages/l1-p08-starter/package.json
packages/l1-p08-starter/src/App.tsx
packages/l1-p08-starter/src/main.tsx
packages/l1-p08-starter/src/styles.css
packages/l1-p08-starter/tests/jest/App.jest.test.tsx
packages/l1-p08-starter/tests/setup.ts
packages/l1-p08-starter/tests/vitest/App.test.tsx
packages/l1-p08-starter/tsconfig.json
packages/l1-p08-starter/vite.config.ts
packages/l1-p08-starter/vitest.config.ts
packages/l1-p09-starter/README.md
packages/l1-p09-starter/babel.config.cjs
packages/l1-p09-starter/index.html
packages/l1-p09-starter/jest.config.cjs
packages/l1-p09-starter/package.json
packages/l1-p09-starter/src/App.tsx
packages/l1-p09-starter/src/main.tsx
packages/l1-p09-starter/src/styles.css
packages/l1-p09-starter/tests/jest/App.jest.test.tsx
packages/l1-p09-starter/tests/setup.ts
packages/l1-p09-starter/tests/vitest/App.test.tsx
packages/l1-p09-starter/tsconfig.json
packages/l1-p09-starter/vite.config.ts
packages/l1-p09-starter/vitest.config.ts
packages/l1-p10-starter/README.md
packages/l1-p10-starter/babel.config.cjs
packages/l1-p10-starter/index.html
packages/l1-p10-starter/jest.config.cjs
packages/l1-p10-starter/package.json
packages/l1-p10-starter/src/App.tsx
packages/l1-p10-starter/src/main.tsx
packages/l1-p10-starter/src/styles.css
packages/l1-p10-starter/tests/jest/App.jest.test.tsx
packages/l1-p10-starter/tests/setup.ts
packages/l1-p10-starter/tests/vitest/App.test.tsx
packages/l1-p10-starter/tsconfig.json
packages/l1-p10-starter/vite.config.ts
packages/l1-p10-starter/vitest.config.ts
packages/l1-p11-starter/README.md
packages/l1-p11-starter/babel.config.cjs
packages/l1-p11-starter/index.html
packages/l1-p11-starter/jest.config.cjs
packages/l1-p11-starter/package.json
packages/l1-p11-starter/src/App.tsx
packages/l1-p11-starter/src/main.tsx
packages/l1-p11-starter/src/styles.css
packages/l1-p11-starter/tests/jest/App.jest.test.tsx
packages/l1-p11-starter/tests/setup.ts
packages/l1-p11-starter/tests/vitest/App.test.tsx
packages/l1-p11-starter/tsconfig.json
packages/l1-p11-starter/vite.config.ts
packages/l1-p11-starter/vitest.config.ts
packages/l1-p12-starter/README.md
packages/l1-p12-starter/babel.config.cjs
packages/l1-p12-starter/index.html
packages/l1-p12-starter/jest.config.cjs
packages/l1-p12-starter/package.json
packages/l1-p12-starter/src/App.tsx
packages/l1-p12-starter/src/main.tsx
packages/l1-p12-starter/src/styles.css
packages/l1-p12-starter/tests/jest/App.jest.test.tsx
packages/l1-p12-starter/tests/setup.ts
packages/l1-p12-starter/tests/vitest/App.test.tsx
packages/l1-p12-starter/tsconfig.json
packages/l1-p12-starter/vite.config.ts
packages/l1-p12-starter/vitest.config.ts
packages/l1-p13-starter/README.md
packages/l1-p13-starter/babel.config.cjs
packages/l1-p13-starter/index.html
packages/l1-p13-starter/jest.config.cjs
packages/l1-p13-starter/package.json
packages/l1-p13-starter/src/App.tsx
packages/l1-p13-starter/src/main.tsx
packages/l1-p13-starter/src/styles.css
packages/l1-p13-starter/tests/jest/App.jest.test.tsx
packages/l1-p13-starter/tests/setup.ts
packages/l1-p13-starter/tests/vitest/App.test.tsx
packages/l1-p13-starter/tsconfig.json
packages/l1-p13-starter/vite.config.ts
packages/l1-p13-starter/vitest.config.ts
packages/l1-p14-starter/README.md
packages/l1-p14-starter/babel.config.cjs
packages/l1-p14-starter/index.html
packages/l1-p14-starter/jest.config.cjs
packages/l1-p14-starter/package.json
packages/l1-p14-starter/src/App.tsx
packages/l1-p14-starter/src/main.tsx
packages/l1-p14-starter/src/styles.css
packages/l1-p14-starter/tests/jest/App.jest.test.tsx
packages/l1-p14-starter/tests/setup.ts
packages/l1-p14-starter/tests/vitest/App.test.tsx
packages/l1-p14-starter/tsconfig.json
packages/l1-p14-starter/vite.config.ts
packages/l1-p14-starter/vitest.config.ts
packages/l1-p15-starter/README.md
packages/l1-p15-starter/babel.config.cjs
packages/l1-p15-starter/index.html
packages/l1-p15-starter/jest.config.cjs
packages/l1-p15-starter/package.json
packages/l1-p15-starter/src/App.tsx
packages/l1-p15-starter/src/main.tsx
packages/l1-p15-starter/src/styles.css
packages/l1-p15-starter/tests/jest/App.jest.test.tsx
packages/l1-p15-starter/tests/setup.ts
packages/l1-p15-starter/tests/vitest/App.test.tsx
packages/l1-p15-starter/tsconfig.json
packages/l1-p15-starter/vite.config.ts
packages/l1-p15-starter/vitest.config.ts
packages/l2-p01-starter/README.md
packages/l2-p01-starter/babel.config.cjs
packages/l2-p01-starter/index.html
packages/l2-p01-starter/jest.config.cjs
packages/l2-p01-starter/package.json
packages/l2-p01-starter/src/App.tsx
packages/l2-p01-starter/src/main.tsx
packages/l2-p01-starter/src/styles.css
packages/l2-p01-starter/tests/jest/App.jest.test.tsx
packages/l2-p01-starter/tests/setup.ts
packages/l2-p01-starter/tests/vitest/App.test.tsx
packages/l2-p01-starter/tsconfig.json
packages/l2-p01-starter/vite.config.ts
packages/l2-p01-starter/vitest.config.ts
packages/l2-p02-starter/README.md
packages/l2-p02-starter/babel.config.cjs
packages/l2-p02-starter/index.html
packages/l2-p02-starter/jest.config.cjs
packages/l2-p02-starter/package.json
packages/l2-p02-starter/src/App.tsx
packages/l2-p02-starter/src/main.tsx
packages/l2-p02-starter/src/styles.css
packages/l2-p02-starter/tests/jest/App.jest.test.tsx
packages/l2-p02-starter/tests/setup.ts
packages/l2-p02-starter/tests/vitest/App.test.tsx
packages/l2-p02-starter/tsconfig.json
packages/l2-p02-starter/vite.config.ts
packages/l2-p02-starter/vitest.config.ts
packages/l2-p03-starter/README.md
packages/l2-p03-starter/babel.config.cjs
packages/l2-p03-starter/index.html
packages/l2-p03-starter/jest.config.cjs
packages/l2-p03-starter/package.json
packages/l2-p03-starter/src/App.tsx
packages/l2-p03-starter/src/main.tsx
packages/l2-p03-starter/src/styles.css
packages/l2-p03-starter/tests/jest/App.jest.test.tsx
packages/l2-p03-starter/tests/setup.ts
packages/l2-p03-starter/tests/vitest/App.test.tsx
packages/l2-p03-starter/tsconfig.json
packages/l2-p03-starter/vite.config.ts
packages/l2-p03-starter/vitest.config.ts
packages/l2-p04-starter/README.md
packages/l2-p04-starter/babel.config.cjs
packages/l2-p04-starter/index.html
packages/l2-p04-starter/jest.config.cjs
packages/l2-p04-starter/package.json
packages/l2-p04-starter/src/App.tsx
packages/l2-p04-starter/src/main.tsx
packages/l2-p04-starter/src/styles.css
packages/l2-p04-starter/tests/jest/App.jest.test.tsx
packages/l2-p04-starter/tests/setup.ts
packages/l2-p04-starter/tests/vitest/App.test.tsx
packages/l2-p04-starter/tsconfig.json
packages/l2-p04-starter/vite.config.ts
packages/l2-p04-starter/vitest.config.ts
packages/l2-p05-starter/README.md
packages/l2-p05-starter/babel.config.cjs
packages/l2-p05-starter/index.html
packages/l2-p05-starter/jest.config.cjs
packages/l2-p05-starter/package.json
packages/l2-p05-starter/src/App.tsx
packages/l2-p05-starter/src/main.tsx
packages/l2-p05-starter/src/styles.css
packages/l2-p05-starter/tests/jest/App.jest.test.tsx
packages/l2-p05-starter/tests/setup.ts
packages/l2-p05-starter/tests/vitest/App.test.tsx
packages/l2-p05-starter/tsconfig.json
packages/l2-p05-starter/vite.config.ts
packages/l2-p05-starter/vitest.config.ts
packages/l2-p06-starter/README.md
packages/l2-p06-starter/babel.config.cjs
packages/l2-p06-starter/index.html
packages/l2-p06-starter/jest.config.cjs
packages/l2-p06-starter/package.json
packages/l2-p06-starter/src/App.tsx
packages/l2-p06-starter/src/main.tsx
packages/l2-p06-starter/src/styles.css
packages/l2-p06-starter/tests/jest/App.jest.test.tsx
packages/l2-p06-starter/tests/setup.ts
packages/l2-p06-starter/tests/vitest/App.test.tsx
packages/l2-p06-starter/tsconfig.json
packages/l2-p06-starter/vite.config.ts
packages/l2-p06-starter/vitest.config.ts
packages/l2-p07-starter/README.md
packages/l2-p07-starter/babel.config.cjs
packages/l2-p07-starter/index.html
packages/l2-p07-starter/jest.config.cjs
packages/l2-p07-starter/package.json
packages/l2-p07-starter/src/App.tsx
packages/l2-p07-starter/src/main.tsx
packages/l2-p07-starter/src/styles.css
packages/l2-p07-starter/tests/jest/App.jest.test.tsx
packages/l2-p07-starter/tests/setup.ts
packages/l2-p07-starter/tests/vitest/App.test.tsx
packages/l2-p07-starter/tsconfig.json
packages/l2-p07-starter/vite.config.ts
packages/l2-p07-starter/vitest.config.ts
packages/l2-p08-starter/README.md
packages/l2-p08-starter/babel.config.cjs
packages/l2-p08-starter/index.html
packages/l2-p08-starter/jest.config.cjs
packages/l2-p08-starter/package.json
packages/l2-p08-starter/src/App.tsx
packages/l2-p08-starter/src/main.tsx
packages/l2-p08-starter/src/styles.css
packages/l2-p08-starter/tests/jest/App.jest.test.tsx
packages/l2-p08-starter/tests/setup.ts
packages/l2-p08-starter/tests/vitest/App.test.tsx
packages/l2-p08-starter/tsconfig.json
packages/l2-p08-starter/vite.config.ts
packages/l2-p08-starter/vitest.config.ts
packages/l2-p09-starter/README.md
packages/l2-p09-starter/babel.config.cjs
packages/l2-p09-starter/index.html
packages/l2-p09-starter/jest.config.cjs
packages/l2-p09-starter/package.json
packages/l2-p09-starter/src/App.tsx
packages/l2-p09-starter/src/main.tsx
packages/l2-p09-starter/src/styles.css
packages/l2-p09-starter/tests/jest/App.jest.test.tsx
packages/l2-p09-starter/tests/setup.ts
packages/l2-p09-starter/tests/vitest/App.test.tsx
packages/l2-p09-starter/tsconfig.json
packages/l2-p09-starter/vite.config.ts
packages/l2-p09-starter/vitest.config.ts
packages/l2-p10-starter/README.md
packages/l2-p10-starter/babel.config.cjs
packages/l2-p10-starter/index.html
packages/l2-p10-starter/jest.config.cjs
packages/l2-p10-starter/package.json
packages/l2-p10-starter/src/App.tsx
packages/l2-p10-starter/src/main.tsx
packages/l2-p10-starter/src/styles.css
packages/l2-p10-starter/tests/jest/App.jest.test.tsx
packages/l2-p10-starter/tests/setup.ts
packages/l2-p10-starter/tests/vitest/App.test.tsx
packages/l2-p10-starter/tsconfig.json
packages/l2-p10-starter/vite.config.ts
packages/l2-p10-starter/vitest.config.ts
packages/l2-p11-starter/README.md
packages/l2-p11-starter/babel.config.cjs
packages/l2-p11-starter/index.html
packages/l2-p11-starter/jest.config.cjs
packages/l2-p11-starter/package.json
packages/l2-p11-starter/src/App.tsx
packages/l2-p11-starter/src/main.tsx
packages/l2-p11-starter/src/styles.css
packages/l2-p11-starter/tests/jest/App.jest.test.tsx
packages/l2-p11-starter/tests/setup.ts
packages/l2-p11-starter/tests/vitest/App.test.tsx
packages/l2-p11-starter/tsconfig.json
packages/l2-p11-starter/vite.config.ts
packages/l2-p11-starter/vitest.config.ts
packages/l2-p12-starter/README.md
packages/l2-p12-starter/babel.config.cjs
packages/l2-p12-starter/index.html
packages/l2-p12-starter/jest.config.cjs
packages/l2-p12-starter/package.json
packages/l2-p12-starter/src/App.tsx
packages/l2-p12-starter/src/main.tsx
packages/l2-p12-starter/src/styles.css
packages/l2-p12-starter/tests/jest/App.jest.test.tsx
packages/l2-p12-starter/tests/setup.ts
packages/l2-p12-starter/tests/vitest/App.test.tsx
packages/l2-p12-starter/tsconfig.json
packages/l2-p12-starter/vite.config.ts
packages/l2-p12-starter/vitest.config.ts
packages/l2-p13-starter/README.md
packages/l2-p13-starter/babel.config.cjs
packages/l2-p13-starter/index.html
packages/l2-p13-starter/jest.config.cjs
packages/l2-p13-starter/package.json
packages/l2-p13-starter/src/App.tsx
packages/l2-p13-starter/src/main.tsx
packages/l2-p13-starter/src/styles.css
packages/l2-p13-starter/tests/jest/App.jest.test.tsx
packages/l2-p13-starter/tests/setup.ts
packages/l2-p13-starter/tests/vitest/App.test.tsx
packages/l2-p13-starter/tsconfig.json
packages/l2-p13-starter/vite.config.ts
packages/l2-p13-starter/vitest.config.ts
packages/l2-p14-starter/README.md
packages/l2-p14-starter/babel.config.cjs
packages/l2-p14-starter/index.html
packages/l2-p14-starter/jest.config.cjs
packages/l2-p14-starter/package.json
packages/l2-p14-starter/src/App.tsx
packages/l2-p14-starter/src/main.tsx
packages/l2-p14-starter/src/styles.css
packages/l2-p14-starter/tests/jest/App.jest.test.tsx
packages/l2-p14-starter/tests/setup.ts
packages/l2-p14-starter/tests/vitest/App.test.tsx
packages/l2-p14-starter/tsconfig.json
packages/l2-p14-starter/vite.config.ts
packages/l2-p14-starter/vitest.config.ts
packages/l2-p15-starter/README.md
packages/l2-p15-starter/babel.config.cjs
packages/l2-p15-starter/index.html
packages/l2-p15-starter/jest.config.cjs
packages/l2-p15-starter/package.json
packages/l2-p15-starter/src/App.tsx
packages/l2-p15-starter/src/main.tsx
packages/l2-p15-starter/src/styles.css
packages/l2-p15-starter/tests/jest/App.jest.test.tsx
packages/l2-p15-starter/tests/setup.ts
packages/l2-p15-starter/tests/vitest/App.test.tsx
packages/l2-p15-starter/tsconfig.json
packages/l2-p15-starter/vite.config.ts
packages/l2-p15-starter/vitest.config.ts
packages/l3-p01-starter/README.md
packages/l3-p01-starter/babel.config.cjs
packages/l3-p01-starter/index.html
packages/l3-p01-starter/jest.config.cjs
packages/l3-p01-starter/package.json
packages/l3-p01-starter/src/App.tsx
packages/l3-p01-starter/src/main.tsx
packages/l3-p01-starter/src/styles.css
packages/l3-p01-starter/tests/jest/App.jest.test.tsx
packages/l3-p01-starter/tests/setup.ts
packages/l3-p01-starter/tests/vitest/App.test.tsx
packages/l3-p01-starter/tsconfig.json
packages/l3-p01-starter/vite.config.ts
packages/l3-p01-starter/vitest.config.ts
packages/l3-p02-starter/README.md
packages/l3-p02-starter/babel.config.cjs
packages/l3-p02-starter/index.html
packages/l3-p02-starter/jest.config.cjs
packages/l3-p02-starter/package.json
packages/l3-p02-starter/src/App.tsx
packages/l3-p02-starter/src/main.tsx
packages/l3-p02-starter/src/styles.css
packages/l3-p02-starter/tests/jest/App.jest.test.tsx
packages/l3-p02-starter/tests/setup.ts
packages/l3-p02-starter/tests/vitest/App.test.tsx
packages/l3-p02-starter/tsconfig.json
packages/l3-p02-starter/vite.config.ts
packages/l3-p02-starter/vitest.config.ts
packages/l3-p03-starter/README.md
packages/l3-p03-starter/babel.config.cjs
packages/l3-p03-starter/index.html
packages/l3-p03-starter/jest.config.cjs
packages/l3-p03-starter/package.json
packages/l3-p03-starter/src/App.tsx
packages/l3-p03-starter/src/main.tsx
packages/l3-p03-starter/src/styles.css
packages/l3-p03-starter/tests/jest/App.jest.test.tsx
packages/l3-p03-starter/tests/setup.ts
packages/l3-p03-starter/tests/vitest/App.test.tsx
packages/l3-p03-starter/tsconfig.json
packages/l3-p03-starter/vite.config.ts
packages/l3-p03-starter/vitest.config.ts
packages/l3-p04-starter/README.md
packages/l3-p04-starter/babel.config.cjs
packages/l3-p04-starter/index.html
packages/l3-p04-starter/jest.config.cjs
packages/l3-p04-starter/package.json
packages/l3-p04-starter/src/App.tsx
packages/l3-p04-starter/src/main.tsx
packages/l3-p04-starter/src/styles.css
packages/l3-p04-starter/tests/jest/App.jest.test.tsx
packages/l3-p04-starter/tests/setup.ts
packages/l3-p04-starter/tests/vitest/App.test.tsx
packages/l3-p04-starter/tsconfig.json
packages/l3-p04-starter/vite.config.ts
packages/l3-p04-starter/vitest.config.ts
packages/l3-p05-starter/README.md
packages/l3-p05-starter/babel.config.cjs
packages/l3-p05-starter/index.html
packages/l3-p05-starter/jest.config.cjs
packages/l3-p05-starter/package.json
packages/l3-p05-starter/src/App.tsx
packages/l3-p05-starter/src/main.tsx
packages/l3-p05-starter/src/styles.css
packages/l3-p05-starter/tests/jest/App.jest.test.tsx
packages/l3-p05-starter/tests/setup.ts
packages/l3-p05-starter/tests/vitest/App.test.tsx
packages/l3-p05-starter/tsconfig.json
packages/l3-p05-starter/vite.config.ts
packages/l3-p05-starter/vitest.config.ts
packages/l3-p06-starter/README.md
packages/l3-p06-starter/babel.config.cjs
packages/l3-p06-starter/index.html
packages/l3-p06-starter/jest.config.cjs
packages/l3-p06-starter/package.json
packages/l3-p06-starter/src/App.tsx
packages/l3-p06-starter/src/main.tsx
packages/l3-p06-starter/src/styles.css
packages/l3-p06-starter/tests/jest/App.jest.test.tsx
packages/l3-p06-starter/tests/setup.ts
packages/l3-p06-starter/tests/vitest/App.test.tsx
packages/l3-p06-starter/tsconfig.json
packages/l3-p06-starter/vite.config.ts
packages/l3-p06-starter/vitest.config.ts
packages/l3-p07-starter/README.md
packages/l3-p07-starter/babel.config.cjs
packages/l3-p07-starter/index.html
packages/l3-p07-starter/jest.config.cjs
packages/l3-p07-starter/package.json
packages/l3-p07-starter/src/App.tsx
packages/l3-p07-starter/src/main.tsx
packages/l3-p07-starter/src/styles.css
packages/l3-p07-starter/tests/jest/App.jest.test.tsx
packages/l3-p07-starter/tests/setup.ts
packages/l3-p07-starter/tests/vitest/App.test.tsx
packages/l3-p07-starter/tsconfig.json
packages/l3-p07-starter/vite.config.ts
packages/l3-p07-starter/vitest.config.ts
packages/l3-p08-starter/README.md
packages/l3-p08-starter/babel.config.cjs
packages/l3-p08-starter/index.html
packages/l3-p08-starter/jest.config.cjs
packages/l3-p08-starter/package.json
packages/l3-p08-starter/src/App.tsx
packages/l3-p08-starter/src/main.tsx
packages/l3-p08-starter/src/styles.css
packages/l3-p08-starter/tests/jest/App.jest.test.tsx
packages/l3-p08-starter/tests/setup.ts
packages/l3-p08-starter/tests/vitest/App.test.tsx
packages/l3-p08-starter/tsconfig.json
packages/l3-p08-starter/vite.config.ts
packages/l3-p08-starter/vitest.config.ts
packages/l3-p09-starter/README.md
packages/l3-p09-starter/babel.config.cjs
packages/l3-p09-starter/index.html
packages/l3-p09-starter/jest.config.cjs
packages/l3-p09-starter/package.json
packages/l3-p09-starter/src/App.tsx
packages/l3-p09-starter/src/main.tsx
packages/l3-p09-starter/src/styles.css
packages/l3-p09-starter/tests/jest/App.jest.test.tsx
packages/l3-p09-starter/tests/setup.ts
packages/l3-p09-starter/tests/vitest/App.test.tsx
packages/l3-p09-starter/tsconfig.json
packages/l3-p09-starter/vite.config.ts
packages/l3-p09-starter/vitest.config.ts
packages/l3-p10-starter/README.md
packages/l3-p10-starter/babel.config.cjs
packages/l3-p10-starter/index.html
packages/l3-p10-starter/jest.config.cjs
packages/l3-p10-starter/package.json
packages/l3-p10-starter/src/App.tsx
packages/l3-p10-starter/src/main.tsx
packages/l3-p10-starter/src/styles.css
packages/l3-p10-starter/tests/jest/App.jest.test.tsx
packages/l3-p10-starter/tests/setup.ts
packages/l3-p10-starter/tests/vitest/App.test.tsx
packages/l3-p10-starter/tsconfig.json
packages/l3-p10-starter/vite.config.ts
packages/l3-p10-starter/vitest.config.ts
packages/l3-p11-starter/README.md
packages/l3-p11-starter/babel.config.cjs
packages/l3-p11-starter/index.html
packages/l3-p11-starter/jest.config.cjs
packages/l3-p11-starter/package.json
packages/l3-p11-starter/src/App.tsx
packages/l3-p11-starter/src/main.tsx
packages/l3-p11-starter/src/styles.css
packages/l3-p11-starter/tests/jest/App.jest.test.tsx
packages/l3-p11-starter/tests/setup.ts
packages/l3-p11-starter/tests/vitest/App.test.tsx
packages/l3-p11-starter/tsconfig.json
packages/l3-p11-starter/vite.config.ts
packages/l3-p11-starter/vitest.config.ts
packages/l3-p12-starter/README.md
packages/l3-p12-starter/babel.config.cjs
packages/l3-p12-starter/index.html
packages/l3-p12-starter/jest.config.cjs
packages/l3-p12-starter/package.json
packages/l3-p12-starter/src/App.tsx
packages/l3-p12-starter/src/main.tsx
packages/l3-p12-starter/src/styles.css
packages/l3-p12-starter/tests/jest/App.jest.test.tsx
packages/l3-p12-starter/tests/setup.ts
packages/l3-p12-starter/tests/vitest/App.test.tsx
packages/l3-p12-starter/tsconfig.json
packages/l3-p12-starter/vite.config.ts
packages/l3-p12-starter/vitest.config.ts
packages/l3-p13-starter/README.md
packages/l3-p13-starter/babel.config.cjs
packages/l3-p13-starter/index.html
packages/l3-p13-starter/jest.config.cjs
packages/l3-p13-starter/package.json
packages/l3-p13-starter/src/App.tsx
packages/l3-p13-starter/src/main.tsx
packages/l3-p13-starter/src/styles.css
packages/l3-p13-starter/tests/jest/App.jest.test.tsx
packages/l3-p13-starter/tests/setup.ts
packages/l3-p13-starter/tests/vitest/App.test.tsx
packages/l3-p13-starter/tsconfig.json
packages/l3-p13-starter/vite.config.ts
packages/l3-p13-starter/vitest.config.ts
packages/l3-p14-starter/README.md
packages/l3-p14-starter/babel.config.cjs
packages/l3-p14-starter/index.html
packages/l3-p14-starter/jest.config.cjs
packages/l3-p14-starter/package.json
packages/l3-p14-starter/src/App.tsx
packages/l3-p14-starter/src/main.tsx
packages/l3-p14-starter/src/styles.css
packages/l3-p14-starter/tests/jest/App.jest.test.tsx
packages/l3-p14-starter/tests/setup.ts
packages/l3-p14-starter/tests/vitest/App.test.tsx
packages/l3-p14-starter/tsconfig.json
packages/l3-p14-starter/vite.config.ts
packages/l3-p14-starter/vitest.config.ts
packages/l3-p15-starter/README.md
packages/l3-p15-starter/babel.config.cjs
packages/l3-p15-starter/index.html
packages/l3-p15-starter/jest.config.cjs
packages/l3-p15-starter/package.json
packages/l3-p15-starter/src/App.tsx
packages/l3-p15-starter/src/main.tsx
packages/l3-p15-starter/src/styles.css
packages/l3-p15-starter/tests/jest/App.jest.test.tsx
packages/l3-p15-starter/tests/setup.ts
packages/l3-p15-starter/tests/vitest/App.test.tsx
packages/l3-p15-starter/tsconfig.json
packages/l3-p15-starter/vite.config.ts
packages/l3-p15-starter/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** starter: 630.

**Categorii de fișiere:** config: 272, public: 45, docs: 45, code: 135, tests: 135.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s10p3-monorepo` type=`module` workspaces=True
- `packages/l1-p01-starter/package.json`: name=`l1-p01-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p02-starter/package.json`: name=`l1-p02-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p03-starter/package.json`: name=`l1-p03-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p04-starter/package.json`: name=`l1-p04-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p05-starter/package.json`: name=`l1-p05-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p06-starter/package.json`: name=`l1-p06-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p07-starter/package.json`: name=`l1-p07-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p08-starter/package.json`: name=`l1-p08-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p09-starter/package.json`: name=`l1-p09-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p10-starter/package.json`: name=`l1-p10-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p11-starter/package.json`: name=`l1-p11-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p12-starter/package.json`: name=`l1-p12-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p13-starter/package.json`: name=`l1-p13-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p14-starter/package.json`: name=`l1-p14-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l1-p15-starter/package.json`: name=`l1-p15-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p01-starter/package.json`: name=`l2-p01-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p02-starter/package.json`: name=`l2-p02-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p03-starter/package.json`: name=`l2-p03-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p04-starter/package.json`: name=`l2-p04-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p05-starter/package.json`: name=`l2-p05-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p06-starter/package.json`: name=`l2-p06-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p07-starter/package.json`: name=`l2-p07-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p08-starter/package.json`: name=`l2-p08-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p09-starter/package.json`: name=`l2-p09-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p10-starter/package.json`: name=`l2-p10-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p11-starter/package.json`: name=`l2-p11-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p12-starter/package.json`: name=`l2-p12-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p13-starter/package.json`: name=`l2-p13-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p14-starter/package.json`: name=`l2-p14-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l2-p15-starter/package.json`: name=`l2-p15-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p01-starter/package.json`: name=`l3-p01-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p02-starter/package.json`: name=`l3-p02-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p03-starter/package.json`: name=`l3-p03-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p04-starter/package.json`: name=`l3-p04-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p05-starter/package.json`: name=`l3-p05-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p06-starter/package.json`: name=`l3-p06-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p07-starter/package.json`: name=`l3-p07-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p08-starter/package.json`: name=`l3-p08-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p09-starter/package.json`: name=`l3-p09-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p10-starter/package.json`: name=`l3-p10-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p11-starter/package.json`: name=`l3-p11-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p12-starter/package.json`: name=`l3-p12-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p13-starter/package.json`: name=`l3-p13-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p14-starter/package.json`: name=`l3-p14-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `packages/l3-p15-starter/package.json`: name=`l3-p15-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest

### Seminar10_Partea3_p3-standalone.zip

> Structura este mare; se afișează începutul și sfârșitul.

```
L1/L1-P01/solution/README.md
L1/L1-P01/solution/babel.config.cjs
L1/L1-P01/solution/index.html
L1/L1-P01/solution/jest.config.cjs
L1/L1-P01/solution/package.json
L1/L1-P01/solution/src/App.tsx
L1/L1-P01/solution/src/main.tsx
L1/L1-P01/solution/src/styles.css
L1/L1-P01/solution/tests/jest/App.jest.test.tsx
L1/L1-P01/solution/tests/setup.ts
L1/L1-P01/solution/tests/vitest/App.test.tsx
L1/L1-P01/solution/tsconfig.json
L1/L1-P01/solution/vite.config.ts
L1/L1-P01/solution/vitest.config.ts
L1/L1-P01/starter/README.md
L1/L1-P01/starter/babel.config.cjs
L1/L1-P01/starter/index.html
L1/L1-P01/starter/jest.config.cjs
L1/L1-P01/starter/package.json
L1/L1-P01/starter/src/App.tsx
L1/L1-P01/starter/src/main.tsx
L1/L1-P01/starter/src/styles.css
L1/L1-P01/starter/tests/jest/App.jest.test.tsx
L1/L1-P01/starter/tests/setup.ts
L1/L1-P01/starter/tests/vitest/App.test.tsx
L1/L1-P01/starter/tsconfig.json
L1/L1-P01/starter/vite.config.ts
L1/L1-P01/starter/vitest.config.ts
L1/L1-P02/solution/README.md
L1/L1-P02/solution/babel.config.cjs
L1/L1-P02/solution/index.html
L1/L1-P02/solution/jest.config.cjs
L1/L1-P02/solution/package.json
L1/L1-P02/solution/src/App.tsx
L1/L1-P02/solution/src/main.tsx
L1/L1-P02/solution/src/styles.css
L1/L1-P02/solution/tests/jest/App.jest.test.tsx
L1/L1-P02/solution/tests/setup.ts
L1/L1-P02/solution/tests/vitest/App.test.tsx
L1/L1-P02/solution/tsconfig.json
L1/L1-P02/solution/vite.config.ts
L1/L1-P02/solution/vitest.config.ts
L1/L1-P02/starter/README.md
L1/L1-P02/starter/babel.config.cjs
L1/L1-P02/starter/index.html
L1/L1-P02/starter/jest.config.cjs
L1/L1-P02/starter/package.json
L1/L1-P02/starter/src/App.tsx
L1/L1-P02/starter/src/main.tsx
L1/L1-P02/starter/src/styles.css
L1/L1-P02/starter/tests/jest/App.jest.test.tsx
L1/L1-P02/starter/tests/setup.ts
L1/L1-P02/starter/tests/vitest/App.test.tsx
L1/L1-P02/starter/tsconfig.json
L1/L1-P02/starter/vite.config.ts
L1/L1-P02/starter/vitest.config.ts
L1/L1-P03/solution/README.md
L1/L1-P03/solution/babel.config.cjs
L1/L1-P03/solution/index.html
L1/L1-P03/solution/jest.config.cjs
L1/L1-P03/solution/package.json
L1/L1-P03/solution/src/App.tsx
L1/L1-P03/solution/src/main.tsx
L1/L1-P03/solution/src/styles.css
L1/L1-P03/solution/tests/jest/App.jest.test.tsx
L1/L1-P03/solution/tests/setup.ts
L1/L1-P03/solution/tests/vitest/App.test.tsx
L1/L1-P03/solution/tsconfig.json
L1/L1-P03/solution/vite.config.ts
L1/L1-P03/solution/vitest.config.ts
L1/L1-P03/starter/README.md
L1/L1-P03/starter/babel.config.cjs
L1/L1-P03/starter/index.html
L1/L1-P03/starter/jest.config.cjs
L1/L1-P03/starter/package.json
L1/L1-P03/starter/src/App.tsx
L1/L1-P03/starter/src/main.tsx
L1/L1-P03/starter/src/styles.css
L1/L1-P03/starter/tests/jest/App.jest.test.tsx
L1/L1-P03/starter/tests/setup.ts
L1/L1-P03/starter/tests/vitest/App.test.tsx
L1/L1-P03/starter/tsconfig.json
L1/L1-P03/starter/vite.config.ts
L1/L1-P03/starter/vitest.config.ts
L1/L1-P04/solution/README.md
L1/L1-P04/solution/babel.config.cjs
L1/L1-P04/solution/index.html
L1/L1-P04/solution/jest.config.cjs
L1/L1-P04/solution/package.json
L1/L1-P04/solution/src/App.tsx
L1/L1-P04/solution/src/main.tsx
L1/L1-P04/solution/src/styles.css
L1/L1-P04/solution/tests/jest/App.jest.test.tsx
L1/L1-P04/solution/tests/setup.ts
L1/L1-P04/solution/tests/vitest/App.test.tsx
L1/L1-P04/solution/tsconfig.json
L1/L1-P04/solution/vite.config.ts
L1/L1-P04/solution/vitest.config.ts
L1/L1-P04/starter/README.md
L1/L1-P04/starter/babel.config.cjs
L1/L1-P04/starter/index.html
L1/L1-P04/starter/jest.config.cjs
L1/L1-P04/starter/package.json
L1/L1-P04/starter/src/App.tsx
L1/L1-P04/starter/src/main.tsx
L1/L1-P04/starter/src/styles.css
L1/L1-P04/starter/tests/jest/App.jest.test.tsx
L1/L1-P04/starter/tests/setup.ts
L1/L1-P04/starter/tests/vitest/App.test.tsx
L1/L1-P04/starter/tsconfig.json
L1/L1-P04/starter/vite.config.ts
L1/L1-P04/starter/vitest.config.ts
L1/L1-P05/solution/README.md
L1/L1-P05/solution/babel.config.cjs
L1/L1-P05/solution/index.html
L1/L1-P05/solution/jest.config.cjs
L1/L1-P05/solution/package.json
L1/L1-P05/solution/src/App.tsx
L1/L1-P05/solution/src/main.tsx
L1/L1-P05/solution/src/styles.css
L1/L1-P05/solution/tests/jest/App.jest.test.tsx
L1/L1-P05/solution/tests/setup.ts
L1/L1-P05/solution/tests/vitest/App.test.tsx
L1/L1-P05/solution/tsconfig.json
L1/L1-P05/solution/vite.config.ts
L1/L1-P05/solution/vitest.config.ts
L1/L1-P05/starter/README.md
L1/L1-P05/starter/babel.config.cjs
L1/L1-P05/starter/index.html
L1/L1-P05/starter/jest.config.cjs
L1/L1-P05/starter/package.json
L1/L1-P05/starter/src/App.tsx
L1/L1-P05/starter/src/main.tsx
L1/L1-P05/starter/src/styles.css
L1/L1-P05/starter/tests/jest/App.jest.test.tsx
L1/L1-P05/starter/tests/setup.ts
L1/L1-P05/starter/tests/vitest/App.test.tsx
L1/L1-P05/starter/tsconfig.json
L1/L1-P05/starter/vite.config.ts
L1/L1-P05/starter/vitest.config.ts
L1/L1-P06/solution/README.md
L1/L1-P06/solution/babel.config.cjs
L1/L1-P06/solution/index.html
L1/L1-P06/solution/jest.config.cjs
L1/L1-P06/solution/package.json
L1/L1-P06/solution/src/App.tsx
L1/L1-P06/solution/src/main.tsx
L1/L1-P06/solution/src/styles.css
L1/L1-P06/solution/tests/jest/App.jest.test.tsx
L1/L1-P06/solution/tests/setup.ts
L1/L1-P06/solution/tests/vitest/App.test.tsx
L1/L1-P06/solution/tsconfig.json
L1/L1-P06/solution/vite.config.ts
L1/L1-P06/solution/vitest.config.ts
L1/L1-P06/starter/README.md
L1/L1-P06/starter/babel.config.cjs
L1/L1-P06/starter/index.html
L1/L1-P06/starter/jest.config.cjs
L1/L1-P06/starter/package.json
L1/L1-P06/starter/src/App.tsx
L1/L1-P06/starter/src/main.tsx
L1/L1-P06/starter/src/styles.css
L1/L1-P06/starter/tests/jest/App.jest.test.tsx
L1/L1-P06/starter/tests/setup.ts
L1/L1-P06/starter/tests/vitest/App.test.tsx
L1/L1-P06/starter/tsconfig.json
L1/L1-P06/starter/vite.config.ts
L1/L1-P06/starter/vitest.config.ts
L1/L1-P07/solution/README.md
L1/L1-P07/solution/babel.config.cjs
L1/L1-P07/solution/index.html
L1/L1-P07/solution/jest.config.cjs
L1/L1-P07/solution/package.json
L1/L1-P07/solution/src/App.tsx
L1/L1-P07/solution/src/main.tsx
L1/L1-P07/solution/src/styles.css
L1/L1-P07/solution/tests/jest/App.jest.test.tsx
L1/L1-P07/solution/tests/setup.ts
L1/L1-P07/solution/tests/vitest/App.test.tsx
L1/L1-P07/solution/tsconfig.json
L1/L1-P07/solution/vite.config.ts
L1/L1-P07/solution/vitest.config.ts
L1/L1-P07/starter/README.md
L1/L1-P07/starter/babel.config.cjs
L1/L1-P07/starter/index.html
L1/L1-P07/starter/jest.config.cjs
L1/L1-P07/starter/package.json
L1/L1-P07/starter/src/App.tsx
L1/L1-P07/starter/src/main.tsx
L1/L1-P07/starter/src/styles.css
L1/L1-P07/starter/tests/jest/App.jest.test.tsx
L1/L1-P07/starter/tests/setup.ts
L1/L1-P07/starter/tests/vitest/App.test.tsx
L1/L1-P07/starter/tsconfig.json
L1/L1-P07/starter/vite.config.ts
L1/L1-P07/starter/vitest.config.ts
L1/L1-P08/solution/README.md
L1/L1-P08/solution/babel.config.cjs
L1/L1-P08/solution/index.html
L1/L1-P08/solution/jest.config.cjs
L1/L1-P08/solution/package.json
L1/L1-P08/solution/src/App.tsx
L1/L1-P08/solution/src/main.tsx
L1/L1-P08/solution/src/styles.css
L1/L1-P08/solution/tests/jest/App.jest.test.tsx
L1/L1-P08/solution/tests/setup.ts
L1/L1-P08/solution/tests/vitest/App.test.tsx
L1/L1-P08/solution/tsconfig.json
L1/L1-P08/solution/vite.config.ts
L1/L1-P08/solution/vitest.config.ts
L1/L1-P08/starter/README.md
L1/L1-P08/starter/babel.config.cjs
L1/L1-P08/starter/index.html
L1/L1-P08/starter/jest.config.cjs
L1/L1-P08/starter/package.json
L1/L1-P08/starter/src/App.tsx
L1/L1-P08/starter/src/main.tsx
L1/L1-P08/starter/src/styles.css
L1/L1-P08/starter/tests/jest/App.jest.test.tsx
L1/L1-P08/starter/tests/setup.ts
L1/L1-P08/starter/tests/vitest/App.test.tsx
L1/L1-P08/starter/tsconfig.json
L1/L1-P08/starter/vite.config.ts
L1/L1-P08/starter/vitest.config.ts
L1/L1-P09/solution/README.md
L1/L1-P09/solution/babel.config.cjs
L1/L1-P09/solution/index.html
L1/L1-P09/solution/jest.config.cjs
L1/L1-P09/solution/package.json
L1/L1-P09/solution/src/App.tsx
L1/L1-P09/solution/src/main.tsx
L1/L1-P09/solution/src/styles.css
L1/L1-P09/solution/tests/jest/App.jest.test.tsx
L1/L1-P09/solution/tests/setup.ts
L1/L1-P09/solution/tests/vitest/App.test.tsx
L1/L1-P09/solution/tsconfig.json
L1/L1-P09/solution/vite.config.ts
L1/L1-P09/solution/vitest.config.ts
L1/L1-P09/starter/README.md
L1/L1-P09/starter/babel.config.cjs
L1/L1-P09/starter/index.html
L1/L1-P09/starter/jest.config.cjs
L1/L1-P09/starter/package.json
L1/L1-P09/starter/src/App.tsx
L1/L1-P09/starter/src/main.tsx
L1/L1-P09/starter/src/styles.css
L1/L1-P09/starter/tests/jest/App.jest.test.tsx
L1/L1-P09/starter/tests/setup.ts
L1/L1-P09/starter/tests/vitest/App.test.tsx
L1/L1-P09/starter/tsconfig.json
L1/L1-P09/starter/vite.config.ts
L1/L1-P09/starter/vitest.config.ts
L1/L1-P10/solution/README.md
L1/L1-P10/solution/babel.config.cjs
L1/L1-P10/solution/index.html
L1/L1-P10/solution/jest.config.cjs
L1/L1-P10/solution/package.json
L1/L1-P10/solution/src/App.tsx
L1/L1-P10/solution/src/main.tsx
L1/L1-P10/solution/src/styles.css
L1/L1-P10/solution/tests/jest/App.jest.test.tsx
L1/L1-P10/solution/tests/setup.ts
L1/L1-P10/solution/tests/vitest/App.test.tsx
L1/L1-P10/solution/tsconfig.json
L1/L1-P10/solution/vite.config.ts
L1/L1-P10/solution/vitest.config.ts
L1/L1-P10/starter/README.md
L1/L1-P10/starter/babel.config.cjs
L1/L1-P10/starter/index.html
L1/L1-P10/starter/jest.config.cjs
L1/L1-P10/starter/package.json
L1/L1-P10/starter/src/App.tsx
L1/L1-P10/starter/src/main.tsx
L1/L1-P10/starter/src/styles.css
L1/L1-P10/starter/tests/jest/App.jest.test.tsx
L1/L1-P10/starter/tests/setup.ts
L1/L1-P10/starter/tests/vitest/App.test.tsx
L1/L1-P10/starter/tsconfig.json
L1/L1-P10/starter/vite.config.ts
L1/L1-P10/starter/vitest.config.ts
L1/L1-P11/solution/README.md
L1/L1-P11/solution/babel.config.cjs
L1/L1-P11/solution/index.html
L1/L1-P11/solution/jest.config.cjs
L1/L1-P11/solution/package.json
L1/L1-P11/solution/src/App.tsx
L1/L1-P11/solution/src/main.tsx
L1/L1-P11/solution/src/styles.css
L1/L1-P11/solution/tests/jest/App.jest.test.tsx
L1/L1-P11/solution/tests/setup.ts
L1/L1-P11/solution/tests/vitest/App.test.tsx
L1/L1-P11/solution/tsconfig.json
L1/L1-P11/solution/vite.config.ts
L1/L1-P11/solution/vitest.config.ts
L1/L1-P11/starter/README.md
L1/L1-P11/starter/babel.config.cjs
L1/L1-P11/starter/index.html
L1/L1-P11/starter/jest.config.cjs
L1/L1-P11/starter/package.json
L1/L1-P11/starter/src/App.tsx
L1/L1-P11/starter/src/main.tsx
L1/L1-P11/starter/src/styles.css
L1/L1-P11/starter/tests/jest/App.jest.test.tsx
L1/L1-P11/starter/tests/setup.ts
L1/L1-P11/starter/tests/vitest/App.test.tsx
L1/L1-P11/starter/tsconfig.json
L1/L1-P11/starter/vite.config.ts
L1/L1-P11/starter/vitest.config.ts
L1/L1-P12/solution/README.md
L1/L1-P12/solution/babel.config.cjs
L1/L1-P12/solution/index.html
L1/L1-P12/solution/jest.config.cjs
L1/L1-P12/solution/package.json
L1/L1-P12/solution/src/App.tsx
L1/L1-P12/solution/src/main.tsx
L1/L1-P12/solution/src/styles.css
L1/L1-P12/solution/tests/jest/App.jest.test.tsx
L1/L1-P12/solution/tests/setup.ts
L1/L1-P12/solution/tests/vitest/App.test.tsx
L1/L1-P12/solution/tsconfig.json
L1/L1-P12/solution/vite.config.ts
L1/L1-P12/solution/vitest.config.ts
L1/L1-P12/starter/README.md
L1/L1-P12/starter/babel.config.cjs
L1/L1-P12/starter/index.html
L1/L1-P12/starter/jest.config.cjs
L1/L1-P12/starter/package.json
L1/L1-P12/starter/src/App.tsx
L1/L1-P12/starter/src/main.tsx
L1/L1-P12/starter/src/styles.css
L1/L1-P12/starter/tests/jest/App.jest.test.tsx
L1/L1-P12/starter/tests/setup.ts
L1/L1-P12/starter/tests/vitest/App.test.tsx
L1/L1-P12/starter/tsconfig.json
L1/L1-P12/starter/vite.config.ts
L1/L1-P12/starter/vitest.config.ts
L1/L1-P13/solution/README.md
L1/L1-P13/solution/babel.config.cjs
L1/L1-P13/solution/index.html
L1/L1-P13/solution/jest.config.cjs
L1/L1-P13/solution/package.json
L1/L1-P13/solution/src/App.tsx
L1/L1-P13/solution/src/main.tsx
L1/L1-P13/solution/src/styles.css
L1/L1-P13/solution/tests/jest/App.jest.test.tsx
L1/L1-P13/solution/tests/setup.ts
L1/L1-P13/solution/tests/vitest/App.test.tsx
L1/L1-P13/solution/tsconfig.json
L1/L1-P13/solution/vite.config.ts
L1/L1-P13/solution/vitest.config.ts
L1/L1-P13/starter/README.md
L1/L1-P13/starter/babel.config.cjs
L1/L1-P13/starter/index.html
L1/L1-P13/starter/jest.config.cjs
L1/L1-P13/starter/package.json
L1/L1-P13/starter/src/App.tsx
L1/L1-P13/starter/src/main.tsx
L1/L1-P13/starter/src/styles.css
L1/L1-P13/starter/tests/jest/App.jest.test.tsx
L1/L1-P13/starter/tests/setup.ts
L1/L1-P13/starter/tests/vitest/App.test.tsx
L1/L1-P13/starter/tsconfig.json
L1/L1-P13/starter/vite.config.ts
L1/L1-P13/starter/vitest.config.ts
L1/L1-P14/solution/README.md
L1/L1-P14/solution/babel.config.cjs
L1/L1-P14/solution/index.html
L1/L1-P14/solution/jest.config.cjs
L1/L1-P14/solution/package.json
L1/L1-P14/solution/src/App.tsx
L1/L1-P14/solution/src/main.tsx
L1/L1-P14/solution/src/styles.css
L1/L1-P14/solution/tests/jest/App.jest.test.tsx
L1/L1-P14/solution/tests/setup.ts
L1/L1-P14/solution/tests/vitest/App.test.tsx
L1/L1-P14/solution/tsconfig.json
L1/L1-P14/solution/vite.config.ts
L1/L1-P14/solution/vitest.config.ts
L1/L1-P14/starter/README.md
L1/L1-P14/starter/babel.config.cjs
L1/L1-P14/starter/index.html
L1/L1-P14/starter/jest.config.cjs
L1/L1-P14/starter/package.json
L1/L1-P14/starter/src/App.tsx
L1/L1-P14/starter/src/main.tsx
L1/L1-P14/starter/src/styles.css
L1/L1-P14/starter/tests/jest/App.jest.test.tsx
L1/L1-P14/starter/tests/setup.ts
L1/L1-P14/starter/tests/vitest/App.test.tsx
L1/L1-P14/starter/tsconfig.json
L1/L1-P14/starter/vite.config.ts
L1/L1-P14/starter/vitest.config.ts
L1/L1-P15/solution/README.md
L1/L1-P15/solution/babel.config.cjs
L1/L1-P15/solution/index.html
L1/L1-P15/solution/jest.config.cjs
L1/L1-P15/solution/package.json
L1/L1-P15/solution/src/App.tsx
L1/L1-P15/solution/src/main.tsx
L1/L1-P15/solution/src/styles.css
L1/L1-P15/solution/tests/jest/App.jest.test.tsx
L1/L1-P15/solution/tests/setup.ts
L1/L1-P15/solution/tests/vitest/App.test.tsx
L1/L1-P15/solution/tsconfig.json
L1/L1-P15/solution/vite.config.ts
L1/L1-P15/solution/vitest.config.ts
L1/L1-P15/starter/README.md
L1/L1-P15/starter/babel.config.cjs
L1/L1-P15/starter/index.html
L1/L1-P15/starter/jest.config.cjs
L1/L1-P15/starter/package.json
L1/L1-P15/starter/src/App.tsx
L1/L1-P15/starter/src/main.tsx
L1/L1-P15/starter/src/styles.css
L1/L1-P15/starter/tests/jest/App.jest.test.tsx
L1/L1-P15/starter/tests/setup.ts
L1/L1-P15/starter/tests/vitest/App.test.tsx
L1/L1-P15/starter/tsconfig.json
L1/L1-P15/starter/vite.config.ts
L1/L1-P15/starter/vitest.config.ts
L2/L2-P01/solution/README.md
L2/L2-P01/solution/babel.config.cjs
L2/L2-P01/solution/index.html
L2/L2-P01/solution/jest.config.cjs
L2/L2-P01/solution/package.json
L2/L2-P01/solution/src/App.tsx
L2/L2-P01/solution/src/main.tsx
L2/L2-P01/solution/src/styles.css
L2/L2-P01/solution/tests/jest/App.jest.test.tsx
L2/L2-P01/solution/tests/setup.ts
L2/L2-P01/solution/tests/vitest/App.test.tsx
L2/L2-P01/solution/tsconfig.json
L2/L2-P01/solution/vite.config.ts
L2/L2-P01/solution/vitest.config.ts
L2/L2-P01/starter/README.md
L2/L2-P01/starter/babel.config.cjs
L2/L2-P01/starter/index.html
L2/L2-P01/starter/jest.config.cjs
L2/L2-P01/starter/package.json
L2/L2-P01/starter/src/App.tsx
L2/L2-P01/starter/src/main.tsx
L2/L2-P01/starter/src/styles.css
L2/L2-P01/starter/tests/jest/App.jest.test.tsx
L2/L2-P01/starter/tests/setup.ts
L2/L2-P01/starter/tests/vitest/App.test.tsx
L2/L2-P01/starter/tsconfig.json
L2/L2-P01/starter/vite.config.ts
L2/L2-P01/starter/vitest.config.ts
L2/L2-P02/solution/README.md
L2/L2-P02/solution/babel.config.cjs
L2/L2-P02/solution/index.html
L2/L2-P02/solution/jest.config.cjs
L2/L2-P02/solution/package.json
L2/L2-P02/solution/src/App.tsx
L2/L2-P02/solution/src/main.tsx
L2/L2-P02/solution/src/styles.css
L2/L2-P02/solution/tests/jest/App.jest.test.tsx
L2/L2-P02/solution/tests/setup.ts
L2/L2-P02/solution/tests/vitest/App.test.tsx
L2/L2-P02/solution/tsconfig.json
L2/L2-P02/solution/vite.config.ts
L2/L2-P02/solution/vitest.config.ts
L2/L2-P02/starter/README.md
L2/L2-P02/starter/babel.config.cjs
L2/L2-P02/starter/index.html
L2/L2-P02/starter/jest.config.cjs
L2/L2-P02/starter/package.json
L2/L2-P02/starter/src/App.tsx
L2/L2-P02/starter/src/main.tsx
L2/L2-P02/starter/src/styles.css
L2/L2-P02/starter/tests/jest/App.jest.test.tsx
L2/L2-P02/starter/tests/setup.ts
L2/L2-P02/starter/tests/vitest/App.test.tsx
L2/L2-P02/starter/tsconfig.json
L2/L2-P02/starter/vite.config.ts
L2/L2-P02/starter/vitest.config.ts
L2/L2-P03/solution/README.md
L2/L2-P03/solution/babel.config.cjs
L2/L2-P03/solution/index.html
L2/L2-P03/solution/jest.config.cjs
L2/L2-P03/solution/package.json
L2/L2-P03/solution/src/App.tsx
L2/L2-P03/solution/src/main.tsx
L2/L2-P03/solution/src/styles.css
L2/L2-P03/solution/tests/jest/App.jest.test.tsx
L2/L2-P03/solution/tests/setup.ts
L2/L2-P03/solution/tests/vitest/App.test.tsx
L2/L2-P03/solution/tsconfig.json
L2/L2-P03/solution/vite.config.ts
L2/L2-P03/solution/vitest.config.ts
L2/L2-P03/starter/README.md
L2/L2-P03/starter/babel.config.cjs
L2/L2-P03/starter/index.html
L2/L2-P03/starter/jest.config.cjs
L2/L2-P03/starter/package.json
L2/L2-P03/starter/src/App.tsx
L2/L2-P03/starter/src/main.tsx
L2/L2-P03/starter/src/styles.css
L2/L2-P03/starter/tests/jest/App.jest.test.tsx
L2/L2-P03/starter/tests/setup.ts
L2/L2-P03/starter/tests/vitest/App.test.tsx
L2/L2-P03/starter/tsconfig.json
L2/L2-P03/starter/vite.config.ts
L2/L2-P03/starter/vitest.config.ts
L2/L2-P04/solution/README.md
L2/L2-P04/solution/babel.config.cjs
L2/L2-P04/solution/index.html
L2/L2-P04/solution/jest.config.cjs
L2/L2-P04/solution/package.json
L2/L2-P04/solution/src/App.tsx
L2/L2-P04/solution/src/main.tsx
L2/L2-P04/solution/src/styles.css
L2/L2-P04/solution/tests/jest/App.jest.test.tsx
L2/L2-P04/solution/tests/setup.ts
L2/L2-P04/solution/tests/vitest/App.test.tsx
L2/L2-P04/solution/tsconfig.json
L2/L2-P04/solution/vite.config.ts
L2/L2-P04/solution/vitest.config.ts
L2/L2-P04/starter/README.md
L2/L2-P04/starter/babel.config.cjs
L2/L2-P04/starter/index.html
L2/L2-P04/starter/jest.config.cjs
L2/L2-P04/starter/package.json
L2/L2-P04/starter/src/App.tsx
L2/L2-P04/starter/src/main.tsx
L2/L2-P04/starter/src/styles.css
L2/L2-P04/starter/tests/jest/App.jest.test.tsx
L2/L2-P04/starter/tests/setup.ts
L2/L2-P04/starter/tests/vitest/App.test.tsx
L2/L2-P04/starter/tsconfig.json
L2/L2-P04/starter/vite.config.ts
L2/L2-P04/starter/vitest.config.ts
L2/L2-P05/solution/README.md
L2/L2-P05/solution/babel.config.cjs
L2/L2-P05/solution/index.html
L2/L2-P05/solution/jest.config.cjs
L2/L2-P05/solution/package.json
L2/L2-P05/solution/src/App.tsx
L2/L2-P05/solution/src/main.tsx
L2/L2-P05/solution/src/styles.css
L2/L2-P05/solution/tests/jest/App.jest.test.tsx
L2/L2-P05/solution/tests/setup.ts
L2/L2-P05/solution/tests/vitest/App.test.tsx
L2/L2-P05/solution/tsconfig.json
L2/L2-P05/solution/vite.config.ts
L2/L2-P05/solution/vitest.config.ts
L2/L2-P05/starter/README.md
L2/L2-P05/starter/babel.config.cjs
L2/L2-P05/starter/index.html
L2/L2-P05/starter/jest.config.cjs
L2/L2-P05/starter/package.json
L2/L2-P05/starter/src/App.tsx
L2/L2-P05/starter/src/main.tsx
L2/L2-P05/starter/src/styles.css
L2/L2-P05/starter/tests/jest/App.jest.test.tsx
L2/L2-P05/starter/tests/setup.ts
L2/L2-P05/starter/tests/vitest/App.test.tsx
L2/L2-P05/starter/tsconfig.json
L2/L2-P05/starter/vite.config.ts
L2/L2-P05/starter/vitest.config.ts
L2/L2-P06/solution/README.md
L2/L2-P06/solution/babel.config.cjs
L2/L2-P06/solution/index.html
L2/L2-P06/solution/jest.config.cjs
L2/L2-P06/solution/package.json
L2/L2-P06/solution/src/App.tsx
L2/L2-P06/solution/src/main.tsx
L2/L2-P06/solution/src/styles.css
L2/L2-P06/solution/tests/jest/App.jest.test.tsx
L2/L2-P06/solution/tests/setup.ts
L2/L2-P06/solution/tests/vitest/App.test.tsx
L2/L2-P06/solution/tsconfig.json
L2/L2-P06/solution/vite.config.ts
L2/L2-P06/solution/vitest.config.ts
L2/L2-P06/starter/README.md
L2/L2-P06/starter/babel.config.cjs
L2/L2-P06/starter/index.html
L2/L2-P06/starter/jest.config.cjs
L2/L2-P06/starter/package.json
L2/L2-P06/starter/src/App.tsx
L2/L2-P06/starter/src/main.tsx
L2/L2-P06/starter/src/styles.css
L2/L2-P06/starter/tests/jest/App.jest.test.tsx
L2/L2-P06/starter/tests/setup.ts
L2/L2-P06/starter/tests/vitest/App.test.tsx
L2/L2-P06/starter/tsconfig.json
L2/L2-P06/starter/vite.config.ts
L2/L2-P06/starter/vitest.config.ts
L2/L2-P07/solution/README.md
L2/L2-P07/solution/babel.config.cjs
L2/L2-P07/solution/index.html
L2/L2-P07/solution/jest.config.cjs
L2/L2-P07/solution/package.json
L2/L2-P07/solution/src/App.tsx
L2/L2-P07/solution/src/main.tsx
L2/L2-P07/solution/src/styles.css
L2/L2-P07/solution/tests/jest/App.jest.test.tsx
L2/L2-P07/solution/tests/setup.ts
L2/L2-P07/solution/tests/vitest/App.test.tsx
L2/L2-P07/solution/tsconfig.json
…
L2/L2-P09/starter/index.html
L2/L2-P09/starter/jest.config.cjs
L2/L2-P09/starter/package.json
L2/L2-P09/starter/src/App.tsx
L2/L2-P09/starter/src/main.tsx
L2/L2-P09/starter/src/styles.css
L2/L2-P09/starter/tests/jest/App.jest.test.tsx
L2/L2-P09/starter/tests/setup.ts
L2/L2-P09/starter/tests/vitest/App.test.tsx
L2/L2-P09/starter/tsconfig.json
L2/L2-P09/starter/vite.config.ts
L2/L2-P09/starter/vitest.config.ts
L2/L2-P10/solution/README.md
L2/L2-P10/solution/babel.config.cjs
L2/L2-P10/solution/index.html
L2/L2-P10/solution/jest.config.cjs
L2/L2-P10/solution/package.json
L2/L2-P10/solution/src/App.tsx
L2/L2-P10/solution/src/main.tsx
L2/L2-P10/solution/src/styles.css
L2/L2-P10/solution/tests/jest/App.jest.test.tsx
L2/L2-P10/solution/tests/setup.ts
L2/L2-P10/solution/tests/vitest/App.test.tsx
L2/L2-P10/solution/tsconfig.json
L2/L2-P10/solution/vite.config.ts
L2/L2-P10/solution/vitest.config.ts
L2/L2-P10/starter/README.md
L2/L2-P10/starter/babel.config.cjs
L2/L2-P10/starter/index.html
L2/L2-P10/starter/jest.config.cjs
L2/L2-P10/starter/package.json
L2/L2-P10/starter/src/App.tsx
L2/L2-P10/starter/src/main.tsx
L2/L2-P10/starter/src/styles.css
L2/L2-P10/starter/tests/jest/App.jest.test.tsx
L2/L2-P10/starter/tests/setup.ts
L2/L2-P10/starter/tests/vitest/App.test.tsx
L2/L2-P10/starter/tsconfig.json
L2/L2-P10/starter/vite.config.ts
L2/L2-P10/starter/vitest.config.ts
L2/L2-P11/solution/README.md
L2/L2-P11/solution/babel.config.cjs
L2/L2-P11/solution/index.html
L2/L2-P11/solution/jest.config.cjs
L2/L2-P11/solution/package.json
L2/L2-P11/solution/src/App.tsx
L2/L2-P11/solution/src/main.tsx
L2/L2-P11/solution/src/styles.css
L2/L2-P11/solution/tests/jest/App.jest.test.tsx
L2/L2-P11/solution/tests/setup.ts
L2/L2-P11/solution/tests/vitest/App.test.tsx
L2/L2-P11/solution/tsconfig.json
L2/L2-P11/solution/vite.config.ts
L2/L2-P11/solution/vitest.config.ts
L2/L2-P11/starter/README.md
L2/L2-P11/starter/babel.config.cjs
L2/L2-P11/starter/index.html
L2/L2-P11/starter/jest.config.cjs
L2/L2-P11/starter/package.json
L2/L2-P11/starter/src/App.tsx
L2/L2-P11/starter/src/main.tsx
L2/L2-P11/starter/src/styles.css
L2/L2-P11/starter/tests/jest/App.jest.test.tsx
L2/L2-P11/starter/tests/setup.ts
L2/L2-P11/starter/tests/vitest/App.test.tsx
L2/L2-P11/starter/tsconfig.json
L2/L2-P11/starter/vite.config.ts
L2/L2-P11/starter/vitest.config.ts
L2/L2-P12/solution/README.md
L2/L2-P12/solution/babel.config.cjs
L2/L2-P12/solution/index.html
L2/L2-P12/solution/jest.config.cjs
L2/L2-P12/solution/package.json
L2/L2-P12/solution/src/App.tsx
L2/L2-P12/solution/src/main.tsx
L2/L2-P12/solution/src/styles.css
L2/L2-P12/solution/tests/jest/App.jest.test.tsx
L2/L2-P12/solution/tests/setup.ts
L2/L2-P12/solution/tests/vitest/App.test.tsx
L2/L2-P12/solution/tsconfig.json
L2/L2-P12/solution/vite.config.ts
L2/L2-P12/solution/vitest.config.ts
L2/L2-P12/starter/README.md
L2/L2-P12/starter/babel.config.cjs
L2/L2-P12/starter/index.html
L2/L2-P12/starter/jest.config.cjs
L2/L2-P12/starter/package.json
L2/L2-P12/starter/src/App.tsx
L2/L2-P12/starter/src/main.tsx
L2/L2-P12/starter/src/styles.css
L2/L2-P12/starter/tests/jest/App.jest.test.tsx
L2/L2-P12/starter/tests/setup.ts
L2/L2-P12/starter/tests/vitest/App.test.tsx
L2/L2-P12/starter/tsconfig.json
L2/L2-P12/starter/vite.config.ts
L2/L2-P12/starter/vitest.config.ts
L2/L2-P13/solution/README.md
L2/L2-P13/solution/babel.config.cjs
L2/L2-P13/solution/index.html
L2/L2-P13/solution/jest.config.cjs
L2/L2-P13/solution/package.json
L2/L2-P13/solution/src/App.tsx
L2/L2-P13/solution/src/main.tsx
L2/L2-P13/solution/src/styles.css
L2/L2-P13/solution/tests/jest/App.jest.test.tsx
L2/L2-P13/solution/tests/setup.ts
L2/L2-P13/solution/tests/vitest/App.test.tsx
L2/L2-P13/solution/tsconfig.json
L2/L2-P13/solution/vite.config.ts
L2/L2-P13/solution/vitest.config.ts
L2/L2-P13/starter/README.md
L2/L2-P13/starter/babel.config.cjs
L2/L2-P13/starter/index.html
L2/L2-P13/starter/jest.config.cjs
L2/L2-P13/starter/package.json
L2/L2-P13/starter/src/App.tsx
L2/L2-P13/starter/src/main.tsx
L2/L2-P13/starter/src/styles.css
L2/L2-P13/starter/tests/jest/App.jest.test.tsx
L2/L2-P13/starter/tests/setup.ts
L2/L2-P13/starter/tests/vitest/App.test.tsx
L2/L2-P13/starter/tsconfig.json
L2/L2-P13/starter/vite.config.ts
L2/L2-P13/starter/vitest.config.ts
L2/L2-P14/solution/README.md
L2/L2-P14/solution/babel.config.cjs
L2/L2-P14/solution/index.html
L2/L2-P14/solution/jest.config.cjs
L2/L2-P14/solution/package.json
L2/L2-P14/solution/src/App.tsx
L2/L2-P14/solution/src/main.tsx
L2/L2-P14/solution/src/styles.css
L2/L2-P14/solution/tests/jest/App.jest.test.tsx
L2/L2-P14/solution/tests/setup.ts
L2/L2-P14/solution/tests/vitest/App.test.tsx
L2/L2-P14/solution/tsconfig.json
L2/L2-P14/solution/vite.config.ts
L2/L2-P14/solution/vitest.config.ts
L2/L2-P14/starter/README.md
L2/L2-P14/starter/babel.config.cjs
L2/L2-P14/starter/index.html
L2/L2-P14/starter/jest.config.cjs
L2/L2-P14/starter/package.json
L2/L2-P14/starter/src/App.tsx
L2/L2-P14/starter/src/main.tsx
L2/L2-P14/starter/src/styles.css
L2/L2-P14/starter/tests/jest/App.jest.test.tsx
L2/L2-P14/starter/tests/setup.ts
L2/L2-P14/starter/tests/vitest/App.test.tsx
L2/L2-P14/starter/tsconfig.json
L2/L2-P14/starter/vite.config.ts
L2/L2-P14/starter/vitest.config.ts
L2/L2-P15/solution/README.md
L2/L2-P15/solution/babel.config.cjs
L2/L2-P15/solution/index.html
L2/L2-P15/solution/jest.config.cjs
L2/L2-P15/solution/package.json
L2/L2-P15/solution/src/App.tsx
L2/L2-P15/solution/src/main.tsx
L2/L2-P15/solution/src/styles.css
L2/L2-P15/solution/tests/jest/App.jest.test.tsx
L2/L2-P15/solution/tests/setup.ts
L2/L2-P15/solution/tests/vitest/App.test.tsx
L2/L2-P15/solution/tsconfig.json
L2/L2-P15/solution/vite.config.ts
L2/L2-P15/solution/vitest.config.ts
L2/L2-P15/starter/README.md
L2/L2-P15/starter/babel.config.cjs
L2/L2-P15/starter/index.html
L2/L2-P15/starter/jest.config.cjs
L2/L2-P15/starter/package.json
L2/L2-P15/starter/src/App.tsx
L2/L2-P15/starter/src/main.tsx
L2/L2-P15/starter/src/styles.css
L2/L2-P15/starter/tests/jest/App.jest.test.tsx
L2/L2-P15/starter/tests/setup.ts
L2/L2-P15/starter/tests/vitest/App.test.tsx
L2/L2-P15/starter/tsconfig.json
L2/L2-P15/starter/vite.config.ts
L2/L2-P15/starter/vitest.config.ts
L3/L3-P01/solution/README.md
L3/L3-P01/solution/babel.config.cjs
L3/L3-P01/solution/index.html
L3/L3-P01/solution/jest.config.cjs
L3/L3-P01/solution/package.json
L3/L3-P01/solution/src/App.tsx
L3/L3-P01/solution/src/main.tsx
L3/L3-P01/solution/src/styles.css
L3/L3-P01/solution/tests/jest/App.jest.test.tsx
L3/L3-P01/solution/tests/setup.ts
L3/L3-P01/solution/tests/vitest/App.test.tsx
L3/L3-P01/solution/tsconfig.json
L3/L3-P01/solution/vite.config.ts
L3/L3-P01/solution/vitest.config.ts
L3/L3-P01/starter/README.md
L3/L3-P01/starter/babel.config.cjs
L3/L3-P01/starter/index.html
L3/L3-P01/starter/jest.config.cjs
L3/L3-P01/starter/package.json
L3/L3-P01/starter/src/App.tsx
L3/L3-P01/starter/src/main.tsx
L3/L3-P01/starter/src/styles.css
L3/L3-P01/starter/tests/jest/App.jest.test.tsx
L3/L3-P01/starter/tests/setup.ts
L3/L3-P01/starter/tests/vitest/App.test.tsx
L3/L3-P01/starter/tsconfig.json
L3/L3-P01/starter/vite.config.ts
L3/L3-P01/starter/vitest.config.ts
L3/L3-P02/solution/README.md
L3/L3-P02/solution/babel.config.cjs
L3/L3-P02/solution/index.html
L3/L3-P02/solution/jest.config.cjs
L3/L3-P02/solution/package.json
L3/L3-P02/solution/src/App.tsx
L3/L3-P02/solution/src/main.tsx
L3/L3-P02/solution/src/styles.css
L3/L3-P02/solution/tests/jest/App.jest.test.tsx
L3/L3-P02/solution/tests/setup.ts
L3/L3-P02/solution/tests/vitest/App.test.tsx
L3/L3-P02/solution/tsconfig.json
L3/L3-P02/solution/vite.config.ts
L3/L3-P02/solution/vitest.config.ts
L3/L3-P02/starter/README.md
L3/L3-P02/starter/babel.config.cjs
L3/L3-P02/starter/index.html
L3/L3-P02/starter/jest.config.cjs
L3/L3-P02/starter/package.json
L3/L3-P02/starter/src/App.tsx
L3/L3-P02/starter/src/main.tsx
L3/L3-P02/starter/src/styles.css
L3/L3-P02/starter/tests/jest/App.jest.test.tsx
L3/L3-P02/starter/tests/setup.ts
L3/L3-P02/starter/tests/vitest/App.test.tsx
L3/L3-P02/starter/tsconfig.json
L3/L3-P02/starter/vite.config.ts
L3/L3-P02/starter/vitest.config.ts
L3/L3-P03/solution/README.md
L3/L3-P03/solution/babel.config.cjs
L3/L3-P03/solution/index.html
L3/L3-P03/solution/jest.config.cjs
L3/L3-P03/solution/package.json
L3/L3-P03/solution/src/App.tsx
L3/L3-P03/solution/src/main.tsx
L3/L3-P03/solution/src/styles.css
L3/L3-P03/solution/tests/jest/App.jest.test.tsx
L3/L3-P03/solution/tests/setup.ts
L3/L3-P03/solution/tests/vitest/App.test.tsx
L3/L3-P03/solution/tsconfig.json
L3/L3-P03/solution/vite.config.ts
L3/L3-P03/solution/vitest.config.ts
L3/L3-P03/starter/README.md
L3/L3-P03/starter/babel.config.cjs
L3/L3-P03/starter/index.html
L3/L3-P03/starter/jest.config.cjs
L3/L3-P03/starter/package.json
L3/L3-P03/starter/src/App.tsx
L3/L3-P03/starter/src/main.tsx
L3/L3-P03/starter/src/styles.css
L3/L3-P03/starter/tests/jest/App.jest.test.tsx
L3/L3-P03/starter/tests/setup.ts
L3/L3-P03/starter/tests/vitest/App.test.tsx
L3/L3-P03/starter/tsconfig.json
L3/L3-P03/starter/vite.config.ts
L3/L3-P03/starter/vitest.config.ts
L3/L3-P04/solution/README.md
L3/L3-P04/solution/babel.config.cjs
L3/L3-P04/solution/index.html
L3/L3-P04/solution/jest.config.cjs
L3/L3-P04/solution/package.json
L3/L3-P04/solution/src/App.tsx
L3/L3-P04/solution/src/main.tsx
L3/L3-P04/solution/src/styles.css
L3/L3-P04/solution/tests/jest/App.jest.test.tsx
L3/L3-P04/solution/tests/setup.ts
L3/L3-P04/solution/tests/vitest/App.test.tsx
L3/L3-P04/solution/tsconfig.json
L3/L3-P04/solution/vite.config.ts
L3/L3-P04/solution/vitest.config.ts
L3/L3-P04/starter/README.md
L3/L3-P04/starter/babel.config.cjs
L3/L3-P04/starter/index.html
L3/L3-P04/starter/jest.config.cjs
L3/L3-P04/starter/package.json
L3/L3-P04/starter/src/App.tsx
L3/L3-P04/starter/src/main.tsx
L3/L3-P04/starter/src/styles.css
L3/L3-P04/starter/tests/jest/App.jest.test.tsx
L3/L3-P04/starter/tests/setup.ts
L3/L3-P04/starter/tests/vitest/App.test.tsx
L3/L3-P04/starter/tsconfig.json
L3/L3-P04/starter/vite.config.ts
L3/L3-P04/starter/vitest.config.ts
L3/L3-P05/solution/README.md
L3/L3-P05/solution/babel.config.cjs
L3/L3-P05/solution/index.html
L3/L3-P05/solution/jest.config.cjs
L3/L3-P05/solution/package.json
L3/L3-P05/solution/src/App.tsx
L3/L3-P05/solution/src/main.tsx
L3/L3-P05/solution/src/styles.css
L3/L3-P05/solution/tests/jest/App.jest.test.tsx
L3/L3-P05/solution/tests/setup.ts
L3/L3-P05/solution/tests/vitest/App.test.tsx
L3/L3-P05/solution/tsconfig.json
L3/L3-P05/solution/vite.config.ts
L3/L3-P05/solution/vitest.config.ts
L3/L3-P05/starter/README.md
L3/L3-P05/starter/babel.config.cjs
L3/L3-P05/starter/index.html
L3/L3-P05/starter/jest.config.cjs
L3/L3-P05/starter/package.json
L3/L3-P05/starter/src/App.tsx
L3/L3-P05/starter/src/main.tsx
L3/L3-P05/starter/src/styles.css
L3/L3-P05/starter/tests/jest/App.jest.test.tsx
L3/L3-P05/starter/tests/setup.ts
L3/L3-P05/starter/tests/vitest/App.test.tsx
L3/L3-P05/starter/tsconfig.json
L3/L3-P05/starter/vite.config.ts
L3/L3-P05/starter/vitest.config.ts
L3/L3-P06/solution/README.md
L3/L3-P06/solution/babel.config.cjs
L3/L3-P06/solution/index.html
L3/L3-P06/solution/jest.config.cjs
L3/L3-P06/solution/package.json
L3/L3-P06/solution/src/App.tsx
L3/L3-P06/solution/src/main.tsx
L3/L3-P06/solution/src/styles.css
L3/L3-P06/solution/tests/jest/App.jest.test.tsx
L3/L3-P06/solution/tests/setup.ts
L3/L3-P06/solution/tests/vitest/App.test.tsx
L3/L3-P06/solution/tsconfig.json
L3/L3-P06/solution/vite.config.ts
L3/L3-P06/solution/vitest.config.ts
L3/L3-P06/starter/README.md
L3/L3-P06/starter/babel.config.cjs
L3/L3-P06/starter/index.html
L3/L3-P06/starter/jest.config.cjs
L3/L3-P06/starter/package.json
L3/L3-P06/starter/src/App.tsx
L3/L3-P06/starter/src/main.tsx
L3/L3-P06/starter/src/styles.css
L3/L3-P06/starter/tests/jest/App.jest.test.tsx
L3/L3-P06/starter/tests/setup.ts
L3/L3-P06/starter/tests/vitest/App.test.tsx
L3/L3-P06/starter/tsconfig.json
L3/L3-P06/starter/vite.config.ts
L3/L3-P06/starter/vitest.config.ts
L3/L3-P07/solution/README.md
L3/L3-P07/solution/babel.config.cjs
L3/L3-P07/solution/index.html
L3/L3-P07/solution/jest.config.cjs
L3/L3-P07/solution/package.json
L3/L3-P07/solution/src/App.tsx
L3/L3-P07/solution/src/main.tsx
L3/L3-P07/solution/src/styles.css
L3/L3-P07/solution/tests/jest/App.jest.test.tsx
L3/L3-P07/solution/tests/setup.ts
L3/L3-P07/solution/tests/vitest/App.test.tsx
L3/L3-P07/solution/tsconfig.json
L3/L3-P07/solution/vite.config.ts
L3/L3-P07/solution/vitest.config.ts
L3/L3-P07/starter/README.md
L3/L3-P07/starter/babel.config.cjs
L3/L3-P07/starter/index.html
L3/L3-P07/starter/jest.config.cjs
L3/L3-P07/starter/package.json
L3/L3-P07/starter/src/App.tsx
L3/L3-P07/starter/src/main.tsx
L3/L3-P07/starter/src/styles.css
L3/L3-P07/starter/tests/jest/App.jest.test.tsx
L3/L3-P07/starter/tests/setup.ts
L3/L3-P07/starter/tests/vitest/App.test.tsx
L3/L3-P07/starter/tsconfig.json
L3/L3-P07/starter/vite.config.ts
L3/L3-P07/starter/vitest.config.ts
L3/L3-P08/solution/README.md
L3/L3-P08/solution/babel.config.cjs
L3/L3-P08/solution/index.html
L3/L3-P08/solution/jest.config.cjs
L3/L3-P08/solution/package.json
L3/L3-P08/solution/src/App.tsx
L3/L3-P08/solution/src/main.tsx
L3/L3-P08/solution/src/styles.css
L3/L3-P08/solution/tests/jest/App.jest.test.tsx
L3/L3-P08/solution/tests/setup.ts
L3/L3-P08/solution/tests/vitest/App.test.tsx
L3/L3-P08/solution/tsconfig.json
L3/L3-P08/solution/vite.config.ts
L3/L3-P08/solution/vitest.config.ts
L3/L3-P08/starter/README.md
L3/L3-P08/starter/babel.config.cjs
L3/L3-P08/starter/index.html
L3/L3-P08/starter/jest.config.cjs
L3/L3-P08/starter/package.json
L3/L3-P08/starter/src/App.tsx
L3/L3-P08/starter/src/main.tsx
L3/L3-P08/starter/src/styles.css
L3/L3-P08/starter/tests/jest/App.jest.test.tsx
L3/L3-P08/starter/tests/setup.ts
L3/L3-P08/starter/tests/vitest/App.test.tsx
L3/L3-P08/starter/tsconfig.json
L3/L3-P08/starter/vite.config.ts
L3/L3-P08/starter/vitest.config.ts
L3/L3-P09/solution/README.md
L3/L3-P09/solution/babel.config.cjs
L3/L3-P09/solution/index.html
L3/L3-P09/solution/jest.config.cjs
L3/L3-P09/solution/package.json
L3/L3-P09/solution/src/App.tsx
L3/L3-P09/solution/src/main.tsx
L3/L3-P09/solution/src/styles.css
L3/L3-P09/solution/tests/jest/App.jest.test.tsx
L3/L3-P09/solution/tests/setup.ts
L3/L3-P09/solution/tests/vitest/App.test.tsx
L3/L3-P09/solution/tsconfig.json
L3/L3-P09/solution/vite.config.ts
L3/L3-P09/solution/vitest.config.ts
L3/L3-P09/starter/README.md
L3/L3-P09/starter/babel.config.cjs
L3/L3-P09/starter/index.html
L3/L3-P09/starter/jest.config.cjs
L3/L3-P09/starter/package.json
L3/L3-P09/starter/src/App.tsx
L3/L3-P09/starter/src/main.tsx
L3/L3-P09/starter/src/styles.css
L3/L3-P09/starter/tests/jest/App.jest.test.tsx
L3/L3-P09/starter/tests/setup.ts
L3/L3-P09/starter/tests/vitest/App.test.tsx
L3/L3-P09/starter/tsconfig.json
L3/L3-P09/starter/vite.config.ts
L3/L3-P09/starter/vitest.config.ts
L3/L3-P10/solution/README.md
L3/L3-P10/solution/babel.config.cjs
L3/L3-P10/solution/index.html
L3/L3-P10/solution/jest.config.cjs
L3/L3-P10/solution/package.json
L3/L3-P10/solution/src/App.tsx
L3/L3-P10/solution/src/main.tsx
L3/L3-P10/solution/src/styles.css
L3/L3-P10/solution/tests/jest/App.jest.test.tsx
L3/L3-P10/solution/tests/setup.ts
L3/L3-P10/solution/tests/vitest/App.test.tsx
L3/L3-P10/solution/tsconfig.json
L3/L3-P10/solution/vite.config.ts
L3/L3-P10/solution/vitest.config.ts
L3/L3-P10/starter/README.md
L3/L3-P10/starter/babel.config.cjs
L3/L3-P10/starter/index.html
L3/L3-P10/starter/jest.config.cjs
L3/L3-P10/starter/package.json
L3/L3-P10/starter/src/App.tsx
L3/L3-P10/starter/src/main.tsx
L3/L3-P10/starter/src/styles.css
L3/L3-P10/starter/tests/jest/App.jest.test.tsx
L3/L3-P10/starter/tests/setup.ts
L3/L3-P10/starter/tests/vitest/App.test.tsx
L3/L3-P10/starter/tsconfig.json
L3/L3-P10/starter/vite.config.ts
L3/L3-P10/starter/vitest.config.ts
L3/L3-P11/solution/README.md
L3/L3-P11/solution/babel.config.cjs
L3/L3-P11/solution/index.html
L3/L3-P11/solution/jest.config.cjs
L3/L3-P11/solution/package.json
L3/L3-P11/solution/src/App.tsx
L3/L3-P11/solution/src/main.tsx
L3/L3-P11/solution/src/styles.css
L3/L3-P11/solution/tests/jest/App.jest.test.tsx
L3/L3-P11/solution/tests/setup.ts
L3/L3-P11/solution/tests/vitest/App.test.tsx
L3/L3-P11/solution/tsconfig.json
L3/L3-P11/solution/vite.config.ts
L3/L3-P11/solution/vitest.config.ts
L3/L3-P11/starter/README.md
L3/L3-P11/starter/babel.config.cjs
L3/L3-P11/starter/index.html
L3/L3-P11/starter/jest.config.cjs
L3/L3-P11/starter/package.json
L3/L3-P11/starter/src/App.tsx
L3/L3-P11/starter/src/main.tsx
L3/L3-P11/starter/src/styles.css
L3/L3-P11/starter/tests/jest/App.jest.test.tsx
L3/L3-P11/starter/tests/setup.ts
L3/L3-P11/starter/tests/vitest/App.test.tsx
L3/L3-P11/starter/tsconfig.json
L3/L3-P11/starter/vite.config.ts
L3/L3-P11/starter/vitest.config.ts
L3/L3-P12/solution/README.md
L3/L3-P12/solution/babel.config.cjs
L3/L3-P12/solution/index.html
L3/L3-P12/solution/jest.config.cjs
L3/L3-P12/solution/package.json
L3/L3-P12/solution/src/App.tsx
L3/L3-P12/solution/src/main.tsx
L3/L3-P12/solution/src/styles.css
L3/L3-P12/solution/tests/jest/App.jest.test.tsx
L3/L3-P12/solution/tests/setup.ts
L3/L3-P12/solution/tests/vitest/App.test.tsx
L3/L3-P12/solution/tsconfig.json
L3/L3-P12/solution/vite.config.ts
L3/L3-P12/solution/vitest.config.ts
L3/L3-P12/starter/README.md
L3/L3-P12/starter/babel.config.cjs
L3/L3-P12/starter/index.html
L3/L3-P12/starter/jest.config.cjs
L3/L3-P12/starter/package.json
L3/L3-P12/starter/src/App.tsx
L3/L3-P12/starter/src/main.tsx
L3/L3-P12/starter/src/styles.css
L3/L3-P12/starter/tests/jest/App.jest.test.tsx
L3/L3-P12/starter/tests/setup.ts
L3/L3-P12/starter/tests/vitest/App.test.tsx
L3/L3-P12/starter/tsconfig.json
L3/L3-P12/starter/vite.config.ts
L3/L3-P12/starter/vitest.config.ts
L3/L3-P13/solution/README.md
L3/L3-P13/solution/babel.config.cjs
L3/L3-P13/solution/index.html
L3/L3-P13/solution/jest.config.cjs
L3/L3-P13/solution/package.json
L3/L3-P13/solution/src/App.tsx
L3/L3-P13/solution/src/main.tsx
L3/L3-P13/solution/src/styles.css
L3/L3-P13/solution/tests/jest/App.jest.test.tsx
L3/L3-P13/solution/tests/setup.ts
L3/L3-P13/solution/tests/vitest/App.test.tsx
L3/L3-P13/solution/tsconfig.json
L3/L3-P13/solution/vite.config.ts
L3/L3-P13/solution/vitest.config.ts
L3/L3-P13/starter/README.md
L3/L3-P13/starter/babel.config.cjs
L3/L3-P13/starter/index.html
L3/L3-P13/starter/jest.config.cjs
L3/L3-P13/starter/package.json
L3/L3-P13/starter/src/App.tsx
L3/L3-P13/starter/src/main.tsx
L3/L3-P13/starter/src/styles.css
L3/L3-P13/starter/tests/jest/App.jest.test.tsx
L3/L3-P13/starter/tests/setup.ts
L3/L3-P13/starter/tests/vitest/App.test.tsx
L3/L3-P13/starter/tsconfig.json
L3/L3-P13/starter/vite.config.ts
L3/L3-P13/starter/vitest.config.ts
L3/L3-P14/solution/README.md
L3/L3-P14/solution/babel.config.cjs
L3/L3-P14/solution/index.html
L3/L3-P14/solution/jest.config.cjs
L3/L3-P14/solution/package.json
L3/L3-P14/solution/src/App.tsx
L3/L3-P14/solution/src/main.tsx
L3/L3-P14/solution/src/styles.css
L3/L3-P14/solution/tests/jest/App.jest.test.tsx
L3/L3-P14/solution/tests/setup.ts
L3/L3-P14/solution/tests/vitest/App.test.tsx
L3/L3-P14/solution/tsconfig.json
L3/L3-P14/solution/vite.config.ts
L3/L3-P14/solution/vitest.config.ts
L3/L3-P14/starter/README.md
L3/L3-P14/starter/babel.config.cjs
L3/L3-P14/starter/index.html
L3/L3-P14/starter/jest.config.cjs
L3/L3-P14/starter/package.json
L3/L3-P14/starter/src/App.tsx
L3/L3-P14/starter/src/main.tsx
L3/L3-P14/starter/src/styles.css
L3/L3-P14/starter/tests/jest/App.jest.test.tsx
L3/L3-P14/starter/tests/setup.ts
L3/L3-P14/starter/tests/vitest/App.test.tsx
L3/L3-P14/starter/tsconfig.json
L3/L3-P14/starter/vite.config.ts
L3/L3-P14/starter/vitest.config.ts
L3/L3-P15/solution/README.md
L3/L3-P15/solution/babel.config.cjs
L3/L3-P15/solution/index.html
L3/L3-P15/solution/jest.config.cjs
L3/L3-P15/solution/package.json
L3/L3-P15/solution/src/App.tsx
L3/L3-P15/solution/src/main.tsx
L3/L3-P15/solution/src/styles.css
L3/L3-P15/solution/tests/jest/App.jest.test.tsx
L3/L3-P15/solution/tests/setup.ts
L3/L3-P15/solution/tests/vitest/App.test.tsx
L3/L3-P15/solution/tsconfig.json
L3/L3-P15/solution/vite.config.ts
L3/L3-P15/solution/vitest.config.ts
L3/L3-P15/starter/README.md
L3/L3-P15/starter/babel.config.cjs
L3/L3-P15/starter/index.html
L3/L3-P15/starter/jest.config.cjs
L3/L3-P15/starter/package.json
L3/L3-P15/starter/src/App.tsx
L3/L3-P15/starter/src/main.tsx
L3/L3-P15/starter/src/styles.css
L3/L3-P15/starter/tests/jest/App.jest.test.tsx
L3/L3-P15/starter/tests/setup.ts
L3/L3-P15/starter/tests/vitest/App.test.tsx
L3/L3-P15/starter/tsconfig.json
L3/L3-P15/starter/vite.config.ts
L3/L3-P15/starter/vitest.config.ts
```

**Variante detectate:** solution: 630, starter: 630.

**Categorii de fișiere:** config: 540, public: 90, docs: 90, code: 270, tests: 270.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `L1/L1-P01/starter/package.json`: name=`l1-p01-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P01/solution/package.json`: name=`l1-p01-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P02/starter/package.json`: name=`l1-p02-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P02/solution/package.json`: name=`l1-p02-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P03/starter/package.json`: name=`l1-p03-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P03/solution/package.json`: name=`l1-p03-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P04/starter/package.json`: name=`l1-p04-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P04/solution/package.json`: name=`l1-p04-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P05/starter/package.json`: name=`l1-p05-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P05/solution/package.json`: name=`l1-p05-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P06/starter/package.json`: name=`l1-p06-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P06/solution/package.json`: name=`l1-p06-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P07/starter/package.json`: name=`l1-p07-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P07/solution/package.json`: name=`l1-p07-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P08/starter/package.json`: name=`l1-p08-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P08/solution/package.json`: name=`l1-p08-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P09/starter/package.json`: name=`l1-p09-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P09/solution/package.json`: name=`l1-p09-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P10/starter/package.json`: name=`l1-p10-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P10/solution/package.json`: name=`l1-p10-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P11/starter/package.json`: name=`l1-p11-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P11/solution/package.json`: name=`l1-p11-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P12/starter/package.json`: name=`l1-p12-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P12/solution/package.json`: name=`l1-p12-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P13/starter/package.json`: name=`l1-p13-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P13/solution/package.json`: name=`l1-p13-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P14/starter/package.json`: name=`l1-p14-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P14/solution/package.json`: name=`l1-p14-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P15/starter/package.json`: name=`l1-p15-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L1/L1-P15/solution/package.json`: name=`l1-p15-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P01/starter/package.json`: name=`l2-p01-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P01/solution/package.json`: name=`l2-p01-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P02/starter/package.json`: name=`l2-p02-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P02/solution/package.json`: name=`l2-p02-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P03/starter/package.json`: name=`l2-p03-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P03/solution/package.json`: name=`l2-p03-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P04/starter/package.json`: name=`l2-p04-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P04/solution/package.json`: name=`l2-p04-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P05/starter/package.json`: name=`l2-p05-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P05/solution/package.json`: name=`l2-p05-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P06/starter/package.json`: name=`l2-p06-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P06/solution/package.json`: name=`l2-p06-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P07/starter/package.json`: name=`l2-p07-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P07/solution/package.json`: name=`l2-p07-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P08/starter/package.json`: name=`l2-p08-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P08/solution/package.json`: name=`l2-p08-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P09/starter/package.json`: name=`l2-p09-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P09/solution/package.json`: name=`l2-p09-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P10/starter/package.json`: name=`l2-p10-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P10/solution/package.json`: name=`l2-p10-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P11/starter/package.json`: name=`l2-p11-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P11/solution/package.json`: name=`l2-p11-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P12/starter/package.json`: name=`l2-p12-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P12/solution/package.json`: name=`l2-p12-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P13/starter/package.json`: name=`l2-p13-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P13/solution/package.json`: name=`l2-p13-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P14/starter/package.json`: name=`l2-p14-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P14/solution/package.json`: name=`l2-p14-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P15/starter/package.json`: name=`l2-p15-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L2/L2-P15/solution/package.json`: name=`l2-p15-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P01/starter/package.json`: name=`l3-p01-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P01/solution/package.json`: name=`l3-p01-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P02/starter/package.json`: name=`l3-p02-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P02/solution/package.json`: name=`l3-p02-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P03/starter/package.json`: name=`l3-p03-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P03/solution/package.json`: name=`l3-p03-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P04/starter/package.json`: name=`l3-p04-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P04/solution/package.json`: name=`l3-p04-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P05/starter/package.json`: name=`l3-p05-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P05/solution/package.json`: name=`l3-p05-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P06/starter/package.json`: name=`l3-p06-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P06/solution/package.json`: name=`l3-p06-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P07/starter/package.json`: name=`l3-p07-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P07/solution/package.json`: name=`l3-p07-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P08/starter/package.json`: name=`l3-p08-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P08/solution/package.json`: name=`l3-p08-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P09/starter/package.json`: name=`l3-p09-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P09/solution/package.json`: name=`l3-p09-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P10/starter/package.json`: name=`l3-p10-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P10/solution/package.json`: name=`l3-p10-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P11/starter/package.json`: name=`l3-p11-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P11/solution/package.json`: name=`l3-p11-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P12/starter/package.json`: name=`l3-p12-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P12/solution/package.json`: name=`l3-p12-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P13/starter/package.json`: name=`l3-p13-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P13/solution/package.json`: name=`l3-p13-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P14/starter/package.json`: name=`l3-p14-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P14/solution/package.json`: name=`l3-p14-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P15/starter/package.json`: name=`l3-p15-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest
- `L3/L3-P15/solution/package.json`: name=`l3-p15-react` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** react, react-dom
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, typescript, vite, vitest

### Seminar10_Partea3_p3-READMEs.zip

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

### Seminar10_Partea1_React_Componente_JSX.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 10 — React: componente și JSX — Partea 1 (Teorie)
- **Context didactic şi ţintă:** Această Parte 1 este o **introducere riguroasă şi narativă** în React (componente funcţionale şi **JSX**), aliniată la **React 19** şi la modul în care documentaţia oficială recomandă să începem proiectele moderne: cu un **build tool** precum **Vite/Parcel/Rsbuild** şi o gândire „**Thinking in React**” asupra structurării UI‑ului. În tot textul, termenii tehnici şi comenzile vor rămâne în **English** (unde se potriveşte), iar explicaţiile conceptuale sunt în **română**, cu analogii din lumea reală. Vom face şi trimiteri precise la documentaţia oficială acolo unde contează, pentru a evita mitologii sau practici depăşite.
- # 0. Hook realist: de ce React, de ce acum (şi de ce JSX)?

### Seminar10_Partea2_React_Laborator.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 10 — React: componente și JSX — Partea 2 (Laborator extins)
- **Scopul Părții 2** este să construim, *end‑to‑end*, o aplicație didactică „**ClubHub**” în **React 19** cu **Vite** și **TypeScript**, prin exerciții progresive ce ating esența subiectului „Componente și JSX”: *props/state*, *events*, *lists & keys*, *controlled forms*, *composition*, cu un prim contact disciplinat cu *transitions* (non‑blocking updates). Fiecare etapă are: **worksheet (cerință + checklist)**, **cod** (starter + completare), **teste** **Vitest & Jest** (side‑by‑side), și **AI‑assist (VSL)**.
- ---
## 0) Setup: proiect Vite + React (TS) și configurarea testelor (Vitest & Jest)
(Conținut identic cu livrarea anterioară: cerințe, comenzi, explicații, checklist)
---
## 1) Componente & JSX (Header, Footer, ClubCard)
(Conținut identic: cerințe, explicații, teste, AI‑assist)
---
## 2) State & Events (SearchBox controlat + filtrare listă)
...
---
## 3) Lists & keys (ClubList cu `key` stabil)
...
---
## 4) Controlled forms (AddClubForm)
...
---
## 5) Composition & children
...
---
## 6) Performance primer (startTransition)
...
---
## 7) Refactoring + a11y pass
...
---
## Codul livrat (în arhiva ZIP)
...
---
## AI‑assist (VSL) — prompts
...
---
## Troubleshooting
...
---
## Extensii
...

### Seminar10_Partea3_Arhive_Ghid.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhive (Seminarul 10, Partea 3)
- **Arhive livrate:** s10p3-standalone.zip (toate proiectele, starter + solution), s10p3-monorepo.zip (toți starterii), s10p3-readmes.zip (toate README).
- **Rulare standalone:** `cd L1/L1-P01/starter && npm i && npm test && npm run dev`.

### Seminar10_Partea3_React_Proiecte_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 10 — React: componente și JSX — Partea 3 (Proiecte/teme, extins)
- **Structură generală:** 45 proiecte (15 × L1, 15 × L2, 15 × L3). Fiecare are `starter/` + `solution/`, teste Vitest & Jest, README cu cerințe și pași.
- # L1 (Fundamental)

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
| `tsconfig.json` | Setări TypeScript (strict, jsx, paths). |
| `vite.config.ts` | Config Vite (plugin React, aliasuri, test include). |
| `vitest.config.ts` | Configurarea Vitest (JSDOM/Node, reporters, setup). |
| `jest.config.cjs` | Configurarea Jest (JSDOM, transform TSX cu `babel-jest`). |
| `babel.config.cjs` | Preseturi Babel pentru Jest (env/react/typescript). |
| `index.html` | Punct de intrare HTML (Vite). |
| `src/App.tsx` | Compoziția principală UI: titlu, căutare controlată, listă, formular. |
| `src/hooks/useFilteredClubs.ts` | Hook personalizat pentru filtrare memoizată. |

## 5. Corelații cod ↔ configurări ↔ teste


- **Componentele & rutele UI** din `src/App.tsx` și `src/components/*` sunt verificate prin suite **Vitest** și **Jest** (aceleași aserții cu RTL).  
- **`.env.example`**: variabilele `VITE_*` se propagă în build-ul Vite; restul pot fi folosite în scripturi/CI.  
- **ESLint + CI**: pipeline-urile (`.github/workflows/*`) rulează `lint` și `test`, blocând PR-uri cu erori.  
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S10 constituie o introducere aplicată în **React (componente & JSX)**, cu **testare duală** (Vitest & Jest) și standardizare pe **Vite + TypeScript**. Teoria (Partea 1) este mapată direct în laborator (Partea 2) și proiecte (Partea 3), astfel încât contractele de test să ghideze designul componentelor și calitatea codului. fileciteturn3file0### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; rădăcină + `packages/*` |
| Instalare | `npm i` | `pnpm i -w` |
| Testare | `npm test` (Vitest & Jest) | `pnpm -w run test` sau `--filter` |
| CI | Workflows simple per proiect | Workflows agregate, matrice pe pachete |
| Scalare (45 proiecte) | multiplicare directoare | pachete dedicate în `packages/*` |
| Public țintă | începători | echipe/colecții avansate |
### Inventar pe arhivă (roluri)

- **Seminar10_Partea2_p2-monorepo.zip** — config=8, public=1, code=11, tests=9, docs=2.
- **Seminar10_Partea2_p2-standalone.zip** — config=6, public=1, code=11, tests=9, docs=2.
- **Seminar10_Partea3_p3-monorepo.zip** — config=272, public=45, docs=45, code=135, tests=135.
- **Seminar10_Partea3_p3-standalone.zip** — config=540, public=90, docs=90, code=270, tests=270.
- **Seminar10_Partea3_p3-READMEs.zip** — docs=90.
### Explicații fișier-cu-fișier

Consultați tabelul din §4; detaliile de configurare și testare sunt aliniate cu **Laboratorul**. fileciteturn3file1
### Corelații între fișiere


- `src/App.tsx` ↔ `tests/*`: componente, input controlat, liste & keys, evenimente — aceleași aserții în Vitest & Jest. fileciteturn3file1  
- `.github/workflows/*` ↔ `lint`/`test`: pipeline determinist pentru PR-uri. fileciteturn3file2  
- Proiectele L1–L3 (starter/solution) ↔ README‑urile dedicate: progresie, rubrică, contracte de test. fileciteturn3file3  
### Recomandări pentru studenți


1) **Începeți în standalone** (curba mai lină), apoi treceți la monorepo pentru colecții mari.  
2) **Testați în paralel** cu Vitest și Jest; păstrați testele izomorfe (aceleași aserții). fileciteturn3file1  
3) **Listați contractele** (titluri, a11y, inputuri controlate) în README‑ul fiecărui proiect. fileciteturn3file3  
4) **Respectați accesibilitatea** (roluri/etichete) și **keys** stabile.  
5) **Versionare disciplinată**: commit‑uri mici, mesaje clare; rulați `lint` + `test` înainte de push.  
### Instrucțiuni „Quick start” per arhivă


**Partea 2 — standalone:**
```bash
unzip "Seminar10_Partea2_p2-standalone.zip" -d s10p2-standalone
cd s10p2-standalone
npm i
npm test
npm run dev
```

**Partea 2 — monorepo:**
```bash
unzip "Seminar10_Partea2_p2-monorepo.zip" -d s10p2-monorepo
cd s10p2-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter lab run dev
```

**Partea 3 — standalone (proiecte):**
```bash
unzip "Seminar10_Partea3_p3-standalone.zip" -d s10p3-standalone
cd s10p3-standalone/L1/L1-P01/starter
npm i
npm test
npm run dev
```

**Partea 3 — monorepo (proiecte):**
```bash
unzip "Seminar10_Partea3_p3-monorepo.zip" -d s10p3-monorepo
cd s10p3-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter l1-p01-starter run dev
```
### Troubleshooting (erori frecvente)


- **Jest nu transpilează TSX** → `babel-jest` + preseturi; `testEnvironment:'jsdom'`. fileciteturn3file1  
- **Vitest fără JSDOM** → `environment:'jsdom'` + `setupFiles`; verifică `vitest.config.ts`. fileciteturn3file1  
- **Keys instabile** → re‑montări surpriză; folosește ID‑uri reale. fileciteturn3file0  
- **PNPM filter** → dacă un pachet nu este găsit, verifică `pnpm-workspace.yaml` și `name` în `package.json`. fileciteturn3file2  
- **Port Vite** → schimbă cu `--port` sau `VITE_PORT`; evită conflicte în e2e. fileciteturn3file2  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** — componente funcționale, JSX, events, lists & keys, controlled forms, composition, transitions — fundamente pentru designul proiectelor. fileciteturn3file0  
- **Partea 2 (Laborator)** — „ClubHub” progresiv, cu testare dublă și configurări Jest/Vitest; Quick start & VSL prompts. fileciteturn3file1  
- **Partea 3 (Ghid Arhive)** — structură pe arhive, comenzi, CI la scară; diferențe de rulare standalone vs. monorepo. fileciteturn3file2  
- **Partea 3 (Proiecte extins)** — 45 proiecte L1–L3, fiecare cu **starter/solution** și suite de teste echivalente. fileciteturn3file3  
### Prompt-șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S10** (standalone & monorepo) o aplicație React/TS cu componente & JSX, input controlat, liste & keys, composition, un prim `startTransition`, testare duală **Vitest/Jest**, CI, README cu Quick start & Troubleshooting, și variante **starter**/**solution**.”
