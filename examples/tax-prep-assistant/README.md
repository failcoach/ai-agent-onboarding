# Worked Example: Tax Prep Assistant

This is a simpler example than the [Operations Assistant](../operations-assistant/). One person, one workflow, narrow scope. If the Operations Assistant shows what a multi-task agent looks like, this shows what a focused single-workflow agent looks like.

We'll follow Priya. She runs a solo CPA practice with about 40 small-business clients (restaurants, local contractors, small retailers). Her workflow is predictable: monthly bookkeeping reviews, quarterly tax prep, annual filings. The quarterly crunch is killing her weekends. Four times a year she spends two full weekends reviewing QuickBooks exports, chasing clients for missing documents, flagging anomalies, and compiling filing packages.

She doesn't want an agent for everything. She wants an agent for the quarterly crunch.

---

## The Interview (Condensed)

### The Business

- **What's the business?** Solo CPA practice. Small-business bookkeeping, tax prep, and advisory.
- **Who are your customers?** About 40 small businesses, mostly in my local area. Revenue range from $200K to $3M. Mix of restaurants, contractors, retail.
- **How big is the team?** Just me. I use a bookkeeper for a few larger clients, but she's a contractor, not staff.
- **What tools?** QuickBooks Online for client books, TaxDome for document collection and client communication, Google Drive for working files, Excel for my internal tracking.

### The Role

The interviewer asked what eats up her time. Priya's first answer: "quarterly tax prep." The interviewer pushed: what specifically?

- **What exactly happens during quarterly prep?** I pull QuickBooks reports for each client. I review P&L and balance sheet for anomalies (unusual expenses, misclassified income, missing months). I cross-reference against last quarter. I draft emails to clients asking for missing receipts or clarifications. I compile a filing package for each one.
- **Which parts are pattern-matching vs. judgment?** The anomaly-spotting is mostly pattern-matching, the client emails are templated, the package compilation is mechanical. The actual tax strategy and filing decisions are judgment. I don't want an agent anywhere near that.
- **What would a perfect first version of this agent do?** Review the QuickBooks exports I give it, flag anomalies against the previous quarter, draft the follow-up emails for my review, and produce a prep summary I can use to actually do the filing work.
- **Decision authority?** Can decide what counts as an anomaly worth flagging. Can draft emails in my voice. Cannot send any email. Cannot make tax decisions. Cannot communicate with clients directly.
- **What does good look like?** I open the prep summary on a Friday afternoon and have everything I need. The anomalies are real ones, not noise. The draft emails are 90% ready to send. I spend Saturday reviewing and filing, not chasing data.
- **What should it NOT do?** No client contact. No actual filing. No tax strategy. No pricing decisions. No access to anything beyond what I upload for a given prep cycle.

### Tools and Access

- QuickBooks exports (CSV, uploaded by Priya per client per quarter)
- Priya's client roster (simple spreadsheet with business type, typical revenue range, known quirks)
- Email templates she already uses
- Previous quarter's prep summary (for comparison)

No live access to QuickBooks, no TaxDome integration, no Google Drive. Everything goes through Priya uploading files. This matters: the agent doesn't touch anything live, it only reviews what she hands it.

### Memory

- Needs to remember: each client's business type, known quirks ("Bob's restaurant has a weird comp-meal expense pattern that's legitimate"), what was flagged last quarter, Priya's email voice
- Changes quarterly: current prep cycle data, anomalies flagged
- Stays stable: client list, Priya's style preferences, common false-positive patterns

### Feedback and Growth

- **How will you review?** I'll review every flagged anomaly the first quarter. After that, I'll spot-check.
- **When something's off?** Immediately, during the same session.
- **How often updates?** Probably heavy for Q1 while we calibrate what counts as a real flag vs. noise. Then twice a year after cycle wraps.

The interviewer explained the Weekly Check-in and Memory Health Check. Priya pushed back: "My agent won't run weekly. I'll use it four times a year."

The interviewer adapted the cadence, not the pattern. The brief still has a "Weekly Check-in" section -- the trigger just fires at the start of each prep cycle (about quarterly), not every seven days. Same for the Memory Health Check: it runs between cycles instead of every two weeks. The rule stays: the agent initiates the conversation, the owner doesn't have to remember. The frequency matches the work rhythm.

### Timeline Expectation

Priya understood Q1 would be rough. She committed to treating the first quarterly prep as a calibration cycle -- she'd do her normal manual process alongside the agent, compare outputs, and use Q2 onwards as the real workflow.

---

## What Got Generated

### 1. The Agent Brief

See [generated-agent-brief.md](generated-agent-brief.md). Notice it's shorter than Marco's. Narrower scope = shorter brief.

### 2. The Memory Structure

See [generated-memory-structure.md](generated-memory-structure.md). Level 2, but a simpler layout -- no pipeline or project tracking because there isn't any.

### 3. The Feedback Template

See [generated-feedback-template.md](generated-feedback-template.md). Customized for the two outputs Priya actually reviews: flagged anomalies and draft emails.

### 4. The First Quarter Plan

Not a first-week plan -- a first-quarter plan, because the work cycle is quarterly.

**Weeks 1-2 (start of Q1 prep):**
- Upload client roster and prior-quarter summary to memory
- Process 5 client exports as a test batch (smallest clients first)
- Review every flagged anomaly, mark which were real vs. false positives
- Update agent instructions based on the false-positive patterns

**Weeks 3-4:**
- Process remaining 35 clients
- Review in two passes: anomalies first, then email drafts
- Track time spent vs. previous quarter manually
- Note any clients the agent struggled with (complex books, unusual patterns)

**Between Q1 and Q2:**
- Memory health check: what context should persist for next cycle?
- Update the client roster with anything learned (Bob's comp-meals, etc.)
- Adjust flagging criteria based on what was noise

---

## What It Looked Like After Two Quarters

Priya reported back after Q2 wrapped:

**What worked well:**
- Anomaly detection was genuinely useful by Q2. The agent caught three things she would have missed (two misclassified income entries, one duplicate vendor payment).
- Email drafts saved hours. Her voice was captured well after she fed it 10 examples during Q1 calibration.
- The per-client notes in memory paid off. "Bob's comp-meal thing" stopped getting flagged by Q2.

**What needed adjustment:**
- Q1 had too many false positives on small expense variations. Priya added a threshold: only flag variations over 20% or $500, whichever is higher.
- Initial email drafts were too formal. She fed the agent her actual sent emails from last year and the voice tightened up.
- The agent tried to add commentary on tax implications. Priya cut that out of the brief entirely. "Your job ends at flagging. I handle tax."

**What she added:**
- A "common false positives" file in memory that catches the patterns she doesn't want flagged (seasonal businesses, known contractors, etc.)
- A "client-specific quirks" file with one-liners per client

**What she learned:**
- The agent is useful because it has narrow scope. She considered expanding it ("could it also do monthly bookkeeping review?") and decided against it. Quarterly prep is the painful workflow. Monthly review isn't. Adding monthly to the agent's scope would dilute it.

---

## The Takeaway

Priya's Tax Prep Assistant does one thing. That's what makes it good.

Every instinct in the ebook points away from "CEO agents" and toward "roles specific enough that a real hire could do them." A tax prep assistant is a real job. Marco's Operations Assistant is a real job. "AI assistant for my business" is not.

The narrower the scope, the faster the agent gets useful. Priya had a genuinely helpful agent by the end of Q1 because she didn't ask it to be everything.

If her first quarter had been spent building a "solo CPA agent that does bookkeeping review, tax prep, client communication, advisory work, and scheduling" she'd still be debugging it. She isn't. She's doing her filings on Saturday afternoons instead of Saturday-and-Sunday.
