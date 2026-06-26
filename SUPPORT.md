# PRetty Smart Support

## Before asking for help

Please check:

1. Visual Studio Code is open.
2. The PRetty Smart VS Code extension is installed and enabled.
3. The GitHub Pull Requests extension is installed and enabled.
4. A GitHub repository is open in VS Code.
5. A pull request is open or checked out through the GitHub Pull Requests extension.
6. The Logitech plugin can reach the VS Code bridge at `127.0.0.1:56789`.

## Useful diagnostic commands

Run these commands from the VS Code Command Palette:

- `PRetty Smart: Ping VS Code`
- `PRetty Smart: Diagnose Review Providers`
- `PRetty Smart: Diagnose GitHub Internal Comments`

Open the PRetty Smart output channel:

```text
View > Output > PRetty Smart
```

## Common issues

### The Logitech action opens a browser page

The Logitech plugin could not reach the PRetty Smart VS Code bridge. Open VS Code, install or enable the PRetty Smart extension, and try again.

### No active pull request model found

Open or checkout a pull request using the GitHub Pull Requests extension.

### Approve or Request Changes fails

GitHub may block the action if you are reviewing your own PR or if your account lacks permission to review the repository.

### AI provider unavailable

Use local fallback drafts, enable GitHub Copilot, or configure an OpenAI API key.

## Reporting issues

When reporting an issue, include:

- Operating system.
- VS Code version.
- PRetty Smart VS Code extension version.
- Logitech plugin version.
- Logi Options+ version.
- GitHub Pull Requests extension version.
- Output from `PRetty Smart: Diagnose Review Providers`.
- Output from `PRetty Smart: Diagnose GitHub Internal Comments`, if relevant.
- Steps to reproduce the problem.

Do not include private repository code, API keys, tokens, or confidential review text in public bug reports.

