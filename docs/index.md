# Personal Knowledge Repository

A personal knowledge base for technical learnings, how-to guides, meeting notes, and project tracking. Built with markdown for simplicity, portability, and version control via Git

**Navigation:** [Automatic-KS](/pages-mgomes/automatic-ks/) • [Technical Learnings](/pages-mgomes/technical-learnings/) • [Reference](/pages-mgomes/reference/) • [Meeting Notes](/pages-mgomes/meeting-notes/) • [Projects](/pages-mgomes/projects/)

---

## 📚 Repository Structure

```
personal-repo/
├── README.md                    # This file
├── .gitignore                   # Git ignore patterns
├── INDEX.md                     # Master index and quick links
│
├── /01-technical-learnings/     # Technical guides and how-tos
│   ├── programming/
│   ├── tools-and-frameworks/
│   ├── devops-and-infrastructure/
│   └── debugging-notes/
│
├── /02-reference-material/      # Quick reference and checklists
│   ├── apis/
│   ├── commands/
│   ├── templates/
│   └── checklists/
│
├── /03-meeting-notes/           # Meeting notes and decisions
│   ├── 2026-08/
│   ├── 2026-09/
│   └── decisions-log.md
│
├── /04-projects/                # Project tracking and progress
│   ├── project-a/
│   ├── project-b/
│   └── projects-overview.md
│
└── /templates/                  # Template files (for reference)
    ├── TECHNICAL-GUIDE.md
    ├── MEETING-NOTE.md
    ├── REFERENCE.md
    └── PROJECT-LOG.md
```

---

## 🚀 Quick Start

### 1. Initialize the Repository Locally
```bash
# Clone or create the repo
git clone <your-repo-url> personal-repo
cd personal-repo

# Create the directory structure
mkdir -p 01-technical-learnings/{programming,tools-and-frameworks,devops-and-infrastructure,debugging-notes}
mkdir -p 02-reference-material/{apis,commands,templates,checklists}
mkdir -p 03-meeting-notes/{2026-08,2026-09}
mkdir -p 04-projects
mkdir -p templates
```

### 2. Add Content
Start by copying the templates from `/templates` into the relevant directories and filling them in.

### 3. Keep INDEX.md Updated
Whenever you add new notes, update `INDEX.md` with a link for quick navigation.

### 4. Commit and Push
```bash
git add .
git commit -m "Add new notes on [topic]"
git push origin main
```

---

## 📖 How to Use Each Section

### 📚 01-Technical-Learnings/
For deep-dive guides, tutorials, and how-tos on technical topics.

**Examples:**
- `programming/python-async.md` - Async/await patterns
- `tools-and-frameworks/react-patterns.md` - React best practices
- `debugging-notes/kafka-consumer-lag.md` - Solutions to common issues

**Template:** See `templates/TECHNICAL-GUIDE.md`

---

### 🔍 02-Reference-Material/
Quick lookups, API docs, commands, templates, and checklists.

**Examples:**
- `apis/slack-api-endpoints.md` - Slack API reference
- `commands/docker-cheatsheet.md` - Useful Docker commands
- `templates/pr-checklist.md` - PR review template
- `checklists/deployment-checklist.md` - Pre-deployment steps

**Template:** See `templates/REFERENCE.md`

---

### 📝 03-Meeting-Notes/
Meeting notes, decisions, and action items organized by date.

**File naming:** `YYYY-MM-DD-topic-slug.md`

**Examples:**
- `2026-08/2026-08-20-price-confidence-review.md`
- `2026-08/2026-08-15-sprint-planning.md`

**decisions-log.md:** Running log of decisions made. Update whenever an important decision is documented.

**Template:** See `templates/MEETING-NOTE.md`

---

### 🎯 04-Projects/
Active projects, their progress, and status. One folder per project.

**File structure per project:**
```
project-name/
├── README.md              # Project overview
├── progress.md            # Current status and next steps
├── decisions.md           # Project-specific decisions
├── blockers.md            # Current blockers and resolutions
└── learnings.md           # Lessons learned as you go
```

**projects-overview.md:** Summary of all active projects.

**Template:** See `templates/PROJECT-LOG.md`

---

## ✅ Best Practices

1. **Use clear file names** - Include dates for time-sensitive content (meeting notes), use slug-style names (lowercase, hyphens).

2. **Link to related notes** - Use relative links to connect related content:
   ```markdown
   [See also: Python async guide](../01-technical-learnings/programming/python-async.md)
   ```

3. **Keep INDEX.md current** - Maintain a master index at the root for quick navigation.

4. **One idea per file** - Keep files focused; link to related files rather than bundling everything.

5. **Use frontmatter for metadata** (optional):
   ```markdown
   ---
   title: Python Async Patterns
   date: 2026-08-20
   tags: [python, async, concurrency]
   status: draft
   ---
   ```

6. **Organize chronologically where it matters** - Meeting notes and project progress should be time-stamped.

7. **Review and update regularly** - Review old notes quarterly; remove outdated info or mark as archived.

8. **Search-friendly writing** - Use clear headers, bold key terms, include aliases for searchability.

---

## 🔄 Maintenance Schedule

- **Weekly:** Add meeting notes and quick learnings
- **Bi-weekly:** Update project progress logs
- **Monthly:** Review and reorganize; update INDEX.md
- **Quarterly:** Archive old meeting notes; consolidate learnings into refined guides

---

## 📱 Viewing in GitHub

- README files in each folder show up automatically on GitHub
- Use the GitHub interface to browse or search
- Clone locally for offline access and Git history

---

## 🛠 Tools to Enhance Your Repository

### Optional Integrations
- **Obsidian:** Local editor with excellent markdown support and link visualization
- **VS Code:** Native Git support, markdown preview, search across files
- **GitHub CLI:** Manage commits and syncs from terminal
- **GitHub Actions:** Auto-generate a searchable index or deploy as a website

### Deploy as a Website (Optional)
If you want a public-facing version:
- **GitHub Pages + mkdocs:** Auto-generate a searchable site from markdown
- **Notion:** Copy content to Notion for collaborative sharing
- **Quartz:** Static site generator designed for knowledge bases

---

## 🔐 Privacy & Organization

- Keep sensitive information in a `.private/` folder (add to .gitignore)
- Use a private GitHub repo if sharing company/sensitive information
- For public repos, avoid storing credentials, API keys, or personal data

---

## 📞 Quick Links

- [INDEX.md](INDEX.md) - Master navigation
- [Templates](templates/) - Content templates
- [Latest Meeting Notes](03-meeting-notes/2026-08/) - Recent notes
- [Active Projects](04-projects/projects-overview.md) - Current work

---

Happy learning! 📚
