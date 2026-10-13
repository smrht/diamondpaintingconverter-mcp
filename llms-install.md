# Installing Diamond Painting Converter in Cline

This is a hosted remote MCP server. There is nothing to clone, build or install.

Add this entry to `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "diamondpaintingconverter": {
      "type": "streamableHttp",
      "url": "https://diamondpaintingconverter.com/mcp",
      "disabled": false
    }
  }
}
```

Authentication: OAuth with PKCE (S256), dynamic client registration and client ID metadata documents, so MCP clients connect without manual setup. Sign in with your diamondpaintingconverter.com account.

With OAuth, Cline opens the sign-in page the first time a tool is used; approve access and return to Cline.

Check the connection by asking: "Which diamond painting patterns do I have?"
