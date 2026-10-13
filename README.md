<img src="logo-400.png" alt="Diamond Painting Converter logo" width="96" height="96">

# Diamond Painting Converter MCP server

**Find your purchased diamond painting patterns and download the PDF with DMC colour legend.**

Remote MCP server: `https://diamondpaintingconverter.com/mcp` (Streamable HTTP) · Website: [diamondpaintingconverter.com](https://diamondpaintingconverter.com/)

## What it does

Diamond Painting Converter turns a photo into a diamond painting pattern. Through this MCP server an assistant finds the patterns already bought and linked to your account, checks the canvas size and drill type (round or square), and downloads the pattern PDF with the DMC colour legend.

It does not buy products, change designs or process payments. Purchases happen on the website.

## Connect

- **Server URL:** `https://diamondpaintingconverter.com/mcp`
- **Transport:** Streamable HTTP
- **Authentication:** OAuth with PKCE (S256), dynamic client registration and client ID metadata documents, so MCP clients connect without manual setup. Sign in with your diamondpaintingconverter.com account.

**Claude (claude.ai, Desktop):** Settings → Connectors → Add custom connector → paste the server URL.

**Claude Code:**

```bash
claude mcp add --transport http diamondpaintingconverter https://diamondpaintingconverter.com/mcp
```

**Cursor, VS Code, Cline, Windsurf and other clients** (`mcp.json` / `cline_mcp_settings.json`):

```json
{
  "mcpServers": {
    "diamondpaintingconverter": {
      "type": "http",
      "url": "https://diamondpaintingconverter.com/mcp"
    }
  }
}
```

Cline uses `"type": "streamableHttp"`; see [llms-install.md](llms-install.md).

## Tools

| Tool | What it does |
|---|---|
| `pattern_account / list_patterns` | Account and purchased patterns. |
| `prepare_pattern / render_pattern / get_pattern` | Check size and drill type, render, download the PDF. |

## Example prompts

- Which diamond painting patterns do I have?
- Download the pattern of my dog photo with the DMC legend.
- What size and drill type is my last pattern?

## Links

- Website: https://diamondpaintingconverter.com/
- Documentation: https://diamondpaintingconverter.com/plugin/
- Privacy policy: https://diamondpaintingconverter.com/plugin/privacy/
- Support: mailto:support@diamondpaintingconverter.com

## Keywords

diamond painting converter, photo to diamond painting, diamond painting pattern, DMC colour chart, custom diamond art, drill chart PDF.

Nederlands: diamond painting eigen foto, diamond painting patroon, DMC kleuren, foto omzetten naar diamond painting, diamond painting maken.

## More MCP servers by Samautomation

- [Scamchecker.nl](https://scamchecker.nl/): Check a suspicious email, SMS, WhatsApp message or link for scam signals (Netherlands, Belgium). ([listing](https://github.com/smrht/scamchecker-mcp))
- [Klussenbeheer](https://samdesk.nl/klussenbeheer/): Job management for Dutch service companies: jobs, customers, planning, quotes and invoices. ([listing](https://github.com/smrht/klussenbeheer-mcp))
- [Muziek maken met AI](https://muziekmakenmetai.nl/): Make an original song from a prompt or your own lyrics. Two versions per song, MP3 download. ([listing](https://github.com/smrht/muziekmakenmetai-mcp))
- [Beheer je WP](https://beheerjewp.nl/): Manage a WordPress site from your AI assistant: read, search, propose edits, Search Console data. ([listing](https://github.com/beheerjewp/beheerjewp-mcp))
- [UlazAI Media](https://ulazai.com/): Create private AI images with your UlazAI account: pick a model, confirm, generate, download. ([listing](https://github.com/ulazai/ulazai-mcp))
- [Backlinkswinkel](https://backlinkswinkel.nl/): Search Dutch websites for backlinks, check metrics and prices, order after confirmation, track. ([listing](https://github.com/backlinkswinkel/backlinkswinkel-mcp))
- [Backlinksbeheer](https://backlinksbeheer.nl/): Read your stored backlinks, link checks and lost-link alerts per domain. Read-only. ([listing](https://github.com/smrht/backlinksbeheer-mcp))
- [Samautomation Video](https://samautomation.work/): Render an MP4 from your own images, clips, voice-over and timed captions. JSON to video. ([listing](https://github.com/smrht/samautomation-video-mcp))
- [PDF Samenvoegen](https://pdfsamenvoegen.nl/): Merge your own PDFs in a confirmed order and get one downloadable PDF. ([listing](https://github.com/smrht/pdfsamenvoegen-mcp))
- [Nummerschilderen.com shop advisor](https://nummerschilderen.com/): Search paint-by-number kits, get size and price advice for your own photo, shop info. No login. ([listing](https://github.com/smrht/nummerschilderen-mcp))
- [DiamondPaintingWinkel.nl shop advisor](https://diamondpaintingwinkel.nl/): Search diamond painting kits, get size and price advice for your own photo, shop info. No login. ([listing](https://github.com/smrht/diamondpaintingwinkel-mcp))
- [AI Rechtshulp](https://ai-rechtshulp.nl/): Search Dutch and EU case law with ECLI sources and verify quotes against the judgment. ([listing](https://github.com/smrht/ai-rechtshulp-mcp))
- [SamDesk Support](https://samdesk.nl/support/plugin/): Read your SamDesk support inbox, find customer agreements and draft replies. Read-only. ([listing](https://github.com/smrht/samdesk-support-mcp))

## Publisher

Samautomation, Wognum, the Netherlands · https://samautomation.work

This repository holds the public listing (README, `server.json`, install notes). The server itself is hosted by the publisher; there is nothing to install or build.
