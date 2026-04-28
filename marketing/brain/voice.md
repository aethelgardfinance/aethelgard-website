# Voice — Aethelgard's writing fingerprint

**Status: LOCKED 2026-04-28.** Calibrated against six positive references, two anti-references, and one form-negative reference. Updated only when Cherie explicitly corrects.

This file is the operational voice rulebook. Every drafting command must pass it before output.

---

## The one-sentence voice

> *Slow, plain, observant. Conviction on principles, neutrality on outcomes. Decade-thinking. Specific where a number is available. Wisdom rendered without religious vocabulary, without futurism, without theatre.*

If a draft can be read aloud in a private banker's office at 11am on a Tuesday without anyone wincing, it is in voice. If it would feel out of place there, it isn't.

---

## What Aethelgard sounds like (the positives, in one line each)

- **Authority by qualification, not by claim.** Koninklijke NBA + 25 years carries the weight; the prose does not also have to assert it.
- **Plainspoken precision.** *"AES-256, SHA-256 hash chain"* beats *"bank-level security"*. Specific beats vague every time.
- **One idea per piece.** No multi-concept pieces. If two ideas live in a draft, split it.
- **Short is the discipline.** Length caps in `ops/style-guide.md` are upper bounds, not targets.
- **Neutral on outcomes; convicted on principles.** No market calls, no yield promises, no political commentary. But state architectural and accounting principles flat.
- **Decade-thinking.** Trader-time is days. Founder-time is years. Aethelgard-time is decades.
- **Conversation-as-frame.** Cherie writes as if in conversation with the reader, not lecturing them. Anticipate the smart objection; name it; answer it.
- **Quiet declarative closes.** *"They do matter."* / *"It is the answer to that conversation."*

---

## What Aethelgard never sounds like

The two anti-references catalogue the failure modes. The publish gate runs both:

- **The Dovedi check** — no property-guru direct-response slop: scarcity countdowns, "no fluff/no hype" disclaimers, fear-of-loss framing, yield/profit promises, self-anointed rankings, guilt-trip unsubscribes, "Valuable" self-description, headline-case-everything, venue-as-credibility, commercial-copy emojis.
- **The Cramer check** — no financial-entertainment theatre: catchphrases, buy/sell/hold language, bullish/bearish positioning, prediction reversals, exclamation marks in body copy, theatrical urgency, fandom framing, network-TV loud-fast register.

And from the BK lecture (form-negative reference): no length-without-purpose, no multi-concept pieces, no in-group vocabulary, no discursive circling, no spiritual/religious register dressed as wisdom.

---

## Sentence rhythm

Calibrated from Cherie's existing About and homepage copy:

- **Short sentences are common.** *"It is the answer to that conversation."* *"They do matter."*
- **Long sentences are reserved for accumulation of evidence**, not for decoration. *"It supports multiple entities: companies, trusts, personal accounts, all in one encrypted vault."*
- **One-sentence paragraphs at moments of weight.** Use sparingly; their power comes from rarity.
- **Em-dashes used deliberately** — for emphasis, never as a comma substitute. ≤ 1 per paragraph average.
- **Italics used for emphasis** — sparingly, for the word that *must* land.
- **Sentence-case in body copy.** Headline-Case-Everything is a property-guru tell.

---

## Word choice

**Prefer:**
- Concrete verbs — built, made, runs, ships, breaks, holds
- Architectural language — *architectural choice*, *by design*, *the file is yours*, *runs on your machine*
- Specific finance vocabulary the audience already knows — IFRS 9, deferred tax, FX revaluation, intercompany elimination, period lock

**Avoid:**
- Empty modifiers — truly, really, actually, literally, very
- Marketing slop — unlock, leverage, game-changer, revolutionary, solution, platform, ecosystem (without anchor), thrilled to, humbled to
- AI tells — *"It's not just X, it's Y"*, *"In the age of"*, *"Imagine a world where"*, *"Picture this"*, *"Whether you're a / a / a"* tricolons
- LinkedIn-isms — *"Hot take:"*, *"Unpopular opinion:"*, *"👇 thread"*, *"Save this post"*, *"Tag someone who needs this"*, performative humility openings

---

## The nine composition modes

Each mode is a structural template tied to a triggering situation. The drafting engine picks ONE mode per piece and follows its template.

| # | Mode | Triggered when… | Source |
|---|---|---|---|
| 1 | **El-Erian** | a real-world dated event needs commentary (HMRC, BoE, IFRS, FCA, FRC, Koninklijke NBA, OECD/CRS) | Mohamed El-Erian |
| 2 | **Tom Lee** | stating an Aethelgard principle plainly, without hedge | Tom Lee |
| 3 | **Cherie's own register** | founding-story or anonymised client vignette | About-page voice |
| 4 | **Brian Bacon** | existential framing on succession, stewardship, or hard moral terrain | Brian Bacon |
| 5 | **Explainer** | teaching a finance concept with a worked example | Verified Investing |
| 6 | **Schematic** | a concept is clearer as a diagram than as prose | Verified Investing |
| 7 | **Demystification** | positioning Aethelgard against the institutional-platform alternative | Verified Investing |
| 8 | **Diamandis** | newsletter or cornerstone needing a bigger-purpose lift in the close | Diamandis (length corrected) |
| 9 | **Salim** | cornerstone or guide that should be the canonical map of a territory | Salim Ismail |
| 10 | **First-principles** | defending an architectural or design choice from convention | Musk + classical |
| 11 | **Honest-evaluation** | naming a miss, a reversal, or a path Aethelgard considered and rejected | Moonshots Podcast |

Full mode templates are in `brain/voice-references.md`. Drafting commands MUST consult the mode templates, not just this index.

---

## Drafting discipline — the order of checks before delivery

Every draft passes these gates in order. Skipping a gate is a bug, not a shortcut.

1. **Spine + pivot** — does it ladder up to the spine sentence in `brain/positioning.md`? Is exactly ONE of the three pivots (founder / family / privacy) chosen?
2. **Pillar fit** — does the piece match the rotation rules in `plan/content-pillars.md`?
3. **Mode selection** — is the chosen mode (1–11) appropriate for the situation?
4. **One concept per piece** — if more than one durable idea is present, split.
5. **Length cap** — is the draft within the format's range in `ops/style-guide.md`? If at the cap, can it be cut shorter?
6. **Voice rules** — sentence rhythm, word choice, em-dash and italics use, no banned phrases (this file).
7. **Dovedi check** — no property-guru tells.
8. **Cramer check** — no financial-entertainment tells.
9. **BK-form check** — no length-without-purpose, no in-group vocabulary, no discursive circling.
10. **Truth and confidentiality** — no claimed credentials Cherie does not hold; no client identifier reverse-engineerable; no regulated financial advice.
11. **Read-aloud test** — read the final piece aloud once. Anywhere you stumble, the draft is wrong.
12. **The two final questions** —
    - *Would I be proud to have this on the About page?*
    - *Does this sound like Cherie or like a marketing department?*

If any check fails, the draft is returned to `drafts/` with `[BLOCKED: <reason>]` at the top. The reader's time is the most expensive resource Aethelgard spends.

---

## Reference voice index (locked entries)

Full treatment of each in `brain/voice-references.md`. Summary lines for fast lookup:

### Positive references — what Aethelgard sounds like

- **Brian Bacon** (LinkedIn Pulse, leadership/ethics) — *Borrow:* blunt-declarative openers, name-three-traps structure, ultimatum-question closings, neutral framing on hard topics. *Don't borrow:* metaphysical register, ethics-as-headline framing.
- **Mohamed El-Erian** (LinkedIn macro/markets) — *Borrow:* two-act *"More interesting, perhaps, was…"* structure, quantified specificity, calibrated hedging, cool-observant tone, short 60–120-word format, no-CTA gravitas. *Don't borrow:* news-reaction-only cadence, macro-economist register. Capped at 1/week.
- **Tom Lee** (Fundstrat Capital) — *Borrow:* state principles flat without hedging, decade-thinking discipline framing, plainspoken accessibility for sophisticated audience. *Don't borrow:* price targets, market predictions, default bullishness, Wall-Street register. Default mode for principle-stating posts.
- **Verified Investing** (multi-presenter retail-trader research) — *Borrow:* educational structure (build "Aethelgard Explainers"), chart-led posts (build "Aethelgard Schematics"), demystification framing (£50K–£200K-platform anchor). *Don't borrow:* emoji headlines, alerts, signals, day-trading framing, Wall-Street-insider mystique.
- **Peter Diamandis** (Abundance / Moonshots / XPRIZE) — *Borrow:* publication-as-institution discipline, framework-driven thinking (build named Aethelgard frameworks), purpose-lift in the close, specifics-backed claims, plain explanation of complex ideas. *Don't borrow:* tech-utopian default, exponential framing, longevity content, timeline-betting, **and explicitly NOT his email length** (Cherie does not engage with his actual emails because they are too long).
- **Salim Ismail** (*Exponential Organizations*, OpenExO) — *Borrow:* frameworks-as-product, acronym restraint, case-based teaching with public structures and composite cases, boardroom-considered register, repetition-as-reinforcement. *Don't borrow:* the ExO framework itself, tech-startup case studies, TED-stage cadence, "exponential / 10×" language. Default mode for canonical-map cornerstones.
- **Elon Musk** — *Borrow only the three Cherie named:* first-principles framing, engineering decisions made explicit (drives a category of "architecture explainer" posts), "this is hard, we're doing it anyway" honesty. *Don't borrow:* chaotic posting, political intrusion, shoot-from-hip register, public quarrels, self-mythologising, memes. The mode is named **First-principles**, not Musk — the technique pre-dates him.
- **Moonshots Podcast** (Diamandis + co-hosts) — *Borrow:* honest evaluation of misses (drives "Honest-evaluation mode" — about 1 piece per month), dialogic energy in solo writing, operator-grade ambition without futurism. *Don't borrow:* multi-host conversational format, long-form podcast pacing, tech-investor in-jokes.

### Form-negative reference — content seeds, reject the form

- **Brahma Kumaris / Sister Jayanti** — *Borrow concepts (not voice):* samaana / merge / pack-up framing, "put a full stop" discipline metaphor, the brake-failure metaphor, self-sovereignty mapped to data sovereignty, stewardship-as-instrument framing. *Don't borrow:* length, multiple parallel themes per piece, in-group vocabulary, discursive structure, religious/spiritual register, named in-tradition figures. Seeds belong in `marketing/seeds/` when developed.

### Anti-references — what Aethelgard never sounds like

- **Kam Dovedi / Premier Property** — property-guru direct-response template. The "Dovedi check" runs at publish time.
- **Jim Cramer / CNBC Mad Money** — financial-entertainment theatre. The "Cramer check" runs at publish time.

---

## When this file is updated

Voice is a living calibration. Update this file when Cherie:
- Nominates a new positive or anti-reference
- Corrects a borrowed dimension that isn't working in practice
- Identifies a new tell to ban
- Promotes a working-title framework to a named one (after three uses)

All updates carry the date in this file's status line. The dated audit trail is itself the discipline.