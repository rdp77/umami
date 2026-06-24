---
name: fix-dropdown-ui
description: Workflow command scaffold for fix-dropdown-ui in umami.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /fix-dropdown-ui

Use this workflow when working on **fix-dropdown-ui** in `umami`.

## Goal

Adjust dropdown UI components for better usability, such as changing maxHeight or pageSize.

## Common Files

- `src/components/input/*Select.tsx`
- `src/app/(main)/settings/preferences/*.tsx`
- `src/app/(main)/websites/[websiteId]/*/*.tsx`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit one or more dropdown-related component files (e.g., WebsiteSelect.tsx, BoardSelect.tsx, etc.).
- Adjust properties like maxHeight or pageSize.
- Test the dropdown in the UI.
- Commit the changes, often touching multiple dropdown components at once.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.