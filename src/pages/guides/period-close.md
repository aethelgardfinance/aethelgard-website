---
layout: ../../layouts/GuideLayout.astro
title: Month-end and year-end close in Aethelgard
description: The discipline that turns a ledger into a defensible record — reconcile, balance, lock, and post the year-end close so the structure your accountant inherits is auditable.
slug: period-close
---

The reason a wealth ledger and a list of bank transactions diverge over time is that one is closed regularly and the other is not. A closed period is a frozen, signed-off statement: every account reconciled, every accrual posted, every intercompany transfer matched, and a date-range lock that prevents anyone — including you, six months later — from quietly editing the past.

Aethelgard treats the close as a process, not a button. The button is the last step.

## What a month-end close actually does

A month-end close converts unstructured activity (statements, receipts, recurring items) into a defensible position at a single moment in time. Four things have to be true before the period is sound.

**Every transaction is imported and posted.** Bank statements, credit card statements, brokerage activity, dividends, recurring items, manual journals (depreciation, accruals, prepayments). Aethelgard's auto-rules will categorise most lines; the leftover handful that need a decision are the ones worth ten minutes of attention.

**Every cash account reconciles.** Open the reconciliation screen and tick each end-of-month balance against its statement. A reconciliation difference of anything other than zero is a missing transaction, a duplicate import, or a wrong amount — it is not a rounding error you can "force balance" past. The point of reconciling is to find the line, not to make the screen go green.

**Every intercompany transfer matches on both sides.** Money moving between entities in the same group needs to be posted in both books, in the same period, against accounts flagged `is_intercompany`. Aethelgard's Integrity Dashboard surfaces unmatched intercompany pairs — fix them before the trial balance, not after.

**The trial balance balances.** Total debits must equal total credits. A non-zero net discrepancy means one side of a journal entry is missing or malformed. Investigate; don't close.

Only when these four conditions hold do you lock the period.

## The lock is the contract

Period locks are not advisory. Once a date range is locked, transactions cannot be posted into it without an explicit unlock. This is what makes the chain of monthly statements trustworthy: each one was true on the day it was sealed, and anything that contradicts it later is visible as either a current-period adjustment or an explicit reopening.

If you need to post a correction after locking, unlock the period, post the correction, re-run the trial balance, and re-lock. Don't leave a period unlocked "in case something comes in" — that defeats the entire point.

## Year-end close: the same process, plus four adjustments

A year-end close is a month-end close for the final month of the fiscal year, plus a small set of adjustments specific to closing the books for tax and reporting. The adjustments are:

- **Depreciation** posted on fixed assets for the year
- **Accruals** for expenses incurred but not yet invoiced (your year-end accountancy fee accrual is the classic one)
- **Prepayments** released or recognised across the boundary
- **Tax provision** posted — your estimated corporation tax liability against `2300 Corporation Tax Provision`

Once these are in and the trial balance still balances, the Year-End Close button in the reporting section posts the closing entries: every revenue and expense account is zeroed by transferring its balance to `3100 Retained Earnings`. The closing entry is auditable — it appears in the ledger like any other transaction.

After the close, your balance sheet should show every P&L account at zero, Retained Earnings increased by the year's net profit (or decreased by a loss), and the accounting equation still satisfied. If anything is off, the cause is almost always a late transaction posted into a previously-closed year — unlock, correct, repost, re-lock.

## Practical advice

- **Take a Sovereign Snapshot before the year-end close.** It is a destructive-by-design operation (it modifies retained earnings); a snapshot gives you a clean restore point if you need to redo it.
- **Use the official HMRC monthly exchange rates** for HMRC-reportable entities at the FX update step, not live spot rates. The HMRC rates are the basis on which your return will be assessed.
- **Run the year-end close once per period.** Aethelgard rejects a second close for the same period-end date by design. If a correction lands late, delete the existing closing transaction, fix, and re-run — don't try to "top up" a close.
- **Export the trial balance, P&L, and balance sheet as CSV for your accountant.** Aethelgard generates the working papers; your accountant turns them into Companies House and HMRC filings. The export buttons live on each report.

The close is not paperwork. It is the moment at which the ledger becomes a record someone else can rely on — your accountant for filings, your auditor for assurance, your successors for continuity. The work is to keep it honest enough that all three can.
