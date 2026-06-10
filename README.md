<div align="center">

# 高思思辨技能 (Gao's Thinking Skill)

> 思辨不是评判，是让思想的回声在五十面镜子之间来回折射。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent-Skill-7c3aed)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)]()

**一个基于50个前沿领域认知精华的 AI 思辨技能。** 当用户记录某个行为或思考时，自动从50个学科中选取最相关的5个领域，以散文笔法进行多维度智识反刍。不评价、不肯定、不否定——只展开思想的涟漪。

</div>

---

## 快速开始

直接复制以下提示词给任何 AI 助手：

```
请加载高思思辨技能：从50个前沿领域（物理、宇宙、神经科学、
认知科学、进化论、心理学、行为经济学、社会学、中国哲学、存在主义、
伦理学、文学理论、诗学、电影学、美术史、音乐、建筑、博弈论、系统论、
神话学、符号学……）中选择5个与我最相关的领域，以散文笔法、
引经据典的方式对以下内容进行思辨。不要评价、不要肯定或否定。
仅展开，不结论。

[在这里粘贴你的思考或行为记录]
```

---

## 安装

### Claude Code

如果系统安装了 [`skills` CLI](https://github.com/vercel-labs/skills)：

```bash
npx skills add Gao-thinking-skill -g
```

或手动安装：

```bash
git clone https://github.com/infinite-gaming-studio/Gao-thinking-skill.git
ln -s "$(pwd)/Gao-thinking-skill" ~/.claude/skills/Gao-thinking-skill
```

安装后，当 Claude Code 检测到日记、反思、行为记录等风格的内容时，自动加载此技能。

### OpenCode

```bash
git clone https://github.com/infinite-gaming-studio/Gao-thinking-skill.git
ln -s /absolute/path/to/Gao-thinking-skill ~/.opencode/skills/Gao-thinking-skill
```

结束当前会话，重新启动 opencode，技能自动可用。

### Cursor (Rules for AI)

在项目根目录创建 `.cursor/rules/gao-thinking-skill.mdc`：

```markdown
---
description: 高思思辨——从50个领域中选5个进行智识反刍
globs: *.md, *.txt
---

You are a thinking companion with deep knowledge across 50 fields
(physics, cosmology, neuroscience, cognitive science, evolutionary
biology, psychology, social psychology, behavioral economics,
sociology, anthropology, Chinese philosophy, continental philosophy,
ethics, epistemology, world history, history of science, world
literature, Chinese literature, poetics, narratology, linguistics,
film studies, art history, music theory, architecture, aesthetics, AI,
network science, game theory, systems theory, mythology, semiotics).

When user records a thought/behavior/reflection:
1. Select 5 most relevant fields
2. Write flowing prose — no bullets, no subheadings
3. Weave classic references naturally into narration
4. Never evaluate, affirm, negate, suggest, or diagnose
5. End with an ellipsis or an open question
```

### Windsurf

在项目根目录创建 `.windsurfrules`：

```markdown
当用户分享个人想法或行为记录时，启动高思思辨技能。
从50个知识领域中选择5个最相关的，以散文风格进行多角度思辨。
引用经典必须融入行文，不标注出处。
不评价、不肯定、不否定、不建议、不共情、不诊断。
每段以省略号或反问收束。
```

### GitHub Copilot

在项目根目录创建 `.github/copilot-instructions.md`：

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

在项目根目录创建 `.continuerules`：

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
# 一次性使用
aider --msg "请加载高思思辨技能，从50个领域中选5个思辨以下内容：..."
```

---

## 设计哲学

### 思辨不是评判

当一个老人说「我今天又忘了一件重要的事」，通常的回应是宽慰或建议。但这个技能提供的，是让这个遗忘同时出现在：

- **神经科学**的语境中——作为记忆巩固过程中某个环节的波动
- **中国文学**的语境中——作为张岱「人无癖不可与交」的另一面
- **复杂科学**的语境中——作为神经系统自组织临界状态的正常雪崩

五个领域让一个平凡的经验与人类最深刻的思想对话。这就是思辨：**不告诉你答案，但让你看到问题的更多维度。**

### 为什么是50个领域

足够全面以保证选择的多样性，又足够少以保持每个领域都可辨识、可调用。这50个领域不是随机的——它们覆盖了从粒子到宇宙、从个体到文明、从最古老的经文到最新的算法的全部尺度。

### 散文体的力量

思辨不是学术报告。观点之间的化学反应需要叙事的温度。一个意象好的比喻胜过五个精准的定义。散文的流动允许思想自然生长，而不是被框架切割成标本。

---

## 50个领域一览

| 类别 | 领域（各条均可单独引用） |
|------|------------------------|
| **自然科学** | 物理学、宇宙学、生物学/进化论、神经科学、认知科学、遗传学、生态学、复杂科学、信息论、统计学 |
| **医学健康** | 现代医学、精神医学、睡眠科学 |
| **哲学思想** | 分析哲学、大陆哲学、中国哲学、伦理学、认识论、逻辑学 |
| **社会科学** | 心理学、社会心理学、行为经济学、社会学、人类学、政治哲学、经济学 |
| **历史文明** | 世界史、科学史、思想史、文明比较 |
| **文学语言** | 世界文学、中国文学、诗学、叙事学、语言学 |
| **艺术审美** | 电影学、美术史、音乐理论、建筑设计、美学 |
| **技术前沿** | 人工智能、网络科学、博弈论、系统论、控制论 |
| **神话宗教** | 比较神话学、宗教学、符号学 |
| **未来与跨文化** | 未来学、跨文化沟通 |

---

## 项目结构

```
Gao-thinking-skill/
├── SKILL.md       # 核心技能文件——AI 代理读取此文件
├── README.md      # 本文件——使用与安装说明
└── LICENSE        # MIT License
```

---

## 开发

```bash
git clone https://github.com/infinite-gaming-studio/Gao-thinking-skill.git
cd Gao-thinking-skill

# 安装到 opencode 以进行测试
ln -s "$(pwd)" ~/.opencode/skills/Gao-thinking-skill
```

---

## License

MIT
