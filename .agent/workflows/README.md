# Antigravity Workflows Guide

This directory contains your **specialized agent workflows**. Each `.md` file here becomes a callable command.

---

## How to Create a Workflow

### 1. Create a new file
Create a file named `your-command.md` in this folder.

**Example:** `engagement-replies.md` → Invoke with `/engagement-replies`

---

### 2. File Structure

Every workflow follows this format:

```markdown
---
description: Short description of what this agent does
---

## Context
[Optional] Background information the agent should know.

## Steps
1. First step to execute
2. Second step to execute
3. Continue as needed...

## Output Format
[Optional] How the agent should format its response.
```

---

## Example Workflow

**File:** `seo-optimize.md`

```markdown
---
description: Generate SEO-optimized descriptions and hashtags for social media posts
---

## Context
I manage faceless content accounts across TikTok, YouTube Shorts, and Instagram Reels.
My niches include: Finance, Health, Motivation, Beauty, DIY, and EdTech.

## Steps
1. Take the video topic and target niche as input
2. Research trending hashtags in that niche
3. Generate an optimized title (under 100 characters)
4. Write a hook-driven description with keywords
5. Provide 10-15 hashtags (mix of high-volume and niche-specific)

## Output Format
- **Title:** [optimized title]
- **Description:** [2-3 sentences with keywords]
- **Hashtags:** #tag1 #tag2 #tag3...
```

---

## Tips for Effective Workflows

| Tip | Why It Matters |
|-----|----------------|
| **Be specific** | Vague instructions = vague results |
| **Include examples** | Show the agent what good output looks like |
| **Define constraints** | Character limits, tone, format requirements |
| **Add context** | Reference your niche, brand voice, or target audience |

---

## Auto-Run Commands

Add special annotations to auto-approve certain commands:

- `// turbo` above a step → Auto-run **that step only**
- `// turbo-all` anywhere → Auto-run **all command steps**

**Example:**
```markdown
## Steps
1. Analyze the input file
// turbo
2. Create a backup copy
3. Apply transformations
```

---

## Quick Reference

| Action | How |
|--------|-----|
| Create workflow | Add `name.md` to this folder |
| Invoke workflow | Type `/name` in chat |
| Edit workflow | Modify the `.md` file directly |
| Delete workflow | Remove the `.md` file |

---

Ready to build your first agent? Create a new `.md` file in this directory!
