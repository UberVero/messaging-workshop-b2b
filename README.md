# [Eldur Studio](https://eldur.studio) Plugins

This repository contains [Eldur Studio](https://eldur.studio) plugins for ChatGPT and Codex.

## Available plugin

### B2B Messaging Workshop

A guided, evidence-aware workshop that takes a founder or product marketer through company context, product-marketing strategy, positioning, and a six-part pressure test. 
It's grounded in a decade of B2B product marketing experience at companies like Verizon and Amazon, and countless client engagements where I was tasked with the #1 job of Product Marketing: write a clear, defensible positioning for a company/product that can be developed into all sort of marketing messaging: website copy, sales slides, LinkedIn profile, RFP responses, etc.
Consistency is key. 

The structure of the interview and related questions and prompts are all original, but the framework closely follows [April Dunford's approach](https://www.aprildunford.com/) and it has been updated to modern standards. The pressure tests uses rigorous principles, I credit [Emily Kramer](https://www.mkt1.co/) with the approach and I recommend her MCP, which inspired me to "clone myself" in this plugin.

It produces a clean Markdown document as Product Marketing source of truth for your product that can be also imported to Notion.

Please allow 30m to 1 h to go through the workshop (it will be worth it). If you find yourself struggling to provide answers, use it as a sign your business strategy might not be there and take time for reflecting and pivoting, then try again. Quick, superficial answers will produce poor results.

## Install in ChatGPT desktop

No Terminal is required.

1. Open [B2B Messaging Workshop in the Plugins Directory](https://chatgpt.com/plugins/plugins_6a8f237c51488191a3bb6c3accefc4b5).
2. Select **Install plugin**.
3. Start a new chat and enter:

   ```text
   Start my B2B messaging workshop.
   ```

You can also open **Plugins** in ChatGPT, search for **B2B Messaging Workshop**,
and select **Install plugin**. In a new chat, type `@B2B Messaging Workshop` to
select it explicitly. See [OpenAI's plugin installation guide](https://learn.chatgpt.com/docs/plugins)
for more information.

## Install in Codex CLI

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

## Update a Git marketplace installation

Plugins installed from ChatGPT's public directory receive the currently
published version. If you installed the Git marketplace version in Codex,
refresh its snapshot and reinstall the plugin:

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

The canonical messaging framework and its guidance are owned by [Eldur Studio LLC](https://eldur.studio). Copyright [Eldur Studio LLC](https://eldur.studio) 2026.

## License

You may install and use the workshop personally or inside your organization,
including for a commercial business. You own the messaging and other original
outputs you create with it.

The workshop itself may not be resold, redistributed, white-labeled, offered as
a paid client service, or used to create a competing product without written
permission from [Eldur Studio](https://eldur.studio). See [LICENSE](LICENSE) for the complete terms.
