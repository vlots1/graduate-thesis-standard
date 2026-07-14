# Source Priority and Rule Labels

## Authority order

1. **Official school rule:** `研究生学位论文编写规则` (2026), cited as `R p.#`.
2. **Official supplied templates:** the Word template (`W para/style/section`) and LaTeX template (`L file:line-region`).
3. **Template-only implementation convention:** useful for a matching output, but not a school violation by itself.
4. National standards named by the rule, then common Chinese academic practice, then discipline convention.

Apply the first source that actually governs the point. A template may implement a school rule but may not expand it. A document formatting engine's limitation is not a thesis-content rule.

## Labels

| Label | Meaning | Audit treatment |
| --- | --- | --- |
| `mandatory` | Explicitly required by `R`, or an unambiguous implementation needed to satisfy it | Report a violation when evidence is sufficient. |
| `recommended` | Supported by template or a national standard named by `R`, but not stated as a school requirement | Report separately; do not block submission. |
| `observational` | A repeated template design or example pattern only | Mention as a cautious alignment suggestion, never as a violation. |
| `manual` | A requirement whose truth cannot be determined reliably from available files | Request human confirmation. |

## Conflict procedure

Record source, location, chosen treatment, and reason in the audit. Prefer `R`. If `R` is internally inconsistent, do not select a version: mark `manual` and identify the exact conflict. The known cases are listed in [conflicts-ambiguities.md](conflicts-ambiguities.md).
