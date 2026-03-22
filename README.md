# Bible Studies

A Claude Code skill for building Bible studies through conversation — not generating them. You bring the topic and the audience. The assistant brings passages, context, questions, and connections. You shape it together.

**Live example:** [bible-studies-five.vercel.app](https://bible-studies-five.vercel.app)

## What This Is

A `/bible-study` skill for [Claude Code](https://docs.anthropic.com/en/docs/claude-code) that walks you through creating a Bible study from scratch:

1. **Explore** — Surface relevant passages (not just the obvious ones), provide historical and linguistic context, and generate open-ended discussion questions
2. **Refine** — You prune what doesn't resonate and go deeper on what does. The assistant redirects, not just removes
3. **Export** — Produce a self-contained HTML file with interactive note-taking, text-to-speech for scripture, and sharing via email or native share

The finished HTML works everywhere — host it on Vercel, email it to your small group, print it to PDF, or open it offline. No dependencies, no build step, no server required.

## Features

- **Collaborative, not generative** — The skill brings raw material; you build the study through iteration
- **Audience-aware** — Adapts tone, questions, and interactive elements for teens, couples, mixed family groups, or solo study
- **Inline reflection questions** — Each question appears right after the scripture it references, not grouped at the end
- **Hero images** — Optionally add a visual element with AI image generation prompts tailored to your study's passages
- **Interactive notes** — Text areas under each question + a floating notes drawer, all auto-saved to localStorage
- **Share your notes** — Email them to yourself or share via your phone's native share sheet
- **Listen to Scripture** — Text-to-speech button on every passage
- **Fully portable** — Images embedded as base64, single-file HTML, works offline

## Getting Started

### Prerequisites

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed and configured

### Usage

Clone this repo and run Claude Code from within it:

```bash
git clone https://github.com/oscarecas-PM/BibleStudies.git
cd BibleStudies
claude
```

Then invoke the skill:

```
/bible-study
```

Claude will ask about your audience, topic, and preferred Bible translation, then start surfacing material for you to work with.

## Example Studies

| Study | Topic | Passages |
|-------|-------|----------|
| [People Can Change](people-can-change.html) | Transformation | 2 Cor 5:17, Ezekiel 36:26–27, Psalm 103:8–12, Colossians 3:12–15, Romans 12:2 |

## Project Structure

```
BibleStudies/
├── .claude/
│   └── skills/
│       └── bible-study/
│           ├── SKILL.md              # Skill definition
│           ├── examples/
│           │   └── lent-study.md     # Reference study for tone and quality
│           └── templates/
│               └── study.html        # Interactive HTML template
├── people-can-change.html            # Exported study (self-contained)
└── README.md
```

## How It Works

The skill operates in phases:

**Starting a session** — Understands your audience (teens, couples, mixed family, solo) and topic. If you don't have a topic, it suggests ideas tailored to your audience.

**Exploring** — Surfaces 4–6 passages with full text, context (Hebrew/Greek meanings, historical background), and 5–6 discussion questions. Draws connections across Old and New Testaments.

**Refining** — You give feedback ("go deeper on Isaiah," "drop that question," "push harder on the application"). This phase repeats until the study feels right.

**Hero image** — Suggests AI image generation prompts based on your study's key metaphors. You generate the image in ChatGPT, Midjourney, or similar, then provide it for embedding.

**Exporting** — Generates a single HTML file with everything baked in — styling, interactivity, images, notes — ready to deploy or share.

## Contributing

This is a personal project, but if you build a study with the skill and want to share it, pull requests for new studies are welcome.

## License

MIT
