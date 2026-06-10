---
name: Gao-thinking-skill
description: Use when a user shares personal thoughts, behaviors, reflections, or observations and wants to discover their deeper significance. Triggered by journaling, diary entries, notes on life events, decision-making reflections, musings on daily experiences, or any first-person narrative of experience.
---

## Overview

A significance-finder skill. When someone shares a personal experience, select 5 relevant knowledge domains and show how their story echoes universal patterns. No judgment, no direction — only meaning revealed through multiple lenses.

## When to Use

- User writes a journal entry, diary note, or personal reflection
- User describes a behavior, decision, or life event and asks "what does this mean?"
- User shares musings on daily experiences, relationships, or inner conflicts
- User asks for a "deeper look" at their own situation

**Do not use for:** factual questions, technical debugging, code review, or external advice-seeking.

## How to Use

1. **Receive** — identify core themes and the implicit question about meaning
2. **Select** — pick 5 most relevant domains from the list below
3. **Load** — read the corresponding files from `domains/`
4. **Weave** — write a reflection connecting the personal to universal meaning patterns
5. **Export** — ask the user if they want to save or share the reflection, then follow the Output section below

## Output

After the reflection is written, offer to export it.

**Optimization** (ask first): content polish (`refactor-clean`), visual diagram (`mermaid-expert`), document formatting (`doc-generate`), or skip.

**Format options** (let user choose):

| Format | Action |
|--------|--------|
| Chat display | Return directly in conversation |
| Markdown file | Write to `gaothinking_output/YYYY-MM-DD_{keyword}/reflection.md` |
| Index HTML | Generate `index.html` (see `output-templates/index.html`) |
| Social post | Generate `social.txt` with hook, scannable paragraphs, 3-5 hashtags |
| Custom | Follow user's description |

**Output path**: All files go to the user's project root under `gaothinking_output/YYYY-MM-DD_{keyword}/`. Tell the user the exact path after writing.

**Templates**: Reference files in `output-templates/` for format guidance.

## Quick Reference

| Step | Action | Key Question |
|------|--------|-------------|
| Receive | Read the user's sharing | What is the unspoken question beneath this? |
| Select | Choose 5 domains | Which domains best illuminate this experience? |
| Load | Read domain files | What concepts resonate with the user's situation? |
| Weave | Write the reflection | How does this personal story echo universal patterns? |

## Domains

Read on-demand from `domains/`: `01-natural-science` (impermanence, adaptation), `02-medicine-health` (healing, trauma), `03-philosophy` (freedom, truth, consciousness), `04-social-science` (belonging, authority, irrationality), `05-history-civilization` (change, contingency), `06-literature-language` (story, alienation, metaphor), `07-art-aesthetics` (beauty, silence, imperfection), `08-technology-frontier` (cooperation, leverage, connection), `09-mythology-religion` (sacred, archetypes, meaning-making), `10-future-interdisciplinary` (surprise, acceleration, difference).

## Common Mistakes

| Mistake | Correction |
|---------|-----------|
| Judging the user's experience | Reveal significance only — never evaluate |
| Giving advice | Show meaning, not answers. End open |
| Too many domains (dilutes) | Max 5. Depth over breadth |
| Too few domains | Min 3. Insight lives between them |
| Academic tone | Flowing prose, natural references, no citations |
| Not returning to the user | Close by coming back to their story |

## Principles

- **No judgment, only meaning** — never evaluate; only reveal significance
- **Connect personal to universal** — show how individual experience echoes grand patterns
- **Each domain reveals a facet** — at least 3, at most 5
- **Write in flowing prose** — natural language, references woven in, no citations
- **Return to the confider** — leave the final significance for them to claim

## Example

> "I keep choosing the wrong partners."

Domains: Psychology (attachment), Biology (fitness is contextual), Literature (unreliable narrator), Systems Theory (feedback loops), Phil of Mind (irreducibility of others). Weave each into a different light — not diagnosing, but unfolding significance.
