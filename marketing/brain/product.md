# Aethelgard — Product Brain

The durable WHAT, WHY and HOW of the core product. Update only when the product itself changes.

---

## What it is, in one sentence

Aethelgard is a **professional-grade, double-entry accounting application** for individuals managing serious wealth — built to run **entirely on the user's machine**, with **AES-256 encryption** and a **SHA-256 tamper-evident hash chain**.

---

## What problem it solves

The gap between consumer budgeting apps (YNAB, Copilot, Emma) and institutional wealth platforms (Addepar, Dynamo, Masttro). The first are wrong-job; the second cost £50K–£200K/year and require a team to operate.

The people who fall into that gap — founder-operators with exits, family principals, HNW individuals with multi-entity structures — currently patch together spreadsheets and outsource complexity to their accountant. Neither approach answers the simplest, hardest question:

> "What do I own, in one place, today?"

Aethelgard answers it.

---

## What it actually does

A double-entry ledger that supports:

- **Multi-entity** — companies, trusts, personal accounts in one encrypted vault
- **Multi-currency** with IFRS-compliant FX revaluation
- **Group consolidation** with intercompany elimination
- **Fixed assets** and depreciation schedules
- **Accruals and prepayments**
- **Hedge accounting** (IFRS 9)
- **Deferred tax** workings
- **Illiquid asset revaluations**
- **Period locks** and reconciliation
- **SHA-256 tamper-evident hash chain** — every journal entry cryptographically linked to the previous; any historical tampering breaks the chain

All built as a Registered Accountant (Koninklijke NBA) would expect. **Not approximate. Not "near enough." Correct.**

---

## How it runs — the architecture decisions

These are not implementation details. They are the product.

1. **Local-first, by architectural choice.** Aethelgard runs on the user's device. The vault is an encrypted SQLite file. No cloud. No telemetry. No background sync unless the user configures their own WebDAV target (Nextcloud, NAS, any WebDAV-compatible storage).

2. **AES-256 encrypted vault.** Even Aethelgard cannot read it.

3. **Zero telemetry.** No analytics, no crash reports, no calls home.

4. **The user owns the file.** It can be backed up, moved, archived, and remains usable indefinitely. There is no subscription lock-in for the ledger itself.

5. **Tamper-evident by hash chain.** Every entry is cryptographically anchored to the previous one.

These decisions are not negotiable. They are the product's reason to exist.

---

## Who it's for

See `brain/icp.md`. Summary: founder-operators with exits, family principals sub-£50M, HNW privacy-conscious individuals, and the multipliers (Koninklijke NBA peers, STEP trustees, HNW IFAs) who recommend tools to them.

---

## Who it is *not* for

- People who'd be happy with YNAB or a single bank dashboard
- PAYE / W-2 only earners with no entities
- Anyone whose first question is "does it sync with my bank?"
- £200M+ family offices already on Addepar

---

## Pricing tiers

See `brain/pricing-tiers.md`. Current tiers: Personal, Sovereign, Corporate, Lifetime. PDF Studio is included free with any Aethelgard licence; £99/year standalone.

---

## Platform

**Windows at launch.** Mac on the roadmap. Cross-platform consistent vault format.

Distribution: signed installers via the public release repo at `github.com/aethelgardfinance/aethelgard-releases`.

---

## The two narratives that sell it

The product can be told two ways depending on audience. Both are true. Both are in the founder's own words on the website. Pick one per piece of content; never dilute by mixing.

### Narrative A — The accounting narrative
*"There's no good tool between Xero and Addepar. Spreadsheets aren't a system; they're a coping mechanism. Aethelgard is what professional accounting looks like when it's built for one person managing real complexity."*

### Narrative B — The succession narrative
*"At some point — for all of us — someone else will need to understand what we own. They will arrive at this task at a moment of grief or urgency. The records people leave their successors are almost universally inadequate. Aethelgard is, at one level, an accounting application. At another, it is the answer to the conversation that should happen while it can happen."*

Narrative A converts founders. Narrative B converts family principals. Both convert privacy buyers.

---

## What we don't say about the product

- We don't claim "AI-powered" anything. Aethelgard is not an AI product.
- We don't compare on price to consumer apps — wrong frame.
- We don't promise bank sync. We don't have it. It's a feature, not a gap.
- We don't say "secure" — we say *encrypted, local, and not on our servers.* Specific beats vague.
- We don't promise mobile. Desktop is the right form factor for this work.

---

## The moat

Three layers, in order of durability:

1. **Cherie's Koninklijke NBA + 25 years HNW practice.** No SaaS marketing team can fake this. The product correctness comes from the founder's expertise, not from chasing customer feedback.
2. **Local-first architecture.** Cloud-first competitors cannot retrofit this without rebuilding. It is a permanent strategic difference.
3. **The succession framing.** Nobody else in this category talks this way. It is emotionally true and commercially defensible.
