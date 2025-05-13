# System Patterns

## Recurring Patterns
- Modular, layered architecture: strict separation of UI (renderer), backend logic (main), and API/service layers
- Secure IPC and contextIsolation for all main-renderer communication
- Provider pattern for all LLM and media API integrations (OpenAI, Anthropic, Gemini, Grok, Groq, FAL)
- Service abstraction for Git, storage, and external APIs (never direct calls from UI)
- All sensitive operations and secrets handled in main process only
- All state and config persisted in encrypted SQLite; migrations for schema changes
- All workflows, rules, and compliance enforced via .md files and validation scripts
- Continuous documentation and memory updates at every milestone
- All technical decisions logged in ADRs and decisionLog.md

## Standards
- All code strictly typed with TypeScript
- All React components and hooks follow strict linting and best practices (no conditional hooks, direct ref usage, etc.)
- All API/service modules have robust error handling, input validation, and output sanitization
- All API key management via Keytar/OS keychain
- All Git operations via NodeGit abstraction, never CLI or shell from renderer
- All external API responses validated and sanitized before use
- All code, features, and workflows adhere to Windsurf Master Global Rules and workspace overrides
