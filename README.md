# Bindly for Claude Code

**Complete your thoughts. Make them reusable.**

Bindly is a knowledge completion layer for Claude Code. It helps you finish your thinking and save it in a way that's accessible across sessions and agents.

---

## What Bindly Is (and Isn't)

Bindly is **not** auto-memory. It doesn't silently log your conversations.

Instead, Bindly helps you:
- **Form** your thoughts into reusable knowledge
- **Refine** your understanding over time with version control
- **Organize** ideas into project-specific collections
- **Access** the same knowledge from any connected agent

> "Bindly is about completing knowledge, not auto-logging conversations."

---

## How It Works

When you install this plugin:

1. **MCP Tools** become available automatically
   - Search your knowledge base
   - Create and update bindings
   - Organize into Sets
   - Share with others

2. **Skills** guide your workflow
   - `/bindly:save` — Complete and save your current thinking
   - `/bindly:search` — Find knowledge you've stored
   - `/bindly:organize` — Group knowledge into Sets

---

## Where Your Data Lives

When you connect via OAuth, your knowledge is stored in your **Bindly account at [bindly.app](https://bindly.app)** — not inside Claude Code.

This means:
- **Persistent**: Survives across sessions and reinstalls
- **Portable**: Access from ChatGPT, Claude Web, IDE agents, or any MCP client
- **Yours**: You control your knowledge, not any single chat app

---

## Quick Start

### 1. Add the Marketplace

```bash
/plugin marketplace add seongjaeryu/bindly-claude-code
```

### 2. Install the Plugin

```bash
/plugin install bindly@bindly-claude-code
```

### 3. Authenticate

```bash
/mcp
```

Select Bindly and complete OAuth authentication.

### 4. Start Using

```bash
# Save something you've learned
/bindly:save

# Search your knowledge base
/bindly:search

# Organize into collections
/bindly:organize
```

---

## Example Workflows

### Research Assistant

```
You: "I've been debugging this auth issue for an hour. Save what I learned."

Claude: [Searches for existing auth knowledge]
        "I found 2 related bindings. Should I update 'OAuth Token Handling'
        or create a new binding?"

You: "Update the existing one with the new edge case."

Claude: [Creates new version with your findings]
        "Saved to your Bindly account. This is now version 3 of
        'OAuth Token Handling'."
```

### Cross-Agent Knowledge

```
# In Claude Code
You: "Save my API design decisions for this project."
Claude: [Saves to Bindly]

# Later, in ChatGPT with Bindly connected
You: "What were my API design decisions?"
ChatGPT: [Retrieves from Bindly] "Here are your 5 key decisions..."
```

---

## Available MCP Tools

When the plugin is installed, these tools are automatically available:

| Tool | Purpose |
|------|---------|
| `mcp_search` | Semantic search across your knowledge |
| `mcp_get_binding` | Retrieve a specific binding |
| `mcp_list_bindings` | List bindings in a Space |
| `request_create_binding` | Save new knowledge |
| `request_update_binding` | Create new version of existing knowledge |
| `mcp_list_sets` | View your curated collections |
| `request_create_set` | Create a new collection |
| `request_add_version_to_set` | Add knowledge to a collection |
| `request_create_binding_share` | Create a public share link |

---

## Core Concepts

| Concept | Description |
|---------|-------------|
| **Binding** | A piece of knowledge (article, note, insight) |
| **Version** | An immutable snapshot — edits create new versions |
| **Set** | A curated collection of versions |
| **Space** | Your knowledge workspace |

---

## Links

- **Website**: [https://bind.ly](https://bind.ly)
- **Documentation**: [https://bindly.app/docs](https://bindly.app/docs)
- **Main Repository**: [bindly-new](https://github.com/seongjaeryu/bindly-new)

---

## License

MIT License — see [LICENSE](LICENSE)
