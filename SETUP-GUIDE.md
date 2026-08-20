# Setup Guide: Personal Knowledge Repository

Get your personal knowledge repository up and running in 5 minutes.

---

## Step 1: Create GitHub Repository

1. Go to [GitHub.com](https://github.com) and log in
2. Click **New repository**
3. Set repository name: `personal-knowledge-repo` (or your preferred name)
4. Choose **Private** (recommended) or **Public**
5. Do NOT initialize with README (you'll add your own)
6. Click **Create repository**

---

## Step 2: Clone and Initialize Locally

```bash
# Clone the empty repo
git clone https://github.com/YOUR-USERNAME/personal-knowledge-repo.git
cd personal-knowledge-repo

# Create the directory structure
mkdir -p 01-technical-learnings/{programming,tools-and-frameworks,devops-and-infrastructure,debugging-notes}
mkdir -p 02-reference-material/{apis,commands,templates,checklists}
mkdir -p 03-meeting-notes/{2026-08,2026-09}
mkdir -p 04-projects
mkdir -p templates
```

---

## Step 3: Add the Files

Copy these files from the templates provided:

```bash
# Copy the main files to your repo root
cp README.md .
cp INDEX.md .
cp TECHNICAL-GUIDE-TEMPLATE.md templates/
cp MEETING-NOTE-TEMPLATE.md templates/
cp REFERENCE-TEMPLATE.md templates/
cp PROJECT-LOG-TEMPLATE.md templates/
cp .gitignore .
```

---

## Step 4: Initial Commit and Push

```bash
# Add all files
git add .

# Create first commit
git commit -m "Initial commit: personal knowledge repository setup"

# Push to GitHub
git push -u origin main
```

---

## Step 5: Start Adding Content

### Option A: Quick Start (5 minutes)
Create one note in each category to get the feel:

1. **Technical Learning:** Create `01-technical-learnings/programming/python-basics.md`
   ```bash
   cp templates/TECHNICAL-GUIDE-TEMPLATE.md 01-technical-learnings/programming/python-basics.md
   ```

2. **Reference:** Create `02-reference-material/commands/useful-commands.md`
   ```bash
   cp templates/REFERENCE-TEMPLATE.md 02-reference-material/commands/useful-commands.md
   ```

3. **Meeting Note:** Create `03-meeting-notes/2026-08/2026-08-20-kickoff.md`
   ```bash
   cp templates/MEETING-NOTE-TEMPLATE.md 03-meeting-notes/2026-08/2026-08-20-kickoff.md
   ```

4. **Project:** Create `04-projects/project-alpha/README.md`
   ```bash
   cp templates/PROJECT-LOG-TEMPLATE.md 04-projects/project-alpha/progress.md
   ```

### Option B: Start Fresh (As You Go)
Just start taking notes and creating files as needed.

---

## Step 6: Update INDEX.md

Edit `INDEX.md` to add links to your new files.

---

## Step 7: Commit Your First Notes

```bash
# Add your new content
git add .

# Commit
git commit -m "Add initial notes and templates"

# Push
git push
```

---

## Common Workflows

### Adding a New Technical Guide

```bash
# Copy template
cp templates/TECHNICAL-GUIDE-TEMPLATE.md 01-technical-learnings/[category]/[topic].md

# Edit the file
code 01-technical-learnings/[category]/[topic].md

# Add to INDEX.md with a link

# Commit
git add .
git commit -m "Add technical guide: [topic]"
git push
```

### Adding Meeting Notes

```bash
# Copy template
cp templates/MEETING-NOTE-TEMPLATE.md 03-meeting-notes/2026-08/2026-08-20-topic.md

# Edit and fill in details
code 03-meeting-notes/2026-08/2026-08-20-topic.md

# Add to INDEX.md

# Commit
git add .
git commit -m "Add meeting notes: [date] - [topic]"
git push
```

### Adding a New Project

```bash
# Create project directory
mkdir 04-projects/project-name
cd 04-projects/project-name

# Copy templates
cp ../../templates/PROJECT-LOG-TEMPLATE.md progress.md

# Create additional files as needed
touch decisions.md blockers.md learnings.md

# Edit progress.md
code progress.md

# Commit
git add .
git commit -m "Add project: [project-name]"
git push
```

---

## Editing Tips

### Use VS Code
```bash
# Open entire repo
code .

# Open specific file
code 01-technical-learnings/programming/python-basics.md
```

### Use Obsidian (Optional)
For a better markdown editing experience with backlinks and visualization:

1. Download [Obsidian](https://obsidian.md/)
2. Open vault from your repo folder
3. Edit with backlinks and graph view

### Use GitHub Web Editor
1. Go to your repo on GitHub
2. Click `.` (period) on keyboard to open web editor
3. Edit files directly

---

## Daily Workflow

### Add a new note:
```bash
# Create file
touch 01-technical-learnings/category/new-topic.md

# Edit
code 01-technical-learnings/category/new-topic.md

# Update INDEX.md with a link

# Commit and push
git add .
git commit -m "Add notes on [topic]"
git push
```

### Update meeting notes:
```bash
# Edit existing file
code 03-meeting-notes/2026-08/2026-08-20-meeting.md

# Commit
git add .
git commit -m "Update meeting notes: [topic]"
git push
```

### Update project status:
```bash
# Edit progress
code 04-projects/project-name/progress.md

# Commit
git add .
git commit -m "Update progress: [project-name]"
git push
```

---

## Pro Tips

### 1. Keep commits atomic
One idea = one commit. Makes history searchable.

```bash
git commit -m "Add guide: Python async patterns"  # ✅ Good
git commit -m "Various updates"                    # ❌ Vague
```

### 2. Use consistent date format
Dates in filenames: `YYYY-MM-DD`
```
2026-08-20-meeting-notes.md  # ✅ Searchable, sorts chronologically
august-20-notes.md           # ❌ Hard to sort
```

### 3. Link liberally
Use relative links to connect related notes:
```markdown
[See also: Python async guide](../01-technical-learnings/programming/python-async.md)
```

### 4. Keep INDEX.md updated
Your INDEX.md is your navigation hub. Add every new note you create.

### 5. Review quarterly
- Consolidate learnings into refined guides
- Move old meeting notes to archive
- Update project status

---

## Backup & Sync

### Automatic Backups
Since you're using GitHub, your repo is automatically backed up.

### Multiple Machines
```bash
# On new machine, clone your repo
git clone https://github.com/YOUR-USERNAME/personal-knowledge-repo.git

# Before closing work on any machine
git push
```

---

## Troubleshooting

### "fatal: could not read Username"
You need to set up Git credentials. Use personal access tokens:

```bash
git config --global user.email "miguel.gomes2@fanduel.com"
git config --global user.name "Miguel Gomes"
```

### "Nothing added to commit"
Make sure you've created files:
```bash
git status  # See what's tracked
git add .   # Stage all changes
```

### Changes not showing up on GitHub
Make sure you pushed:
```bash
git push    # Sends your commits to GitHub
```

---

## Next Steps

1. ✅ Create repo on GitHub
2. ✅ Clone locally
3. ✅ Set up directory structure
4. ✅ Add initial files
5. ✅ Create first notes
6. 🚀 Start using it daily!

**Ready to go?** See [README.md](README.md) for complete documentation.

Happy learning! 📚
