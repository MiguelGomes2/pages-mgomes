# Personal Knowledge Repository

A personal knowledge base for technical learnings, how-to guides, meeting notes, and project tracking. Built with markdown for simplicity, portability, and version control via Git

**Navigation:** [Automatic-KS](/pages-mgomes/automaticks/) • [Price Confidence](/pages-mgomes/price-confidence/) • [Meeting Notes](/pages-mgomes/meeting-notes/) • [Liability Engine](/pages-mgomes/liabilityengine/)

---

## 📚 Repository Structure

```
docs/
├── index.md                     # This file
├── about.md                     # About page
│
├── /price-confidence/           # Price Confidence reference and checklists
│   ├── index.md
│   ├── apis/
│   ├── commands/
│   ├── templates/
│   └── checklists/
│
├── /liabilityengine/            # Liability Engine tracking and progress
│   ├── index.md
│   └── tracking/
│
└── /meeting-notes/              # Meeting notes organized by date
    └── YYYY-MM/
```

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

- [Price Confidence](price-confidence/index.md) - Reference material
- [Liability Engine](liabilityengine/index.md) - Current work
- [Meeting Notes](meeting-notes/index.md) - Recent notes

---

Happy learning! 📚
