# Example: Project Knowledge Base

This example shows how to build and maintain a project-specific knowledge base using Bindly Sets.

---

## Scenario

You're starting a new project and want to create a dedicated knowledge space for all project-related decisions, learnings, and documentation.

---

## The Workflow

### 1. Create a Project Set

```
You: Create a Set for my new authentication service project.

Claude: I'll create a Set for your project. Let me check your existing Sets first...

No existing Sets match "authentication service".

Creating Set: "Auth Service Project"
Description: Knowledge base for the authentication service development

Set created in your Bindly account. Ready to add knowledge.
```

### 2. Add Knowledge as You Work

#### Day 1: Architecture Decision

```
You: Save my decision to use JWT instead of sessions for this project.

Claude: [Searches existing knowledge]
No existing bindings about this decision.

Creating new binding:
- Title: "Auth Service: JWT vs Sessions Decision"
- Key points:
  - Chose JWT for stateless scaling
  - Trade-off: Larger request payload
  - Mitigation: Short expiry with refresh tokens

Saved and added to "Auth Service Project" Set.
```

#### Day 3: Implementation Learning

```
You: Save what I learned about bcrypt cost factors.

Claude: [Searches]
Found related: "Password Hashing Best Practices" (general knowledge)

Should I:
1. Update the general binding with project-specific notes?
2. Create a new project-specific binding?
3. Just add the general binding to this project's Set?

You: Create a new project-specific one.

Claude: Creating: "Auth Service: Bcrypt Configuration"
- Cost factor: 12 for production
- Rationale: Balance between security and response time
- Testing showed: ~250ms hash time

Added to "Auth Service Project" Set.
```

### 3. Review Your Project Knowledge

```
You: What's in my Auth Service Project Set?

Claude: "Auth Service Project" contains 5 bindings:

1. JWT vs Sessions Decision (v1) - Day 1
2. Bcrypt Configuration (v2) - Day 3, updated Day 5
3. API Rate Limiting Strategy (v1) - Day 4
4. Token Refresh Flow (v1) - Day 6
5. Security Audit Checklist (v1) - Day 7

Want me to summarize any of these?
```

### 4. Share with Team

```
You: Share this Set with my team for the design review.

Claude: Creating a public share link for "Auth Service Project"...

Share link: https://bind.ly/s/abc123
Expires in: 7 days

Anyone with this link can view the Set and its contents.
Share this with your team for the design review.
```

---

## Set Organization Patterns

### By Project

```
Sets:
├── Auth Service Project
├── Payment Integration
└── Mobile App v2
```

### By Topic

```
Sets:
├── React Patterns
├── Database Optimization
└── Security Practices
```

### By Phase

```
Sets:
├── Q1 2024 Research
├── Q2 2024 Implementation
└── Q3 2024 Optimization
```

---

## Key Takeaways

1. **Sets group related knowledge** — Keep project context together
2. **Add as you work** — Build knowledge incrementally
3. **Review periodically** — See what you've accumulated
4. **Share when needed** — Collaborate with time-limited links
5. **Cross-agent access** — Same Set visible from any connected agent
