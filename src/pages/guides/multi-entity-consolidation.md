---
layout: ../../layouts/GuideLayout.astro
title: Multi-entity consolidation in Aethelgard
description: How to model an operating company, a holding company, a personal account, and a trust as one group — and produce both standalone and consolidated reports.
slug: multi-entity-consolidation
---

Most wealth at scale is not held in a single legal entity. A typical structure has an operating company, a holding company that owns equity and property, a personal account for daily life, and possibly a trust or SPV layered for tax or succession reasons.

Spreadsheets and consumer accounting apps treat each of these as separate, unrelated worlds. Aethelgard treats them as what they are: distinct entities that need to be reported on individually *and* rolled up into a single, consistent group view.

## How Aethelgard structures entities

Each entity in Aethelgard — company, trust, holding vehicle, or individual — is a first-class object with its own chart of accounts, its own books, and its own reports. Entities can be grouped under a parent for consolidation.

When you create an entity, you classify it as **Corporate**, **Trust**, or **Individual**. This is not cosmetic. The class drives the equity vocabulary Aethelgard uses (share capital and retained earnings for a company, principal and undistributed income for a trust, owner's capital for an individual) and the close-period orchestrator that runs accruals, depreciation, and FX revaluation in the right order for that class.

## Inter-company transactions

The hardest part of multi-entity accounting is handling money that moves *within* the group — a holding company lending to an operating company, or paying an inter-company management fee. If you simply add the entities together, the same money appears on both sides of the consolidated Balance Sheet.

Aethelgard solves this with an `is_intercompany` flag on accounts:

- Mark the loan-receivable account in HoldCo and the matching loan-payable account in OpCo as inter-company.
- Aethelgard's consolidation engine pairs them at run-time and posts an explicit elimination journal so the consolidated view shows the net group position.
- The elimination is auditable: every elimination journal is captured, so you can produce a textbook eliminate-on-consolidate trail for an auditor.

## Single-entity vs consolidated reports

The reporting engine respects your structure both ways.

- Pick a single entity from the entity selector and you get a clean, standalone P&L and Balance Sheet for that company alone.
- Pick the parent group and you get a consolidated set, with inter-company eliminations applied automatically, currencies translated where needed, and equity-method investments treated correctly.

This is what makes it possible to answer two questions with the same data: *how is OpCo doing?* and *how is the family doing in total?*

## Practical advice

- **Use a consistent chart of accounts across entities.** If "Legal Fees" is the same account code in OpCo and HoldCo, the consolidated view is materially cleaner.
- **Separate funds in fact, not just on paper.** Pay personal expenses from the personal entity, not from a corporate card with a "directors' loan" plug at year-end. The audit trail is what protects the corporate veil if it is ever tested.
- **Reconcile inter-company balances every period.** If OpCo records a £50,000 liability to HoldCo, HoldCo must record the matching £50,000 receivable. Aethelgard's period-close orchestrator surfaces mismatches; fix them in the period they appear, not at year-end.

## Setting up

Create your entities from the **Entities** section in the sidebar. Set the entity class on each. Where you intend to consolidate, group entities under a parent. Once accounts are flagged inter-company on both sides of any internal balance, consolidation runs automatically when you select the parent in the reporting view.
