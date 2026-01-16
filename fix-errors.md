---
description: Fix errors by checking VSCode problems first
allowed-tools: mcp__ide__getDiagnostics, Read, Edit, MultiEdit, Bash
---
Please fix errors in the code: $ARGUMENTS

- Check VSCode problems panel for diagnostics
- Run `npx tsc --noEmit` to catch TypeScript errors
- Fix identified issues