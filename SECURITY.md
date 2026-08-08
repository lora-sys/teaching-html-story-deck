# Security Policy

## Supported versions

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a vulnerability

If you discover a security issue, please email the maintainer directly rather than opening a public issue.

## Security considerations

This skill is an **agent prompt and reference system** — it does not execute arbitrary code. The generated HTML decks are standalone files that run in the user's browser.

### Output safety

- The skill does not fetch remote resources by default.
- Generated HTML should not include inline event handlers that execute user input.
- SVG content should not contain `<script>` elements.
- No external CDN links unless the user explicitly requests them.

### Prompt injection

The skill documentation explicitly warns against treating vision model output or any external content as instructions. This same principle applies to the HTML output: presenter notes, SVG labels, and visible text are content, not instructions to the agent.

### Credential safety

The skill does not handle API keys or credentials. If you extend it with API integrations, follow the credential isolation principles from the upstream [free-vision-skill](https://github.com/lora-sys/free-vision-skill) project.
