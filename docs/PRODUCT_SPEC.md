# KhataFlow Product Specification

## Product
KhataFlow — Simple Khata. Clear Ledger.

An open-source, privacy-first digital ledger for individuals and small businesses.

## Users
Small shop owners, traders, suppliers, freelancers, service providers, home businesses, and individuals maintaining lending/borrowing records.

## Ledger Types
- GENERAL
- TRADER
- CASH
- BANK

## Trader Roles
Only for TRADER:
- CUSTOMER
- SUPPLIER
- BOTH

## Trader/Business Details
Optional:
- Trade Name
- Legal Name
- GSTIN
- PAN
- Phone
- Email
- Address
- City
- State
- Pincode
- Notes

GSTIN/PAN are optional.

## Opening Balance
Ledger creation asks for:
- Opening Amount
- Opening Type: DR / CR

## Core Vouchers
- Receipt
- Payment
- Journal (future)

## Receipt
Party: Ahmed Traders, Account: CASH A/C, Amount: ₹5,000
- CASH A/C DR ₹5,000
- Ahmed Traders CR ₹5,000

## Payment
Party: Ahmed Traders, Account: CASH A/C, Amount: ₹5,000
- Ahmed Traders DR ₹5,000
- CASH A/C CR ₹5,000

## Screens
- Dashboard
- Ledgers
- Ledger Details
- Transaction Entry
- Day Book
- Reports
- Backup & Restore
- Settings

## Reports
- All Ledgers
- General
- Traders
- Cash
- Bank
- Customer Outstanding
- Supplier Outstanding
- Party Ledger
- Cash Book
- Bank Book
- Day Book
- Trial Balance
- Account Summary

## Privacy / MVP
Data stays locally in IndexedDB. No backend or account is required for basic MVP use.

## PWA
Installable and offline-capable.

## Localization
Initial language: English. Architecture must support Hindi later.

## Currency
Default INR (₹), but accounting logic must not hard-code INR.
