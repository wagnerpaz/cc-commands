---
description: Check and fix React component hook declaration order
allowed-tools: Read, Edit
---

Check if the currently open component follows the standardized hook and function declaration order. Add `// MARK: <label>` comments to organize sections.

## Required Order

1. **resources**: Context parameters and resources (`useRef`, `useParams`, `useRouter`, `useAuth`)
2. **stores**: Global state (`useContext`, zustand store selectors)
3. **state**: Local state (`useState`)
4. **memos**: Memoizations (`useMemo`, `useCallback`)
5. **queries**: Async data fetching (`useQuery`, react-query hooks)
6. **mutations**: Mutations (`useUpsertShapedRecord`)
7. **effects**: Effects (`useEffect`)
8. **handlers**: Handler functions (`handleAdd`, `handleSubmit`, etc.)
9. **render**: Rendering
9. **pure functions**: Pure functions should be moved to the bottom of the file, outside the component.

## Hook Import Style

- Import hooks directly instead of using `React.` prefix
- Prefer: `import { useEffect, useMemo, useState } from 'react'`
- Avoid: `React.useEffect`, `React.useMemo`, `React.useState`

## Import Aliases

- Prefer path aliases (e.g., `@/apps/web/...`, `@/components/...`) over relative backwards imports (e.g., `../../../`)
- Check for alias support in `tsconfig.json` or `jsconfig.json` under `compilerOptions.paths`
- Only use relative imports for files in the same directory or immediate subdirectories

## Component Order

When a file contains multiple components:
- The **main component** (usually matching the filename) must be declared **first**
- Helper or sub-components should come after the main component
- Pure functions used by components should be at the bottom of the file

## Action

1. **Check alias support**: Look for `tsconfig.json` or `jsconfig.json` to identify available path aliases
2. **Organize imports**: Replace relative backwards imports (`../`) with path aliases when available
3. **Review the component structure**: Ensure declarations follow the required order
4. **Reorder declarations**: Move hooks and functions to match the pattern above
5. **Add `// MARK:` comments**: Separate each section with appropriate markers
6. **Fix hook imports**: Change any `React.useHook` patterns to use direct imports

# Follow `useEffect` Rules

- `useEffect` should use a named function declared in the first argument
- the name should describe what the effect does clearly
