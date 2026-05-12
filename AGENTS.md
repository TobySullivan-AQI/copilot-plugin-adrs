# AGENTS.md

## Versioning

This plugin uses [Semantic Versioning](https://semver.org/) (SemVer). The version is stored in the `version` field of `plugin.json`.

**Always increment the version in `plugin.json` before preparing a pull request.**

### Version format

The version follows the pattern `MAJOR.MINOR.PATCH`:

- **PATCH** — Backward-compatible bug fixes and minor corrections.
- **MINOR** — Backward-compatible new functionality.
- **MAJOR** — Breaking changes that are not backward-compatible.

### v0 — Initial development (current)

While the major version is `0`, the plugin is in initial development and the SemVer spec considers the API unstable ([spec item 4](https://semver.org/#spec-item-4)). During this phase, version segments shift right by one position compared to post-v1 rules:

| Change type              | Post-v1 bump | v0 bump            |
| ------------------------ | ------------ | ------------------ |
| Bug fix                  | PATCH        | PATCH              |
| New feature              | MINOR        | PATCH              |
| Breaking change          | MAJOR        | MINOR (reset patch to `0`) |

#### PATCH (e.g. `0.1.0` → `0.1.1`)

Increment the patch version for bug fixes **and** new backward-compatible functionality.

Examples:
- Fixing a typo or inaccuracy in an agent prompt or skill description
- Correcting a broken link in documentation
- Fixing a regex or template that was producing incorrect output
- Adding a new agent to the `agents/` directory
- Adding a new skill to the `skills/` directory
- Expanding an existing agent or skill with additional capabilities

#### MINOR (e.g. `0.1.3` → `0.2.0`)

Increment the minor version for breaking changes. Reset the patch version to `0`.

Examples:
- Removing or renaming an existing agent or skill
- Changing the behavior of an agent or skill in a way that alters its expected output
- Restructuring `plugin.json` in a way that requires users to reinstall or reconfigure
- Changing the plugin name or directory structure

#### MAJOR — Graduating to v1

Do **not** bump to `1.0.0` as part of a routine change. The transition to v1 is a deliberate decision that signals the plugin's public API is stable. Until that decision is made, use the v0 rules above.

### Post-v1 rules

Once the plugin reaches `1.0.0`, the standard SemVer rules apply:

#### PATCH (e.g. `1.0.0` → `1.0.1`)

Increment for backward-compatible bug fixes.

#### MINOR (e.g. `1.0.1` → `1.1.0`)

Increment for new backward-compatible functionality. Reset the patch version to `0`.

#### MAJOR (e.g. `1.1.0` → `2.0.0`)

Increment for breaking changes. Reset minor and patch to `0`.
