---
name: update-translations
description: Workflow command scaffold for update-translations in umami.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-translations

Use this workflow when working on **update-translations** in `umami`.

## Goal

Update or add translations for one or more languages to improve consistency, clarity, or coverage.

## Common Files

- `public/intl/messages/*.json`
- `public/intl/country/*.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or add the appropriate JSON file(s) in public/intl/messages or public/intl/country.
- Commit the changes with a message referencing the language and purpose.
- Optionally, repeat for multiple languages in separate commits.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.