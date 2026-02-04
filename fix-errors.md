---
description: Fix errors by checking VSCode problems first
allowed-tools: mcp__ide__getDiagnostics, Read, Edit, MultiEdit, Bash
---
Fix errors and warnings in the changed files only: $ARGUMENTS

Follow these steps:
1. Check VSCode problems panel for diagnostics
2. Run a TypeScript check
3. Fix identified issues

After you finish, output a table with a brief explanation of each issue solved