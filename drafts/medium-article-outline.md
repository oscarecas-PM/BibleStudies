# I Built a Bible Study Skill for Claude Code — Here's What I Learned About AI as a Collaborator

*Draft outline for Medium — matches Oscar's existing article style: personal narrative → technical insight → broader industry implication*

---

## Opening Hook (Personal Story)

Start with the moment that sparked the idea. Something like:

> I was sitting at my kitchen table trying to put together a Bible study for my family. I had a topic — transformation, how people can genuinely change — but I was stuck in the same loop: Google a verse, read three commentary sites, copy-paste into a doc, try to write a discussion question that didn't sound like a Sunday school worksheet. Two hours in, I had half a page.

> I'd spent my career in aerospace and defense, where I'd watched Model-Based Definition replace 2D drawings and AR work instructions replace paper procedures. The pattern was always the same: technology didn't replace the engineer's judgment — it gave them better raw material to work with. I wondered if the same principle could apply here.

Bridge to: *What if AI could bring me the raw material — passages, context, questions — and I could shape it into something worth sharing?*

---

## Section 1: The Problem — Why "AI-Generated" Isn't the Answer

- The current landscape: you can ask ChatGPT to "write a Bible study about forgiveness" and get something in 10 seconds. It's also generic, shallow, and reads like it was written by committee.
- The opposite extreme: fully manual research is rich but slow — great for pastors with seminary training, not accessible for a dad who wants to lead his family through Scripture on a Tuesday night.
- **The gap**: there's nothing in between. No tool that treats the human as the author and AI as the research partner.
- Connect to your MBD article's thesis: just as MBD doesn't replace the engineer (it gives them a richer model to work from), AI shouldn't replace the study author.

---

## Section 2: What I Built — The Skill Architecture

Introduce Claude Code skills briefly for non-technical readers, then go into the design.

### The Conversational Flow (reference the diagram below)

1. **Start** — The skill asks three things: Who is this for? (audience), What do you want to explore? (topic), What translation? Then it adapts everything downstream.
2. **Explore** — AI surfaces 4–6 passages with full text, historical/linguistic context, and open-ended discussion questions. It draws connections across Old and New Testaments. At least one passage should surprise.
3. **Refine** — This is where the "collaborator, not generator" principle lives. The user says "go deeper on Isaiah, drop the Exodus reference, push harder on application." The AI doesn't just delete — it redirects, offering alternative angles.
4. **Refine again** — This phase repeats. The study gets shaped through conversation, not produced in one shot.
5. **Export** — A single self-contained HTML file with interactive note-taking, text-to-speech for scripture passages, and sharing via email or native share. No dependencies, works offline.

### Key Design Decisions

- **Audience-first**: A study for teens looks fundamentally different from one for couples. The skill doesn't just change vocabulary — it changes passage selection, question style, and interactive elements.
- **Inline questions**: Every discussion question appears right after the scripture it references, not grouped at the end. This was a UX lesson from watching my own family lose the thread when questions were separated from text.
- **Self-contained HTML**: The output is a single file with everything embedded (including images as base64). You can email it, host it on Vercel, print to PDF, or open it on a plane. This came from the same instinct as MBD — keep all the information in one artifact.

---

## Section 3: What I Learned About Prompt Engineering as Product Design

This is the section that generalizes beyond Bible studies — the part your LinkedIn network will care about.

- **Constraints make AI useful.** The most important line in the skill prompt: "You are not a Bible study generator. You do not produce a finished product." Without that constraint, the AI defaults to producing a polished-looking deliverable that nobody actually shaped.
- **Conversation phases are an architecture.** Structuring the interaction into Explore → Refine → Export isn't just UX — it's a way of encoding the human's role into the system. The AI can't skip to the end because the phases enforce iteration.
- **Anti-patterns are as important as patterns.** The skill explicitly lists what to avoid: devotional clichés, questions with obvious answers, over-explaining. These negative constraints were harder to write than the positive instructions and made more difference.
- **Templates are the bridge between AI and craft.** The HTML template isn't just formatting — it encodes design decisions (inline questions, note-taking UX, print layout) that the AI doesn't have to reinvent every time.

---

## Section 4: The Bigger Idea — Technology That Makes Us More Present

- Connect to your career arc: aerospace engineer → factory modernization → digital transformation → now using AI for something deeply personal
- The thesis: the best technology doesn't make us more efficient — it makes us more *present*. MBD made engineers more present with their designs. AR work instructions make technicians more present with their assemblies. This skill makes me more present with Scripture and my family.
- Your aspiration: that we adopt technology to do more, be more at peace, find fulfillment — not to automate away the things that matter
- Close with something concrete — a moment from using the study with your family, or a passage that hit differently because you'd spent time shaping the study rather than just reading someone else's

---

## Closing

Link to the GitHub repo. Mention it's free and open source. Invite readers to try `/bible-study` and build their own.

---

## Flow Diagram (for the article)

Include this Mermaid diagram rendered as an image:

```
┌─────────────────────────────────────────────────────────┐
│                    /bible-study                         │
│                   User invokes skill                    │
└─────────────────────┬───────────────────────────────────┘
                      │
                      ▼
         ┌────────────────────────┐
         │      UNDERSTAND        │
         │                        │
         │  • Audience            │
         │    (teens / couples /  │
         │     family / solo)     │
         │  • Topic               │
         │  • Bible translation   │
         └───────────┬────────────┘
                     │
                     ▼
         ┌────────────────────────┐
         │       EXPLORE          │
         │                        │
         │  AI surfaces:          │
         │  • 4–6 passages        │
         │  • Historical context  │
         │  • Greek/Hebrew roots  │
         │  • 5–6 questions       │
         │  • Cross-testament     │
         │    connections         │
         └───────────┬────────────┘
                     │
                     ▼
         ┌────────────────────────┐
         │       REFINE           │◄──────────┐
         │                        │           │
         │  User shapes:          │           │
         │  • "Go deeper here"    │    Iterate│
         │  • "Drop that"         │    until  │
         │  • "Push harder"       │    ready  │
         │                        │           │
         │  AI redirects,         │           │
         │  doesn't just delete   ├───────────┘
         └───────────┬────────────┘
                     │  User satisfied
                     ▼
         ┌────────────────────────┐
         │    HERO IMAGE          │
         │    (optional)          │
         │                        │
         │  AI suggests prompts   │
         │  → User generates      │
         │  → Embedded as base64  │
         └───────────┬────────────┘
                     │
                     ▼
         ┌────────────────────────┐
         │       EXPORT           │
         │                        │
         │  Self-contained HTML   │
         │  ┌──────────────────┐  │
         │  │ • Inline questions│  │
         │  │ • Note-taking    │  │
         │  │ • Text-to-speech │  │
         │  │ • Share / email  │  │
         │  │ • Works offline  │  │
         │  └──────────────────┘  │
         │                        │
         │  → Vercel / email /    │
         │    PDF / offline       │
         └────────────────────────┘
```

---

*Estimated length: ~1,800–2,200 words (consistent with Oscar's existing articles)*
