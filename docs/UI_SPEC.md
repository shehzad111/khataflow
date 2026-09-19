# KhataFlow UI Specification

## Design
Clean, modern, friendly, professional, mobile-first.

## Desktop Navigation
- Dashboard
- Ledgers
- Transactions
- Reports
- Backup
- Settings

## Mobile Navigation
- Home
- Ledgers
- Add
- Reports
- More

## Ledger Form
- Name
- Ledger Type
- Trader Role when type is Traders
- Trade Name
- Legal Name
- Phone
- Email
- GSTIN
- PAN
- Address
- City
- State
- Pincode
- Opening Balance
- Opening Type DR/CR
- Notes

## Transaction Form
- Date
- Voucher Type: Receipt / Payment
- Party/Ledger
- Account
- Amount
- Narration

## Ledger Details
Show:
- Name
- Type
- Trader role
- Business/contact details
- Current balance
- Receipt action
- Payment action
- Ledger table

Columns:
Date | Particular | Debit | Credit | Balance

## Balance
Example: `₹15,000 DR` with `Party owes you`.
Example: `₹5,000 CR` with `You owe party`.

## Dashboard
- Receivable
- Payable
- Cash
- Bank
- Today's receipts
- Today's payments
- Recent transactions
- Outstanding traders

## UX
- Labels always visible
- Mobile-friendly numeric amount input
- Clear validation
- Confirmation for destructive actions
- Keyboard accessible

## Accessibility
Semantic HTML, proper labels, visible focus, accessible dialogs/errors, sufficient contrast. Do not communicate DR/CR by color alone.

## Theme
Light, Dark, System.

## Responsive
Mobile is a first-class layout, not merely a scaled desktop screen.
