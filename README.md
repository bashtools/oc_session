# oc_sessions - Opencode Session Lister

## Description
A bash script that scans the opencode session storage directory for JSON files,
extracts key metadata (session ID, working directory, title, and creation
timestamp), and outputs a formatted markdown table for easy viewing of past
sessions.

Note: There is also a more feature rich version written in Go available at
[github.com/mclarkson/ocs](https://github.com/mclarkson/ocs).

## Installation
1. Clone the repository: `git clone https://github.com/bashtools/oc_session`
2. Ensure jq and glow are installed (`brew install jq glow` on macOS or `apt
   install jq` and `snap install glow` on Ubuntu).
3. Run `make` to copy the script to `~/.local/bin`, or place it manually in your PATH.

## Usage
Run the script to generate a table of sessions:
```bash
./oc_sessions
```
This will output a markdown table like:
| id | directory | title | time |
|----|-----------|-------|------|
| ... | ... | ... | ... |

## Requirements
- jq for JSON parsing
- glow for markdown rendering (install with `brew install glow` on macOS or
  `snap install glow` on Linux)
- Bash shell
- GNU date for timestamp conversion (install with `brew install coreutils`
  on macOS)
- Access to ~/.local/share/opencode/storage/session/global directory

## Contributing
Feel free to submit issues or pull requests for improvements.

## License
MIT
