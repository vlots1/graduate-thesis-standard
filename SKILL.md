---
name: graduate-thesis-standard
description: Apply Beijing Normal University graduate thesis writing rules to drafting, rewriting, formatting, or auditing master's and doctoral theses. Use for a thesis section or a completed Word, LaTeX, Markdown, or plain-text thesis when the task needs BNU-specific structure, abstracts, headings, layout, figures, tables, equations, references, consistency checks, safe formatting fixes, or a source-traceable compliance report.
---

# BNU Graduate Thesis Standard

Use one shared BNU rule model in exactly one mode at a time. Do not load every reference for a local writing task.

## Natural-language input and default

Treat ordinary language as the primary interface. Infer the thesis type, discipline, source format, target section, task, strictness, and whether the user is drafting or auditing from the request and available files. For example, “审计这篇教育学硕士 Word 论文，只改明确的格式问题” is sufficient.

Accept optional fields only when supplied for precise control: `mode` (`prewrite` or `audit`), `document_type` (`doctoral_thesis` or `master_thesis`), `discipline`, `source_format` (`docx`, `latex`, `markdown`, or `plain_text`), `target_section`, `operation`, `strictness` (`mandatory_only`, `standard`, or `exhaustive`), and `auto_fix` (`false`, `safe_only`, or `true`).

Infer `prewrite` for a scoped drafting, rewriting, expanding, translating, or inserting request. Infer `audit` only for a completed thesis or an explicit inspect/revise request. If unclear, use `prewrite` with `mandatory_only` and state the assumption. Treat `auto_fix: true` as `safe_only`; it never authorizes substantive changes.

## Authority and evidence

Read [source-priority.md](references/source-priority.md) first. The official 2026 rule overrides both templates. The Word and LaTeX templates implement the same school model but are not independent authorities. Never turn an example, a software instruction, or a template-only habit into a mandatory school rule. Use [source-index.md](references/source-index.md) to cite a page, template paragraph/style, or LaTeX file/line region in every material finding.

Load only the needed rule files:

| Need | Read |
| --- | --- |
| Any task | `references/source-priority.md` |
| Cover, declarations, components, abstract, keywords | `references/components-abstract.md` |
| Body headings, page layout, typography, captions, equations, notes | `references/layout-headings-objects.md` |
| Citations, terminology, cross-section consistency | `references/citations-language-consistency.md` |
| Word or LaTeX mechanics | `references/implementation-mappings.md` |
| A conflict or an unclear requirement | `references/conflicts-ambiguities.md` |
| Full audit | all five references above and `checklists/full-audit.md` |

## Mode: `prewrite`

Read [workflows/prewrite.md](workflows/prewrite.md), then load only the section-relevant rule files in the table. Preserve the section's academic purpose. Give the writer only the short output below; do not paste a general handbook.

```markdown
## 当前任务适用的硬性约束
## 推荐性约束
## 当前写作结构
## 禁止或需要避免的做法
## 写作完成后的局部自检
```

Separate content constraints from Word/LaTeX implementation notes. Where school rules leave chapter organization to disciplines, defer to the applicable writing task or discipline and label it as a choice, not a BNU requirement.

## Mode: `audit`

Read [workflows/audit.md](workflows/audit.md), all rule references, [checklists/full-audit.md](checklists/full-audit.md), and the relevant format mapping. Inspect the real submitted files, not a generic checklist. If only text is available, report page/layout checks as unavailable.

Return the exact report sections and issue schema in the audit workflow. Cite every issue as mandatory, recommended, or observational. Aggregate repeated instances but show representative locations and the total count.

Before modifying any document, follow [workflows/safe-fix.md](workflows/safe-fix.md). Keep the original intact and write a distinct rollback copy. Never modify research questions, reasoning, data, sample sizes, statistical results, citation meaning or metadata, conclusions, or an ambiguous interpretation.

## Non-negotiable boundaries

- Do not invent a university requirement, source location, citation, result, or rule.
- Do not let format work replace checking argument quality, factual accuracy, or discipline-specific methods.
- Mark rules that cannot be checked reliably as manual review; do not claim they passed.
- Report a source conflict or ambiguity instead of silently choosing, except where the official rule resolves it.
- Do not edit template core files merely to force a local layout result; identify the deviation and ask for confirmation if changing a core file is the only route.

## Useful examples

See [examples/mode-examples.md](examples/mode-examples.md) for two calls per mode and [examples/test-cases.md](examples/test-cases.md) for the acceptance cases.
