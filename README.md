# Eldur Studio Codex Plugins

This Git marketplace distributes Eldur Studio plugins for Codex.

## Available plugin

### B2B Messaging Workshop

A guided, evidence-aware workshop that takes a founder or product marketer through company context, product-marketing strategy, positioning, and a six-part pressure test. It produces a Markdown source of truth and can optionally create a separate Notion page after the user confirms the write.

## Install in Codex

Add this Git repository as the `eldur-studio` marketplace:

```bash
codex plugin marketplace add UberVero/messaging-workshop-b2b --ref main
```

Then install the workshop:

```bash
codex plugin add messaging-workshop-b2b@eldur-studio
```

Start a new Codex task so the plugin is loaded, then select **B2B Messaging Workshop** or enter:

```text
Start my B2B messaging workshop.
```

## Update

Refresh the marketplace snapshot and reinstall the plugin:

```bash
codex plugin marketplace upgrade eldur-studio
codex plugin add messaging-workshop-b2b@eldur-studio
```

## Repository layout

- `.agents/plugins/marketplace.json` — marketplace identity and plugin listing.
- `plugins/messaging-workshop-b2b/` — the complete plugin package.
- `plugins/messaging-workshop-b2b/tests/` — reproducible behavioral acceptance cases and fixtures.

## Privacy and data handling

The plugin is skills-only. It has no hosted service, account, database, telemetry, or bundled customer data. It instructs Codex to ask before creating a Notion page and to preserve customer-source attribution and anonymization preferences.

The canonical messaging framework and its guidance are owned by Eldur Studio LLC. Copyright Eldur Studio LLC 2026.
