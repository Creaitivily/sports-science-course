# Tech Stack

The essential toolkit for Person B.

---

## Core Operations

| Category | Tool | Purpose |
|----------|------|---------|
| **Project Management** | Notion or ClickUp | Central hub for scripts, calendars, and tasks |
| **Automation** | Make (formerly Integromat) | Connect apps (e.g., "video upload → create editor task") |
| **Scripting/Ideation** | ChatGPT / Claude | Brainstorming hooks and formatting scripts |
| **Scheduling** | Metricool / Buffer | Multi-platform posting |
| **Communication** | Slack / Discord | Keep business chat separate from personal messages |

---

## File Management

| Component | Recommendation | Why? |
|-----------|----------------|------|
| **Cloud Storage** | Google Drive (Business) or Dropbox | Reliable "Desktop Sync" apps. Dropbox is faster for large video files. |
| **Large Transfer** | MASV (Optional) | For slow internet + huge files (50GB+). Costs per GB. |
| **Automation** | Make.com | Cheaper and more flexible than Zapier for file watching |
| **Physical Storage** | SanDisk Extreme Pro SSD | Fast transfers and local editing |

---

## Recommended Automations

### 1. New Footage Alert
```
Trigger: New file in "INBOX" folder (>50MB)
Action: Send Slack message to #production-alerts
Message: "🚨 New Footage Detected! [Filename] uploaded by Person A."
```

### 2. Content Calendar Reminder
```
Trigger: 48 hours before scheduled post
Action: Send reminder to Person B
Message: "📅 Content due for review: [Video Title]"
```

### 3. Performance Report
```
Trigger: Every Monday 9am
Action: Pull analytics from YouTube/IG APIs
Message: Weekly performance summary to Notion
```
