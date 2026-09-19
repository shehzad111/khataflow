# KhataFlow Accounting Specification

## Model
KhataFlow uses double-entry accounting.

**Every posted voucher must satisfy: Total DR = Total CR.**

## Ledger Balance
For a ledger:

`Balance = Opening DR - Opening CR + Transaction DR - Transaction CR`

Display the resulting side as DR or CR.

For trader ledgers:
- DR balance = Party owes you.
- CR balance = You owe party.

## Opening Balance
Opening amount and opening type (DR/CR) participate in reporting and running balances.

## Receipt
Money received from a party into an account:
- Account DR
- Party CR

## Payment
Money paid to a party from an account:
- Party DR
- Account CR

## Journal
Future feature supporting multiple DR/CR lines. Total DR must equal Total CR.

## Voucher Rules
- Amount > 0
- Date required
- Voucher type required
- Source/account required
- Party required for Receipt/Payment
- Voucher cannot post unless balanced
- Failed saves must not leave half-written entries

## Atomic Save
Voucher header and all ledger entries must be saved as one atomic logical operation using Dexie's transaction support.

## Financial Records
Posted records must not be physically deleted. Future versions should use cancellation/reversal.

## Day Book
Show posted vouchers chronologically with date, voucher no, type, particulars, debit, credit, narration.

## Trial Balance
Aggregate posted entries only. Always validate that total debit equals total credit.
