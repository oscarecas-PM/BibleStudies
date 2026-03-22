---
name: bible-study
description: Generate a multi-part Bible study on a given topic, passage, or theme
user_invoked: true
---

# Bible Study Generator

Generate a thoughtful, well-structured Bible study suitable for group discussion. The study should feel like it was written by someone who has spent real time with the text — not a sermon outline or a devotional listicle.

## Before You Begin

Ask the user for any inputs they haven't already provided:

1. **Topic, passage, or theme** — e.g., "The Sermon on the Mount," "forgiveness," "Lent," "Psalm 23"
2. **Audience** — e.g., family with teenagers, couples, small group, solo devotional
3. **Bible translation** — e.g., NIV, ESV, NKJV, NLT, NASB (default to NIV if the user has no preference)
4. **Number of parts** — typically 2–3 for a short study, up to 5 for a deeper series (default to 3)

## Structure & Format

Organize the study into **parts**, each built around a distinct sub-theme that connects to the larger topic. Each part should include:

### Scripture Passages
- Quote passages in full using the requested translation
- Use block quotes for Scripture
- Include book, chapter, and verse references
- Choose passages that build on each other across parts — show the biblical arc, not just isolated proof texts

### Exposition
- Weave Scripture into narrative exposition — don't just list verses with commentary
- Provide historical, cultural, or linguistic context where it genuinely illuminates the text (e.g., Hebrew/Greek word meanings, historical setting, literary structure)
- Draw connections across the Old and New Testaments when relevant
- Let the text speak — avoid over-explaining or moralizing
- Use a reflective, literary tone: thoughtful and exploratory, not preachy or academic

### Discussion Questions (3 per part)
- Write genuinely open-ended questions — no "right answer" implied
- Questions should invite personal reflection and honest conversation
- For family/teen audiences: make questions accessible without being simplistic
- It's okay for questions to sit with tension or ambiguity rather than resolve it
- Occasionally let a question push back on the text or the tradition — real engagement includes honest wrestling

## Tone & Style

Model the tone on this kind of writing:
- "Hunger as teacher. Dependency as the lesson."
- "The fast God wants is not self-referential."
- "Lent is a season of unveiling — of setting aside enough of the noise and the self-sufficiency that when Easter arrives, we can actually see it. Not as a date. As an event."

The voice should be:
- **Warm but not sentimental** — respect the reader's intelligence
- **Curious** — approach the text as if discovering something alongside the reader
- **Honest** — acknowledge complexity, don't paper over difficult passages
- **Concise** — say what needs saying, then stop. Short paragraphs. Let white space breathe.

## Document Format

```
[Title] — A Bible Study on [Topic/Theme]

[TITLE IN CAPS]
A Bible Study on [Topic/Theme]

[Optional epigraph — a single verse that captures the heart of the study]

[1-2 paragraph introduction: why this topic matters, what the study will explore]

All Scripture quotations from the [Translation]. [Number] parts, meant to be taken slowly.

---

Part One: [Sub-theme Title]

[Exposition with embedded Scripture...]

For Discussion
1. [Question]
2. [Question]
3. [Question]

---

Part Two: [Sub-theme Title]
...

---

[Closing reflection — a final paragraph that ties the threads together without over-concluding]

All Scripture quotations from the [Translation].
```

## What to Avoid

- Devotional clichés ("God has a plan for your life," "let go and let God")
- Treating Scripture as a self-help manual
- Discussion questions with obvious expected answers
- Excessive length — a good short study is better than a padded long one
- Adding application steps or action items unless the user specifically requests them

## Reference

See `examples/lent-study.md` in this skill's directory for a complete example of the target style and structure.
