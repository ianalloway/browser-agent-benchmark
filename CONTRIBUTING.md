# Contributing to browser-agent-benchmark

Thanks for your interest in improving the browser agent evaluation rubric!

## How to Contribute

### Reporting Issues

If you find a gap in the checklist, a misleading item, or have an idea for a new evaluation dimension, please open an issue:

1. Use the Bug Report template for errors or omissions
2. Use the Feature Request template to suggest new checklist items or scoring criteria

### Suggesting Checklist Changes

The checklist is the core of this project. When proposing changes:

1. **Fork** the repository
2. **Edit** `checklist.md` or `README.md`
3. **Open a PR** describing what evaluation gap your change addresses
4. For new checklist sections, include:
   - A clear section title
   - 3–5 concrete, testable items
   - How each item should be scored (0 / 1 / 2)

### Scoring Philosophy

Every checklist item must be:

- **Observable** — you can point to evidence (a screenshot, a log, a URL)
- **Binary in outcome** — either the agent did it or it didn't
- **Independent** — passing one item shouldn't require passing another

### Pull Requests

1. Fork and create a branch: `git checkout -b improvement/new-checklist-section`
2. Make your changes
3. Ensure the README and checklist remain consistent
4. Commit with a descriptive message
5. Open a Pull Request

## Style

- Markdown only
- One sentence per checklist item where possible
- No marketing language — this is a diagnostic tool
