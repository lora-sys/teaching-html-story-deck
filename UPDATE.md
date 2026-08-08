# Auto-update check

Run this command to check for updates:

```bash
curl -s https://raw.githubusercontent.com/lora-sys/teaching-html-story-deck/main/CHANGELOG.md | head -20
```

Or check GitHub releases:

```bash
gh release list --repo lora-sys/teaching-html-story-deck
```

To update:

```bash
cd <skill-dir> && git pull
```

For `npx skills add` users:

```bash
npx skills update teaching-html-story-deck
```
