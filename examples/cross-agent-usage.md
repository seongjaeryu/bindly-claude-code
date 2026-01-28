# Example: Cross-Agent Knowledge Usage

This example demonstrates how knowledge saved from Claude Code can be accessed from other chat agents and environments.

---

## The Core Idea

When you save knowledge to Bindly, it's stored in your **account at bindly.app**, not inside any specific chat application.

This means the same knowledge is accessible from:
- Claude Code (CLI)
- Claude Web
- ChatGPT (with Bindly connection)
- IDE extensions with MCP support
- Any future MCP client

---

## Scenario

You're working on a project across different environments and tools. You want your knowledge to follow you.

---

## The Workflow

### Step 1: Save from Claude Code

During a coding session in your terminal:

```
You: I figured out how to optimize our GraphQL resolver.
     Save this pattern for future reference.

Claude Code: [Creates binding]
Saved "GraphQL Resolver Optimization Pattern" to your Bindly account.

Key points:
- DataLoader for N+1 prevention
- Field-level caching with TTL
- Lazy resolution for nested objects
```

### Step 2: Access from Claude Web

Later, you're using Claude in the browser for documentation:

```
You: What do I know about GraphQL optimization?

Claude Web: [Searches your Bindly account]
Found "GraphQL Resolver Optimization Pattern" from 2 days ago.

Key points:
- DataLoader for N+1 prevention
- Field-level caching with TTL
- Lazy resolution for nested objects

Would you like the full details?
```

### Step 3: Extend from ChatGPT

Working with a team member who uses ChatGPT:

```
You: Search my Bindly for GraphQL patterns.

ChatGPT: [Via Bindly MCP connection]
Found your binding on GraphQL Resolver Optimization.

Your team member: Can you add our new batching insight to that?

ChatGPT: [Updates the binding]
Added "Request batching with maxBatchSize: 100" as a new version.
```

### Step 4: Review Changes from Claude Code

Back in your terminal:

```
You: What changed in my GraphQL optimization notes?

Claude Code: [Checks version history]
"GraphQL Resolver Optimization Pattern" has 2 versions:

Version 1 (you, 2 days ago):
- Original 3 key points

Version 2 (via ChatGPT, today):
- Added: Request batching with maxBatchSize

Want to see the diff?
```

---

## Why This Matters

### Context Continuity

Your thinking doesn't reset when you switch tools. Knowledge built in Claude Code is immediately available in Claude Web or ChatGPT.

### Team Collaboration

Team members using different tools can contribute to the same knowledge base:

```
Team Structure:
├── Alice (Claude Code) → Saves architecture decisions
├── Bob (ChatGPT) → Adds implementation notes
└── Carol (Claude Web) → Reviews and organizes into Sets
```

### Tool Independence

You're not locked into any single AI provider. Your knowledge is:
- Stored independently at bindly.app
- Accessible via standard MCP protocol
- Portable if you switch tools

---

## Practical Patterns

### Morning Research, Afternoon Coding

```
Morning (Claude Web):
- Research authentication patterns
- Save findings to Bindly

Afternoon (Claude Code):
- "What did I find about auth patterns this morning?"
- Implement based on your saved knowledge
```

### Mobile to Desktop

```
On Phone (ChatGPT):
- Quick idea or insight
- Save to Bindly

At Desk (Claude Code):
- "What was that idea I had earlier?"
- Expand and implement
```

### Multi-Project Context

```
Project A (Claude Code):
- Save debugging insights

Project B (different repo, Claude Code):
- "Search my debugging patterns"
- Apply learnings across projects
```

---

## Key Takeaways

1. **One knowledge base, many interfaces** — Bindly is the source of truth
2. **Agent-agnostic** — Not tied to Claude, ChatGPT, or any specific tool
3. **Real-time sync** — Changes from one agent appear in others immediately
4. **Version history** — See who added what, from where
5. **Designed feature** — This portability is intentional, not incidental
