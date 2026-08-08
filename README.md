# Teaching HTML Story Deck

A reusable Agent Skill for producing polished standalone teaching HTML pages with content-specific SVG diagrams and advanced but restrained motion.

## What it creates

- interactive teaching decks;
- product and methodology explainers;
- architecture walkthroughs;
- Bilibili horizontal teaching pages;
- Douyin vertical explainers;
- course lessons;
- launch demos that reveal the product only after the problem is understood;
- upgraded versions of existing HTML presentations.

## Core workflow

```text
Raw content
→ Teaching objective
→ Narrative spine
→ Visual mapping
→ Content-specific inline SVG
→ Motion system
→ Single-file HTML
→ Validation
```

The Skill chooses diagrams according to the content. It does not paste a fixed architecture image into every deck.

## Installation

```bash
mkdir -p ~/.agents/skills
cp -R teaching-html-story-deck ~/.agents/skills/
```

Invoke:

```text
$teaching-html-story-deck

把下面内容做成一份教学 HTML。
先从问题开始，最后一页再揭示产品。
根据内容自动生成 SVG 架构图、思维导图和高级但克制的动效。
```

For Claude Code:

```bash
mkdir -p ~/.claude/skills
cp -R teaching-html-story-deck ~/.claude/skills/
```

Then use:

```text
/teaching-html-story-deck
```

## Example prompts

```text
把这篇系统设计文章变成一个可全屏讲解的单文件 HTML。
需要问题、原理、数据流、架构、实战和最后总结。
```

```text
优化这个已有 HTML。保留内容，但改成黑白克制、现代开发者产品感的高级动效版本，并增加真正服务理解的 SVG。
```

```text
把我的开源 Agent Skill 做成一个故事型演示：先讲为什么开发者会过早开工，最后才揭示 Skill。
```

## Key files

- `SKILL.md`: core workflow and rules;
- `references/user-preferences.md`: persistent design and teaching preferences;
- `references/story-and-visual-framework.md`: narrative and diagram selection;
- `references/svg-and-motion-system.md`: implementation patterns;
- `references/design-rationale.md`: lessons from the Shape Up deck process;
- `references/quality-gates.md`: final review;
- `assets/`: reusable intake and blueprint templates;
- `scripts/validate_deck.py`: standalone HTML validator;
- `examples/`: worked Shape Up example.

## Design philosophy

The deck succeeds when the audience can explain the topic after seeing it—not merely when the page looks impressive.

The strongest visual makes a relationship obvious.
The strongest animation makes a state change understandable.
