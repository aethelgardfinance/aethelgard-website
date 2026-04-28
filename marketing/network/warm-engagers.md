# Warm Engagers — first organic engagement signals

Tracks named people who have engaged with Aethelgard's LinkedIn content. Updated manually after each weekly stats refresh; eventually auto-populated by the `/partners` and `/comments` commands once built.

**Purpose:** these are the people most likely to introduce, refer, or buy. Engagement is the early ICP signal we have before the buyer list exists.

---

## Engagement log

### 2026-04-28 — first organic signals on founder content

Cherie's Wednesday founder-story post (5 days before this entry) and Sunday composite-vignette follow-up both pulled named reactions. Cherie has confirmed both names below are **1st-degree connections** — warm, immediately reachable.

| Name | Engagement | Connection | Status |
|---|---|---|---|
| **Vijay Jayasuriya** | Reacted to founder-story post (the *"Why I built Aethelgard"* post) | 1st-degree | Active ICP signal |
| **Shashin Shah** | Reacted to follow-up post (*"A week after discussing the motivations…"*) | 1st-degree | Active ICP signal — second post in the series, suggests sustained attention |

Both names need to be added to `network/connections-1st.csv` when Cherie does the LinkedIn export pass. Until then they live here.

### Suggested next moves (low-cost, high-trust)

These are *founder-personal* moves; Claude does not action them. Cherie performs them in the Friday engagement window.

1. **Reply personally** to each reaction — short, warm, NOT a pitch. *"Thanks Vijay — this resonated with you, I'd value your thoughts on whether the gap I'm describing matches what you've seen."* Or whatever feels natural in the relationship. The engagement is *more valuable* than the buy at this stage, because it signals attention from inside Cherie's circle.
2. **Light DM follow-up** within the week — only if there's a real basis. *"Saw you reacted to the post — happy to walk you through the demo if you'd ever find it useful. No pressure if not."* This is the weakest possible CTA, which is the right strength for warm-but-untested connections.
3. **Score for ICP fit** when ready — see `partner-targets.md` (to be built).

### What NOT to do

- ❌ Mass-DM either of them from a templated message
- ❌ Add them to a marketing list without consent
- ❌ Tag them in subsequent posts ("as Shashin Shah noted…") — performative and breaks the conversation
- ❌ Treat the reaction as a buying signal — it's an *attention* signal; the gap to a paying customer is several steps

---

## Tracking schema (for future entries)

When new engagers appear, log with:

| Field | Example |
|---|---|
| Name | First Last |
| Engagement | What they did + which post + date |
| Degree | 1st / 2nd / 3rd |
| ICP-fit signal (if known) | "Likely Ring 1 — sold business, multi-entity" |
| Action taken | "Replied; DM'd; intro'd to X; nothing yet" |
| Date logged | YYYY-MM-DD |

---

## What this file becomes

This is the seed file for the `/partners` command (planned in `plan/90-day-plan.md`, Phase 2). When that ships, it will:
- Read this file as warm-engager input
- Cross-reference against the LinkedIn 1st-degree connections export
- Score each entry for ICP fit and multiplier potential
- Output a ranked outreach list with per-person angle suggestions

Until then, this file is hand-maintained.
