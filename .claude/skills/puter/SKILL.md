```markdown
# puter Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development conventions and workflows for the `puter` repository, a TypeScript project using the Express framework. You'll learn how to structure code, follow commit patterns, and write tests in alignment with the project's established practices.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userController.ts`, `apiRoutes.ts`

### Import Style
- Use **relative imports** for modules within the project.
  ```typescript
  import { getUser } from './userService';
  ```

### Export Style
- Use **named exports** for all modules.
  ```typescript
  // userService.ts
  export function getUser(id: string) { ... }
  export const USER_ROLE = 'admin';
  ```

### Commit Patterns
- Follow **conventional commit** style.
- Use the `chore` prefix for maintenance commits.
  - Example: `chore: update dependencies for security patches`
- Keep commit messages concise (average 77 characters).

## Workflows

### Code Contribution
**Trigger:** When adding or updating features, bug fixes, or refactoring.
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Make changes following coding conventions.
3. Write or update tests as needed.
4. Commit using the conventional commit style.
   ```bash
   git commit -m "chore: add new API endpoint for user data"
   ```
5. Push your branch and open a pull request.

### Dependency Update
**Trigger:** When dependencies need to be updated.
**Command:** `/update-deps`

1. Run the package manager to update dependencies.
   ```bash
   npm update
   ```
2. Test the application to ensure compatibility.
3. Commit changes with a `chore` prefix.
   ```bash
   git commit -am "chore: update dependencies"
   ```

## Testing Patterns

- Test files follow the `*.test.*` naming convention.
  - Example: `userService.test.ts`
- The specific testing framework is **unknown**, but tests are colocated with source files or in a dedicated test directory.
- Write tests for new features and bug fixes.

  ```typescript
  // userService.test.ts
  import { getUser } from './userService';

  describe('getUser', () => {
    it('returns user data for a valid ID', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command        | Purpose                                         |
|----------------|-------------------------------------------------|
| /contribute    | Start the code contribution workflow            |
| /update-deps   | Update project dependencies                     |
```
