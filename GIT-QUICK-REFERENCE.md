# Git Quick Reference for Your Knowledge Repo

Essential Git commands for managing your personal knowledge repository.

---

## Initial Setup (One Time)

```bash
# Configure your identity
git config --global user.email "miguel.gomes2@fanduel.com"
git config --global user.name "Miguel Gomes"

# Clone your repo (only first time)
git clone https://github.com/YOUR-USERNAME/personal-knowledge-repo.git
cd personal-knowledge-repo
```

---

## Daily Workflow

### See what changed
```bash
git status
```
Shows untracked, modified, and staged files.

### Stage changes
```bash
# Stage specific file
git add 01-technical-learnings/python-basics.md

# Stage all changes
git add .

# Unstage a file
git restore --staged filename.md
```

### Commit
```bash
# Commit with message
git commit -m "Add Python async patterns guide"

# See example messages below
```

### Push to GitHub
```bash
# Push to main branch
git push

# Or explicitly
git push origin main
```

---

## Commit Message Conventions

Good commit messages make history searchable.

### Format
```
[type]: [short description]

[optional detailed explanation]
```

### Types
- `add:` - New note or content
- `update:` - Modified existing content
- `fix:` - Correction or typo fix
- `reorganize:` - Moved or renamed files
- `archive:` - Moved content to archive

### Examples

✅ **Good:**
```bash
git commit -m "add: Python async patterns guide"
git commit -m "update: Meeting notes - Q3 planning, added decisions"
git commit -m "fix: Typo in Kafka reference guide"
git commit -m "reorganize: Move 2026-06 meeting notes to archive"
```

❌ **Avoid:**
```bash
git commit -m "updates"              # Too vague
git commit -m "stuff"                # Meaningless
git commit -m "asdf"                 # Not descriptive
git commit -m "work in progress"     # Unhelpful
```

---

## Checking Your Work

### View recent commits
```bash
# Last 5 commits
git log --oneline -5

# Pretty log with dates
git log --oneline --date=short --pretty=format:"%h %ad %s"
```

### See what you changed
```bash
# See unstaged changes
git diff

# See staged changes
git diff --staged

# See changes in a specific file
git diff filename.md
```

### View a specific commit
```bash
git show <commit-hash>
```

---

## Fixing Mistakes

### Undo unstaged changes
```bash
# Undo changes in one file
git restore filename.md

# Undo all unstaged changes
git restore .
```

### Unstage changes
```bash
git restore --staged filename.md
```

### Fix last commit message
```bash
git commit --amend -m "New message"
```

### Add forgotten file to last commit
```bash
git add forgotten-file.md
git commit --amend --no-edit
```

### Undo last commit (keep changes)
```bash
git reset --soft HEAD~1
```

---

## Syncing with GitHub

### Pull latest changes (if editing on multiple machines)
```bash
git pull
```

### Push your commits
```bash
git push
```

### See what's different from GitHub
```bash
git status  # Shows if you're ahead or behind
```

---

## Branches (Optional)

For experimenting without affecting main:

```bash
# Create new branch
git checkout -b experimental-feature

# Switch back to main
git checkout main

# Merge changes from branch
git merge experimental-feature

# Delete branch
git branch -d experimental-feature
```

---

## Useful Commands

### Search commit history
```bash
# Find commits mentioning a keyword
git log --all --oneline --grep="Python"

# Find commits changing a specific file
git log --oneline -- filename.md
```

### See who changed what
```bash
git blame filename.md
```

### Stash changes (temporarily save)
```bash
# Save current changes
git stash

# Get them back later
git stash pop
```

### Check GitHub repo status
```bash
# URL of your remote
git remote -v

# See if local matches GitHub
git status
```

---

## Troubleshooting

### "fatal: not a git repository"
You're not in the repo directory. Navigate to it:
```bash
cd personal-knowledge-repo
```

### "nothing to commit"
No changes detected. Create or modify a file:
```bash
# Check what's tracked
git status

# Add your file
git add new-file.md
git commit -m "add: new-file"
```

### "error: src refspec main does not match any"
Your repo might be on `master` not `main`:
```bash
git branch              # See your branch
git push origin master  # Push to master if that's the default
```

### Changes not on GitHub
You need to push:
```bash
git push origin main
```

### Merge conflicts
When pulling changes:
```bash
git status  # See conflicted files

# Edit conflicted files manually, then:
git add .
git commit -m "Resolve merge conflicts"
git push
```

---

## One-Minute Workflows

### Add one new note
```bash
git add 01-technical-learnings/topic.md
git commit -m "add: [topic] guide"
git push
```

### Update multiple notes
```bash
git add .
git commit -m "update: Various notes"
git push
```

### Update INDEX.md after adding notes
```bash
git add INDEX.md
git commit -m "update: INDEX with new notes"
git push
```

### Fix a typo across multiple files
```bash
# Edit files...
git add .
git commit -m "fix: Typos and formatting"
git push
```

---

## Reference Card

| Task | Command |
|------|---------|
| Check status | `git status` |
| Stage all | `git add .` |
| Stage one file | `git add filename.md` |
| Commit | `git commit -m "message"` |
| Push | `git push` |
| Pull | `git pull` |
| See recent commits | `git log --oneline -5` |
| Undo changes | `git restore filename.md` |
| View history | `git log filename.md` |
| See changes | `git diff` |

---

## Pro Tips

1. **Commit often.** Small commits are easier to understand and revert if needed.

2. **Write clear messages.** Future you will thank present you.

3. **Pull before pushing.** If multiple devices, pull first to avoid conflicts.

4. **Review before committing.** Use `git diff` to see what you're committing.

5. **Use `.gitignore`.** Keep private files and IDE config out of your repo.

---

For more help:
```bash
git help [command]
# Example: git help commit
```

Or visit [Git Documentation](https://git-scm.com/doc)
