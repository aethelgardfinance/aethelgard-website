---
layout: ../../layouts/GuideLayout.astro
title: Reading Aethelgard's P&L and Balance Sheet
description: How principals, founders, and family-office operators can use the two core financial statements as decision tools rather than compliance artefacts.
slug: financial-reports
---

The two financial statements Aethelgard produces from your day-to-day entries — the Profit & Loss and the Balance Sheet — are the same statements your accountant prepares at year-end. The difference is that yours are live, on your machine, and tied directly to the underlying transactions.

This guide is for principals, founders, and family-office operators who want to use them as decision tools rather than compliance artefacts.

## The Profit & Loss

The P&L answers a single question: how did we do over a period? Aethelgard generates it for any date range you select.

It is structured the way IFRS expects:

- **Revenue.** Money earned in the period, regardless of when it was received.
- **Cost of sales.** Direct costs of producing the revenue. Aethelgard distinguishes these from operating expenses so gross margin is visible.
- **Operating expenses.** Overhead — software, rent, professional fees, salaries.
- **Below-the-line items.** Interest, tax, depreciation, amortisation. Separated so operating performance is not obscured by financing or capital-allocation choices.
- **Net income.** What is left.

### What to look for

- **Trend, not level.** A single month's number tells you almost nothing. Compare the period to the same period last year, or to a rolling average. Aethelgard lets you generate the same report across any two date ranges.
- **Gross margin.** Compute revenue minus cost of sales, divided by revenue. A falling gross margin means either pricing pressure or rising input costs — both worth investigating before the operating line tells you something is wrong.
- **Where the money went.** When operating expenses look high, drill into the line. Aethelgard's reports are interactive: click any figure and it opens the underlying ledger entries filtered to that account and period.

## The Balance Sheet

If the P&L is a film of the period, the Balance Sheet is a still photograph at a date. It tells you what the entity owns, what it owes, and what the residual is.

The identity is always the same: **Assets = Liabilities + Equity**.

### What to look for

- **Liquidity.** Current assets divided by current liabilities. Below 1.0 means short-term obligations exceed short-term resources — a working-capital warning.
- **Leverage.** Total liabilities relative to equity. High leverage amplifies returns in good periods and amplifies losses in bad ones. There is no universally correct ratio; the right one depends on the cash-flow stability of the underlying business.
- **Inter-company balances.** If you run multiple entities, their internal loans should net to zero on the consolidated Balance Sheet. Aethelgard handles this automatically when accounts are flagged as inter-company; see the [Multi-entity consolidation](/guides/multi-entity-consolidation) guide.

## Drilling in

Aethelgard's reports are not static PDFs. Every figure on the P&L and Balance Sheet is a link.

- Click a line — say, *Legal & Professional Fees* — and the General Ledger opens, scoped to that account and the period.
- From there you can see every individual entry that contributed to the total, with the date, counter-party, and any attached document.

This is what turns the reports from compliance documents into management information.
