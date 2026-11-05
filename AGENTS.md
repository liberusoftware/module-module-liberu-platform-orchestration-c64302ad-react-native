# Capability module guidance — Liberu Platform Orchestration, React Native · Expo

Read README.md and the [capability presentation plan](https://github.com/liberusoftware/documentation/blob/main/projects/accounting/react-native/liberu-platform-orchestration.md). Exact ownership key: `liberusoftware/module-liberu-platform-orchestration`. Naming conflict review required: `true`.

- This is a reusable npm presentation package. Keep explicit exports, actual package identities and independent release metadata. Application hosts own routing, navigation, session composition and deployment.
- Keep core behavior, tenant authorization, policies, records, transactions and durable events in canonical Laravel owners. Use reviewed public contracts; never invent endpoints, replace source owners silently or copy host App aliases into reusable packages.
- Add only this capability's UI/transport mapping. Preserve framework-specific server/client, Inertia, native lifecycle and cache boundaries described in the [layer guide](https://github.com/liberusoftware/documentation/blob/main/guides/presentation/REACT-NATIVE.md).
- Verify package builds and clean consumers. Add meaningful access, tenant, validation, concurrency and recovery tests when real workflows exist. Current skeleton metadata proves no business behavior.
- Keep secrets outside source and client bundles. Clear scoped state on logout. Do not publish to registries or deploy without task authorization.
