---
name: github-workflow-update
description: Workflow command scaffold for github-workflow-update in soybean-admin.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /github-workflow-update

Use this workflow when working on **github-workflow-update** in `soybean-admin`.

## Goal

Updates GitHub Actions workflow files for CI/CD improvements or dependency bumps.

## Common Files

- `.github/workflows/*.yml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit .github/workflows/*.yml files to update action versions or workflow logic.
- Commit the updated workflow files.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.