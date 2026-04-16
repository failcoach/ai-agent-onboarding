# Memory Structure for Marco's Operations Assistant

This is the Level 2 memory structure generated during the onboarding interview. Marco would create this `docs/` folder inside his Operations Assistant project folder.

---

## Folder Structure

```
docs/
  KNOWLEDGE_MAP.md
  business-overview.md
  current-priorities.md
  decisions-log.md
  session-log.md
  client-intelligence.md       (added after month 1)
```

## KNOWLEDGE_MAP.md

```markdown
# Knowledge Map

## Core Context
business-overview.md:
  purpose: Company background, services, team, tools, key clients
  keywords: who we are, consulting, team, clients, tools

current-priorities.md:
  purpose: This month's focus areas and active initiatives
  keywords: priorities, focus, this month, goals

## Working History
decisions-log.md:
  purpose: Key operational and business decisions with reasoning
  keywords: decided, chose, changed, why

session-log.md:
  purpose: Recent session summaries, newest first
  keywords: last session, worked on, recent

## Client Context
client-intelligence.md:
  purpose: Key client relationships, tiers, dynamics, preferences
  keywords: client, relationship, tier, strategic, history
```

## business-overview.md

```markdown
---
summary: 15-person IT consulting firm. Cloud migrations, security audits, managed
  services for mid-sized companies (50-200 employees). Marco is owner/bottleneck.
updated: 2026-04-16
---

## The Business
IT consulting firm specializing in infrastructure modernization. We help companies
that have outgrown their current IT setup but aren't big enough for a full internal team.

Core services:
- Cloud migrations (AWS, Azure)
- Security audits and compliance
- Managed IT services (ongoing)

## Customers
CFOs and IT directors at companies with 50-200 employees. They know they need to
modernize but don't have the in-house expertise.

## Team
15 people total:
- 10 consultants (the delivery team)
- 2 project managers
- 1 office manager
- 1 sales person
- Marco (owner -- client relationships, business development, and currently the
  operational bottleneck)

## Tools and Systems
- Monday.com -- project tracking, timelines, resource allocation
- HubSpot -- CRM, deal pipeline, client communication history
- Slack -- internal team communication
- Google Workspace -- docs, email, calendar, meeting notes
- QuickBooks -- invoicing and financials (agent does not access this)
```

## current-priorities.md

```markdown
---
summary: 3 priorities this month. [Marco fills in after first session.]
updated: 2026-04-16
---

| Priority | Why | Status |
|----------|-----|--------|
| [Priority 1] | [Why it matters now] | [Status] |
| [Priority 2] | [Why it matters now] | [Status] |
| [Priority 3] | [Why it matters now] | [Status] |
```

## decisions-log.md

```markdown
---
summary: Operational and business decisions. 0 entries so far.
updated: 2026-04-16
---

| Date | Decision | Reasoning | Affects |
|------|----------|-----------|---------|
| 2026-04-16 | Built Operations Assistant agent | Marco spending too much time on status tracking, meeting prep, and follow-ups. Agent handles routine operational monitoring. | Weekly workflow, meeting prep, pipeline tracking |
```

## session-log.md

```markdown
---
summary: Session history, newest first.
updated: 2026-04-16
---

## 2026-04-16 -- Initial setup
- Completed onboarding interview
- Generated agent brief, memory structure, first week plan
- Next: Marco to provide company context details, client tier list, and recent meeting notes
```

---

## Notes on This Structure

**Why Level 2 and not Level 1?** Marco's agent needs to track ongoing projects, client relationships, and a pipeline. That's too much context for simple memory entries. The structured docs let the agent quickly find what it needs.

**Why not Level 3?** Marco is starting out. The manual session documentation and text files are enough for now. If after 2-3 months he's doing daily sessions and managing a lot of data, he can upgrade to automatic session notes or a database.

**The client-intelligence.md file** isn't created on day one. Marco added it after the first month when he realized the agent needed to understand which clients are strategic and what their dynamics look like. This is normal. The memory structure evolves as you learn what the agent actually needs.
