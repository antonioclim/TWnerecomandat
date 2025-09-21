# Seminarul S3 — Obiecte, erori, memoization, async/await — Analiză integrată (standalone & monorepo)

*Generat la 2025-09-21 10:14.*

## 1. Inventarul arhivelor ZIP și structura completă

### Seminar3_Partea2_lab-standalone-v2.zip

```
.gitignore
README.md
babel.config.cjs
jest.config.cjs
package.json
src/entities.js
src/errors.js
src/services/concurrency.js
src/services/directory.js
src/services/memo.js
src/services/report.js
tests/jest/async.jest.test.js
tests/jest/entities.jest.test.js
tests/vitest/async.test.js
tests/vitest/entities.test.js
tests/vitest/memo-ttl.test.js
tests/vitest/memo.test.js
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 5, docs: 1, code: 6, tests: 6.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s3-lab` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env

### Seminar3_Partea2_lab-monorepo-v2.zip

```
.gitignore
babel.config.cjs
jest.config.cjs
package.json
packages/core/README.md
packages/core/package.json
packages/core/src/entities.js
packages/core/src/errors.js
packages/core/src/services/concurrency.js
packages/core/src/services/directory.js
packages/core/src/services/memo.js
packages/core/src/services/report.js
packages/core/tests/jest/async.jest.test.js
packages/core/tests/jest/entities.jest.test.js
packages/core/tests/vitest/async.test.js
packages/core/tests/vitest/entities.test.js
packages/core/tests/vitest/memo-ttl.test.js
packages/core/tests/vitest/memo.test.js
pnpm-workspace.yaml
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 7, docs: 1, code: 6, tests: 6.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s3-lab-monorepo-v2` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `pnpm -r --filter './packages/*' exec vitest run --reporter verbose`
  - `test:jest` → `pnpm -r --filter './packages/*' exec jest --runInBand`
  - `test` → `pnpm run test:vitest && pnpm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `packages/core/package.json`: name=`@s3/core` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`

### Seminar3_Partea3_p3-standalone.zip

```
L1/L1-p01-student-vo/.gitignore
L1/L1-p01-student-vo/README.md
L1/L1-p01-student-vo/babel.config.cjs
L1/L1-p01-student-vo/jest.config.cjs
L1/L1-p01-student-vo/package.json
L1/L1-p01-student-vo/src/index.js
L1/L1-p01-student-vo/tests/jest/spec.jest.test.js
L1/L1-p01-student-vo/tests/vitest/spec.test.js
L1/L1-p01-student-vo/vitest.config.ts
L1/L1-p02-club-vo/.gitignore
L1/L1-p02-club-vo/README.md
L1/L1-p02-club-vo/babel.config.cjs
L1/L1-p02-club-vo/jest.config.cjs
L1/L1-p02-club-vo/package.json
L1/L1-p02-club-vo/src/index.js
L1/L1-p02-club-vo/tests/jest/spec.jest.test.js
L1/L1-p02-club-vo/tests/vitest/spec.test.js
L1/L1-p02-club-vo/vitest.config.ts
L1/L1-p03-event-vo/.gitignore
L1/L1-p03-event-vo/README.md
L1/L1-p03-event-vo/babel.config.cjs
L1/L1-p03-event-vo/jest.config.cjs
L1/L1-p03-event-vo/package.json
L1/L1-p03-event-vo/src/index.js
L1/L1-p03-event-vo/tests/jest/spec.jest.test.js
L1/L1-p03-event-vo/tests/vitest/spec.test.js
L1/L1-p03-event-vo/vitest.config.ts
L1/L1-p04-factory-student/.gitignore
L1/L1-p04-factory-student/README.md
L1/L1-p04-factory-student/babel.config.cjs
L1/L1-p04-factory-student/jest.config.cjs
L1/L1-p04-factory-student/package.json
L1/L1-p04-factory-student/src/index.js
L1/L1-p04-factory-student/tests/jest/spec.jest.test.js
L1/L1-p04-factory-student/tests/vitest/spec.test.js
L1/L1-p04-factory-student/vitest.config.ts
L1/L1-p05-descriptor-secret/.gitignore
L1/L1-p05-descriptor-secret/README.md
L1/L1-p05-descriptor-secret/babel.config.cjs
L1/L1-p05-descriptor-secret/jest.config.cjs
L1/L1-p05-descriptor-secret/package.json
L1/L1-p05-descriptor-secret/src/index.js
L1/L1-p05-descriptor-secret/tests/jest/spec.jest.test.js
L1/L1-p05-descriptor-secret/tests/vitest/spec.test.js
L1/L1-p05-descriptor-secret/vitest.config.ts
L1/L1-p06-branding-tag/.gitignore
L1/L1-p06-branding-tag/README.md
L1/L1-p06-branding-tag/babel.config.cjs
L1/L1-p06-branding-tag/jest.config.cjs
L1/L1-p06-branding-tag/package.json
L1/L1-p06-branding-tag/src/index.js
L1/L1-p06-branding-tag/tests/jest/spec.jest.test.js
L1/L1-p06-branding-tag/tests/vitest/spec.test.js
L1/L1-p06-branding-tag/vitest.config.ts
L1/L1-p07-catalog-iterable/.gitignore
L1/L1-p07-catalog-iterable/README.md
L1/L1-p07-catalog-iterable/babel.config.cjs
L1/L1-p07-catalog-iterable/jest.config.cjs
L1/L1-p07-catalog-iterable/package.json
L1/L1-p07-catalog-iterable/src/index.js
L1/L1-p07-catalog-iterable/tests/jest/spec.jest.test.js
L1/L1-p07-catalog-iterable/tests/vitest/spec.test.js
L1/L1-p07-catalog-iterable/vitest.config.ts
L1/L1-p08-equals-by/.gitignore
L1/L1-p08-equals-by/README.md
L1/L1-p08-equals-by/babel.config.cjs
L1/L1-p08-equals-by/jest.config.cjs
L1/L1-p08-equals-by/package.json
L1/L1-p08-equals-by/src/index.js
L1/L1-p08-equals-by/tests/jest/spec.jest.test.js
L1/L1-p08-equals-by/tests/vitest/spec.test.js
L1/L1-p08-equals-by/vitest.config.ts
L1/L1-p09-key-by-email/.gitignore
L1/L1-p09-key-by-email/README.md
L1/L1-p09-key-by-email/babel.config.cjs
L1/L1-p09-key-by-email/jest.config.cjs
L1/L1-p09-key-by-email/package.json
L1/L1-p09-key-by-email/src/index.js
L1/L1-p09-key-by-email/tests/jest/spec.jest.test.js
L1/L1-p09-key-by-email/tests/vitest/spec.test.js
L1/L1-p09-key-by-email/vitest.config.ts
L1/L1-p10-find-or-throw/.gitignore
L1/L1-p10-find-or-throw/README.md
L1/L1-p10-find-or-throw/babel.config.cjs
L1/L1-p10-find-or-throw/jest.config.cjs
L1/L1-p10-find-or-throw/package.json
L1/L1-p10-find-or-throw/src/index.js
L1/L1-p10-find-or-throw/tests/jest/spec.jest.test.js
L1/L1-p10-find-or-throw/tests/vitest/spec.test.js
L1/L1-p10-find-or-throw/vitest.config.ts
L1/L1-p11-validation-report/.gitignore
L1/L1-p11-validation-report/README.md
L1/L1-p11-validation-report/babel.config.cjs
L1/L1-p11-validation-report/jest.config.cjs
L1/L1-p11-validation-report/package.json
L1/L1-p11-validation-report/src/index.js
L1/L1-p11-validation-report/tests/jest/spec.jest.test.js
L1/L1-p11-validation-report/tests/vitest/spec.test.js
L1/L1-p11-validation-report/vitest.config.ts
L1/L1-p12-mixins/.gitignore
L1/L1-p12-mixins/README.md
L1/L1-p12-mixins/babel.config.cjs
L1/L1-p12-mixins/jest.config.cjs
L1/L1-p12-mixins/package.json
L1/L1-p12-mixins/src/index.js
L1/L1-p12-mixins/tests/jest/spec.jest.test.js
L1/L1-p12-mixins/tests/vitest/spec.test.js
L1/L1-p12-mixins/vitest.config.ts
L1/L1-p13-brand-id/.gitignore
L1/L1-p13-brand-id/README.md
L1/L1-p13-brand-id/babel.config.cjs
L1/L1-p13-brand-id/jest.config.cjs
L1/L1-p13-brand-id/package.json
L1/L1-p13-brand-id/src/index.js
L1/L1-p13-brand-id/tests/jest/spec.jest.test.js
L1/L1-p13-brand-id/tests/vitest/spec.test.js
L1/L1-p13-brand-id/vitest.config.ts
L1/L1-p14-clone-shallow/.gitignore
L1/L1-p14-clone-shallow/README.md
L1/L1-p14-clone-shallow/babel.config.cjs
L1/L1-p14-clone-shallow/jest.config.cjs
L1/L1-p14-clone-shallow/package.json
L1/L1-p14-clone-shallow/src/index.js
L1/L1-p14-clone-shallow/tests/jest/spec.jest.test.js
L1/L1-p14-clone-shallow/tests/vitest/spec.test.js
L1/L1-p14-clone-shallow/vitest.config.ts
L1/L1-p15-memoize-basic/.gitignore
L1/L1-p15-memoize-basic/README.md
L1/L1-p15-memoize-basic/babel.config.cjs
L1/L1-p15-memoize-basic/jest.config.cjs
L1/L1-p15-memoize-basic/package.json
L1/L1-p15-memoize-basic/src/index.js
L1/L1-p15-memoize-basic/tests/jest/spec.jest.test.js
L1/L1-p15-memoize-basic/tests/vitest/spec.test.js
L1/L1-p15-memoize-basic/vitest.config.ts
L2/L2-p01-catalog-repo/.gitignore
L2/L2-p01-catalog-repo/README.md
L2/L2-p01-catalog-repo/babel.config.cjs
L2/L2-p01-catalog-repo/jest.config.cjs
L2/L2-p01-catalog-repo/package.json
L2/L2-p01-catalog-repo/src/index.js
L2/L2-p01-catalog-repo/tests/jest/spec.jest.test.js
L2/L2-p01-catalog-repo/tests/vitest/spec.test.js
L2/L2-p01-catalog-repo/vitest.config.ts
L2/L2-p02-memoize-weak/.gitignore
L2/L2-p02-memoize-weak/README.md
L2/L2-p02-memoize-weak/babel.config.cjs
L2/L2-p02-memoize-weak/jest.config.cjs
L2/L2-p02-memoize-weak/package.json
L2/L2-p02-memoize-weak/src/index.js
L2/L2-p02-memoize-weak/tests/jest/spec.jest.test.js
L2/L2-p02-memoize-weak/tests/vitest/spec.test.js
L2/L2-p02-memoize-weak/vitest.config.ts
L2/L2-p03-errors-cause/.gitignore
L2/L2-p03-errors-cause/README.md
L2/L2-p03-errors-cause/babel.config.cjs
L2/L2-p03-errors-cause/jest.config.cjs
L2/L2-p03-errors-cause/package.json
L2/L2-p03-errors-cause/src/index.js
L2/L2-p03-errors-cause/tests/jest/spec.jest.test.js
L2/L2-p03-errors-cause/tests/vitest/spec.test.js
L2/L2-p03-errors-cause/vitest.config.ts
L2/L2-p04-directory-allsettled/.gitignore
L2/L2-p04-directory-allsettled/README.md
L2/L2-p04-directory-allsettled/babel.config.cjs
L2/L2-p04-directory-allsettled/jest.config.cjs
L2/L2-p04-directory-allsettled/package.json
L2/L2-p04-directory-allsettled/src/index.js
L2/L2-p04-directory-allsettled/tests/jest/spec.jest.test.js
L2/L2-p04-directory-allsettled/tests/vitest/spec.test.js
L2/L2-p04-directory-allsettled/vitest.config.ts
L2/L2-p05-report-topk/.gitignore
L2/L2-p05-report-topk/README.md
L2/L2-p05-report-topk/babel.config.cjs
L2/L2-p05-report-topk/jest.config.cjs
L2/L2-p05-report-topk/package.json
L2/L2-p05-report-topk/src/index.js
L2/L2-p05-report-topk/tests/jest/spec.jest.test.js
L2/L2-p05-report-topk/tests/vitest/spec.test.js
L2/L2-p05-report-topk/vitest.config.ts
L2/L2-p06-adapter-dto/.gitignore
L2/L2-p06-adapter-dto/README.md
L2/L2-p06-adapter-dto/babel.config.cjs
L2/L2-p06-adapter-dto/jest.config.cjs
L2/L2-p06-adapter-dto/package.json
L2/L2-p06-adapter-dto/src/index.js
L2/L2-p06-adapter-dto/tests/jest/spec.jest.test.js
L2/L2-p06-adapter-dto/tests/vitest/spec.test.js
L2/L2-p06-adapter-dto/vitest.config.ts
L2/L2-p07-async-iterator/.gitignore
L2/L2-p07-async-iterator/README.md
L2/L2-p07-async-iterator/babel.config.cjs
L2/L2-p07-async-iterator/jest.config.cjs
L2/L2-p07-async-iterator/package.json
L2/L2-p07-async-iterator/src/index.js
L2/L2-p07-async-iterator/tests/jest/spec.jest.test.js
L2/L2-p07-async-iterator/tests/vitest/spec.test.js
L2/L2-p07-async-iterator/vitest.config.ts
L2/L2-p08-decorator-logger/.gitignore
L2/L2-p08-decorator-logger/README.md
L2/L2-p08-decorator-logger/babel.config.cjs
L2/L2-p08-decorator-logger/jest.config.cjs
L2/L2-p08-decorator-logger/package.json
L2/L2-p08-decorator-logger/src/index.js
L2/L2-p08-decorator-logger/tests/jest/spec.jest.test.js
L2/L2-p08-decorator-logger/tests/vitest/spec.test.js
L2/L2-p08-decorator-logger/vitest.config.ts
L2/L2-p09-idempotent-add/.gitignore
L2/L2-p09-idempotent-add/README.md
L2/L2-p09-idempotent-add/babel.config.cjs
L2/L2-p09-idempotent-add/jest.config.cjs
L2/L2-p09-idempotent-add/package.json
L2/L2-p09-idempotent-add/src/index.js
L2/L2-p09-idempotent-add/tests/jest/spec.jest.test.js
L2/L2-p09-idempotent-add/tests/vitest/spec.test.js
L2/L2-p09-idempotent-add/vitest.config.ts
L2/L2-p10-schema-check/.gitignore
L2/L2-p10-schema-check/README.md
L2/L2-p10-schema-check/babel.config.cjs
L2/L2-p10-schema-check/jest.config.cjs
L2/L2-p10-schema-check/package.json
L2/L2-p10-schema-check/src/index.js
L2/L2-p10-schema-check/tests/jest/spec.jest.test.js
L2/L2-p10-schema-check/tests/vitest/spec.test.js
L2/L2-p10-schema-check/vitest.config.ts
L2/L2-p11-compose-pipeline/.gitignore
L2/L2-p11-compose-pipeline/README.md
L2/L2-p11-compose-pipeline/babel.config.cjs
L2/L2-p11-compose-pipeline/jest.config.cjs
L2/L2-p11-compose-pipeline/package.json
L2/L2-p11-compose-pipeline/src/index.js
L2/L2-p11-compose-pipeline/tests/jest/spec.jest.test.js
L2/L2-p11-compose-pipeline/tests/vitest/spec.test.js
L2/L2-p11-compose-pipeline/vitest.config.ts
L2/L2-p12-hasinstance/.gitignore
L2/L2-p12-hasinstance/README.md
L2/L2-p12-hasinstance/babel.config.cjs
L2/L2-p12-hasinstance/jest.config.cjs
L2/L2-p12-hasinstance/package.json
L2/L2-p12-hasinstance/src/index.js
L2/L2-p12-hasinstance/tests/jest/spec.jest.test.js
L2/L2-p12-hasinstance/tests/vitest/spec.test.js
L2/L2-p12-hasinstance/vitest.config.ts
L2/L2-p13-collator-sort/.gitignore
L2/L2-p13-collator-sort/README.md
L2/L2-p13-collator-sort/babel.config.cjs
L2/L2-p13-collator-sort/jest.config.cjs
L2/L2-p13-collator-sort/package.json
L2/L2-p13-collator-sort/src/index.js
L2/L2-p13-collator-sort/tests/jest/spec.jest.test.js
L2/L2-p13-collator-sort/tests/vitest/spec.test.js
L2/L2-p13-collator-sort/vitest.config.ts
L2/L2-p14-deep-freeze/.gitignore
L2/L2-p14-deep-freeze/README.md
L2/L2-p14-deep-freeze/babel.config.cjs
L2/L2-p14-deep-freeze/jest.config.cjs
L2/L2-p14-deep-freeze/package.json
L2/L2-p14-deep-freeze/src/index.js
L2/L2-p14-deep-freeze/tests/jest/spec.jest.test.js
L2/L2-p14-deep-freeze/tests/vitest/spec.test.js
L2/L2-p14-deep-freeze/vitest.config.ts
L2/L2-p15-memo-ttl/.gitignore
L2/L2-p15-memo-ttl/README.md
L2/L2-p15-memo-ttl/babel.config.cjs
L2/L2-p15-memo-ttl/jest.config.cjs
L2/L2-p15-memo-ttl/package.json
L2/L2-p15-memo-ttl/src/index.js
L2/L2-p15-memo-ttl/tests/jest/spec.jest.test.js
L2/L2-p15-memo-ttl/tests/vitest/spec.test.js
L2/L2-p15-memo-ttl/vitest.config.ts
L3/L3-p01-retry-backoff/.gitignore
L3/L3-p01-retry-backoff/README.md
L3/L3-p01-retry-backoff/babel.config.cjs
L3/L3-p01-retry-backoff/jest.config.cjs
L3/L3-p01-retry-backoff/package.json
L3/L3-p01-retry-backoff/src/index.js
L3/L3-p01-retry-backoff/tests/jest/spec.jest.test.js
L3/L3-p01-retry-backoff/tests/vitest/spec.test.js
L3/L3-p01-retry-backoff/vitest.config.ts
L3/L3-p02-timeout/.gitignore
L3/L3-p02-timeout/README.md
L3/L3-p02-timeout/babel.config.cjs
L3/L3-p02-timeout/jest.config.cjs
L3/L3-p02-timeout/package.json
L3/L3-p02-timeout/src/index.js
L3/L3-p02-timeout/tests/jest/spec.jest.test.js
L3/L3-p02-timeout/tests/vitest/spec.test.js
L3/L3-p02-timeout/vitest.config.ts
L3/L3-p03-semaphore/.gitignore
L3/L3-p03-semaphore/README.md
L3/L3-p03-semaphore/babel.config.cjs
L3/L3-p03-semaphore/jest.config.cjs
L3/L3-p03-semaphore/package.json
L3/L3-p03-semaphore/src/index.js
L3/L3-p03-semaphore/tests/jest/spec.jest.test.js
L3/L3-p03-semaphore/tests/vitest/spec.test.js
L3/L3-p03-semaphore/vitest.config.ts
L3/L3-p04-abort/.gitignore
L3/L3-p04-abort/README.md
L3/L3-p04-abort/babel.config.cjs
L3/L3-p04-abort/jest.config.cjs
L3/L3-p04-abort/package.json
L3/L3-p04-abort/src/index.js
L3/L3-p04-abort/tests/jest/spec.jest.test.js
L3/L3-p04-abort/tests/vitest/spec.test.js
L3/L3-p04-abort/vitest.config.ts
L3/L3-p05-circuit-breaker/.gitignore
L3/L3-p05-circuit-breaker/README.md
L3/L3-p05-circuit-breaker/babel.config.cjs
L3/L3-p05-circuit-breaker/jest.config.cjs
L3/L3-p05-circuit-breaker/package.json
L3/L3-p05-circuit-breaker/src/index.js
L3/L3-p05-circuit-breaker/tests/jest/spec.jest.test.js
L3/L3-p05-circuit-breaker/tests/vitest/spec.test.js
L3/L3-p05-circuit-breaker/vitest.config.ts
L3/L3-p06-async-pipeline/.gitignore
L3/L3-p06-async-pipeline/README.md
L3/L3-p06-async-pipeline/babel.config.cjs
L3/L3-p06-async-pipeline/jest.config.cjs
L3/L3-p06-async-pipeline/package.json
L3/L3-p06-async-pipeline/src/index.js
L3/L3-p06-async-pipeline/tests/jest/spec.jest.test.js
L3/L3-p06-async-pipeline/tests/vitest/spec.test.js
L3/L3-p06-async-pipeline/vitest.config.ts
L3/L3-p07-e2e-site/.gitignore
L3/L3-p07-e2e-site/README.md
L3/L3-p07-e2e-site/babel.config.cjs
L3/L3-p07-e2e-site/jest.config.cjs
L3/L3-p07-e2e-site/package.json
L3/L3-p07-e2e-site/public/index.html
L3/L3-p07-e2e-site/server.js
L3/L3-p07-e2e-site/src/index.js
L3/L3-p07-e2e-site/tests/e2e.spec.ts
L3/L3-p07-e2e-site/vitest.config.ts
L3/L3-p08-pwa-workbox/.gitignore
L3/L3-p08-pwa-workbox/README.md
L3/L3-p08-pwa-workbox/babel.config.cjs
L3/L3-p08-pwa-workbox/build-sw.mjs
L3/L3-p08-pwa-workbox/jest.config.cjs
L3/L3-p08-pwa-workbox/package.json
L3/L3-p08-pwa-workbox/public/index.html
L3/L3-p08-pwa-workbox/src/index.js
L3/L3-p08-pwa-workbox/tests/pwa.spec.ts
L3/L3-p08-pwa-workbox/vitest.config.ts
L3/L3-p09-stable-hash/.gitignore
L3/L3-p09-stable-hash/README.md
L3/L3-p09-stable-hash/babel.config.cjs
L3/L3-p09-stable-hash/jest.config.cjs
L3/L3-p09-stable-hash/package.json
L3/L3-p09-stable-hash/src/index.js
L3/L3-p09-stable-hash/tests/jest/spec.jest.test.js
L3/L3-p09-stable-hash/tests/vitest/spec.test.js
L3/L3-p09-stable-hash/vitest.config.ts
L3/L3-p10-plugins/.gitignore
L3/L3-p10-plugins/README.md
L3/L3-p10-plugins/babel.config.cjs
L3/L3-p10-plugins/jest.config.cjs
L3/L3-p10-plugins/package.json
L3/L3-p10-plugins/src/index.js
L3/L3-p10-plugins/tests/jest/spec.jest.test.js
L3/L3-p10-plugins/tests/vitest/spec.test.js
L3/L3-p10-plugins/vitest.config.ts
L3/L3-p11-fault-injection/.gitignore
L3/L3-p11-fault-injection/README.md
L3/L3-p11-fault-injection/babel.config.cjs
L3/L3-p11-fault-injection/jest.config.cjs
L3/L3-p11-fault-injection/package.json
L3/L3-p11-fault-injection/src/index.js
L3/L3-p11-fault-injection/tests/jest/spec.jest.test.js
L3/L3-p11-fault-injection/tests/vitest/spec.test.js
L3/L3-p11-fault-injection/vitest.config.ts
L3/L3-p12-randomized-tests/.gitignore
L3/L3-p12-randomized-tests/README.md
L3/L3-p12-randomized-tests/babel.config.cjs
L3/L3-p12-randomized-tests/jest.config.cjs
L3/L3-p12-randomized-tests/package.json
L3/L3-p12-randomized-tests/src/index.js
L3/L3-p12-randomized-tests/tests/jest/spec.jest.test.js
L3/L3-p12-randomized-tests/tests/vitest/spec.test.js
L3/L3-p12-randomized-tests/vitest.config.ts
L3/L3-p13-async-queue/.gitignore
L3/L3-p13-async-queue/README.md
L3/L3-p13-async-queue/babel.config.cjs
L3/L3-p13-async-queue/jest.config.cjs
L3/L3-p13-async-queue/package.json
L3/L3-p13-async-queue/src/index.js
L3/L3-p13-async-queue/tests/jest/spec.jest.test.js
L3/L3-p13-async-queue/tests/vitest/spec.test.js
L3/L3-p13-async-queue/vitest.config.ts
L3/L3-p14-e2e-table/.gitignore
L3/L3-p14-e2e-table/README.md
L3/L3-p14-e2e-table/babel.config.cjs
L3/L3-p14-e2e-table/jest.config.cjs
L3/L3-p14-e2e-table/package.json
L3/L3-p14-e2e-table/public/index.html
L3/L3-p14-e2e-table/server.js
L3/L3-p14-e2e-table/src/index.js
L3/L3-p14-e2e-table/tests/e2e.spec.ts
L3/L3-p14-e2e-table/vitest.config.ts
L3/L3-p15-e2e-form/.gitignore
L3/L3-p15-e2e-form/README.md
L3/L3-p15-e2e-form/babel.config.cjs
L3/L3-p15-e2e-form/jest.config.cjs
L3/L3-p15-e2e-form/package.json
L3/L3-p15-e2e-form/public/index.html
L3/L3-p15-e2e-form/server.js
L3/L3-p15-e2e-form/src/index.js
L3/L3-p15-e2e-form/tests/e2e.spec.ts
L3/L3-p15-e2e-form/vitest.config.ts
README.md
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** docs: 45, config: 225, code: 45, tests: 86, other: 3, public: 4, pwa: 2.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `L1/L1-p01-student-vo/package.json`: name=`L1-p01-student-vo` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p02-club-vo/package.json`: name=`L1-p02-club-vo` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p03-event-vo/package.json`: name=`L1-p03-event-vo` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p04-factory-student/package.json`: name=`L1-p04-factory-student` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p05-descriptor-secret/package.json`: name=`L1-p05-descriptor-secret` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p06-branding-tag/package.json`: name=`L1-p06-branding-tag` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p07-catalog-iterable/package.json`: name=`L1-p07-catalog-iterable` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p08-equals-by/package.json`: name=`L1-p08-equals-by` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p09-key-by-email/package.json`: name=`L1-p09-key-by-email` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p10-find-or-throw/package.json`: name=`L1-p10-find-or-throw` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p11-validation-report/package.json`: name=`L1-p11-validation-report` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p12-mixins/package.json`: name=`L1-p12-mixins` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p13-brand-id/package.json`: name=`L1-p13-brand-id` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p14-clone-shallow/package.json`: name=`L1-p14-clone-shallow` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L1/L1-p15-memoize-basic/package.json`: name=`L1-p15-memoize-basic` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p01-catalog-repo/package.json`: name=`L2-p01-catalog-repo` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p02-memoize-weak/package.json`: name=`L2-p02-memoize-weak` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p03-errors-cause/package.json`: name=`L2-p03-errors-cause` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p04-directory-allsettled/package.json`: name=`L2-p04-directory-allsettled` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p05-report-topk/package.json`: name=`L2-p05-report-topk` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p06-adapter-dto/package.json`: name=`L2-p06-adapter-dto` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p07-async-iterator/package.json`: name=`L2-p07-async-iterator` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p08-decorator-logger/package.json`: name=`L2-p08-decorator-logger` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p09-idempotent-add/package.json`: name=`L2-p09-idempotent-add` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p10-schema-check/package.json`: name=`L2-p10-schema-check` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p11-compose-pipeline/package.json`: name=`L2-p11-compose-pipeline` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p12-hasinstance/package.json`: name=`L2-p12-hasinstance` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p13-collator-sort/package.json`: name=`L2-p13-collator-sort` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p14-deep-freeze/package.json`: name=`L2-p14-deep-freeze` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L2/L2-p15-memo-ttl/package.json`: name=`L2-p15-memo-ttl` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p01-retry-backoff/package.json`: name=`L3-p01-retry-backoff` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p02-timeout/package.json`: name=`L3-p02-timeout` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p03-semaphore/package.json`: name=`L3-p03-semaphore` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p04-abort/package.json`: name=`L3-p04-abort` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p05-circuit-breaker/package.json`: name=`L3-p05-circuit-breaker` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p06-async-pipeline/package.json`: name=`L3-p06-async-pipeline` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p07-e2e-site/package.json`: name=`L3-p07-e2e-site` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `test:e2e` → `playwright test`
  - `serve` → `node server.js`
  - **Deps:** express
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, @playwright/test
- `L3/L3-p08-pwa-workbox/package.json`: name=`L3-p08-pwa-workbox` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `build:sw` → `node build-sw.mjs`
  - `test:e2e` → `playwright test`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, workbox-build, @playwright/test
- `L3/L3-p09-stable-hash/package.json`: name=`L3-p09-stable-hash` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p10-plugins/package.json`: name=`L3-p10-plugins` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p11-fault-injection/package.json`: name=`L3-p11-fault-injection` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p12-randomized-tests/package.json`: name=`L3-p12-randomized-tests` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p13-async-queue/package.json`: name=`L3-p13-async-queue` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env
- `L3/L3-p14-e2e-table/package.json`: name=`L3-p14-e2e-table` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `test:e2e` → `playwright test`
  - `serve` → `node server.js`
  - **Deps:** express
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, @playwright/test
- `L3/L3-p15-e2e-form/package.json`: name=`L3-p15-e2e-form` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `test` → `npm run test:vitest && npm run test:jest`
  - `test:e2e` → `playwright test`
  - `serve` → `node server.js`
  - **Deps:** express
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, @playwright/test

### Seminar3_Partea3_p3-monorepo.zip

```
.github/workflows/e2e.yml
.github/workflows/unit-jest.yml
.github/workflows/unit-vitest.yml
.github/workflows/workbox-sw.yml
.gitignore
README.md
babel.config.cjs
jest.config.cjs
package.json
packages/L1-p01-student-vo/README.md
packages/L1-p01-student-vo/babel.config.cjs
packages/L1-p01-student-vo/jest.config.cjs
packages/L1-p01-student-vo/package.json
packages/L1-p01-student-vo/src/index.js
packages/L1-p01-student-vo/tests/jest/spec.jest.test.js
packages/L1-p01-student-vo/tests/vitest/spec.test.js
packages/L1-p01-student-vo/vitest.config.ts
packages/L1-p02-club-vo/README.md
packages/L1-p02-club-vo/babel.config.cjs
packages/L1-p02-club-vo/jest.config.cjs
packages/L1-p02-club-vo/package.json
packages/L1-p02-club-vo/src/index.js
packages/L1-p02-club-vo/tests/jest/spec.jest.test.js
packages/L1-p02-club-vo/tests/vitest/spec.test.js
packages/L1-p02-club-vo/vitest.config.ts
packages/L1-p03-event-vo/README.md
packages/L1-p03-event-vo/babel.config.cjs
packages/L1-p03-event-vo/jest.config.cjs
packages/L1-p03-event-vo/package.json
packages/L1-p03-event-vo/src/index.js
packages/L1-p03-event-vo/tests/jest/spec.jest.test.js
packages/L1-p03-event-vo/tests/vitest/spec.test.js
packages/L1-p03-event-vo/vitest.config.ts
packages/L1-p04-factory-student/README.md
packages/L1-p04-factory-student/babel.config.cjs
packages/L1-p04-factory-student/jest.config.cjs
packages/L1-p04-factory-student/package.json
packages/L1-p04-factory-student/src/index.js
packages/L1-p04-factory-student/tests/jest/spec.jest.test.js
packages/L1-p04-factory-student/tests/vitest/spec.test.js
packages/L1-p04-factory-student/vitest.config.ts
packages/L1-p05-descriptor-secret/README.md
packages/L1-p05-descriptor-secret/babel.config.cjs
packages/L1-p05-descriptor-secret/jest.config.cjs
packages/L1-p05-descriptor-secret/package.json
packages/L1-p05-descriptor-secret/src/index.js
packages/L1-p05-descriptor-secret/tests/jest/spec.jest.test.js
packages/L1-p05-descriptor-secret/tests/vitest/spec.test.js
packages/L1-p05-descriptor-secret/vitest.config.ts
packages/L1-p06-branding-tag/README.md
packages/L1-p06-branding-tag/babel.config.cjs
packages/L1-p06-branding-tag/jest.config.cjs
packages/L1-p06-branding-tag/package.json
packages/L1-p06-branding-tag/src/index.js
packages/L1-p06-branding-tag/tests/jest/spec.jest.test.js
packages/L1-p06-branding-tag/tests/vitest/spec.test.js
packages/L1-p06-branding-tag/vitest.config.ts
packages/L1-p07-catalog-iterable/README.md
packages/L1-p07-catalog-iterable/babel.config.cjs
packages/L1-p07-catalog-iterable/jest.config.cjs
packages/L1-p07-catalog-iterable/package.json
packages/L1-p07-catalog-iterable/src/index.js
packages/L1-p07-catalog-iterable/tests/jest/spec.jest.test.js
packages/L1-p07-catalog-iterable/tests/vitest/spec.test.js
packages/L1-p07-catalog-iterable/vitest.config.ts
packages/L1-p08-equals-by/README.md
packages/L1-p08-equals-by/babel.config.cjs
packages/L1-p08-equals-by/jest.config.cjs
packages/L1-p08-equals-by/package.json
packages/L1-p08-equals-by/src/index.js
packages/L1-p08-equals-by/tests/jest/spec.jest.test.js
packages/L1-p08-equals-by/tests/vitest/spec.test.js
packages/L1-p08-equals-by/vitest.config.ts
packages/L1-p09-key-by-email/README.md
packages/L1-p09-key-by-email/babel.config.cjs
packages/L1-p09-key-by-email/jest.config.cjs
packages/L1-p09-key-by-email/package.json
packages/L1-p09-key-by-email/src/index.js
packages/L1-p09-key-by-email/tests/jest/spec.jest.test.js
packages/L1-p09-key-by-email/tests/vitest/spec.test.js
packages/L1-p09-key-by-email/vitest.config.ts
packages/L1-p10-find-or-throw/README.md
packages/L1-p10-find-or-throw/babel.config.cjs
packages/L1-p10-find-or-throw/jest.config.cjs
packages/L1-p10-find-or-throw/package.json
packages/L1-p10-find-or-throw/src/index.js
packages/L1-p10-find-or-throw/tests/jest/spec.jest.test.js
packages/L1-p10-find-or-throw/tests/vitest/spec.test.js
packages/L1-p10-find-or-throw/vitest.config.ts
packages/L1-p11-validation-report/README.md
packages/L1-p11-validation-report/babel.config.cjs
packages/L1-p11-validation-report/jest.config.cjs
packages/L1-p11-validation-report/package.json
packages/L1-p11-validation-report/src/index.js
packages/L1-p11-validation-report/tests/jest/spec.jest.test.js
packages/L1-p11-validation-report/tests/vitest/spec.test.js
packages/L1-p11-validation-report/vitest.config.ts
packages/L1-p12-mixins/README.md
packages/L1-p12-mixins/babel.config.cjs
packages/L1-p12-mixins/jest.config.cjs
packages/L1-p12-mixins/package.json
packages/L1-p12-mixins/src/index.js
packages/L1-p12-mixins/tests/jest/spec.jest.test.js
packages/L1-p12-mixins/tests/vitest/spec.test.js
packages/L1-p12-mixins/vitest.config.ts
packages/L1-p13-brand-id/README.md
packages/L1-p13-brand-id/babel.config.cjs
packages/L1-p13-brand-id/jest.config.cjs
packages/L1-p13-brand-id/package.json
packages/L1-p13-brand-id/src/index.js
packages/L1-p13-brand-id/tests/jest/spec.jest.test.js
packages/L1-p13-brand-id/tests/vitest/spec.test.js
packages/L1-p13-brand-id/vitest.config.ts
packages/L1-p14-clone-shallow/README.md
packages/L1-p14-clone-shallow/babel.config.cjs
packages/L1-p14-clone-shallow/jest.config.cjs
packages/L1-p14-clone-shallow/package.json
packages/L1-p14-clone-shallow/src/index.js
packages/L1-p14-clone-shallow/tests/jest/spec.jest.test.js
packages/L1-p14-clone-shallow/tests/vitest/spec.test.js
packages/L1-p14-clone-shallow/vitest.config.ts
packages/L1-p15-memoize-basic/README.md
packages/L1-p15-memoize-basic/babel.config.cjs
packages/L1-p15-memoize-basic/jest.config.cjs
packages/L1-p15-memoize-basic/package.json
packages/L1-p15-memoize-basic/src/index.js
packages/L1-p15-memoize-basic/tests/jest/spec.jest.test.js
packages/L1-p15-memoize-basic/tests/vitest/spec.test.js
packages/L1-p15-memoize-basic/vitest.config.ts
packages/L2-p01-catalog-repo/README.md
packages/L2-p01-catalog-repo/babel.config.cjs
packages/L2-p01-catalog-repo/jest.config.cjs
packages/L2-p01-catalog-repo/package.json
packages/L2-p01-catalog-repo/src/index.js
packages/L2-p01-catalog-repo/tests/jest/spec.jest.test.js
packages/L2-p01-catalog-repo/tests/vitest/spec.test.js
packages/L2-p01-catalog-repo/vitest.config.ts
packages/L2-p02-memoize-weak/README.md
packages/L2-p02-memoize-weak/babel.config.cjs
packages/L2-p02-memoize-weak/jest.config.cjs
packages/L2-p02-memoize-weak/package.json
packages/L2-p02-memoize-weak/src/index.js
packages/L2-p02-memoize-weak/tests/jest/spec.jest.test.js
packages/L2-p02-memoize-weak/tests/vitest/spec.test.js
packages/L2-p02-memoize-weak/vitest.config.ts
packages/L2-p03-errors-cause/README.md
packages/L2-p03-errors-cause/babel.config.cjs
packages/L2-p03-errors-cause/jest.config.cjs
packages/L2-p03-errors-cause/package.json
packages/L2-p03-errors-cause/src/index.js
packages/L2-p03-errors-cause/tests/jest/spec.jest.test.js
packages/L2-p03-errors-cause/tests/vitest/spec.test.js
packages/L2-p03-errors-cause/vitest.config.ts
packages/L2-p04-directory-allsettled/README.md
packages/L2-p04-directory-allsettled/babel.config.cjs
packages/L2-p04-directory-allsettled/jest.config.cjs
packages/L2-p04-directory-allsettled/package.json
packages/L2-p04-directory-allsettled/src/index.js
packages/L2-p04-directory-allsettled/tests/jest/spec.jest.test.js
packages/L2-p04-directory-allsettled/tests/vitest/spec.test.js
packages/L2-p04-directory-allsettled/vitest.config.ts
packages/L2-p05-report-topk/README.md
packages/L2-p05-report-topk/babel.config.cjs
packages/L2-p05-report-topk/jest.config.cjs
packages/L2-p05-report-topk/package.json
packages/L2-p05-report-topk/src/index.js
packages/L2-p05-report-topk/tests/jest/spec.jest.test.js
packages/L2-p05-report-topk/tests/vitest/spec.test.js
packages/L2-p05-report-topk/vitest.config.ts
packages/L2-p06-adapter-dto/README.md
packages/L2-p06-adapter-dto/babel.config.cjs
packages/L2-p06-adapter-dto/jest.config.cjs
packages/L2-p06-adapter-dto/package.json
packages/L2-p06-adapter-dto/src/index.js
packages/L2-p06-adapter-dto/tests/jest/spec.jest.test.js
packages/L2-p06-adapter-dto/tests/vitest/spec.test.js
packages/L2-p06-adapter-dto/vitest.config.ts
packages/L2-p07-async-iterator/README.md
packages/L2-p07-async-iterator/babel.config.cjs
packages/L2-p07-async-iterator/jest.config.cjs
packages/L2-p07-async-iterator/package.json
packages/L2-p07-async-iterator/src/index.js
packages/L2-p07-async-iterator/tests/jest/spec.jest.test.js
packages/L2-p07-async-iterator/tests/vitest/spec.test.js
packages/L2-p07-async-iterator/vitest.config.ts
packages/L2-p08-decorator-logger/README.md
packages/L2-p08-decorator-logger/babel.config.cjs
packages/L2-p08-decorator-logger/jest.config.cjs
packages/L2-p08-decorator-logger/package.json
packages/L2-p08-decorator-logger/src/index.js
packages/L2-p08-decorator-logger/tests/jest/spec.jest.test.js
packages/L2-p08-decorator-logger/tests/vitest/spec.test.js
packages/L2-p08-decorator-logger/vitest.config.ts
packages/L2-p09-idempotent-add/README.md
packages/L2-p09-idempotent-add/babel.config.cjs
packages/L2-p09-idempotent-add/jest.config.cjs
packages/L2-p09-idempotent-add/package.json
packages/L2-p09-idempotent-add/src/index.js
packages/L2-p09-idempotent-add/tests/jest/spec.jest.test.js
packages/L2-p09-idempotent-add/tests/vitest/spec.test.js
packages/L2-p09-idempotent-add/vitest.config.ts
packages/L2-p10-schema-check/README.md
packages/L2-p10-schema-check/babel.config.cjs
packages/L2-p10-schema-check/jest.config.cjs
packages/L2-p10-schema-check/package.json
packages/L2-p10-schema-check/src/index.js
packages/L2-p10-schema-check/tests/jest/spec.jest.test.js
packages/L2-p10-schema-check/tests/vitest/spec.test.js
packages/L2-p10-schema-check/vitest.config.ts
packages/L2-p11-compose-pipeline/README.md
packages/L2-p11-compose-pipeline/babel.config.cjs
packages/L2-p11-compose-pipeline/jest.config.cjs
packages/L2-p11-compose-pipeline/package.json
packages/L2-p11-compose-pipeline/src/index.js
packages/L2-p11-compose-pipeline/tests/jest/spec.jest.test.js
packages/L2-p11-compose-pipeline/tests/vitest/spec.test.js
packages/L2-p11-compose-pipeline/vitest.config.ts
packages/L2-p12-hasinstance/README.md
packages/L2-p12-hasinstance/babel.config.cjs
packages/L2-p12-hasinstance/jest.config.cjs
packages/L2-p12-hasinstance/package.json
packages/L2-p12-hasinstance/src/index.js
packages/L2-p12-hasinstance/tests/jest/spec.jest.test.js
packages/L2-p12-hasinstance/tests/vitest/spec.test.js
packages/L2-p12-hasinstance/vitest.config.ts
packages/L2-p13-collator-sort/README.md
packages/L2-p13-collator-sort/babel.config.cjs
packages/L2-p13-collator-sort/jest.config.cjs
packages/L2-p13-collator-sort/package.json
packages/L2-p13-collator-sort/src/index.js
packages/L2-p13-collator-sort/tests/jest/spec.jest.test.js
packages/L2-p13-collator-sort/tests/vitest/spec.test.js
packages/L2-p13-collator-sort/vitest.config.ts
packages/L2-p14-deep-freeze/README.md
packages/L2-p14-deep-freeze/babel.config.cjs
packages/L2-p14-deep-freeze/jest.config.cjs
packages/L2-p14-deep-freeze/package.json
packages/L2-p14-deep-freeze/src/index.js
packages/L2-p14-deep-freeze/tests/jest/spec.jest.test.js
packages/L2-p14-deep-freeze/tests/vitest/spec.test.js
packages/L2-p14-deep-freeze/vitest.config.ts
packages/L2-p15-memo-ttl/README.md
packages/L2-p15-memo-ttl/babel.config.cjs
packages/L2-p15-memo-ttl/jest.config.cjs
packages/L2-p15-memo-ttl/package.json
packages/L2-p15-memo-ttl/src/index.js
packages/L2-p15-memo-ttl/tests/jest/spec.jest.test.js
packages/L2-p15-memo-ttl/tests/vitest/spec.test.js
packages/L2-p15-memo-ttl/vitest.config.ts
packages/L3-p01-retry-backoff/README.md
packages/L3-p01-retry-backoff/babel.config.cjs
packages/L3-p01-retry-backoff/jest.config.cjs
packages/L3-p01-retry-backoff/package.json
packages/L3-p01-retry-backoff/src/index.js
packages/L3-p01-retry-backoff/tests/jest/spec.jest.test.js
packages/L3-p01-retry-backoff/tests/vitest/spec.test.js
packages/L3-p01-retry-backoff/vitest.config.ts
packages/L3-p02-timeout/README.md
packages/L3-p02-timeout/babel.config.cjs
packages/L3-p02-timeout/jest.config.cjs
packages/L3-p02-timeout/package.json
packages/L3-p02-timeout/src/index.js
packages/L3-p02-timeout/tests/jest/spec.jest.test.js
packages/L3-p02-timeout/tests/vitest/spec.test.js
packages/L3-p02-timeout/vitest.config.ts
packages/L3-p03-semaphore/README.md
packages/L3-p03-semaphore/babel.config.cjs
packages/L3-p03-semaphore/jest.config.cjs
packages/L3-p03-semaphore/package.json
packages/L3-p03-semaphore/src/index.js
packages/L3-p03-semaphore/tests/jest/spec.jest.test.js
packages/L3-p03-semaphore/tests/vitest/spec.test.js
packages/L3-p03-semaphore/vitest.config.ts
packages/L3-p04-abort/README.md
packages/L3-p04-abort/babel.config.cjs
packages/L3-p04-abort/jest.config.cjs
packages/L3-p04-abort/package.json
packages/L3-p04-abort/src/index.js
packages/L3-p04-abort/tests/jest/spec.jest.test.js
packages/L3-p04-abort/tests/vitest/spec.test.js
packages/L3-p04-abort/vitest.config.ts
packages/L3-p05-circuit-breaker/README.md
packages/L3-p05-circuit-breaker/babel.config.cjs
packages/L3-p05-circuit-breaker/jest.config.cjs
packages/L3-p05-circuit-breaker/package.json
packages/L3-p05-circuit-breaker/src/index.js
packages/L3-p05-circuit-breaker/tests/jest/spec.jest.test.js
packages/L3-p05-circuit-breaker/tests/vitest/spec.test.js
packages/L3-p05-circuit-breaker/vitest.config.ts
packages/L3-p06-async-pipeline/README.md
packages/L3-p06-async-pipeline/babel.config.cjs
packages/L3-p06-async-pipeline/jest.config.cjs
packages/L3-p06-async-pipeline/package.json
packages/L3-p06-async-pipeline/src/index.js
packages/L3-p06-async-pipeline/tests/jest/spec.jest.test.js
packages/L3-p06-async-pipeline/tests/vitest/spec.test.js
packages/L3-p06-async-pipeline/vitest.config.ts
packages/L3-p07-e2e-site/README.md
packages/L3-p07-e2e-site/babel.config.cjs
packages/L3-p07-e2e-site/jest.config.cjs
packages/L3-p07-e2e-site/package.json
packages/L3-p07-e2e-site/playwright.config.ts
packages/L3-p07-e2e-site/public/index.html
packages/L3-p07-e2e-site/server.js
packages/L3-p07-e2e-site/src/index.js
packages/L3-p07-e2e-site/tests/e2e.spec.ts
packages/L3-p07-e2e-site/vitest.config.ts
packages/L3-p08-pwa-workbox/README.md
packages/L3-p08-pwa-workbox/babel.config.cjs
packages/L3-p08-pwa-workbox/build-sw.mjs
packages/L3-p08-pwa-workbox/jest.config.cjs
packages/L3-p08-pwa-workbox/package.json
packages/L3-p08-pwa-workbox/playwright.config.ts
packages/L3-p08-pwa-workbox/public/index.html
packages/L3-p08-pwa-workbox/src/index.js
packages/L3-p08-pwa-workbox/tests/pwa.spec.ts
packages/L3-p08-pwa-workbox/vitest.config.ts
packages/L3-p09-stable-hash/README.md
packages/L3-p09-stable-hash/babel.config.cjs
packages/L3-p09-stable-hash/jest.config.cjs
packages/L3-p09-stable-hash/package.json
packages/L3-p09-stable-hash/src/index.js
packages/L3-p09-stable-hash/tests/jest/spec.jest.test.js
packages/L3-p09-stable-hash/tests/vitest/spec.test.js
packages/L3-p09-stable-hash/vitest.config.ts
packages/L3-p10-plugins/README.md
packages/L3-p10-plugins/babel.config.cjs
packages/L3-p10-plugins/jest.config.cjs
packages/L3-p10-plugins/package.json
packages/L3-p10-plugins/src/index.js
packages/L3-p10-plugins/tests/jest/spec.jest.test.js
packages/L3-p10-plugins/tests/vitest/spec.test.js
packages/L3-p10-plugins/vitest.config.ts
packages/L3-p11-fault-injection/README.md
packages/L3-p11-fault-injection/babel.config.cjs
packages/L3-p11-fault-injection/jest.config.cjs
packages/L3-p11-fault-injection/package.json
packages/L3-p11-fault-injection/src/index.js
packages/L3-p11-fault-injection/tests/jest/spec.jest.test.js
packages/L3-p11-fault-injection/tests/vitest/spec.test.js
packages/L3-p11-fault-injection/vitest.config.ts
packages/L3-p12-randomized-tests/README.md
packages/L3-p12-randomized-tests/babel.config.cjs
packages/L3-p12-randomized-tests/jest.config.cjs
packages/L3-p12-randomized-tests/package.json
packages/L3-p12-randomized-tests/src/index.js
packages/L3-p12-randomized-tests/tests/jest/spec.jest.test.js
packages/L3-p12-randomized-tests/tests/vitest/spec.test.js
packages/L3-p12-randomized-tests/vitest.config.ts
packages/L3-p13-async-queue/README.md
packages/L3-p13-async-queue/babel.config.cjs
packages/L3-p13-async-queue/jest.config.cjs
packages/L3-p13-async-queue/package.json
packages/L3-p13-async-queue/src/index.js
packages/L3-p13-async-queue/tests/jest/spec.jest.test.js
packages/L3-p13-async-queue/tests/vitest/spec.test.js
packages/L3-p13-async-queue/vitest.config.ts
packages/L3-p14-e2e-table/README.md
packages/L3-p14-e2e-table/babel.config.cjs
packages/L3-p14-e2e-table/jest.config.cjs
packages/L3-p14-e2e-table/package.json
packages/L3-p14-e2e-table/playwright.config.ts
packages/L3-p14-e2e-table/public/index.html
packages/L3-p14-e2e-table/server.js
packages/L3-p14-e2e-table/src/index.js
packages/L3-p14-e2e-table/tests/e2e.spec.ts
packages/L3-p14-e2e-table/vitest.config.ts
packages/L3-p15-e2e-form/README.md
packages/L3-p15-e2e-form/babel.config.cjs
packages/L3-p15-e2e-form/jest.config.cjs
packages/L3-p15-e2e-form/package.json
packages/L3-p15-e2e-form/playwright.config.ts
packages/L3-p15-e2e-form/public/index.html
packages/L3-p15-e2e-form/server.js
packages/L3-p15-e2e-form/src/index.js
packages/L3-p15-e2e-form/tests/e2e.spec.ts
packages/L3-p15-e2e-form/vitest.config.ts
pnpm-workspace.yaml
vitest.config.ts
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** config: 190, docs: 45, ci: 4, code: 45, tests: 86, other: 3, public: 4, pwa: 2.

**package.json — sinteză: scripturi, workspaces, dependențe (eșantion)**

- `package.json`: name=`s3-p3-monorepo` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `pnpm -r --filter './packages/*' exec vitest run --reporter verbose`
  - `test:jest` → `pnpm -r --filter './packages/*' exec jest --runInBand`
  - `test` → `pnpm run test:vitest && pnpm run test:jest`
  - **Deps:** 
  - **DevDeps:** vitest, jest, babel-jest, @babel/preset-env, @playwright/test, workbox-build, express
- `packages/L1-p01-student-vo/package.json`: name=`@s3/L1-p01-student-vo` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p02-club-vo/package.json`: name=`@s3/L1-p02-club-vo` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p03-event-vo/package.json`: name=`@s3/L1-p03-event-vo` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p04-factory-student/package.json`: name=`@s3/L1-p04-factory-student` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p05-descriptor-secret/package.json`: name=`@s3/L1-p05-descriptor-secret` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p06-branding-tag/package.json`: name=`@s3/L1-p06-branding-tag` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p07-catalog-iterable/package.json`: name=`@s3/L1-p07-catalog-iterable` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p08-equals-by/package.json`: name=`@s3/L1-p08-equals-by` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p09-key-by-email/package.json`: name=`@s3/L1-p09-key-by-email` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p10-find-or-throw/package.json`: name=`@s3/L1-p10-find-or-throw` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p11-validation-report/package.json`: name=`@s3/L1-p11-validation-report` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p12-mixins/package.json`: name=`@s3/L1-p12-mixins` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p13-brand-id/package.json`: name=`@s3/L1-p13-brand-id` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p14-clone-shallow/package.json`: name=`@s3/L1-p14-clone-shallow` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L1-p15-memoize-basic/package.json`: name=`@s3/L1-p15-memoize-basic` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p01-catalog-repo/package.json`: name=`@s3/L2-p01-catalog-repo` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p02-memoize-weak/package.json`: name=`@s3/L2-p02-memoize-weak` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p03-errors-cause/package.json`: name=`@s3/L2-p03-errors-cause` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p04-directory-allsettled/package.json`: name=`@s3/L2-p04-directory-allsettled` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p05-report-topk/package.json`: name=`@s3/L2-p05-report-topk` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p06-adapter-dto/package.json`: name=`@s3/L2-p06-adapter-dto` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p07-async-iterator/package.json`: name=`@s3/L2-p07-async-iterator` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p08-decorator-logger/package.json`: name=`@s3/L2-p08-decorator-logger` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p09-idempotent-add/package.json`: name=`@s3/L2-p09-idempotent-add` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p10-schema-check/package.json`: name=`@s3/L2-p10-schema-check` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p11-compose-pipeline/package.json`: name=`@s3/L2-p11-compose-pipeline` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p12-hasinstance/package.json`: name=`@s3/L2-p12-hasinstance` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p13-collator-sort/package.json`: name=`@s3/L2-p13-collator-sort` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p14-deep-freeze/package.json`: name=`@s3/L2-p14-deep-freeze` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L2-p15-memo-ttl/package.json`: name=`@s3/L2-p15-memo-ttl` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p01-retry-backoff/package.json`: name=`@s3/L3-p01-retry-backoff` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p02-timeout/package.json`: name=`@s3/L3-p02-timeout` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p03-semaphore/package.json`: name=`@s3/L3-p03-semaphore` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p04-abort/package.json`: name=`@s3/L3-p04-abort` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p05-circuit-breaker/package.json`: name=`@s3/L3-p05-circuit-breaker` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p06-async-pipeline/package.json`: name=`@s3/L3-p06-async-pipeline` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p07-e2e-site/package.json`: name=`@s3/L3-p07-e2e-site` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `serve` → `node server.js`
  - `test:e2e` → `playwright test`
  - **Deps:** express
  - **DevDeps:** 
- `packages/L3-p08-pwa-workbox/package.json`: name=`@s3/L3-p08-pwa-workbox` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `build:sw` → `node build-sw.mjs`
  - `test:e2e` → `playwright test`
- `packages/L3-p09-stable-hash/package.json`: name=`@s3/L3-p09-stable-hash` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p10-plugins/package.json`: name=`@s3/L3-p10-plugins` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p11-fault-injection/package.json`: name=`@s3/L3-p11-fault-injection` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p12-randomized-tests/package.json`: name=`@s3/L3-p12-randomized-tests` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p13-async-queue/package.json`: name=`@s3/L3-p13-async-queue` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
- `packages/L3-p14-e2e-table/package.json`: name=`@s3/L3-p14-e2e-table` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `serve` → `node server.js`
  - `test:e2e` → `playwright test`
  - **Deps:** express
  - **DevDeps:** 
- `packages/L3-p15-e2e-form/package.json`: name=`@s3/L3-p15-e2e-form` type=`module` workspaces=False
  - **Scripturi:**
  - `test:vitest` → `vitest run --reporter verbose`
  - `test:jest` → `jest --runInBand`
  - `serve` → `node server.js`
  - `test:e2e` → `playwright test`
  - **Deps:** express
  - **DevDeps:** 

### Seminar3_Partea3_p3-readmes.zip

```
L1/L1-p01-student-vo/README.md
L1/L1-p02-club-vo/README.md
L1/L1-p03-event-vo/README.md
L1/L1-p04-factory-student/README.md
L1/L1-p05-descriptor-secret/README.md
L1/L1-p06-branding-tag/README.md
L1/L1-p07-catalog-iterable/README.md
L1/L1-p08-equals-by/README.md
L1/L1-p09-key-by-email/README.md
L1/L1-p10-find-or-throw/README.md
L1/L1-p11-validation-report/README.md
L1/L1-p12-mixins/README.md
L1/L1-p13-brand-id/README.md
L1/L1-p14-clone-shallow/README.md
L1/L1-p15-memoize-basic/README.md
L2/L2-p01-catalog-repo/README.md
L2/L2-p02-memoize-weak/README.md
L2/L2-p03-errors-cause/README.md
L2/L2-p04-directory-allsettled/README.md
L2/L2-p05-report-topk/README.md
L2/L2-p06-adapter-dto/README.md
L2/L2-p07-async-iterator/README.md
L2/L2-p08-decorator-logger/README.md
L2/L2-p09-idempotent-add/README.md
L2/L2-p10-schema-check/README.md
L2/L2-p11-compose-pipeline/README.md
L2/L2-p12-hasinstance/README.md
L2/L2-p13-collator-sort/README.md
L2/L2-p14-deep-freeze/README.md
L2/L2-p15-memo-ttl/README.md
L3/L3-p01-retry-backoff/README.md
L3/L3-p02-timeout/README.md
L3/L3-p03-semaphore/README.md
L3/L3-p04-abort/README.md
L3/L3-p05-circuit-breaker/README.md
L3/L3-p06-async-pipeline/README.md
L3/L3-p07-e2e-site/README.md
L3/L3-p08-pwa-workbox/README.md
L3/L3-p09-stable-hash/README.md
L3/L3-p10-plugins/README.md
L3/L3-p11-fault-injection/README.md
L3/L3-p12-randomized-tests/README.md
L3/L3-p13-async-queue/README.md
L3/L3-p14-e2e-table/README.md
L3/L3-p15-e2e-form/README.md
README.md
```

**Variante detectate:** nedefinit (numele nu conține indicatori).

**Categorii de fișiere:** docs: 45, pwa: 1.

## 2. Sinteza documentelor DOCX (teorie ↔ laborator ↔ proiecte)

### Seminar3_Partea1_Teorie_extins.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 3 — Partea 1: Teorie (Obiecte și OOP în JS — prototipuri, excepții, memoization, async/await)
- Hook realist: „StudentHub” — când prototipurile și asincronia îți țin sistemul în viață
- 1. De ce OOP în JavaScript (și de ce „prototype delegation”, nu numai clase)?

**Headings principale (eșantion):**

- Seminarul 3 — Partea 1: Teorie (Obiecte și OOP în JS — prototipuri, excepții, memoization, async/await)
- Hook realist: „StudentHub” — când prototipurile și asincronia îți țin sistemul în viață
- 1. De ce OOP în JavaScript (și de ce „prototype delegation”, nu numai clase)?
- 2. Modelul de obiecte: identitate, valoare, proprietăți, prototipuri
- 2.1. Identitate vs. valoare
- 2.2. Proprietăți și descriptori
- 2.3. Crearea obiectelor și prototipuri
- 2.4. `this`, `new`, `super`, `instanceof`
- 2.5. Simboluri utile și protocoale
- 3. Compoziție, mixins și *factory functions* (vs. moștenire adâncă)
- 3.1. De ce compoziție?
- 3.2. *Mixins*

### Seminar3_Partea2_Ghid_Arhive_v2.docx

**Titluri/Heading-uri (eșantion):**

- Ghid de utilizare — Arhivele Seminarului 3 (Partea 2, v2)
- 1) Arhiva Standalone
- 2) Arhiva Monorepo (PNPM workspaces)

**Headings principale (eșantion):**

- Ghid de utilizare — Arhivele Seminarului 3 (Partea 2, v2)
- 1) Arhiva Standalone
- 2) Arhiva Monorepo (PNPM workspaces)
- 3) Note de proiectare
- 4) Troubleshooting rapid

### Seminar3_Partea2_Laborator_extins_v2.docx

**Titluri/Heading-uri (eșantion):**

- Seminarul 3 — Partea 2: Laborator practic (progresiv, extins)
- 0) Principii de lucru & evaluare
- 1) Worksheet — Cerințe & Checklist

**Headings principale (eșantion):**

- Seminarul 3 — Partea 2: Laborator practic (progresiv, extins)
- 0) Principii de lucru & evaluare
- 1) Worksheet — Cerințe & Checklist
- 2) Inițializare proiect (scaffold)
- 3) Starter code (explicat)
- 3.1) Erori (taxonomie aplicată)
- 3.2) Entități (immutabile superficial, invariante)
- 3.3) Memoization (Map, WeakMap, TTL)
- 3.4) Raport (funcție pură, deterministă, memoizată)
- 3.5) Async utilities (timeout, retry/backoff, semafor)
- 3.6) Directory service (mock concurent + abort)
- 4) Exerciții L1 (fundamental) — pas cu pas

### Seminar3_Partea3_Ghid_Arhive.docx

**Titluri/Heading-uri (eșantion):**

- 1) Arhiva Standalone — s3-p3-standalone.zip
- 2) Arhiva Monorepo (PNPM workspaces) — s3-p3-monorepo.zip
- 3) Workflow‑uri CI (GitHub Actions)

**Headings principale (eșantion):**

- 1) Arhiva Standalone — s3-p3-standalone.zip
- 2) Arhiva Monorepo (PNPM workspaces) — s3-p3-monorepo.zip
- 3) Workflow‑uri CI (GitHub Actions)
- 4) Troubleshooting

### Seminar3_Partea3_Proiecte_extins.docx

**Titluri/Heading-uri (eșantion):**

- L1 — Fundamental
- L1-p01-student-vo: Student VO — invariante, freeze, branding
- L1-p02-club-vo: Club VO — invariante și tags

**Headings principale (eșantion):**

- L1 — Fundamental
- L1-p01-student-vo: Student VO — invariante, freeze, branding
- L1-p02-club-vo: Club VO — invariante și tags
- L1-p03-event-vo: Event VO — dată și toString()
- L1-p04-factory-student: Factory + Object.create + prototip
- L1-p05-descriptor-secret: Descriptori — proprietate neenumerabilă
- L1-p06-branding-tag: Branding — Symbol.toStringTag utilitar
- L1-p07-catalog-iterable: Catalog iterabil — Symbol.iterator
- L1-p08-equals-by: equalsBy — egalitate pe câmpuri
- L1-p09-key-by-email: keyByEmail — mapare rapidă
- L1-p10-find-or-throw: findStudentById — NotFoundError
- L1-p11-validation-report: Raport de validare (Ok/Err)

## 3. Monorepo vs. standalone — analiză comparativă


**Manageri de pachete & workspaces.** Monorepo (PNPM) declară `packages/*` în `pnpm-workspace.yaml` (plus `workspaces` în `package.json`) și rulează testele agregat; standalone izolează dependențele pe directorul proiectului.

**Comenzi de instalare/testare.** Monorepo: `pnpm i -w`, `pnpm -w run test` sau `--filter`. Standalone: `npm i`, `npm test`. Suitele sunt **oglindite** (Vitest & Jest) pe aceleași **contracte** (entități, erori, memo, async). 

**Integrare CI.** Monorepo include workflows `.github/workflows/*` (unit Vitest/Jest, e2e, workbox); standalone are workflows per proiect. 

**Avantaje/Dezavantaje.** Standalone — curba de învățare mai lină (începători). Monorepo — productiv pentru colecții mari (45 proiecte L1–L3) și pentru partajarea configurațiilor; costul e înțelegerea filtrării PNPM și a matricei CI.
## 4. Rolul fișierelor cheie (config, cod, teste, extra)

| Fișier / tip | Rol |
|---|---|
| `package.json` | Manifest: metadate, dependențe, scripturi; ESM (`type: module`). |
| `jest.config.cjs` | Configurare Jest (`babel-jest`, `extensionsToTreatAsEsm`). |
| `babel.config.cjs` | Preset `@babel/preset-env` pentru Jest. |
| `vitest.config.ts` | Configurare Vitest (env node), include `tests/vitest/**/*.test.js`. |
| `pnpm-workspace.yaml` | Declară pachetele din monorepo pentru PNPM. |
| `playwright.config.ts` | Config E2E (pachete L3). |
| `src/entities.js` | Entități `Student`/`Club`/`Event` cu invariante și branding. |
| `src/errors.js` | Ierarhie de erori: `AppError`, `ValidationError`, `NotFoundError`, `RemoteError`, `TimeoutError`. |
| `src/services/memo.js` | Memoization (`memoize`, `memoizeWeak`, `memoizeWithTTL`). |
| `src/services/report.js` | `ReportService.topInterests` — pură + deterministă + memoizată. |
| `src/services/concurrency.js` | `withTimeout`, `withRetry(backoff)`, `makeSemaphore`. |
| `src/services/directory.js` | `DirectoryService.loadAll` cu `Promise.allSettled` + `AbortController`. |

## 5. Corelații cod ↔ configurări ↔ teste


- **Entități & erori** (`src/entities.js`, `src/errors.js`) → teste Vitest & Jest care verifică **invariantele** și încadrarea erorilor cu `cause`.  
- **Memoization** (`src/services/memo.js`, `src/services/report.js`) → teste de **determinism**, **cache-hit** și **TTL**.  
- **Async** (`src/services/concurrency.js`, `src/services/directory.js`) → teste pentru `withTimeout`, `withRetry(backoff)`, semafor și `AbortController`.  
- **CI** (`.github/workflows/*`) → rulează `lint` + `test` (și E2E/PWA la L3), blocând regresiile înainte de merge.  
- **`.env.example`** (unde apare) — documentează `K`, `TTL_MS` etc.; legături explicite în scripturile din `package.json`.  
## 6. Ghid practic (README unificat)

### Prezentare generală și scop

Seminarul S3 aprofundează **obiectele** (cu delegare pe prototip), **ierarhiile de erori** aplicate domeniului, **memoization** sigură (chei stabile, `WeakMap`, `TTL`) și **asincronia** robustă (`async/await` cu `timeout`/`retry`/`abort`/semafor). Toate sunt integrate într-un laborator progresiv și în setul de 45 de proiecte (L1–L3), cu **testare în oglindă** (Vitest & Jest) și extensii E2E/PWA pe nivelul avansat. fileciteturn11file0 fileciteturn11file2### Analiză comparativă — monorepo vs. standalone


| Criteriu | Standalone | Monorepo (PNPM workspaces) |
|---|---|---|
| Complexitate | Redusă; un singur `package.json` | Mai ridicată; rădăcină + `packages/*` |
| Instalare | `npm i` | `pnpm i -w` |
| Testare | `npm test` (Vitest & Jest) | `pnpm -w run test` sau `--filter` |
| CI | Workflows per proiect | Workflows agregate, matrice pe pachete |
| Scalare (45 proiecte) | multiplicare directoare | pachete curate în `packages/*` |
| Public țintă | începători | echipe/colecții avansate |
### Inventar pe arhivă (roluri)

- **Seminar3_Partea2_lab-standalone-v2.zip** — config=5, docs=1, code=6, tests=6.
- **Seminar3_Partea2_lab-monorepo-v2.zip** — config=7, docs=1, code=6, tests=6.
- **Seminar3_Partea3_p3-standalone.zip** — docs=45, config=225, code=45, tests=86, other=3, public=4, pwa=2.
- **Seminar3_Partea3_p3-monorepo.zip** — config=190, docs=45, ci=4, code=45, tests=86, other=3, public=4, pwa=2.
- **Seminar3_Partea3_p3-readmes.zip** — docs=45, pwa=1.
### Explicații fișier-cu-fișier

Consultați tabelul din §4. Maparea exactă a entităților, erorilor, memoization-ului și utilitarelor async pe structura arhivelor este documentată în ghidul de arhive și în laboratorul extins (v2). fileciteturn11file1 fileciteturn11file2
### Corelații între fișiere


- `src/entities.js` ↔ teste: invariante, branding (`Symbol.toStringTag`), imutabilitate superficială. fileciteturn11file2  
- `src/services/memo.js`/`report.js` ↔ teste: determinism, cache-hit, `memoizeWeak`, `TTL`. fileciteturn11file2  
- `src/services/concurrency.js`/`directory.js` ↔ teste: `withTimeout`, `withRetry` (backoff), semafor, `AbortController`, `allSettled`. fileciteturn11file2  
- `.github/workflows/*` ↔ `lint`/`test`/`e2e`/`workbox`: pipeline determinist în monorepo. fileciteturn11file3  
### Recomandări pentru studenți


1) **Contracte peste implementări**: scrieți întâi invariantele și erorile tipizate; implementarea le urmează. fileciteturn11file2  
2) **Puritate locală**: separați calculul (pur) de I/O; *memoization* doar pentru funcții deterministe. fileciteturn11file2  
3) **Async previzibil**: limitați așteptarea (timeout), reîncercați doar erorile „retryable”, permiteți anulare, folosiți semafor. fileciteturn11file0  
4) **Testare în oglindă**: păstrați aceleași contracte în Vitest & Jest; evitați „adapta­rea” testelor. fileciteturn11file2  
5) **ESM + Jest**: folosiți `babel-jest` și `extensionsToTreatAsEsm` când apar erori ESM. fileciteturn11file1  
### Instrucțiuni „Quick start” per arhivă


**Partea 2 — standalone (lab):**
```bash
unzip "Seminar3_Partea2_lab-standalone-v2.zip" -d s3-lab-standalone
cd s3-lab-standalone
npm i
npm test          # rulează Vitest + Jest
```
fileciteturn11file1

**Partea 2 — monorepo (lab):**
```bash
unzip "Seminar3_Partea2_lab-monorepo-v2.zip" -d s3-lab-monorepo
cd s3-lab-monorepo
pnpm i -w
pnpm -w run test
```
fileciteturn11file1

**Partea 3 — standalone (proiecte):**
```bash
unzip "Seminar3_Partea3_p3-standalone.zip" -d s3-p3-standalone
cd s3-p3-standalone/L1/L1-p01-student-vo
npm i
npm test
```
fileciteturn11file3

**Partea 3 — monorepo (proiecte):**
```bash
unzip "Seminar3_Partea3_p3-monorepo.zip" -d s3-p3-monorepo
cd s3-p3-monorepo
pnpm i
pnpm run test
pnpm -F @s3/L3-p07-e2e-site exec playwright test      # doar pentru pachetele E2E
pnpm -F @s3/L3-p08-pwa-workbox exec node build-sw.mjs # doar pentru pachetul PWA
```
fileciteturn11file3
### Troubleshooting (erori frecvente)


- **Jest + ESM**: verifică `babel-jest` și `extensionsToTreatAsEsm`. fileciteturn11file1  
- **Timings instabile** (TTL sau fake timers) → mărește `ttlMs` sau latențele de test pe mașini lente/CI. fileciteturn11file1  
- **E2E Playwright** (L3): pornește serverul (`npm run serve` sau `webServer` în `playwright.config.ts`). fileciteturn11file3  
- **Workbox/PWA**: rulează constructorul de SW înainte de test (`node build-sw.mjs`). fileciteturn11file3  
- **Divergențe între suite**: menține aceleași aserții în Vitest & Jest (oglindă). fileciteturn11file2  
### Integrarea ghidurilor DOCX (teorie ↔ laborator ↔ proiecte)


- **Partea 1 (Teorie, extins)** — modelează „de ce”-ul: prototipuri, ierarhii de erori, memoization, async/await cu timeout/retry/abort/semafor. fileciteturn11file0  
- **Partea 2 (Laborator extins v2 + Ghid arhive v2)** — „StudentHub Core”: entități + erori + memo + async + suite oglindă; structură și comenzi pentru standalone/monorepo. fileciteturn11file2 fileciteturn11file1  
- **Partea 3 (Ghid arhive + Proiecte extins)** — 45 proiecte L1–L3, inclusiv E2E și PWA; workflows CI și depanare. fileciteturn11file3 fileciteturn11file4  
### Prompt-șablon reutilizabil (seminarele următoare)


> „Generează pentru **Seminarul S3** (standalone & monorepo) un nucleu „StudentHub Core” cu entități imuabile superficial, ierarhii de erori (`AppError` & co.), `ReportService.topInterests` **pur + determinist + memoizat**, utilitare **async** (`withTimeout`, `withRetry` cu backoff, `makeSemaphore`, `AbortController`), **teste în oglindă** (Vitest/Jest), CI, README cu Quick start & Troubleshooting, și variante **starter**/**solution**. Include E2E/PWA doar pentru L3.”
