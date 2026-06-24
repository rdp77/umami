```markdown
# umami Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches the core development patterns, coding conventions, and common workflows used in the [umami](https://github.com/umami-software/umami) repository. Umami is a web analytics platform built with TypeScript and Next.js. The codebase emphasizes clarity, modularity, and consistency, with a focus on maintainable UI components and internationalization support.

## Coding Conventions

### File Naming

- Use **camelCase** for file names.
  - Example: `websiteSelect.tsx`, `boardSelect.tsx`

### Import Style

- Use **alias imports** for modules.
  - Example:
    ```typescript
    import { useUser } from 'lib/auth';
    import WebsiteSelect from 'components/input/websiteSelect';
    ```

### Export Style

- Mixed: Both default and named exports are used.
  - Example (default export):
    ```typescript
    export default WebsiteSelect;
    ```
  - Example (named export):
    ```typescript
    export function getUser() { ... }
    ```

### Commit Patterns

- Prefixes: `fix`, `refactor` (freeform, not strict)
- Messages are concise, averaging ~52 characters.
  - Example: `fix: update dropdown maxHeight for usability`

## Workflows

### Update Translations
**Trigger:** When you want to update, add, or refine translations for supported languages.  
**Command:** `/update-translation`

1. Edit or add the relevant JSON file(s) in `public/intl/messages` or `public/intl/country`.
2. Commit your changes with a message referencing the language and purpose.
   - Example: `fix: update French translations for dashboard`
3. Optionally, repeat for multiple languages in separate commits.

**Files Involved:**
- `public/intl/messages/*.json`
- `public/intl/country/*.json`

---

### Dependency Update
**Trigger:** When you need to update project dependencies for security, bugfixes, or new features.  
**Command:** `/update-dependencies`

1. Update `package.json` with new dependency versions.
2. Update `pnpm-lock.yaml` (or the relevant lockfile).
3. Test the build to ensure compatibility.
4. Commit both files together.
   - Example: `refactor: bump next.js to v13.4.0`

**Files Involved:**
- `package.json`
- `pnpm-lock.yaml`

---

### Fix Dropdown UI
**Trigger:** When you want to improve dropdown usability or fix display issues.  
**Command:** `/fix-dropdown`

1. Edit one or more dropdown-related component files (e.g., `websiteSelect.tsx`, `boardSelect.tsx`).
2. Adjust properties like `maxHeight` or `pageSize`.
   - Example:
     ```tsx
     <Dropdown maxHeight={320} pageSize={10} ... />
     ```
3. Test the dropdown in the UI.
4. Commit the changes, often touching multiple dropdown components at once.

**Files Involved:**
- `src/components/input/*Select.tsx`
- `src/app/(main)/settings/preferences/*.tsx`
- `src/app/(main)/websites/[websiteId]/*/*.tsx`

---

### Bugfix (Single File)
**Trigger:** When you need to fix a minor bug affecting a specific feature or component.  
**Command:** `/bugfix`

1. Identify the file with the bug.
2. Edit the file to fix the issue.
3. Test the fix locally.
4. Commit the change.
   - Example: `fix: correct typo in userMenu.tsx`

**Files Involved:**
- `src/components/**/*.tsx`
- `src/lib/**/*.ts`
- `src/queries/**/*.ts`

---

## Testing Patterns

- Test files follow the pattern: `*.test.*`
- The testing framework is not explicitly specified.
- Example test file: `userMenu.test.tsx`
- Tests are colocated with source files or in dedicated test directories.

## Commands

| Command               | Purpose                                                    |
|-----------------------|------------------------------------------------------------|
| /update-translation   | Update or add translations for supported languages         |
| /update-dependencies  | Update npm/yarn/pnpm dependencies                         |
| /fix-dropdown         | Adjust dropdown UI components for better usability         |
| /bugfix               | Fix a bug or issue isolated to a single file/component     |
```