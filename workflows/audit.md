# Full Audit Workflow

## 1. Establish what can be inspected

Record supplied files, format, version/date, page count or source-file count, and whether the document can be rendered. Use page/paragraph/style/line locations native to the format. Do not claim a visual check from plain text.

## 2. Inspect in dependency order

1. Components and order.
2. Section breaks, pagination, headers, contents, and heading hierarchy.
3. Body typography and captions.
4. Figure/table/equation/footnote objects and cross-references.
5. Citations/references.
6. Abstract/keyword and cross-section semantic consistency.
7. Format-specific template use and prohibited core changes.

## 3. Classify issues

Use `blocker` for a confirmed missing mandatory component, invalid page/numbering regime, serious mandatory structure failure, or an unresolved factual consistency contradiction that could affect degree review. Use `major` for a confirmed mandatory rule violation that does not stop inspection. Use `minor` for a localized mandatory presentation issue. Use `advisory` for recommended/observational alignment.

Use this schema for every issue or aggregated issue family:

```yaml
id: BNU-AREA-001
severity: blocker | major | minor | advisory
rule_level: mandatory | recommended | observational | manual
category: components | headings | layout | objects | references | consistency | implementation
location: page / section / paragraph / style / file:line
observed: concrete evidence
expected: concrete requirement
source: R p.#; W …; L …
confidence: high | medium | low
auto_fixable: no | safe_only
recommended_action: specific next action
instances: count and representative locations
```

## 4. Report

```markdown
# 学位论文规范审计报告

## 1. 审计范围与文件状态
## 2. 总体结论
- 严重问题数量：
- 重要问题数量：
- 一般问题数量：
- 无法自动判断的问题数量：
## 3. 阻断提交的问题
## 4. 结构与组成问题
## 5. 标题、编号与目录问题
## 6. 页面和排版问题
## 7. 图表、公式和注释问题
## 8. 引用与参考文献问题
## 9. 中英文摘要及术语一致性问题
## 10. 跨章节一致性问题
## 11. 需要人工确认的问题
## 12. 建议修复顺序
## 13. 自动修复记录或修复建议
```

Put mandatory and recommendation-only findings in separate entries. A no-finding category should say what was checked and its limitation.

## 5. Re-audit after a safe fix

Recheck the changed locations and all dependent fields: contents/list pages after heading or caption edits; citations after reference edits; layout after section changes. Mark an earlier issue `resolved`, `not resolved`, or `not rechecked`; do not silently remove history.
