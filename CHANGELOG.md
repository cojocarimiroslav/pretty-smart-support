# Changelog

## 0.1.1

Maintenance and release cleanup update.

### Changed

- Simplified the VS Code extension contribution metadata to reduce confusing menu and command-palette entries.
- Kept the public extension surface focused on the supported PRetty Smart workflow.
- Updated package metadata for a cleaner Marketplace release.

### Removed

- Removed experimental, debug, and development-only commands from the public VS Code UI.
- Removed confusing menu entries that were not needed for the Logitech-driven workflow.
- Removed unreleased or unreliable review actions from the public command surface.
- Removed leftover references to non-final review workflows from the extension package metadata.

### Notes

- Core Logitech-to-VS Code local bridge behavior is unchanged.
- This update is focused on Marketplace polish and reducing user-facing confusion.


## 0.1.0

Initial public release target.

### Added

- Logitech Actions SDK plugin for PRetty Smart.
- VS Code local bridge on `127.0.0.1:56789`.
- GitHub provider detection through repository remotes.
- GitHub Pull Requests extension integration.
- Next / Previous Change navigation.
- Next / Previous Review Comment navigation.
- Display-only review comment panel.
- Delete Current Review Comment.
- AI-assisted review drafts.
- Multiple refined draft variants.
- Draft option selection.
- Add Selected Draft at Cursor.
- Submit final review as Comment.
- Submit final review as Approve.
- Submit final review as Request Changes.
- Copy Draft and Clear Draft.
- Open VS Code Extension setup action.
- Recommended Logitech profiles for MX Creative Keypad and MX Creative Dialpad.

### Known limitations

- GitHub is the primary supported provider in version 0.1.0.
- GitLab, Azure DevOps, and Bitbucket workflows are not fully implemented.
- PRetty Smart relies on the GitHub Pull Requests extension and the active PR model in VS Code.
- GitHub review permissions and repository rules still apply.

