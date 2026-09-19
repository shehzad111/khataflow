# KhataFlow Technical Specification

## Stack
- React 19
- TypeScript
- Vite
- Tailwind CSS
- React Router
- Dexie / IndexedDB
- Zustand
- Zod
- Vitest
- React Testing Library
- PWA/service worker

## Architecture
Feature-based:
- src/app
- src/components
- src/features
- src/db
- src/services
- src/stores
- src/hooks
- src/utils
- src/types
- src/i18n
- src/assets

## Source of Truth
Dexie/IndexedDB is the source of truth. Zustand must not duplicate the database.

## Domain Services
Accounting logic belongs in services/domain modules:
- calculateLedgerBalance()
- createReceiptVoucher()
- createPaymentVoucher()
- validateVoucher()
- calculateTrialBalance()
- calculateOutstanding()
- exportBackup()
- importBackup()

## Atomic Voucher Creation
Use a Dexie transaction to save voucher + all ledger entries together.

## Validation
Use Zod for forms and imported backup structure. Keep accounting rules in domain validation.

## Routes
/
 /ledgers
 /ledgers/:id
 /transactions
 /transactions/new
 /reports
 /reports/day-book
 /reports/trial-balance
 /backup
 /settings

## Backup
JSON backup contains schema version, export timestamp, ledgers, vouchers, ledger entries, settings. Validate before import.

## Testing
Must cover opening DR/CR, receipt, payment, zero balance, DR/CR balances, multiple vouchers, filtering, trial balance, backup/restore.

## Code Quality
Strict TypeScript, ESLint, Prettier, small components, reusable services, no duplicated accounting formulas.
