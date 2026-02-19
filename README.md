# Particl Claude Plugins

Official [Claude.ai](https://claude.ai) plugins for [Particl](https://particl.com) — e-commerce market research and competitor intelligence.

## Plugins

### [Particl Market Research](plugins/particl-market-research/)

Access Particl's e-commerce intelligence directly in Claude. Search companies, analyze product catalogs, discover top sellers, and get pricing insights across thousands of tracked brands.

**Features:**
- Search and discover e-commerce companies
- Analyze product catalogs with filtering, sorting, and pagination
- Get market-level intelligence: top companies, top products, pricing analysis
- Credit-aware — check balance and estimate costs before large queries

## Installation

### Claude.ai
1. Go to Claude.ai Settings
2. Add this marketplace from GitHub: `particlhq/claude-plugins`
3. Install the "Particl Market Research" plugin
4. Sign in with your Particl account when prompted

### Claude Code (CLI)
Add to your project's `.mcp.json`:
```json
{
  "mcpServers": {
    "particl": {
      "type": "http",
      "url": "https://particl-mcp.onrender.com/mcp"
    }
  }
}
```

### ChatGPT
See [ChatGPT MCP Connector setup guide](https://github.com/particlhq/particl-api/blob/main/mcp/docs/chatgpt-setup.md).

## Authentication

Plugins use OAuth to connect to your Particl account via Clerk. Your existing Particl export credits are used for MCP queries.

## License

[MIT](LICENSE)
