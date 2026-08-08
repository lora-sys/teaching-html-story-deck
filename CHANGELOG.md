# Changelog

All notable changes to Teaching HTML Story Deck will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/2.0.0.html).

## [1.0.0] - 2026-08-05

### Added

- **Complete Agent Skill definition** — `SKILL.md` with full workflow, rules, and output contract
  - Problem-first narrative design principles (10 non-negotiable rules)
  - Content-to-visual mapping system (11 relationship types → diagram selection)
  - Inline SVG generation rules (accessibility, readability, semantic groups)
  - Restrained motion system (ambient, transition, reveal, semantic, interaction layers)
  - Presenter notes support (toggle with `N` key)
  - Upgrade mode for existing HTML presentations
  - Default precision-dark editorial design system
- **Persistent user preferences** — `references/user-preferences.md` with style, motion, and teaching defaults
- **Story and visual framework** — `references/story-and-visual-framework.md`
  - 10-step narrative blueprint (hook → problem → method → reveal)
  - 11 diagram-type selection rules
- **SVG and motion system** — `references/svg-and-motion-system.md`
  - Implementation patterns for inline SVG
  - CSS-first animation with JavaScript state management
- **Design rationale** — `references/design-rationale.md`
  - Lessons learned from the Shape Up story deck process
- **Quality gates** — `references/quality-gates.md`
  - 10-point final review checklist
- **Standalone HTML scaffold** — `scripts/init_deck.py`
- **HTML validator** — `scripts/validate_deck.py`
  - Checks: doctype, viewport, slides, keyboard, fullscreen, reduced-motion, no external deps, SVG accessibility
- **Static checker** — `scripts/static_check.py`
  - Validates skill structure, references, and eval JSON integrity
- **Agent adapter** — `agents/openai.yaml` for OpenCode / Cursor integration
- **Evaluation suite** — `evals/cases.json` (5 test cases) + `evals/RUBRIC.md` (7 categories, 17/21 passing)
- **Bundled example** — `examples/shapeup-skill-linear-vercel-deck.html`
  - Complete 10-slide Shape Up story deck with 7 accessible inline SVGs
- **Assets** — intake template, story blueprint template, visual map template, base HTML shell

### Design

- Precision-dark editorial style (near-black surfaces, fine borders, fluorescent yellow-green accent)
- No external dependencies by default (all CSS/JS/SVG inline)
- Keyboard navigation (arrows, space, Home/End, F fullscreen, O overview, N presenter notes)
- Responsive layout with `prefers-reduced-motion` support

### Planned

- [ ] More worked examples for different content types
- [ ] Additional diagram templates (sequence, Sankey, Sankey-like flow)
- [ ] Theme variants (light editorial, warm academic)
- [ ] Slide-to-video export helper
- [ ] Accessibility audit automation
