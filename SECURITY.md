# Security Policy

## Supported versions

| Version | Supported |
| --- | --- |
| 0.1.x | Yes |

## Reporting a vulnerability

Please report security issues privately through the maintainer contact listed in the Marketplace listing or repository.

Do not open a public issue containing:

- API keys.
- GitHub tokens.
- Private repository contents.
- Confidential review comments.
- Vulnerability details that could harm users before a fix is available.

## Security model

PRetty Smart has two local components:

- Logitech plugin.
- VS Code extension.

The Logitech plugin sends local command names to the VS Code extension through localhost.

The VS Code extension may interact with:

- The local workspace.
- Git metadata.
- GitHub Pull Requests extension.
- GitHub review workflows.
- Optional AI providers.

## Sensitive data

PRetty Smart may process repository metadata, selected review text, diff snippets, and pull request comments.

PRetty Smart does not intentionally collect telemetry, sell data, or run a backend service.

OpenAI API keys are stored using VS Code SecretStorage.

## Recommendations

- Do not paste secrets into review drafts.
- Review AI-generated text before posting.
- Keep VS Code, Logi Options+, GitHub Pull Requests, and PRetty Smart updated.
- Disable AI provider features if your organization does not allow sending code snippets to external AI services.
- Avoid sharing diagnostic logs publicly without reviewing them first.

