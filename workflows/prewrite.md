# Prewrite Workflow

## 1. Identify the scope

Classify `target_section` as front matter, abstract, body section, object insertion, references, appendix, or full-thesis plan. Identify whether `operation` creates content or only changes format. Record `document_type`, discipline, and source format when known.

## 2. Load narrowly

Always read `source-priority.md`. Then use this routing table:

| Target | Additional material |
| --- | --- |
| Abstract / keywords | `components-abstract.md` |
| Introduction, literature review, methods, results, discussion, conclusion | `layout-headings-objects.md` and `citations-language-consistency.md` |
| Figure, table, equation, footnote | `layout-headings-objects.md`; format mapping only if implementation is requested |
| References | `citations-language-consistency.md`; `conflicts-ambiguities.md` for GB/T edition |
| Appendix | `components-abstract.md`, `layout-headings-objects.md` |
| Cover / declarations / contents | `components-abstract.md`, `layout-headings-objects.md` as needed |

Do not load implementation mapping for a pure prose request. Do not load unrelated whole-thesis checks.

## 3. Produce constraints, not a rewrite

Use exactly these sections. Keep hard constraints short and traceable; omit a section only if it would be empty.

```markdown
## 当前任务适用的硬性约束
- [rule]（来源：R p.#）

## 推荐性约束
- [template-supported suggestion]（来源：W … / L …）

## 当前写作结构
- [only the required function and safe outline]

## 禁止或需要避免的做法
- [specific failure]

## 写作完成后的局部自检
- [observable check]
```

State explicitly when a section's intellectual organization is discipline-dependent. Never create data, findings, citations, or claims to fill a prescribed slot.
