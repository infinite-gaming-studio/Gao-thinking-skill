<div align="center">

# Gao's Thinking Skill

> Thinking is not judging — it is letting echoes of thought refract between fifty mirrors.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent-Skill-7c3aed)]()
[![skills.sh](https://img.shields.io/badge/skills.sh-Compatible-blue)](https://skills.sh)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)]()

**An AI thinking companion skill.** When a user records a thought, behavior, or reflection, it selects relevant knowledge domains and universal mental models to reveal deeper significance in flowing prose. No judgment, no direction — only meaning revealed through multiple lenses.

</div>

---

## What's New in v2

| Feature | Description |
|---------|-------------|
| **CORE_MODELS.md** | 15 universal mental models across 4 categories (systems, cognitive, time, structure) — reusable across domains |
| **DOMAIN_TENSIONS.md** | 6 productive tension pairs — insight lives in contradiction, not consensus |
| **Agentic Workflow** | Step-based process with checkpoints + 5 fallback scenarios |
| **Expression DNA** | Vocabulary, sentence patterns, rhythm, and Chinese prose rules |
| **散文模式 (Essay Mode)** | New output format — paragraphs separated by `§`, reads like a magazine essay |
| **Expanded Domains** | All 10 domains now include core mental models, classic thought experiments, cross-domain connections, and anti-pattern warnings |

---

## Quick Start

```
Apply Gao's Thinking Skill: From 10 knowledge domains (natural science,
medicine, philosophy, social science, history, literature, art, technology,
mythology, future studies) select 3-5 most relevant to my situation
and contemplate the following in flowing prose with references woven
naturally. Use universal mental models as structure, never as labels.
Do not evaluate, affirm, or negate. Only unfold, never conclude.

[Paste your thought or reflection here]
```

---

## Installation

### One-line (any runtime, auto-detect)

```bash
npx skills add infinite-gaming-studio/Gao-thinking-skill
```

The [skills CLI](https://github.com/vercel-labs/skills) auto-detects your runtime (Claude Code, Codex, Cursor, OpenCode, Gemini CLI, etc.) and installs to the correct directory.

### Manual by runtime

| Runtime | Command |
|---------|---------|
| **OpenCode** | `git clone https://github.com/infinite-gaming-studio/Gao-thinking-skill.git && ln -s "$(pwd)/Gao-thinking-skill" ~/.opencode/skills/Gao-thinking-skill` |
| **Claude Code** | `npx skills add infinite-gaming-studio/Gao-thinking-skill -g` or manually: `git clone ... && ln -s "$(pwd)/Gao-thinking-skill" ~/.claude/skills/Gao-thinking-skill` |
| **Codex CLI** | `npx skills add infinite-gaming-studio/Gao-thinking-skill -a codex` |
| **Cursor** | `npx skills add infinite-gaming-studio/Gao-thinking-skill -a cursor` |

After installation, restart your AI assistant — the skill auto-loads when triggered.

### Reference-only mode

If your runtime doesn't support Agent Skills auto-loading, paste the contents of `SKILL.md` into your conversation. The skill works as plain Markdown + YAML frontmatter.

---

## Project Structure

```
Gao-thinking-skill/
├── SKILL.md              # Core skill — AI agents read this on activation
├── README.md             # This file
├── CORE_MODELS.md        # 15 universal mental models (4 categories)
├── DOMAIN_TENSIONS.md    # 6 productive tension pairs
├── domains/              # 10 knowledge domains (loaded on-demand)
│   ├── 01-natural-science.md
│   ├── 02-medicine-health.md
│   ├── 03-philosophy.md
│   ├── 04-social-science.md
│   ├── 05-history-civilization.md
│   ├── 06-literature-language.md
│   ├── 07-art-aesthetics.md
│   ├── 08-technology-frontier.md
│   ├── 09-mythology-religion.md
│   └── 10-future-interdisciplinary.md
├── scripts/              # Utility scripts
│   └── update.sh         # Update script (curl-pipe compatible)
├── output-templates/     # Output format templates
│   ├── essay.md          # 散文模式 — flowing prose with § separators
│   ├── markdown.md       # Standard markdown output
│   ├── index.html        # HTML output with icons and watermarks
│   └── social.md         # Social post format
├── LICENSE               # MIT License
```

---

## Design Philosophy

### Thinking is Not Judging

When someone says "I keep choosing the wrong partners," the usual response is comfort or advice. Instead, this skill reveals significance through multiple dimensions:

- **Social Science** — feedback loops of repeated patterns, the structure of attachment
- **Natural Science** — dual-process cognition, system 1 recognizing familiar shapes
- **Literature** — unreliable narrator, the gap between how you experience and how you tell

Three domains, each shedding a different light — not telling you the answer, but showing you more dimensions of the question.

### The Architecture

| Layer | File | Role |
|-------|------|------|
| **Domains** | `domains/*.md` | 10 knowledge areas, each with concepts + significance + cross-domain links |
| **Mental Models** | `CORE_MODELS.md` | 15 universal patterns that re-appear across domains |
| **Tensions** | `DOMAIN_TENSIONS.md` | Productive contradictions between domains — where insight lives |
| **Workflow** | `SKILL.md` | Step-by-step process with checkpoints and fallback |

### Why 10 Domains + 15 Models

10 domains provide sufficient breadth (from particles to civilizations), while 15 reusable mental models provide depth (patterns that repeat across domains). A domain tells you *what* to look at; a mental model tells you *how* to see it. Combined, they create a lattice of understanding — not a list of facts.

### The Power of Prose

Contemplation is not an academic report. The chemistry between ideas requires the warmth of narrative. A well-placed metaphor surpasses five precise definitions. The flow of prose allows thoughts to grow naturally, rather than being cut into specimens by frameworks.

---

## 10 Domains Overview

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

## 15 Mental Models (CORE_MODELS.md)

| Category | Models |
|----------|--------|
| **Systems** | Feedback Loops, Emergence vs Reduction, Threshold Effect, Second-order Effects |
| **Cognitive** | Confirmation Bias, Availability Heuristic, Narrative Fallacy, Dual Process Theory |
| **Time** | Temporal Discounting, Path Dependence, Regression to the Mean |
| **Structure** | Pareto Distribution, Local vs Global Optima, Evolvability vs Efficiency, Margin of Safety |

Plus 6 combination patterns for using 2-3 models together.

---

## 6 Domain Tensions

| Tension Pair | Core Contradiction |
|-------------|-------------------|
| Philosophy × Medicine | Free will vs biological determinism |
| Evolution × Art | Survival fitness vs purposeless creation |
| Mythology × Technology | Sacred meaning vs deconstructive reason |
| Literature × Social Science | Narrative self vs statistical self |
| History × Future Studies | Historical cycles vs accelerating mutation |
| Philosophy × Natural Science | Ought vs is |

---

## Updating

**Note**: `npx skills update` cannot resolve `Gao-thinking-skill` back to the GitHub source. Use one of the reliable methods below.

### Method 1: curl pipe (recommended)

```bash
curl -fsSL https://raw.githubusercontent.com/infinite-gaming-studio/Gao-thinking-skill/main/scripts/update.sh | bash
```

This downloads the update script, runs it in `/tmp/`, and cleans up. No files remain after completion.

### Method 2: one-liner

```bash
npx skills remove Gao-thinking-skill -g -y && npx skills add infinite-gaming-studio/Gao-thinking-skill -g
```

### Method 3: git pull (if cloned manually)

```bash
cd Gao-thinking-skill && git pull
```

After updating, restart your AI assistant to load the latest SKILL.md.

## Troubleshooting

If the update fails:
- Check your internet connection
- Try Method 2 (one-liner) directly
- If uninstalled but not reinstalled, run: `npx skills add infinite-gaming-studio/Gao-thinking-skill -g`

## Uninstalling

| Runtime | Command |
|---------|---------|
| **npx (any runtime)** | `npx skills remove Gao-thinking-skill` |
| **Manual** | Delete the skill directory from your runtime's skills folder (e.g. `rm -rf ~/.opencode/skills/Gao-thinking-skill`) |

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
