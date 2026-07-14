# Safe Fix Boundary

## Required preparation

1. Preserve the source file unchanged.
2. Create a new, clearly named rollback copy before changes.
3. State file, expected change, source rule, and whether the operation is reversible.
4. Apply only deterministic changes and render/reinspect affected output.
5. Record old state, new state, location, rule source, and validation result.

## `safe_only` may change

- Explicit font, size, paragraph, heading, and caption style mappings.
- Mechanical heading/number style formatting where the intended hierarchy is already unambiguous.
- Explicit Chinese/English keyword separators and clearly accidental spacing.
- Deterministic figure/table caption position/style and field/list refresh.
- Unambiguous cross-reference display formatting.

## Never change automatically

- Research question, evidence, theoretical reasoning, methods, sample sizes, statistics, results, or conclusion.
- Meaning or metadata of citations/references.
- Content order that has multiple permissible readings.
- Any apparent requirement affected by `conflicts-ambiguities.md`.
- Core LaTeX template files, unless the user explicitly approves a documented template maintenance change.
- Any operation that discards information.

If `auto_fix: true` is supplied, apply this same boundary. It does not override it.
