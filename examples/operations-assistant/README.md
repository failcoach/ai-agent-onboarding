# Worked Example: Operations Assistant

This example shows what the full onboarding process looks like from start to finish. We'll follow a fictional business owner named Marco as he builds his Operations Assistant using the interview process in this repo.

Marco runs a 15-person IT consulting firm. He's the bottleneck for everything: tracking projects, following up with clients, preparing for meetings, making sure nothing falls through the cracks. He tried using AI a few times but kept getting generic advice that didn't fit his business. He wants an agent that helps him stay on top of operations so he can focus on client relationships and business development.

---

## The Interview (Condensed)

Here's what the interview covered and what Marco said. In practice, each section involves more back-and-forth. This is the condensed version.

### The Business

- **What's the business?** IT consulting. We help mid-sized companies (50-200 employees) modernize their infrastructure. Cloud migrations, security audits, managed services.
- **Who are your customers?** CFOs and IT directors at companies that have outgrown their current setup but aren't big enough for a full internal IT team.
- **How big is the team?** 15 people. 10 consultants, 2 project managers, 1 office manager, 1 sales person, and me.
- **What tools do you use?** Monday.com for project tracking, HubSpot for CRM, Slack for team communication, Google Workspace for everything else. Invoicing through QuickBooks.

### The Role

The interviewer pushed Marco to be specific. His first answer was "help me manage operations." After some back-and-forth:

- **What eats up your time?** Checking in on every active project to see if things are on track. Preparing for my Monday leadership meeting. Following up on proposals that went out but haven't gotten a response. Making sure the consultants have what they need for their current engagements.
- **What would this person do all day?**
  - Review active projects in Monday.com and flag anything behind schedule or at risk
  - Prepare a weekly status summary for the Monday leadership meeting
  - Track outstanding proposals in HubSpot and remind me which ones need follow-up
  - Maintain a running list of open action items from meetings and flag overdue ones
  - Prepare briefing notes before client meetings (recent history, open issues, what we promised last time)
- **Decision authority?** Can prioritize what goes into the weekly summary. Can flag items as urgent vs. routine. Cannot reach out to clients. Cannot commit resources or timelines. Cannot make financial decisions.
- **What does "good" look like?** I walk into Monday's meeting already knowing what's on fire and what's on track. I don't get surprised. Client meetings are prepared, not winging it. Nothing falls through the cracks for more than a week.
- **What should it NOT do?** No client communication. No financial decisions. No team management or performance conversations. No accessing individual consultant billing rates.

### Tools and Access

- Monday.com project data (read-only)
- HubSpot deal pipeline and contact history (read-only)
- Meeting notes from Google Docs
- A "company context" document Marco will write covering how the firm operates, key clients, current priorities

### Memory

- Needs to remember: active projects and their status, client relationships, team capacity patterns, decisions from leadership meetings, Marco's preferences for briefing format
- Changes frequently: project status, deal pipeline, weekly priorities
- Stays stable: company background, key client relationships, team structure

### Feedback and Growth

The interviewer asked how Marco plans to manage the agent ongoing:

- **How will you review its work?** I'll review the weekly summary every Monday before the meeting. Briefing notes I'll scan before each client call. I'll do a proper review of everything at the end of each week.
- **When something's off, how will you tell the agent?** Right away, in the same session. If I wait, I forget the specifics.
- **How often are you willing to update the agent's instructions?** Weekly for the first month. After that, probably when something changes or a pattern shows up.

The interviewer also explained two things that would happen automatically:
- A **weekly check-in** where the agent asks for feedback if it's been 7+ days since the last one. Marco doesn't have to remember. The agent initiates it.
- A **memory health check** every two weeks where the agent audits its own files and proposes changes if things are getting cluttered or stale.

### Timeline Expectation

Marco understood this would take time. He committed to working with the agent daily for the first two weeks, then tapering to 3x/week as it learns his patterns.

---

## What Got Generated

The interview produced four documents. Here they are, exactly as generated.

### 1. The Agent Brief

See [generated-agent-brief.md](generated-agent-brief.md) -- this is the instruction file that Marco would put in his Operations Assistant folder. (In Claude Code, this file is called CLAUDE.md. It's what Claude reads automatically when it opens the folder. Think of it as standing instructions for the agent.)

### 2. The Memory Structure

See [generated-memory-structure.md](generated-memory-structure.md) -- the starting docs/ folder for the agent.

### 3. The Feedback Template

See [generated-feedback-template.md](generated-feedback-template.md) -- customized for the Operations Assistant role, with specific checkboxes for the types of outputs Marco reviews.

### 4. The First Week Plan

**Day 1-2: Get oriented**
- Read the company context document Marco provides
- Review active projects in Monday.com data
- Review current deal pipeline in HubSpot data
- Produce a first draft of the weekly status summary (Marco will review heavily and give feedback)

**Day 3-4: Start the routine**
- Prepare briefing notes for Marco's next two client meetings
- Identify any overdue action items from the last two weeks of meeting notes
- Produce second weekly summary incorporating Marco's feedback from the first draft

**Day 5: Calibrate**
- Marco reviews the week. What's working? What's off? What's missing?
- Update the agent's instructions based on findings
- Update memory with any context that kept coming up

---

## What It Looked Like After One Month

Marco reported back after four weeks:

**What worked well:**
- Weekly status summaries became reliable by week 2. He stopped dreading Monday mornings.
- Client meeting prep was the biggest time saver. The agent pulled together recent history, open issues, and commitments in 5 minutes. Used to take him 30.
- The action item tracker caught things he'd forgotten about. Two client follow-ups that would have slipped.

**What needed adjustment:**
- The first version flagged too many things as "at risk." Marco had to calibrate what actually counts as a risk vs. normal project fluctuation. Added specific criteria to the agent's instructions.
- Meeting summaries were too detailed. Marco wanted bullet points, not paragraphs. Quick feedback fixed this.
- The agent didn't initially understand which clients are strategic vs. routine. Marco added a client tier list to the memory.

**What he added:**
- A "client intelligence" memory file tracking relationship dynamics, preferences, and history for key accounts
- Monthly review prompt: once a month, the agent looks across all projects and flags patterns (recurring delays, resource crunches, clients needing more attention)

---

## The Takeaway

Marco's Operations Assistant isn't magic. It's the same work a good human executive assistant would do. The difference: it's available every session, it never forgets what it was told, and it cost $0 to hire.

But it only works because Marco invested the time to set it up properly. The interview forced him to articulate what he actually needed. The first two weeks required daily attention. The instructions got refined multiple times.

If he'd spent one afternoon and expected perfection, he would have gotten the same garbage everyone else gets and given up.

He didn't. And now he has an extra 5-6 hours a week.
