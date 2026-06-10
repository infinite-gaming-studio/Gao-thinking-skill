<div align="center">

# Gao's Thinking Skill

> Thinking is not judging — it is letting echoes of thought refract between fifty mirrors.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent-Skill-7c3aed)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)]()

**An AI thinking companion skill based on 50 essential knowledge domains.** When a user records a thought, behavior, or reflection, it automatically selects the 5 most relevant domains and provides multi-dimensional intellectual contemplation in flowing prose. No evaluation, no affirmation, no negation — only ripples of thought.

</div>

---

## Quick Start

Copy this prompt to any AI assistant:

```
Apply Gao's Thinking Skill: From 50 essential domains (physics, cosmology,
neuroscience, cognitive science, evolutionary biology, psychology, behavioral
economics, sociology, philosophy, ethics, world literature, poetics, film
studies, art history, music theory, architecture, game theory, systems theory,
mythology, semiotics...) select the 5 most relevant to my situation and
contemplate the following in flowing prose with classic references.
Do not evaluate, affirm, or negate. Only unfold, never conclude.

[Paste your thought or reflection here]
```

---

## Installation

### Claude Code

If you have the [`skills` CLI](https://github.com/vercel-labs/skills) installed:

```bash
npx skills add infinite-gaming-studio/Gao-thinking-skill -g
```

Or install manually:

```bash
git clone https://github.com/infinite-gaming-studio/Gao-thinking-skill.git
ln -s "$(pwd)/Gao-thinking-skill" ~/.claude/skills/Gao-thinking-skill
```

After installation, the skill automatically loads when Claude Code detects journal-like, reflective, or behavioral content.

### OpenCode

```bash
git clone https://github.com/infinite-gaming-studio/Gao-thinking-skill.git
ln -s /absolute/path/to/Gao-thinking-skill ~/.opencode/skills/Gao-thinking-skill
```

End your current session and restart OpenCode — the skill will be available.

### Cursor (Rules for AI)

Create `.cursor/rules/gao-thinking-skill.mdc` in your project root:

```markdown
---
description: Gao Thinking — multi-domain intellectual contemplation from 50 fields
globs: *.md, *.txt
---

You are a thinking companion with deep knowledge across 50 fields
(physics, cosmology, neuroscience, cognitive science, evolutionary
biology, psychology, social psychology, behavioral economics,
sociology, anthropology, philosophy, ethics, epistemology, world
history, history of science, world literature, poetics, narratology,
linguistics, film studies, art history, music theory, architecture,
aesthetics, AI, network science, game theory, systems theory,
mythology, semiotics, futurology).

When user records a thought/behavior/reflection:
1. Select 5 most relevant fields
2. Write flowing prose — no bullets, no subheadings
3. Weave classic references naturally into narration
4. Never evaluate, affirm, negate, suggest, or diagnose
5. End with an ellipsis or an open question
```

### Windsurf

Create `.windsurfrules` in your project root:

```markdown
When user shares personal thoughts or behavioral observations,
activate the Gao Thinking Skill.
Select 5 most relevant domains from 50 knowledge fields and
contemplate in flowing prose with classic references woven naturally.
No evaluation, affirmation, negation, suggestion, empathy, or diagnosis.
End each reflection with ellipsis or open question.
```

### GitHub Copilot

Create `.github/copilot-instructions.md` in your project root:

```markdown
## Gao Thinking Skill

When the user writes a personal thought, behavior, or reflection:

1. Choose the 5 most relevant domains from 50 fields across natural
   sciences, medicine, philosophy, social sciences, history, literature,
   arts, technology, mythology, and futurology.
2. Write one paragraph per domain in flowing prose — no bullet points.
3. Weave classic references into the text (no footnotes or citations).
4. Do NOT evaluate, affirm, negate, suggest, empathize, or diagnose.
5. End each perspective with an ellipsis or open question.
```

### Continue.dev

Create `.continuerules` in your project root:

```markdown
When user records personal thoughts or behavioral observations,
apply the Gao Thinking Skill methodology:
- Select 5 relevant fields from 50-domain knowledge base
- Write prose-style reflection with classic references
- No evaluation, affirmation, or negation
- End with open-ended ellipsis or question
```

### Aider

```bash
# One-time use
aider --msg "Apply Gao's Thinking Skill, contemplate from 50 domains:..."
```

---

## Design Philosophy

### Thinking is Not Judging

When someone says "I forgot something important today," the usual response is comfort or advice. But what this skill offers is to let that forgetting simultaneously appear in:

- **Neuroscience** — as a fluctuation in the memory consolidation process
- **Literature** — as the flip side of Zhang Dai's "one cannot befriend someone without quirks"
- **Complexity Science** — as a normal avalanche in the self-organized criticality of neural systems

Five domains let an ordinary experience dialogue with humanity's deepest thoughts. This is contemplation: **not telling you the answer, but showing you more dimensions of the question.**

### Why 50 Domains

Comprehensive enough to ensure diversity of selection, yet small enough that each domain remains identifiable and accessible. These 50 domains are not random — they span the full scale from particles to cosmos, from individuals to civilizations, from ancient scriptures to modern algorithms.

### The Power of Prose

Contemplation is not an academic report. The chemistry between ideas requires the warmth of narrative. A well-placed metaphor surpasses five precise definitions. The flow of prose allows thoughts to grow naturally, rather than being cut into specimens by frameworks.

---

## 50 Domains Overview

| Category | Domains |
|----------|---------|
| **Natural Sciences** | Physics, Cosmology, Biology/Evolution, Neuroscience, Cognitive Science, Genetics, Ecology, Complexity Science, Information Theory, Statistics |
| **Medicine & Health** | Modern Medicine, Psychiatry, Sleep Science |
| **Philosophy** | Analytic Philosophy, Continental Philosophy, Ethics, Epistemology, Logic, Philosophy of Mind |
| **Social Sciences** | Psychology, Social Psychology, Behavioral Economics, Sociology, Anthropology, Political Philosophy, Economics |
| **History & Civilization** | World History, History of Science, Intellectual History, Comparative Civilization |
| **Literature & Language** | World Literature, Poetics, Narratology, Linguistics, Rhetoric |
| **Arts & Aesthetics** | Film Studies, Art History, Music Theory, Architecture, Aesthetics |
| **Technology & Frontiers** | Artificial Intelligence, Network Science, Game Theory, Systems Theory, Cybernetics |
| **Mythology & Ritual** | Comparative Mythology, Religious Studies, Semiotics |
| **Future & Cross-Cultural** | Futurology, Cross-Cultural Communication |

---

## Project Structure

```
Gao-thinking-skill/
├── SKILL.md       # Core skill file — AI agents read this
├── README.md      # This file — usage and installation guide
├── domains/       # Detailed domain content (loaded on-demand)
└── LICENSE        # MIT License
```

---

## Updating

| Installation Method | Update Command |
|--------------------|----------------|
| `npx skills add` | `npx skills update infinite-gaming-studio/Gao-thinking-skill` |
| Manual symlink / `git clone` | `cd Gao-thinking-skill && git pull` |
| Manual copy | Re-clone with `git clone` |

**Note:** After updating, you need to **restart your AI assistant** (new session loads the latest SKILL.md).

---

## Development

```bash
git clone https://github.com/infinite-gaming-studio/Gao-thinking-skill.git
cd Gao-thinking-skill

# Install to OpenCode for testing
ln -s "$(pwd)" ~/.opencode/skills/Gao-thinking-skill
```

---

## License

MIT
