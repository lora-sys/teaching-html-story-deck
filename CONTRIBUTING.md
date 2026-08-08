# Contributing to Teaching HTML Story Deck

Thank you for your interest in improving this skill!

## How to contribute

### Report issues

Open a GitHub issue with:
- The content type you tried to teach (e.g., architecture walkthrough, research paper)
- What the skill did well
- What could be improved (narrative, visuals, motion, accessibility)
- The prompt you used

### Add worked examples

1. Create a new file in `examples/` named `<topic>-deck.html`
2. Include presenter notes in `<script type="text/plain" class="presenter-notes">`
3. Ensure the deck passes `python scripts/validate_deck.py examples/your-deck.html`
4. Open a PR with a description of the teaching scenario

### Improve the skill definition

Changes to `SKILL.md` should be tested against all `evals/cases.json` cases and validated with `scripts/static_check.py`.

### Add diagram templates

New diagram types go in `references/svg-and-motion-system.md`. Each should include:
- When to use it (content signal)
- Minimal viable SVG structure
- Animation pattern
- Accessibility requirements

## Development workflow

```bash
# Clone your fork
git clone https://github.com/<you>/teaching-html-story-deck.git
cd teaching-html-story-deck

# Run checks
python scripts/static_check.py
python scripts/validate_deck.py examples/shapeup-skill-linear-vercel-deck.html

# Commit
git commit -m "feat: add X diagram template"
git push
```

## Code of conduct

Be precise, be kind. This skill is about clarity — the same standard applies to collaboration.
