# LinkedIn Post — Bible Study Skill for Claude Code

*Shorter format, professional audience. Lead with the pattern, use the Bible study as the case study.*

---

## Option A: Technical Narrative (recommended)

---

I spent my career in aerospace watching technology reshape how engineers work — not by replacing their judgment, but by giving them better material to work with. Model-Based Definition didn't eliminate the engineer. It gave them a richer model. AR work instructions didn't replace the technician. They made the procedure more present.

I've been thinking about that same principle in a very different context.

I built a skill for Claude Code that helps people create Bible studies through conversation. Not generate them — build them. The AI surfaces passages, historical context, Greek and Hebrew word meanings, and open-ended discussion questions. Then I shape it: go deeper here, drop that, push harder on application. The study gets built through iteration, not produced in one shot.

The architecture is simple but deliberate:

→ Understand (audience, topic, translation)
→ Explore (AI brings raw material)
→ Refine (human shapes it — repeats until right)
→ Export (self-contained HTML with notes, audio, sharing)

Three things I learned about designing AI-as-collaborator experiences:

1. **Constraints beat capabilities.** The most important line in the prompt: "You are not a Bible study generator." Without that, the AI defaults to producing something polished that nobody actually shaped.

2. **Conversation phases are architecture.** Explore → Refine → Export isn't just UX. It encodes the human's role. The AI can't skip to the end because the structure enforces iteration.

3. **Anti-patterns matter more than patterns.** Explicitly listing what to avoid (clichés, obvious-answer questions, over-explaining) made more difference than the positive instructions.

The skill is open source: github.com/oscarecas-PM/BibleStudies

The output is a single HTML file — works offline, prints to PDF, runs on any phone. No app, no account, no build step.

Whether it's a 3D model, a work instruction, or a Bible study — the best tools don't automate away the thinking. They make the thinking better.

#AI #PromptEngineering #ClaudeCode #ProductDesign #DigitalTransformation

---

## Option B: Personal + Professional Blend

---

I'm a Christian, a husband, a father, and an engineer. These days I'm trying to figure out how all four of those fit together.

One small experiment: I built an open-source skill for Claude Code that helps people create Bible studies through conversation. The AI surfaces passages and context. I decide what resonates. The study gets shaped through iteration — not generated in one shot.

[Include the same 3 lessons + link]

The longer version of this story — including what aerospace engineering taught me about AI collaboration — is on Medium: [link]

---

## Notes on LinkedIn Strategy

- **Post the Option A version as a standalone LinkedIn post** (not an article — posts get 5–10x the reach)
- **Link to the Medium article** in the first comment, not in the post body (LinkedIn suppresses posts with external links)
- **The diagram**: LinkedIn supports image posts. Render the flow diagram as a clean image and attach it to the post — visual posts get significantly more engagement
- **Hashtags**: Keep to 3–5. #AI #PromptEngineering #ClaudeCode are niche enough to be useful. #DigitalTransformation connects to your existing professional brand.
- **Timing**: Post Tuesday–Thursday morning (your network's likely timezone)
