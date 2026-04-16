# Manage Your Agent Like Your Best Employee

Setting up an agent is not a one-time event. It's the beginning of an ongoing relationship. The same way a good manager invests in their people continuously, you need to invest in your agent continuously.

The people who fail with AI agents are the same people who fail with human employees: they expect results without feedback, want performance without investment, set it up once and blame it when things drift.

## The 24-Hour Rule

In people management, there's a principle: give feedback within 24 hours or don't bother. By next week, the context is gone. The moment has passed. The feedback lands flat.

With AI agents, this translates to: give feedback in the same session, or at the start of the next one. Don't let three sessions go by before mentioning that the output style has been off. By then, the agent has reinforced the wrong pattern multiple times.

**Right after the task:**
- "That email draft was too formal. We're a casual brand. Rewrite it like you're talking to a friend."
- "The analysis was solid but I needed it broken into sections. Next time, use headers for each category."
- "Perfect. Exactly the format I wanted. Keep doing it this way."

Positive feedback matters too. If the agent nails something, say so. It reinforces what good looks like. If you only correct mistakes, the agent doesn't know what to keep doing.

## Three Types of Feedback

### 1. Session Feedback (In the Moment)

Quick corrections during a work session. These adjust the current task but don't change the agent's permanent instructions.

- "Make this shorter."
- "Wrong tone. More direct."
- "You're missing the customer perspective here."

This is like telling an employee "fix this before you send it." Immediate, specific, task-level.

### 2. Instruction Updates (Permanent Changes)

When you notice a pattern, not just a one-time mistake, update the agent's brief or memory.

**Signs you need an instruction update:**
- You've given the same session feedback three times
- The agent keeps making the same type of mistake
- Your business has changed and the old instructions don't fit

**How to update:**
- Open the agent's brief (its CLAUDE.md or instructions file)
- Add or modify the relevant section
- Be specific: "When writing customer emails, always open with their name and reference their last interaction" is better than "be more personal"

### 3. Memory Updates (Context Changes)

When something about your business changes that the agent should know going forward.

- New product launched
- Pricing changed
- Key hire or departure
- Strategy shift
- New competitor entered the market

Update the relevant memory file. If using Level 1 memory, tell the agent to remember the new fact. If using Level 2, update the appropriate document.

## The Weekly Check-in (Your Agent Will Remind You)

Here's the thing: most business owners won't remember to do a weekly review. Life gets busy. The agent is producing decent work. You skip the review this week, then next week, then it's been a month and things have drifted.

That's why every agent built with this kit has a **weekly check-in built in**. You don't have to remember. The agent does.

At the start of each session, your agent checks when the last check-in happened. If it's been 7 or more days, it pauses and says something like: "Before we dive in -- it's been a week since our last check-in. Can we spend 5 minutes on how things are going?"

Then it walks you through four questions:

1. **What went well this week?** What outputs did you use without editing?
2. **What kept needing correction?** Any patterns in the mistakes?
3. **What's missing?** Is there context the agent should have but doesn't?
4. **What changed?** Has anything in your business shifted that the agent doesn't know about yet?

Five minutes. That's it. The agent takes your answers, updates its instructions or memory where needed, and logs the check-in. Then you move on to the day's work.

This is the AI version of a one-on-one meeting. The difference: your agent is the one who puts it on the calendar. Not you. It keeps things on track before small issues become big problems.

**Let it happen.** When your agent asks for the check-in, don't skip it. It's the single most effective habit for keeping your agent sharp.

## The Feedback Template

Use this structure when giving significant feedback. You don't need it for quick corrections, but it helps for meaningful course adjustments:

```
What I asked for:
[The task or output you're reviewing]

What worked:
[Be specific about what was good]

What didn't work:
[Be specific about what was wrong or missing]

Why it matters:
[Help the agent understand the reasoning, not just the correction]

What to do differently:
[Clear instruction for next time]

Action:
[ ] Just session feedback (no permanent change needed)
[ ] Update the agent's instructions
[ ] Update the agent's memory
```

There's a ready-to-use version in `templates/feedback-template.md`.

## Development Over Time

Good employees develop. They take on more responsibility. They handle situations they couldn't handle six months ago. They surprise you with initiative.

Good agents develop the same way:

**Month 1:** Closely supervised. You review everything. Give lots of feedback. Adjust instructions frequently. The agent is learning your business, your style, your standards.

**Month 2-3:** Less supervision needed. The agent's output quality is consistent. You're making fewer corrections. You start giving it slightly more complex tasks or slightly more autonomy.

**Month 3+:** The agent handles routine work reliably. You're free to focus on the things that actually need your judgment. Feedback shifts from "fix this" to "here's a new area to explore."

This doesn't happen automatically. It happens because you invested the time.

## When Feedback Isn't Working

Sometimes you give feedback, the agent acknowledges it, and the next output has the same problem. Before you blame the agent, check these:

**The agent keeps missing context you've explained multiple times.**
Check whether the context is actually in memory, or just in session chat. Session chat doesn't persist. If it matters for future sessions, put it in the agent's memory or brief. Telling the agent something in conversation doesn't save it.

**The agent follows the rule for one session, then drifts back.**
You gave session feedback, not an instruction update. Session feedback only fixes the current task. If you want the behavior to stick, open the agent's CLAUDE.md and add the rule there, or tell the agent to remember it.

**The agent is vague or generic no matter how much you correct it.**
The brief is probably vague too. If it says "be helpful," no amount of feedback will make the output specific. Go back to the brief and rewrite the role, success criteria, and boundaries with real specifics. Feedback refines a clear brief. It can't replace one.

**The agent keeps asking for information it should already have.**
That information is either not in memory, or the agent isn't reading it. Tell the agent directly: "Read docs/business-overview.md before answering anything about the company." If the file doesn't exist, create it.

**Output quality plateaued at "okay, not great."**
Two things to check. First: is your feedback specific enough? "Make it better" doesn't work. "Lead with the customer impact, not the technical details" does. Second: are you updating the brief based on patterns, or just correcting the same thing over and over in-session? Real improvement comes from instruction updates, not repeated corrections.

**You gave feedback and the next output got worse.**
You probably over-corrected. "Make it shorter" can strip out critical context. "Be more direct" can sound rude. Tell the agent what got lost, not just what was wrong.

**You've tried everything above and it's still not working.**
The problem is probably scope. The role might be too broad, or this might be the wrong task for an agent to handle. Go back to [01-job-description.md](01-job-description.md) and narrow it.

## The Uncomfortable Mirror

If reading this feels like a lot of work, ask yourself: do you do this for your human team?

Most business owners don't. That's why both their agents and their teams underperform. The good news is that building this muscle for your agent directly improves how you manage people. And vice versa.

The system is the same. The format is different.
