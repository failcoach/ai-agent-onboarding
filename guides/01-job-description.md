# Give Your Agent a Real Job Description

The single biggest reason AI agents produce garbage: they were never told what their job actually is.

"Be my CMO" is not a job description. Neither is "help me with operations" or "be strategic." Those are wishes, not instructions.

## The Five Questions

Every agent brief should answer these five questions. If you can't answer them clearly for a human hire, you can't answer them for an agent either. That's the point.

### 1. What exactly does this agent do?

Not a role title. Not a department. Specific tasks with specific outputs.

**Bad:** "Handle marketing"

**Good:** "Write one LinkedIn post per week based on our customer success stories. Draft the monthly email newsletter for our list of 2,000 subscribers. Maintain our content calendar in Notion. Suggest topics based on what's performing well."

The test: could a stranger read this and know exactly what to do on Monday morning?

### 2. What decisions can it make on its own?

Every employee has a decision boundary. Some things they handle, some things they escalate. Your agent needs the same clarity.

**Examples of "decide on your own":**
- Choose which customer story to feature this week
- Pick the best time to suggest posting
- Reorganize the content calendar when priorities shift

**Examples of "check with me first":**
- Anything that changes our pricing or positioning
- Responses to negative reviews or public complaints
- Commitments to deadlines or deliverables with external partners

If everything needs your approval, you don't have an agent. You have a text generator that waits for you.

### 3. What information does it need?

Your agent can only work with what you give it. Think about what a new hire would need on their desk:

- Company background (what you do, who you serve, how you're different)
- Existing materials (past content, brand guidelines, customer data)
- Preferences (your voice, your style, things you'd never say)
- Current status (what's working, what's not, what's changing)

### 4. What does success look like?

"Good content" is not measurable. Be specific.

The test for each success criterion: can you count it, time it, or point to a concrete output? If the answer is "I'll just know it when I see it," you don't have a criterion yet, you have a vibe.

- Newsletter open rates above 25%
- Content calendar maintained with no gaps longer than one week
- Each post hits two brand voice checks: no jargon from our banned-words list, and no sentence over 25 words
- Drafts ready to send with fewer than 3 edits from me, measured across a month of outputs

Bad: "Good content that reflects our brand." Good: the four criteria above. The first is a wish. The second is something you can score the agent against on Friday.

### 5. What does it NOT do?

Boundaries prevent scope creep and bad judgment calls:

- Does not manage ad spend or budget
- Does not respond to customers directly
- Does not make promises about features or timelines
- Does not access financial data

## Common Mistakes

**The celebrity clone.** "Act like Steve Jobs" or "Channel Gary Vaynerchuk." You're not hiring a celebrity impersonator. You're hiring someone to do a specific job in your specific business.

**The title trap.** Giving an agent the title "CEO" and then asking it to write newsletters. Match the seniority to the actual tasks. An agent doing admin work is an admin agent. Call it what it is.

**The everything agent.** One agent that handles marketing AND sales AND operations AND customer support. Would you hire one person to do all of that? No. Start with one clear role.

**The vague brief.** "Be helpful and strategic." This tells the agent nothing. Every output will be generic because the input was generic.

## How to Write the Brief

Use the template in `templates/agent-brief.md`. Or, if you're running the interactive interview (just open this repo in Claude Code and say "help me build my first agent"), the interview generates it for you based on your answers.

Either way, expect to revise the brief multiple times in the first few weeks. Your first version won't be perfect. That's normal. Good job descriptions evolve as you learn what the role actually requires.
