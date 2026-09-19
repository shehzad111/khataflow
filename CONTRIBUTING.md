# Contributing to KhataFlow

Read README.md, AGENTS.md, and the relevant files under `docs/` before contributing.

## Rules
- Keep changes focused.
- Update accounting documentation when accounting behavior changes.
- Add tests for accounting/business logic.
- Never commit secrets or real customer financial data.
- Do not copy proprietary/client code.
- Keep mobile and desktop behavior working.

## Pull Requests
Explain:
1. What changed.
2. Why.
3. Tests performed.
4. Accounting/database implications.

## Accounting Changes
Changes affecting DR/CR, vouchers, opening balance, running balance, Trial Balance, or ledger reports require tests.

## Commit Examples
- feat: add receipt voucher
- fix: correct ledger balance
- docs: update accounting specification
- test: add payment voucher tests
