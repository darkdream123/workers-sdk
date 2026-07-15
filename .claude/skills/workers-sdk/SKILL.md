```markdown
# workers-sdk Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `workers-sdk` TypeScript codebase. You'll learn about file naming, import/export styles, commit conventions, and how to structure and run tests. While no explicit workflows were detected, this guide provides best practices and suggested commands for common development tasks.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myWorkerFile.ts`

### Import Style
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { myFunction } from './utils';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    export function myFunction() { /* ... */ }
    export const MY_CONSTANT = 42;
    ```

### Commit Patterns
- Commit messages are **freeform** with no strict prefix requirements.
- Average commit message length is about 62 characters.
  - Example:
    ```
    Add support for custom worker configuration options
    ```

## Workflows

### Adding a New Module
**Trigger:** When you need to add new functionality to the SDK  
**Command:** `/add-module`

1. Create a new file using camelCase naming, e.g., `myNewModule.ts`.
2. Implement your functionality using named exports.
3. Use relative imports to reference other modules.
4. Write corresponding tests in a file named `myNewModule.test.ts`.
5. Commit your changes with a clear, descriptive message.

### Running Tests
**Trigger:** When you want to verify code correctness  
**Command:** `/run-tests`

1. Identify test files matching the `*.test.*` pattern.
2. Use the project's test runner (framework unknown; check project scripts).
3. Review test results and fix any failures.

### Refactoring Existing Code
**Trigger:** When improving or updating existing modules  
**Command:** `/refactor-module`

1. Locate the target file (camelCase).
2. Update code, maintaining named exports and relative imports.
3. Update or add tests as needed.
4. Commit changes with a descriptive message.

## Testing Patterns

- Test files follow the pattern: `*.test.*` (e.g., `utils.test.ts`).
- The specific testing framework is not detected; check project documentation or scripts for details.
- Place tests alongside or near the modules they cover.
- Example test file:
  ```typescript
  import { myFunction } from './myModule';

  test('myFunction returns correct value', () => {
    expect(myFunction()).toBe(42);
  });
  ```

## Commands
| Command         | Purpose                                    |
|-----------------|--------------------------------------------|
| /add-module     | Scaffold and add a new module              |
| /run-tests      | Run all test files in the project          |
| /refactor-module| Refactor an existing module                |
```
