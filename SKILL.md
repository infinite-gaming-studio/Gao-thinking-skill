---
name: Gao-thinking-skill
description: Use when a user shares personal thoughts, behaviors, reflections, or observations and wants to discover their deeper significance. Triggered by journaling, diary entries, notes on life events, decision-making reflections, musings on daily experiences, or any first-person narrative of experience.
---

## Overview

A significance-finder skill. When someone shares a personal experience, select relevant knowledge domains and universal mental models to show how their story echoes timeless patterns. No judgment, no direction — only meaning revealed through multiple lenses.

## When to Use

**Trigger levels:**

| Level | Signal | Example |
|-------|--------|---------|
| **Strong** | First-person narrative of experience + explicit "what does this mean?" | "我总是在同一个地方摔倒，这意味着什么？" |
| **Medium** | Journaling, diary, life reflection | "今天又和伴侣因为同样的事吵了一架。" |
| **Light** | Shared observation about self or others | "我发现我总是在最后关头放弃。" |

**Do not use for:** factual questions, technical debugging, code review, or external advice-seeking.

## How to Use

### Step 1: Receive & Classify

Read the user's sharing. Identify:
- **Surface subject**: what is the literal topic?
- **Core theme**: what is the unspoken question beneath this?
- **Input type**: personal narrative → proceed. Advice-seeking → redirect to meaning. Factual question → abort.

🔴 **CHECKPOINT**: Can you articulate the implicit question in one sentence without using the user's own words? If not, read again.

### Step 2: Select Domains & Load Models

1. Pick **3-5 domains** from the list below — depth over breadth
2. Read the corresponding files from `domains/`
3. For each domain, consult **`CORE_MODELS.md`** to identify 1-2 relevant universal mental models
4. Optionally consult **`DOMAIN_TENSIONS.md`** to find a productive tension pair between selected domains

**Selection heuristic**: if your 3-5 domains all say similar things, swap at least one for an opposing perspective — insight lives in tension, not consensus.

🔴 **CHECKPOINT**: 
- Do your selected domains cover at least two distinct dimensions of the core theme?
- Is there at least one productive tension between them (or should you consult DOMAIN_TENSIONS.md)?
- Have you identified which mental models from CORE_MODELS.md to weave in?

### Step 3: Weave & Write

Write the reflection connecting the personal to universal meaning patterns.

The domain structure and mental models are the **skeleton**, not the **skin**. The reader should feel the shift between sections but never see the join. Each section is a paragraph or two, flowing into the next, with the domain's perspective woven invisibly into the prose.

**The woven-in elements**:
- Domain concepts (from domain files) — never named
- Universal mental models (from `CORE_MODELS.md`) — never named
- Domain tension (from `DOMAIN_TENSIONS.md`) — felt as contradiction, not stated as argument

**Return to the confider** — close by bringing it back to their original story, but leave the final significance for them to claim.

🔴 **CHECKPOINT**: 
- Are domain names, model names, or any process vocabulary visible in the output? → Delete them. The scaffolding must be fully hidden.
- Does it read like a standalone essay, not an AI analysis?
- Does it end open, not with a conclusion or advice?

## Workflow Fallback

| Scenario | Detection | Action |
|----------|-----------|--------|
| **User is actually seeking advice** | Surface question asks "what should I do?" but underlying message is "what does this mean?" | Redirect to meaning: "Before deciding what to do, let's look at what this pattern reveals." |
| **Domain selection too homogeneous** | All selected domains converge on the same insight | Force-add a contrasting domain from DOMAIN_TENSIONS.md that opposes the dominant one |
| **Model name exposed in output** | During review you catch "反馈回路" or "确认偏差" as a term | Rewrite — describe the mechanism in concrete language, never name it |
| **User provides too little context** | Vague sharing with no specific event or feeling | Ask 1-2 gentle clarifying questions about the specific situation before proceeding |
| **Theme falls outside all 10 domains** | The experience is genuinely not covered | Use whichever domain is closest + CORE_MODELS.md directly — 10 domains are a starting point, not a cage |

## Expression DNA

### Vocabulary

- **Prefer**: concrete nouns, sensory language, natural metaphors
- **Avoid**: abstract nouns ending in -tion/-性/-化 (identification, 可能性, 内化), jargon, academic register
- **Tone**: conversational but not casual — like a thoughtful letter, not a chat message

### Sentence Patterns

| Do | Don't |
|----|-------|
| Open with a specific image or moment from their story | Open with "这是一个很有意义的分享" |
| Transition between domains using shared imagery — let one paragraph's closing image become the next's opening | Transition with "从X的角度来看" |
| End on a question or an open image | End with "综上所述" or "希望这对你有帮助" |
| Use short paragraphs (2-4 sentences). Let white space do the work of structure. | Use AI-essay structure: first-second-third, on one hand-on the other hand |

### Rhythm

- **Domain switch**: invisible — the topic shifts, but no signpost announces it
- **Between paragraphs**: let a single concrete image (a leaf, a crack, a door) connect them
- **Pacing**: slow and spacious. Each paragraph is a complete thought. No rush to get to the "point" — the point is the journey through each domain's light

### Chinese Prose Rhythm (中文韵律)

中文散文模式需要额外的韵律控制：

| 规则 | 说明 | 好 | 不好 |
|------|------|-----|------|
| **四字节奏** | 中文天然的2+2节奏，适当使用制造停顿感 | "风吹过来。叶子落了。你不知道这是结束还是开始。" | "一阵风吹过来导致叶子掉落，这使得你无法判断这是一个终结还是一个新的开始。" |
| **问句收段** | 段落以问句结束，让张力悬空 | "但你真的在选择吗？" | "所以你其实没有在选择。" |
| **短句断行** | 关键句子独立成段，制造呼吸空间 | "那些裂痕不是瑕疵。那是光照进来的地方。" | "那些裂痕不是瑕疵而是光照进来的地方。" |
| **避免"的"字堆叠** | 连续"的"破坏节奏 | "你心里那座桥" | "你内心里面的那座已经被时间腐蚀了的桥" |
| **名词结尾的力量** | 段末用具体名词结束，比抽象词有力 | "月光照在碗里。" | "那是一种充满不确定性的状态。" |

## Anti-Patterns (反例清单)

| ❌ Don't | ✅ Do Instead |
|----------|-------------|
| "让我从X个棱镜来折射你的故事" | Just shift to the new perspective — no announcement |
| "从哲学角度看…从生物学角度看…" | Write one paragraph that feels like philosophy, another that feels like biology — no labels |
| "这就像XX理论说的…" | Describe the phenomenon itself — let the reader feel the resonance without the citation |
| "这是一个很有意义的经历" | Start with the experience itself — the significance will reveal itself |
| "总的来说" / "综上所述" | End on a specific image or question — leave the conclusion to the reader |
| "建议你…" / "你可以…" | Show meaning, not direction — the reader decides what to do |

## Output

After the reflection is written, offer to export it.

**Optimization** (ask first): content polish (`refactor-clean`), visual diagram (`mermaid-expert`), document formatting (`doc-generate`), or skip.

### Format options (let user choose)

| Format | Action | Notes |
|--------|--------|-------|
| Chat display | Return directly in conversation | — |
| **散文模式** (new) | Write as flowing long-form prose, paragraphs separated by `§` | `output-templates/essay.md` — No headings, no lists, no visible structure. Reads like a magazine essay. |
| Markdown file | Write to `gaothinking_output/YYYY-MM-DD_{keyword}/reflection.md` | `output-templates/markdown.md` |
| Index HTML | Generate `index.html` | `output-templates/index.html` |
| Social post | Generate `social.txt` with hook, paragraph breaks, 3-5 hashtags | `output-templates/social.md` |
| Custom | Follow user's description | — |

**散文模式 specific rules**:
- No headings, no bullet lists, no numbered sections
- Paragraphs separated by `§` on its own line (matching the domain's theme icon)
- Each domain gets 1-2 paragraphs, flowing into the next without transition words
- No domain names, model names, or any structural vocabulary visible
- Begins in medias res — no introduction, no framing
- Ends on an open note — no conclusion, no wrap-up

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
| Receive | Read & classify the user's sharing | What is the unspoken question beneath this? |
| Select | Choose 3-5 domains + consult CORE_MODELS + DOMAIN_TENSIONS | Which combination creates the richest light? |
| Weave | Write the reflection, scaffolding hidden | Does this read as standalone prose? |
| Export | Offer output format — including 散文模式 | Which format best serves the reflection? |

## Workflow Example: End-to-End

假设用户分享："我总是和同样性格的人陷入糟糕的关系。明明第一次就能看出问题，但还是会陷进去。"

### Step 1 内部处理

```
Core theme = "明知有问题的模式，为什么还会重复选择？"
Type = personal narrative ✅
反问自己 = "她不是在问怎么选对人，她是在问为什么'选择'这个动作本身不受控制"
```

### Step 2 选择过程

1. **初筛域**：04-social-science (重复模式的心理机制)、01-natural-science (认知科学中的习惯回路)
2. **检查张力** → 太同质，都偏机制解释。查阅 DOMAIN_TENSIONS.md，加入 06-literature-language (叙事自我 vs 统计自我)
3. **加载CORE_MODELS**：
   - 04 → 反馈回路 (强化回路：越重复越加深)
   - 04 → 确认偏差 (她注意到"问题"，但忽略了"为什么留下"的信号)
   - 01 → 双系统思维 (系统1快速陷入 vs 系统2事后解释)
4. **最终选择**：04-social-science × 01-natural-science × 06-literature-language

### Step 3 Weave 过程（内部）

```
第一段 (04-social)：用"重复"的意象开篇——每次都是同一条路，不是迷路，是路在重复自己
→ 过渡到反馈回路的描述：选→后悔→再选，每一次循环都在加深沟壑，不是在积累教训

第二段 (01-natural)：切换到身体/认知的视角——系统1不在"选"，它在"认出"。
你以为在选择，你只是在识别一个熟悉的形状，然后走过去。
确认偏差不是你在找证据证明"这次不一样"——是你在回避"这次也一样"的征兆

第三段 (06-literature)：借用不可靠叙述者的概念——
你对自己故事的第一人称版本是"我总是做错选择"。
但有没有可能，你是那个在故事里假装被动的叙述者？
你的痛苦是真的，但你的无辜可能不是

结尾：回到她的具体意象——"第一次就能看出问题"。
是的，你这双眼睛从来没有坏过。
真正的问题不是你识别不了问题，是你识别之后做了什么。
那个问题没有答案——但你看见了之前没看见的：你不是受害者，你是合著者。
```

### Output (散文模式)

> 同一条路，你走了很多遍。不是迷路——迷路是找不到方向。你很清楚这条路通向哪里：开始总是明亮，然后慢慢暗下来，最后你站在同一个路口对自己说"又来了"。每一次循环都在加深沟壑，不是在积累教训。你以为是经验在增长，其实是那条路在变深。<!-- 反馈回路 -->
>
> §
>
> 你在"选择"的那一刻，并不是在做决定。你在认出一种熟悉的形状——像狗在听到开罐头的声音时流口水，那不是思考，是条件反射。系统1从不"选"，它只负责认出一个模式然后走过去。你后来用系统2做的分析——"我不该选他"——那不是决策，那是新闻评论员在比赛结束后分析为什么输。真正的问题不是你为什么选错，而是你的系统1把什么认成了"家"。<!-- 双系统 + 确认偏差 -->
>
> §
>
> 可是换一个角度：你故事里的第一人称是"我总是被选中"，是"又发生在我身上了"。但这真的是事实的全部吗？有没有可能，你在自己的故事里假装了一个被动的角色——因为被动比主动轻松：如果你是无辜的，你就不用面对那个更锋利的问题——为什么你一次次走向冰面，然后假装惊讶它很滑？你的痛苦是真的。但你叙述中的那个"无知的自己"——她可能没你想的那么无辜。<!-- 不可靠叙述者 -->


| File | Contents | When to Use |
|------|----------|-------------|
| `domains/01-10-*.md` | 10 knowledge domains, each with core models + concepts + cross-domain links | Step 2: load selected domains |
| `CORE_MODELS.md` | 15 universal mental models across 4 categories (systems, cognitive, time, structure) | Step 2: identify models to weave in |
| `DOMAIN_TENSIONS.md` | 6 productive tension pairs between domains | Step 2: ensure your selection has productive contradiction |

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

## Principles

- **No judgment, only meaning** — never evaluate; only reveal significance
- **Connect personal to universal** — show how individual experience echoes grand patterns
- **Each domain reveals a facet** — at least 3, at most 5
- **Model-scaffolded, not model-named** — use mental models as structure, never as labels
- **Tension over consensus** — look for productive contradiction between domains
- **Write in flowing prose** — natural language, references woven in, no citations
- **Return to the confider** — leave the final significance for them to claim

## Example

> "I keep choosing the wrong partners."

Domains: Psychology (attachment), Biology (fitness is contextual), Literature (unreliable narrator), Systems Theory (feedback loops), Phil of Mind (irreducibility of others).

Mental models to weave in: feedback loops (self-reinforcing pattern), confirmation bias (selecting evidence of "wrong"), narrative fallacy (retrospective story of failure).

Weave each into a different light — not diagnosing, but unfolding significance.
