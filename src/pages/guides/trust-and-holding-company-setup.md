---
layout: ../../layouts/GuideLayout.astro
title: Setting up trusts and holding companies
description: Use Aethelgard's entity classes and inter-company tools to model trusts, holding companies, and their internal loans with the audit trail required to protect the structure.
slug: trust-and-holding-company-setup
---

For high-net-worth families, trusts and holding companies are the load-bearing structures of the wealth: they hold the equity, hold the property, and structure how value passes between generations. The accounting requirements are unforgiving — fiduciary distinctions matter, principal and income are not the same thing, and the audit trail is what protects the structure if it is ever tested.

Aethelgard's data model was built for this. Each entity has its own books, its own equity vocabulary, and its own period-close behaviour, with consolidation across entities handled at the reporting layer.

## Entity classes

When you create an entity in Aethelgard you classify it as **Corporate**, **Trust**, or **Individual**. The class is not just a label — it changes:

- **The equity vocabulary.** A Corporate entity uses share capital and retained earnings; a Trust uses trust principal (corpus) and undistributed income; an Individual uses owner's capital and drawings. The distinction matters because beneficiary distributions, dividend payments, and personal drawings are not the same accounting event.
- **The period-close orchestrator.** Aethelgard's close-period routine posts accruals, depreciation, and FX revaluation in the order appropriate for the class. A trust's close, for example, distinguishes principal from income before deciding what is distributable.

Setting the class correctly at creation saves rework later.

## A typical holding company

A holding company normally holds equity in operating companies, real estate, and investment portfolios, but does not trade itself. Set up:

1. Create the entity in Aethelgard, class **Corporate**.
2. Build a chart of accounts dominated by long-term investment, inter-company loan, and equity-investment lines. The operating-expense list will be short — director fees, professional fees, the bank charges on the holding accounts.
3. Where the holding company owns an operating company, record dividends as income on the HoldCo's P&L when declared, with the matching cash receipt against the HoldCo's bank account when paid.

## A typical trust

Trusts split assets between **principal** (the corpus settled into the trust) and **income** (what those assets earn). Distributions to beneficiaries are taxed differently depending on which they come from. The accounting must reflect that distinction.

1. Create the entity, class **Trust**. Aethelgard provides the principal and undistributed-income equity accounts automatically.
2. Hold the trust's bank, brokerage, and property accounts under the trust entity. Do not commingle with personal or corporate accounts — fiduciary segregation is the point.
3. When recording distributions, tag the entry with the beneficiary and identify whether the distribution is from principal or income. The audit trail produced by this tagging is what an auditor or tax authority will ask for.

## Inter-entity loans

A common structure has the holding company act as an internal treasury, lending to operating companies or, at times, to the family personally.

- Create a receivable account in the lender (*Loan to OpCo*) and a matching payable in the borrower (*Loan from HoldCo*). Mark both as inter-company.
- For interest-bearing loans, set up a recurring transaction that accrues interest at the agreed rate (see the [Recurring transactions](/guides/recurring-transactions) guide). Record the interest as income in the lender and an expense in the borrower.
- When the loan is repaid, the entries clean down both sides; the consolidated view eliminates the loan automatically because the accounts are inter-company flagged.

## Why the rigour matters

The principal risk to a complex family structure is the corporate veil being pierced — a court treating connected entities as if they were one because the books did not maintain real separation. The defence is contemporaneous, double-entry, segregated bookkeeping that demonstrates each entity operated as an independent reality.

That is exactly what Aethelgard produces as a side-effect of being used correctly. Set the entity class on each, segregate the accounts, flag the inter-company balances, and the audit trail builds itself.
