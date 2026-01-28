# Setup Guide

This guide covers how to install and configure the Bindly plugin for Claude Code.

---

## Prerequisites

- Claude Code installed and running
- A Bindly account at [bindly.app](https://bindly.app)

---

## Installation

### Step 1: Add the Marketplace

```bash
/plugin marketplace add seongjaeryu/bindly-claude-code
```

This registers the Bindly marketplace with Claude Code.

### Step 2: Install the Plugin

```bash
/plugin install bindly@seongjaeryu-bindly-claude-code
```

This installs the Bindly plugin, which includes:
- MCP server configuration
- Three workflow Skills (`save`, `search`, `organize`)

### Step 3: Authenticate with OAuth

Run the MCP command to see connected servers:

```bash
/mcp
```

Select **Bindly** and choose **Authenticate**. This will open your browser for OAuth login.

---

## Understanding Data Storage

### Where is my knowledge stored?

When you authenticate via OAuth, all knowledge is stored in your **Bindly account at bindly.app**.

This is important to understand:

| What it means | Details |
|---------------|---------|
| **Not local** | Data is not stored inside Claude Code or on your machine |
| **Account-based** | Tied to your Bindly account, not your chat session |
| **Persistent** | Survives across sessions, reinstalls, and device changes |
| **Portable** | Accessible from any agent that connects to Bindly |

### Cross-Agent Access

The same knowledge you save from Claude Code can be accessed from:

- **ChatGPT** (with Bindly GPT or MCP connection)
- **Claude Web** (via Bindly MCP)
- **IDE Extensions** (VS Code, JetBrains with MCP support)
- **Any future MCP client**

This is a core design feature, not a side effect.

---

## Configuration Options

### Scopes

When installing, you can choose the scope:

| Scope | Description |
|-------|-------------|
| **User** | Available to you across all projects |
| **Project** | Shared with collaborators on this repository |
| **Local** | Only for you in this repository |

### Manual MCP Configuration

If you prefer manual setup, add this to your MCP configuration:

```json
{
  "mcpServers": {
    "bindly": {
      "type": "http",
      "url": "https://mcp.bind.ly/mcp"
    }
  }
}
```

---

## Troubleshooting

### OAuth authentication fails

1. Check your internet connection
2. Try clearing authentication: `/mcp` → Select Bindly → Clear authentication
3. Re-authenticate

### MCP tools not appearing

1. Verify the plugin is installed: `/plugin`
2. Check the Installed tab for "bindly"
3. Restart Claude Code if needed

### Skills not working

1. Skills are namespaced: use `/bindly:save`, not `/save`
2. Check `/plugin` → Installed tab for skill status

---

## Next Steps

- Try `/bindly:save` to save your first piece of knowledge
- Use `/bindly:search` to find existing knowledge
- Read the [examples](examples/) for workflow ideas

---

## Links

- **Website**: [https://bind.ly](https://bind.ly)
- **Documentation**: [https://bindly.app/docs](https://bindly.app/docs)
- **Support**: support@bind.ly
