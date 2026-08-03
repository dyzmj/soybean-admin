---
name: dependency-update-workflow
description: Workflow command scaffold for dependency-update-workflow in soybean-admin.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /dependency-update-workflow

Use this workflow when working on **dependency-update-workflow** in `soybean-admin`.

## Goal

Updates project dependencies across multiple package.json files and lockfile.

## Common Files

- `package.json`
- `packages/*/package.json`
- `pnpm-lock.yaml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update version numbers in package.json files across packages.
- Update the pnpm-lock.yaml lockfile to reflect new dependency versions.
- Commit all updated package.json and lockfile files.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.