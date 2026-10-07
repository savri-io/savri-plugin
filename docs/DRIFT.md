# Distribution history

## 2026-10-07, Codex: guided start source published, ChatGPT in review

Published portable Agent Plugin 1.2.0 (`663c75c`, annotated `v1.2.0`),
then compatibility patch 1.2.1 (`d12dc12`, annotated `v1.2.1`). Each release
was pushed atomically with main. All seven files retrieved from the public
1.2.1 tag match the prepared package. License, icon and MCP endpoint remain
intact. Package schema and skill validation passed.

The dashboard requires the existing package identity, so 1.2.1 preserves
`app-6a92b83f356881918b51987e6312ab4a`. The original published tag was not
changed. The upload to the existing Savri app succeeded. The dashboard's
downloaded archive contains the same seven file contents; its ZIP container
hash differs because the dashboard repacks the archive.

Metadata and skill checks passed. After correcting write annotations in the
remote MCP server, all 30 tools are Live with no scan issues. Version 1.2.1
was submitted and is **In review** on 2026-10-07; the public ChatGPT listing
still publishes **1.1.0**. Existing targeting and reviewer settings were
preserved. Submission is not catalog publication or an installed-client test.

**Source distribution complete; ChatGPT delivery partially complete.**
Next: after OpenAI approval, the executing agent publishes 1.2.1 on the same
app and verifies its actual catalog installation and guided-start journeys.
No new publishing authorization is required. No recurring task was created.
Historical reports below were moved from CLAUDE.md. Documentation is
committed/pushed separately without changing version tags.

## 2026-09-15, Codex


På Aarons Google/Bing-releaseorder: **1.1.0**, fyra selektivt synkade filer
(manifest, README, skill och botprofil). Åtta sökläsningar i remote MCP 1.1.0,
27 verktyg. Google använder sajtens koppling, Bing användarens personliga.
Filerna matchar källan; endast CRLF/LF normaliserat vid textjämförelsen.
Ikon byteidentisk, befintliga mcp.json och licens bevarade.

**Publicerad 15/9:** main och annoterad `v1.1.0` pushade atomärt till
`1f4080bb5b741040cbe360cf1932a6233366695a`, fjärrtaggens commit återläst.
Alla sju paketfiler hämtade från den publika taggen och matchade mot källan.
Manifest och mcp.json validerade mot Agent Plugins officiella 1.0.0-scheman.
Generisk MCP SDK läste distribuerad mcp.json: 27 verktyg, remote 1.1.0 och
riktiga Google-/Bingöversikter gröna. Testets credentials/poster därefter städade.
Detta bevisar paketet/protokollet; faktisk Cursor-/Grok-installation är ännu
inte verifierad. Ingen marketplacepublicering eller formatkonvertering gjord.
Full kanalstatus: källrepots `docs/impl/gsc-mcp-bwt-analys-2026-09-15.md`, avsnitt 15.
Todoist: befintlig `6hWHc3Wm3G2FrwqM`, öppen 22 september.
