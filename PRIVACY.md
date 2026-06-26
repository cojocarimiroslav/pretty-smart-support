# PRetty Smart Privacy Policy

Effective date: 2026-06-18

PRetty Smart is a developer productivity tool for pull request review workflows in Visual Studio Code and Logitech devices.

This document explains what data PRetty Smart accesses, how it is used, and what may be sent to third-party services when optional AI features are enabled.

## Summary

PRetty Smart does not sell user data, does not include advertising, and does not collect analytics or telemetry.

PRetty Smart only processes data needed for pull request review workflows.

## Components

PRetty Smart has two components:

1. **Logitech plugin**
   - Runs through Logi Options+ / Logi Plugin Service.
   - Sends local command names to the VS Code extension through `http://127.0.0.1:56789/command`.
   - Does not send repository contents, source code, comments, or AI prompts to external services.

2. **VS Code extension**
   - Runs inside Visual Studio Code.
   - Reads local workspace and pull request context needed to perform review actions.
   - May send limited context to an AI provider if AI features are enabled.

## Data processed locally

The VS Code extension may access:

- Current workspace folder.
- Git remote information.
- Current branch information.
- Changed file names.
- Git diff snippets.
- Selected text in the editor.
- Current review cursor position.
- Current draft text.
- GitHub pull request review comments visible through the GitHub Pull Requests extension.
- Active pull request state from the GitHub Pull Requests extension.

This data is used to:

- Navigate pull request changes.
- Generate or refine review drafts.
- Display selected review comments.
- Add drafts to GitHub review comments.
- Submit final pull request reviews.

## Data sent over localhost

The Logitech plugin sends only command payloads to the VS Code extension, for example:

```json
{ "command": "nextChange" }
```

This communication uses localhost only:

```text
http://127.0.0.1:56789/command
```

No external server is used for the Logitech-to-VS Code bridge.

## AI provider data

If AI features are enabled, PRetty Smart may send limited review context to the configured AI provider.

This may include:

- Selected review text.
- Rough comment drafts typed by the user.
- Changed file names.
- Git diff snippets.
- Short previews of new or untracked text files.
- PR summary context.

PRetty Smart does not automatically send the entire repository.

PRetty Smart does not automatically modify code.

## AI providers

PRetty Smart can use:

- VS Code language models, such as GitHub Copilot, when available.
- OpenAI-compatible API endpoints when configured by the user.
- Local fallback text generation when no AI provider is available.

Data sent to GitHub Copilot, OpenAI, or another configured provider is handled according to that provider’s own terms and privacy policy.

## API keys and secrets

If the user configures an OpenAI API key, it is stored locally using VS Code SecretStorage.

PRetty Smart does not hard-code API keys and does not intentionally write API keys to logs.

## GitHub data

PRetty Smart uses the GitHub Pull Requests extension to work with active pull requests.

Depending on the command, PRetty Smart may trigger GitHub review actions, including:

- Adding review comments.
- Deleting the selected review comment.
- Submitting a review comment.
- Approving a pull request.
- Requesting changes.

GitHub permissions and repository rules still apply.

## Telemetry

PRetty Smart does not include custom telemetry or analytics in version 0.1.0.

## Logs

PRetty Smart writes diagnostic messages to the VS Code Output panel and Logitech plugin logs. These logs are intended for troubleshooting.

Avoid sharing logs publicly if they include repository names, file paths, branch names, or review text.

## Data retention

PRetty Smart does not run a backend service and does not store user data on a PRetty Smart server.

Local state, drafts, settings, and secrets remain on the user’s machine, inside VS Code or the Logitech plugin environment.

## User control

Users can:

- Disable AI by setting `prettySmart.aiProvider` to `disabled`.
- Clear the OpenAI API key with `PRetty Smart: Clear OpenAI API Key`.
- Review drafts before posting.
- Cancel final review actions before running them.
- Uninstall the PRetty Smart VS Code extension.
- Remove the PRetty Smart Logitech plugin.

## Contact

For privacy questions, contact the project maintainer through the support channel listed in the Marketplace listing or repository.

