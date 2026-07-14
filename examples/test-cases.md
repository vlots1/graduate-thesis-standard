# Acceptance Cases

| ID | Request / artifact condition | Expected mode and result |
| --- | --- | --- |
| T01 | Draft a Chinese abstract | `prewrite`; load abstract rules only; mandatory vs recommendation separated. |
| T02 | Draft methods | `prewrite`; preserve discipline-specific method design; apply terms, headings, citations only. |
| T03 | Revise results statistics | `prewrite`; check terminology/units/cross-reference consistency; refuse substantive statistical rewrite. |
| T04 | Insert a figure/table | `prewrite`; use object rules and format-specific caption mechanics only when requested. |
| T05 | Organize references | `prewrite`; require one GB/T system and mark edition ambiguity/manual metadata validation. |
| T06 | Audit a complete DOCX | `audit`; inspect real styles, fields, sections, headers/footers, and rendered pages where available. |
| T07 | Audit a complete LaTeX thesis | `audit`; inspect source, compile/render output, labels, bibliography, and local class overrides. |
| T08 | Figure numbering conflict | `audit`; report C-01, do not auto-renumber. |
| T09 | Template-only sample item | `prewrite` or `audit`; classify observational, not mandatory. |
| T10 | Text-only or incomplete file | `audit`; mark layout/page checks manual or unavailable, never claim a pass. |

Pass criteria for all cases: the mode does not load the other mode's complete checklist; every mandatory conclusion has an `R` citation; no template-only item is elevated; and any proposed automatic change stays inside `safe-fix.md`.
