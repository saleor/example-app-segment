# saleor-app-segment

## 1.3.4

### Patch Changes

- 17077505: Updated TypeScript version to 4.5.4.
- Updated dependencies [17077505]
  - @saleor/react-hook-form-macaw@0.2.9
  - @saleor/sentry-utils@0.2.3
  - @saleor/apps-logger@1.2.9
  - @saleor/apps-shared@1.11.1
  - @saleor/trpc@3.0.1
  - @saleor/apps-ui@1.2.7

## 1.3.3

### Patch Changes

- fbdbaa28: Remove custom Next.js + Sentry error. It was causing non existing paths to be reported as 500 instead of 404. We catch Sentry errors in implicit anyway in api routes.
- Updated dependencies [fbdbaa28]
  - @saleor/sentry-utils@0.2.2

## 1.3.2

### Patch Changes

- 2f59041c: Reverted shared Sentry configuration (init() part). It was not working properly - source maps were not properly assigned. Now configuration is not shared, but repeated in every app separately
- Updated dependencies [2f59041c]
  - @saleor/sentry-utils@0.2.1

## 1.3.1

### Patch Changes

- 0c4ba39f: Update next.js config after Sentry rollback.
- Updated dependencies [5c851a6c]
  - @saleor/apps-logger@1.2.8

## 1.3.0

### Minor Changes

- c4dcb863: Remove Pino logger library. It was already deprecated but for non migrated apps it was causing build errors. Right now we have one logger - @saleor/app-logger pkg.
- 1a9912f5: Setup Sentry inside Next.js instrumentation file. It ensures that Sentry works properly for serverless environment.

### Patch Changes

- 37ecb246: Update pnpm to 9.2.0 version. It means that we also dropped support for Node.js less than 16.
- cc047b1d: Downgraded Sentry package to v7. Previous upgrade to 8.x cause Sentry to conflict with Open Telemetry setup and Sentry was not working
- Updated dependencies [37ecb246]
- Updated dependencies [c4dcb863]
- Updated dependencies [1a9912f5]
  - @saleor/apps-logger@1.2.7
  - @saleor/react-hook-form-macaw@0.2.8
  - @saleor/sentry-utils@0.2.0
  - @saleor/apps-shared@1.11.0
  - @saleor/trpc@3.0.0
  - @saleor/apps-ui@1.2.6

## 1.2.3

### Patch Changes

- 64d88b24: Update packages to ESM. See node [docs](https://nodejs.org/api/esm.html) for more info.
- 5cbd3b63: Updated @saleor/app-sdk package to 0.50.1
- Updated dependencies [64d88b24]
- Updated dependencies [5cbd3b63]
  - @saleor/react-hook-form-macaw@0.2.7
  - @saleor/apps-shared@1.10.3
  - @saleor/trpc@2.0.3
  - @saleor/apps-ui@1.2.5

## 1.2.2

### Patch Changes

- 4ffef6be: Update `@sentry/nextjs` to 8.0.0 version. It should help us with attaching additional data to Sentry errors.
- 2604ce1e: Updated Next.js to 14.2.3
- Updated dependencies [2604ce1e]
  - @saleor/apps-shared@1.10.2
  - @saleor/trpc@2.0.2
  - @saleor/apps-ui@1.2.4
  - @saleor/react-hook-form-macaw@0.2.6

## 1.2.1

### Patch Changes

- Updated dependencies [f22f2b8a]
  - @saleor/apps-shared@1.10.1
  - @saleor/trpc@2.0.1

## 1.2.0

### Minor Changes

- b29318a2: Currently, Dashboard requires from a user to have "MANAGE_APPS" to have access to the apps tab.
  Since the release 3.20 Dashboard will allow all users to access to apps tabs without checking permission.
  This means that apps will be checking if the user has "MANAGE_APPS" internally and show message "You do not have permission to access this page" if the user does not have the permission.

### Patch Changes

- Updated dependencies [b29318a2]
  - @saleor/apps-shared@1.10.0
  - @saleor/trpc@2.0.0

## 1.1.5

### Patch Changes

- 29d10d4a: Update Next.js to version 14.1.0.
- Updated dependencies [29d10d4a]
  - @saleor/apps-shared@1.9.4
  - @saleor/trpc@1.0.4
  - @saleor/apps-ui@1.2.3
  - @saleor/react-hook-form-macaw@0.2.6

## 1.1.4

### Patch Changes

- Updated dependencies [67afe8e4]
  - @saleor/apps-shared@1.9.3
  - @saleor/trpc@1.0.3

## 1.1.3

### Patch Changes

- 5f564a0: Updated @saleor/app-sdk to 0.47.2

## 1.1.2

### Patch Changes

- 531e7c1: Disabled Sentry tracing and Replays by default

## 1.1.1

### Patch Changes

- 99f7066: Updated Macaw UI to 1.0.0-pre.7. Removed legacy Material UI dependency from older Macaw. Code was updated to work properly with some API changes
- Updated dependencies [99f7066]
  - @saleor/react-hook-form-macaw@0.2.6
  - @saleor/apps-shared@1.9.2
  - @saleor/apps-ui@1.2.2
  - @saleor/trpc@1.0.2

## 1.1.0

### Minor Changes

- a50df02: Reduced Sentry traces sample rate to 0.1

### Patch Changes

- f4c67e8: Updated TRPC version

## 1.0.5

### Patch Changes

- fdabc51: Mapped app-sdk package to root library
- Updated dependencies [fdabc51]
  - @saleor/apps-shared@1.9.1
  - @saleor/trpc@1.0.1
  - @saleor/apps-ui@1.2.1

## 1.0.4

### Patch Changes

- 148a6d7: Updated Sentry to 7.77.0

## 1.0.3

### Patch Changes

- 5d3d81d: Bumped @hookform/resolvers from 2.9.11 to 3.3.1
- 5dee65a: Updated dependencies:
  - @graphql-codegen/cli@5.0.0
- 2e29699: Updated Sentry package

## 1.0.2

### Patch Changes

- e8660e8: Implemented ButtonsBox and SkeletonLayout from shared package. This should not have visual effect other than better looking Skeleton animation
- e8660e8: Replaced GraphQL provider with shared package
- e8660e8: Implemented ThemeSynchronizer from shared package
- e8660e8: Extracted some tRPC utilities to shared package
- Updated dependencies [e8660e8]
- Updated dependencies [e8660e8]
- Updated dependencies [e8660e8]
- Updated dependencies [e8660e8]
- Updated dependencies [e8660e8]
- Updated dependencies [e8660e8]
- Updated dependencies [e8660e8]
  - @saleor/apps-shared@1.9.0
  - @saleor/apps-ui@1.2.0
  - @saleor/trpc@1.0.0

## 1.0.1

### Patch Changes

- a81f061: Updated Macaw to pre-127
- fcc37e7: Remove clsx package from the projects no longer using it.
- 254cd4c: Fix typo in the UI ("configration" -> "configuration").
- Updated dependencies [2a1385b]
- Updated dependencies [a81f061]
- Updated dependencies [fcc37e7]
  - @saleor/apps-shared@1.8.1
  - @saleor/react-hook-form-macaw@0.2.5
  - @saleor/apps-ui@1.1.8

## 1.0.0

### Major Changes

- 7d574c7: Introduced a Segment.io app that integrates order events with Segment tracking

### Patch Changes

- 8b3d961: Updated Macaw UI to pre.118
- c50797e: Extracted MetadataManager creation to factory from shared package
- 6ea3e38: Changed semantic Segment events to match exactly Saleor events.
  Saleor checkout & order process is more complex than built-in Segment flow, so instead trying to fit, send only custom ones matching events from Saleor webhooks
- Updated dependencies [8b3d961]
- Updated dependencies [c50797e]
  - @saleor/react-hook-form-macaw@0.2.4
  - @saleor/apps-shared@1.8.0
  - @saleor/apps-ui@1.1.7
