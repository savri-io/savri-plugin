# Savri analytics plugin

![Savri](assets/icon.png)

Connect your own [Savri](https://savri.io) account and ask about visitors, traffic sources, top pages, countries, goals, funnels, and registered event properties.

This [Agent Plugin](https://agent-plugins.org) packages Savri's hosted MCP connection and a web analytics skill. It runs no local server and contains no credentials. Cursor supports the Agent Plugins format. Marketplace approval and end-to-end Grok Bot compatibility are separate checks; this source repository does not imply a published marketplace listing.

## Search reports (1.1.0)

Remote MCP 1.1.0 provides 27 tools, including eight read-only Google/Bing reports. Package distribution and each directory's discovery/review are separate steps. Check the tools exposed by your installed client; this repository does not establish marketplace availability.

Connect Google Search Console or Bing Webmaster Tools in the site dashboard from Basic. Google uses the site's shared connection; Bing uses your own connection per site. The hosted OAuth connection needs no API key. The separate local `@savri/mcp` package requires an account API key and API access from Growth.

Search tools are `savri_get_gsc_overview`, `savri_get_gsc_queries`, `savri_get_gsc_pages`, `savri_get_gsc_trend`, `savri_get_bing_overview`, `savri_get_bing_queries`, `savri_get_bing_pages`, and `savri_get_bing_trend`. Check which tools your client actually exposes. If these are missing, use the dashboard; do not infer an empty report.

- Google uses final days in Pacific Time, exact page/query filters, optional country/device and equal-length comparisons. Limited candidate rows are not a complete query history; missing values remain unknown.
- Bing daily traffic and weekly Web query/page reports have different coverage. Select returned report dates without inventing week boundaries. Country/device filters are unsupported.
- These reports do not link a query to a person or order and do not provide separate AI citation counts. Keep sources and periods separate.

Guides: [Google](https://savri.io/docs/gsc), [Bing](https://savri.io/docs/bing), [API contract](https://savri.io/docs/public-api#search-reports).

## Requirements

- A Savri account with access to the website you want to analyze.
- Collected analytics for questions about your traffic. Install the [tracking script](https://savri.io/docs/integration-guides) first if needed.
- A client supporting Agent Plugins, Streamable HTTP MCP and client-managed OAuth. Workspace policies may restrict custom plugins.

## Connect

Install this package using your client's supported plugin workflow. The MCP server is:

```text
https://savri.io/api/mcp
```

When the client starts authentication, sign in to Savri in your browser and review the requested permissions. Never paste your password or access token into chat. Client-specific setup and availability are documented in [Savri's connector guides](https://savri.io/docs/connectors).

For manual Cursor MCP setup, add the following entry to your existing `mcpServers` object without replacing other servers:

```json
{
  "savri": {
    "url": "https://savri.io/api/mcp"
  }
}
```

That manual entry connects the server; it does not install the packaged skill. Restart or refresh the client's MCP connection, then complete OAuth when prompted. The actual callback must be accepted by Savri; a working desktop connection does not prove compatibility with every cloud client.

## Try it

- "Which of my sites can you access through Savri?"
- "Compare visitors to example.com over the last 7 days with the previous period."
- "Which pages and traffic sources brought the most visitors?"
- "Review the existing goals and funnels for example.com."
- "Show Google queries for example.com over the last seven final days, then show Bing’s latest weekly queries separately with actual coverage."

The skill selects a real site ID, keeps periods consistent, distinguishes observations from explanations, and avoids treating outbound clicks as purchases. Visitor analytics use rolling `7d`, `30d`, and `90d`. Google and Bing use the separate date contracts above.

## Permissions and data

OAuth controls access to your own authorized sites. The server supports read and write scopes. It can also create, rename, or delete supported resources when write access is granted; the analytics skill uses read tools for reporting. Skill instructions are not a security boundary.

Tool results are sent to the AI client you choose. Review that client's data settings and [Savri's privacy policy](https://savri.io/privacy). Each user authenticates separately; sharing the plugin does not share your account or data. Disconnect through your AI client's integration settings when you no longer need access.

## Optional Grok Bot profile

[Savri Analytics Analyst](bots/analytics-analyst.md) provides a suggested name and profile for a bot that uses this plugin. Create it only after verifying the connection in Grok Bot. It schedules nothing by default and contains no customer-specific data. Sharing a bot template does not automatically list it in the public Bot Marketplace.

## Package and maintenance

- `plugin.json`: portable manifest.
- `mcp.json`: hosted server definition.
- `skills/web-analytics/SKILL.md`: reporting workflow and interpretation rules.
- `bots/analytics-analyst.md`: optional bot profile.

Source files are maintained by the Savri team and distributed here. This package is MIT licensed; using the hosted service is governed by [Savri's terms](https://savri.io/terms). For support, contact [hello@savri.io](mailto:hello@savri.io).
