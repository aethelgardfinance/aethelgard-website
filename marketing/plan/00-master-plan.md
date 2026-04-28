# Master Plan — Aethelgard Marketing Operating System

**Status:** Approved 2026-04-28. Build in progress.
**Owner:** Cherie (founder) + Claude (CMO co-founder)
**Review cadence:** End of each 30-day phase.

---

## What we're building

A repo-resident system that:

1. **Remembers** — durable brain layer holding the WHY/WHAT/HOW of Aethelgard, PDF Studio, ICP, positioning, voice, and pricing
2. **Drafts** — slash commands that turn a weekly 30-minute seed into channel-ready content for LinkedIn, blog, and newsletter, in Cherie's voice
3. **Measures** — weekly LinkedIn stats ingestion and comment triage, plain-English summaries with outliers flagged
4. **Maps the network** — scores 1st-degree LinkedIn connections against ICP fit and multiplier value, surfaces 2nd/3rd-degree introductions, logs outreach
5. **Learns** — monthly retrospective synthesises archive + stats into "double down on this, drop that"

---

## What we're explicitly NOT building

- A CRM (we use a flat-file repo on purpose)
- An autoposter (Cherie approves every published piece — voice has to stay hers)
- A growth-hack stack (no engagement pods, no follower-bait, no AI reply farms)
- Automated 2nd/3rd-degree LinkedIn harvesting (violates ToS — we do this manually-assisted)

---

## The weekly operating rhythm

| When | What | Who | Tool |
|---|---|---|---|
| Monday 10:00 local | 30-min seed | Cherie | `/seed` |
| Monday PM | Expand seed → 6+ drafts | Claude | `/draft` |
| Tuesday AM | Edit drafts (~60 mins) | Cherie | manual |
| Tuesday PM | Schedule everything | Cherie | Buffer / Beehiiv / Astro |
| As pieces ship | Promote to archive | Claude | `/publish` |
| Friday | Authentic engagement | Cherie | LinkedIn (manual) |
| Sunday | Stats refresh | Cherie + Claude | `/stats`, `/comments` |
| End of month | Retrospective | Claude | `/retro` |

**Total Cherie time: ~2.5 hours/week.**

---

## The four content pillars

Rotate weekly. Never deviate.

1. **Technical authority** — IFRS 9, deferred tax, FX revaluation, intercompany elimination, explained for the founder without a CFO. *This is the moat — no competitor can fake it.*
2. **Founding story / client vignettes** — anonymised, emotional, sticky, never preachy.
3. **The succession angle** — soft, occasional, unforgettable. Highest-share content.
4. **Contrarian takes on wealth-tech** — why Xero is not for your life; why £50K/yr platforms fail HNW individuals; why local-first is a feature for the user, not the vendor.

**Banned formats:** motivational quotes, "10 things I learned" lists, generic hustle content, AI-generated emoji-list posts.

---

## The Ideal Customer Profile (summary — full version in `brain/icp.md`)

**Ring 1 — Bullseye**
- Founder-operator with exit / mid-exit, £3M–£40M, multi-entity, UK/NL/DE/CI/SG/UAE
- Family principal, sub-£50M, succession-aware

**Ring 2 — Multipliers**
- Koninklijke NBA peers, ICAEW/ACCA HNW practitioners, STEP trustees, boutique IFAs

**Ring 3 — Privacy-weighted buyers**
- Crypto wealth, expat wealth (HK→UK, RU→EU, MENA), privacy-maxi tech founders

**Anti-ICP:** YNAB-happy users, PAYE-only, "does it sync with my bank?" askers, £200M+ family offices.

---

## Channel strategy (full detail in `plan/channel-strategy.md`)

| Channel | Priority | Use |
|---|---|---|
| LinkedIn (Cherie's personal profile) | **Primary** | 3 posts/week, founder-led, 4-pillar rotation |
| Owned newsletter (Beehiiv) | **Primary** | Monthly long-form, sign-up on every page |
| Website blog | **Secondary** | 2000–3500 words, SEO cornerstones, biweekly |
| Strategic partnerships | **Secondary** | 5 hand-picked allies year 1 |
| Podcast appearances (guest) | **Secondary** | 1/quarter |
| Reddit / niche communities | **Surgical** | Answer-only, never promotional |
| Facebook | **No** | Wrong demographic, hurts positioning |
| Twitter / X | **No** | Low signal for this audience |
| TikTok / Instagram | **No** | Wrong audience |

---

## 30-60-90 day plan

### Days 1–30 — Foundation
- Scaffold `marketing/` ✅
- Write brain layer (product, pdf-studio, icp, positioning, voice, pricing, credentials) ✅ (in progress this session)
- Lock voice profile after Cherie sends 5–10 reference posts
- Write 90-day plan, content pillars, channel strategy, KPIs
- Generate 50-topic backlog
- Stand up Beehiiv, embed sign-up site-wide
- Build `/seed`, `/draft`, `/publish` slash commands
- First seed → first published LinkedIn post

### Days 31–60 — Traction
- Build `/stats`, `/comments`, `/partners` commands
- Cherie exports LinkedIn connections; first 25 partners scored
- 5 strategic partners identified and approached
- 2 podcast pitches sent
- First newsletter issue ships
- 5 cornerstone blog posts published
- Design Partner cohort launched (10 ICP customers, free Lifetime in exchange for case-study material)

### Days 61–90 — Compounding
- 2 anonymised case studies published
- First podcast appearance lands
- First `/retro` informs Q2 doubling-down
- Small paid lookalike test (£500–£1500) — only if buyer list ≥ 50

---

## KPIs — what we measure

**Primary (revenue-linked):**
- Paying customers per quarter, segmented by tier (Personal / Sovereign / Corporate / Lifetime)
- PDF Studio standalone subscriptions
- Qualified inbound demos / design-partner conversations

**Secondary (leading indicators):**
- Newsletter subscribers and open rate
- LinkedIn impressions per pillar, top 5% post analysis
- Partner intros booked

**Vanity metrics we ignore:**
- LinkedIn follower count in isolation
- Website traffic without conversion context
- Blog post shares without sign-up attribution

---

## The voice profile — pending input

Awaiting from Cherie:
- 5–10 LinkedIn posts she'd point at and say *"this is the voice"*
- 2–3 posts that make her cringe — equally important

When received, Claude codifies into `brain/voice.md`. Every drafting command must pass voice.md before output.

---

## What this plan depends on

The single non-negotiable: **Cherie commits to a 30-minute seed every Monday by 10:00 local time, wherever she is.** ✅ Confirmed.

Without that one input the whole system collapses. With it, everything else compounds.

---

## Decision log

| Date | Decision | Rationale |
|---|---|---|
| 2026-04-28 | Approved folder structure | Flat-file repo for auditability, ownership, composability |
| 2026-04-28 | No Facebook, no Twitter, no TikTok | Wrong audience, hurts premium positioning |
| 2026-04-28 | LinkedIn analytics tier 1 (manual CSV export) | 5 mins/week, no tooling cost until signal proven |
| 2026-04-28 | Beehiiv recommended for newsletter | Free to 2,500 subs, owns the data, better deliverability than Substack |
| 2026-04-28 | Cherie commits to Monday 10:00 seed | System depends on this single input |
