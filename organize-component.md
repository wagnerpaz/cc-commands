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

## Action

- Review the component structure
- Reorder declarations to match the pattern above
- Add `// MARK:` comments to separate each section
- Ensure all hooks and functions are in their correct section

# Follow `useEffect` Rules

- `useEffect` should use a named function declared in the first argument
- the name should describe what the effect does clearly
