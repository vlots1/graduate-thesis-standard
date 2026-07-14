# Word and LaTeX Implementation Mappings

This file maps the shared school model to two formats. It does not create new school rules.

## Word (`.docx`)

| Check | Evidence / method | Classification |
| --- | --- | --- |
| Page setup and sections | Inspect each section: A4 inner pages, required margins, section breaks, header/footer and page-number fields. Word template has 18 sections with 2.54/3.17 cm margins. `W sections 1-18`. | Mandatory where it implements `R p.8`. |
| Styles | Map headings 1–4, Normal, Caption, `图标题格式`, `表标题格式`; flag direct formatting that overrides a mapped style. `W styles`; `W paras 189-194, 227-289`. | Styles are recommended implementation; resulting layout is mandatory. |
| Contents / lists | Require Word TOC fields and figure/table caption fields where available; update fields before pagination audit. `W paras 79-175, 223-275`. | Recommended mechanics; resulting lists/locations mandatory where `R` requires them. |
| Headers / footers | Check section linkage, header text, Roman-to-Arabic restart, centered footer page number. | Mandatory outcome; inspect field codes manually if library cannot evaluate them. |
| Anchors and cross-references | Inspect whether figures/tables are anchored near text and captioned using fields; flag typed numbers only as a recommendation. | Recommended. |

## LaTeX (`.tex`)

| Check | Evidence / method | Classification |
| --- | --- | --- |
| Entry and degree | Check `\documentclass[degree=doctor|master]{bnuthesis}` and `\bnusetup` metadata. `L bnuthesis-example.tex:5-17`; `L bnusetup.tex:1-99`. | Recommended template integration; degree-specific spine remains mandatory. |
| Engine / fonts | Template declares XeLaTeX and supplies cross-platform font sets; comments recommend Windows fonts for final output. `L bnuthesis-example.tex:1-15`; `L latexmkrc`. | Observational implementation. Verify final PDF appearance, not a particular engine. |
| Page setup / headings | The class uses A4 graduate margins and defines headings, headers, front/main page numbering. `L bnuthesis.cls:414-459, 1474-1565, 1847-1960`. | Expected implementation of mandatory rule; do not change class core casually. |
| Contents and components | Use `\frontmatter`, `\mainmatter`, `\backmatter`, `\tableofcontents`, and supplied component environments. `L bnuthesis-example.tex:29-81`. | Mandatory outcome; commands themselves are recommended. |
| Captions / references | Use `\caption`, `\label`, `\ref`/`\eqref`, bibliography style matching the selected citation system. `L bnusetup.tex:145-166`; `L bnuthesis.cls:1729-1836`. | Mandatory outcomes; commands/styles recommended. |
| Core template files | Treat `bnuthesis.cls`, supplied `.bst/.bbx/.cbx`, and core layout setup as protected. Inspect local overrides before conclusions. | Safe-fix boundary. |

The LaTeX template exposes optional APA/MLA styles in comments. These are capabilities, not permission from `R`; do not select them unless an approved additional requirement supersedes the school rule.
