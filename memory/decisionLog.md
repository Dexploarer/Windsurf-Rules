# Decision Log

## 2025-05-13
- Adopted Electron + React + Typescript as core stack for cross-platform desktop app
- Enforced strict main/renderer separation and secure IPC as per Electron/OWASP best practices
- All API keys and secrets to be handled via Keytar/OS keychain in main process only
- All LLM/media APIs to be integrated via modular provider pattern (OpenAI, Anthropic, Gemini, Grok, Groq, FAL)
- NodeGit is not compatible with Node.js 24.x on Windows (see GitHub issue #1259); switching to simple-git for cross-platform Git integration
- All Git operations abstracted via simple-git and handled in main process
- SQLite chosen for local, encrypted project and config storage
- All rules, workflows, and compliance enforced via .windsurf/ .md files and validation scripts
- All technical decisions to be logged in ADRs and decisionLog.md for traceability
