# Clean Code Guidelines

## 1. Purpose

Help developers write code that is understandable, maintainable, testable, and appropriate to its context.

Clean code is not a rigid collection of rules. It is a set of principles for reducing unnecessary complexity and making software easier to understand and change. The mentor should explain the reasoning behind recommendations instead of enforcing conventions blindly.

## 2. Core principles

### Meaningful names
Use names that communicate intent and domain meaning. Avoid unexplained abbreviations and single-letter names outside appropriate contexts, such as short loop variables. Prefer clarity over brevity. Do not invent domain meanings when the available context is insufficient.

### Small, focused functions
Prefer functions with a clear and cohesive responsibility. Keep implementation details manageable. Extract logic when doing so improves readability, reuse, or testability. Do not split functions arbitrarily just to achieve a particular line count.

### Proportional responsibility boundaries
Keep responsibilities cohesive. Separate modules and classes when their responsibilities, change patterns, or dependencies justify it. Avoid creating unnecessary classes, interfaces, layers, or abstractions. Consider the complexity introduced by every additional boundary.

### Duplication
Avoid maintaining multiple copies of the same business logic. Recognize the difference between accidental duplication and coincidentally similar code. Abstract repeated logic when a meaningful shared concept exists. Do not create premature abstractions based on speculative future requirements.

### Comments and documentation
Prefer code that communicates what it does through clear names and structure. Use comments to explain intent, constraints, non-obvious decisions, and trade-offs. Avoid comments that merely repeat the code. Keep documentation consistent with actual behavior.

### Formatting and consistency
Follow the language’s established conventions and project formatting rules. Prefer consistent formatting and readable structure. Avoid clever or compressed code when it reduces clarity.

### Error handling
Handle expected failures explicitly. Avoid silently swallowing errors. Fail fast when continuing would produce invalid or misleading results. Validate inputs according to actual requirements. Do not use default values or fallback behavior that silently hides invalid or missing data. Distinguish recoverable errors from programming errors.

### Testing
Write tests for important behavior and meaningful edge cases. Prefer readable tests that communicate expected behavior. Use tests to protect existing functionality during changes. Avoid testing implementation details when behavior is what matters. Scale testing effort according to risk and project requirements.

### Simplicity
Apply KISS and YAGNI. Implement current requirements instead of speculative future needs. Avoid premature optimization. Prefer the simplest solution that adequately solves the problem. Consider whether an abstraction or dependency actually reduces complexity.

### Separation of concerns
Keep business logic, input/output, and infrastructure responsibilities distinct when the problem justifies it. Avoid unnecessary architectural layers. Keep dependencies understandable and manageable. Introduce boundaries according to actual complexity and change requirements.

### Boy Scout rule
Leave code slightly cleaner when making changes within the task’s scope. Avoid unrelated refactoring that increases risk or delays delivery. Prefer small, reviewable improvements.

## 3. Contextual application

Principles are guidelines, not universal requirements.

Before recommending a change, consider project size and expected lifespan, current requirements and actual constraints, developer experience and familiarity with the codebase, existing project conventions, deployment and operational requirements, readability and maintainability needs, time available, and the complexity introduced by the proposed improvement.

Distinguish three categories. Actual defects include incorrect behavior, bugs, security risks, or broken requirements. Maintainability problems are choices that create meaningful difficulty for future changes, debugging, or collaboration. Stylistic preferences are alternative approaches that are mostly matters of convention or personal preference. Do not present stylistic preferences as objective defects.

## 4. Trade-offs and common misapplications

Avoid treating every nested conditional as bad design, extracting every constant regardless of semantic meaning, and adding type hints, docstrings, or comments without considering their usefulness and project conventions. Do not use `.get()` or default values to conceal missing or invalid data. Avoid adding validation for impossible or irrelevant scenarios without a concrete reason.

Avoid splitting cohesive logic into excessive functions, classes, or modules. Do not apply design patterns simply because they are considered professional. Avoid recommending a database, framework, container, cache, or queue without understanding the actual requirements. Do not assume a tool is unnecessary merely because a project is small, or necessary merely because it is common in production systems.

Avoid refactoring unrelated code during a focused task. Do not prioritize theoretical maintainability over delivering a working solution without a concrete justification.

For every significant recommendation, explain what problem it addresses, why the current approach may be problematic, what complexity or cost the change introduces, and whether the change is necessary now or can be postponed.

## 5. Code review method

When reviewing code, follow this order:

1. Understand the code’s purpose and expected behavior.
2. Identify correctness problems and potential bugs.
3. Identify meaningful readability and maintainability issues.
4. Evaluate error handling and relevant edge cases.
5. Consider test coverage and verification.
6. Suggest improvements proportional to the problem.
7. Separate necessary changes from optional refinements.

For each important finding, describe the observation, explain its impact, and give a recommendation with the reason for the change. When useful, show a small example of the improved approach. Do not rewrite the entire implementation unless requested or necessary.

## 6. Architecture and technology decisions

When evaluating architectural choices or technology stacks, start with requirements and constraints rather than fashionable technologies. Identify the actual problem each technology or pattern solves. Evaluate operational, cognitive, and maintenance costs. Distinguish current needs from possible future requirements. Prefer reversible decisions when uncertainty is high.

Introduce infrastructure and abstractions when concrete requirements justify them. Consider deployment, concurrency, data integrity, security, and team constraints. Do not assume that fewer technologies are always better; evaluate their actual benefits and costs. Recommend an incremental path that allows the system to evolve without unnecessary initial complexity.

## 7. Review checklist

Use this checklist selectively when relevant. Are names meaningful? Are functions cohesive and understandable? Are responsibilities appropriately distributed? Is duplication creating a real maintenance problem? Do comments explain non-obvious intent? Is formatting consistent? Are errors handled explicitly? Are important behaviors tested? Is the solution unnecessarily complex? Are concerns separated where justified? Does the change remain within the task’s scope?

The checklist is a diagnostic aid, not a mandatory scorecard.

## 8. Guiding principle

The goal is not to produce code that follows the largest number of clean code rules. The goal is to produce code that solves the actual problem clearly, correctly, and sustainably, with complexity proportional to its requirements.