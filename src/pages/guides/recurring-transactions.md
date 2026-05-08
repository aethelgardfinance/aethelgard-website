---
layout: ../../layouts/GuideLayout.astro
title: Recurring transactions
description: Define repeated entries — software, rent, salary, scheduled investment transfers — once, then have Aethelgard either post them automatically or remind you to confirm them.
slug: recurring-transactions
---

Most ledgers carry a long tail of repeated entries: monthly software, rent, salary, scheduled investment transfers, quarterly tax payments. Aethelgard handles these as named templates that either post themselves on the due date or remind you to confirm them.

Either way, you only define the entries once.

## What you can automate

- **Fixed expenses** — software subscriptions, rent, insurance premiums, professional retainers.
- **Recurring income** — salary, regular consulting retainers, expected dividends.
- **Internal transfers** — sweeps from current account to savings, or scheduled top-ups to an investment account.
- **Periodic accruals** — recognising a fraction of an annual expense each month so the P&L is not distorted at the renewal date.

## Creating a recurring template

A recurring transaction in Aethelgard is a template — a named, balanced set of debits and credits — plus a schedule.

1. Open **Recurring Transactions** from the sidebar.
2. Click **New template** and give it a clear name (for example, *AWS Hosting — OpCo*).
3. Add the debit and credit lines exactly as the posted journal should appear, including memo and the entity it belongs to.
4. Pick a frequency: daily, weekly, monthly, quarterly, or annual. For monthly, set the day of the month (1–28). Use *manual* if you want a template that never posts on a schedule but is available to apply by hand.
5. Choose how it posts:
   - **Remind me.** Aethelgard creates a draft on the due date and surfaces it for you to confirm. Use this for variable-amount entries (utilities, usage-based software).
   - **Auto-post.** Aethelgard posts the entry automatically. Use this for known-amount fixed entries.

## Editing the schedule

A template's frequency, day of month, and auto-post setting can be changed at any time. Setting a template to *inactive* stops further postings without deleting the history. The journals already posted are not affected — they are normal transactions in the ledger like any other.

## Variable amounts

Where the amount changes each period — utility bills, metered services — keep the template on **remind**. Aethelgard creates the draft with the last known amount and the matching account split; you adjust the figures and confirm. The categorisation and account split are reused so you only have to decide the number.

## Practical advice

- **Name templates by what they are, not by the vendor alone.** *AWS Hosting — OpCo* survives a vendor consolidation; *AWS* does not.
- **Review the active list each quarter.** Recurring templates are how subscription drift accumulates. Half the value of having them is the audit you do when you look at the list.
- **Use the entity field deliberately.** Cross-entity recurring transfers (HoldCo dividend to personal, for example) should sit on the receiving entity's books, not the payer's, so the consolidated view treats them correctly.
