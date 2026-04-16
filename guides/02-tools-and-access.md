# Give Your Agent the Right Tools

Think about a new employee's first day. They show up eager to work. But nobody set up their computer. They can't log into any systems. They don't know where the files are. Nobody showed them the shared drive.

What happens? They sit there. Useless. Not because they're incompetent, but because you failed to set them up.

AI agents are the same. Before you blame the agent, check what you gave it to work with.

## The First-Day Checklist

Go through this list for whatever role your agent fills. Not everything applies to every agent, but if an item is relevant and the agent doesn't have access, that's a gap.

### Documents and Files

- [ ] Company overview or "about us" document
- [ ] Product or service descriptions
- [ ] Customer profiles or personas (even informal ones)
- [ ] Brand guidelines, tone of voice, or style preferences
- [ ] Past work samples (previous reports, content, analyses)
- [ ] SOPs or process documents relevant to the role
- [ ] Any templates the role uses regularly

### Data and Systems

- [ ] CRM data (customer lists, deal stages, contact history)
- [ ] Analytics (website traffic, social media stats, sales figures)
- [ ] Financial data (only what's relevant to the role)
- [ ] Project management boards (Trello, Asana, Notion, etc.)
- [ ] Email or communication history (relevant threads)
- [ ] Calendar or scheduling information

### Context That Lives in Your Head

This is the one most people miss. You know things about your business that aren't written down anywhere:

- [ ] Who your best customers are and why
- [ ] What you've tried before and why it didn't work
- [ ] Competitive landscape and how you're positioned
- [ ] Current priorities and what's changing
- [ ] Relationships and dynamics (who the key stakeholders are)
- [ ] Unwritten rules ("we never discount more than 15%", "we don't work with competitor X")

If it matters for the role and it's only in your head, the agent can't use it. Write it down or tell the agent during the interview.

## How to Give Access

In Claude Code, there are a few ways your agent can access information.

### What you can do right now (no setup required)

**Put files in the folder.** The simplest approach. Put relevant documents in the same folder where your agent works. Text files, spreadsheets, PDFs. The agent can read them directly. Think of the folder as the agent's desk -- whatever's on the desk, the agent can use.

**Copy and paste.** For quick context that doesn't need to be permanent. Just paste relevant information into the conversation. Good for one-off tasks, not great for ongoing work.

**Web access.** Claude Code can pull information from websites if you give it a link. Useful for checking live pages, reading documentation, or grabbing current data.

### Advanced: connecting live tools

**Connect external tools.** Claude Code can connect to apps like Google Drive, Notion, and others. This is more powerful but requires some setup. If you're not technical, you can ignore this for now -- your agent can do plenty with just the files in its folder.

You don't need any integrations on day one. Start with files. Add connections later if you actually hit a wall without them.

## What NOT to Give Access To

Just like you wouldn't give a new hire the keys to everything on day one:

- **Financial accounts or banking.** Unless the role specifically requires it.
- **Admin credentials.** Give the minimum access needed for the job.
- **Customer PII beyond what's needed.** If the agent doesn't need social security numbers or credit card details, don't include them.
- **Anything you'd be uncomfortable with a new employee seeing in their first week.**

Start narrow. Expand access as you build trust and see what the agent actually needs. You can always give more later. Taking away access after a mistake is messier.

## The "Do I Have Everything?" Test

Before each work session with your agent, ask yourself:

1. Does the agent have everything it needs to complete this task without asking me for more information?
2. If a new hire sat down to do this task, what would they reach for? Does the agent have that?
3. Am I about to spend 10 minutes explaining context that I could have written down once?

If you're constantly re-explaining the same background, that's a sign something should be in a document, not repeated in conversation.
