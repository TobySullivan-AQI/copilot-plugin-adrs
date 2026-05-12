# AGENTS.md

## Versioning

This plugin uses [Semantic Versioning](https://semver.org/) (SemVer). The version is stored in the `version` field of `plugin.json`.

**Always increment the version in `plugin.json` before preparing a pull request.**

### Version format

The version follows the pattern `MAJOR.MINOR.PATCH`:

- **PATCH** — Backward-compatible bug fixes and minor corrections.
- **MINOR** — Backward-compatible new functionality.
- **MAJOR** — Breaking changes that are not backward-compatible.

### When to increment each segment

#### PATCH (e.g. `0.1.0` → `0.1.1`)

Increment the patch version for changes that fix bugs or make small improvements without adding new features or breaking existing behavior.

Examples:
- Fixing a typo or inaccuracy in an agent prompt or skill description
- Correcting a broken link in documentation
- Fixing a regex or template that was producing incorrect output

#### MINOR (e.g. `0.1.1` → `0.2.0`)

Increment the minor version when adding new functionality that is backward-compatible. Reset the patch version to `0` when incrementing minor.

Examples:
- Adding a new agent to the `agents/` directory
- Adding a new skill to the `skills/` directory
- Adding a new optional field to `plugin.json` (e.g. `keywords`)
- Expanding an existing agent or skill with additional capabilities

#### MAJOR (e.g. `0.2.0` → `1.0.0`)

Increment the major version for changes that break backward compatibility. Reset the minor and patch versions to `0` when incrementing major.

Examples:
- Removing or renaming an existing agent or skill
- Changing the behavior of an agent or skill in a way that alters its expected output
- Restructuring `plugin.json` in a way that requires users to reinstall or reconfigure
- Changing the plugin name or directory structure
