# mini-quote-app

**A one‑sentence “Quote of the Day” web page** – perfect for practicing Git basics.

## Goal
- Master branch creation, PR workflow, merging, and conflict resolution.
- Build a minimal HTML + CSS app that displays a single sentence.

## Quick start
```bash
git clone https://github.com/<your-id>/mini-quote-app.git
cd mini-quote-app
python -m http.server 8000   # open http://localhost:8000
```

## File tree

```
mini-quote-app/
├─ index.html   # single <h1> sentence
├─ style.css    # simple style, changed per branch
└─ README.md    # this file

## Git workflow
- Initialize – commit index.html on main.
- Feature branches – e.g. v1-author, v2-style, v3-date-feature.
- Pull Request – create PR, review, approve, merge.
- Conflict practice – edit main directly, then resolve conflict on a feature branch.

### Initial setup
```bash
git init
git add README.md
git commit -m "Initial quote app"
git branch dev
git checkout dev
```

### Now each team member does:
```bash
# Edit content
# 1) On dev branch
git checkout dev
# edit index.html or style.css
git add index.html style.css README.md
git commit -m "Change quote text/style"
git push origin dev

# 2) On main branch (same user or another)
git checkout main
# edit index.html or style.css (optional)
git add index.html style.css README.md
git commit -m "Quote update on main"
git push origin main

# 3) Handle conflicts
# If conflicts occur during push/pull:
# resolve conflicts manually in the file
git add <resolved-file>
git commit -m "Resolve merge conflict"
git push origin dev   # or main

# 4) Create Pull Request
# Open GitHub: New pull request → compare dev → main
# Add team members for review
# Merge after approval
```

## Tips for collaboration
- PR title: Add <feature>
- PR description: brief reason for the change.
- Always run git pull origin main before merging.
- When a conflict appears, resolve it, git add <file>, commit and push.
- Make small commits with clear messages.
- Update README.md with branch-specific changes.
- Practice code review and conflict resolution with other team members.
- Celebrate successful merges!

## Author
- Name : Kyumun Hwang
- Git ID : Kyumunhwang
