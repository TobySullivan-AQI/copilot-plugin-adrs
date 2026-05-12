# copilot-plugin-adrs

A [Copilot CLI plugin](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/about-cli-plugins) for managing Architecture Decision Records (ADRs).

## Install

```sh
copilot plugin install OWNER/copilot-plugin-adrs
```

Or from a local clone:

```sh
copilot plugin install ./copilot-plugin-adrs
```

## Verify

```sh
copilot plugin list
```

## Structure

```
copilot-plugin-adrs/
├── plugin.json   # Plugin manifest
├── agents/       # Agent profiles
└── skills/       # Skills
```
