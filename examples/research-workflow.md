# Example: Research Workflow

This example demonstrates how to use Bindly for intentional knowledge saving during research and development.

---

## Scenario

You're debugging a complex authentication issue and have spent an hour figuring out the solution. Now you want to save what you learned for future reference.

---

## The Workflow

### 1. Trigger the Save Skill

```
You: Save what I learned about this OAuth token refresh issue.
```

### 2. Claude Searches First

Before creating new knowledge, Claude searches your existing Bindly knowledge base:

```
Claude: I found 2 related bindings in your knowledge base:

1. "OAuth Token Handling" (version 2, updated 3 days ago)
   - Key points: Token expiry, refresh flow, error codes

2. "API Authentication Patterns" (version 1, created 2 weeks ago)
   - Key points: Bearer tokens, session management

Should I:
- Update "OAuth Token Handling" with this new edge case?
- Create a new binding for this specific issue?
```

### 3. You Decide Intentionally

```
You: Update the existing one. This is the same topic, just a new edge case.
```

### 4. Claude Helps Formulate

```
Claude: Great. Let me help you formulate this addition:

Title: OAuth Token Handling (updating)

New content to add:
- Edge case: Token refresh during concurrent requests
- Solution: Implement request queuing with mutex lock
- Key insight: Race condition occurs when multiple API calls...

Key points I'll add:
- Concurrent request handling
- Mutex-based queuing pattern
- Race condition prevention

Does this capture what you learned?
```

### 5. Confirm and Save

```
You: Yes, save it.

Claude: Saved as version 3 of "OAuth Token Handling".
This is stored in your Bindly account at bindly.app and can be
accessed from other connected agents.
```

---

## Why This Matters

### Intentional vs Automatic

Notice how the workflow is **intentional**:

- You decide when to save
- You choose whether to update or create new
- You confirm the formulation

This is different from auto-logging tools that capture everything without thought.

### Knowledge Evolution

By updating the existing binding:

- Version history is preserved
- Related knowledge stays connected
- You can use `mcp_get_diff` to see what changed

### Cross-Agent Value

Later, in a different context:

```
# In ChatGPT with Bindly connected
You: What do I know about OAuth token handling?

ChatGPT: Based on your Bindly knowledge, you have "OAuth Token Handling"
with 3 versions. The latest includes handling concurrent requests
with a mutex-based queuing pattern...
```

---

## Key Takeaways

1. **Search first** — Avoid duplicating knowledge
2. **Update or create** — Make a conscious choice
3. **Formulate clearly** — Knowledge is formed, not just captured
4. **Confirm storage** — Understand where your data lives
