# Aethelgard Marketing Operating System

The single source of truth for everything Aethelgard says, plans, publishes, and learns.

This folder is read by Claude Code at the start of every session. Future-you and future-Claude both look here first.

---

## How it works in one paragraph

Cherie records a 30-minute **seed** every Monday by 10:00 (wherever she is in the world). Claude expands the seed into all weekly channel-ready drafts (LinkedIn × 3, blog, newsletter section, carousel). Cherie edits in ~60 minutes. Drafts are published, archived, and measured. The system reads the archive and the stats every week to get smarter about what works.

Total weekly cost to Cherie: ~2.5 hours. Output: 3 LinkedIn posts, 1 carousel, ½ blog post, ¼ newsletter issue, plus partner-outreach proposals.

---

## Folder map

| Folder | What lives here | Who writes it |
|---|---|---|
| `brain/` | The durable WHY/WHAT/HOW of Aethelgard — product, ICP, voice, positioning, pricing, credentials | Cherie + Claude, updated rarely |
| `plan/` | Strategy docs — 90-day plan, content pillars, channel strategy, KPIs, 50-topic backlog | Cherie + Claude, reviewed quarterly |
| `archive/` | Every published post/article/issue, with metadata and metrics | `/publish` command, automatic |
| `stats/` | LinkedIn and newsletter analytics — CSVs in, summaries out | `/stats` and `/comments` commands |
| `network/` | LinkedIn connections export + scored partner targets + outreach log | `/partners` command |
| `seeds/` | Cherie's raw Monday seeds | Cherie, weekly |
| `drafts/` | AI-expanded drafts awaiting Cherie's edit | `/draft` command |
| `ops/` | Style guide, publish checklist, prompts powering each command | Claude, updated as the system learns |

---

## The weekly rhythm

| When | What | Who | How |
|---|---|---|---|
| Monday 10:00 local | Seed | Cherie | `/seed` (30 mins, voice memo OK) |
| Monday afternoon | Expand to 6+ drafts | Claude | `/draft` |
| Tuesday morning | Edit drafts | Cherie | ~60 mins, kill AI tells, sharpen voice |
| Tuesday afternoon | Schedule | Cherie | Buffer/Hypefury → LinkedIn; Beehiiv → newsletter; Astro → blog |
| Throughout week | As each piece ships | `/publish` | Moves draft → archive, captures URL |
| Friday | Authentic engagement | Cherie | 30–60 mins, comments + DMs (never automated) |
| Sunday | Stats refresh | Cherie + Claude | Export LinkedIn CSV → `/stats` |
| Monthly | Retrospective | Claude | `/retro` reads archive + stats → "what to double down on" |

---

## Why a flat-file repo and not a SaaS

- **Auditable** — every change is git-tracked
- **Owned** — survives any vendor going away
- **Composable** — Claude reads and writes it natively, no API keys for the brain layer
- **Private** — same architecture principle as Aethelgard itself: your data on your machine

---

## For future Claude sessions

If you are reading this in a future session: **start with `brain/` then `plan/`**. Those two folders contain everything you need to draft in Cherie's voice and represent the company correctly. Do not invent positioning. Do not deviate from the spine sentence. When Cherie corrects something, update the relevant brain file before continuing.

If asked to draft anything publishable, run the `ops/checklist-publish.md` gate before delivering.
