```markdown
# ragflow Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `ragflow` TypeScript codebase. You'll learn about file naming, import/export styles, commit conventions, and how to write and run tests following the project's standards. This guide is ideal for onboarding new contributors or maintaining consistency across the project.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myModule.ts`, `dataProcessor.ts`

### Import Style
- Use **relative imports** for modules within the repository.
  - Example:
    ```typescript
    import { processData } from './dataProcessor';
    ```

### Export Style
- Use **named exports** instead of default exports.
  - Example:
    ```typescript
    // dataProcessor.ts
    export function processData(input: string): string {
      // ...
    }
    ```

### Commit Messages
- Follow the **conventional commit** style.
- Use prefixes such as `chore`.
- Example:
  ```
  chore: update dependencies to latest versions
  ```

## Workflows

### Committing Changes
**Trigger:** When you are ready to commit code changes  
**Command:** `/commit`

1. Stage your changes:
   ```
   git add .
   ```
2. Write a commit message using the conventional commit format:
   ```
   git commit -m "chore: describe your change in present tense"
   ```
3. Push your changes:
   ```
   git push
   ```

### Writing New Modules
**Trigger:** When adding new functionality  
**Command:** `/new-module`

1. Create a new file using camelCase naming, e.g., `myFeature.ts`.
2. Use named exports for all exported functions or variables.
   ```typescript
   // myFeature.ts
   export function newFeature() {
     // implementation
   }
   ```
3. Import using relative paths where needed.

### Running Tests
**Trigger:** When you want to verify your code with tests  
**Command:** `/test`

1. Ensure your test files follow the `*.test.*` pattern, e.g., `myFeature.test.ts`.
2. Use the project's test runner (framework not specified; check project documentation or package.json).
3. Run the test command, e.g.:
   ```
   npm test
   ```
   or
   ```
   yarn test
   ```

## Testing Patterns

- Test files are named using the `*.test.*` pattern, such as `example.test.ts`.
- The specific testing framework is not detected; check the repository for more details.
- Example test file:
  ```typescript
  // myFeature.test.ts
  import { newFeature } from './myFeature';

  describe('newFeature', () => {
    it('should perform its task', () => {
      expect(newFeature()).toBe(/* expected result */);
    });
  });
  ```

## Commands
| Command      | Purpose                                   |
|--------------|-------------------------------------------|
| /commit      | Commit changes following conventions      |
| /new-module  | Create a new module with proper patterns  |
| /test        | Run tests in the codebase                 |
```
