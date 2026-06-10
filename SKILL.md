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

**Crucial — hide the scaffolding.** The reflection must read as a standalone piece of writing, not an AI analysis. Never include:
- "Let me refract this through five lenses" or any meta-framing
- The fact that domains were selected or loaded
- Any explanation of the process or methodology
- "表面上是关于X，但更深的问题是Y" / "让我从X个棱镜来折射" — these are AI's work notes, not part of the essay
- Domain names as visible labels or section headers

The domain structure is the **skeleton**, not the **skin**. The reader should feel the shift between sections but never see the join. Each section is a paragraph or two, flowing into the next, with the domain's perspective woven invisibly into the prose. The only visible markers are the tone change and the thin decorative rules in HTML output.

**Format options** (let user choose):

| Format | Action | Template Reference |
|--------|--------|-------------------|
| Chat display | Return directly in conversation | — |
| Markdown file | Write to `gaothinking_output/YYYY-MM-DD_{keyword}/reflection.md` | `output-templates/markdown.md` |
| Index HTML | Generate `index.html` | `output-templates/index.html` |
| Social post | Generate `social.txt` with hook, paragraph breaks, 3-5 hashtags | `output-templates/social.md` |
| Custom | Follow user's description | — |

**Output path**: All files go to the user's project root under `gaothinking_output/YYYY-MM-DD_{keyword}/`. Tell the user the exact path after writing.

**Design notes for HTML output**:
- Warm paper tones (#f7f3ed background, #2c2416 text) — easy on elderly eyes
- Serif body font for comfortable long-form reading
- Generous line-height (2.0) and font-size (1.05rem) — no squinting
- Drop cap on first paragraph, ornamental separators between sections
- Domain tags with § prefix for visual clarity
- Print and mobile responsive

**Templates** are in `output-templates/`. Adapt freely — the structure is a guide, not a constraint.

## Quick Reference

| Step | Action | Key Question |
|------|--------|-------------|
| Receive | Read the user's sharing | What is the unspoken question beneath this? |
| Select | Choose 5 domains | Which domains best illuminate this experience? |
| Load | Read domain files | What concepts resonate with the user's situation? |
| Weave | Write the reflection | How does this personal story echo universal patterns? |

## Domains

Read on-demand from `domains/`: `01-natural-science` (impermanence, adaptation), `02-medicine-health` (healing, trauma), `03-philosophy` (freedom, truth, consciousness), `04-social-science` (belonging, authority, irrationality), `05-history-civilization` (change, contingency), `06-literature-language` (story, alienation, metaphor), `07-art-aesthetics` (beauty, silence, imperfection), `08-technology-frontier` (cooperation, leverage, connection), `09-mythology-religion` (sacred, archetypes, meaning-making), `10-future-interdisciplinary` (surprise, acceleration, difference).

## Theme Icon System

When generating HTML output, match the watermark and decorative icons to the reflection's dominant domain. The template uses three placeholders:

- `{{WATERMARK_ICON}}` — massive background watermark (upper-right)
- `{{WATERMARK_SECONDARY}}` — smaller background watermark (bottom-left)
- `{{DECORATIVE_ICON}}` — ornament used in title, separator, blockquote, pull quote, footer

| Domain | Main Icon | Unicode | Secondary (fallback) | Meaning |
|--------|-----------|---------|----------------------|---------|
| General (default) | ❦ | U+2766 | 思 | Floral heart — significance blooming |
| Physics | ∞ | U+221E | 思 | Infinity — endless recursion |
| Biology | ✤ | U+2724 | 思 | Four petals — life's patterns |
| Literature | ❧ | U+2767 | 思 | Rotated heart — story's turn |
| Music | ♪ | U+266A | 思 | Note — a single pitch |
| Art | ◇ | U+25C7 | 思 | Diamond — pure form |
| History | ✦ | U+2726 | 思 | Star — marking time |
| Business | ⊕ | U+2295 | 思 | Exchange — value circulating |
| Technology | ⌘ | U+2318 | 思 | Command — tool of thought |
| Psychology | ☯ | U+262F | 思 | Yin yang — mirror of self |
| Spirituality | ✧ | U+2727 | 思 | Light star — beyond knowing |

**Selection rule**: If the reflection spans multiple domains, use the dominant domain's icon for `WATERMARK_ICON`. Set `WATERMARK_SECONDARY` to the second-most-relevant domain's icon, or default to "思". `DECORATIVE_ICON` matches `WATERMARK_ICON` unless the reflection calls for a lighter touch.

## Common Mistakes

| Mistake | Correction |
|---------|-----------|
| Judging the user's experience | Reveal significance only — never evaluate |
| Giving advice | Show meaning, not answers. End open |
| Too many domains (dilutes) | Max 5. Depth over breadth |
| Too few domains | Min 3. Insight lives between them |
| Academic tone | Flowing prose, natural references, no citations |
| Visible scaffolding ("five lenses", domain names) | Hide the process. Reader should never know domains were selected |
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
