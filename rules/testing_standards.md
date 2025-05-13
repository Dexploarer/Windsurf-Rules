# Testing Standards

## General
- All code must be tested before merging to main/master.
- Use automated testing for all critical paths and business logic.
- All new features must include corresponding unit and integration tests.
- Test coverage must be >90% for all critical modules.
- All tests must be run in CI and must pass before merge.

## Tools
- Use Jest or Vitest for all JS/TS unit and integration tests.
- Use React Testing Library for React components.
- Use Spectron or Playwright for Electron end-to-end testing.
- Use ESLint and Prettier for linting and formatting checks.

## Types of Tests
- Unit tests for all functions, services, and hooks.
- Integration tests for API, IPC, and service interactions.
- End-to-end tests for all user workflows (chat, project management, research, media gen).
- Security tests for IPC, API, and sensitive flows.

## Review
- All test code must be reviewed with the same rigor as production code.
- All bugs must have a regression test added before closing.

## Documentation
- All test suites must be documented with expected behavior and edge cases.
- Test results and coverage reports must be archived for each release.
