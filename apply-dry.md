# Apply DRY (Don't Repeat Yourself) Principle

Analyze the provided code and apply the DRY principle to eliminate repetition.

## Context

$ARGUMENTS

## Instructions

1. **Identify the target**: Use the selected code block, the argument provided, or infer from recent context what code needs DRY refactoring.

2. **Find repetition patterns**:
   - Look for duplicated code blocks
   - Identify similar logic that differs only in values
   - Find repeated expressions or computations
   - Spot copy-pasted code with minor variations
   - Check for repeated patterns across multiple files if context suggests

3. **Apply DRY refactoring**:
   - Extract repeated logic into reusable functions or utilities
   - Create shared constants for repeated values
   - Use higher-order functions, generics, or abstractions where appropriate
   - Consider creating custom hooks (React) or composables for repeated stateful logic
   - Use mapping/configuration objects to reduce repetitive conditionals

4. **Maintain code quality**:
   - Ensure the refactored code is readable and not over-abstracted
   - Keep the same behavior and functionality
   - Name extracted functions/constants clearly based on their purpose
   - Add type safety where applicable

5. **Output**:
   - Show the refactored code
   - Briefly explain what was deduplicated and why
   - If no meaningful repetition is found, explain why the code is already DRY

Focus on practical improvements that reduce maintenance burden without sacrificing clarity.
