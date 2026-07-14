# Mode Examples

Natural language is the default. The YAML blocks below are optional equivalents for callers that need exact control.

## Prewrite 1: Chinese abstract

```text
请为特殊教育硕士论文撰写中文摘要前，列出需要遵守的学校要求。
```

Optional equivalent:

```yaml
mode: prewrite
document_type: master_thesis
discipline: special_education
source_format: docx
target_section: abstract
operation: draft
strictness: standard
auto_fix: false
```

Expected loading: `source-priority.md`, `components-abstract.md`, `workflows/prewrite.md`. Output is limited to abstract purpose/method/result/conclusion, ~1,000-character expectation, 3–8 keywords, Chinese-English correspondence, and Word notes only if requested.

## Prewrite 2: Results statistics revision

```text
我正在修改教育学博士论文的结果部分。请先检查相关写作要求，不要修改统计结果。
```

Optional equivalent:

```yaml
mode: prewrite
document_type: doctoral_thesis
discipline: education
source_format: latex
target_section: results
operation: rewrite
strictness: mandatory_only
auto_fix: safe_only
```

Expected loading: source priority, layout/objects, citations/language, and prewrite workflow. It protects terms/units/figure/table/equation numbering and flags cross-section number consistency. It does not generate or revise statistics.

## Audit 1: Completed Word thesis

```text
请全面审计这篇 Word 格式的硕士论文，只自动修复明确的格式问题。
```

Optional equivalent:

```yaml
mode: audit
document_type: master_thesis
source_format: docx
target_section: full_thesis
operation: inspect
strictness: exhaustive
auto_fix: safe_only
```

Expected loading: all references, full audit checklist, audit workflow, and Word mapping. Report paragraph/style/section/page locations and distinguish rendered checks from field-code checks.

## Audit 2: Completed LaTeX thesis

```text
请审计这篇 LaTeX 格式的博士论文，完成后给出问题报告；所有含义不明确的内容都请人工确认。
```

Optional equivalent:

```yaml
mode: audit
document_type: doctoral_thesis
source_format: latex
target_section: full_thesis
operation: revise
strictness: standard
auto_fix: true
```

Expected loading: all references, full audit checklist, audit workflow, safe-fix boundary, and LaTeX mapping. `auto_fix: true` remains safe-only and writes a rollback copy before mechanical changes.
