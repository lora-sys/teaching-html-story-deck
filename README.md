<div align="center">

![MIT License](https://img.shields.io/badge/license-MIT-0ea5e9?style=flat-square)
![Node 18+](https://img.shields.io/badge/node-%3E%3D18-22c55e?style=flat-square)
![Python 3.10+](https://img.shields.io/badge/python-%3E%3D3.10-22c55e?style=flat-square)
![CI](https://img.shields.io/badge/CI-passing-brightgreen?style=flat-square)
![v1.0.0](https://img.shields.io/badge/version-1.0.0-blue?style=flat-square)

</div>

---

# Teaching HTML Story Deck

> A reusable Agent Skill for producing polished standalone teaching HTML pages with content-specific SVG diagrams and advanced but restrained motion.

给没有设计背景的开发者，一个能产出高质量教学演示页面的 Agent Skill。

## What it creates

| Type | Use case |
|------|----------|
| Interactive teaching decks | Screen-recorded lessons, Bilibili horizontal pages |
| Product & methodology explainers | Reveal the product only after the audience understands the problem |
| Architecture walkthroughs | Data flow, permission graphs, decision boundaries |
| Vertical short explainers | Douyin-style compact vertical presentations |
| Course lessons | Step-by-step curriculum with SVG illustrations |
| Deck upgrades | Improve existing HTML presentations with better hierarchy and motion |

## Core workflow

```text
Raw content
    ↓
Teaching objective
    ↓
Narrative spine
    ↓
Visual mapping
    ↓
Content-specific inline SVG
    ↓
Motion system
    ↓
Single-file HTML
    ↓
Validation
```

The Skill chooses diagrams according to the content. It does not paste a fixed architecture image into every deck.

## Installation

### Claude Code (Recommended)

```bash
npx skills add lora-sys/teaching-html-story-deck
```

Then use `/teaching-html-story-deck` or invoke the skill name.

### Manual install

```bash
mkdir -p ~/.claude/skills
cp -R teaching-html-story-deck ~/.claude/skills/
```

### OpenCode / Cursor

```bash
mkdir -p ~/.agents/skills
cp -R teaching-html-story-deck ~/.agents/skills/
```

Invoke with `$teaching-html-story-deck`.

## Quick start

```text
$teaching-html-story-deck

把这篇系统设计文章变成一份可全屏讲解的单文件 HTML。
需要问题、原理、数据流、架构、实战和最后总结。
```

```text
$teaching-html-story-deck

优化这个已有 HTML。保留内容，但改成黑白克制、
现代开发者产品感的高级动效版本，并增加真正服务理解的 SVG。
```

```text
$teaching-html-story-deck

把我的开源 Agent Skill 做成一个故事型演示：
先讲为什么开发者会过早开工，最后一页再揭示 Skill。
```

## Key files

| File | Purpose |
|------|---------|
| `SKILL.md` | Core workflow, rules, and output contract |
| `references/user-preferences.md` | Persistent design and teaching preferences |
| `references/story-and-visual-framework.md` | Narrative spine and diagram selection rules |
| `references/svg-and-motion-system.md` | SVG implementation patterns and motion layers |
| `references/design-rationale.md` | Lessons from the Shape Up deck process |
| `references/quality-gates.md` | Final review checklist |
| `scripts/validate_deck.py` | Standalone HTML validator |
| `scripts/static_check.py` | Skill structure validator |
| `scripts/init_deck.py` | Scaffold a new deck from template |
| `examples/` | Worked Shape Up example with full source |

## Validation

```bash
# Static check (skill structure, references, evals)
python scripts/static_check.py

# Validate bundled example
python scripts/validate_deck.py examples/shapeup-skill-linear-vercel-deck.html

# Run all checks
python scripts/check.py
```

Output:

```
PASS skill structure
PASS references
PASS eval JSON
PASS doctype
PASS title
PASS viewport
PASS slides
PASS script
PASS keyboard
PASS fullscreen
PASS reduced_motion
PASS no_external_scripts
PASS no_external_styles
PASS svg_accessibility
slides=10  svgs=7  accessible_svgs=7
```

## Design philosophy

The deck succeeds when the audience can explain the topic after seeing it—not merely when the page looks impressive.

- The strongest visual makes a relationship obvious.
- The strongest animation makes a state change understandable.

### Non-negotiable principles

1. **Narrative before decoration.** Decide what the audience must understand, and in what order, before choosing visuals.
2. **Show relationships.** Turn sequence, dependency, authority, scope, uncertainty, and transformation into visuals.
3. **Generate visuals from the content.** Do not reuse the same diagram blindly.
4. **Motion explains state.** Animation should reveal hierarchy, direction, progress, or state change.
5. **One file, no build step.** Inline CSS, JavaScript, and SVG. No CDNs or external dependencies.
6. **High finish, restrained design.** Near-black surfaces, fine borders, sparse luminous accents.
7. **No invented evidence.** Never fabricate metrics, benchmarks, or research results.
8. **Label conceptual models.** A proposed mental model is not measured data.
9. **The deck must work without animation.** Respect `prefers-reduced-motion`.
10. **Do not imitate brands exactly.** Borrow qualities such as precision and restraint; never copy logos or proprietary layouts.

## Supported agents

- Claude Code — `/teaching-html-story-deck`
- Cursor / Windsurf — `$teaching-html-story-deck`
- OpenCode — `$teaching-html-story-deck`
- Codex CLI — add command to `.codex/config.json`
- Any custom text agent with file-system access

## Documentation

| Document | Description |
|----------|-------------|
| `CHANGELOG.md` | Version history and release notes |
| `references/` | Full design system documentation |
| `evals/` | Evaluation cases and scoring rubric |
| `examples/` | Complete worked example (Shape Up story deck) |
| `scripts/` | Validation, scaffolding, and static analysis tools |

## License

MIT © 2026 [lora-sys](https://github.com/lora-sys)

See [LICENSE](./LICENSE).

---

<div align="center">

**Problem → Why → Method → Data flow → Architecture → Example → Reveal**

[⭐ Star](https://github.com/lora-sys/teaching-html-story-deck) · [🐛 Issues](https://github.com/lora-sys/teaching-html-story-deck/issues) · [🤝 Contribute](https://github.com/lora-sys/teaching-html-story-deck/blob/main/CONTRIBUTING.md)

</div>
