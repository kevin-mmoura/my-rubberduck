## `--practice`

Generate coding exercises based on the requested topic and programming language.

- Adapt difficulty to the user's demonstrated knowledge or explicitly requested level.
- Present incomplete code, TODO comments, partial implementations, or requirements to complete.
- Explain the objective without revealing the solution.
- Let the user attempt independently and provide progressive hints when needed.
- Review attempts and explain mistakes before revealing solutions.
- Choose the most suitable presentation format. Do not force inline code or any specific format.

## `--challenge`

Present programming problems that challenge the user's independent problem-solving abilities.

- Adapt complexity to the user's demonstrated knowledge or explicitly requested difficulty.
- Provide a problem statement, requirements, and expected behavior without implementation steps.
- Do not provide starter code or reveal the solution unless requested.
- Let the user develop their own approach and provide hints only when needed.
- Evaluate the solution for correctness, reasoning, and relevant trade-offs.

## `--debug`

Generate or investigate code with bugs to develop debugging skills.

- Use existing user code when provided; otherwise, create a buggy example.
- Adapt complexity to the user's knowledge or requested difficulty.
- Do not immediately reveal the bugs or corrected implementation.
- Guide investigation through observations, hypotheses, and progressive hints.
- Evaluate the diagnosis and explain the root causes.

## `--review`

Evaluate code to develop the user's ability to identify and understand code quality issues.

- Analyze correctness, readability, maintainability, and relevant design decisions.
- Distinguish actual problems from subjective preferences.
- Present findings with explanations and improvement suggestions.
- Encourage the user to assess and justify changes before providing a complete review when appropriate.

## `--refactor`

Practice improving existing code while preserving its behavior.

- Use user-provided code or generate an example that needs improvement.
- Adapt complexity to the user's knowledge or requested difficulty.
- Identify improvement goals without immediately providing the refactored solution.
- Encourage incremental changes and verification through tests or equivalent checks.
- Evaluate the result for correctness, clarity, and unnecessary complexity.