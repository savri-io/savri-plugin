# Savri for Claude

Use Savri to check your website's measurement, understand booking interest
and sales, choose content from actual site and search data, and draft an
article when requested. This Claude plugin includes the guided analytics
skill and uses the existing Savri connector with your own account.

## Install and connect

Download **savri-claude-plugin-1.2.2.zip** from the
[Claude release](https://github.com/savri-io/savri-plugin/releases/tag/claude-v1.2.2).
On claude.ai, open **Customize > Plugins > Add > Upload plugin** and select
that ZIP. Open the plugin's **Connectors** tab and connect Savri through
the normal sign-in flow. If you already use the Savri directory connector,
this plugin uses the same `https://savri.io/api/mcp` URL. Keep that account
connection; never paste passwords, API keys or tokens into chat.

Start a new chat and check that Claude has the `web-analytics` skill from
Savri and can list your sites. Installing the connector by itself does not
install this skill. Workspace policies may restrict custom plugins.
For Claude Code, use `claude --plugin-dir ./claude` from a checkout of this
repository and connect through the MCP authentication UI when prompted.

## Ask naturally

- Help me get more bookings or enquiries from my website.
- Help me understand how my website contributes to sales.
- What content should I write next based on my website data? Draft an article.

The workflow checks available measurement, explains missing access or data,
then answers the business question using the evidence that exists. It keeps
booking-link clicks separate from confirmed bookings and labels hypotheses.
An article request produces a draft in your chat using accessible business
material, without inventing business claims or publishing automatically.

Google uses the site's shared connection; Bing uses your own connection
for that site. Connect providers in the site dashboard from Basic. Reports
keep source dates and coverage; they do not identify which person used a
search query or provide separate AI citation counts. Missing crawler
telemetry does not prove that no AI bots visited.

Saving a business profile, recording feedback or changing goals requires
your explicit request and the appropriate site role and write permission.
The plugin does not save conversation transcripts or create recurring work.
Sharing this package shares no account access. Each user connects separately.

## Release and verification

Version 1.2.2 uses the guided workflow from portable Savri 1.2.1, with
Claude context guidance and corrections from actual Claude client tests:
provide useful business help even without traffic data, avoid promising
unsupported attribution, and do not divide unrelated booking and click
totals into a conversion rate. The package and skill can be
validated locally; that does not establish installation in your Claude
account or availability through Anthropic's public directory. Directory
metadata is maintained separately through our existing Anthropic listing.

The canonical skill is maintained in `analytics-value/packages/agent-plugin`.
`scripts/prepare-claude-plugin.mjs` builds this package from that source;
maintainers should not edit its generated skill independently.

Guides: [Claude connection](https://savri.io/docs/connectors/claude),
[Google](https://savri.io/docs/gsc), [Bing](https://savri.io/docs/bing).
Review [Savri's privacy policy](https://savri.io/privacy) and the data
settings of your Claude account before connecting. MIT licensed;
hosted use follows [Savri's terms](https://savri.io/terms).
Support: [hello@savri.io](mailto:hello@savri.io).
