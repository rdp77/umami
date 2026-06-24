---
name: dependency-update
description: Workflow command scaffold for dependency-update in umami.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /dependency-update

Use this workflow when working on **dependency-update** in `umami`.

## Goal

Update npm/yarn/pnpm dependencies to newer versions, including major upgrades.

## Common Files

- `package.json`
- `pnpm-lock.yaml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update package.json with new dependency versions.
- Update pnpm-lock.yaml (or equivalent lockfile).
- Test the build for compatibility.
- Commit both files together.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.