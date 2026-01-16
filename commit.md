---
description: Commit changes in logical chunks with concise messages
allowed-tools: Bash, Read
---

Review the current git changes and help commit them in logical chunks.

## Process

1. Run `git status` and `git diff` to see all changes
2. Analyze which changes belong together logically (same feature, same file type, related fixes)
3. For each logical chunk, ask the user if they want to commit it
4. Stage only the files for that chunk using `git add <files>`
5. Create a commit with a concise message

## Commit Message Format

- **Title**: Max 50 chars, imperative mood (e.g., "add user auth", "fix nav bug")
- **Description**: Optional, only if needed to explain "why" (not "what")
- Use conventional commit prefixes: feat, fix, chore, refactor, docs, style, test

## Rules

- NEVER add Co-Authored-By or any attribution
- Keep messages minimal and informative
- Group related changes together
- Ask before each commit
- Use HEREDOC format for commit messages:
```bash
git commit -m "$(cat <<'EOF'
feat(scope): concise title

Optional description if needed.
EOF
)"
```
