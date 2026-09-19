# KhataFlow Database Specification

MVP storage: IndexedDB through Dexie.

## Tables

### ledgers
- id
- code
- name
- type
- role
- trade_name
- legal_name
- gstin
- pan
- phone
- email
- address
- city
- state
- pincode
- opening_balance
- opening_type
- notes
- active
- created_at
- updated_at

`type`: GENERAL | TRADER | CASH | BANK

`role`: CUSTOMER | SUPPLIER | BOTH, only for TRADER

`opening_type`: DR | CR

### vouchers
- id
- voucher_no
- voucher_type
- date
- narration
- status
- created_at
- updated_at

`voucher_type`: RECEIPT | PAYMENT in MVP; JOURNAL later.

`status`: DRAFT | POSTED; CANCELLED later.

### ledger_entries
- id
- voucher_id
- ledger_id
- entry_type
- amount
- narration
- created_at

`entry_type`: DR | CR

Amount is always positive. DR/CR is explicit.

### settings
Key/value settings such as theme, language, currency, business details, and last backup time.

## Indexes
Ledgers: code, name, type, role, phone, active.
Vouchers: voucher_no, voucher_type, date, status.
Entries: voucher_id, ledger_id, entry_type, created_at.

## Integrity
Before posting:
- valid voucher
- at least two entries
- valid ledger IDs
- amount > 0
- Total DR = Total CR

## Archive
Ledgers may be archived with `active=false`. Posted financial entries remain for history.

## Future Cloud
Keep domain logic independent of IndexedDB so the same logical model can later map to PostgreSQL/MySQL.
