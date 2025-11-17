# AGENTS.md - Guidelines for Agentic Coding in oc_sessions

## Build/Lint/Test Commands
- **Lint**: `shellcheck oc_sessions` (install shellcheck for bash linting)
- **Test**: No automated tests; manually run `./oc_sessions` to verify output
- **Single test**: N/A (no test suite)

## Code Style Guidelines
- **Language**: Bash scripting
- **Imports**: Use `#!/bin/bash` shebang; source external scripts if needed
- **Formatting**: 4-space indentation; consistent spacing around operators
- **Naming**: Functions in snake_case (e.g., `convert_time`); variables in UPPER_SNAKE_CASE for globals, lower_snake_case for locals
- **Types**: Bash is untyped; use `local` for function variables; validate inputs
- **Error Handling**: Use `||` for fallbacks; redirect stderr with `2>/dev/null`; exit codes for scripts
- **Comments**: Add comments for complex logic; keep concise
- **Best Practices**: Quote variables; use `[[ ]]` for tests; avoid global variables in functions
- **Dependencies**: Ensure jq and GNU date are available; check in script
- **Security**: Avoid eval; sanitize inputs; no secrets in code

No Cursor or Copilot rules found in repository.