# Feedback Template: Tax Prep Assistant

This is the customized feedback template generated during Priya's onboarding interview. Based on the generic template in `templates/feedback-template.md`, tailored for the Tax Prep Assistant's narrow scope.

---

## Feedback: [Date] -- [Cycle, e.g., 2026-Q1]

### What I'm Reviewing

Which output is this about? (Check one)

- [ ] Anomaly flag (specific entry)
- [ ] Draft email to a client
- [ ] Per-client prep summary
- [ ] False positive that shouldn't have been flagged
- [ ] Something that wasn't flagged but should have been
- [ ] Other: _______________

### Client Context (if applicable)

- Client: _______________
- Business type: _______________

### What Worked

For flags:
- Was the flag real (meaning I actually needed to follow up)?
- Was the context provided enough for me to act without reading the raw books?

For emails:
- Did it sound like me?
- Was the ask clear?
- Did it need any editing or was it ready to send?

### What Didn't Work

For flags:
- False positive: what made it look suspicious when it wasn't? (This goes into common-false-positives.md)
- Missed flag: what was the pattern the agent didn't catch? (Add to flagging criteria)
- Too vague: did the flag tell me what to look at but not why?

For emails:
- Voice off: too formal, too casual, wrong word choice
- Missing info: what should have been in the ask but wasn't
- Redundant: agent asked for something I already have
- Tone: too demanding, too apologetic, etc.

### Why This Matters

Be specific. Examples:

- "This flag was a false positive because the client always has a Q1 insurance payment that looks like a spike. We have 4 other clients with the same pattern. Add to common-false-positives.md."
- "This email was too formal for Dave -- we've worked together 6 years. My real emails to him don't have a subject line this formal."
- "The agent didn't flag a $4,000 vendor payment to someone new. The flagging criteria says flag new vendors over $1,000, so this should have triggered. What happened?"

### What to Do Differently

Clear instruction for next time. Specific enough that the agent could follow it without interpretation.

### Action Needed

- [ ] Session-only correction (just this one)
- [ ] Update client-quirks.md (specific client)
- [ ] Update common-false-positives.md (general pattern)
- [ ] Update email-voice.md (voice tweak)
- [ ] Update flagging criteria in agent brief (rule change)
- [ ] Update client-roster.md (client info changed)
