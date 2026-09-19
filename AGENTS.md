# KhataFlow AI Development Rules

1. Read relevant files in `docs/` before implementing features.
2. Do not change accounting rules without updating `docs/ACCOUNTING_SPEC.md`.
3. Do not change entities/schema without updating `docs/DATABASE_SPEC.md`.
4. Keep accounting/business logic outside React components.
5. Dexie/IndexedDB is the MVP source of truth.
6. Zustand is for UI/application state, not a database copy.
7. Every posted voucher must balance: Total DR = Total CR.
8. Never silently delete posted financial records.
9. Validate backup imports before writing data.
10. Do not add backend/cloud/authentication to MVP unless the roadmap reaches that phase.
11. Do not copy proprietary code from private/client projects.
12. Prefer small, focused changes.
13. Add/update tests for accounting changes.
14. Use strict TypeScript and avoid unnecessary `any`.
15. Keep user-facing strings ready for i18n.
16. Maintain mobile-first responsive behavior and accessibility.

Before finishing: run type checks, relevant tests, build, and review accounting balance behavior.
