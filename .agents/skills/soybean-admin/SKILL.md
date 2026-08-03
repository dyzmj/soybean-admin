```markdown
# soybean-admin Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and workflows used in the `soybean-admin` TypeScript codebase, which is built with the Vue framework. You'll learn the project's coding conventions, commit message style, testing patterns, and how to perform common maintenance workflows using standardized commands.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `dashboardView.vue`

### Import Style
- Use **alias imports** for modules.
  - Example:
    ```typescript
    import { fetchData } from '@/api/dataService';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```typescript
    export function calculateTotal(a: number, b: number): number {
      return a + b;
    }
    ```

### Commit Messages
- Follow **Conventional Commits** with these prefixes: `fix`, `chore`, `refactor`, `optimize`, `docs`
- Average commit message length: ~56 characters
  - Example:  
    ```
    fix: correct user permissions check in dashboard view
    ```

## Workflows

### Dependency Update Workflow
**Trigger:** When you need to update dependencies to their latest versions  
**Command:** `/update-deps`

1. Update version numbers in all relevant `package.json` files:
    - Root `package.json`
    - Each package: `packages/*/package.json`
2. Update the `pnpm-lock.yaml` lockfile to reflect new dependency versions.
3. Commit all updated `package.json` and lockfile files.

**Example:**
```bash
pnpm up -r
git add package.json packages/*/package.json pnpm-lock.yaml
git commit -m "chore: update dependencies"
```

### GitHub Workflow Update
**Trigger:** When you need to update or fix GitHub Actions workflows  
**Command:** `/update-github-workflow`

1. Edit `.github/workflows/*.yml` files to update action versions or workflow logic.
2. Commit the updated workflow files.

**Example:**
```bash
vim .github/workflows/ci.yml
git add .github/workflows/ci.yml
git commit -m "chore: update CI workflow to use latest node version"
```

## Testing Patterns

- **Test File Pattern:** Files are named with `*.test.*` (e.g., `userService.test.ts`)
- **Testing Framework:** Not specified in the repository analysis.
- **Test Example:**
  ```typescript
  import { calculateTotal } from './mathUtils';

  test('adds two numbers', () => {
    expect(calculateTotal(2, 3)).toBe(5);
  });
  ```

## Commands

| Command                  | Purpose                                               |
|--------------------------|-------------------------------------------------------|
| /update-deps             | Update all dependencies and lockfiles                 |
| /update-github-workflow  | Update GitHub Actions workflow files                  |
```
