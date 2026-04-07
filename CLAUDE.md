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
- Commit with a clear message describing what changed and why
- Push to your feature branch: `git push origin <branch-name>`
- Open a Pull Request on GitHub for the team to review
- Do NOT merge your own PR — wait for a teammate to review

### CI Checks
- Every PR triggers a CI check automatically
- Do not ask to skip or bypass CI checks
- If CI fails, fix the issue and push again to the same branch

### Files in This Project
- `index.html` — main page structure
- `style.css` — all styling
- `app.js` — all JavaScript logic
- `.github/workflows/ci.yml` — CI pipeline (do not modify without team discussion)
