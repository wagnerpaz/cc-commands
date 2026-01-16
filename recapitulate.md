---
description: Summarize recent commits and show current uncommitted changes
allowed-tools: Bash
---

Provide a quick recap of the repository's recent activity and current state.

## Process

1. Run `git log --oneline -10` to get the last 10 commits
2. Run `git status` to see current uncommitted changes
3. Run `git diff --stat` to see a summary of modified files

## Output Format

Provide a concise summary with:

### Recent Commits
- Briefly describe the pattern/theme of recent work (e.g., "Recent work focused on X feature and Y fixes")
- Highlight any notable commits

### Current Changes
- List files that have been modified, added, or deleted
- Briefly describe what each change appears to be about based on the file names and diff stats
- Note any untracked files

Keep the summary brief and actionable. Help the user understand where they left off and what's in progress.
