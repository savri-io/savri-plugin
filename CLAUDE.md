# Savri Agent Plugin, publik distribution

Källa: `../analytics-value/packages/agent-plugin`. Detta är det portabla
Agent Plugin-formatet; konvertera inte till ett annat klientformat som bieffekt.
Main, selektiv staging och bevara befintliga mcp.json, ikon och licens.

## Status 2026-09-15, Codex

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
