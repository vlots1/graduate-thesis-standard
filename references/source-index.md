# Source Index

## Identifiers

- `R`: `研究生学位论文编写规则` (北京师范大学学位评定委员会办公室, January 2026), supplied PDF. PDF page numbers below are document pages, not viewer index.
- `W`: `北京师范大学学位论文word版参考模板（一）`, supplied DOCX. Paragraph numbers are extraction order; style and section names are from the document package.
- `L`: `bnuthesis-latex-template20260301`, supplied directory. Line references are stable regions in the named source files.

## Evidence map

| Topic | Primary source | Template corroboration | Rule class |
| --- | --- | --- | --- |
| National basis; faculty additions permitted | `R p.2` | — | mandatory context |
| Integrity, language, terminology, units, clear images | `R p.3` | `L data/abstract.tex` | mandatory |
| Main components and cover/title fields | `R p.3` | `W paras 4-41`; `L bnusetup.tex:1-99` | mandatory |
| Abstract content and lengths | `R pp.3-4` | `W paras 52-75`; `L data/abstract.tex` | mandatory |
| Keywords | `R p.4` | `W paras 59,74-75`; `L data/abstract.tex` | mandatory |
| Contents, object lists, symbol list | `R p.4` | `W paras 78-175`; `L bnuthesis-example.tex:35-43` | mandatory/conditional |
| Body scope and discipline freedom | `R pp.4-5` | `W paras 189-218` | mandatory principle |
| Figures, tables, equations | `R pp.5,8-9` | `W paras 219-292`; `L bnuthesis.cls:1729-1836` | mandatory |
| Citations and references | `R p.5, p.9` | `W paras 411-465`; `L bnusetup.tex:145-166` | mandatory |
| Appendix / index / achievements / acknowledgement | `R p.6` | `W paras 468-507`; `L data/appendix.tex`, `data/index.tex`, `data/resume.tex`, `data/acknowledgements.tex` | mixed |
| Paper, printing, assembly, cover/title/spine | `R pp.6-7` | `W paras 4-48`; `L bnuthesis-example.tex:20-29` | mandatory |
| Abstract typography; TOC typography | `R pp.7-8` | `W styles and paras 52-175`; `L bnuthesis.cls:1836-1960` | mandatory outcome |
| Margins, headers, pagination, headings, body | `R p.8` | `W sections/styles`; `L bnuthesis.cls:414-459, 1505-1565, 1847-1960` | mandatory |
| Captions, equations, footnotes, other back matter | `R p.9` | `W styles/paras 227-289, 411-536`; `L bnuthesis.cls:1729-1836` | mandatory / conflicts noted |

No rule in this index is inferred solely from a file name. The source extraction evidence is retained in this task's `work/` directory, but is not part of the reusable skill.
