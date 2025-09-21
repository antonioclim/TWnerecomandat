# Seminarul S4 — ES Modules, Events & DOM — Analiză integrată (standalone & monorepo)

*Generat la 2025-09-21 10:24.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar4_p2-lab-standalone.zip

```
README.md
babel.config.cjs
jest.config.cjs
package.json
public/data/events.json
public/index.html
public/styles.css
src/bus.js
src/dom.js
src/events.js
src/filters.js
src/loader.js
src/main.js
src/services/data.js
src/ui/list.js
tests/jest/abort.jest.test.js
tests/jest/bus.jest.test.js
tests/jest/csp.jest.test.js
tests/jest/delegation.jest.test.js
tests/jest/dom.jest.test.js
tests/jest/lazy.jest.test.js
tests/jest/renderList.jest.test.js
tests/vitest/abort.test.js
tests/vitest/bus.test.js
tests/vitest/csp.test.js
tests/vitest/delegation.test.js
tests/vitest/dom.test.js
tests/vitest/lazy.test.js
tests/vitest/renderList.test.js
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 4, docs: 1, code: 8, public: 3, tests: 14.

**package.json — sinteză (scripturi, workspaces, dependențe — eșantion)**

- `package.json`: name=`s4-p2-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server

### Seminar4_p2-monorepo.zip

```
.github/workflows/unit-jest.yml
.github/workflows/unit-vitest.yml
package.json
packages/lab-s4/README.md
packages/lab-s4/babel.config.cjs
packages/lab-s4/jest.config.cjs
packages/lab-s4/package.json
packages/lab-s4/public/data/events.json
packages/lab-s4/public/index.html
packages/lab-s4/public/styles.css
packages/lab-s4/src/bus.js
packages/lab-s4/src/dom.js
packages/lab-s4/src/events.js
packages/lab-s4/src/filters.js
packages/lab-s4/src/loader.js
packages/lab-s4/src/main.js
packages/lab-s4/src/services/data.js
packages/lab-s4/src/ui/list.js
packages/lab-s4/tests/jest/abort.jest.test.js
packages/lab-s4/tests/jest/bus.jest.test.js
packages/lab-s4/tests/jest/csp.jest.test.js
packages/lab-s4/tests/jest/delegation.jest.test.js
packages/lab-s4/tests/jest/dom.jest.test.js
packages/lab-s4/tests/jest/lazy.jest.test.js
packages/lab-s4/tests/jest/renderList.jest.test.js
packages/lab-s4/tests/vitest/abort.test.js
packages/lab-s4/tests/vitest/bus.test.js
packages/lab-s4/tests/vitest/csp.test.js
packages/lab-s4/tests/vitest/delegation.test.js
packages/lab-s4/tests/vitest/dom.test.js
packages/lab-s4/tests/vitest/lazy.test.js
packages/lab-s4/tests/vitest/renderList.test.js
packages/lab-s4/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 6, docs: 1, code: 8, public: 3, tests: 14, ci: 2.

**package.json — sinteză (scripturi, workspaces, dependențe — eșantion)**

- `package.json`: name=`s4-p2-monorepo` type=`None` workspaces=False
  - **Scripturi:**
  - `test` → `pnpm -r run test`
  - **Deps:** 
  - **DevDeps:** vitest, jest, @babel/preset-env, babel-jest, jsdom, http-server
- `packages/lab-s4/package.json`: name=`@s4/lab-s4` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server

### Seminar4_p3-standalone.zip

```
L1/L1-p01-esm-bootstrap/README.md
L1/L1-p01-esm-bootstrap/babel.config.cjs
L1/L1-p01-esm-bootstrap/jest.config.cjs
L1/L1-p01-esm-bootstrap/package.json
L1/L1-p01-esm-bootstrap/public/data/events.json
L1/L1-p01-esm-bootstrap/public/index.html
L1/L1-p01-esm-bootstrap/public/styles.css
L1/L1-p01-esm-bootstrap/src/dom.js
L1/L1-p01-esm-bootstrap/src/events.js
L1/L1-p01-esm-bootstrap/src/filters.js
L1/L1-p01-esm-bootstrap/src/loader.js
L1/L1-p01-esm-bootstrap/src/main.js
L1/L1-p01-esm-bootstrap/src/services/data.js
L1/L1-p01-esm-bootstrap/src/ui/list.js
L1/L1-p01-esm-bootstrap/tests/jest/spec.jest.test.js
L1/L1-p01-esm-bootstrap/tests/vitest/spec.test.js
L1/L1-p01-esm-bootstrap/vitest.config.ts
L1/L1-p02-dom-helpers/README.md
L1/L1-p02-dom-helpers/babel.config.cjs
L1/L1-p02-dom-helpers/jest.config.cjs
L1/L1-p02-dom-helpers/package.json
L1/L1-p02-dom-helpers/public/data/events.json
L1/L1-p02-dom-helpers/public/index.html
L1/L1-p02-dom-helpers/public/styles.css
L1/L1-p02-dom-helpers/src/dom.js
L1/L1-p02-dom-helpers/src/events.js
L1/L1-p02-dom-helpers/src/filters.js
L1/L1-p02-dom-helpers/src/loader.js
L1/L1-p02-dom-helpers/src/main.js
L1/L1-p02-dom-helpers/src/services/data.js
L1/L1-p02-dom-helpers/src/ui/list.js
L1/L1-p02-dom-helpers/tests/jest/spec.jest.test.js
L1/L1-p02-dom-helpers/tests/vitest/spec.test.js
L1/L1-p02-dom-helpers/vitest.config.ts
L1/L1-p03-delegation-click/README.md
L1/L1-p03-delegation-click/babel.config.cjs
L1/L1-p03-delegation-click/jest.config.cjs
L1/L1-p03-delegation-click/package.json
L1/L1-p03-delegation-click/public/data/events.json
L1/L1-p03-delegation-click/public/index.html
L1/L1-p03-delegation-click/public/styles.css
L1/L1-p03-delegation-click/src/dom.js
L1/L1-p03-delegation-click/src/events.js
L1/L1-p03-delegation-click/src/filters.js
L1/L1-p03-delegation-click/src/loader.js
L1/L1-p03-delegation-click/src/main.js
L1/L1-p03-delegation-click/src/services/data.js
L1/L1-p03-delegation-click/src/ui/list.js
L1/L1-p03-delegation-click/tests/jest/spec.jest.test.js
L1/L1-p03-delegation-click/tests/vitest/spec.test.js
L1/L1-p03-delegation-click/vitest.config.ts
L1/L1-p04-once-passive-capture/README.md
L1/L1-p04-once-passive-capture/babel.config.cjs
L1/L1-p04-once-passive-capture/jest.config.cjs
L1/L1-p04-once-passive-capture/package.json
L1/L1-p04-once-passive-capture/public/data/events.json
L1/L1-p04-once-passive-capture/public/index.html
L1/L1-p04-once-passive-capture/public/styles.css
L1/L1-p04-once-passive-capture/src/dom.js
L1/L1-p04-once-passive-capture/src/events.js
L1/L1-p04-once-passive-capture/src/filters.js
L1/L1-p04-once-passive-capture/src/loader.js
L1/L1-p04-once-passive-capture/src/main.js
L1/L1-p04-once-passive-capture/src/services/data.js
L1/L1-p04-once-passive-capture/src/ui/list.js
L1/L1-p04-once-passive-capture/tests/jest/spec.jest.test.js
L1/L1-p04-once-passive-capture/tests/vitest/spec.test.js
L1/L1-p04-once-passive-capture/vitest.config.ts
L1/L1-p05-custom-event-basics/README.md
L1/L1-p05-custom-event-basics/babel.config.cjs
L1/L1-p05-custom-event-basics/jest.config.cjs
L1/L1-p05-custom-event-basics/package.json
L1/L1-p05-custom-event-basics/public/data/events.json
L1/L1-p05-custom-event-basics/public/index.html
L1/L1-p05-custom-event-basics/public/styles.css
L1/L1-p05-custom-event-basics/src/dom.js
L1/L1-p05-custom-event-basics/src/events.js
L1/L1-p05-custom-event-basics/src/filters.js
L1/L1-p05-custom-event-basics/src/loader.js
L1/L1-p05-custom-event-basics/src/main.js
L1/L1-p05-custom-event-basics/src/services/data.js
L1/L1-p05-custom-event-basics/src/ui/list.js
L1/L1-p05-custom-event-basics/tests/jest/spec.jest.test.js
L1/L1-p05-custom-event-basics/tests/vitest/spec.test.js
L1/L1-p05-custom-event-basics/vitest.config.ts
L1/L1-p06-template-clone/README.md
L1/L1-p06-template-clone/babel.config.cjs
L1/L1-p06-template-clone/jest.config.cjs
L1/L1-p06-template-clone/package.json
L1/L1-p06-template-clone/public/data/events.json
L1/L1-p06-template-clone/public/index.html
L1/L1-p06-template-clone/public/styles.css
L1/L1-p06-template-clone/src/dom.js
L1/L1-p06-template-clone/src/events.js
L1/L1-p06-template-clone/src/filters.js
L1/L1-p06-template-clone/src/loader.js
L1/L1-p06-template-clone/src/main.js
L1/L1-p06-template-clone/src/services/data.js
L1/L1-p06-template-clone/src/ui/list.js
L1/L1-p06-template-clone/tests/jest/spec.jest.test.js
L1/L1-p06-template-clone/tests/vitest/spec.test.js
L1/L1-p06-template-clone/vitest.config.ts
L1/L1-p07-fragment-render/README.md
L1/L1-p07-fragment-render/babel.config.cjs
L1/L1-p07-fragment-render/jest.config.cjs
L1/L1-p07-fragment-render/package.json
L1/L1-p07-fragment-render/public/data/events.json
L1/L1-p07-fragment-render/public/index.html
L1/L1-p07-fragment-render/public/styles.css
L1/L1-p07-fragment-render/src/dom.js
L1/L1-p07-fragment-render/src/events.js
L1/L1-p07-fragment-render/src/filters.js
L1/L1-p07-fragment-render/src/loader.js
L1/L1-p07-fragment-render/src/main.js
L1/L1-p07-fragment-render/src/services/data.js
L1/L1-p07-fragment-render/src/ui/list.js
L1/L1-p07-fragment-render/tests/jest/spec.jest.test.js
L1/L1-p07-fragment-render/tests/vitest/spec.test.js
L1/L1-p07-fragment-render/vitest.config.ts
L1/L1-p08-dataset-attrs/README.md
L1/L1-p08-dataset-attrs/babel.config.cjs
L1/L1-p08-dataset-attrs/jest.config.cjs
L1/L1-p08-dataset-attrs/package.json
L1/L1-p08-dataset-attrs/public/data/events.json
L1/L1-p08-dataset-attrs/public/index.html
L1/L1-p08-dataset-attrs/public/styles.css
L1/L1-p08-dataset-attrs/src/dom.js
L1/L1-p08-dataset-attrs/src/events.js
L1/L1-p08-dataset-attrs/src/filters.js
L1/L1-p08-dataset-attrs/src/loader.js
L1/L1-p08-dataset-attrs/src/main.js
L1/L1-p08-dataset-attrs/src/services/data.js
L1/L1-p08-dataset-attrs/src/ui/list.js
L1/L1-p08-dataset-attrs/tests/jest/spec.jest.test.js
L1/L1-p08-dataset-attrs/tests/vitest/spec.test.js
L1/L1-p08-dataset-attrs/vitest.config.ts
L1/L1-p09-class-toggle/README.md
L1/L1-p09-class-toggle/babel.config.cjs
L1/L1-p09-class-toggle/jest.config.cjs
L1/L1-p09-class-toggle/package.json
L1/L1-p09-class-toggle/public/data/events.json
L1/L1-p09-class-toggle/public/index.html
L1/L1-p09-class-toggle/public/styles.css
L1/L1-p09-class-toggle/src/dom.js
L1/L1-p09-class-toggle/src/events.js
L1/L1-p09-class-toggle/src/filters.js
L1/L1-p09-class-toggle/src/loader.js
L1/L1-p09-class-toggle/src/main.js
L1/L1-p09-class-toggle/src/services/data.js
L1/L1-p09-class-toggle/src/ui/list.js
L1/L1-p09-class-toggle/tests/jest/spec.jest.test.js
L1/L1-p09-class-toggle/tests/vitest/spec.test.js
L1/L1-p09-class-toggle/vitest.config.ts
L1/L1-p10-form-input-sync/README.md
L1/L1-p10-form-input-sync/babel.config.cjs
L1/L1-p10-form-input-sync/jest.config.cjs
L1/L1-p10-form-input-sync/package.json
L1/L1-p10-form-input-sync/public/data/events.json
L1/L1-p10-form-input-sync/public/index.html
L1/L1-p10-form-input-sync/public/styles.css
L1/L1-p10-form-input-sync/src/dom.js
L1/L1-p10-form-input-sync/src/events.js
L1/L1-p10-form-input-sync/src/filters.js
L1/L1-p10-form-input-sync/src/loader.js
L1/L1-p10-form-input-sync/src/main.js
L1/L1-p10-form-input-sync/src/services/data.js
L1/L1-p10-form-input-sync/src/ui/list.js
L1/L1-p10-form-input-sync/tests/jest/spec.jest.test.js
L1/L1-p10-form-input-sync/tests/vitest/spec.test.js
L1/L1-p10-form-input-sync/vitest.config.ts
L1/L1-p11-aria-live/README.md
L1/L1-p11-aria-live/babel.config.cjs
L1/L1-p11-aria-live/jest.config.cjs
L1/L1-p11-aria-live/package.json
L1/L1-p11-aria-live/public/data/events.json
L1/L1-p11-aria-live/public/index.html
L1/L1-p11-aria-live/public/styles.css
L1/L1-p11-aria-live/src/dom.js
L1/L1-p11-aria-live/src/events.js
L1/L1-p11-aria-live/src/filters.js
L1/L1-p11-aria-live/src/loader.js
L1/L1-p11-aria-live/src/main.js
L1/L1-p11-aria-live/src/services/data.js
L1/L1-p11-aria-live/src/ui/list.js
L1/L1-p11-aria-live/tests/jest/spec.jest.test.js
L1/L1-p11-aria-live/tests/vitest/spec.test.js
L1/L1-p11-aria-live/vitest.config.ts
L1/L1-p12-keyboard-events/README.md
L1/L1-p12-keyboard-events/babel.config.cjs
L1/L1-p12-keyboard-events/jest.config.cjs
L1/L1-p12-keyboard-events/package.json
L1/L1-p12-keyboard-events/public/data/events.json
L1/L1-p12-keyboard-events/public/index.html
L1/L1-p12-keyboard-events/public/styles.css
L1/L1-p12-keyboard-events/src/dom.js
L1/L1-p12-keyboard-events/src/events.js
L1/L1-p12-keyboard-events/src/filters.js
L1/L1-p12-keyboard-events/src/loader.js
L1/L1-p12-keyboard-events/src/main.js
L1/L1-p12-keyboard-events/src/services/data.js
L1/L1-p12-keyboard-events/src/ui/list.js
L1/L1-p12-keyboard-events/tests/jest/spec.jest.test.js
L1/L1-p12-keyboard-events/tests/vitest/spec.test.js
L1/L1-p12-keyboard-events/vitest.config.ts
L1/L1-p13-target-currentTarget/README.md
L1/L1-p13-target-currentTarget/babel.config.cjs
L1/L1-p13-target-currentTarget/jest.config.cjs
L1/L1-p13-target-currentTarget/package.json
L1/L1-p13-target-currentTarget/public/data/events.json
L1/L1-p13-target-currentTarget/public/index.html
L1/L1-p13-target-currentTarget/public/styles.css
L1/L1-p13-target-currentTarget/src/dom.js
L1/L1-p13-target-currentTarget/src/events.js
L1/L1-p13-target-currentTarget/src/filters.js
L1/L1-p13-target-currentTarget/src/loader.js
L1/L1-p13-target-currentTarget/src/main.js
L1/L1-p13-target-currentTarget/src/services/data.js
L1/L1-p13-target-currentTarget/src/ui/list.js
L1/L1-p13-target-currentTarget/tests/jest/spec.jest.test.js
L1/L1-p13-target-currentTarget/tests/vitest/spec.test.js
L1/L1-p13-target-currentTarget/vitest.config.ts
L1/L1-p14-cleanup-abort/README.md
L1/L1-p14-cleanup-abort/babel.config.cjs
L1/L1-p14-cleanup-abort/jest.config.cjs
L1/L1-p14-cleanup-abort/package.json
L1/L1-p14-cleanup-abort/public/data/events.json
L1/L1-p14-cleanup-abort/public/index.html
L1/L1-p14-cleanup-abort/public/styles.css
L1/L1-p14-cleanup-abort/src/dom.js
L1/L1-p14-cleanup-abort/src/events.js
L1/L1-p14-cleanup-abort/src/filters.js
L1/L1-p14-cleanup-abort/src/loader.js
L1/L1-p14-cleanup-abort/src/main.js
L1/L1-p14-cleanup-abort/src/services/data.js
L1/L1-p14-cleanup-abort/src/ui/list.js
L1/L1-p14-cleanup-abort/tests/jest/spec.jest.test.js
L1/L1-p14-cleanup-abort/tests/vitest/spec.test.js
L1/L1-p14-cleanup-abort/vitest.config.ts
L1/L1-p15-module-boundary/README.md
L1/L1-p15-module-boundary/babel.config.cjs
L1/L1-p15-module-boundary/jest.config.cjs
L1/L1-p15-module-boundary/package.json
L1/L1-p15-module-boundary/public/data/events.json
L1/L1-p15-module-boundary/public/index.html
L1/L1-p15-module-boundary/public/styles.css
L1/L1-p15-module-boundary/src/dom.js
L1/L1-p15-module-boundary/src/events.js
L1/L1-p15-module-boundary/src/filters.js
L1/L1-p15-module-boundary/src/loader.js
L1/L1-p15-module-boundary/src/main.js
L1/L1-p15-module-boundary/src/services/data.js
L1/L1-p15-module-boundary/src/ui/list.js
L1/L1-p15-module-boundary/tests/jest/spec.jest.test.js
L1/L1-p15-module-boundary/tests/vitest/spec.test.js
L1/L1-p15-module-boundary/vitest.config.ts
L2/L2-p01-import-maps/README.md
L2/L2-p01-import-maps/babel.config.cjs
L2/L2-p01-import-maps/jest.config.cjs
L2/L2-p01-import-maps/package.json
L2/L2-p01-import-maps/public/data/events.json
L2/L2-p01-import-maps/public/index.html
L2/L2-p01-import-maps/public/styles.css
L2/L2-p01-import-maps/src/dom.js
L2/L2-p01-import-maps/src/events.js
L2/L2-p01-import-maps/src/filters.js
L2/L2-p01-import-maps/src/loader.js
L2/L2-p01-import-maps/src/main.js
L2/L2-p01-import-maps/src/services/data.js
L2/L2-p01-import-maps/src/ui/list.js
L2/L2-p01-import-maps/tests/jest/spec.jest.test.js
L2/L2-p01-import-maps/tests/vitest/spec.test.js
L2/L2-p01-import-maps/vitest.config.ts
L2/L2-p02-services-json/README.md
L2/L2-p02-services-json/babel.config.cjs
L2/L2-p02-services-json/jest.config.cjs
L2/L2-p02-services-json/package.json
L2/L2-p02-services-json/public/data/events.json
L2/L2-p02-services-json/public/index.html
L2/L2-p02-services-json/public/styles.css
L2/L2-p02-services-json/src/dom.js
L2/L2-p02-services-json/src/events.js
L2/L2-p02-services-json/src/filters.js
L2/L2-p02-services-json/src/loader.js
L2/L2-p02-services-json/src/main.js
L2/L2-p02-services-json/src/services/data.js
L2/L2-p02-services-json/src/ui/list.js
L2/L2-p02-services-json/tests/jest/spec.jest.test.js
L2/L2-p02-services-json/tests/vitest/spec.test.js
L2/L2-p02-services-json/vitest.config.ts
L2/L2-p03-dynamic-import/README.md
L2/L2-p03-dynamic-import/babel.config.cjs
L2/L2-p03-dynamic-import/jest.config.cjs
L2/L2-p03-dynamic-import/package.json
L2/L2-p03-dynamic-import/public/data/events.json
L2/L2-p03-dynamic-import/public/index.html
L2/L2-p03-dynamic-import/public/styles.css
L2/L2-p03-dynamic-import/src/dom.js
L2/L2-p03-dynamic-import/src/events.js
L2/L2-p03-dynamic-import/src/filters.js
L2/L2-p03-dynamic-import/src/loader.js
L2/L2-p03-dynamic-import/src/main.js
L2/L2-p03-dynamic-import/src/services/data.js
L2/L2-p03-dynamic-import/src/ui/list.js
L2/L2-p03-dynamic-import/tests/jest/spec.jest.test.js
L2/L2-p03-dynamic-import/tests/vitest/spec.test.js
L2/L2-p03-dynamic-import/vitest.config.ts
L2/L2-p04-reexports/README.md
L2/L2-p04-reexports/babel.config.cjs
L2/L2-p04-reexports/jest.config.cjs
L2/L2-p04-reexports/package.json
L2/L2-p04-reexports/public/data/events.json
L2/L2-p04-reexports/public/index.html
L2/L2-p04-reexports/public/styles.css
L2/L2-p04-reexports/src/dom.js
L2/L2-p04-reexports/src/events.js
L2/L2-p04-reexports/src/filters.js
L2/L2-p04-reexports/src/loader.js
L2/L2-p04-reexports/src/main.js
L2/L2-p04-reexports/src/services/data.js
L2/L2-p04-reexports/src/ui/list.js
L2/L2-p04-reexports/tests/jest/spec.jest.test.js
L2/L2-p04-reexports/tests/vitest/spec.test.js
L2/L2-p04-reexports/vitest.config.ts
L2/L2-p05-tree-shaking/README.md
L2/L2-p05-tree-shaking/babel.config.cjs
L2/L2-p05-tree-shaking/jest.config.cjs
L2/L2-p05-tree-shaking/package.json
L2/L2-p05-tree-shaking/public/data/events.json
L2/L2-p05-tree-shaking/public/index.html
L2/L2-p05-tree-shaking/public/styles.css
L2/L2-p05-tree-shaking/src/dom.js
L2/L2-p05-tree-shaking/src/events.js
L2/L2-p05-tree-shaking/src/filters.js
L2/L2-p05-tree-shaking/src/loader.js
L2/L2-p05-tree-shaking/src/main.js
L2/L2-p05-tree-shaking/src/services/data.js
L2/L2-p05-tree-shaking/src/ui/list.js
L2/L2-p05-tree-shaking/tests/jest/spec.jest.test.js
L2/L2-p05-tree-shaking/tests/vitest/spec.test.js
L2/L2-p05-tree-shaking/vitest.config.ts
L2/L2-p06-code-splitting/README.md
L2/L2-p06-code-splitting/babel.config.cjs
L2/L2-p06-code-splitting/jest.config.cjs
L2/L2-p06-code-splitting/package.json
L2/L2-p06-code-splitting/public/data/events.json
L2/L2-p06-code-splitting/public/index.html
L2/L2-p06-code-splitting/public/styles.css
L2/L2-p06-code-splitting/src/dom.js
L2/L2-p06-code-splitting/src/events.js
L2/L2-p06-code-splitting/src/filters.js
L2/L2-p06-code-splitting/src/loader.js
L2/L2-p06-code-splitting/src/main.js
L2/L2-p06-code-splitting/src/secondary.js
L2/L2-p06-code-splitting/src/services/data.js
L2/L2-p06-code-splitting/src/ui/list.js
L2/L2-p06-code-splitting/tests/jest/spec.jest.test.js
L2/L2-p06-code-splitting/tests/vitest/spec.test.js
L2/L2-p06-code-splitting/vitest.config.ts
L2/L2-p07-modulepreload-metrics/README.md
L2/L2-p07-modulepreload-metrics/babel.config.cjs
L2/L2-p07-modulepreload-metrics/jest.config.cjs
L2/L2-p07-modulepreload-metrics/package.json
L2/L2-p07-modulepreload-metrics/public/data/events.json
L2/L2-p07-modulepreload-metrics/public/index.html
L2/L2-p07-modulepreload-metrics/public/styles.css
L2/L2-p07-modulepreload-metrics/src/dom.js
L2/L2-p07-modulepreload-metrics/src/events.js
L2/L2-p07-modulepreload-metrics/src/filters.js
L2/L2-p07-modulepreload-metrics/src/loader.js
L2/L2-p07-modulepreload-metrics/src/main.js
L2/L2-p07-modulepreload-metrics/src/services/data.js
L2/L2-p07-modulepreload-metrics/src/ui/list.js
L2/L2-p07-modulepreload-metrics/tests/jest/spec.jest.test.js
L2/L2-p07-modulepreload-metrics/tests/vitest/spec.test.js
L2/L2-p07-modulepreload-metrics/vitest.config.ts
L2/L2-p08-csp-scan/README.md
L2/L2-p08-csp-scan/babel.config.cjs
L2/L2-p08-csp-scan/jest.config.cjs
L2/L2-p08-csp-scan/package.json
L2/L2-p08-csp-scan/public/data/events.json
L2/L2-p08-csp-scan/public/index.html
L2/L2-p08-csp-scan/public/styles.css
L2/L2-p08-csp-scan/src/dom.js
L2/L2-p08-csp-scan/src/events.js
L2/L2-p08-csp-scan/src/filters.js
L2/L2-p08-csp-scan/src/loader.js
L2/L2-p08-csp-scan/src/main.js
L2/L2-p08-csp-scan/src/services/data.js
L2/L2-p08-csp-scan/src/ui/list.js
L2/L2-p08-csp-scan/tests/jest/spec.jest.test.js
L2/L2-p08-csp-scan/tests/vitest/spec.test.js
L2/L2-p08-csp-scan/vitest.config.ts
L2/L2-p09-adapter/README.md
L2/L2-p09-adapter/babel.config.cjs
L2/L2-p09-adapter/jest.config.cjs
L2/L2-p09-adapter/package.json
L2/L2-p09-adapter/public/data/events.json
L2/L2-p09-adapter/public/index.html
L2/L2-p09-adapter/public/styles.css
L2/L2-p09-adapter/src/dom.js
L2/L2-p09-adapter/src/events.js
L2/L2-p09-adapter/src/filters.js
L2/L2-p09-adapter/src/loader.js
L2/L2-p09-adapter/src/main.js
L2/L2-p09-adapter/src/services/data.js
L2/L2-p09-adapter/src/ui/list.js
L2/L2-p09-adapter/tests/jest/spec.jest.test.js
L2/L2-p09-adapter/tests/vitest/spec.test.js
L2/L2-p09-adapter/vitest.config.ts
L2/L2-p10-mutation-observer/README.md
L2/L2-p10-mutation-observer/babel.config.cjs
L2/L2-p10-mutation-observer/jest.config.cjs
L2/L2-p10-mutation-observer/package.json
L2/L2-p10-mutation-observer/public/data/events.json
L2/L2-p10-mutation-observer/public/index.html
L2/L2-p10-mutation-observer/public/styles.css
L2/L2-p10-mutation-observer/src/dom.js
L2/L2-p10-mutation-observer/src/events.js
L2/L2-p10-mutation-observer/src/filters.js
L2/L2-p10-mutation-observer/src/loader.js
L2/L2-p10-mutation-observer/src/main.js
L2/L2-p10-mutation-observer/src/mut.js
L2/L2-p10-mutation-observer/src/services/data.js
L2/L2-p10-mutation-observer/src/ui/list.js
L2/L2-p10-mutation-observer/tests/jest/spec.jest.test.js
L2/L2-p10-mutation-observer/tests/vitest/spec.test.js
L2/L2-p10-mutation-observer/vitest.config.ts
L2/L2-p11-throttle-input/README.md
L2/L2-p11-throttle-input/babel.config.cjs
L2/L2-p11-throttle-input/jest.config.cjs
L2/L2-p11-throttle-input/package.json
L2/L2-p11-throttle-input/public/data/events.json
L2/L2-p11-throttle-input/public/index.html
L2/L2-p11-throttle-input/public/styles.css
L2/L2-p11-throttle-input/src/dom.js
L2/L2-p11-throttle-input/src/events.js
L2/L2-p11-throttle-input/src/filters.js
L2/L2-p11-throttle-input/src/loader.js
L2/L2-p11-throttle-input/src/main.js
L2/L2-p11-throttle-input/src/services/data.js
L2/L2-p11-throttle-input/src/throttle.js
L2/L2-p11-throttle-input/src/ui/list.js
L2/L2-p11-throttle-input/tests/jest/spec.jest.test.js
L2/L2-p11-throttle-input/tests/vitest/spec.test.js
L2/L2-p11-throttle-input/vitest.config.ts
L2/L2-p12-event-guards/README.md
L2/L2-p12-event-guards/babel.config.cjs
L2/L2-p12-event-guards/jest.config.cjs
L2/L2-p12-event-guards/package.json
L2/L2-p12-event-guards/public/data/events.json
L2/L2-p12-event-guards/public/index.html
L2/L2-p12-event-guards/public/styles.css
L2/L2-p12-event-guards/src/dom.js
L2/L2-p12-event-guards/src/events.js
L2/L2-p12-event-guards/src/filters.js
L2/L2-p12-event-guards/src/loader.js
L2/L2-p12-event-guards/src/main.js
L2/L2-p12-event-guards/src/services/data.js
L2/L2-p12-event-guards/src/ui/list.js
L2/L2-p12-event-guards/tests/jest/spec.jest.test.js
L2/L2-p12-event-guards/tests/vitest/spec.test.js
L2/L2-p12-event-guards/vitest.config.ts
L2/L2-p13-import-conditions-doc/README.md
L2/L2-p13-import-conditions-doc/babel.config.cjs
L2/L2-p13-import-conditions-doc/jest.config.cjs
L2/L2-p13-import-conditions-doc/package.json
L2/L2-p13-import-conditions-doc/public/data/events.json
L2/L2-p13-import-conditions-doc/public/index.html
L2/L2-p13-import-conditions-doc/public/styles.css
L2/L2-p13-import-conditions-doc/src/dom.js
L2/L2-p13-import-conditions-doc/src/events.js
L2/L2-p13-import-conditions-doc/src/filters.js
L2/L2-p13-import-conditions-doc/src/loader.js
L2/L2-p13-import-conditions-doc/src/main.js
L2/L2-p13-import-conditions-doc/src/services/data.js
L2/L2-p13-import-conditions-doc/src/ui/list.js
L2/L2-p13-import-conditions-doc/tests/jest/spec.jest.test.js
L2/L2-p13-import-conditions-doc/tests/vitest/spec.test.js
L2/L2-p13-import-conditions-doc/vitest.config.ts
L2/L2-p14-subpath-exports-doc/README.md
L2/L2-p14-subpath-exports-doc/babel.config.cjs
L2/L2-p14-subpath-exports-doc/jest.config.cjs
L2/L2-p14-subpath-exports-doc/package.json
L2/L2-p14-subpath-exports-doc/public/data/events.json
L2/L2-p14-subpath-exports-doc/public/index.html
L2/L2-p14-subpath-exports-doc/public/styles.css
L2/L2-p14-subpath-exports-doc/src/dom.js
L2/L2-p14-subpath-exports-doc/src/events.js
L2/L2-p14-subpath-exports-doc/src/filters.js
L2/L2-p14-subpath-exports-doc/src/loader.js
L2/L2-p14-subpath-exports-doc/src/main.js
L2/L2-p14-subpath-exports-doc/src/services/data.js
L2/L2-p14-subpath-exports-doc/src/ui/list.js
L2/L2-p14-subpath-exports-doc/tests/jest/spec.jest.test.js
L2/L2-p14-subpath-exports-doc/tests/vitest/spec.test.js
L2/L2-p14-subpath-exports-doc/vitest.config.ts
L2/L2-p15-esm-cjs-interop-doc/README.md
L2/L2-p15-esm-cjs-interop-doc/babel.config.cjs
L2/L2-p15-esm-cjs-interop-doc/jest.config.cjs
L2/L2-p15-esm-cjs-interop-doc/package.json
L2/L2-p15-esm-cjs-interop-doc/public/data/events.json
L2/L2-p15-esm-cjs-interop-doc/public/index.html
L2/L2-p15-esm-cjs-interop-doc/public/styles.css
L2/L2-p15-esm-cjs-interop-doc/src/dom.js
L2/L2-p15-esm-cjs-interop-doc/src/events.js
L2/L2-p15-esm-cjs-interop-doc/src/filters.js
L2/L2-p15-esm-cjs-interop-doc/src/loader.js
L2/L2-p15-esm-cjs-interop-doc/src/main.js
L2/L2-p15-esm-cjs-interop-doc/src/services/data.js
L2/L2-p15-esm-cjs-interop-doc/src/ui/list.js
L2/L2-p15-esm-cjs-interop-doc/tests/jest/spec.jest.test.js
L2/L2-p15-esm-cjs-interop-doc/tests/vitest/spec.test.js
L2/L2-p15-esm-cjs-interop-doc/vitest.config.ts
L3/L3-p01-bus-namespaced/README.md
L3/L3-p01-bus-namespaced/babel.config.cjs
L3/L3-p01-bus-namespaced/jest.config.cjs
L3/L3-p01-bus-namespaced/package.json
L3/L3-p01-bus-namespaced/public/data/events.json
L3/L3-p01-bus-namespaced/public/index.html
L3/L3-p01-bus-namespaced/public/styles.css
L3/L3-p01-bus-namespaced/src/dom.js
L3/L3-p01-bus-namespaced/src/events.js
L3/L3-p01-bus-namespaced/src/filters.js
L3/L3-p01-bus-namespaced/src/loader.js
L3/L3-p01-bus-namespaced/src/main.js
L3/L3-p01-bus-namespaced/src/services/data.js
L3/L3-p01-bus-namespaced/src/ui/list.js
L3/L3-p01-bus-namespaced/tests/jest/spec.jest.test.js
L3/L3-p01-bus-namespaced/tests/vitest/spec.test.js
L3/L3-p01-bus-namespaced/vitest.config.ts
L3/L3-p02-timeout-signal/README.md
L3/L3-p02-timeout-signal/babel.config.cjs
L3/L3-p02-timeout-signal/jest.config.cjs
L3/L3-p02-timeout-signal/package.json
L3/L3-p02-timeout-signal/public/data/events.json
L3/L3-p02-timeout-signal/public/index.html
L3/L3-p02-timeout-signal/public/styles.css
L3/L3-p02-timeout-signal/src/dom.js
L3/L3-p02-timeout-signal/src/events.js
L3/L3-p02-timeout-signal/src/filters.js
L3/L3-p02-timeout-signal/src/loader.js
L3/L3-p02-timeout-signal/src/main.js
L3/L3-p02-timeout-signal/src/services/data.js
L3/L3-p02-timeout-signal/src/timeout.js
L3/L3-p02-timeout-signal/src/ui/list.js
L3/L3-p02-timeout-signal/tests/jest/spec.jest.test.js
L3/L3-p02-timeout-signal/tests/vitest/spec.test.js
L3/L3-p02-timeout-signal/vitest.config.ts
L3/L3-p03-intersection-observer/README.md
L3/L3-p03-intersection-observer/babel.config.cjs
L3/L3-p03-intersection-observer/jest.config.cjs
L3/L3-p03-intersection-observer/package.json
L3/L3-p03-intersection-observer/public/data/events.json
L3/L3-p03-intersection-observer/public/index.html
L3/L3-p03-intersection-observer/public/styles.css
L3/L3-p03-intersection-observer/src/dom.js
L3/L3-p03-intersection-observer/src/events.js
L3/L3-p03-intersection-observer/src/filters.js
L3/L3-p03-intersection-observer/src/lazy.js
L3/L3-p03-intersection-observer/src/loader.js
L3/L3-p03-intersection-observer/src/main.js
L3/L3-p03-intersection-observer/src/services/data.js
L3/L3-p03-intersection-observer/src/ui/list.js
L3/L3-p03-intersection-observer/tests/jest/spec.jest.test.js
L3/L3-p03-intersection-observer/tests/vitest/spec.test.js
L3/L3-p03-intersection-observer/vitest.config.ts
L3/L3-p04-mutation-raf-batch/README.md
L3/L3-p04-mutation-raf-batch/babel.config.cjs
L3/L3-p04-mutation-raf-batch/jest.config.cjs
L3/L3-p04-mutation-raf-batch/package.json
L3/L3-p04-mutation-raf-batch/public/data/events.json
L3/L3-p04-mutation-raf-batch/public/index.html
L3/L3-p04-mutation-raf-batch/public/styles.css
L3/L3-p04-mutation-raf-batch/src/dom.js
L3/L3-p04-mutation-raf-batch/src/events.js
L3/L3-p04-mutation-raf-batch/src/filters.js
L3/L3-p04-mutation-raf-batch/src/loader.js
L3/L3-p04-mutation-raf-batch/src/main.js
L3/L3-p04-mutation-raf-batch/src/services/data.js
L3/L3-p04-mutation-raf-batch/src/ui/list.js
L3/L3-p04-mutation-raf-batch/tests/jest/spec.jest.test.js
L3/L3-p04-mutation-raf-batch/tests/vitest/spec.test.js
L3/L3-p04-mutation-raf-batch/vitest.config.ts
L3/L3-p05-composed-events/README.md
L3/L3-p05-composed-events/babel.config.cjs
L3/L3-p05-composed-events/jest.config.cjs
L3/L3-p05-composed-events/package.json
L3/L3-p05-composed-events/public/data/events.json
L3/L3-p05-composed-events/public/index.html
L3/L3-p05-composed-events/public/styles.css
L3/L3-p05-composed-events/src/dom.js
L3/L3-p05-composed-events/src/events.js
L3/L3-p05-composed-events/src/filters.js
L3/L3-p05-composed-events/src/loader.js
L3/L3-p05-composed-events/src/main.js
L3/L3-p05-composed-events/src/services/data.js
L3/L3-p05-composed-events/src/ui/list.js
L3/L3-p05-composed-events/tests/jest/spec.jest.test.js
L3/L3-p05-composed-events/tests/vitest/spec.test.js
L3/L3-p05-composed-events/vitest.config.ts
L3/L3-p06-event-replay/README.md
L3/L3-p06-event-replay/babel.config.cjs
L3/L3-p06-event-replay/jest.config.cjs
L3/L3-p06-event-replay/package.json
L3/L3-p06-event-replay/public/data/events.json
L3/L3-p06-event-replay/public/index.html
L3/L3-p06-event-replay/public/styles.css
L3/L3-p06-event-replay/src/dom.js
L3/L3-p06-event-replay/src/events.js
L3/L3-p06-event-replay/src/filters.js
L3/L3-p06-event-replay/src/loader.js
L3/L3-p06-event-replay/src/main.js
L3/L3-p06-event-replay/src/replay.js
L3/L3-p06-event-replay/src/services/data.js
L3/L3-p06-event-replay/src/ui/list.js
L3/L3-p06-event-replay/tests/jest/spec.jest.test.js
L3/L3-p06-event-replay/tests/vitest/spec.test.js
L3/L3-p06-event-replay/vitest.config.ts
L3/L3-p07-e2e-filter/README.md
L3/L3-p07-e2e-filter/babel.config.cjs
L3/L3-p07-e2e-filter/jest.config.cjs
L3/L3-p07-e2e-filter/package.json
L3/L3-p07-e2e-filter/playwright.config.ts
L3/L3-p07-e2e-filter/public/data/events.json
L3/L3-p07-e2e-filter/public/index.html
L3/L3-p07-e2e-filter/public/styles.css
L3/L3-p07-e2e-filter/src/dom.js
L3/L3-p07-e2e-filter/src/events.js
L3/L3-p07-e2e-filter/src/filters.js
L3/L3-p07-e2e-filter/src/loader.js
L3/L3-p07-e2e-filter/src/main.js
L3/L3-p07-e2e-filter/src/services/data.js
L3/L3-p07-e2e-filter/src/ui/list.js
L3/L3-p07-e2e-filter/tests/e2e.spec.ts
L3/L3-p07-e2e-filter/tests/jest/spec.jest.test.js
L3/L3-p07-e2e-filter/tests/vitest/spec.test.js
L3/L3-p07-e2e-filter/vitest.config.ts
L3/L3-p08-e2e-keyboard/README.md
L3/L3-p08-e2e-keyboard/babel.config.cjs
L3/L3-p08-e2e-keyboard/jest.config.cjs
L3/L3-p08-e2e-keyboard/package.json
L3/L3-p08-e2e-keyboard/playwright.config.ts
L3/L3-p08-e2e-keyboard/public/data/events.json
L3/L3-p08-e2e-keyboard/public/index.html
L3/L3-p08-e2e-keyboard/public/styles.css
L3/L3-p08-e2e-keyboard/src/dom.js
L3/L3-p08-e2e-keyboard/src/events.js
L3/L3-p08-e2e-keyboard/src/filters.js
L3/L3-p08-e2e-keyboard/src/loader.js
L3/L3-p08-e2e-keyboard/src/main.js
L3/L3-p08-e2e-keyboard/src/services/data.js
L3/L3-p08-e2e-keyboard/src/ui/list.js
L3/L3-p08-e2e-keyboard/tests/e2e.spec.ts
L3/L3-p08-e2e-keyboard/tests/jest/spec.jest.test.js
L3/L3-p08-e2e-keyboard/tests/vitest/spec.test.js
L3/L3-p08-e2e-keyboard/vitest.config.ts
L3/L3-p09-pwa-workbox/README.md
L3/L3-p09-pwa-workbox/babel.config.cjs
L3/L3-p09-pwa-workbox/build-sw.mjs
L3/L3-p09-pwa-workbox/jest.config.cjs
L3/L3-p09-pwa-workbox/package.json
L3/L3-p09-pwa-workbox/public/data/events.json
L3/L3-p09-pwa-workbox/public/index.html
L3/L3-p09-pwa-workbox/public/styles.css
L3/L3-p09-pwa-workbox/src/dom.js
L3/L3-p09-pwa-workbox/src/events.js
L3/L3-p09-pwa-workbox/src/filters.js
L3/L3-p09-pwa-workbox/src/loader.js
L3/L3-p09-pwa-workbox/src/main.js
L3/L3-p09-pwa-workbox/src/services/data.js
L3/L3-p09-pwa-workbox/src/ui/list.js
L3/L3-p09-pwa-workbox/tests/jest/spec.jest.test.js
L3/L3-p09-pwa-workbox/tests/jest/workbox.jest.test.js
L3/L3-p09-pwa-workbox/tests/vitest/spec.test.js
L3/L3-p09-pwa-workbox/tests/vitest/workbox.test.js
L3/L3-p09-pwa-workbox/vitest.config.ts
L3/L3-p10-e2e-offline-smoke/README.md
L3/L3-p10-e2e-offline-smoke/babel.config.cjs
L3/L3-p10-e2e-offline-smoke/jest.config.cjs
L3/L3-p10-e2e-offline-smoke/package.json
L3/L3-p10-e2e-offline-smoke/playwright.config.ts
L3/L3-p10-e2e-offline-smoke/public/data/events.json
L3/L3-p10-e2e-offline-smoke/public/index.html
L3/L3-p10-e2e-offline-smoke/public/styles.css
L3/L3-p10-e2e-offline-smoke/src/dom.js
L3/L3-p10-e2e-offline-smoke/src/events.js
L3/L3-p10-e2e-offline-smoke/src/filters.js
L3/L3-p10-e2e-offline-smoke/src/loader.js
L3/L3-p10-e2e-offline-smoke/src/main.js
L3/L3-p10-e2e-offline-smoke/src/services/data.js
L3/L3-p10-e2e-offline-smoke/src/ui/list.js
L3/L3-p10-e2e-offline-smoke/tests/e2e.spec.ts
L3/L3-p10-e2e-offline-smoke/tests/jest/spec.jest.test.js
L3/L3-p10-e2e-offline-smoke/tests/vitest/spec.test.js
L3/L3-p10-e2e-offline-smoke/vitest.config.ts
L3/L3-p11-module-graph/README.md
L3/L3-p11-module-graph/babel.config.cjs
L3/L3-p11-module-graph/jest.config.cjs
L3/L3-p11-module-graph/package.json
L3/L3-p11-module-graph/public/data/events.json
L3/L3-p11-module-graph/public/index.html
L3/L3-p11-module-graph/public/styles.css
L3/L3-p11-module-graph/scripts/graph.mjs
L3/L3-p11-module-graph/src/dom.js
L3/L3-p11-module-graph/src/events.js
L3/L3-p11-module-graph/src/filters.js
L3/L3-p11-module-graph/src/loader.js
L3/L3-p11-module-graph/src/main.js
L3/L3-p11-module-graph/src/services/data.js
L3/L3-p11-module-graph/src/ui/list.js
L3/L3-p11-module-graph/tests/jest/spec.jest.test.js
L3/L3-p11-module-graph/tests/vitest/spec.test.js
L3/L3-p11-module-graph/vitest.config.ts
L3/L3-p12-feature-toggles/README.md
L3/L3-p12-feature-toggles/babel.config.cjs
L3/L3-p12-feature-toggles/jest.config.cjs
L3/L3-p12-feature-toggles/package.json
L3/L3-p12-feature-toggles/public/data/events.json
L3/L3-p12-feature-toggles/public/index.html
L3/L3-p12-feature-toggles/public/styles.css
L3/L3-p12-feature-toggles/src/advanced.js
L3/L3-p12-feature-toggles/src/dom.js
L3/L3-p12-feature-toggles/src/events.js
L3/L3-p12-feature-toggles/src/filters.js
L3/L3-p12-feature-toggles/src/loader.js
L3/L3-p12-feature-toggles/src/main.js
L3/L3-p12-feature-toggles/src/services/data.js
L3/L3-p12-feature-toggles/src/toggles.js
L3/L3-p12-feature-toggles/src/ui/list.js
L3/L3-p12-feature-toggles/tests/jest/spec.jest.test.js
L3/L3-p12-feature-toggles/tests/vitest/spec.test.js
L3/L3-p12-feature-toggles/vitest.config.ts
L3/L3-p13-microfrontend-bridge/README.md
L3/L3-p13-microfrontend-bridge/babel.config.cjs
L3/L3-p13-microfrontend-bridge/jest.config.cjs
L3/L3-p13-microfrontend-bridge/package.json
L3/L3-p13-microfrontend-bridge/public/data/events.json
L3/L3-p13-microfrontend-bridge/public/index.html
L3/L3-p13-microfrontend-bridge/public/styles.css
L3/L3-p13-microfrontend-bridge/src/dom.js
L3/L3-p13-microfrontend-bridge/src/events.js
L3/L3-p13-microfrontend-bridge/src/filters.js
L3/L3-p13-microfrontend-bridge/src/loader.js
L3/L3-p13-microfrontend-bridge/src/main.js
L3/L3-p13-microfrontend-bridge/src/services/data.js
L3/L3-p13-microfrontend-bridge/src/ui/list.js
L3/L3-p13-microfrontend-bridge/tests/jest/spec.jest.test.js
L3/L3-p13-microfrontend-bridge/tests/vitest/spec.test.js
L3/L3-p13-microfrontend-bridge/vitest.config.ts
L3/L3-p14-perf-budget/README.md
L3/L3-p14-perf-budget/babel.config.cjs
L3/L3-p14-perf-budget/jest.config.cjs
L3/L3-p14-perf-budget/package.json
L3/L3-p14-perf-budget/public/data/events.json
L3/L3-p14-perf-budget/public/index.html
L3/L3-p14-perf-budget/public/styles.css
L3/L3-p14-perf-budget/src/dom.js
L3/L3-p14-perf-budget/src/events.js
L3/L3-p14-perf-budget/src/filters.js
L3/L3-p14-perf-budget/src/loader.js
L3/L3-p14-perf-budget/src/main.js
L3/L3-p14-perf-budget/src/services/data.js
L3/L3-p14-perf-budget/src/ui/list.js
L3/L3-p14-perf-budget/tests/jest/spec.jest.test.js
L3/L3-p14-perf-budget/tests/vitest/spec.test.js
L3/L3-p14-perf-budget/vitest.config.ts
L3/L3-p15-ci-matrix/README.md
L3/L3-p15-ci-matrix/babel.config.cjs
L3/L3-p15-ci-matrix/jest.config.cjs
L3/L3-p15-ci-matrix/package.json
L3/L3-p15-ci-matrix/public/data/events.json
L3/L3-p15-ci-matrix/public/index.html
L3/L3-p15-ci-matrix/public/styles.css
L3/L3-p15-ci-matrix/src/dom.js
L3/L3-p15-ci-matrix/src/events.js
L3/L3-p15-ci-matrix/src/filters.js
L3/L3-p15-ci-matrix/src/loader.js
L3/L3-p15-ci-matrix/src/main.js
L3/L3-p15-ci-matrix/src/services/data.js
L3/L3-p15-ci-matrix/src/ui/list.js
L3/L3-p15-ci-matrix/tests/jest/spec.jest.test.js
L3/L3-p15-ci-matrix/tests/vitest/spec.test.js
L3/L3-p15-ci-matrix/vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 184, docs: 44, public: 135, code: 323, tests: 95, pwa: 1, other: 1.

**package.json — sinteză (scripturi, workspaces, dependențe — eșantion)**

- `L1/L1-p01-esm-bootstrap/package.json`: name=`L1-p01-esm-bootstrap` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p02-dom-helpers/package.json`: name=`L1-p02-dom-helpers` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p03-delegation-click/package.json`: name=`L1-p03-delegation-click` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p04-once-passive-capture/package.json`: name=`L1-p04-once-passive-capture` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p05-custom-event-basics/package.json`: name=`L1-p05-custom-event-basics` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p06-template-clone/package.json`: name=`L1-p06-template-clone` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p07-fragment-render/package.json`: name=`L1-p07-fragment-render` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p08-dataset-attrs/package.json`: name=`L1-p08-dataset-attrs` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p09-class-toggle/package.json`: name=`L1-p09-class-toggle` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p10-form-input-sync/package.json`: name=`L1-p10-form-input-sync` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p11-aria-live/package.json`: name=`L1-p11-aria-live` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p12-keyboard-events/package.json`: name=`L1-p12-keyboard-events` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p13-target-currentTarget/package.json`: name=`L1-p13-target-currentTarget` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p14-cleanup-abort/package.json`: name=`L1-p14-cleanup-abort` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L1/L1-p15-module-boundary/package.json`: name=`L1-p15-module-boundary` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p01-import-maps/package.json`: name=`L2-p01-import-maps` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p02-services-json/package.json`: name=`L2-p02-services-json` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p03-dynamic-import/package.json`: name=`L2-p03-dynamic-import` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p04-reexports/package.json`: name=`L2-p04-reexports` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p05-tree-shaking/package.json`: name=`L2-p05-tree-shaking` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p06-code-splitting/package.json`: name=`L2-p06-code-splitting` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p07-modulepreload-metrics/package.json`: name=`L2-p07-modulepreload-metrics` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p08-csp-scan/package.json`: name=`L2-p08-csp-scan` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p09-adapter/package.json`: name=`L2-p09-adapter` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p10-mutation-observer/package.json`: name=`L2-p10-mutation-observer` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p11-throttle-input/package.json`: name=`L2-p11-throttle-input` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p12-event-guards/package.json`: name=`L2-p12-event-guards` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p13-import-conditions-doc/package.json`: name=`L2-p13-import-conditions-doc` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p14-subpath-exports-doc/package.json`: name=`L2-p14-subpath-exports-doc` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L2/L2-p15-esm-cjs-interop-doc/package.json`: name=`L2-p15-esm-cjs-interop-doc` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L3/L3-p01-bus-namespaced/package.json`: name=`L3-p01-bus-namespaced` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L3/L3-p02-timeout-signal/package.json`: name=`L3-p02-timeout-signal` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L3/L3-p03-intersection-observer/package.json`: name=`L3-p03-intersection-observer` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L3/L3-p04-mutation-raf-batch/package.json`: name=`L3-p04-mutation-raf-batch` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L3/L3-p05-composed-events/package.json`: name=`L3-p05-composed-events` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L3/L3-p06-event-replay/package.json`: name=`L3-p06-event-replay` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L3/L3-p07-e2e-filter/package.json`: name=`L3-p07-e2e-filter` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `test:e2e` → `playwright test`
  - `serve:e2e` → `http-server -p 4173 .`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server, playwright
- `L3/L3-p08-e2e-keyboard/package.json`: name=`L3-p08-e2e-keyboard` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `test:e2e` → `playwright test`
  - `serve:e2e` → `http-server -p 4173 .`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server, playwright
- `L3/L3-p09-pwa-workbox/package.json`: name=`L3-p09-pwa-workbox` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `build:sw` → `node build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server, workbox-build
- `L3/L3-p10-e2e-offline-smoke/package.json`: name=`L3-p10-e2e-offline-smoke` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `test:e2e` → `playwright test`
  - `serve:e2e` → `http-server -p 4173 .`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server, playwright
- `L3/L3-p11-module-graph/package.json`: name=`L3-p11-module-graph` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L3/L3-p12-feature-toggles/package.json`: name=`L3-p12-feature-toggles` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L3/L3-p13-microfrontend-bridge/package.json`: name=`L3-p13-microfrontend-bridge` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L3/L3-p14-perf-budget/package.json`: name=`L3-p14-perf-budget` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `L3/L3-p15-ci-matrix/package.json`: name=`L3-p15-ci-matrix` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server

### Seminar4_p3-monorepo.zip

```
.github/workflows/e2e.yml
.github/workflows/unit-jest.yml
.github/workflows/unit-vitest.yml
.github/workflows/workbox-sw.yml
package.json
packages/L1-p01-esm-bootstrap/README.md
packages/L1-p01-esm-bootstrap/babel.config.cjs
packages/L1-p01-esm-bootstrap/jest.config.cjs
packages/L1-p01-esm-bootstrap/package.json
packages/L1-p01-esm-bootstrap/public/data/events.json
packages/L1-p01-esm-bootstrap/public/index.html
packages/L1-p01-esm-bootstrap/public/styles.css
packages/L1-p01-esm-bootstrap/src/dom.js
packages/L1-p01-esm-bootstrap/src/events.js
packages/L1-p01-esm-bootstrap/src/filters.js
packages/L1-p01-esm-bootstrap/src/loader.js
packages/L1-p01-esm-bootstrap/src/main.js
packages/L1-p01-esm-bootstrap/src/services/data.js
packages/L1-p01-esm-bootstrap/src/ui/list.js
packages/L1-p01-esm-bootstrap/tests/jest/spec.jest.test.js
packages/L1-p01-esm-bootstrap/tests/vitest/spec.test.js
packages/L1-p01-esm-bootstrap/vitest.config.ts
packages/L1-p02-dom-helpers/README.md
packages/L1-p02-dom-helpers/babel.config.cjs
packages/L1-p02-dom-helpers/jest.config.cjs
packages/L1-p02-dom-helpers/package.json
packages/L1-p02-dom-helpers/public/data/events.json
packages/L1-p02-dom-helpers/public/index.html
packages/L1-p02-dom-helpers/public/styles.css
packages/L1-p02-dom-helpers/src/dom.js
packages/L1-p02-dom-helpers/src/events.js
packages/L1-p02-dom-helpers/src/filters.js
packages/L1-p02-dom-helpers/src/loader.js
packages/L1-p02-dom-helpers/src/main.js
packages/L1-p02-dom-helpers/src/services/data.js
packages/L1-p02-dom-helpers/src/ui/list.js
packages/L1-p02-dom-helpers/tests/jest/spec.jest.test.js
packages/L1-p02-dom-helpers/tests/vitest/spec.test.js
packages/L1-p02-dom-helpers/vitest.config.ts
packages/L1-p03-delegation-click/README.md
packages/L1-p03-delegation-click/babel.config.cjs
packages/L1-p03-delegation-click/jest.config.cjs
packages/L1-p03-delegation-click/package.json
packages/L1-p03-delegation-click/public/data/events.json
packages/L1-p03-delegation-click/public/index.html
packages/L1-p03-delegation-click/public/styles.css
packages/L1-p03-delegation-click/src/dom.js
packages/L1-p03-delegation-click/src/events.js
packages/L1-p03-delegation-click/src/filters.js
packages/L1-p03-delegation-click/src/loader.js
packages/L1-p03-delegation-click/src/main.js
packages/L1-p03-delegation-click/src/services/data.js
packages/L1-p03-delegation-click/src/ui/list.js
packages/L1-p03-delegation-click/tests/jest/spec.jest.test.js
packages/L1-p03-delegation-click/tests/vitest/spec.test.js
packages/L1-p03-delegation-click/vitest.config.ts
packages/L1-p04-once-passive-capture/README.md
packages/L1-p04-once-passive-capture/babel.config.cjs
packages/L1-p04-once-passive-capture/jest.config.cjs
packages/L1-p04-once-passive-capture/package.json
packages/L1-p04-once-passive-capture/public/data/events.json
packages/L1-p04-once-passive-capture/public/index.html
packages/L1-p04-once-passive-capture/public/styles.css
packages/L1-p04-once-passive-capture/src/dom.js
packages/L1-p04-once-passive-capture/src/events.js
packages/L1-p04-once-passive-capture/src/filters.js
packages/L1-p04-once-passive-capture/src/loader.js
packages/L1-p04-once-passive-capture/src/main.js
packages/L1-p04-once-passive-capture/src/services/data.js
packages/L1-p04-once-passive-capture/src/ui/list.js
packages/L1-p04-once-passive-capture/tests/jest/spec.jest.test.js
packages/L1-p04-once-passive-capture/tests/vitest/spec.test.js
packages/L1-p04-once-passive-capture/vitest.config.ts
packages/L1-p05-custom-event-basics/README.md
packages/L1-p05-custom-event-basics/babel.config.cjs
packages/L1-p05-custom-event-basics/jest.config.cjs
packages/L1-p05-custom-event-basics/package.json
packages/L1-p05-custom-event-basics/public/data/events.json
packages/L1-p05-custom-event-basics/public/index.html
packages/L1-p05-custom-event-basics/public/styles.css
packages/L1-p05-custom-event-basics/src/dom.js
packages/L1-p05-custom-event-basics/src/events.js
packages/L1-p05-custom-event-basics/src/filters.js
packages/L1-p05-custom-event-basics/src/loader.js
packages/L1-p05-custom-event-basics/src/main.js
packages/L1-p05-custom-event-basics/src/services/data.js
packages/L1-p05-custom-event-basics/src/ui/list.js
packages/L1-p05-custom-event-basics/tests/jest/spec.jest.test.js
packages/L1-p05-custom-event-basics/tests/vitest/spec.test.js
packages/L1-p05-custom-event-basics/vitest.config.ts
packages/L1-p06-template-clone/README.md
packages/L1-p06-template-clone/babel.config.cjs
packages/L1-p06-template-clone/jest.config.cjs
packages/L1-p06-template-clone/package.json
packages/L1-p06-template-clone/public/data/events.json
packages/L1-p06-template-clone/public/index.html
packages/L1-p06-template-clone/public/styles.css
packages/L1-p06-template-clone/src/dom.js
packages/L1-p06-template-clone/src/events.js
packages/L1-p06-template-clone/src/filters.js
packages/L1-p06-template-clone/src/loader.js
packages/L1-p06-template-clone/src/main.js
packages/L1-p06-template-clone/src/services/data.js
packages/L1-p06-template-clone/src/ui/list.js
packages/L1-p06-template-clone/tests/jest/spec.jest.test.js
packages/L1-p06-template-clone/tests/vitest/spec.test.js
packages/L1-p06-template-clone/vitest.config.ts
packages/L1-p07-fragment-render/README.md
packages/L1-p07-fragment-render/babel.config.cjs
packages/L1-p07-fragment-render/jest.config.cjs
packages/L1-p07-fragment-render/package.json
packages/L1-p07-fragment-render/public/data/events.json
packages/L1-p07-fragment-render/public/index.html
packages/L1-p07-fragment-render/public/styles.css
packages/L1-p07-fragment-render/src/dom.js
packages/L1-p07-fragment-render/src/events.js
packages/L1-p07-fragment-render/src/filters.js
packages/L1-p07-fragment-render/src/loader.js
packages/L1-p07-fragment-render/src/main.js
packages/L1-p07-fragment-render/src/services/data.js
packages/L1-p07-fragment-render/src/ui/list.js
packages/L1-p07-fragment-render/tests/jest/spec.jest.test.js
packages/L1-p07-fragment-render/tests/vitest/spec.test.js
packages/L1-p07-fragment-render/vitest.config.ts
packages/L1-p08-dataset-attrs/README.md
packages/L1-p08-dataset-attrs/babel.config.cjs
packages/L1-p08-dataset-attrs/jest.config.cjs
packages/L1-p08-dataset-attrs/package.json
packages/L1-p08-dataset-attrs/public/data/events.json
packages/L1-p08-dataset-attrs/public/index.html
packages/L1-p08-dataset-attrs/public/styles.css
packages/L1-p08-dataset-attrs/src/dom.js
packages/L1-p08-dataset-attrs/src/events.js
packages/L1-p08-dataset-attrs/src/filters.js
packages/L1-p08-dataset-attrs/src/loader.js
packages/L1-p08-dataset-attrs/src/main.js
packages/L1-p08-dataset-attrs/src/services/data.js
packages/L1-p08-dataset-attrs/src/ui/list.js
packages/L1-p08-dataset-attrs/tests/jest/spec.jest.test.js
packages/L1-p08-dataset-attrs/tests/vitest/spec.test.js
packages/L1-p08-dataset-attrs/vitest.config.ts
packages/L1-p09-class-toggle/README.md
packages/L1-p09-class-toggle/babel.config.cjs
packages/L1-p09-class-toggle/jest.config.cjs
packages/L1-p09-class-toggle/package.json
packages/L1-p09-class-toggle/public/data/events.json
packages/L1-p09-class-toggle/public/index.html
packages/L1-p09-class-toggle/public/styles.css
packages/L1-p09-class-toggle/src/dom.js
packages/L1-p09-class-toggle/src/events.js
packages/L1-p09-class-toggle/src/filters.js
packages/L1-p09-class-toggle/src/loader.js
packages/L1-p09-class-toggle/src/main.js
packages/L1-p09-class-toggle/src/services/data.js
packages/L1-p09-class-toggle/src/ui/list.js
packages/L1-p09-class-toggle/tests/jest/spec.jest.test.js
packages/L1-p09-class-toggle/tests/vitest/spec.test.js
packages/L1-p09-class-toggle/vitest.config.ts
packages/L1-p10-form-input-sync/README.md
packages/L1-p10-form-input-sync/babel.config.cjs
packages/L1-p10-form-input-sync/jest.config.cjs
packages/L1-p10-form-input-sync/package.json
packages/L1-p10-form-input-sync/public/data/events.json
packages/L1-p10-form-input-sync/public/index.html
packages/L1-p10-form-input-sync/public/styles.css
packages/L1-p10-form-input-sync/src/dom.js
packages/L1-p10-form-input-sync/src/events.js
packages/L1-p10-form-input-sync/src/filters.js
packages/L1-p10-form-input-sync/src/loader.js
packages/L1-p10-form-input-sync/src/main.js
packages/L1-p10-form-input-sync/src/services/data.js
packages/L1-p10-form-input-sync/src/ui/list.js
packages/L1-p10-form-input-sync/tests/jest/spec.jest.test.js
packages/L1-p10-form-input-sync/tests/vitest/spec.test.js
packages/L1-p10-form-input-sync/vitest.config.ts
packages/L1-p11-aria-live/README.md
packages/L1-p11-aria-live/babel.config.cjs
packages/L1-p11-aria-live/jest.config.cjs
packages/L1-p11-aria-live/package.json
packages/L1-p11-aria-live/public/data/events.json
packages/L1-p11-aria-live/public/index.html
packages/L1-p11-aria-live/public/styles.css
packages/L1-p11-aria-live/src/dom.js
packages/L1-p11-aria-live/src/events.js
packages/L1-p11-aria-live/src/filters.js
packages/L1-p11-aria-live/src/loader.js
packages/L1-p11-aria-live/src/main.js
packages/L1-p11-aria-live/src/services/data.js
packages/L1-p11-aria-live/src/ui/list.js
packages/L1-p11-aria-live/tests/jest/spec.jest.test.js
packages/L1-p11-aria-live/tests/vitest/spec.test.js
packages/L1-p11-aria-live/vitest.config.ts
packages/L1-p12-keyboard-events/README.md
packages/L1-p12-keyboard-events/babel.config.cjs
packages/L1-p12-keyboard-events/jest.config.cjs
packages/L1-p12-keyboard-events/package.json
packages/L1-p12-keyboard-events/public/data/events.json
packages/L1-p12-keyboard-events/public/index.html
packages/L1-p12-keyboard-events/public/styles.css
packages/L1-p12-keyboard-events/src/dom.js
packages/L1-p12-keyboard-events/src/events.js
packages/L1-p12-keyboard-events/src/filters.js
packages/L1-p12-keyboard-events/src/loader.js
packages/L1-p12-keyboard-events/src/main.js
packages/L1-p12-keyboard-events/src/services/data.js
packages/L1-p12-keyboard-events/src/ui/list.js
packages/L1-p12-keyboard-events/tests/jest/spec.jest.test.js
packages/L1-p12-keyboard-events/tests/vitest/spec.test.js
packages/L1-p12-keyboard-events/vitest.config.ts
packages/L1-p13-target-currentTarget/README.md
packages/L1-p13-target-currentTarget/babel.config.cjs
packages/L1-p13-target-currentTarget/jest.config.cjs
packages/L1-p13-target-currentTarget/package.json
packages/L1-p13-target-currentTarget/public/data/events.json
packages/L1-p13-target-currentTarget/public/index.html
packages/L1-p13-target-currentTarget/public/styles.css
packages/L1-p13-target-currentTarget/src/dom.js
packages/L1-p13-target-currentTarget/src/events.js
packages/L1-p13-target-currentTarget/src/filters.js
packages/L1-p13-target-currentTarget/src/loader.js
packages/L1-p13-target-currentTarget/src/main.js
packages/L1-p13-target-currentTarget/src/services/data.js
packages/L1-p13-target-currentTarget/src/ui/list.js
packages/L1-p13-target-currentTarget/tests/jest/spec.jest.test.js
packages/L1-p13-target-currentTarget/tests/vitest/spec.test.js
packages/L1-p13-target-currentTarget/vitest.config.ts
packages/L1-p14-cleanup-abort/README.md
packages/L1-p14-cleanup-abort/babel.config.cjs
packages/L1-p14-cleanup-abort/jest.config.cjs
packages/L1-p14-cleanup-abort/package.json
packages/L1-p14-cleanup-abort/public/data/events.json
packages/L1-p14-cleanup-abort/public/index.html
packages/L1-p14-cleanup-abort/public/styles.css
packages/L1-p14-cleanup-abort/src/dom.js
packages/L1-p14-cleanup-abort/src/events.js
packages/L1-p14-cleanup-abort/src/filters.js
packages/L1-p14-cleanup-abort/src/loader.js
packages/L1-p14-cleanup-abort/src/main.js
packages/L1-p14-cleanup-abort/src/services/data.js
packages/L1-p14-cleanup-abort/src/ui/list.js
packages/L1-p14-cleanup-abort/tests/jest/spec.jest.test.js
packages/L1-p14-cleanup-abort/tests/vitest/spec.test.js
packages/L1-p14-cleanup-abort/vitest.config.ts
packages/L1-p15-module-boundary/README.md
packages/L1-p15-module-boundary/babel.config.cjs
packages/L1-p15-module-boundary/jest.config.cjs
packages/L1-p15-module-boundary/package.json
packages/L1-p15-module-boundary/public/data/events.json
packages/L1-p15-module-boundary/public/index.html
packages/L1-p15-module-boundary/public/styles.css
packages/L1-p15-module-boundary/src/dom.js
packages/L1-p15-module-boundary/src/events.js
packages/L1-p15-module-boundary/src/filters.js
packages/L1-p15-module-boundary/src/loader.js
packages/L1-p15-module-boundary/src/main.js
packages/L1-p15-module-boundary/src/services/data.js
packages/L1-p15-module-boundary/src/ui/list.js
packages/L1-p15-module-boundary/tests/jest/spec.jest.test.js
packages/L1-p15-module-boundary/tests/vitest/spec.test.js
packages/L1-p15-module-boundary/vitest.config.ts
packages/L2-p01-import-maps/README.md
packages/L2-p01-import-maps/babel.config.cjs
packages/L2-p01-import-maps/jest.config.cjs
packages/L2-p01-import-maps/package.json
packages/L2-p01-import-maps/public/data/events.json
packages/L2-p01-import-maps/public/index.html
packages/L2-p01-import-maps/public/styles.css
packages/L2-p01-import-maps/src/dom.js
packages/L2-p01-import-maps/src/events.js
packages/L2-p01-import-maps/src/filters.js
packages/L2-p01-import-maps/src/loader.js
packages/L2-p01-import-maps/src/main.js
packages/L2-p01-import-maps/src/services/data.js
packages/L2-p01-import-maps/src/ui/list.js
packages/L2-p01-import-maps/tests/jest/spec.jest.test.js
packages/L2-p01-import-maps/tests/vitest/spec.test.js
packages/L2-p01-import-maps/vitest.config.ts
packages/L2-p02-services-json/README.md
packages/L2-p02-services-json/babel.config.cjs
packages/L2-p02-services-json/jest.config.cjs
packages/L2-p02-services-json/package.json
packages/L2-p02-services-json/public/data/events.json
packages/L2-p02-services-json/public/index.html
packages/L2-p02-services-json/public/styles.css
packages/L2-p02-services-json/src/dom.js
packages/L2-p02-services-json/src/events.js
packages/L2-p02-services-json/src/filters.js
packages/L2-p02-services-json/src/loader.js
packages/L2-p02-services-json/src/main.js
packages/L2-p02-services-json/src/services/data.js
packages/L2-p02-services-json/src/ui/list.js
packages/L2-p02-services-json/tests/jest/spec.jest.test.js
packages/L2-p02-services-json/tests/vitest/spec.test.js
packages/L2-p02-services-json/vitest.config.ts
packages/L2-p03-dynamic-import/README.md
packages/L2-p03-dynamic-import/babel.config.cjs
packages/L2-p03-dynamic-import/jest.config.cjs
packages/L2-p03-dynamic-import/package.json
packages/L2-p03-dynamic-import/public/data/events.json
packages/L2-p03-dynamic-import/public/index.html
packages/L2-p03-dynamic-import/public/styles.css
packages/L2-p03-dynamic-import/src/dom.js
packages/L2-p03-dynamic-import/src/events.js
packages/L2-p03-dynamic-import/src/filters.js
packages/L2-p03-dynamic-import/src/loader.js
packages/L2-p03-dynamic-import/src/main.js
packages/L2-p03-dynamic-import/src/services/data.js
packages/L2-p03-dynamic-import/src/ui/list.js
packages/L2-p03-dynamic-import/tests/jest/spec.jest.test.js
packages/L2-p03-dynamic-import/tests/vitest/spec.test.js
packages/L2-p03-dynamic-import/vitest.config.ts
packages/L2-p04-reexports/README.md
packages/L2-p04-reexports/babel.config.cjs
packages/L2-p04-reexports/jest.config.cjs
packages/L2-p04-reexports/package.json
packages/L2-p04-reexports/public/data/events.json
packages/L2-p04-reexports/public/index.html
packages/L2-p04-reexports/public/styles.css
packages/L2-p04-reexports/src/dom.js
packages/L2-p04-reexports/src/events.js
packages/L2-p04-reexports/src/filters.js
packages/L2-p04-reexports/src/loader.js
packages/L2-p04-reexports/src/main.js
packages/L2-p04-reexports/src/services/data.js
packages/L2-p04-reexports/src/ui/list.js
packages/L2-p04-reexports/tests/jest/spec.jest.test.js
packages/L2-p04-reexports/tests/vitest/spec.test.js
packages/L2-p04-reexports/vitest.config.ts
packages/L2-p05-tree-shaking/README.md
packages/L2-p05-tree-shaking/babel.config.cjs
packages/L2-p05-tree-shaking/jest.config.cjs
packages/L2-p05-tree-shaking/package.json
packages/L2-p05-tree-shaking/public/data/events.json
packages/L2-p05-tree-shaking/public/index.html
packages/L2-p05-tree-shaking/public/styles.css
packages/L2-p05-tree-shaking/src/dom.js
packages/L2-p05-tree-shaking/src/events.js
packages/L2-p05-tree-shaking/src/filters.js
packages/L2-p05-tree-shaking/src/loader.js
packages/L2-p05-tree-shaking/src/main.js
packages/L2-p05-tree-shaking/src/services/data.js
packages/L2-p05-tree-shaking/src/ui/list.js
packages/L2-p05-tree-shaking/tests/jest/spec.jest.test.js
packages/L2-p05-tree-shaking/tests/vitest/spec.test.js
packages/L2-p05-tree-shaking/vitest.config.ts
packages/L2-p06-code-splitting/README.md
packages/L2-p06-code-splitting/babel.config.cjs
packages/L2-p06-code-splitting/jest.config.cjs
packages/L2-p06-code-splitting/package.json
packages/L2-p06-code-splitting/public/data/events.json
packages/L2-p06-code-splitting/public/index.html
packages/L2-p06-code-splitting/public/styles.css
packages/L2-p06-code-splitting/src/dom.js
packages/L2-p06-code-splitting/src/events.js
packages/L2-p06-code-splitting/src/filters.js
packages/L2-p06-code-splitting/src/loader.js
packages/L2-p06-code-splitting/src/main.js
packages/L2-p06-code-splitting/src/secondary.js
packages/L2-p06-code-splitting/src/services/data.js
packages/L2-p06-code-splitting/src/ui/list.js
packages/L2-p06-code-splitting/tests/jest/spec.jest.test.js
packages/L2-p06-code-splitting/tests/vitest/spec.test.js
packages/L2-p06-code-splitting/vitest.config.ts
packages/L2-p07-modulepreload-metrics/README.md
packages/L2-p07-modulepreload-metrics/babel.config.cjs
packages/L2-p07-modulepreload-metrics/jest.config.cjs
packages/L2-p07-modulepreload-metrics/package.json
packages/L2-p07-modulepreload-metrics/public/data/events.json
packages/L2-p07-modulepreload-metrics/public/index.html
packages/L2-p07-modulepreload-metrics/public/styles.css
packages/L2-p07-modulepreload-metrics/src/dom.js
packages/L2-p07-modulepreload-metrics/src/events.js
packages/L2-p07-modulepreload-metrics/src/filters.js
packages/L2-p07-modulepreload-metrics/src/loader.js
packages/L2-p07-modulepreload-metrics/src/main.js
packages/L2-p07-modulepreload-metrics/src/services/data.js
packages/L2-p07-modulepreload-metrics/src/ui/list.js
packages/L2-p07-modulepreload-metrics/tests/jest/spec.jest.test.js
packages/L2-p07-modulepreload-metrics/tests/vitest/spec.test.js
packages/L2-p07-modulepreload-metrics/vitest.config.ts
packages/L2-p08-csp-scan/README.md
packages/L2-p08-csp-scan/babel.config.cjs
packages/L2-p08-csp-scan/jest.config.cjs
packages/L2-p08-csp-scan/package.json
packages/L2-p08-csp-scan/public/data/events.json
packages/L2-p08-csp-scan/public/index.html
packages/L2-p08-csp-scan/public/styles.css
packages/L2-p08-csp-scan/src/dom.js
packages/L2-p08-csp-scan/src/events.js
packages/L2-p08-csp-scan/src/filters.js
packages/L2-p08-csp-scan/src/loader.js
packages/L2-p08-csp-scan/src/main.js
packages/L2-p08-csp-scan/src/services/data.js
packages/L2-p08-csp-scan/src/ui/list.js
packages/L2-p08-csp-scan/tests/jest/spec.jest.test.js
packages/L2-p08-csp-scan/tests/vitest/spec.test.js
packages/L2-p08-csp-scan/vitest.config.ts
packages/L2-p09-adapter/README.md
packages/L2-p09-adapter/babel.config.cjs
packages/L2-p09-adapter/jest.config.cjs
packages/L2-p09-adapter/package.json
packages/L2-p09-adapter/public/data/events.json
packages/L2-p09-adapter/public/index.html
packages/L2-p09-adapter/public/styles.css
packages/L2-p09-adapter/src/dom.js
packages/L2-p09-adapter/src/events.js
packages/L2-p09-adapter/src/filters.js
packages/L2-p09-adapter/src/loader.js
packages/L2-p09-adapter/src/main.js
packages/L2-p09-adapter/src/services/data.js
packages/L2-p09-adapter/src/ui/list.js
packages/L2-p09-adapter/tests/jest/spec.jest.test.js
packages/L2-p09-adapter/tests/vitest/spec.test.js
packages/L2-p09-adapter/vitest.config.ts
packages/L2-p10-mutation-observer/README.md
packages/L2-p10-mutation-observer/babel.config.cjs
packages/L2-p10-mutation-observer/jest.config.cjs
packages/L2-p10-mutation-observer/package.json
packages/L2-p10-mutation-observer/public/data/events.json
packages/L2-p10-mutation-observer/public/index.html
packages/L2-p10-mutation-observer/public/styles.css
packages/L2-p10-mutation-observer/src/dom.js
packages/L2-p10-mutation-observer/src/events.js
packages/L2-p10-mutation-observer/src/filters.js
packages/L2-p10-mutation-observer/src/loader.js
packages/L2-p10-mutation-observer/src/main.js
packages/L2-p10-mutation-observer/src/mut.js
packages/L2-p10-mutation-observer/src/services/data.js
packages/L2-p10-mutation-observer/src/ui/list.js
packages/L2-p10-mutation-observer/tests/jest/spec.jest.test.js
packages/L2-p10-mutation-observer/tests/vitest/spec.test.js
packages/L2-p10-mutation-observer/vitest.config.ts
packages/L2-p11-throttle-input/README.md
packages/L2-p11-throttle-input/babel.config.cjs
packages/L2-p11-throttle-input/jest.config.cjs
packages/L2-p11-throttle-input/package.json
packages/L2-p11-throttle-input/public/data/events.json
packages/L2-p11-throttle-input/public/index.html
packages/L2-p11-throttle-input/public/styles.css
packages/L2-p11-throttle-input/src/dom.js
packages/L2-p11-throttle-input/src/events.js
packages/L2-p11-throttle-input/src/filters.js
packages/L2-p11-throttle-input/src/loader.js
packages/L2-p11-throttle-input/src/main.js
packages/L2-p11-throttle-input/src/services/data.js
packages/L2-p11-throttle-input/src/throttle.js
packages/L2-p11-throttle-input/src/ui/list.js
packages/L2-p11-throttle-input/tests/jest/spec.jest.test.js
packages/L2-p11-throttle-input/tests/vitest/spec.test.js
packages/L2-p11-throttle-input/vitest.config.ts
packages/L2-p12-event-guards/README.md
packages/L2-p12-event-guards/babel.config.cjs
packages/L2-p12-event-guards/jest.config.cjs
packages/L2-p12-event-guards/package.json
packages/L2-p12-event-guards/public/data/events.json
packages/L2-p12-event-guards/public/index.html
packages/L2-p12-event-guards/public/styles.css
packages/L2-p12-event-guards/src/dom.js
packages/L2-p12-event-guards/src/events.js
packages/L2-p12-event-guards/src/filters.js
packages/L2-p12-event-guards/src/loader.js
packages/L2-p12-event-guards/src/main.js
packages/L2-p12-event-guards/src/services/data.js
packages/L2-p12-event-guards/src/ui/list.js
packages/L2-p12-event-guards/tests/jest/spec.jest.test.js
packages/L2-p12-event-guards/tests/vitest/spec.test.js
packages/L2-p12-event-guards/vitest.config.ts
packages/L2-p13-import-conditions-doc/README.md
packages/L2-p13-import-conditions-doc/babel.config.cjs
packages/L2-p13-import-conditions-doc/jest.config.cjs
packages/L2-p13-import-conditions-doc/package.json
packages/L2-p13-import-conditions-doc/public/data/events.json
packages/L2-p13-import-conditions-doc/public/index.html
packages/L2-p13-import-conditions-doc/public/styles.css
packages/L2-p13-import-conditions-doc/src/dom.js
packages/L2-p13-import-conditions-doc/src/events.js
packages/L2-p13-import-conditions-doc/src/filters.js
packages/L2-p13-import-conditions-doc/src/loader.js
packages/L2-p13-import-conditions-doc/src/main.js
packages/L2-p13-import-conditions-doc/src/services/data.js
packages/L2-p13-import-conditions-doc/src/ui/list.js
packages/L2-p13-import-conditions-doc/tests/jest/spec.jest.test.js
packages/L2-p13-import-conditions-doc/tests/vitest/spec.test.js
packages/L2-p13-import-conditions-doc/vitest.config.ts
packages/L2-p14-subpath-exports-doc/README.md
packages/L2-p14-subpath-exports-doc/babel.config.cjs
packages/L2-p14-subpath-exports-doc/jest.config.cjs
packages/L2-p14-subpath-exports-doc/package.json
packages/L2-p14-subpath-exports-doc/public/data/events.json
packages/L2-p14-subpath-exports-doc/public/index.html
packages/L2-p14-subpath-exports-doc/public/styles.css
packages/L2-p14-subpath-exports-doc/src/dom.js
packages/L2-p14-subpath-exports-doc/src/events.js
packages/L2-p14-subpath-exports-doc/src/filters.js
packages/L2-p14-subpath-exports-doc/src/loader.js
packages/L2-p14-subpath-exports-doc/src/main.js
packages/L2-p14-subpath-exports-doc/src/services/data.js
packages/L2-p14-subpath-exports-doc/src/ui/list.js
packages/L2-p14-subpath-exports-doc/tests/jest/spec.jest.test.js
packages/L2-p14-subpath-exports-doc/tests/vitest/spec.test.js
packages/L2-p14-subpath-exports-doc/vitest.config.ts
packages/L2-p15-esm-cjs-interop-doc/README.md
packages/L2-p15-esm-cjs-interop-doc/babel.config.cjs
packages/L2-p15-esm-cjs-interop-doc/jest.config.cjs
packages/L2-p15-esm-cjs-interop-doc/package.json
packages/L2-p15-esm-cjs-interop-doc/public/data/events.json
packages/L2-p15-esm-cjs-interop-doc/public/index.html
packages/L2-p15-esm-cjs-interop-doc/public/styles.css
packages/L2-p15-esm-cjs-interop-doc/src/dom.js
packages/L2-p15-esm-cjs-interop-doc/src/events.js
packages/L2-p15-esm-cjs-interop-doc/src/filters.js
packages/L2-p15-esm-cjs-interop-doc/src/loader.js
packages/L2-p15-esm-cjs-interop-doc/src/main.js
packages/L2-p15-esm-cjs-interop-doc/src/services/data.js
packages/L2-p15-esm-cjs-interop-doc/src/ui/list.js
packages/L2-p15-esm-cjs-interop-doc/tests/jest/spec.jest.test.js
packages/L2-p15-esm-cjs-interop-doc/tests/vitest/spec.test.js
packages/L2-p15-esm-cjs-interop-doc/vitest.config.ts
packages/L3-p01-bus-namespaced/README.md
packages/L3-p01-bus-namespaced/babel.config.cjs
packages/L3-p01-bus-namespaced/jest.config.cjs
packages/L3-p01-bus-namespaced/package.json
packages/L3-p01-bus-namespaced/public/data/events.json
packages/L3-p01-bus-namespaced/public/index.html
packages/L3-p01-bus-namespaced/public/styles.css
packages/L3-p01-bus-namespaced/src/dom.js
packages/L3-p01-bus-namespaced/src/events.js
packages/L3-p01-bus-namespaced/src/filters.js
packages/L3-p01-bus-namespaced/src/loader.js
packages/L3-p01-bus-namespaced/src/main.js
packages/L3-p01-bus-namespaced/src/services/data.js
packages/L3-p01-bus-namespaced/src/ui/list.js
packages/L3-p01-bus-namespaced/tests/jest/spec.jest.test.js
packages/L3-p01-bus-namespaced/tests/vitest/spec.test.js
packages/L3-p01-bus-namespaced/vitest.config.ts
packages/L3-p02-timeout-signal/README.md
packages/L3-p02-timeout-signal/babel.config.cjs
packages/L3-p02-timeout-signal/jest.config.cjs
packages/L3-p02-timeout-signal/package.json
packages/L3-p02-timeout-signal/public/data/events.json
packages/L3-p02-timeout-signal/public/index.html
packages/L3-p02-timeout-signal/public/styles.css
packages/L3-p02-timeout-signal/src/dom.js
packages/L3-p02-timeout-signal/src/events.js
packages/L3-p02-timeout-signal/src/filters.js
packages/L3-p02-timeout-signal/src/loader.js
packages/L3-p02-timeout-signal/src/main.js
packages/L3-p02-timeout-signal/src/services/data.js
packages/L3-p02-timeout-signal/src/timeout.js
packages/L3-p02-timeout-signal/src/ui/list.js
packages/L3-p02-timeout-signal/tests/jest/spec.jest.test.js
packages/L3-p02-timeout-signal/tests/vitest/spec.test.js
packages/L3-p02-timeout-signal/vitest.config.ts
packages/L3-p03-intersection-observer/README.md
packages/L3-p03-intersection-observer/babel.config.cjs
packages/L3-p03-intersection-observer/jest.config.cjs
packages/L3-p03-intersection-observer/package.json
packages/L3-p03-intersection-observer/public/data/events.json
packages/L3-p03-intersection-observer/public/index.html
packages/L3-p03-intersection-observer/public/styles.css
packages/L3-p03-intersection-observer/src/dom.js
packages/L3-p03-intersection-observer/src/events.js
packages/L3-p03-intersection-observer/src/filters.js
packages/L3-p03-intersection-observer/src/lazy.js
packages/L3-p03-intersection-observer/src/loader.js
packages/L3-p03-intersection-observer/src/main.js
packages/L3-p03-intersection-observer/src/services/data.js
packages/L3-p03-intersection-observer/src/ui/list.js
packages/L3-p03-intersection-observer/tests/jest/spec.jest.test.js
packages/L3-p03-intersection-observer/tests/vitest/spec.test.js
packages/L3-p03-intersection-observer/vitest.config.ts
packages/L3-p04-mutation-raf-batch/README.md
packages/L3-p04-mutation-raf-batch/babel.config.cjs
packages/L3-p04-mutation-raf-batch/jest.config.cjs
packages/L3-p04-mutation-raf-batch/package.json
packages/L3-p04-mutation-raf-batch/public/data/events.json
packages/L3-p04-mutation-raf-batch/public/index.html
packages/L3-p04-mutation-raf-batch/public/styles.css
packages/L3-p04-mutation-raf-batch/src/dom.js
packages/L3-p04-mutation-raf-batch/src/events.js
packages/L3-p04-mutation-raf-batch/src/filters.js
packages/L3-p04-mutation-raf-batch/src/loader.js
packages/L3-p04-mutation-raf-batch/src/main.js
packages/L3-p04-mutation-raf-batch/src/services/data.js
packages/L3-p04-mutation-raf-batch/src/ui/list.js
packages/L3-p04-mutation-raf-batch/tests/jest/spec.jest.test.js
packages/L3-p04-mutation-raf-batch/tests/vitest/spec.test.js
packages/L3-p04-mutation-raf-batch/vitest.config.ts
packages/L3-p05-composed-events/README.md
packages/L3-p05-composed-events/babel.config.cjs
packages/L3-p05-composed-events/jest.config.cjs
packages/L3-p05-composed-events/package.json
packages/L3-p05-composed-events/public/data/events.json
packages/L3-p05-composed-events/public/index.html
packages/L3-p05-composed-events/public/styles.css
packages/L3-p05-composed-events/src/dom.js
packages/L3-p05-composed-events/src/events.js
packages/L3-p05-composed-events/src/filters.js
packages/L3-p05-composed-events/src/loader.js
packages/L3-p05-composed-events/src/main.js
packages/L3-p05-composed-events/src/services/data.js
packages/L3-p05-composed-events/src/ui/list.js
packages/L3-p05-composed-events/tests/jest/spec.jest.test.js
packages/L3-p05-composed-events/tests/vitest/spec.test.js
packages/L3-p05-composed-events/vitest.config.ts
packages/L3-p06-event-replay/README.md
packages/L3-p06-event-replay/babel.config.cjs
packages/L3-p06-event-replay/jest.config.cjs
packages/L3-p06-event-replay/package.json
packages/L3-p06-event-replay/public/data/events.json
packages/L3-p06-event-replay/public/index.html
packages/L3-p06-event-replay/public/styles.css
packages/L3-p06-event-replay/src/dom.js
packages/L3-p06-event-replay/src/events.js
packages/L3-p06-event-replay/src/filters.js
packages/L3-p06-event-replay/src/loader.js
packages/L3-p06-event-replay/src/main.js
packages/L3-p06-event-replay/src/replay.js
packages/L3-p06-event-replay/src/services/data.js
packages/L3-p06-event-replay/src/ui/list.js
packages/L3-p06-event-replay/tests/jest/spec.jest.test.js
packages/L3-p06-event-replay/tests/vitest/spec.test.js
packages/L3-p06-event-replay/vitest.config.ts
packages/L3-p07-e2e-filter/README.md
packages/L3-p07-e2e-filter/babel.config.cjs
packages/L3-p07-e2e-filter/jest.config.cjs
packages/L3-p07-e2e-filter/package.json
packages/L3-p07-e2e-filter/playwright.config.ts
packages/L3-p07-e2e-filter/public/data/events.json
packages/L3-p07-e2e-filter/public/index.html
packages/L3-p07-e2e-filter/public/styles.css
packages/L3-p07-e2e-filter/src/dom.js
packages/L3-p07-e2e-filter/src/events.js
packages/L3-p07-e2e-filter/src/filters.js
packages/L3-p07-e2e-filter/src/loader.js
packages/L3-p07-e2e-filter/src/main.js
packages/L3-p07-e2e-filter/src/services/data.js
packages/L3-p07-e2e-filter/src/ui/list.js
packages/L3-p07-e2e-filter/tests/e2e.spec.ts
packages/L3-p07-e2e-filter/tests/jest/spec.jest.test.js
packages/L3-p07-e2e-filter/tests/vitest/spec.test.js
packages/L3-p07-e2e-filter/vitest.config.ts
packages/L3-p08-e2e-keyboard/README.md
packages/L3-p08-e2e-keyboard/babel.config.cjs
packages/L3-p08-e2e-keyboard/jest.config.cjs
packages/L3-p08-e2e-keyboard/package.json
packages/L3-p08-e2e-keyboard/playwright.config.ts
packages/L3-p08-e2e-keyboard/public/data/events.json
packages/L3-p08-e2e-keyboard/public/index.html
packages/L3-p08-e2e-keyboard/public/styles.css
packages/L3-p08-e2e-keyboard/src/dom.js
packages/L3-p08-e2e-keyboard/src/events.js
packages/L3-p08-e2e-keyboard/src/filters.js
packages/L3-p08-e2e-keyboard/src/loader.js
packages/L3-p08-e2e-keyboard/src/main.js
packages/L3-p08-e2e-keyboard/src/services/data.js
packages/L3-p08-e2e-keyboard/src/ui/list.js
packages/L3-p08-e2e-keyboard/tests/e2e.spec.ts
packages/L3-p08-e2e-keyboard/tests/jest/spec.jest.test.js
packages/L3-p08-e2e-keyboard/tests/vitest/spec.test.js
packages/L3-p08-e2e-keyboard/vitest.config.ts
packages/L3-p09-pwa-workbox/README.md
packages/L3-p09-pwa-workbox/babel.config.cjs
packages/L3-p09-pwa-workbox/build-sw.mjs
packages/L3-p09-pwa-workbox/jest.config.cjs
packages/L3-p09-pwa-workbox/package.json
packages/L3-p09-pwa-workbox/public/data/events.json
packages/L3-p09-pwa-workbox/public/index.html
packages/L3-p09-pwa-workbox/public/styles.css
packages/L3-p09-pwa-workbox/src/dom.js
packages/L3-p09-pwa-workbox/src/events.js
packages/L3-p09-pwa-workbox/src/filters.js
packages/L3-p09-pwa-workbox/src/loader.js
packages/L3-p09-pwa-workbox/src/main.js
packages/L3-p09-pwa-workbox/src/services/data.js
packages/L3-p09-pwa-workbox/src/ui/list.js
packages/L3-p09-pwa-workbox/tests/jest/spec.jest.test.js
packages/L3-p09-pwa-workbox/tests/jest/workbox.jest.test.js
packages/L3-p09-pwa-workbox/tests/vitest/spec.test.js
packages/L3-p09-pwa-workbox/tests/vitest/workbox.test.js
packages/L3-p09-pwa-workbox/vitest.config.ts
packages/L3-p10-e2e-offline-smoke/README.md
packages/L3-p10-e2e-offline-smoke/babel.config.cjs
packages/L3-p10-e2e-offline-smoke/jest.config.cjs
packages/L3-p10-e2e-offline-smoke/package.json
packages/L3-p10-e2e-offline-smoke/playwright.config.ts
packages/L3-p10-e2e-offline-smoke/public/data/events.json
packages/L3-p10-e2e-offline-smoke/public/index.html
packages/L3-p10-e2e-offline-smoke/public/styles.css
packages/L3-p10-e2e-offline-smoke/src/dom.js
packages/L3-p10-e2e-offline-smoke/src/events.js
packages/L3-p10-e2e-offline-smoke/src/filters.js
packages/L3-p10-e2e-offline-smoke/src/loader.js
packages/L3-p10-e2e-offline-smoke/src/main.js
packages/L3-p10-e2e-offline-smoke/src/services/data.js
packages/L3-p10-e2e-offline-smoke/src/ui/list.js
packages/L3-p10-e2e-offline-smoke/tests/e2e.spec.ts
packages/L3-p10-e2e-offline-smoke/tests/jest/spec.jest.test.js
packages/L3-p10-e2e-offline-smoke/tests/vitest/spec.test.js
packages/L3-p10-e2e-offline-smoke/vitest.config.ts
packages/L3-p11-module-graph/README.md
packages/L3-p11-module-graph/babel.config.cjs
packages/L3-p11-module-graph/jest.config.cjs
packages/L3-p11-module-graph/package.json
packages/L3-p11-module-graph/public/data/events.json
packages/L3-p11-module-graph/public/index.html
packages/L3-p11-module-graph/public/styles.css
packages/L3-p11-module-graph/scripts/graph.mjs
packages/L3-p11-module-graph/src/dom.js
packages/L3-p11-module-graph/src/events.js
packages/L3-p11-module-graph/src/filters.js
packages/L3-p11-module-graph/src/loader.js
packages/L3-p11-module-graph/src/main.js
packages/L3-p11-module-graph/src/services/data.js
packages/L3-p11-module-graph/src/ui/list.js
packages/L3-p11-module-graph/tests/jest/spec.jest.test.js
packages/L3-p11-module-graph/tests/vitest/spec.test.js
packages/L3-p11-module-graph/vitest.config.ts
packages/L3-p12-feature-toggles/README.md
packages/L3-p12-feature-toggles/babel.config.cjs
packages/L3-p12-feature-toggles/jest.config.cjs
packages/L3-p12-feature-toggles/package.json
packages/L3-p12-feature-toggles/public/data/events.json
packages/L3-p12-feature-toggles/public/index.html
packages/L3-p12-feature-toggles/public/styles.css
packages/L3-p12-feature-toggles/src/advanced.js
packages/L3-p12-feature-toggles/src/dom.js
packages/L3-p12-feature-toggles/src/events.js
packages/L3-p12-feature-toggles/src/filters.js
packages/L3-p12-feature-toggles/src/loader.js
packages/L3-p12-feature-toggles/src/main.js
packages/L3-p12-feature-toggles/src/services/data.js
packages/L3-p12-feature-toggles/src/toggles.js
packages/L3-p12-feature-toggles/src/ui/list.js
packages/L3-p12-feature-toggles/tests/jest/spec.jest.test.js
packages/L3-p12-feature-toggles/tests/vitest/spec.test.js
packages/L3-p12-feature-toggles/vitest.config.ts
packages/L3-p13-microfrontend-bridge/README.md
packages/L3-p13-microfrontend-bridge/babel.config.cjs
packages/L3-p13-microfrontend-bridge/jest.config.cjs
packages/L3-p13-microfrontend-bridge/package.json
packages/L3-p13-microfrontend-bridge/public/data/events.json
packages/L3-p13-microfrontend-bridge/public/index.html
packages/L3-p13-microfrontend-bridge/public/styles.css
packages/L3-p13-microfrontend-bridge/src/dom.js
packages/L3-p13-microfrontend-bridge/src/events.js
packages/L3-p13-microfrontend-bridge/src/filters.js
packages/L3-p13-microfrontend-bridge/src/loader.js
packages/L3-p13-microfrontend-bridge/src/main.js
packages/L3-p13-microfrontend-bridge/src/services/data.js
packages/L3-p13-microfrontend-bridge/src/ui/list.js
packages/L3-p13-microfrontend-bridge/tests/jest/spec.jest.test.js
packages/L3-p13-microfrontend-bridge/tests/vitest/spec.test.js
packages/L3-p13-microfrontend-bridge/vitest.config.ts
packages/L3-p14-perf-budget/README.md
packages/L3-p14-perf-budget/babel.config.cjs
packages/L3-p14-perf-budget/jest.config.cjs
packages/L3-p14-perf-budget/package.json
packages/L3-p14-perf-budget/public/data/events.json
packages/L3-p14-perf-budget/public/index.html
packages/L3-p14-perf-budget/public/styles.css
packages/L3-p14-perf-budget/src/dom.js
packages/L3-p14-perf-budget/src/events.js
packages/L3-p14-perf-budget/src/filters.js
packages/L3-p14-perf-budget/src/loader.js
packages/L3-p14-perf-budget/src/main.js
packages/L3-p14-perf-budget/src/services/data.js
packages/L3-p14-perf-budget/src/ui/list.js
packages/L3-p14-perf-budget/tests/jest/spec.jest.test.js
packages/L3-p14-perf-budget/tests/vitest/spec.test.js
packages/L3-p14-perf-budget/vitest.config.ts
packages/L3-p15-ci-matrix/README.md
packages/L3-p15-ci-matrix/babel.config.cjs
packages/L3-p15-ci-matrix/jest.config.cjs
packages/L3-p15-ci-matrix/package.json
packages/L3-p15-ci-matrix/public/data/events.json
packages/L3-p15-ci-matrix/public/index.html
packages/L3-p15-ci-matrix/public/styles.css
packages/L3-p15-ci-matrix/src/dom.js
packages/L3-p15-ci-matrix/src/events.js
packages/L3-p15-ci-matrix/src/filters.js
packages/L3-p15-ci-matrix/src/loader.js
packages/L3-p15-ci-matrix/src/main.js
packages/L3-p15-ci-matrix/src/services/data.js
packages/L3-p15-ci-matrix/src/ui/list.js
packages/L3-p15-ci-matrix/tests/jest/spec.jest.test.js
packages/L3-p15-ci-matrix/tests/vitest/spec.test.js
packages/L3-p15-ci-matrix/vitest.config.ts
pnpm-workspace.yaml
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 186, docs: 44, public: 135, code: 323, tests: 95, pwa: 1, other: 1, ci: 4.

**package.json — sinteză (scripturi, workspaces, dependențe — eșantion)**

- `package.json`: name=`s4-p3-monorepo` type=`None` workspaces=False
  - **Scripturi:**
  - `test` → `pnpm -r run test`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, jsdom, http-server, playwright, workbox-build
- `packages/L1-p01-esm-bootstrap/package.json`: name=`@s4/L1-p01-esm-bootstrap` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p02-dom-helpers/package.json`: name=`@s4/L1-p02-dom-helpers` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p03-delegation-click/package.json`: name=`@s4/L1-p03-delegation-click` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p04-once-passive-capture/package.json`: name=`@s4/L1-p04-once-passive-capture` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p05-custom-event-basics/package.json`: name=`@s4/L1-p05-custom-event-basics` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p06-template-clone/package.json`: name=`@s4/L1-p06-template-clone` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p07-fragment-render/package.json`: name=`@s4/L1-p07-fragment-render` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p08-dataset-attrs/package.json`: name=`@s4/L1-p08-dataset-attrs` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p09-class-toggle/package.json`: name=`@s4/L1-p09-class-toggle` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p10-form-input-sync/package.json`: name=`@s4/L1-p10-form-input-sync` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p11-aria-live/package.json`: name=`@s4/L1-p11-aria-live` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p12-keyboard-events/package.json`: name=`@s4/L1-p12-keyboard-events` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p13-target-currentTarget/package.json`: name=`@s4/L1-p13-target-currentTarget` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p14-cleanup-abort/package.json`: name=`@s4/L1-p14-cleanup-abort` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L1-p15-module-boundary/package.json`: name=`@s4/L1-p15-module-boundary` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p01-import-maps/package.json`: name=`@s4/L2-p01-import-maps` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p02-services-json/package.json`: name=`@s4/L2-p02-services-json` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p03-dynamic-import/package.json`: name=`@s4/L2-p03-dynamic-import` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p04-reexports/package.json`: name=`@s4/L2-p04-reexports` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p05-tree-shaking/package.json`: name=`@s4/L2-p05-tree-shaking` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p06-code-splitting/package.json`: name=`@s4/L2-p06-code-splitting` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p07-modulepreload-metrics/package.json`: name=`@s4/L2-p07-modulepreload-metrics` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p08-csp-scan/package.json`: name=`@s4/L2-p08-csp-scan` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p09-adapter/package.json`: name=`@s4/L2-p09-adapter` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p10-mutation-observer/package.json`: name=`@s4/L2-p10-mutation-observer` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p11-throttle-input/package.json`: name=`@s4/L2-p11-throttle-input` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p12-event-guards/package.json`: name=`@s4/L2-p12-event-guards` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p13-import-conditions-doc/package.json`: name=`@s4/L2-p13-import-conditions-doc` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p14-subpath-exports-doc/package.json`: name=`@s4/L2-p14-subpath-exports-doc` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L2-p15-esm-cjs-interop-doc/package.json`: name=`@s4/L2-p15-esm-cjs-interop-doc` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L3-p01-bus-namespaced/package.json`: name=`@s4/L3-p01-bus-namespaced` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L3-p02-timeout-signal/package.json`: name=`@s4/L3-p02-timeout-signal` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L3-p03-intersection-observer/package.json`: name=`@s4/L3-p03-intersection-observer` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L3-p04-mutation-raf-batch/package.json`: name=`@s4/L3-p04-mutation-raf-batch` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L3-p05-composed-events/package.json`: name=`@s4/L3-p05-composed-events` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L3-p06-event-replay/package.json`: name=`@s4/L3-p06-event-replay` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L3-p07-e2e-filter/package.json`: name=`@s4/L3-p07-e2e-filter` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `test:e2e` → `playwright test`
  - `serve:e2e` → `http-server -p 4173 .`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server, playwright
- `packages/L3-p08-e2e-keyboard/package.json`: name=`@s4/L3-p08-e2e-keyboard` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `test:e2e` → `playwright test`
  - `serve:e2e` → `http-server -p 4173 .`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server, playwright
- `packages/L3-p09-pwa-workbox/package.json`: name=`@s4/L3-p09-pwa-workbox` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `build:sw` → `node build-sw.mjs`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server, workbox-build
- `packages/L3-p10-e2e-offline-smoke/package.json`: name=`@s4/L3-p10-e2e-offline-smoke` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `test:e2e` → `playwright test`
  - `serve:e2e` → `http-server -p 4173 .`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server, playwright
- `packages/L3-p11-module-graph/package.json`: name=`@s4/L3-p11-module-graph` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L3-p12-feature-toggles/package.json`: name=`@s4/L3-p12-feature-toggles` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L3-p13-microfrontend-bridge/package.json`: name=`@s4/L3-p13-microfrontend-bridge` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L3-p14-perf-budget/package.json`: name=`@s4/L3-p14-perf-budget` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server
- `packages/L3-p15-ci-matrix/package.json`: name=`@s4/L3-p15-ci-matrix` type=`module` workspaces=False
  - **Scripturi:**
  - `serve` → `http-server -c-1 -p 5173 .`
  - `test:vitest` → `vitest run`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** @babel/preset-env, babel-jest, jest, jsdom, vitest, http-server

### Seminar4_p3-readmes.zip

```
L1/L1-p01-esm-bootstrap/README.md
L1/L1-p02-dom-helpers/README.md
L1/L1-p03-delegation-click/README.md
L1/L1-p04-once-passive-capture/README.md
L1/L1-p05-custom-event-basics/README.md
L1/L1-p06-template-clone/README.md
L1/L1-p07-fragment-render/README.md
L1/L1-p08-dataset-attrs/README.md
L1/L1-p09-class-toggle/README.md
L1/L1-p10-form-input-sync/README.md
L1/L1-p11-aria-live/README.md
L1/L1-p12-keyboard-events/README.md
L1/L1-p13-target-currentTarget/README.md
L1/L1-p14-cleanup-abort/README.md
L1/L1-p15-module-boundary/README.md
L2/L2-p01-import-maps/README.md
L2/L2-p02-services-json/README.md
L2/L2-p03-dynamic-import/README.md
L2/L2-p04-reexports/README.md
L2/L2-p05-tree-shaking/README.md
L2/L2-p06-code-splitting/README.md
L2/L2-p07-modulepreload-metrics/README.md
L2/L2-p08-csp-scan/README.md
L2/L2-p09-adapter/README.md
L2/L2-p10-mutation-observer/README.md
L2/L2-p11-throttle-input/README.md
L2/L2-p12-event-guards/README.md
L2/L2-p13-import-conditions-doc/README.md
L2/L2-p14-subpath-exports-doc/README.md
L2/L2-p15-esm-cjs-interop-doc/README.md
L3/L3-p01-bus-namespaced/README.md
L3/L3-p02-timeout-signal/README.md
L3/L3-p03-intersection-observer/README.md
L3/L3-p04-mutation-raf-batch/README.md
L3/L3-p05-composed-events/README.md
L3/L3-p06-event-replay/README.md
L3/L3-p07-e2e-filter/README.md
L3/L3-p08-e2e-keyboard/README.md
L3/L3-p09-pwa-workbox/README.md
L3/L3-p10-e2e-offline-smoke/README.md
L3/L3-p11-module-graph/README.md
L3/L3-p12-feature-toggles/README.md
L3/L3-p13-microfrontend-bridge/README.md
L3/L3-p14-perf-budget/README.md
L3/L3-p15-ci-matrix/README.md
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** docs: 44, pwa: 1.

## 2. Sinteza documentelor DOCX (teorie ↔ laborator ↔ proiecte)

### Seminar4_Partea1_Teorie_Modules_Events_DOM.docx

**Titluri/Heading-uri (eșantion):**

- Hook realist: „Lansăm luni dimineața”
- 1. De ce ES modules (ESM) în browser?
- 1.1. Exporturi implicite vs nominale

**Headings principale (eșantion):**

- Hook realist: „Lansăm luni dimineața”
- 1. De ce ES modules (ESM) în browser?
- 1.1. Exporturi implicite vs nominale
- 1.2. Re‑exports (agregare de module)
- 1.3. Import dinamic (`import()`) și top‑level await
- 2. Graful de module și rezoluția importurilor
- 4. DOM: arhitectură, querying, actualizare eficientă
- 5. Modelul de evenimente: delegare, opțiuni, AbortController
- 6. Securitate & integritate: CSP
- 7. Performanță & UX: modulepreload, throttle
- 8. Testabilitate: Vitest & Jest (jsdom)
- Bibliografie (APA 7, cu DOI)

### Seminar4_P2_Laborator_Detaliat.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 4 — Partea 2 (Laborator, extins): ESM, evenimente & DOM
- **Obiectiv general.** În această parte practică construim, pas cu pas, „StudentHub UI” folosind **ES modules** (ESM) nativ în browser, gestionăm **evenimente** DOM în mod robust (delegare, opțiuni, cleanup cu `AbortController`) și discutăm **dependency management** (import maps vs bundler) din perspectiva unui laborator didactic. Fiecare exercițiu are un *worksheet* (cerință + checklist), un *starter code* și o suită de **unit tests** în oglindă (**Vitest** și **Jest**) pentru a valida conceptele. Pe parcurs, indicăm *AI‑assist (VSL)* pentru accelerarea muncii: **Verify** (edge‑cases), **Specify** (contracte/semnături), **Learn** (refactor/măsurare).
- ---

### Seminar4_P2_Ghid_Arhive.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — arhive Partea 2 (Laborator)
- Acest ghid descrie conținutul și modul de utilizare pentru arhivele livrate în Partea 2 (Laborator) — varianta **Standalone (npm)** și varianta **Monorepo (PNPM workspaces)**. Include comenzi de rulare, structură de directoare și notițe de depanare.
- ---

### Seminar4_P3_Ghid_Arhive.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhive Partea 3 (Proiecte/teme)
- Acest ghid descrie conținutul și modul de utilizare al arhivelor livrate pentru Partea 3: **s4-p3-standalone.zip** și **s4-p3-monorepo.zip**. Include instrucțiuni de rulare, structură de directoare, CI, e2e și PWA/Workbox.
- ---

### Seminar4_P3_Proiecte_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 4 — Partea 3 (Proiecte/teme, extins)
- **Obiectiv.** Această parte conține 45 de proiecte (15 × L1, 15 × L2, 15 × L3) care consolidează cunoștințele despre ES modules, DOM și modelul de evenimente, cu accent pe dependency management, performanță și testabilitate. Pentru fiecare proiect sunt livrate: (a) schelet complet runnable (HTML/CSS/JS), (b) teste unitare în oglindă (Vitest/Jest), (c) README cu learning goals, (d) pentru subsetul L3: teste E2E (Playwright) și PWA (Workbox).
- ### L1 — Proiecte (15)

## 3. Monorepo vs. standalone — analiză comparativă


**Manageri de pachete & workspaces.** Monorepo (PNPM) declară `packages/*` și rulează testele matricial; standalone izolează dependențele per proiect (`npm`).

**Comenzi de instalare/testare.** Monorepo: `pnpm i -w`, `pnpm -r run test` sau `pnpm --filter <pkg> run test`. Standalone: `npm i`, `npm run test`. Suitele sunt **oglindite** (Vitest & Jest). Pentru subset L3: Playwright & Workbox.

**Integrare CI.** Monorepo include workflows separate (`unit-vitest.yml`, `unit-jest.yml`, `e2e.yml`, `workbox-sw.yml`); standalone are workflows per proiect.

**Avantaje/Dezavantaje.** Standalone — curba de învățare mai lină; Monorepo — scalare și partajare de configuri, util pentru 45 de proiecte (L1–L3). Cost: înțelegerea filtrării PNPM și a matricei CI.
## 4. Rolul fișierelor cheie (config, cod, teste, extra)

| Fișier / tip | Rol |
|---|---|
| `package.json` | Manifest: metadate, dependențe, scripturi; `type:"module"` pentru ESM. |
| `vitest.config.ts` | Configurarea Vitest (jsdom) — verifică aceleași contracte ca Jest. |
| `jest.config.cjs` | Configurarea Jest (jsdom, `babel-jest`, `extensionsToTreatAsEsm`). |
| `babel.config.cjs` | Preseturi Babel pentru Jest (`@babel/preset-env`). |
| `pnpm-workspace.yaml` | Declară pachetele unui monorepo PNPM. |
| `playwright.config.ts` | Config E2E (proiectele L3). |
| `build-sw.mjs` | Script Workbox (PWA, L3). |
| `src/main.js` | Bootstrap `bootstrap(document)`; delegare evenimente; cleanup cu `AbortController`. |
| `src/dom.js` | qs/qsa cu invariante (eșuează devreme). |
| `src/events.js` | Delegare (`on`), `listenWithSignal` pentru cleanup determinist. |
| `src/services/data.js` | Strat de servicii; `loadEvents()` normalizează `{id,title,when,club}`. |
| `src/filters.js` | Filtrare; încărcată **lazy** via `import()` (wrapper spies). |
| `public/index.html` | Conectează ESM (`<script type="module" src="/src/main.js">`), `modulepreload`, markup fără `on*=` (CSP). |

## 5. Corelații cod ↔ configurări ↔ teste


- **Rutele și fluxurile din `main.js`** (delegare, filtrare lazy, cleanup) sunt verificate în **ambele suite** (Vitest & Jest) cu `jsdom`, *mocks* pentru `fetch` și spion pe `dynamicImport`. 
- **`.env.example`** (când apare) documentează `PORT`/variabile utile; serverul de dev servește `public/` și `src/` ca rădăcină. 
- **ESLint + CI**: workflows rulează `lint` și `test`; subsetul L3 adaugă **Playwright** (E2E) și **Workbox** (PWA). 
- **CSP**: testul `csp.test.js` scanează `public/index.html` pentru a preveni `on*=`; politica este explicată în teorie. 
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S4 unifică **ES modules în browser**, **modelul de evenimente DOM** (delegare, opțiuni, cleanup) și un **strat minim de servicii** (încărcare/normalizare date), cu accent pe **dependency management** (import maps vs. bundler), **testabilitate** (Vitest & Jest în oglindă) și extensii L3 (E2E/Workbox). Mappingul teorie ↔ laborator ↔ proiecte este explicit și reproductibil (contracte de test).### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; `packages/*` + workflows |
| Instalare | `npm i` | `pnpm i -w` |
| Testare | `npm run test` (Vitest & Jest) | `pnpm -r run test` sau `--filter` |
| CI | Workflows simple per proiect | Workflows separate: Vitest, Jest, E2E, Workbox |
| Scalare (45 proiecte) | multiplicare directoare | pachete curate în `packages/*` |
| Public țintă | începători | echipe/colecții avansate |
### Inventar pe arhivă (roluri)

- **Seminar4_p2-lab-standalone.zip** — config=4, docs=1, code=8, public=3, tests=14.
- **Seminar4_p2-monorepo.zip** — config=6, docs=1, code=8, public=3, tests=14, ci=2.
- **Seminar4_p3-standalone.zip** — config=184, docs=44, public=135, code=323, tests=95, pwa=1, other=1.
- **Seminar4_p3-monorepo.zip** — config=186, docs=44, public=135, code=323, tests=95, pwa=1, other=1, ci=4.
- **Seminar4_p3-readmes.zip** — docs=44, pwa=1.
### Explicații fișier-cu-fișier

Consultați tabelul din §4; detaliile pentru E2E/PWA sunt prezente doar în subsetul L3 (pachete dedicate). 
### Corelații între fișiere


- `src/dom.js` & `src/events.js` ↔ `tests/*`: invariante, delegare, `AbortController`.  
- `src/services/data.js` ↔ `tests/*`: normalizare date, *mocks* pentru `fetch`.  
- `src/filters.js` ↔ `tests/*`: **lazy import** verificat prin spion.  
- `.github/workflows/*` ↔ `lint`/`test`/`e2e`/`workbox`: pipeline determinist pentru PR-uri.  
### Recomandări pentru studenți


1) **Bootstrap ESM** cu `script type="module"` și importuri relative (`/src/...`).  
2) **Eșuați devreme** cu `qs`/`qsa` — evitați propagarea `null`.  
3) **Delegare + cleanup**: un singur handler pe container; `AbortController` pentru teardown.  
4) **Încărcare lazy** pentru costuri amânate; documentați observabilele (ex.: *first interaction time*).  
5) **Testare în oglindă**: păstrați aceleași aserții în Vitest & Jest.  
6) **CSP igienic**: fără `on*=` în HTML; preferați addEventListener.  
### Instrucțiuni „Quick start” per arhivă (comenzi)


**Partea 2 — laborator (standalone):**
```bash
unzip "Seminar4_p2-lab-standalone.zip" -d s4p2-standalone
cd s4p2-standalone
npm i
npm run test
npm run serve   # http://localhost:5173/public/index.html
```

**Partea 2 — laborator (monorepo):**
```bash
unzip "Seminar4_p2-monorepo.zip" -d s4p2-monorepo
cd s4p2-monorepo
pnpm i -w
pnpm -r run test
pnpm -F @s4/lab-s4 run serve
```

**Partea 3 — proiecte (standalone):**
```bash
unzip "Seminar4_p3-standalone.zip" -d s4p3-standalone
cd s4p3-standalone/L1/L1-p01-esm-bootstrap
npm i
npm run test
npm run serve
```

**Partea 3 — proiecte (monorepo):**
```bash
unzip "Seminar4_p3-monorepo.zip" -d s4p3-monorepo
cd s4p3-monorepo
pnpm i -w
pnpm -r run test                 # unit (Vitest & Jest)
pnpm -F @s4/L3-p07-e2e-filter run test:e2e
pnpm -F @s4/L3-p09-pwa-workbox run build:sw
```

**Partea 3 — README-uri agregate:**
```bash
unzip "Seminar4_p3-readmes.zip" -d s4p3-readmes
ls s4p3-readmes | head -n 10
```
### Troubleshooting (erori frecvente)


- **ESM + Jest**: folosiți `babel-jest` + `extensionsToTreatAsEsm`.  
- **Căi HTML → module**: încărcați modulele cu rute absolute relative la server (`/src/...`).  
- **`fetch` în teste**: *mock* în ambele suite; nu depindeți de rețea.  
- **Playwright în CI**: rulați `npx playwright install --with-deps` înainte de `test:e2e`.  
- **Workbox**: rulați `node build-sw.mjs` înainte de a testa `sw.js`.  
- **PNPM filter**: verificați `pnpm-workspace.yaml` (nume pachete) și `name` în `package.json`.  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie)** — ESM, graful de module, import dinamic, DOM helpers, delegare, CSP, `modulepreload`.  
- **Partea 2 (Laborator + Ghid arhive)** — „StudentHub UI” pas cu pas: bootstrap ESM, delegare, cleanup, servicii date, lazy import, modulepreload; suite în oglindă Vitest & Jest.  
- **Partea 3 (Ghid + Proiecte)** — 45 de proiecte L1–L3, subset L3 cu E2E (Playwright) și PWA (Workbox), CI la scară.  
### Prompt‑șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S4** (standalone & monorepo) o aplicație **ESM în browser** cu `bootstrap(document)`, `qs/qsa` cu invariante, **delegare** și cleanup cu `AbortController`, strat `services/data.js` cu normalizare, **lazy import** la primul input, `modulepreload`, **teste în oglindă** (Vitest & Jest), CI, README cu Quick start & Troubleshooting, plus proiecte L3 cu **Playwright** și **Workbox**.”
