# Give Your Agent a Memory

This is the single thing that finally made it click for me. The moment my agents got proper memory, they went from tools to teammates.

Without memory, every session is groundhog day. You explain the same context. Repeat the same preferences. Rehash the same decisions. The agent starts from zero every single time.

With memory, the agent picks up where you left off. It remembers what you decided last week. It knows your preferences. It builds on previous work instead of starting over.

## The Three Levels

Don't try to build the perfect memory system on day one. Start simple. Your agent will tell you when it's time to upgrade -- that's built into how agents from this kit work. You don't need to monitor this yourself.

### Level 1: Built-in Memory (Start Here)

Claude Code has a built-in memory system that works automatically. It stores memories in a hidden folder inside your project. You don't need to set anything up or find this folder -- Claude Code manages it for you behind the scenes.

**How it works:**
- Tell Claude "remember that we never discount more than 15%" and it saves that
- Tell Claude "remember that our target audience is restaurant owners in the US" and it saves that
- Next session, Claude reads these memories and picks up the context

**What it's good for:**
- Preferences and rules ("always use casual tone", "never mention competitor X")
- Key business facts ("we have 12 employees", "our main product costs $299/month")
- Decisions you've made ("we chose Stripe over Square because...")

**Every two weeks, your agent pauses at the start of a session and audits its own memory.** It counts memories, checks for duplicates, looks for contradictions (old facts that are no longer true). When things are getting cluttered, it won't just silently struggle. It will tell you: "We have 25+ memories and some are duplicated. I'd like to move to a structured docs folder. Here's what that looks like and I can do the migration for you."

You don't need to watch for this yourself. The agent raises it on a schedule, the same way it initiates the weekly feedback check-in.

This level is enough for most people getting started. Expect to use it for a few weeks before the agent suggests moving up.

### Level 2: Structured Documentation

When your agent tells you built-in memory is getting cluttered, the next step is a structured folder. Create a `docs/` directory in your agent's project with organized files:

```
docs/
  KNOWLEDGE_MAP.md           -- Index of what's where (the agent reads this first)
  business-overview.md       -- Who you are, what you do, who you serve
  current-priorities.md      -- What matters right now
  decisions-log.md           -- What you've decided and why
  session-log.md             -- Summary of recent sessions
```

You can add more files as your needs grow (like a known-issues file or client notes). Start with these five.

The knowledge map (`docs/KNOWLEDGE_MAP.md`) is a table of contents that tells the agent where to look for specific information. The agent reads this first and then only opens the files it actually needs. Here's what it looks like:

```
business-overview.md:
  What's in it: Company background, products, customers, team
  Look here when: you need to know who we are, what we do, our customers, our market

decisions-log.md:
  What's in it: Key business and strategy decisions
  Look here when: you need context on pricing, tools, partnerships, strategy choices

current-priorities.md:
  What's in it: What we're focused on right now
  Look here when: you need to know current goals, this quarter's focus, priorities
```

Don't worry about getting the format exactly right. If you're using the interactive interview, it generates this for you. The important thing is that each file is listed with a short description so the agent knows where to look.

**A filled-in example (from the Operations Assistant):**

```
business-overview.md:
  What's in it: Marco's firm, the 15 people, the consulting practice, the client segments
  Look here when: you need to know who we are and what kind of work we take on

current-priorities.md:
  What's in it: This quarter's goals, open hires, the three clients we're expanding
  Look here when: you need to know what we're focused on right now

client-intelligence.md:
  What's in it: Per-client notes -- known sensitivities, billing preferences, stakeholder map
  Look here when: you're preparing a status summary or meeting prep for a specific client

decisions-log.md:
  What's in it: Pricing changes, vendor choices, why we said no to a partnership
  Look here when: you need context on a decision that's already been made
```

See [examples/operations-assistant/generated-memory-structure.md](../examples/operations-assistant/generated-memory-structure.md) for the full version.

**Key principles:**
- **One topic per file.** Don't dump everything into one giant document.
- **Keep files short.** Under 150 lines each. If a file grows too big, split it.
- **Update regularly.** Outdated information is worse than no information. It actively misleads.
- **Delete what's obsolete.** Don't archive. If it's no longer true, remove it.

The agent reads the knowledge map first, then only opens the files it actually needs. This saves time and keeps the agent focused.

### Level 3: Automatic Notes and Databases (Advanced)

Once your agent is handling complex, ongoing work across many sessions, you might want:

**Automatic end-of-session notes** that capture what happened without you doing it manually:
- What you worked on
- What was decided
- What's pending for next time
- Key context that should carry forward

**A database** for agents that accumulate a lot of structured data over time:
- Client interactions over months
- Project status across dozens of workstreams
- Performance metrics over time

This level is overkill for a first agent. It's here so you know it exists. During its memory health check, your agent will suggest this if Level 2 starts feeling limiting. You'll hear something like: "Session documentation is taking up 10 minutes every session. I can set up automatic notes that handle this in the background. Want me to?"

## What to Remember vs. What to Forget

Not everything deserves to be in memory. Here's a simple filter:

**Worth remembering:**
- Decisions and the reasoning behind them
- Preferences and rules that apply across sessions
- Key business context that doesn't change often
- What worked well and what didn't
- Current priorities and focus areas

**Not worth remembering:**
- One-off task details ("write an email to John about the invoice")
- Temporary context that won't matter next week
- Information that changes so fast it'll be outdated by tomorrow
- Anything you can look up quickly when needed

## The Compound Effect

Good memory compounds. Each session builds on the last. After a month, your agent has context that would take a new hire weeks to accumulate. After three months, it understands patterns and nuances about your business that you might not have even articulated yourself.

But only if you maintain it. Memory needs the same care as a good filing system. Review it periodically. Remove what's stale. Update what's changed. The guide on [feedback](04-feedback.md) covers how to make this part of your regular routine.
