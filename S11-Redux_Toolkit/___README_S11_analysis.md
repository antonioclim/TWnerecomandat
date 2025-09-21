# Seminarul S11 — Redux Toolkit (standalone & monorepo) — Analiză integrată a arhivelor și ghidurilor

*Generat la 2025-09-21 04:39.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar11_Partea2_ReduxToolkit(RTK)_p2-monorepo.zip

```
package.json
packages/lab/babel.config.cjs
packages/lab/docs/README.md
packages/lab/docs/WORKSHEET.md
packages/lab/index.html
packages/lab/jest.config.cjs
packages/lab/package.json
packages/lab/src/App.tsx
packages/lab/src/app/hooks.ts
packages/lab/src/app/store.ts
packages/lab/src/components/AddClubForm.tsx
packages/lab/src/components/CategoryFilter.tsx
packages/lab/src/components/ClubCard.tsx
packages/lab/src/components/ClubList.tsx
packages/lab/src/components/Footer.tsx
packages/lab/src/components/Header.tsx
packages/lab/src/components/SearchBox.tsx
packages/lab/src/features/clubs/clubsSlice.ts
packages/lab/src/main.tsx
packages/lab/src/services/clubsApi.ts
packages/lab/src/styles.css
packages/lab/tests/jest/App.jest.test.tsx
packages/lab/tests/jest/reducer.jest.test.ts
packages/lab/tests/jest/selectors.jest.test.ts
packages/lab/tests/jest/thunk.jest.test.ts
packages/lab/tests/msw/handlers.ts
packages/lab/tests/msw/server.ts
packages/lab/tests/setup.ts
packages/lab/tests/vitest/App.test.tsx
packages/lab/tests/vitest/reducer.test.ts
packages/lab/tests/vitest/selectors.test.ts
packages/lab/tests/vitest/thunk.test.ts
packages/lab/tsconfig.json
packages/lab/vite.config.ts
packages/lab/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 8, public: 1, code: 14, tests: 11, docs: 2.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s11p2-monorepo` type=`module` workspaces=True
- `packages/lab/package.json`: name=`s11p2-rtk-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest

### Seminar11_Partea2_ReduxToolkit(RTK)_p2-standalone.zip

```
babel.config.cjs
docs/README.md
docs/WORKSHEET.md
index.html
jest.config.cjs
package.json
src/App.tsx
src/app/hooks.ts
src/app/store.ts
src/components/AddClubForm.tsx
src/components/CategoryFilter.tsx
src/components/ClubCard.tsx
src/components/ClubList.tsx
src/components/Footer.tsx
src/components/Header.tsx
src/components/SearchBox.tsx
src/features/clubs/clubsSlice.ts
src/main.tsx
src/services/clubsApi.ts
src/styles.css
tests/jest/App.jest.test.tsx
tests/jest/reducer.jest.test.ts
tests/jest/selectors.jest.test.ts
tests/jest/thunk.jest.test.ts
tests/msw/handlers.ts
tests/msw/server.ts
tests/setup.ts
tests/vitest/App.test.tsx
tests/vitest/reducer.test.ts
tests/vitest/selectors.test.ts
tests/vitest/thunk.test.ts
tsconfig.json
vite.config.ts
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 6, public: 1, code: 14, tests: 11, docs: 2.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s11p2-rtk-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest

### Seminar11_Partea3_RTK_p3-monorepo.zip

```
package.json
packages/l1-p01-starter/README.md
packages/l1-p01-starter/babel.config.cjs
packages/l1-p01-starter/index.html
packages/l1-p01-starter/jest.config.cjs
packages/l1-p01-starter/package.json
packages/l1-p01-starter/src/App.tsx
packages/l1-p01-starter/src/app/hooks.ts
packages/l1-p01-starter/src/app/store.ts
packages/l1-p01-starter/src/features/clubs/clubsSlice.ts
packages/l1-p01-starter/src/main.tsx
packages/l1-p01-starter/src/styles.css
packages/l1-p01-starter/tests/jest/logic.jest.test.ts
packages/l1-p01-starter/tests/setup.ts
packages/l1-p01-starter/tests/vitest/logic.test.ts
packages/l1-p01-starter/tsconfig.json
packages/l1-p01-starter/vite.config.ts
packages/l1-p01-starter/vitest.config.ts
packages/l1-p02-starter/README.md
packages/l1-p02-starter/babel.config.cjs
packages/l1-p02-starter/index.html
packages/l1-p02-starter/jest.config.cjs
packages/l1-p02-starter/package.json
packages/l1-p02-starter/src/App.tsx
packages/l1-p02-starter/src/app/hooks.ts
packages/l1-p02-starter/src/app/store.ts
packages/l1-p02-starter/src/features/clubs/clubsSlice.ts
packages/l1-p02-starter/src/main.tsx
packages/l1-p02-starter/src/styles.css
packages/l1-p02-starter/tests/jest/logic.jest.test.ts
packages/l1-p02-starter/tests/setup.ts
packages/l1-p02-starter/tests/vitest/logic.test.ts
packages/l1-p02-starter/tsconfig.json
packages/l1-p02-starter/vite.config.ts
packages/l1-p02-starter/vitest.config.ts
packages/l1-p03-starter/README.md
packages/l1-p03-starter/babel.config.cjs
packages/l1-p03-starter/index.html
packages/l1-p03-starter/jest.config.cjs
packages/l1-p03-starter/package.json
packages/l1-p03-starter/src/App.tsx
packages/l1-p03-starter/src/app/hooks.ts
packages/l1-p03-starter/src/app/store.ts
packages/l1-p03-starter/src/features/clubs/clubsSlice.ts
packages/l1-p03-starter/src/main.tsx
packages/l1-p03-starter/src/styles.css
packages/l1-p03-starter/tests/jest/logic.jest.test.ts
packages/l1-p03-starter/tests/setup.ts
packages/l1-p03-starter/tests/vitest/logic.test.ts
packages/l1-p03-starter/tsconfig.json
packages/l1-p03-starter/vite.config.ts
packages/l1-p03-starter/vitest.config.ts
packages/l1-p04-starter/README.md
packages/l1-p04-starter/babel.config.cjs
packages/l1-p04-starter/index.html
packages/l1-p04-starter/jest.config.cjs
packages/l1-p04-starter/package.json
packages/l1-p04-starter/src/App.tsx
packages/l1-p04-starter/src/app/hooks.ts
packages/l1-p04-starter/src/app/store.ts
packages/l1-p04-starter/src/features/clubs/clubsSlice.ts
packages/l1-p04-starter/src/main.tsx
packages/l1-p04-starter/src/styles.css
packages/l1-p04-starter/tests/jest/logic.jest.test.ts
packages/l1-p04-starter/tests/setup.ts
packages/l1-p04-starter/tests/vitest/logic.test.ts
packages/l1-p04-starter/tsconfig.json
packages/l1-p04-starter/vite.config.ts
packages/l1-p04-starter/vitest.config.ts
packages/l1-p05-starter/README.md
packages/l1-p05-starter/babel.config.cjs
packages/l1-p05-starter/index.html
packages/l1-p05-starter/jest.config.cjs
packages/l1-p05-starter/package.json
packages/l1-p05-starter/src/App.tsx
packages/l1-p05-starter/src/app/hooks.ts
packages/l1-p05-starter/src/app/store.ts
packages/l1-p05-starter/src/features/clubs/clubsSlice.ts
packages/l1-p05-starter/src/main.tsx
packages/l1-p05-starter/src/styles.css
packages/l1-p05-starter/tests/jest/logic.jest.test.ts
packages/l1-p05-starter/tests/setup.ts
packages/l1-p05-starter/tests/vitest/logic.test.ts
packages/l1-p05-starter/tsconfig.json
packages/l1-p05-starter/vite.config.ts
packages/l1-p05-starter/vitest.config.ts
packages/l1-p06-starter/README.md
packages/l1-p06-starter/babel.config.cjs
packages/l1-p06-starter/index.html
packages/l1-p06-starter/jest.config.cjs
packages/l1-p06-starter/package.json
packages/l1-p06-starter/src/App.tsx
packages/l1-p06-starter/src/app/hooks.ts
packages/l1-p06-starter/src/app/store.ts
packages/l1-p06-starter/src/features/clubs/clubsSlice.ts
packages/l1-p06-starter/src/main.tsx
packages/l1-p06-starter/src/styles.css
packages/l1-p06-starter/tests/jest/logic.jest.test.ts
packages/l1-p06-starter/tests/setup.ts
packages/l1-p06-starter/tests/vitest/logic.test.ts
packages/l1-p06-starter/tsconfig.json
packages/l1-p06-starter/vite.config.ts
packages/l1-p06-starter/vitest.config.ts
packages/l1-p07-starter/README.md
packages/l1-p07-starter/babel.config.cjs
packages/l1-p07-starter/index.html
packages/l1-p07-starter/jest.config.cjs
packages/l1-p07-starter/package.json
packages/l1-p07-starter/src/App.tsx
packages/l1-p07-starter/src/app/hooks.ts
packages/l1-p07-starter/src/app/store.ts
packages/l1-p07-starter/src/features/clubs/clubsSlice.ts
packages/l1-p07-starter/src/main.tsx
packages/l1-p07-starter/src/styles.css
packages/l1-p07-starter/tests/jest/logic.jest.test.ts
packages/l1-p07-starter/tests/setup.ts
packages/l1-p07-starter/tests/vitest/logic.test.ts
packages/l1-p07-starter/tsconfig.json
packages/l1-p07-starter/vite.config.ts
packages/l1-p07-starter/vitest.config.ts
packages/l1-p08-starter/README.md
packages/l1-p08-starter/babel.config.cjs
packages/l1-p08-starter/index.html
packages/l1-p08-starter/jest.config.cjs
packages/l1-p08-starter/package.json
packages/l1-p08-starter/src/App.tsx
packages/l1-p08-starter/src/app/hooks.ts
packages/l1-p08-starter/src/app/store.ts
packages/l1-p08-starter/src/features/clubs/clubsSlice.ts
packages/l1-p08-starter/src/main.tsx
packages/l1-p08-starter/src/styles.css
packages/l1-p08-starter/tests/jest/logic.jest.test.ts
packages/l1-p08-starter/tests/setup.ts
packages/l1-p08-starter/tests/vitest/logic.test.ts
packages/l1-p08-starter/tsconfig.json
packages/l1-p08-starter/vite.config.ts
packages/l1-p08-starter/vitest.config.ts
packages/l1-p09-starter/README.md
packages/l1-p09-starter/babel.config.cjs
packages/l1-p09-starter/index.html
packages/l1-p09-starter/jest.config.cjs
packages/l1-p09-starter/package.json
packages/l1-p09-starter/src/App.tsx
packages/l1-p09-starter/src/app/hooks.ts
packages/l1-p09-starter/src/app/store.ts
packages/l1-p09-starter/src/features/clubs/clubsSlice.ts
packages/l1-p09-starter/src/main.tsx
packages/l1-p09-starter/src/styles.css
packages/l1-p09-starter/tests/jest/logic.jest.test.ts
packages/l1-p09-starter/tests/setup.ts
packages/l1-p09-starter/tests/vitest/logic.test.ts
packages/l1-p09-starter/tsconfig.json
packages/l1-p09-starter/vite.config.ts
packages/l1-p09-starter/vitest.config.ts
packages/l1-p10-starter/README.md
packages/l1-p10-starter/babel.config.cjs
packages/l1-p10-starter/index.html
packages/l1-p10-starter/jest.config.cjs
packages/l1-p10-starter/package.json
packages/l1-p10-starter/src/App.tsx
packages/l1-p10-starter/src/app/hooks.ts
packages/l1-p10-starter/src/app/store.ts
packages/l1-p10-starter/src/features/clubs/clubsSlice.ts
packages/l1-p10-starter/src/main.tsx
packages/l1-p10-starter/src/styles.css
packages/l1-p10-starter/tests/jest/logic.jest.test.ts
packages/l1-p10-starter/tests/setup.ts
packages/l1-p10-starter/tests/vitest/logic.test.ts
packages/l1-p10-starter/tsconfig.json
packages/l1-p10-starter/vite.config.ts
packages/l1-p10-starter/vitest.config.ts
packages/l1-p11-starter/README.md
packages/l1-p11-starter/babel.config.cjs
packages/l1-p11-starter/index.html
packages/l1-p11-starter/jest.config.cjs
packages/l1-p11-starter/package.json
packages/l1-p11-starter/src/App.tsx
packages/l1-p11-starter/src/app/hooks.ts
packages/l1-p11-starter/src/app/store.ts
packages/l1-p11-starter/src/features/clubs/clubsSlice.ts
packages/l1-p11-starter/src/main.tsx
packages/l1-p11-starter/src/styles.css
packages/l1-p11-starter/tests/jest/logic.jest.test.ts
packages/l1-p11-starter/tests/setup.ts
packages/l1-p11-starter/tests/vitest/logic.test.ts
packages/l1-p11-starter/tsconfig.json
packages/l1-p11-starter/vite.config.ts
packages/l1-p11-starter/vitest.config.ts
packages/l1-p12-starter/README.md
packages/l1-p12-starter/babel.config.cjs
packages/l1-p12-starter/index.html
packages/l1-p12-starter/jest.config.cjs
packages/l1-p12-starter/package.json
packages/l1-p12-starter/src/App.tsx
packages/l1-p12-starter/src/app/hooks.ts
packages/l1-p12-starter/src/app/store.ts
packages/l1-p12-starter/src/features/clubs/clubsSlice.ts
packages/l1-p12-starter/src/main.tsx
packages/l1-p12-starter/src/styles.css
packages/l1-p12-starter/tests/jest/logic.jest.test.ts
packages/l1-p12-starter/tests/setup.ts
packages/l1-p12-starter/tests/vitest/logic.test.ts
packages/l1-p12-starter/tsconfig.json
packages/l1-p12-starter/vite.config.ts
packages/l1-p12-starter/vitest.config.ts
packages/l1-p13-starter/README.md
packages/l1-p13-starter/babel.config.cjs
packages/l1-p13-starter/index.html
packages/l1-p13-starter/jest.config.cjs
packages/l1-p13-starter/package.json
packages/l1-p13-starter/src/App.tsx
packages/l1-p13-starter/src/app/hooks.ts
packages/l1-p13-starter/src/app/store.ts
packages/l1-p13-starter/src/features/clubs/clubsSlice.ts
packages/l1-p13-starter/src/main.tsx
packages/l1-p13-starter/src/styles.css
packages/l1-p13-starter/tests/jest/logic.jest.test.ts
packages/l1-p13-starter/tests/setup.ts
packages/l1-p13-starter/tests/vitest/logic.test.ts
packages/l1-p13-starter/tsconfig.json
packages/l1-p13-starter/vite.config.ts
packages/l1-p13-starter/vitest.config.ts
packages/l1-p14-starter/README.md
packages/l1-p14-starter/babel.config.cjs
packages/l1-p14-starter/index.html
packages/l1-p14-starter/jest.config.cjs
packages/l1-p14-starter/package.json
packages/l1-p14-starter/src/App.tsx
packages/l1-p14-starter/src/app/hooks.ts
packages/l1-p14-starter/src/app/store.ts
packages/l1-p14-starter/src/features/clubs/clubsSlice.ts
packages/l1-p14-starter/src/main.tsx
packages/l1-p14-starter/src/styles.css
packages/l1-p14-starter/tests/jest/logic.jest.test.ts
packages/l1-p14-starter/tests/setup.ts
packages/l1-p14-starter/tests/vitest/logic.test.ts
packages/l1-p14-starter/tsconfig.json
packages/l1-p14-starter/vite.config.ts
packages/l1-p14-starter/vitest.config.ts
packages/l1-p15-starter/README.md
packages/l1-p15-starter/babel.config.cjs
packages/l1-p15-starter/index.html
packages/l1-p15-starter/jest.config.cjs
packages/l1-p15-starter/package.json
packages/l1-p15-starter/src/App.tsx
packages/l1-p15-starter/src/app/hooks.ts
packages/l1-p15-starter/src/app/store.ts
packages/l1-p15-starter/src/features/clubs/clubsSlice.ts
packages/l1-p15-starter/src/main.tsx
packages/l1-p15-starter/src/styles.css
packages/l1-p15-starter/tests/jest/logic.jest.test.ts
packages/l1-p15-starter/tests/setup.ts
packages/l1-p15-starter/tests/vitest/logic.test.ts
packages/l1-p15-starter/tsconfig.json
packages/l1-p15-starter/vite.config.ts
packages/l1-p15-starter/vitest.config.ts
packages/l2-p01-starter/README.md
packages/l2-p01-starter/babel.config.cjs
packages/l2-p01-starter/index.html
packages/l2-p01-starter/jest.config.cjs
packages/l2-p01-starter/package.json
packages/l2-p01-starter/src/App.tsx
packages/l2-p01-starter/src/app/hooks.ts
packages/l2-p01-starter/src/app/store.ts
packages/l2-p01-starter/src/features/clubs/clubsSlice.ts
packages/l2-p01-starter/src/main.tsx
packages/l2-p01-starter/src/styles.css
packages/l2-p01-starter/tests/jest/async.jest.test.ts
packages/l2-p01-starter/tests/setup.ts
packages/l2-p01-starter/tests/vitest/async.test.ts
packages/l2-p01-starter/tsconfig.json
packages/l2-p01-starter/vite.config.ts
packages/l2-p01-starter/vitest.config.ts
packages/l2-p02-starter/README.md
packages/l2-p02-starter/babel.config.cjs
packages/l2-p02-starter/index.html
packages/l2-p02-starter/jest.config.cjs
packages/l2-p02-starter/package.json
packages/l2-p02-starter/src/App.tsx
packages/l2-p02-starter/src/app/hooks.ts
packages/l2-p02-starter/src/app/store.ts
packages/l2-p02-starter/src/features/clubs/clubsSlice.ts
packages/l2-p02-starter/src/main.tsx
packages/l2-p02-starter/src/styles.css
packages/l2-p02-starter/tests/jest/async.jest.test.ts
packages/l2-p02-starter/tests/setup.ts
packages/l2-p02-starter/tests/vitest/async.test.ts
packages/l2-p02-starter/tsconfig.json
packages/l2-p02-starter/vite.config.ts
packages/l2-p02-starter/vitest.config.ts
packages/l2-p03-starter/README.md
packages/l2-p03-starter/babel.config.cjs
packages/l2-p03-starter/index.html
packages/l2-p03-starter/jest.config.cjs
packages/l2-p03-starter/package.json
packages/l2-p03-starter/src/App.tsx
packages/l2-p03-starter/src/app/hooks.ts
packages/l2-p03-starter/src/app/store.ts
packages/l2-p03-starter/src/features/clubs/clubsSlice.ts
packages/l2-p03-starter/src/main.tsx
packages/l2-p03-starter/src/styles.css
packages/l2-p03-starter/tests/jest/async.jest.test.ts
packages/l2-p03-starter/tests/setup.ts
packages/l2-p03-starter/tests/vitest/async.test.ts
packages/l2-p03-starter/tsconfig.json
packages/l2-p03-starter/vite.config.ts
packages/l2-p03-starter/vitest.config.ts
packages/l2-p04-starter/README.md
packages/l2-p04-starter/babel.config.cjs
packages/l2-p04-starter/index.html
packages/l2-p04-starter/jest.config.cjs
packages/l2-p04-starter/package.json
packages/l2-p04-starter/src/App.tsx
packages/l2-p04-starter/src/app/hooks.ts
packages/l2-p04-starter/src/app/store.ts
packages/l2-p04-starter/src/features/clubs/clubsSlice.ts
packages/l2-p04-starter/src/main.tsx
packages/l2-p04-starter/src/styles.css
packages/l2-p04-starter/tests/jest/async.jest.test.ts
packages/l2-p04-starter/tests/setup.ts
packages/l2-p04-starter/tests/vitest/async.test.ts
packages/l2-p04-starter/tsconfig.json
packages/l2-p04-starter/vite.config.ts
packages/l2-p04-starter/vitest.config.ts
packages/l2-p05-starter/README.md
packages/l2-p05-starter/babel.config.cjs
packages/l2-p05-starter/index.html
packages/l2-p05-starter/jest.config.cjs
packages/l2-p05-starter/package.json
packages/l2-p05-starter/src/App.tsx
packages/l2-p05-starter/src/app/hooks.ts
packages/l2-p05-starter/src/app/store.ts
packages/l2-p05-starter/src/features/clubs/clubsSlice.ts
packages/l2-p05-starter/src/main.tsx
packages/l2-p05-starter/src/styles.css
packages/l2-p05-starter/tests/jest/async.jest.test.ts
packages/l2-p05-starter/tests/setup.ts
packages/l2-p05-starter/tests/vitest/async.test.ts
packages/l2-p05-starter/tsconfig.json
packages/l2-p05-starter/vite.config.ts
packages/l2-p05-starter/vitest.config.ts
packages/l2-p06-starter/README.md
packages/l2-p06-starter/babel.config.cjs
packages/l2-p06-starter/index.html
packages/l2-p06-starter/jest.config.cjs
packages/l2-p06-starter/package.json
packages/l2-p06-starter/src/App.tsx
packages/l2-p06-starter/src/app/hooks.ts
packages/l2-p06-starter/src/app/store.ts
packages/l2-p06-starter/src/features/clubs/clubsSlice.ts
packages/l2-p06-starter/src/main.tsx
packages/l2-p06-starter/src/styles.css
packages/l2-p06-starter/tests/jest/async.jest.test.ts
packages/l2-p06-starter/tests/setup.ts
packages/l2-p06-starter/tests/vitest/async.test.ts
packages/l2-p06-starter/tsconfig.json
packages/l2-p06-starter/vite.config.ts
packages/l2-p06-starter/vitest.config.ts
packages/l2-p07-starter/README.md
packages/l2-p07-starter/babel.config.cjs
packages/l2-p07-starter/index.html
packages/l2-p07-starter/jest.config.cjs
packages/l2-p07-starter/package.json
packages/l2-p07-starter/src/App.tsx
packages/l2-p07-starter/src/app/hooks.ts
packages/l2-p07-starter/src/app/store.ts
packages/l2-p07-starter/src/features/clubs/clubsSlice.ts
packages/l2-p07-starter/src/main.tsx
packages/l2-p07-starter/src/styles.css
packages/l2-p07-starter/tests/jest/async.jest.test.ts
packages/l2-p07-starter/tests/setup.ts
packages/l2-p07-starter/tests/vitest/async.test.ts
packages/l2-p07-starter/tsconfig.json
packages/l2-p07-starter/vite.config.ts
packages/l2-p07-starter/vitest.config.ts
packages/l2-p08-starter/README.md
packages/l2-p08-starter/babel.config.cjs
packages/l2-p08-starter/index.html
packages/l2-p08-starter/jest.config.cjs
packages/l2-p08-starter/package.json
packages/l2-p08-starter/src/App.tsx
packages/l2-p08-starter/src/app/hooks.ts
packages/l2-p08-starter/src/app/store.ts
packages/l2-p08-starter/src/features/clubs/clubsSlice.ts
packages/l2-p08-starter/src/main.tsx
packages/l2-p08-starter/src/styles.css
packages/l2-p08-starter/tests/jest/async.jest.test.ts
packages/l2-p08-starter/tests/setup.ts
packages/l2-p08-starter/tests/vitest/async.test.ts
packages/l2-p08-starter/tsconfig.json
packages/l2-p08-starter/vite.config.ts
packages/l2-p08-starter/vitest.config.ts
packages/l2-p09-starter/README.md
packages/l2-p09-starter/babel.config.cjs
packages/l2-p09-starter/index.html
packages/l2-p09-starter/jest.config.cjs
packages/l2-p09-starter/package.json
packages/l2-p09-starter/src/App.tsx
packages/l2-p09-starter/src/app/hooks.ts
packages/l2-p09-starter/src/app/store.ts
packages/l2-p09-starter/src/features/clubs/clubsSlice.ts
packages/l2-p09-starter/src/main.tsx
packages/l2-p09-starter/src/styles.css
packages/l2-p09-starter/tests/jest/async.jest.test.ts
packages/l2-p09-starter/tests/setup.ts
packages/l2-p09-starter/tests/vitest/async.test.ts
packages/l2-p09-starter/tsconfig.json
packages/l2-p09-starter/vite.config.ts
packages/l2-p09-starter/vitest.config.ts
packages/l2-p10-starter/README.md
packages/l2-p10-starter/babel.config.cjs
packages/l2-p10-starter/index.html
packages/l2-p10-starter/jest.config.cjs
packages/l2-p10-starter/package.json
packages/l2-p10-starter/src/App.tsx
packages/l2-p10-starter/src/app/hooks.ts
packages/l2-p10-starter/src/app/store.ts
packages/l2-p10-starter/src/features/clubs/clubsSlice.ts
packages/l2-p10-starter/src/main.tsx
packages/l2-p10-starter/src/styles.css
packages/l2-p10-starter/tests/jest/async.jest.test.ts
packages/l2-p10-starter/tests/setup.ts
packages/l2-p10-starter/tests/vitest/async.test.ts
packages/l2-p10-starter/tsconfig.json
packages/l2-p10-starter/vite.config.ts
packages/l2-p10-starter/vitest.config.ts
packages/l2-p11-starter/README.md
packages/l2-p11-starter/babel.config.cjs
packages/l2-p11-starter/index.html
packages/l2-p11-starter/jest.config.cjs
packages/l2-p11-starter/package.json
packages/l2-p11-starter/src/App.tsx
packages/l2-p11-starter/src/app/hooks.ts
packages/l2-p11-starter/src/app/store.ts
packages/l2-p11-starter/src/features/clubs/clubsSlice.ts
packages/l2-p11-starter/src/main.tsx
packages/l2-p11-starter/src/styles.css
packages/l2-p11-starter/tests/jest/async.jest.test.ts
packages/l2-p11-starter/tests/setup.ts
packages/l2-p11-starter/tests/vitest/async.test.ts
packages/l2-p11-starter/tsconfig.json
packages/l2-p11-starter/vite.config.ts
packages/l2-p11-starter/vitest.config.ts
packages/l2-p12-starter/README.md
packages/l2-p12-starter/babel.config.cjs
packages/l2-p12-starter/index.html
packages/l2-p12-starter/jest.config.cjs
packages/l2-p12-starter/package.json
packages/l2-p12-starter/src/App.tsx
packages/l2-p12-starter/src/app/hooks.ts
packages/l2-p12-starter/src/app/store.ts
packages/l2-p12-starter/src/features/clubs/clubsSlice.ts
packages/l2-p12-starter/src/main.tsx
packages/l2-p12-starter/src/styles.css
packages/l2-p12-starter/tests/jest/async.jest.test.ts
packages/l2-p12-starter/tests/setup.ts
packages/l2-p12-starter/tests/vitest/async.test.ts
packages/l2-p12-starter/tsconfig.json
packages/l2-p12-starter/vite.config.ts
packages/l2-p12-starter/vitest.config.ts
packages/l2-p13-starter/README.md
packages/l2-p13-starter/babel.config.cjs
packages/l2-p13-starter/index.html
packages/l2-p13-starter/jest.config.cjs
packages/l2-p13-starter/package.json
packages/l2-p13-starter/src/App.tsx
packages/l2-p13-starter/src/app/hooks.ts
packages/l2-p13-starter/src/app/store.ts
packages/l2-p13-starter/src/features/clubs/clubsSlice.ts
packages/l2-p13-starter/src/main.tsx
packages/l2-p13-starter/src/styles.css
packages/l2-p13-starter/tests/jest/async.jest.test.ts
packages/l2-p13-starter/tests/setup.ts
packages/l2-p13-starter/tests/vitest/async.test.ts
packages/l2-p13-starter/tsconfig.json
packages/l2-p13-starter/vite.config.ts
packages/l2-p13-starter/vitest.config.ts
packages/l2-p14-starter/README.md
packages/l2-p14-starter/babel.config.cjs
packages/l2-p14-starter/index.html
packages/l2-p14-starter/jest.config.cjs
packages/l2-p14-starter/package.json
packages/l2-p14-starter/src/App.tsx
packages/l2-p14-starter/src/app/hooks.ts
packages/l2-p14-starter/src/app/store.ts
packages/l2-p14-starter/src/features/clubs/clubsSlice.ts
packages/l2-p14-starter/src/main.tsx
packages/l2-p14-starter/src/styles.css
packages/l2-p14-starter/tests/jest/async.jest.test.ts
packages/l2-p14-starter/tests/setup.ts
packages/l2-p14-starter/tests/vitest/async.test.ts
packages/l2-p14-starter/tsconfig.json
packages/l2-p14-starter/vite.config.ts
packages/l2-p14-starter/vitest.config.ts
packages/l2-p15-starter/README.md
packages/l2-p15-starter/babel.config.cjs
packages/l2-p15-starter/index.html
packages/l2-p15-starter/jest.config.cjs
packages/l2-p15-starter/package.json
packages/l2-p15-starter/src/App.tsx
packages/l2-p15-starter/src/app/hooks.ts
packages/l2-p15-starter/src/app/store.ts
packages/l2-p15-starter/src/features/clubs/clubsSlice.ts
packages/l2-p15-starter/src/main.tsx
packages/l2-p15-starter/src/styles.css
packages/l2-p15-starter/tests/jest/async.jest.test.ts
packages/l2-p15-starter/tests/setup.ts
packages/l2-p15-starter/tests/vitest/async.test.ts
packages/l2-p15-starter/tsconfig.json
packages/l2-p15-starter/vite.config.ts
packages/l2-p15-starter/vitest.config.ts
packages/l3-p01-starter/README.md
packages/l3-p01-starter/babel.config.cjs
packages/l3-p01-starter/index.html
packages/l3-p01-starter/jest.config.cjs
packages/l3-p01-starter/package.json
packages/l3-p01-starter/src/App.tsx
packages/l3-p01-starter/src/app/hooks.ts
packages/l3-p01-starter/src/app/store.ts
packages/l3-p01-starter/src/features/clubs/clubsSlice.ts
packages/l3-p01-starter/src/main.tsx
packages/l3-p01-starter/src/services/clubsApi.ts
packages/l3-p01-starter/src/styles.css
packages/l3-p01-starter/tests/jest/query.jest.test.ts
packages/l3-p01-starter/tests/setup.ts
packages/l3-p01-starter/tests/vitest/query.test.ts
packages/l3-p01-starter/tsconfig.json
packages/l3-p01-starter/vite.config.ts
packages/l3-p01-starter/vitest.config.ts
packages/l3-p02-starter/README.md
packages/l3-p02-starter/babel.config.cjs
packages/l3-p02-starter/index.html
packages/l3-p02-starter/jest.config.cjs
packages/l3-p02-starter/package.json
packages/l3-p02-starter/src/App.tsx
packages/l3-p02-starter/src/app/hooks.ts
packages/l3-p02-starter/src/app/store.ts
packages/l3-p02-starter/src/features/clubs/clubsSlice.ts
packages/l3-p02-starter/src/main.tsx
packages/l3-p02-starter/src/services/clubsApi.ts
packages/l3-p02-starter/src/styles.css
packages/l3-p02-starter/tests/jest/query.jest.test.ts
packages/l3-p02-starter/tests/setup.ts
packages/l3-p02-starter/tests/vitest/query.test.ts
packages/l3-p02-starter/tsconfig.json
packages/l3-p02-starter/vite.config.ts
packages/l3-p02-starter/vitest.config.ts
packages/l3-p03-starter/README.md
packages/l3-p03-starter/babel.config.cjs
packages/l3-p03-starter/index.html
packages/l3-p03-starter/jest.config.cjs
packages/l3-p03-starter/package.json
packages/l3-p03-starter/src/App.tsx
packages/l3-p03-starter/src/app/hooks.ts
packages/l3-p03-starter/src/app/store.ts
packages/l3-p03-starter/src/features/clubs/clubsSlice.ts
packages/l3-p03-starter/src/main.tsx
packages/l3-p03-starter/src/services/clubsApi.ts
packages/l3-p03-starter/src/styles.css
packages/l3-p03-starter/tests/jest/query.jest.test.ts
packages/l3-p03-starter/tests/setup.ts
packages/l3-p03-starter/tests/vitest/query.test.ts
packages/l3-p03-starter/tsconfig.json
packages/l3-p03-starter/vite.config.ts
packages/l3-p03-starter/vitest.config.ts
packages/l3-p04-starter/README.md
packages/l3-p04-starter/babel.config.cjs
packages/l3-p04-starter/index.html
packages/l3-p04-starter/jest.config.cjs
packages/l3-p04-starter/package.json
packages/l3-p04-starter/src/App.tsx
packages/l3-p04-starter/src/app/hooks.ts
packages/l3-p04-starter/src/app/store.ts
packages/l3-p04-starter/src/features/clubs/clubsSlice.ts
packages/l3-p04-starter/src/main.tsx
packages/l3-p04-starter/src/services/clubsApi.ts
packages/l3-p04-starter/src/styles.css
packages/l3-p04-starter/tests/jest/query.jest.test.ts
packages/l3-p04-starter/tests/setup.ts
packages/l3-p04-starter/tests/vitest/query.test.ts
packages/l3-p04-starter/tsconfig.json
packages/l3-p04-starter/vite.config.ts
packages/l3-p04-starter/vitest.config.ts
packages/l3-p05-starter/README.md
packages/l3-p05-starter/babel.config.cjs
packages/l3-p05-starter/index.html
packages/l3-p05-starter/jest.config.cjs
packages/l3-p05-starter/package.json
packages/l3-p05-starter/src/App.tsx
packages/l3-p05-starter/src/app/hooks.ts
packages/l3-p05-starter/src/app/store.ts
packages/l3-p05-starter/src/features/clubs/clubsSlice.ts
packages/l3-p05-starter/src/main.tsx
packages/l3-p05-starter/src/services/clubsApi.ts
packages/l3-p05-starter/src/styles.css
packages/l3-p05-starter/tests/jest/query.jest.test.ts
packages/l3-p05-starter/tests/setup.ts
packages/l3-p05-starter/tests/vitest/query.test.ts
packages/l3-p05-starter/tsconfig.json
packages/l3-p05-starter/vite.config.ts
packages/l3-p05-starter/vitest.config.ts
packages/l3-p06-starter/README.md
packages/l3-p06-starter/babel.config.cjs
packages/l3-p06-starter/index.html
packages/l3-p06-starter/jest.config.cjs
packages/l3-p06-starter/package.json
packages/l3-p06-starter/src/App.tsx
packages/l3-p06-starter/src/app/hooks.ts
packages/l3-p06-starter/src/app/store.ts
packages/l3-p06-starter/src/features/clubs/clubsSlice.ts
packages/l3-p06-starter/src/main.tsx
packages/l3-p06-starter/src/services/clubsApi.ts
packages/l3-p06-starter/src/styles.css
packages/l3-p06-starter/tests/jest/query.jest.test.ts
packages/l3-p06-starter/tests/setup.ts
packages/l3-p06-starter/tests/vitest/query.test.ts
packages/l3-p06-starter/tsconfig.json
packages/l3-p06-starter/vite.config.ts
packages/l3-p06-starter/vitest.config.ts
packages/l3-p07-starter/README.md
packages/l3-p07-starter/babel.config.cjs
packages/l3-p07-starter/index.html
packages/l3-p07-starter/jest.config.cjs
packages/l3-p07-starter/package.json
packages/l3-p07-starter/src/App.tsx
packages/l3-p07-starter/src/app/hooks.ts
packages/l3-p07-starter/src/app/store.ts
packages/l3-p07-starter/src/features/clubs/clubsSlice.ts
packages/l3-p07-starter/src/main.tsx
packages/l3-p07-starter/src/services/clubsApi.ts
packages/l3-p07-starter/src/styles.css
packages/l3-p07-starter/tests/jest/query.jest.test.ts
packages/l3-p07-starter/tests/setup.ts
packages/l3-p07-starter/tests/vitest/query.test.ts
packages/l3-p07-starter/tsconfig.json
packages/l3-p07-starter/vite.config.ts
packages/l3-p07-starter/vitest.config.ts
packages/l3-p08-starter/README.md
packages/l3-p08-starter/babel.config.cjs
packages/l3-p08-starter/index.html
packages/l3-p08-starter/jest.config.cjs
packages/l3-p08-starter/package.json
packages/l3-p08-starter/src/App.tsx
packages/l3-p08-starter/src/app/hooks.ts
packages/l3-p08-starter/src/app/store.ts
packages/l3-p08-starter/src/features/clubs/clubsSlice.ts
packages/l3-p08-starter/src/main.tsx
packages/l3-p08-starter/src/services/clubsApi.ts
packages/l3-p08-starter/src/styles.css
packages/l3-p08-starter/tests/jest/query.jest.test.ts
packages/l3-p08-starter/tests/setup.ts
packages/l3-p08-starter/tests/vitest/query.test.ts
packages/l3-p08-starter/tsconfig.json
packages/l3-p08-starter/vite.config.ts
packages/l3-p08-starter/vitest.config.ts
packages/l3-p09-starter/README.md
packages/l3-p09-starter/babel.config.cjs
packages/l3-p09-starter/index.html
packages/l3-p09-starter/jest.config.cjs
packages/l3-p09-starter/package.json
packages/l3-p09-starter/src/App.tsx
packages/l3-p09-starter/src/app/hooks.ts
packages/l3-p09-starter/src/app/store.ts
packages/l3-p09-starter/src/features/clubs/clubsSlice.ts
packages/l3-p09-starter/src/main.tsx
packages/l3-p09-starter/src/services/clubsApi.ts
packages/l3-p09-starter/src/styles.css
packages/l3-p09-starter/tests/jest/query.jest.test.ts
packages/l3-p09-starter/tests/setup.ts
packages/l3-p09-starter/tests/vitest/query.test.ts
packages/l3-p09-starter/tsconfig.json
packages/l3-p09-starter/vite.config.ts
packages/l3-p09-starter/vitest.config.ts
packages/l3-p10-starter/README.md
packages/l3-p10-starter/babel.config.cjs
packages/l3-p10-starter/index.html
packages/l3-p10-starter/jest.config.cjs
packages/l3-p10-starter/package.json
packages/l3-p10-starter/src/App.tsx
packages/l3-p10-starter/src/app/hooks.ts
packages/l3-p10-starter/src/app/store.ts
packages/l3-p10-starter/src/features/clubs/clubsSlice.ts
packages/l3-p10-starter/src/main.tsx
packages/l3-p10-starter/src/services/clubsApi.ts
packages/l3-p10-starter/src/styles.css
packages/l3-p10-starter/tests/jest/query.jest.test.ts
packages/l3-p10-starter/tests/setup.ts
packages/l3-p10-starter/tests/vitest/query.test.ts
packages/l3-p10-starter/tsconfig.json
packages/l3-p10-starter/vite.config.ts
packages/l3-p10-starter/vitest.config.ts
packages/l3-p11-starter/README.md
packages/l3-p11-starter/babel.config.cjs
packages/l3-p11-starter/index.html
packages/l3-p11-starter/jest.config.cjs
packages/l3-p11-starter/package.json
packages/l3-p11-starter/src/App.tsx
packages/l3-p11-starter/src/app/hooks.ts
packages/l3-p11-starter/src/app/store.ts
packages/l3-p11-starter/src/features/clubs/clubsSlice.ts
packages/l3-p11-starter/src/main.tsx
packages/l3-p11-starter/src/services/clubsApi.ts
packages/l3-p11-starter/src/styles.css
packages/l3-p11-starter/tests/jest/query.jest.test.ts
packages/l3-p11-starter/tests/setup.ts
packages/l3-p11-starter/tests/vitest/query.test.ts
packages/l3-p11-starter/tsconfig.json
packages/l3-p11-starter/vite.config.ts
packages/l3-p11-starter/vitest.config.ts
packages/l3-p12-starter/README.md
packages/l3-p12-starter/babel.config.cjs
packages/l3-p12-starter/index.html
packages/l3-p12-starter/jest.config.cjs
packages/l3-p12-starter/package.json
packages/l3-p12-starter/src/App.tsx
packages/l3-p12-starter/src/app/hooks.ts
packages/l3-p12-starter/src/app/store.ts
packages/l3-p12-starter/src/features/clubs/clubsSlice.ts
packages/l3-p12-starter/src/main.tsx
packages/l3-p12-starter/src/services/clubsApi.ts
packages/l3-p12-starter/src/styles.css
packages/l3-p12-starter/tests/jest/query.jest.test.ts
packages/l3-p12-starter/tests/setup.ts
packages/l3-p12-starter/tests/vitest/query.test.ts
packages/l3-p12-starter/tsconfig.json
packages/l3-p12-starter/vite.config.ts
packages/l3-p12-starter/vitest.config.ts
packages/l3-p13-starter/README.md
packages/l3-p13-starter/babel.config.cjs
packages/l3-p13-starter/index.html
packages/l3-p13-starter/jest.config.cjs
packages/l3-p13-starter/package.json
packages/l3-p13-starter/src/App.tsx
packages/l3-p13-starter/src/app/hooks.ts
packages/l3-p13-starter/src/app/store.ts
packages/l3-p13-starter/src/features/clubs/clubsSlice.ts
packages/l3-p13-starter/src/main.tsx
packages/l3-p13-starter/src/services/clubsApi.ts
packages/l3-p13-starter/src/styles.css
packages/l3-p13-starter/tests/jest/query.jest.test.ts
packages/l3-p13-starter/tests/setup.ts
packages/l3-p13-starter/tests/vitest/query.test.ts
packages/l3-p13-starter/tsconfig.json
packages/l3-p13-starter/vite.config.ts
packages/l3-p13-starter/vitest.config.ts
packages/l3-p14-starter/README.md
packages/l3-p14-starter/babel.config.cjs
packages/l3-p14-starter/index.html
packages/l3-p14-starter/jest.config.cjs
packages/l3-p14-starter/package.json
packages/l3-p14-starter/src/App.tsx
packages/l3-p14-starter/src/app/hooks.ts
packages/l3-p14-starter/src/app/store.ts
packages/l3-p14-starter/src/features/clubs/clubsSlice.ts
packages/l3-p14-starter/src/main.tsx
packages/l3-p14-starter/src/services/clubsApi.ts
packages/l3-p14-starter/src/styles.css
packages/l3-p14-starter/tests/jest/query.jest.test.ts
packages/l3-p14-starter/tests/setup.ts
packages/l3-p14-starter/tests/vitest/query.test.ts
packages/l3-p14-starter/tsconfig.json
packages/l3-p14-starter/vite.config.ts
packages/l3-p14-starter/vitest.config.ts
packages/l3-p15-starter/README.md
packages/l3-p15-starter/babel.config.cjs
packages/l3-p15-starter/index.html
packages/l3-p15-starter/jest.config.cjs
packages/l3-p15-starter/package.json
packages/l3-p15-starter/src/App.tsx
packages/l3-p15-starter/src/app/hooks.ts
packages/l3-p15-starter/src/app/store.ts
packages/l3-p15-starter/src/features/clubs/clubsSlice.ts
packages/l3-p15-starter/src/main.tsx
packages/l3-p15-starter/src/services/clubsApi.ts
packages/l3-p15-starter/src/styles.css
packages/l3-p15-starter/tests/jest/query.jest.test.ts
packages/l3-p15-starter/tests/setup.ts
packages/l3-p15-starter/tests/vitest/query.test.ts
packages/l3-p15-starter/tsconfig.json
packages/l3-p15-starter/vite.config.ts
packages/l3-p15-starter/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** starter: 780.

**Categorii de fișiere:** config: 272, public: 45, docs: 45, code: 285, tests: 135.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s11p3-monorepo` type=`module` workspaces=True
- `packages/l1-p01-starter/package.json`: name=`l1-p01-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p02-starter/package.json`: name=`l1-p02-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p03-starter/package.json`: name=`l1-p03-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p04-starter/package.json`: name=`l1-p04-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p05-starter/package.json`: name=`l1-p05-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p06-starter/package.json`: name=`l1-p06-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p07-starter/package.json`: name=`l1-p07-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p08-starter/package.json`: name=`l1-p08-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p09-starter/package.json`: name=`l1-p09-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p10-starter/package.json`: name=`l1-p10-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p11-starter/package.json`: name=`l1-p11-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p12-starter/package.json`: name=`l1-p12-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p13-starter/package.json`: name=`l1-p13-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p14-starter/package.json`: name=`l1-p14-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l1-p15-starter/package.json`: name=`l1-p15-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p01-starter/package.json`: name=`l2-p01-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p02-starter/package.json`: name=`l2-p02-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p03-starter/package.json`: name=`l2-p03-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p04-starter/package.json`: name=`l2-p04-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p05-starter/package.json`: name=`l2-p05-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p06-starter/package.json`: name=`l2-p06-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p07-starter/package.json`: name=`l2-p07-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p08-starter/package.json`: name=`l2-p08-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p09-starter/package.json`: name=`l2-p09-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p10-starter/package.json`: name=`l2-p10-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p11-starter/package.json`: name=`l2-p11-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p12-starter/package.json`: name=`l2-p12-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p13-starter/package.json`: name=`l2-p13-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p14-starter/package.json`: name=`l2-p14-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l2-p15-starter/package.json`: name=`l2-p15-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p01-starter/package.json`: name=`l3-p01-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p02-starter/package.json`: name=`l3-p02-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p03-starter/package.json`: name=`l3-p03-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p04-starter/package.json`: name=`l3-p04-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p05-starter/package.json`: name=`l3-p05-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p06-starter/package.json`: name=`l3-p06-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p07-starter/package.json`: name=`l3-p07-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p08-starter/package.json`: name=`l3-p08-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p09-starter/package.json`: name=`l3-p09-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p10-starter/package.json`: name=`l3-p10-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p11-starter/package.json`: name=`l3-p11-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p12-starter/package.json`: name=`l3-p12-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p13-starter/package.json`: name=`l3-p13-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p14-starter/package.json`: name=`l3-p14-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `packages/l3-p15-starter/package.json`: name=`l3-p15-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest

### Seminar11_Partea3_RTK_p3-standalone.zip

> Structura este mare; se afișează începutul și sfârșitul.

```
L1/L1-P01/solution/README.md
L1/L1-P01/solution/babel.config.cjs
L1/L1-P01/solution/index.html
L1/L1-P01/solution/jest.config.cjs
L1/L1-P01/solution/package.json
L1/L1-P01/solution/src/App.tsx
L1/L1-P01/solution/src/app/hooks.ts
L1/L1-P01/solution/src/app/store.ts
L1/L1-P01/solution/src/features/clubs/clubsSlice.ts
L1/L1-P01/solution/src/main.tsx
L1/L1-P01/solution/src/styles.css
L1/L1-P01/solution/tests/jest/logic.jest.test.ts
L1/L1-P01/solution/tests/setup.ts
L1/L1-P01/solution/tests/vitest/logic.test.ts
L1/L1-P01/solution/tsconfig.json
L1/L1-P01/solution/vite.config.ts
L1/L1-P01/solution/vitest.config.ts
L1/L1-P01/starter/README.md
L1/L1-P01/starter/babel.config.cjs
L1/L1-P01/starter/index.html
L1/L1-P01/starter/jest.config.cjs
L1/L1-P01/starter/package.json
L1/L1-P01/starter/src/App.tsx
L1/L1-P01/starter/src/app/hooks.ts
L1/L1-P01/starter/src/app/store.ts
L1/L1-P01/starter/src/features/clubs/clubsSlice.ts
L1/L1-P01/starter/src/main.tsx
L1/L1-P01/starter/src/styles.css
L1/L1-P01/starter/tests/jest/logic.jest.test.ts
L1/L1-P01/starter/tests/setup.ts
L1/L1-P01/starter/tests/vitest/logic.test.ts
L1/L1-P01/starter/tsconfig.json
L1/L1-P01/starter/vite.config.ts
L1/L1-P01/starter/vitest.config.ts
L1/L1-P02/solution/README.md
L1/L1-P02/solution/babel.config.cjs
L1/L1-P02/solution/index.html
L1/L1-P02/solution/jest.config.cjs
L1/L1-P02/solution/package.json
L1/L1-P02/solution/src/App.tsx
L1/L1-P02/solution/src/app/hooks.ts
L1/L1-P02/solution/src/app/store.ts
L1/L1-P02/solution/src/features/clubs/clubsSlice.ts
L1/L1-P02/solution/src/main.tsx
L1/L1-P02/solution/src/styles.css
L1/L1-P02/solution/tests/jest/logic.jest.test.ts
L1/L1-P02/solution/tests/setup.ts
L1/L1-P02/solution/tests/vitest/logic.test.ts
L1/L1-P02/solution/tsconfig.json
L1/L1-P02/solution/vite.config.ts
L1/L1-P02/solution/vitest.config.ts
L1/L1-P02/starter/README.md
L1/L1-P02/starter/babel.config.cjs
L1/L1-P02/starter/index.html
L1/L1-P02/starter/jest.config.cjs
L1/L1-P02/starter/package.json
L1/L1-P02/starter/src/App.tsx
L1/L1-P02/starter/src/app/hooks.ts
L1/L1-P02/starter/src/app/store.ts
L1/L1-P02/starter/src/features/clubs/clubsSlice.ts
L1/L1-P02/starter/src/main.tsx
L1/L1-P02/starter/src/styles.css
L1/L1-P02/starter/tests/jest/logic.jest.test.ts
L1/L1-P02/starter/tests/setup.ts
L1/L1-P02/starter/tests/vitest/logic.test.ts
L1/L1-P02/starter/tsconfig.json
L1/L1-P02/starter/vite.config.ts
L1/L1-P02/starter/vitest.config.ts
L1/L1-P03/solution/README.md
L1/L1-P03/solution/babel.config.cjs
L1/L1-P03/solution/index.html
L1/L1-P03/solution/jest.config.cjs
L1/L1-P03/solution/package.json
L1/L1-P03/solution/src/App.tsx
L1/L1-P03/solution/src/app/hooks.ts
L1/L1-P03/solution/src/app/store.ts
L1/L1-P03/solution/src/features/clubs/clubsSlice.ts
L1/L1-P03/solution/src/main.tsx
L1/L1-P03/solution/src/styles.css
L1/L1-P03/solution/tests/jest/logic.jest.test.ts
L1/L1-P03/solution/tests/setup.ts
L1/L1-P03/solution/tests/vitest/logic.test.ts
L1/L1-P03/solution/tsconfig.json
L1/L1-P03/solution/vite.config.ts
L1/L1-P03/solution/vitest.config.ts
L1/L1-P03/starter/README.md
L1/L1-P03/starter/babel.config.cjs
L1/L1-P03/starter/index.html
L1/L1-P03/starter/jest.config.cjs
L1/L1-P03/starter/package.json
L1/L1-P03/starter/src/App.tsx
L1/L1-P03/starter/src/app/hooks.ts
L1/L1-P03/starter/src/app/store.ts
L1/L1-P03/starter/src/features/clubs/clubsSlice.ts
L1/L1-P03/starter/src/main.tsx
L1/L1-P03/starter/src/styles.css
L1/L1-P03/starter/tests/jest/logic.jest.test.ts
L1/L1-P03/starter/tests/setup.ts
L1/L1-P03/starter/tests/vitest/logic.test.ts
L1/L1-P03/starter/tsconfig.json
L1/L1-P03/starter/vite.config.ts
L1/L1-P03/starter/vitest.config.ts
L1/L1-P04/solution/README.md
L1/L1-P04/solution/babel.config.cjs
L1/L1-P04/solution/index.html
L1/L1-P04/solution/jest.config.cjs
L1/L1-P04/solution/package.json
L1/L1-P04/solution/src/App.tsx
L1/L1-P04/solution/src/app/hooks.ts
L1/L1-P04/solution/src/app/store.ts
L1/L1-P04/solution/src/features/clubs/clubsSlice.ts
L1/L1-P04/solution/src/main.tsx
L1/L1-P04/solution/src/styles.css
L1/L1-P04/solution/tests/jest/logic.jest.test.ts
L1/L1-P04/solution/tests/setup.ts
L1/L1-P04/solution/tests/vitest/logic.test.ts
L1/L1-P04/solution/tsconfig.json
L1/L1-P04/solution/vite.config.ts
L1/L1-P04/solution/vitest.config.ts
L1/L1-P04/starter/README.md
L1/L1-P04/starter/babel.config.cjs
L1/L1-P04/starter/index.html
L1/L1-P04/starter/jest.config.cjs
L1/L1-P04/starter/package.json
L1/L1-P04/starter/src/App.tsx
L1/L1-P04/starter/src/app/hooks.ts
L1/L1-P04/starter/src/app/store.ts
L1/L1-P04/starter/src/features/clubs/clubsSlice.ts
L1/L1-P04/starter/src/main.tsx
L1/L1-P04/starter/src/styles.css
L1/L1-P04/starter/tests/jest/logic.jest.test.ts
L1/L1-P04/starter/tests/setup.ts
L1/L1-P04/starter/tests/vitest/logic.test.ts
L1/L1-P04/starter/tsconfig.json
L1/L1-P04/starter/vite.config.ts
L1/L1-P04/starter/vitest.config.ts
L1/L1-P05/solution/README.md
L1/L1-P05/solution/babel.config.cjs
L1/L1-P05/solution/index.html
L1/L1-P05/solution/jest.config.cjs
L1/L1-P05/solution/package.json
L1/L1-P05/solution/src/App.tsx
L1/L1-P05/solution/src/app/hooks.ts
L1/L1-P05/solution/src/app/store.ts
L1/L1-P05/solution/src/features/clubs/clubsSlice.ts
L1/L1-P05/solution/src/main.tsx
L1/L1-P05/solution/src/styles.css
L1/L1-P05/solution/tests/jest/logic.jest.test.ts
L1/L1-P05/solution/tests/setup.ts
L1/L1-P05/solution/tests/vitest/logic.test.ts
L1/L1-P05/solution/tsconfig.json
L1/L1-P05/solution/vite.config.ts
L1/L1-P05/solution/vitest.config.ts
L1/L1-P05/starter/README.md
L1/L1-P05/starter/babel.config.cjs
L1/L1-P05/starter/index.html
L1/L1-P05/starter/jest.config.cjs
L1/L1-P05/starter/package.json
L1/L1-P05/starter/src/App.tsx
L1/L1-P05/starter/src/app/hooks.ts
L1/L1-P05/starter/src/app/store.ts
L1/L1-P05/starter/src/features/clubs/clubsSlice.ts
L1/L1-P05/starter/src/main.tsx
L1/L1-P05/starter/src/styles.css
L1/L1-P05/starter/tests/jest/logic.jest.test.ts
L1/L1-P05/starter/tests/setup.ts
L1/L1-P05/starter/tests/vitest/logic.test.ts
L1/L1-P05/starter/tsconfig.json
L1/L1-P05/starter/vite.config.ts
L1/L1-P05/starter/vitest.config.ts
L1/L1-P06/solution/README.md
L1/L1-P06/solution/babel.config.cjs
L1/L1-P06/solution/index.html
L1/L1-P06/solution/jest.config.cjs
L1/L1-P06/solution/package.json
L1/L1-P06/solution/src/App.tsx
L1/L1-P06/solution/src/app/hooks.ts
L1/L1-P06/solution/src/app/store.ts
L1/L1-P06/solution/src/features/clubs/clubsSlice.ts
L1/L1-P06/solution/src/main.tsx
L1/L1-P06/solution/src/styles.css
L1/L1-P06/solution/tests/jest/logic.jest.test.ts
L1/L1-P06/solution/tests/setup.ts
L1/L1-P06/solution/tests/vitest/logic.test.ts
L1/L1-P06/solution/tsconfig.json
L1/L1-P06/solution/vite.config.ts
L1/L1-P06/solution/vitest.config.ts
L1/L1-P06/starter/README.md
L1/L1-P06/starter/babel.config.cjs
L1/L1-P06/starter/index.html
L1/L1-P06/starter/jest.config.cjs
L1/L1-P06/starter/package.json
L1/L1-P06/starter/src/App.tsx
L1/L1-P06/starter/src/app/hooks.ts
L1/L1-P06/starter/src/app/store.ts
L1/L1-P06/starter/src/features/clubs/clubsSlice.ts
L1/L1-P06/starter/src/main.tsx
L1/L1-P06/starter/src/styles.css
L1/L1-P06/starter/tests/jest/logic.jest.test.ts
L1/L1-P06/starter/tests/setup.ts
L1/L1-P06/starter/tests/vitest/logic.test.ts
L1/L1-P06/starter/tsconfig.json
L1/L1-P06/starter/vite.config.ts
L1/L1-P06/starter/vitest.config.ts
L1/L1-P07/solution/README.md
L1/L1-P07/solution/babel.config.cjs
L1/L1-P07/solution/index.html
L1/L1-P07/solution/jest.config.cjs
L1/L1-P07/solution/package.json
L1/L1-P07/solution/src/App.tsx
L1/L1-P07/solution/src/app/hooks.ts
L1/L1-P07/solution/src/app/store.ts
L1/L1-P07/solution/src/features/clubs/clubsSlice.ts
L1/L1-P07/solution/src/main.tsx
L1/L1-P07/solution/src/styles.css
L1/L1-P07/solution/tests/jest/logic.jest.test.ts
L1/L1-P07/solution/tests/setup.ts
L1/L1-P07/solution/tests/vitest/logic.test.ts
L1/L1-P07/solution/tsconfig.json
L1/L1-P07/solution/vite.config.ts
L1/L1-P07/solution/vitest.config.ts
L1/L1-P07/starter/README.md
L1/L1-P07/starter/babel.config.cjs
L1/L1-P07/starter/index.html
L1/L1-P07/starter/jest.config.cjs
L1/L1-P07/starter/package.json
L1/L1-P07/starter/src/App.tsx
L1/L1-P07/starter/src/app/hooks.ts
L1/L1-P07/starter/src/app/store.ts
L1/L1-P07/starter/src/features/clubs/clubsSlice.ts
L1/L1-P07/starter/src/main.tsx
L1/L1-P07/starter/src/styles.css
L1/L1-P07/starter/tests/jest/logic.jest.test.ts
L1/L1-P07/starter/tests/setup.ts
L1/L1-P07/starter/tests/vitest/logic.test.ts
L1/L1-P07/starter/tsconfig.json
L1/L1-P07/starter/vite.config.ts
L1/L1-P07/starter/vitest.config.ts
L1/L1-P08/solution/README.md
L1/L1-P08/solution/babel.config.cjs
L1/L1-P08/solution/index.html
L1/L1-P08/solution/jest.config.cjs
L1/L1-P08/solution/package.json
L1/L1-P08/solution/src/App.tsx
L1/L1-P08/solution/src/app/hooks.ts
L1/L1-P08/solution/src/app/store.ts
L1/L1-P08/solution/src/features/clubs/clubsSlice.ts
L1/L1-P08/solution/src/main.tsx
L1/L1-P08/solution/src/styles.css
L1/L1-P08/solution/tests/jest/logic.jest.test.ts
L1/L1-P08/solution/tests/setup.ts
L1/L1-P08/solution/tests/vitest/logic.test.ts
L1/L1-P08/solution/tsconfig.json
L1/L1-P08/solution/vite.config.ts
L1/L1-P08/solution/vitest.config.ts
L1/L1-P08/starter/README.md
L1/L1-P08/starter/babel.config.cjs
L1/L1-P08/starter/index.html
L1/L1-P08/starter/jest.config.cjs
L1/L1-P08/starter/package.json
L1/L1-P08/starter/src/App.tsx
L1/L1-P08/starter/src/app/hooks.ts
L1/L1-P08/starter/src/app/store.ts
L1/L1-P08/starter/src/features/clubs/clubsSlice.ts
L1/L1-P08/starter/src/main.tsx
L1/L1-P08/starter/src/styles.css
L1/L1-P08/starter/tests/jest/logic.jest.test.ts
L1/L1-P08/starter/tests/setup.ts
L1/L1-P08/starter/tests/vitest/logic.test.ts
L1/L1-P08/starter/tsconfig.json
L1/L1-P08/starter/vite.config.ts
L1/L1-P08/starter/vitest.config.ts
L1/L1-P09/solution/README.md
L1/L1-P09/solution/babel.config.cjs
L1/L1-P09/solution/index.html
L1/L1-P09/solution/jest.config.cjs
L1/L1-P09/solution/package.json
L1/L1-P09/solution/src/App.tsx
L1/L1-P09/solution/src/app/hooks.ts
L1/L1-P09/solution/src/app/store.ts
L1/L1-P09/solution/src/features/clubs/clubsSlice.ts
L1/L1-P09/solution/src/main.tsx
L1/L1-P09/solution/src/styles.css
L1/L1-P09/solution/tests/jest/logic.jest.test.ts
L1/L1-P09/solution/tests/setup.ts
L1/L1-P09/solution/tests/vitest/logic.test.ts
L1/L1-P09/solution/tsconfig.json
L1/L1-P09/solution/vite.config.ts
L1/L1-P09/solution/vitest.config.ts
L1/L1-P09/starter/README.md
L1/L1-P09/starter/babel.config.cjs
L1/L1-P09/starter/index.html
L1/L1-P09/starter/jest.config.cjs
L1/L1-P09/starter/package.json
L1/L1-P09/starter/src/App.tsx
L1/L1-P09/starter/src/app/hooks.ts
L1/L1-P09/starter/src/app/store.ts
L1/L1-P09/starter/src/features/clubs/clubsSlice.ts
L1/L1-P09/starter/src/main.tsx
L1/L1-P09/starter/src/styles.css
L1/L1-P09/starter/tests/jest/logic.jest.test.ts
L1/L1-P09/starter/tests/setup.ts
L1/L1-P09/starter/tests/vitest/logic.test.ts
L1/L1-P09/starter/tsconfig.json
L1/L1-P09/starter/vite.config.ts
L1/L1-P09/starter/vitest.config.ts
L1/L1-P10/solution/README.md
L1/L1-P10/solution/babel.config.cjs
L1/L1-P10/solution/index.html
L1/L1-P10/solution/jest.config.cjs
L1/L1-P10/solution/package.json
L1/L1-P10/solution/src/App.tsx
L1/L1-P10/solution/src/app/hooks.ts
L1/L1-P10/solution/src/app/store.ts
L1/L1-P10/solution/src/features/clubs/clubsSlice.ts
L1/L1-P10/solution/src/main.tsx
L1/L1-P10/solution/src/styles.css
L1/L1-P10/solution/tests/jest/logic.jest.test.ts
L1/L1-P10/solution/tests/setup.ts
L1/L1-P10/solution/tests/vitest/logic.test.ts
L1/L1-P10/solution/tsconfig.json
L1/L1-P10/solution/vite.config.ts
L1/L1-P10/solution/vitest.config.ts
L1/L1-P10/starter/README.md
L1/L1-P10/starter/babel.config.cjs
L1/L1-P10/starter/index.html
L1/L1-P10/starter/jest.config.cjs
L1/L1-P10/starter/package.json
L1/L1-P10/starter/src/App.tsx
L1/L1-P10/starter/src/app/hooks.ts
L1/L1-P10/starter/src/app/store.ts
L1/L1-P10/starter/src/features/clubs/clubsSlice.ts
L1/L1-P10/starter/src/main.tsx
L1/L1-P10/starter/src/styles.css
L1/L1-P10/starter/tests/jest/logic.jest.test.ts
L1/L1-P10/starter/tests/setup.ts
L1/L1-P10/starter/tests/vitest/logic.test.ts
L1/L1-P10/starter/tsconfig.json
L1/L1-P10/starter/vite.config.ts
L1/L1-P10/starter/vitest.config.ts
L1/L1-P11/solution/README.md
L1/L1-P11/solution/babel.config.cjs
L1/L1-P11/solution/index.html
L1/L1-P11/solution/jest.config.cjs
L1/L1-P11/solution/package.json
L1/L1-P11/solution/src/App.tsx
L1/L1-P11/solution/src/app/hooks.ts
L1/L1-P11/solution/src/app/store.ts
L1/L1-P11/solution/src/features/clubs/clubsSlice.ts
L1/L1-P11/solution/src/main.tsx
L1/L1-P11/solution/src/styles.css
L1/L1-P11/solution/tests/jest/logic.jest.test.ts
L1/L1-P11/solution/tests/setup.ts
L1/L1-P11/solution/tests/vitest/logic.test.ts
L1/L1-P11/solution/tsconfig.json
L1/L1-P11/solution/vite.config.ts
L1/L1-P11/solution/vitest.config.ts
L1/L1-P11/starter/README.md
L1/L1-P11/starter/babel.config.cjs
L1/L1-P11/starter/index.html
L1/L1-P11/starter/jest.config.cjs
L1/L1-P11/starter/package.json
L1/L1-P11/starter/src/App.tsx
L1/L1-P11/starter/src/app/hooks.ts
L1/L1-P11/starter/src/app/store.ts
L1/L1-P11/starter/src/features/clubs/clubsSlice.ts
L1/L1-P11/starter/src/main.tsx
L1/L1-P11/starter/src/styles.css
L1/L1-P11/starter/tests/jest/logic.jest.test.ts
L1/L1-P11/starter/tests/setup.ts
L1/L1-P11/starter/tests/vitest/logic.test.ts
L1/L1-P11/starter/tsconfig.json
L1/L1-P11/starter/vite.config.ts
L1/L1-P11/starter/vitest.config.ts
L1/L1-P12/solution/README.md
L1/L1-P12/solution/babel.config.cjs
L1/L1-P12/solution/index.html
L1/L1-P12/solution/jest.config.cjs
L1/L1-P12/solution/package.json
L1/L1-P12/solution/src/App.tsx
L1/L1-P12/solution/src/app/hooks.ts
L1/L1-P12/solution/src/app/store.ts
L1/L1-P12/solution/src/features/clubs/clubsSlice.ts
L1/L1-P12/solution/src/main.tsx
L1/L1-P12/solution/src/styles.css
L1/L1-P12/solution/tests/jest/logic.jest.test.ts
L1/L1-P12/solution/tests/setup.ts
L1/L1-P12/solution/tests/vitest/logic.test.ts
L1/L1-P12/solution/tsconfig.json
L1/L1-P12/solution/vite.config.ts
L1/L1-P12/solution/vitest.config.ts
L1/L1-P12/starter/README.md
L1/L1-P12/starter/babel.config.cjs
L1/L1-P12/starter/index.html
L1/L1-P12/starter/jest.config.cjs
L1/L1-P12/starter/package.json
L1/L1-P12/starter/src/App.tsx
L1/L1-P12/starter/src/app/hooks.ts
L1/L1-P12/starter/src/app/store.ts
L1/L1-P12/starter/src/features/clubs/clubsSlice.ts
L1/L1-P12/starter/src/main.tsx
L1/L1-P12/starter/src/styles.css
L1/L1-P12/starter/tests/jest/logic.jest.test.ts
L1/L1-P12/starter/tests/setup.ts
L1/L1-P12/starter/tests/vitest/logic.test.ts
L1/L1-P12/starter/tsconfig.json
L1/L1-P12/starter/vite.config.ts
L1/L1-P12/starter/vitest.config.ts
L1/L1-P13/solution/README.md
L1/L1-P13/solution/babel.config.cjs
L1/L1-P13/solution/index.html
L1/L1-P13/solution/jest.config.cjs
L1/L1-P13/solution/package.json
L1/L1-P13/solution/src/App.tsx
L1/L1-P13/solution/src/app/hooks.ts
L1/L1-P13/solution/src/app/store.ts
L1/L1-P13/solution/src/features/clubs/clubsSlice.ts
L1/L1-P13/solution/src/main.tsx
L1/L1-P13/solution/src/styles.css
L1/L1-P13/solution/tests/jest/logic.jest.test.ts
L1/L1-P13/solution/tests/setup.ts
L1/L1-P13/solution/tests/vitest/logic.test.ts
L1/L1-P13/solution/tsconfig.json
L1/L1-P13/solution/vite.config.ts
L1/L1-P13/solution/vitest.config.ts
L1/L1-P13/starter/README.md
L1/L1-P13/starter/babel.config.cjs
L1/L1-P13/starter/index.html
L1/L1-P13/starter/jest.config.cjs
L1/L1-P13/starter/package.json
L1/L1-P13/starter/src/App.tsx
L1/L1-P13/starter/src/app/hooks.ts
L1/L1-P13/starter/src/app/store.ts
L1/L1-P13/starter/src/features/clubs/clubsSlice.ts
L1/L1-P13/starter/src/main.tsx
L1/L1-P13/starter/src/styles.css
L1/L1-P13/starter/tests/jest/logic.jest.test.ts
L1/L1-P13/starter/tests/setup.ts
L1/L1-P13/starter/tests/vitest/logic.test.ts
L1/L1-P13/starter/tsconfig.json
L1/L1-P13/starter/vite.config.ts
L1/L1-P13/starter/vitest.config.ts
L1/L1-P14/solution/README.md
L1/L1-P14/solution/babel.config.cjs
L1/L1-P14/solution/index.html
L1/L1-P14/solution/jest.config.cjs
L1/L1-P14/solution/package.json
L1/L1-P14/solution/src/App.tsx
L1/L1-P14/solution/src/app/hooks.ts
L1/L1-P14/solution/src/app/store.ts
L1/L1-P14/solution/src/features/clubs/clubsSlice.ts
L1/L1-P14/solution/src/main.tsx
L1/L1-P14/solution/src/styles.css
L1/L1-P14/solution/tests/jest/logic.jest.test.ts
L1/L1-P14/solution/tests/setup.ts
L1/L1-P14/solution/tests/vitest/logic.test.ts
L1/L1-P14/solution/tsconfig.json
L1/L1-P14/solution/vite.config.ts
L1/L1-P14/solution/vitest.config.ts
L1/L1-P14/starter/README.md
L1/L1-P14/starter/babel.config.cjs
L1/L1-P14/starter/index.html
L1/L1-P14/starter/jest.config.cjs
L1/L1-P14/starter/package.json
L1/L1-P14/starter/src/App.tsx
L1/L1-P14/starter/src/app/hooks.ts
L1/L1-P14/starter/src/app/store.ts
L1/L1-P14/starter/src/features/clubs/clubsSlice.ts
L1/L1-P14/starter/src/main.tsx
L1/L1-P14/starter/src/styles.css
L1/L1-P14/starter/tests/jest/logic.jest.test.ts
L1/L1-P14/starter/tests/setup.ts
L1/L1-P14/starter/tests/vitest/logic.test.ts
L1/L1-P14/starter/tsconfig.json
L1/L1-P14/starter/vite.config.ts
L1/L1-P14/starter/vitest.config.ts
L1/L1-P15/solution/README.md
L1/L1-P15/solution/babel.config.cjs
L1/L1-P15/solution/index.html
L1/L1-P15/solution/jest.config.cjs
L1/L1-P15/solution/package.json
L1/L1-P15/solution/src/App.tsx
L1/L1-P15/solution/src/app/hooks.ts
L1/L1-P15/solution/src/app/store.ts
L1/L1-P15/solution/src/features/clubs/clubsSlice.ts
L1/L1-P15/solution/src/main.tsx
L1/L1-P15/solution/src/styles.css
L1/L1-P15/solution/tests/jest/logic.jest.test.ts
L1/L1-P15/solution/tests/setup.ts
L1/L1-P15/solution/tests/vitest/logic.test.ts
L1/L1-P15/solution/tsconfig.json
L1/L1-P15/solution/vite.config.ts
L1/L1-P15/solution/vitest.config.ts
L1/L1-P15/starter/README.md
L1/L1-P15/starter/babel.config.cjs
L1/L1-P15/starter/index.html
L1/L1-P15/starter/jest.config.cjs
L1/L1-P15/starter/package.json
L1/L1-P15/starter/src/App.tsx
L1/L1-P15/starter/src/app/hooks.ts
L1/L1-P15/starter/src/app/store.ts
L1/L1-P15/starter/src/features/clubs/clubsSlice.ts
L1/L1-P15/starter/src/main.tsx
L1/L1-P15/starter/src/styles.css
L1/L1-P15/starter/tests/jest/logic.jest.test.ts
L1/L1-P15/starter/tests/setup.ts
L1/L1-P15/starter/tests/vitest/logic.test.ts
L1/L1-P15/starter/tsconfig.json
L1/L1-P15/starter/vite.config.ts
L1/L1-P15/starter/vitest.config.ts
L2/L2-P01/solution/README.md
L2/L2-P01/solution/babel.config.cjs
L2/L2-P01/solution/index.html
L2/L2-P01/solution/jest.config.cjs
L2/L2-P01/solution/package.json
L2/L2-P01/solution/src/App.tsx
L2/L2-P01/solution/src/app/hooks.ts
L2/L2-P01/solution/src/app/store.ts
L2/L2-P01/solution/src/features/clubs/clubsSlice.ts
L2/L2-P01/solution/src/main.tsx
L2/L2-P01/solution/src/styles.css
L2/L2-P01/solution/tests/jest/async.jest.test.ts
L2/L2-P01/solution/tests/setup.ts
L2/L2-P01/solution/tests/vitest/async.test.ts
L2/L2-P01/solution/tsconfig.json
L2/L2-P01/solution/vite.config.ts
L2/L2-P01/solution/vitest.config.ts
L2/L2-P01/starter/README.md
L2/L2-P01/starter/babel.config.cjs
L2/L2-P01/starter/index.html
L2/L2-P01/starter/jest.config.cjs
L2/L2-P01/starter/package.json
L2/L2-P01/starter/src/App.tsx
L2/L2-P01/starter/src/app/hooks.ts
L2/L2-P01/starter/src/app/store.ts
L2/L2-P01/starter/src/features/clubs/clubsSlice.ts
L2/L2-P01/starter/src/main.tsx
L2/L2-P01/starter/src/styles.css
L2/L2-P01/starter/tests/jest/async.jest.test.ts
L2/L2-P01/starter/tests/setup.ts
L2/L2-P01/starter/tests/vitest/async.test.ts
L2/L2-P01/starter/tsconfig.json
L2/L2-P01/starter/vite.config.ts
L2/L2-P01/starter/vitest.config.ts
L2/L2-P02/solution/README.md
L2/L2-P02/solution/babel.config.cjs
L2/L2-P02/solution/index.html
L2/L2-P02/solution/jest.config.cjs
L2/L2-P02/solution/package.json
L2/L2-P02/solution/src/App.tsx
L2/L2-P02/solution/src/app/hooks.ts
L2/L2-P02/solution/src/app/store.ts
L2/L2-P02/solution/src/features/clubs/clubsSlice.ts
L2/L2-P02/solution/src/main.tsx
L2/L2-P02/solution/src/styles.css
L2/L2-P02/solution/tests/jest/async.jest.test.ts
L2/L2-P02/solution/tests/setup.ts
L2/L2-P02/solution/tests/vitest/async.test.ts
L2/L2-P02/solution/tsconfig.json
L2/L2-P02/solution/vite.config.ts
L2/L2-P02/solution/vitest.config.ts
L2/L2-P02/starter/README.md
L2/L2-P02/starter/babel.config.cjs
L2/L2-P02/starter/index.html
L2/L2-P02/starter/jest.config.cjs
L2/L2-P02/starter/package.json
L2/L2-P02/starter/src/App.tsx
L2/L2-P02/starter/src/app/hooks.ts
L2/L2-P02/starter/src/app/store.ts
L2/L2-P02/starter/src/features/clubs/clubsSlice.ts
L2/L2-P02/starter/src/main.tsx
L2/L2-P02/starter/src/styles.css
L2/L2-P02/starter/tests/jest/async.jest.test.ts
L2/L2-P02/starter/tests/setup.ts
L2/L2-P02/starter/tests/vitest/async.test.ts
L2/L2-P02/starter/tsconfig.json
L2/L2-P02/starter/vite.config.ts
L2/L2-P02/starter/vitest.config.ts
L2/L2-P03/solution/README.md
L2/L2-P03/solution/babel.config.cjs
L2/L2-P03/solution/index.html
L2/L2-P03/solution/jest.config.cjs
L2/L2-P03/solution/package.json
L2/L2-P03/solution/src/App.tsx
L2/L2-P03/solution/src/app/hooks.ts
L2/L2-P03/solution/src/app/store.ts
L2/L2-P03/solution/src/features/clubs/clubsSlice.ts
L2/L2-P03/solution/src/main.tsx
L2/L2-P03/solution/src/styles.css
L2/L2-P03/solution/tests/jest/async.jest.test.ts
L2/L2-P03/solution/tests/setup.ts
L2/L2-P03/solution/tests/vitest/async.test.ts
L2/L2-P03/solution/tsconfig.json
L2/L2-P03/solution/vite.config.ts
L2/L2-P03/solution/vitest.config.ts
L2/L2-P03/starter/README.md
L2/L2-P03/starter/babel.config.cjs
L2/L2-P03/starter/index.html
L2/L2-P03/starter/jest.config.cjs
L2/L2-P03/starter/package.json
…
L2/L2-P14/solution/src/features/clubs/clubsSlice.ts
L2/L2-P14/solution/src/main.tsx
L2/L2-P14/solution/src/styles.css
L2/L2-P14/solution/tests/jest/async.jest.test.ts
L2/L2-P14/solution/tests/setup.ts
L2/L2-P14/solution/tests/vitest/async.test.ts
L2/L2-P14/solution/tsconfig.json
L2/L2-P14/solution/vite.config.ts
L2/L2-P14/solution/vitest.config.ts
L2/L2-P14/starter/README.md
L2/L2-P14/starter/babel.config.cjs
L2/L2-P14/starter/index.html
L2/L2-P14/starter/jest.config.cjs
L2/L2-P14/starter/package.json
L2/L2-P14/starter/src/App.tsx
L2/L2-P14/starter/src/app/hooks.ts
L2/L2-P14/starter/src/app/store.ts
L2/L2-P14/starter/src/features/clubs/clubsSlice.ts
L2/L2-P14/starter/src/main.tsx
L2/L2-P14/starter/src/styles.css
L2/L2-P14/starter/tests/jest/async.jest.test.ts
L2/L2-P14/starter/tests/setup.ts
L2/L2-P14/starter/tests/vitest/async.test.ts
L2/L2-P14/starter/tsconfig.json
L2/L2-P14/starter/vite.config.ts
L2/L2-P14/starter/vitest.config.ts
L2/L2-P15/solution/README.md
L2/L2-P15/solution/babel.config.cjs
L2/L2-P15/solution/index.html
L2/L2-P15/solution/jest.config.cjs
L2/L2-P15/solution/package.json
L2/L2-P15/solution/src/App.tsx
L2/L2-P15/solution/src/app/hooks.ts
L2/L2-P15/solution/src/app/store.ts
L2/L2-P15/solution/src/features/clubs/clubsSlice.ts
L2/L2-P15/solution/src/main.tsx
L2/L2-P15/solution/src/styles.css
L2/L2-P15/solution/tests/jest/async.jest.test.ts
L2/L2-P15/solution/tests/setup.ts
L2/L2-P15/solution/tests/vitest/async.test.ts
L2/L2-P15/solution/tsconfig.json
L2/L2-P15/solution/vite.config.ts
L2/L2-P15/solution/vitest.config.ts
L2/L2-P15/starter/README.md
L2/L2-P15/starter/babel.config.cjs
L2/L2-P15/starter/index.html
L2/L2-P15/starter/jest.config.cjs
L2/L2-P15/starter/package.json
L2/L2-P15/starter/src/App.tsx
L2/L2-P15/starter/src/app/hooks.ts
L2/L2-P15/starter/src/app/store.ts
L2/L2-P15/starter/src/features/clubs/clubsSlice.ts
L2/L2-P15/starter/src/main.tsx
L2/L2-P15/starter/src/styles.css
L2/L2-P15/starter/tests/jest/async.jest.test.ts
L2/L2-P15/starter/tests/setup.ts
L2/L2-P15/starter/tests/vitest/async.test.ts
L2/L2-P15/starter/tsconfig.json
L2/L2-P15/starter/vite.config.ts
L2/L2-P15/starter/vitest.config.ts
L3/L3-P01/solution/README.md
L3/L3-P01/solution/babel.config.cjs
L3/L3-P01/solution/index.html
L3/L3-P01/solution/jest.config.cjs
L3/L3-P01/solution/package.json
L3/L3-P01/solution/src/App.tsx
L3/L3-P01/solution/src/app/hooks.ts
L3/L3-P01/solution/src/app/store.ts
L3/L3-P01/solution/src/features/clubs/clubsSlice.ts
L3/L3-P01/solution/src/main.tsx
L3/L3-P01/solution/src/services/clubsApi.ts
L3/L3-P01/solution/src/styles.css
L3/L3-P01/solution/tests/jest/query.jest.test.ts
L3/L3-P01/solution/tests/setup.ts
L3/L3-P01/solution/tests/vitest/query.test.ts
L3/L3-P01/solution/tsconfig.json
L3/L3-P01/solution/vite.config.ts
L3/L3-P01/solution/vitest.config.ts
L3/L3-P01/starter/README.md
L3/L3-P01/starter/babel.config.cjs
L3/L3-P01/starter/index.html
L3/L3-P01/starter/jest.config.cjs
L3/L3-P01/starter/package.json
L3/L3-P01/starter/src/App.tsx
L3/L3-P01/starter/src/app/hooks.ts
L3/L3-P01/starter/src/app/store.ts
L3/L3-P01/starter/src/features/clubs/clubsSlice.ts
L3/L3-P01/starter/src/main.tsx
L3/L3-P01/starter/src/services/clubsApi.ts
L3/L3-P01/starter/src/styles.css
L3/L3-P01/starter/tests/jest/query.jest.test.ts
L3/L3-P01/starter/tests/setup.ts
L3/L3-P01/starter/tests/vitest/query.test.ts
L3/L3-P01/starter/tsconfig.json
L3/L3-P01/starter/vite.config.ts
L3/L3-P01/starter/vitest.config.ts
L3/L3-P02/solution/README.md
L3/L3-P02/solution/babel.config.cjs
L3/L3-P02/solution/index.html
L3/L3-P02/solution/jest.config.cjs
L3/L3-P02/solution/package.json
L3/L3-P02/solution/src/App.tsx
L3/L3-P02/solution/src/app/hooks.ts
L3/L3-P02/solution/src/app/store.ts
L3/L3-P02/solution/src/features/clubs/clubsSlice.ts
L3/L3-P02/solution/src/main.tsx
L3/L3-P02/solution/src/services/clubsApi.ts
L3/L3-P02/solution/src/styles.css
L3/L3-P02/solution/tests/jest/query.jest.test.ts
L3/L3-P02/solution/tests/setup.ts
L3/L3-P02/solution/tests/vitest/query.test.ts
L3/L3-P02/solution/tsconfig.json
L3/L3-P02/solution/vite.config.ts
L3/L3-P02/solution/vitest.config.ts
L3/L3-P02/starter/README.md
L3/L3-P02/starter/babel.config.cjs
L3/L3-P02/starter/index.html
L3/L3-P02/starter/jest.config.cjs
L3/L3-P02/starter/package.json
L3/L3-P02/starter/src/App.tsx
L3/L3-P02/starter/src/app/hooks.ts
L3/L3-P02/starter/src/app/store.ts
L3/L3-P02/starter/src/features/clubs/clubsSlice.ts
L3/L3-P02/starter/src/main.tsx
L3/L3-P02/starter/src/services/clubsApi.ts
L3/L3-P02/starter/src/styles.css
L3/L3-P02/starter/tests/jest/query.jest.test.ts
L3/L3-P02/starter/tests/setup.ts
L3/L3-P02/starter/tests/vitest/query.test.ts
L3/L3-P02/starter/tsconfig.json
L3/L3-P02/starter/vite.config.ts
L3/L3-P02/starter/vitest.config.ts
L3/L3-P03/solution/README.md
L3/L3-P03/solution/babel.config.cjs
L3/L3-P03/solution/index.html
L3/L3-P03/solution/jest.config.cjs
L3/L3-P03/solution/package.json
L3/L3-P03/solution/src/App.tsx
L3/L3-P03/solution/src/app/hooks.ts
L3/L3-P03/solution/src/app/store.ts
L3/L3-P03/solution/src/features/clubs/clubsSlice.ts
L3/L3-P03/solution/src/main.tsx
L3/L3-P03/solution/src/services/clubsApi.ts
L3/L3-P03/solution/src/styles.css
L3/L3-P03/solution/tests/jest/query.jest.test.ts
L3/L3-P03/solution/tests/setup.ts
L3/L3-P03/solution/tests/vitest/query.test.ts
L3/L3-P03/solution/tsconfig.json
L3/L3-P03/solution/vite.config.ts
L3/L3-P03/solution/vitest.config.ts
L3/L3-P03/starter/README.md
L3/L3-P03/starter/babel.config.cjs
L3/L3-P03/starter/index.html
L3/L3-P03/starter/jest.config.cjs
L3/L3-P03/starter/package.json
L3/L3-P03/starter/src/App.tsx
L3/L3-P03/starter/src/app/hooks.ts
L3/L3-P03/starter/src/app/store.ts
L3/L3-P03/starter/src/features/clubs/clubsSlice.ts
L3/L3-P03/starter/src/main.tsx
L3/L3-P03/starter/src/services/clubsApi.ts
L3/L3-P03/starter/src/styles.css
L3/L3-P03/starter/tests/jest/query.jest.test.ts
L3/L3-P03/starter/tests/setup.ts
L3/L3-P03/starter/tests/vitest/query.test.ts
L3/L3-P03/starter/tsconfig.json
L3/L3-P03/starter/vite.config.ts
L3/L3-P03/starter/vitest.config.ts
L3/L3-P04/solution/README.md
L3/L3-P04/solution/babel.config.cjs
L3/L3-P04/solution/index.html
L3/L3-P04/solution/jest.config.cjs
L3/L3-P04/solution/package.json
L3/L3-P04/solution/src/App.tsx
L3/L3-P04/solution/src/app/hooks.ts
L3/L3-P04/solution/src/app/store.ts
L3/L3-P04/solution/src/features/clubs/clubsSlice.ts
L3/L3-P04/solution/src/main.tsx
L3/L3-P04/solution/src/services/clubsApi.ts
L3/L3-P04/solution/src/styles.css
L3/L3-P04/solution/tests/jest/query.jest.test.ts
L3/L3-P04/solution/tests/setup.ts
L3/L3-P04/solution/tests/vitest/query.test.ts
L3/L3-P04/solution/tsconfig.json
L3/L3-P04/solution/vite.config.ts
L3/L3-P04/solution/vitest.config.ts
L3/L3-P04/starter/README.md
L3/L3-P04/starter/babel.config.cjs
L3/L3-P04/starter/index.html
L3/L3-P04/starter/jest.config.cjs
L3/L3-P04/starter/package.json
L3/L3-P04/starter/src/App.tsx
L3/L3-P04/starter/src/app/hooks.ts
L3/L3-P04/starter/src/app/store.ts
L3/L3-P04/starter/src/features/clubs/clubsSlice.ts
L3/L3-P04/starter/src/main.tsx
L3/L3-P04/starter/src/services/clubsApi.ts
L3/L3-P04/starter/src/styles.css
L3/L3-P04/starter/tests/jest/query.jest.test.ts
L3/L3-P04/starter/tests/setup.ts
L3/L3-P04/starter/tests/vitest/query.test.ts
L3/L3-P04/starter/tsconfig.json
L3/L3-P04/starter/vite.config.ts
L3/L3-P04/starter/vitest.config.ts
L3/L3-P05/solution/README.md
L3/L3-P05/solution/babel.config.cjs
L3/L3-P05/solution/index.html
L3/L3-P05/solution/jest.config.cjs
L3/L3-P05/solution/package.json
L3/L3-P05/solution/src/App.tsx
L3/L3-P05/solution/src/app/hooks.ts
L3/L3-P05/solution/src/app/store.ts
L3/L3-P05/solution/src/features/clubs/clubsSlice.ts
L3/L3-P05/solution/src/main.tsx
L3/L3-P05/solution/src/services/clubsApi.ts
L3/L3-P05/solution/src/styles.css
L3/L3-P05/solution/tests/jest/query.jest.test.ts
L3/L3-P05/solution/tests/setup.ts
L3/L3-P05/solution/tests/vitest/query.test.ts
L3/L3-P05/solution/tsconfig.json
L3/L3-P05/solution/vite.config.ts
L3/L3-P05/solution/vitest.config.ts
L3/L3-P05/starter/README.md
L3/L3-P05/starter/babel.config.cjs
L3/L3-P05/starter/index.html
L3/L3-P05/starter/jest.config.cjs
L3/L3-P05/starter/package.json
L3/L3-P05/starter/src/App.tsx
L3/L3-P05/starter/src/app/hooks.ts
L3/L3-P05/starter/src/app/store.ts
L3/L3-P05/starter/src/features/clubs/clubsSlice.ts
L3/L3-P05/starter/src/main.tsx
L3/L3-P05/starter/src/services/clubsApi.ts
L3/L3-P05/starter/src/styles.css
L3/L3-P05/starter/tests/jest/query.jest.test.ts
L3/L3-P05/starter/tests/setup.ts
L3/L3-P05/starter/tests/vitest/query.test.ts
L3/L3-P05/starter/tsconfig.json
L3/L3-P05/starter/vite.config.ts
L3/L3-P05/starter/vitest.config.ts
L3/L3-P06/solution/README.md
L3/L3-P06/solution/babel.config.cjs
L3/L3-P06/solution/index.html
L3/L3-P06/solution/jest.config.cjs
L3/L3-P06/solution/package.json
L3/L3-P06/solution/src/App.tsx
L3/L3-P06/solution/src/app/hooks.ts
L3/L3-P06/solution/src/app/store.ts
L3/L3-P06/solution/src/features/clubs/clubsSlice.ts
L3/L3-P06/solution/src/main.tsx
L3/L3-P06/solution/src/services/clubsApi.ts
L3/L3-P06/solution/src/styles.css
L3/L3-P06/solution/tests/jest/query.jest.test.ts
L3/L3-P06/solution/tests/setup.ts
L3/L3-P06/solution/tests/vitest/query.test.ts
L3/L3-P06/solution/tsconfig.json
L3/L3-P06/solution/vite.config.ts
L3/L3-P06/solution/vitest.config.ts
L3/L3-P06/starter/README.md
L3/L3-P06/starter/babel.config.cjs
L3/L3-P06/starter/index.html
L3/L3-P06/starter/jest.config.cjs
L3/L3-P06/starter/package.json
L3/L3-P06/starter/src/App.tsx
L3/L3-P06/starter/src/app/hooks.ts
L3/L3-P06/starter/src/app/store.ts
L3/L3-P06/starter/src/features/clubs/clubsSlice.ts
L3/L3-P06/starter/src/main.tsx
L3/L3-P06/starter/src/services/clubsApi.ts
L3/L3-P06/starter/src/styles.css
L3/L3-P06/starter/tests/jest/query.jest.test.ts
L3/L3-P06/starter/tests/setup.ts
L3/L3-P06/starter/tests/vitest/query.test.ts
L3/L3-P06/starter/tsconfig.json
L3/L3-P06/starter/vite.config.ts
L3/L3-P06/starter/vitest.config.ts
L3/L3-P07/solution/README.md
L3/L3-P07/solution/babel.config.cjs
L3/L3-P07/solution/index.html
L3/L3-P07/solution/jest.config.cjs
L3/L3-P07/solution/package.json
L3/L3-P07/solution/src/App.tsx
L3/L3-P07/solution/src/app/hooks.ts
L3/L3-P07/solution/src/app/store.ts
L3/L3-P07/solution/src/features/clubs/clubsSlice.ts
L3/L3-P07/solution/src/main.tsx
L3/L3-P07/solution/src/services/clubsApi.ts
L3/L3-P07/solution/src/styles.css
L3/L3-P07/solution/tests/jest/query.jest.test.ts
L3/L3-P07/solution/tests/setup.ts
L3/L3-P07/solution/tests/vitest/query.test.ts
L3/L3-P07/solution/tsconfig.json
L3/L3-P07/solution/vite.config.ts
L3/L3-P07/solution/vitest.config.ts
L3/L3-P07/starter/README.md
L3/L3-P07/starter/babel.config.cjs
L3/L3-P07/starter/index.html
L3/L3-P07/starter/jest.config.cjs
L3/L3-P07/starter/package.json
L3/L3-P07/starter/src/App.tsx
L3/L3-P07/starter/src/app/hooks.ts
L3/L3-P07/starter/src/app/store.ts
L3/L3-P07/starter/src/features/clubs/clubsSlice.ts
L3/L3-P07/starter/src/main.tsx
L3/L3-P07/starter/src/services/clubsApi.ts
L3/L3-P07/starter/src/styles.css
L3/L3-P07/starter/tests/jest/query.jest.test.ts
L3/L3-P07/starter/tests/setup.ts
L3/L3-P07/starter/tests/vitest/query.test.ts
L3/L3-P07/starter/tsconfig.json
L3/L3-P07/starter/vite.config.ts
L3/L3-P07/starter/vitest.config.ts
L3/L3-P08/solution/README.md
L3/L3-P08/solution/babel.config.cjs
L3/L3-P08/solution/index.html
L3/L3-P08/solution/jest.config.cjs
L3/L3-P08/solution/package.json
L3/L3-P08/solution/src/App.tsx
L3/L3-P08/solution/src/app/hooks.ts
L3/L3-P08/solution/src/app/store.ts
L3/L3-P08/solution/src/features/clubs/clubsSlice.ts
L3/L3-P08/solution/src/main.tsx
L3/L3-P08/solution/src/services/clubsApi.ts
L3/L3-P08/solution/src/styles.css
L3/L3-P08/solution/tests/jest/query.jest.test.ts
L3/L3-P08/solution/tests/setup.ts
L3/L3-P08/solution/tests/vitest/query.test.ts
L3/L3-P08/solution/tsconfig.json
L3/L3-P08/solution/vite.config.ts
L3/L3-P08/solution/vitest.config.ts
L3/L3-P08/starter/README.md
L3/L3-P08/starter/babel.config.cjs
L3/L3-P08/starter/index.html
L3/L3-P08/starter/jest.config.cjs
L3/L3-P08/starter/package.json
L3/L3-P08/starter/src/App.tsx
L3/L3-P08/starter/src/app/hooks.ts
L3/L3-P08/starter/src/app/store.ts
L3/L3-P08/starter/src/features/clubs/clubsSlice.ts
L3/L3-P08/starter/src/main.tsx
L3/L3-P08/starter/src/services/clubsApi.ts
L3/L3-P08/starter/src/styles.css
L3/L3-P08/starter/tests/jest/query.jest.test.ts
L3/L3-P08/starter/tests/setup.ts
L3/L3-P08/starter/tests/vitest/query.test.ts
L3/L3-P08/starter/tsconfig.json
L3/L3-P08/starter/vite.config.ts
L3/L3-P08/starter/vitest.config.ts
L3/L3-P09/solution/README.md
L3/L3-P09/solution/babel.config.cjs
L3/L3-P09/solution/index.html
L3/L3-P09/solution/jest.config.cjs
L3/L3-P09/solution/package.json
L3/L3-P09/solution/src/App.tsx
L3/L3-P09/solution/src/app/hooks.ts
L3/L3-P09/solution/src/app/store.ts
L3/L3-P09/solution/src/features/clubs/clubsSlice.ts
L3/L3-P09/solution/src/main.tsx
L3/L3-P09/solution/src/services/clubsApi.ts
L3/L3-P09/solution/src/styles.css
L3/L3-P09/solution/tests/jest/query.jest.test.ts
L3/L3-P09/solution/tests/setup.ts
L3/L3-P09/solution/tests/vitest/query.test.ts
L3/L3-P09/solution/tsconfig.json
L3/L3-P09/solution/vite.config.ts
L3/L3-P09/solution/vitest.config.ts
L3/L3-P09/starter/README.md
L3/L3-P09/starter/babel.config.cjs
L3/L3-P09/starter/index.html
L3/L3-P09/starter/jest.config.cjs
L3/L3-P09/starter/package.json
L3/L3-P09/starter/src/App.tsx
L3/L3-P09/starter/src/app/hooks.ts
L3/L3-P09/starter/src/app/store.ts
L3/L3-P09/starter/src/features/clubs/clubsSlice.ts
L3/L3-P09/starter/src/main.tsx
L3/L3-P09/starter/src/services/clubsApi.ts
L3/L3-P09/starter/src/styles.css
L3/L3-P09/starter/tests/jest/query.jest.test.ts
L3/L3-P09/starter/tests/setup.ts
L3/L3-P09/starter/tests/vitest/query.test.ts
L3/L3-P09/starter/tsconfig.json
L3/L3-P09/starter/vite.config.ts
L3/L3-P09/starter/vitest.config.ts
L3/L3-P10/solution/README.md
L3/L3-P10/solution/babel.config.cjs
L3/L3-P10/solution/index.html
L3/L3-P10/solution/jest.config.cjs
L3/L3-P10/solution/package.json
L3/L3-P10/solution/src/App.tsx
L3/L3-P10/solution/src/app/hooks.ts
L3/L3-P10/solution/src/app/store.ts
L3/L3-P10/solution/src/features/clubs/clubsSlice.ts
L3/L3-P10/solution/src/main.tsx
L3/L3-P10/solution/src/services/clubsApi.ts
L3/L3-P10/solution/src/styles.css
L3/L3-P10/solution/tests/jest/query.jest.test.ts
L3/L3-P10/solution/tests/setup.ts
L3/L3-P10/solution/tests/vitest/query.test.ts
L3/L3-P10/solution/tsconfig.json
L3/L3-P10/solution/vite.config.ts
L3/L3-P10/solution/vitest.config.ts
L3/L3-P10/starter/README.md
L3/L3-P10/starter/babel.config.cjs
L3/L3-P10/starter/index.html
L3/L3-P10/starter/jest.config.cjs
L3/L3-P10/starter/package.json
L3/L3-P10/starter/src/App.tsx
L3/L3-P10/starter/src/app/hooks.ts
L3/L3-P10/starter/src/app/store.ts
L3/L3-P10/starter/src/features/clubs/clubsSlice.ts
L3/L3-P10/starter/src/main.tsx
L3/L3-P10/starter/src/services/clubsApi.ts
L3/L3-P10/starter/src/styles.css
L3/L3-P10/starter/tests/jest/query.jest.test.ts
L3/L3-P10/starter/tests/setup.ts
L3/L3-P10/starter/tests/vitest/query.test.ts
L3/L3-P10/starter/tsconfig.json
L3/L3-P10/starter/vite.config.ts
L3/L3-P10/starter/vitest.config.ts
L3/L3-P11/solution/README.md
L3/L3-P11/solution/babel.config.cjs
L3/L3-P11/solution/index.html
L3/L3-P11/solution/jest.config.cjs
L3/L3-P11/solution/package.json
L3/L3-P11/solution/src/App.tsx
L3/L3-P11/solution/src/app/hooks.ts
L3/L3-P11/solution/src/app/store.ts
L3/L3-P11/solution/src/features/clubs/clubsSlice.ts
L3/L3-P11/solution/src/main.tsx
L3/L3-P11/solution/src/services/clubsApi.ts
L3/L3-P11/solution/src/styles.css
L3/L3-P11/solution/tests/jest/query.jest.test.ts
L3/L3-P11/solution/tests/setup.ts
L3/L3-P11/solution/tests/vitest/query.test.ts
L3/L3-P11/solution/tsconfig.json
L3/L3-P11/solution/vite.config.ts
L3/L3-P11/solution/vitest.config.ts
L3/L3-P11/starter/README.md
L3/L3-P11/starter/babel.config.cjs
L3/L3-P11/starter/index.html
L3/L3-P11/starter/jest.config.cjs
L3/L3-P11/starter/package.json
L3/L3-P11/starter/src/App.tsx
L3/L3-P11/starter/src/app/hooks.ts
L3/L3-P11/starter/src/app/store.ts
L3/L3-P11/starter/src/features/clubs/clubsSlice.ts
L3/L3-P11/starter/src/main.tsx
L3/L3-P11/starter/src/services/clubsApi.ts
L3/L3-P11/starter/src/styles.css
L3/L3-P11/starter/tests/jest/query.jest.test.ts
L3/L3-P11/starter/tests/setup.ts
L3/L3-P11/starter/tests/vitest/query.test.ts
L3/L3-P11/starter/tsconfig.json
L3/L3-P11/starter/vite.config.ts
L3/L3-P11/starter/vitest.config.ts
L3/L3-P12/solution/README.md
L3/L3-P12/solution/babel.config.cjs
L3/L3-P12/solution/index.html
L3/L3-P12/solution/jest.config.cjs
L3/L3-P12/solution/package.json
L3/L3-P12/solution/src/App.tsx
L3/L3-P12/solution/src/app/hooks.ts
L3/L3-P12/solution/src/app/store.ts
L3/L3-P12/solution/src/features/clubs/clubsSlice.ts
L3/L3-P12/solution/src/main.tsx
L3/L3-P12/solution/src/services/clubsApi.ts
L3/L3-P12/solution/src/styles.css
L3/L3-P12/solution/tests/jest/query.jest.test.ts
L3/L3-P12/solution/tests/setup.ts
L3/L3-P12/solution/tests/vitest/query.test.ts
L3/L3-P12/solution/tsconfig.json
L3/L3-P12/solution/vite.config.ts
L3/L3-P12/solution/vitest.config.ts
L3/L3-P12/starter/README.md
L3/L3-P12/starter/babel.config.cjs
L3/L3-P12/starter/index.html
L3/L3-P12/starter/jest.config.cjs
L3/L3-P12/starter/package.json
L3/L3-P12/starter/src/App.tsx
L3/L3-P12/starter/src/app/hooks.ts
L3/L3-P12/starter/src/app/store.ts
L3/L3-P12/starter/src/features/clubs/clubsSlice.ts
L3/L3-P12/starter/src/main.tsx
L3/L3-P12/starter/src/services/clubsApi.ts
L3/L3-P12/starter/src/styles.css
L3/L3-P12/starter/tests/jest/query.jest.test.ts
L3/L3-P12/starter/tests/setup.ts
L3/L3-P12/starter/tests/vitest/query.test.ts
L3/L3-P12/starter/tsconfig.json
L3/L3-P12/starter/vite.config.ts
L3/L3-P12/starter/vitest.config.ts
L3/L3-P13/solution/README.md
L3/L3-P13/solution/babel.config.cjs
L3/L3-P13/solution/index.html
L3/L3-P13/solution/jest.config.cjs
L3/L3-P13/solution/package.json
L3/L3-P13/solution/src/App.tsx
L3/L3-P13/solution/src/app/hooks.ts
L3/L3-P13/solution/src/app/store.ts
L3/L3-P13/solution/src/features/clubs/clubsSlice.ts
L3/L3-P13/solution/src/main.tsx
L3/L3-P13/solution/src/services/clubsApi.ts
L3/L3-P13/solution/src/styles.css
L3/L3-P13/solution/tests/jest/query.jest.test.ts
L3/L3-P13/solution/tests/setup.ts
L3/L3-P13/solution/tests/vitest/query.test.ts
L3/L3-P13/solution/tsconfig.json
L3/L3-P13/solution/vite.config.ts
L3/L3-P13/solution/vitest.config.ts
L3/L3-P13/starter/README.md
L3/L3-P13/starter/babel.config.cjs
L3/L3-P13/starter/index.html
L3/L3-P13/starter/jest.config.cjs
L3/L3-P13/starter/package.json
L3/L3-P13/starter/src/App.tsx
L3/L3-P13/starter/src/app/hooks.ts
L3/L3-P13/starter/src/app/store.ts
L3/L3-P13/starter/src/features/clubs/clubsSlice.ts
L3/L3-P13/starter/src/main.tsx
L3/L3-P13/starter/src/services/clubsApi.ts
L3/L3-P13/starter/src/styles.css
L3/L3-P13/starter/tests/jest/query.jest.test.ts
L3/L3-P13/starter/tests/setup.ts
L3/L3-P13/starter/tests/vitest/query.test.ts
L3/L3-P13/starter/tsconfig.json
L3/L3-P13/starter/vite.config.ts
L3/L3-P13/starter/vitest.config.ts
L3/L3-P14/solution/README.md
L3/L3-P14/solution/babel.config.cjs
L3/L3-P14/solution/index.html
L3/L3-P14/solution/jest.config.cjs
L3/L3-P14/solution/package.json
L3/L3-P14/solution/src/App.tsx
L3/L3-P14/solution/src/app/hooks.ts
L3/L3-P14/solution/src/app/store.ts
L3/L3-P14/solution/src/features/clubs/clubsSlice.ts
L3/L3-P14/solution/src/main.tsx
L3/L3-P14/solution/src/services/clubsApi.ts
L3/L3-P14/solution/src/styles.css
L3/L3-P14/solution/tests/jest/query.jest.test.ts
L3/L3-P14/solution/tests/setup.ts
L3/L3-P14/solution/tests/vitest/query.test.ts
L3/L3-P14/solution/tsconfig.json
L3/L3-P14/solution/vite.config.ts
L3/L3-P14/solution/vitest.config.ts
L3/L3-P14/starter/README.md
L3/L3-P14/starter/babel.config.cjs
L3/L3-P14/starter/index.html
L3/L3-P14/starter/jest.config.cjs
L3/L3-P14/starter/package.json
L3/L3-P14/starter/src/App.tsx
L3/L3-P14/starter/src/app/hooks.ts
L3/L3-P14/starter/src/app/store.ts
L3/L3-P14/starter/src/features/clubs/clubsSlice.ts
L3/L3-P14/starter/src/main.tsx
L3/L3-P14/starter/src/services/clubsApi.ts
L3/L3-P14/starter/src/styles.css
L3/L3-P14/starter/tests/jest/query.jest.test.ts
L3/L3-P14/starter/tests/setup.ts
L3/L3-P14/starter/tests/vitest/query.test.ts
L3/L3-P14/starter/tsconfig.json
L3/L3-P14/starter/vite.config.ts
L3/L3-P14/starter/vitest.config.ts
L3/L3-P15/solution/README.md
L3/L3-P15/solution/babel.config.cjs
L3/L3-P15/solution/index.html
L3/L3-P15/solution/jest.config.cjs
L3/L3-P15/solution/package.json
L3/L3-P15/solution/src/App.tsx
L3/L3-P15/solution/src/app/hooks.ts
L3/L3-P15/solution/src/app/store.ts
L3/L3-P15/solution/src/features/clubs/clubsSlice.ts
L3/L3-P15/solution/src/main.tsx
L3/L3-P15/solution/src/services/clubsApi.ts
L3/L3-P15/solution/src/styles.css
L3/L3-P15/solution/tests/jest/query.jest.test.ts
L3/L3-P15/solution/tests/setup.ts
L3/L3-P15/solution/tests/vitest/query.test.ts
L3/L3-P15/solution/tsconfig.json
L3/L3-P15/solution/vite.config.ts
L3/L3-P15/solution/vitest.config.ts
L3/L3-P15/starter/README.md
L3/L3-P15/starter/babel.config.cjs
L3/L3-P15/starter/index.html
L3/L3-P15/starter/jest.config.cjs
L3/L3-P15/starter/package.json
L3/L3-P15/starter/src/App.tsx
L3/L3-P15/starter/src/app/hooks.ts
L3/L3-P15/starter/src/app/store.ts
L3/L3-P15/starter/src/features/clubs/clubsSlice.ts
L3/L3-P15/starter/src/main.tsx
L3/L3-P15/starter/src/services/clubsApi.ts
L3/L3-P15/starter/src/styles.css
L3/L3-P15/starter/tests/jest/query.jest.test.ts
L3/L3-P15/starter/tests/setup.ts
L3/L3-P15/starter/tests/vitest/query.test.ts
L3/L3-P15/starter/tsconfig.json
L3/L3-P15/starter/vite.config.ts
L3/L3-P15/starter/vitest.config.ts
```

**Variante detectate:** solution: 780, starter: 780.

**Categorii de fișiere:** config: 540, public: 90, docs: 90, code: 570, tests: 270.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `L1/L1-P01/starter/package.json`: name=`l1-p01-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P01/solution/package.json`: name=`l1-p01-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P02/starter/package.json`: name=`l1-p02-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P02/solution/package.json`: name=`l1-p02-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P03/starter/package.json`: name=`l1-p03-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P03/solution/package.json`: name=`l1-p03-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P04/starter/package.json`: name=`l1-p04-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P04/solution/package.json`: name=`l1-p04-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P05/starter/package.json`: name=`l1-p05-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P05/solution/package.json`: name=`l1-p05-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P06/starter/package.json`: name=`l1-p06-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P06/solution/package.json`: name=`l1-p06-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P07/starter/package.json`: name=`l1-p07-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P07/solution/package.json`: name=`l1-p07-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P08/starter/package.json`: name=`l1-p08-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P08/solution/package.json`: name=`l1-p08-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P09/starter/package.json`: name=`l1-p09-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P09/solution/package.json`: name=`l1-p09-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P10/starter/package.json`: name=`l1-p10-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P10/solution/package.json`: name=`l1-p10-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P11/starter/package.json`: name=`l1-p11-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P11/solution/package.json`: name=`l1-p11-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P12/starter/package.json`: name=`l1-p12-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P12/solution/package.json`: name=`l1-p12-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P13/starter/package.json`: name=`l1-p13-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P13/solution/package.json`: name=`l1-p13-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P14/starter/package.json`: name=`l1-p14-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P14/solution/package.json`: name=`l1-p14-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P15/starter/package.json`: name=`l1-p15-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L1/L1-P15/solution/package.json`: name=`l1-p15-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P01/starter/package.json`: name=`l2-p01-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P01/solution/package.json`: name=`l2-p01-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P02/starter/package.json`: name=`l2-p02-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P02/solution/package.json`: name=`l2-p02-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P03/starter/package.json`: name=`l2-p03-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P03/solution/package.json`: name=`l2-p03-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P04/starter/package.json`: name=`l2-p04-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P04/solution/package.json`: name=`l2-p04-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P05/starter/package.json`: name=`l2-p05-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P05/solution/package.json`: name=`l2-p05-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P06/starter/package.json`: name=`l2-p06-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P06/solution/package.json`: name=`l2-p06-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P07/starter/package.json`: name=`l2-p07-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P07/solution/package.json`: name=`l2-p07-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P08/starter/package.json`: name=`l2-p08-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P08/solution/package.json`: name=`l2-p08-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P09/starter/package.json`: name=`l2-p09-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P09/solution/package.json`: name=`l2-p09-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P10/starter/package.json`: name=`l2-p10-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P10/solution/package.json`: name=`l2-p10-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P11/starter/package.json`: name=`l2-p11-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P11/solution/package.json`: name=`l2-p11-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P12/starter/package.json`: name=`l2-p12-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P12/solution/package.json`: name=`l2-p12-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P13/starter/package.json`: name=`l2-p13-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P13/solution/package.json`: name=`l2-p13-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P14/starter/package.json`: name=`l2-p14-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P14/solution/package.json`: name=`l2-p14-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P15/starter/package.json`: name=`l2-p15-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L2/L2-P15/solution/package.json`: name=`l2-p15-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P01/starter/package.json`: name=`l3-p01-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P01/solution/package.json`: name=`l3-p01-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P02/starter/package.json`: name=`l3-p02-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P02/solution/package.json`: name=`l3-p02-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P03/starter/package.json`: name=`l3-p03-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P03/solution/package.json`: name=`l3-p03-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P04/starter/package.json`: name=`l3-p04-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P04/solution/package.json`: name=`l3-p04-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P05/starter/package.json`: name=`l3-p05-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P05/solution/package.json`: name=`l3-p05-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P06/starter/package.json`: name=`l3-p06-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P06/solution/package.json`: name=`l3-p06-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P07/starter/package.json`: name=`l3-p07-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P07/solution/package.json`: name=`l3-p07-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P08/starter/package.json`: name=`l3-p08-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P08/solution/package.json`: name=`l3-p08-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P09/starter/package.json`: name=`l3-p09-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P09/solution/package.json`: name=`l3-p09-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P10/starter/package.json`: name=`l3-p10-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P10/solution/package.json`: name=`l3-p10-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P11/starter/package.json`: name=`l3-p11-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P11/solution/package.json`: name=`l3-p11-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P12/starter/package.json`: name=`l3-p12-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P12/solution/package.json`: name=`l3-p12-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P13/starter/package.json`: name=`l3-p13-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P13/solution/package.json`: name=`l3-p13-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P14/starter/package.json`: name=`l3-p14-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P14/solution/package.json`: name=`l3-p14-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P15/starter/package.json`: name=`l3-p15-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest
- `L3/L3-P15/solution/package.json`: name=`l3-p15-rtk` type=`module` workspaces=False
  - **Scripturi:**
  - `dev` → `vite`
  - `build` → `vite build`
  - `preview` → `vite preview`
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** @reduxjs/toolkit, react, react-dom, react-redux, reselect
  - **DevDeps:** @babel/preset-env, @babel/preset-react, @babel/preset-typescript, @testing-library/jest-dom, @testing-library/react, @testing-library/user-event, @types/jest, @types/node, @types/react, @types/react-dom, @vitejs/plugin-react, babel-jest, jest, jsdom, msw, typescript, vite, vitest

### Seminar11_Partea3_RTK_p3-READMEs.zip

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

### Seminar11_Partea1_ReduxToolkit_Teorie_extinsa.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 11 — Gestionarea stării cu Redux Toolkit
Partea 1 — Teorie extinsă (narativ + exemple)
- HOOK (situație realistă). „ClubHub+” crește: asociația studențească are dintr‑odată mii de membri, mai multe filiale, coordonatori (lead), evenimente recurente și roluri diferite (admin, treasurer, content, logistics). Datele sosesc din multe direcții: formulare de înscriere, endpoint‑uri HTTP (REST), CSV‑uri importate, iar UI‑ul afişează filtre, paginare, dialoguri de confirmare, meniuri. La început, am folosit state local (useState) şi context pentru câteva setări. După câteva săptămâni, apar simptome clasice: „prop drilling”, duplicare de „surse ale adevărului” (aceeaşi persoană apare diferit în două locuri), efecte asincrone presărate prin componente, teste fragile, re‑randări aleatoare, bug‑uri greu de reprodus. Echipa cere un „control room” pentru starea aplicaţiei: un loc previzibil, urmărit în timp, cu reguli clare pentru cum intră, se schimbă şi iese datele. Aici intră Redux Toolkit (RTK): recomandarea oficială pentru a scrie logică Redux modernă, cu API‑uri ce reduc boilerplate‑ul, standardizează structura şi oferă instrumente de performanţă şi testare.
- 1. De ce Redux (şi de ce Redux Toolkit) „astăzi”
În aplicaţii reale, nu toate stările sunt egale. O parte este „UI state” (toggle‑uri, meniuri deschise, input‑uri temporare), o parte este „app state” (date partajate între ecrane: utilizatorul curent, setări, colecţii de entităţi precum clubs/members/events), iar o parte este „server cache” (date provenite din reţea, cu invalidări şi politici de re‑fetch). Încercarea de a le trata pe toate la fel, doar cu state local, produce rapid inconsistenţe. Redux propune un model simplu şi riguros: o „single source of truth”, actualizări prin „actions” şi „reducers” pure (fără efecte colaterale), flux unidirecţional şi posibilitatea de „time‑travel” (DevTools). În practică însă, Redux „clasic” cerea multe fişiere, tipare repetitive şi configurări migăloase. Redux Toolkit (RTK) a apărut exact pentru a face din bunele practici reguli implicite: configureStore, createSlice, createAsyncThunk, createEntityAdapter, plus RTK Query pentru „server state”. Împreună, acestea reduc zgomotul, previn greşelile tipice şi fac codul mai lizibil, mai uşor de testat şi extins.

### Seminar11_Partea2_ReduxToolkit(RTK)_Ghid_Arhive.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhive (Seminarul 11, Partea 2)
- Acest ghid explică **ce conțin** arhivele și **cum se folosesc**.
- ## Arhive livrate
1) **s11p2-standalone.zip** — proiect Vite + React + TS + Redux Toolkit (RTK), React‑Redux, Reselect, MSW; Vitest & Jest (JSDOM).
2) **s11p2-monorepo.zip** — PNPM workspaces; pachet `packages/lab` conține aceeași aplicație (util pentru CI agregat).

### Seminar11_Partea2_ReduxToolkit(RTK)_Laborator_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 11 — Redux Toolkit — Partea 2 (Laborator extins)
- **Obiectivul Părții 2** este să construim, end‑to‑end, o aplicație didactică „**ClubHub+ State**” în **React + TypeScript** cu **Redux Toolkit (RTK)**, pentru a exersa: *slices* cu `createSlice`, *entități normalizate* cu `createEntityAdapter`, *selectori memoizați* (Reselect), *flux asincron* cu `createAsyncThunk` (și, opțional, **RTK Query**), *integrare UI* (React‑Redux), *persistență minimală* și **testare duală** (**Vitest** & **Jest**) pe aceeași bază de cod. Fiecare etapă include: **worksheet** (cerință + checklist), **starter code**, **teste**, și **AI‑assist** (prompts concise pentru GitHub Copilot sub VSL).
- ---

### Seminar11_Partea3_Arhive_Ghid.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhive (Seminarul 11, Partea 3)
- ## Arhive livrate
1) **s11p3-standalone.zip** — toate cele 45 de proiecte, fiecare cu `starter/` + `solution/`, testare duală (Vitest & Jest) și README.
2) **s11p3-monorepo.zip** — PNPM workspaces; toate **starter-ele** în `packages/*` (fără soluții) pentru lucru incremental și CI la scară.
3) **s11p3-readmes.zip** — toate README‑urile (starter + solution) într‑un singur pachet (audit rapid).

## Cum rulezi un proiect (standalone)
```bash
unzip s11p3-standalone.zip
cd s11p3-standalone/L1/L1-P01/starter
npm i
npm test
npm run dev
```

## Cum rulezi monorepo (PNPM)
```bash
unzip s11p3-monorepo.zip
cd s11p3-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter l1-p01-starter run dev
```

## Structură standard de proiect
- `src/app/` (store.ts, hooks.ts)
- `src/features/clubs/` (clubsSlice.ts — diferă între starter/solution și între niveluri)
- `src/services/` (doar la L3: `clubsApi.ts` — RTK Query)
- `src/App.tsx`, `src/main.tsx`, `index.html`, `src/styles.css`
- `tests/` — `setup.ts`, plus suite Vitest/Jest (L1: logic; L2: async thunk; L3: query service)
- `vite.config.ts`, `vitest.config.ts`, `jest.config.cjs`, `babel.config.cjs`, `tsconfig.json`

## Troubleshooting
- **Eșec de build/test**: verifică versiunea Node și instalarea dependențelor.
- **Jest TSX**: necesită `babel-jest` + preseturi corecte (inclus deja).
- **Vitest JSDOM**: `environment: 'jsdom'` și `setupFiles` sunt setate.
- **Testele L2**: necesită `msw` la runtime (start/stop în `tests/setup.ts`).

### Seminar11_Partea3_RTK_Proiecte_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 11 — Redux Toolkit — Partea 3 (Proiecte/teme, extins)
- Această Parte 3 propune **45 de proiecte** (15 × L1, 15 × L2, 15 × L3) pentru consolidarea **Redux Toolkit** într‑un mod progresiv. Fiecare proiect vine cu:
• **specificații**, **learning goals**, **sugestii AI‑assist (VSL)**,
• un **starter** (în care testele pot pica) și o **solution** (minimă, verde),
• **teste duale** (Vitest & Jest) și **README.md** dedicat,
• integrare de bază cu **TypeScript** și structură RTK standard.

Nivelurile acoperă: L1 — *fundamente (slice, entityAdapter, selectors, wiring UI)*; L2 — *asincron (thunks + MSW), persistență, middleware, Reselect perf, code‑splitting, RTK Query intro*; L3 — *modele avansate (multi‑entity, Query avansat, optimistic robust, WS middleware, SSR/hydration, cross‑slice, Zod, profilare, migrare, securitate)*.
- # L1 (Fundamental) — 15 proiecte

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
| `src/app/store.ts` | Store configurat cu RTK (`configureStore`), middleware, DevTools. |
| `src/app/hooks.ts` | „typed hooks” pentru `useDispatch`/`useSelector`. |
| `src/features/clubs/clubsSlice.ts` | Slice RTK (adapter, thunks, selectori). |
| `src/services/clubsApi.ts` | RTK Query `createApi` (server cache). |

## 5. Corelații cod ↔ configurări ↔ teste


- **Slices/Selectors/Thunks** (în `src/features/...`) au **teste duble** (Vitest & Jest) care verifică reducerii, selectorii memoizați (`Reselect`) și tranzițiile de stare ale `createAsyncThunk` — aceleași contracte validate în ambele suite.  
- **`.env.example`**: variabilele `VITE_*` se propagă în build-ul Vite; restul pot fi folosite în scripturi/CI.  
- **ESLint + CI**: pipeline-urile (`.github/workflows/*`) rulează `lint` și `test`, blocând PR‑uri cu erori. Pentru proiectele avansate (L3), pot exista e2e suplimentare.  
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S11 dezvoltă un **model riguros de gestionare a stării** cu **Redux Toolkit** (RTK 2.x) în React + TypeScript, cu **testare duală** (Vitest & Jest), **MSW** pentru mock API și, opțional, **RTK Query** pentru „server cache”. Conținutul teoretic este mapat pe structura arhivelor și pe proiectele L1–L3. ### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; rădăcină + `packages/*` |
| Instalare | `npm i` | `pnpm i -w` |
| Testare | `npm test` (Vitest & Jest) | `pnpm -w run test` sau `--filter` |
| CI | Workflows simple per proiect | Workflows agregate, matrice pe pachete |
| Scalare (45 proiecte) | multiplicare directoare | pachete dedicate în `packages/*` |
| Public țintă | începători | echipe/colecții avansate |
### Inventar pe arhivă (roluri)

- **Seminar11_Partea2_ReduxToolkit(RTK)_p2-monorepo.zip** — config=8, public=1, code=14, tests=11, docs=2.
- **Seminar11_Partea2_ReduxToolkit(RTK)_p2-standalone.zip** — config=6, public=1, code=14, tests=11, docs=2.
- **Seminar11_Partea3_RTK_p3-monorepo.zip** — config=272, public=45, docs=45, code=285, tests=135.
- **Seminar11_Partea3_RTK_p3-standalone.zip** — config=540, public=90, docs=90, code=570, tests=270.
- **Seminar11_Partea3_RTK_p3-READMEs.zip** — docs=90.
### Explicații fișier-cu-fișier

Consultați tabelul din §4; pentru proiectele L3 unde există RTK Query, verificați `src/services/*` și testele aferente.
### Corelații între fișiere


- `src/features/clubs/clubsSlice.ts` ↔ `tests/*`: reduceri, selectori (memoizați), thunks (MSW).  
- `src/services/clubsApi.ts` (dacă prezent) ↔ teste pentru Query/mutations cu invalidări.  
- `.github/workflows/*` ↔ `lint`/`test`: pipeline determinist pentru PR-uri.  
### Recomandări pentru studenți


1) **Începeți în standalone** (curba mai lină).  
2) **Normalizați entitățile** (`createEntityAdapter`) și scrieți **selectori compuși**.  
3) **Separați „app state” de „server cache”**: thunks vs. RTK Query.  
4) **Testați la fiecare pas** (Vitest & Jest) și folosiți **MSW** pentru stabilitate.  
5) **Respectați accesibilitatea** și folosiți chei stabile (`id`).  
6) **Documentați contractele** în README per proiect (starter/solution).  
### Instrucțiuni „Quick start” per arhivă


**Partea 2 — standalone:**
```bash
unzip "Seminar11_Partea2_ReduxToolkit(RTK)_p2-standalone.zip" -d s11p2-standalone
cd s11p2-standalone
npm i
npm test
npm run dev
```

**Partea 2 — monorepo:**
```bash
unzip "Seminar11_Partea2_ReduxToolkit(RTK)_p2-monorepo.zip" -d s11p2-monorepo
cd s11p2-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter lab run dev
```

**Partea 3 — standalone (proiecte):**
```bash
unzip "Seminar11_Partea3_RTK_p3-standalone.zip" -d s11p3-standalone
cd s11p3-standalone/L1/L1-P01/starter
npm i
npm test
npm run dev
```

**Partea 3 — monorepo (proiecte):**
```bash
unzip "Seminar11_Partea3_RTK_p3-monorepo.zip" -d s11p3-monorepo
cd s11p3-monorepo
pnpm i -w
pnpm -w run test
pnpm --filter l1-p01-starter run dev
```
### Troubleshooting (erori frecvente)


- **Jest nu transpilează TSX** → `babel-jest` + preseturi; `testEnvironment:'jsdom'`.  
- **Vitest fără JSDOM** → `environment:'jsdom'` + `setupFiles` corecte.  
- **MSW nu răspunde** → import corect `tests/setup.ts`; nu amesteca *browser* vs. *node server* în teste.  
- **Flaky tests** → `userEvent` + *await* pentru UI asincron; izolați statul între teste.  
- **PNPM filter** → dacă un pachet nu este găsit, verificați `pnpm-workspace.yaml` și `name` în `package.json`.  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** — motivația RTK, slices, entityAdapter, selectori memoizați, thunks, RTK Query (→ reflectate în structura codului și în testele duale).  
- **Partea 2 (Laborator)** — „ClubHub+ State”: pipeline curat, testare duală, MSW, persistență minimală (→ oglindite în structura arhivelor).  
- **Partea 3 (Proiecte)** — 45 proiecte L1–L3 cu extensii (Query avansat, optimistic, WS, SSR) și rubrică de evaluare (→ mapate în folderele starter/solution).  
### Prompt-șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S11** (standalone & monorepo) o aplicație React/TS cu Redux Toolkit 2.x: slices cu `createEntityAdapter`, selectori memoizați, `createAsyncThunk` + MSW și (opțional) RTK Query; include testare dublă **Vitest/Jest**, CI, README cu Quick start & Troubleshooting și variante **starter**/**solution**.”
