# GitHub Pages Setup Guide

Publish your markdown knowledge repository as a searchable website on GitHub Pages. Automatic deployment on every push to main.

---

## What You Get

✅ Beautiful, searchable website  
✅ Auto-deploys when you push to GitHub  
✅ Dark/light theme toggle  
✅ Mobile-responsive  
✅ Full-text search  
✅ Navigation tabs and sidebar  
✅ Code syntax highlighting  

Live at: `https://github.com/YOUR-USERNAME/personal-knowledge-repo/pages` → `https://github.com/pages/YOUR-USERNAME/personal-knowledge-repo/`

---

## Step 1: Copy Files into Your Repo

Copy these files to your repo root:

```bash
cd ~/path/to/personal-knowledge-repo

# Copy config
cp mkdocs.yml .
cp requirements.txt .

# Create GitHub Actions directory
mkdir -p .github/workflows

# Copy workflow
cp deploy.yml .github/workflows/deploy.yml
```

---

## Step 2: Reorganize Your Markdown Files

Move your markdown files into a `docs/` folder:

```bash
mkdir -p docs

# Move content
mv 01-technical-learnings docs/technical-learnings
mv 02-reference-material docs/reference
mv 03-meeting-notes docs/meeting-notes
mv 04-projects docs/projects
mv README.md docs/index.md

# Create section index files
touch docs/technical-learnings/index.md
touch docs/reference/index.md
touch docs/meeting-notes/index.md
touch docs/projects/index.md
```

---

## Step 3: Create Section Index Files

These help organize content. Create simple index files in each section:

### `docs/technical-learnings/index.md`
```markdown
# Technical Learnings

Deep-dive guides, tutorials, and how-tos on technical topics.

## Programming
- [Python Async Patterns](programming/python-async.md)

## Tools & Frameworks
- [Kafka Consumers](tools-frameworks/kafka.md)

## DevOps & Infrastructure
- [Docker Best Practices](devops-infra/docker.md)

## Debugging Notes
- [Debugging Guide](debugging/guide.md)
```

### `docs/reference/index.md`
```markdown
# Reference Material

Quick lookups, APIs, commands, and checklists.

## APIs
- [Slack API](apis/slack.md)

## Commands
- [Docker Cheatsheet](commands/docker.md)

## Templates
- [PR Template](templates/pr-template.md)

## Checklists
- [Deployment Checklist](checklists/deployment.md)
```

Do the same for `docs/meeting-notes/index.md` and `docs/projects/index.md`.

---

## Step 4: Create About Page

Create `docs/about.md`:

```markdown
# About This Knowledge Base

Personal knowledge repository for technical learnings, meeting notes, and project tracking.

**Author:** Miguel Gomes  
**Email:** miguel.gomes2@fanduel.com  
**Last Updated:** 2026-08-20

## How to Use This Site

- **Search** the full-text search bar at the top
- **Navigate** using the sidebar for categories
- **Toggle** dark/light mode in the top right
- **Edit** on GitHub by clicking the edit icon on any page

## Contributing

Have feedback or want to add content? Edit the markdown files in the `docs/` folder and push to `main` — the site redeploys automatically.

See [SETUP-GUIDE.md](https://github.com/fanduel/personal-knowledge-repo/blob/main/SETUP-GUIDE.md) for how to add new notes.
```

---

## Step 5: Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under "Build and deployment":
   - **Source:** Select `GitHub Actions`
   - Leave the rest as default
4. Click **Save**

---

## Step 6: Commit and Push

```bash
git add .
git commit -m "feat: Set up GitHub Pages with mkdocs

- Add mkdocs configuration with Material theme
- Add GitHub Actions workflow for auto-deployment
- Reorganize markdown files into docs/ folder
- Add section index files and about page
- Site will auto-deploy to GitHub Pages on push"
git push origin main
```

---

## Step 7: Watch It Deploy

1. Go to your repo → **Actions** tab
2. You should see a "Deploy to GitHub Pages" workflow running
3. Wait for it to complete (usually 1-2 minutes)
4. Once green, your site is live!

Your site will be at:
```
https://github.com/pages/YOUR-USERNAME/personal-knowledge-repo/
```

Or if your repo is public:
```
https://YOUR-USERNAME.github.io/personal-knowledge-repo/
```

---

## Daily Workflow

### Add a new technical guide:
```bash
# Create file
touch docs/technical-learnings/python-async.md

# Edit
code docs/technical-learnings/python-async.md

# Update docs/technical-learnings/index.md with a link

# Commit and push
git add .
git commit -m "add: Python async patterns guide"
git push
```

### Update meeting notes:
```bash
# Create/edit file
code docs/meeting-notes/2026-08-20-sprint-planning.md

# Update docs/meeting-notes/index.md

# Commit and push
git add .
git commit -m "add: Sprint planning notes - 2026-08-20"
git push
```

That's it! The site automatically redeploys in ~1 minute.

---

## Local Preview (Optional)

Preview your site locally before pushing:

```bash
# Install dependencies (one time)
pip install -r requirements.txt

# Run dev server
mkdocs serve

# Visit http://localhost:8000 in your browser
# Changes auto-refresh as you edit
```

---

## Troubleshooting

### "Pages deployment failed"
Check the GitHub Actions logs:
1. Go to **Actions** tab
2. Click the failed workflow
3. Expand "Deploy site" step to see the error
4. Common issues:
   - Missing `docs/` folder
   - Typo in `mkdocs.yml`
   - Missing index.md files

### "Site not showing content"
Make sure you have:
- `docs/` folder with your markdown files
- `docs/index.md` (the home page)
- Section index files (e.g., `docs/technical-learnings/index.md`)

### "Search not working"
The Material theme search needs indexing. Give it a minute after deployment.

### "Can't find my page"
Check that:
1. File is in `docs/` folder
2. Path in mkdocs.yml nav matches your file structure
3. File has a top-level `# Heading`

---

## Customization

### Change the site name
Edit `mkdocs.yml`:
```yaml
site_name: My Knowledge Base
site_description: My personal notes
```

### Change colors
Edit the `theme.palette` section in `mkdocs.yml`:
```yaml
primary: blue    # Change to: red, green, pink, etc.
accent: cyan     # Change to: lime, orange, purple, etc.
```

### Add more navigation sections
Edit the `nav` section in `mkdocs.yml`:
```yaml
nav:
  - Home: index.md
  - New Section: new-section/index.md
  - Subsection: new-section/subsection.md
```

### Add plugins
Add to `mkdocs.yml`:
```yaml
plugins:
  - search
  - social
  - tags
```

See [Material theme docs](https://squidfunk.github.io/mkdocs-material/) for more options.

---

## Next Steps

1. ✅ Copy configuration files
2. ✅ Reorganize into `docs/` folder
3. ✅ Enable GitHub Pages in settings
4. ✅ Push to GitHub
5. ✅ Wait for deployment
6. 🚀 Share your knowledge base!

---

## Resources

- [MkDocs Docs](https://www.mkdocs.org/)
- [Material Theme](https://squidfunk.github.io/mkdocs-material/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)

---

Happy publishing! 📚
