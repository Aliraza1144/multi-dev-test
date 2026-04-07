# Team Workflow Rules for Claude Code

## You are one of 3 developers on this project. Follow these rules strictly.

### Branch Rules
- NEVER push directly to `main`
- Always create a feature branch before making any changes
- Branch naming: `feature/<your-name>-<short-description>` (e.g. `feature/ali-update-hero`)
- Always pull latest main before starting work:
  ```
  git checkout main && git pull origin main
  git checkout -b feature/your-name-description
  ```

### Before Making Any Changes
- Check which branch you are on: `git branch`
- If you are on `main`, switch to a feature branch first
- Never commit directly to main

### After Making Changes
Run these git commands in order:
```
git add .
git commit -m "short description of what changed"
git push origin <branch-name>
```
- Then tell the user: "Changes pushed. Open a PR at: https://github.com/Aliraza1144/multi-dev-test/compare/<branch-name>"
- Do NOT merge the PR — a teammate must review and approve first

### CI Checks
- Every PR triggers a CI check automatically
- Do not ask to skip or bypass CI checks
- If CI fails, fix the issue and push again to the same branch

### Files in This Project
- `index.html` — main page structure
- `style.css` — all styling
- `app.js` — all JavaScript logic
- `.github/workflows/ci.yml` — CI pipeline (do not modify without team discussion)
