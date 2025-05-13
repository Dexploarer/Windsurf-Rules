# Coding Standards

These standards apply to all code in this project:

## General
- Follow [Windsurf Master Global Rules](../rules/coding_standards.md) and all workspace-specific rules.
- Use Typescript for all frontend (React) and backend (Node.js/Electron) code.
- Enforce strict typing (`strict: true` in tsconfig).
- Use ES6+ features and modern JavaScript/Typescript idioms.
- Prefer functional programming and immutability where practical.
- All code must be linted and formatted using Prettier and ESLint (with recommended configs for React, Node, and Typescript).
- No dead code, commented-out code, or unused variables.

## Electron
- Keep main and renderer process logic strictly separated.
- Use IPC securely; never expose Node APIs to the renderer.
- All Electron APIs must be wrapped in secure, typed interfaces.
- Use contextIsolation and enable sandboxing.

## React
- Use function components and React hooks exclusively.
- All components must be typed with Typescript.
- Use CSS-in-JS or TailwindCSS for styling. No inline styles except for dynamic values.
- All state management must use React context or a dedicated state library (e.g., Redux Toolkit, Zustand) if context is insufficient.
- No direct DOM manipulation (use refs and effects).
- All user input must be sanitized and validated.

## Node.js
- Use async/await for all asynchronous code.
- All modules must be ES modules or use TypeScript import/export syntax.
- Never block the event loop (no sync file or network operations in main thread).
- Use environment variables for all secrets and configuration.

## Git
- All commits must reference a task, feature, or bug.
- No direct commits to main/master; use PRs with review.
- All feature branches must be rebased before merge.

## Security
- Never log or expose API keys or secrets.
- Use Keytar or OS keychain for all sensitive storage.
- Follow OWASP top 10 for Electron/Node/React.

## Testing
- All code must have unit and integration tests.
- Use Jest or Vitest for JS/TS testing.
- All critical paths must have >90% test coverage.

## Documentation
- All exported functions, classes, and components must have JSDoc/TSDoc comments.
- All APIs must be documented in OpenAPI (Swagger) format if public.

## Review
- All code must be reviewed by at least one other team member (or AI agent if solo).
- No merge without passing all CI checks.
