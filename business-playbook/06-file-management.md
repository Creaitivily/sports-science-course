# File Management Protocol

A system where Person A drags files into a "Magic Folder" and walks away, while Person B receives notifications and organized assets automatically.

---

## The Folder Structure

Set up once by Person B. Person A only fills them.

```
📂 [COMPANY NAME] MASTER
 ├── 📂 01_INBOX_UPLOAD_HERE (The "Magic Folder")
 ├── 📂 02_PROJECTS
 │    ├── 📂 2024-01-24_Batch_Shoot
 │    │    ├── 📂 A_Roll (Main footage)
 │    │    ├── 📂 B_Roll (Extra shots)
 │    │    └── 📂 Audio
 ├── 📂 03_ASSETS (Logos, Music, Fonts)
 └── 📂 04_FINAL_EXPORTS (Ready to post)
```

> **The Rule:** Person A **only** touches `01_INBOX_UPLOAD_HERE`. Person B moves files to Project folders.

---

## The Workflow

### Step 1: Digital Dump (Person A)

After filming:
1. Connect SD Card to computer
2. Open `01_INBOX_UPLOAD_HERE` folder
3. Create new sub-folder with today's date (e.g., `2024-01-24_Shoot`)
4. Drag **all** raw footage into that folder
5. Leave computer on for syncing (overnight if needed)

### Step 2: Bat-Signal Automation (Person B)

Set up in Make.com:
- **Trigger:** Watch for new files in `01_INBOX_UPLOAD_HERE`
- **Filter:** File size > 50MB
- **Action:** Send Slack message to `#production-alerts`
- **Message:** `🚨 New Footage Detected! [File Name] uploaded. Ready for review.`

### Step 3: Organization (Person B)

Upon notification:
1. **Verify** files (audio present, video not corrupt)
2. **Move** folder from `01_INBOX` to `02_PROJECTS` → `[Date]_Batch_Shoot`
3. **Signal** Person A: "All Clear" emoji (they can format SD card now)

---

## Fail-Safe Protocols

### The SD Card Rule (Person A)

> ⚠️ **Never format the SD card until Person B gives the "All Clear" emoji.**

Until that signal, footage exists only in the cloud (still uploading) and on the card. The card is the physical backup.

### The 3-2-1 Backup Rule (Person B)

| Copy | Location | Type |
|------|----------|------|
| **1** | Cloud (Google Drive/Dropbox) | Working files |
| **2** | Physical SSD on Person B's desk | Local backup |
| **3** | Amazon S3 / Backblaze | Cold storage |
