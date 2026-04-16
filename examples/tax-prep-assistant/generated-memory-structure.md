# Memory Structure for Priya's Tax Prep Assistant

This is the Level 2 memory structure generated during Priya's onboarding interview. The layout is simpler than Marco's Operations Assistant because the workflow is narrower -- there's no pipeline, no team, no ongoing priorities to track.

---

## Folder Structure

```
docs/
  KNOWLEDGE_MAP.md
  client-roster.md
  client-quirks.md
  common-false-positives.md
  email-voice.md
  session-log.md
  prior-quarters/
    2026-Q1-summary.md      (added after Q1 wraps)
    2026-Q2-summary.md      (added after Q2 wraps)
```

## KNOWLEDGE_MAP.md

```markdown
# Knowledge Map

## Core Context
client-roster.md:
  purpose: Full client list with business type, typical revenue, filing cadence
  keywords: client, clients, list, who

client-quirks.md:
  purpose: Per-client context the agent needs to know (known patterns, seasonal behavior, legitimate-but-unusual entries)
  keywords: client notes, quirks, known patterns

common-false-positives.md:
  purpose: Patterns that should NOT be flagged despite matching criteria
  keywords: false positive, noise, don't flag

email-voice.md:
  purpose: Priya's email style, with examples
  keywords: voice, tone, email style

## Working History
session-log.md:
  purpose: Session summaries and cycle check-in dates
  keywords: last session, cycle, check-in

## Prior Quarters
prior-quarters/:
  purpose: Past cycle summaries used for year-over-quarter comparison
  keywords: last quarter, prior, comparison data
```

## client-roster.md

```markdown
---
summary: 40 clients. Mix of restaurants, contractors, retail. Revenue $200K-$3M.
updated: 2026-04-16
---

| Client | Business Type | Typical Revenue | Filing Cadence | Notes |
|--------|---------------|-----------------|----------------|-------|
| [Priya fills in during Q1 calibration] | | | | |
```

Priya populates this over her first cycle. She doesn't have to do it all upfront. The agent asks for client context as it processes each file.

## client-quirks.md

```markdown
---
summary: Per-client patterns the agent should treat as normal, not anomalies.
updated: 2026-04-16
---

## [Client Name]
- [Known pattern that looks unusual but isn't]
- [Seasonal behavior to expect]
- [Recurring legitimate exceptions]

## Example entry (after Q1)
## Bob's Diner
- Comp meals show up as "employee benefits" around $200-400/month -- legitimate, don't flag
- December revenue drops ~30% every year (slow season) -- normal
- "Produce vendor cash draws" are how Bob pays his produce supplier -- legitimate
```

This file grows quarter by quarter as Priya teaches the agent what's normal for each client.

## common-false-positives.md

```markdown
---
summary: Pattern-level false positives, not client-specific.
updated: 2026-04-16
---

## Patterns to NOT flag

- Quarterly insurance payments (come through once per quarter, look like spikes)
- Annual software license renewals (legitimate one-time entries)
- [More added as Priya identifies them during Q1]
```

This is the file Priya updates most during Q1 calibration. Every false positive she reviews adds one line here.

## email-voice.md

```markdown
---
summary: Priya's voice for client emails. Direct, warm, never corporate.
updated: 2026-04-16
---

## Voice Notes
- First-name basis with most clients
- Short sentences
- Ask for what you need, briefly explain why
- No "please find attached," no "as per our previous correspondence"
- No legal or tax jargon unless necessary
- Friendly but not chatty

## Example Email 1: Missing Receipts
Subject: Quick favor for Q1 prep

Hi Dave,

I'm working on your Q1 and I'm missing receipts for three equipment purchases in February (see attached).

If you can send those over this week I can keep things on track. If they're lost, no big deal -- let me know and I'll work with what we have.

Priya

## Example Email 2: Clarification Request
Subject: Two quick questions on the March books

Hi Maria,

Two things I want to check before I file Q1:

1. There's a $3,200 vendor payment to "Coastal Services" on March 14. I don't recognize them from prior quarters -- what's this?
2. Your catering income dropped about 40% vs. last March. Anything going on, or is this just seasonal?

Let me know when you have a minute.

Priya

## [More examples as Priya feeds them in]
```

## session-log.md

```markdown
---
summary: Session history. Cycle check-ins and memory audits logged here.
updated: 2026-04-16
---

## 2026-04-16 -- Initial setup
- Completed onboarding interview
- Generated agent brief, memory structure, first quarter plan
- Next: Priya to populate client-roster.md and feed in email voice examples before Q1 prep begins
```

---

## Notes on This Structure

**Why Level 2?** Priya works with structured data (books, client records) across 40 clients. Level 1 memory would get overwhelmed. But she doesn't need Level 3 either -- no database, no continuous logging, because the work is quarterly not daily.

**Why the prior-quarters/ subfolder?** Year-over-quarter comparison is core to the flagging logic. The agent needs to compare Q2 2026 to Q1 2026, not just to "general priors." Storing each quarter's summary as a separate file lets the agent reference the right comparison point.

**What's NOT here:** No priorities file. No decisions log. No pipeline tracking. This agent isn't doing ongoing strategic work -- it's doing one narrow workflow four times a year. The memory reflects that.

**Growth path:** If Priya ever decides to expand the agent's scope (she might, she might not), the memory structure will evolve. Most likely additions: a `recurring-vendors.md` file if flagging rules need more structure, or automatic per-client filing notes if she starts reusing insights across years. Neither is needed on day one.
