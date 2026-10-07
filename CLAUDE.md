# Savri Agent Plugin, publik distribution

Källa: `../analytics-value/packages/agent-plugin`. Detta är det portabla
Agent Plugin-formatet; konvertera inte till ett annat klientformat som bieffekt.
Main, selektiv staging och bevara befintliga mcp.json, ikon och licens.

## Current status 2026-10-07

Version **1.2.1** source/tag published. Submitted to the existing OpenAI
plugin; **In review**, while the public ChatGPT listing remains **1.1.0**.
Metadata/skill checks passed; all 30 remote MCP tools are Live.
Full installation from the updated public listing remains to be verified.

Claude adapter source: `../analytics-value/packages/claude-plugin`, built
by `scripts/prepare-claude-plugin.mjs` from the shared skill. Distribute in
`claude/`, with separate `claude-v1.2.1` tag/ZIP. Only the host context
paragraph differs; preserve the portable root and its existing release tags.
Anthropic listing edits use the established mail thread. Publishing this
adapter does not prove installation in Claude or directory publication.

Session reports belong in [docs/DRIFT.md](docs/DRIFT.md), newest first.
