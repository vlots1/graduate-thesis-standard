# Headings, Layout, Figures, Tables, Equations, and Notes

## Page and body layout

- **Mandatory:** Cover is A3. Inner pages and abstracts are A4; print double-sided except cover and copyright page. `R pp.6-7`.
- **Mandatory:** Main-text margins are top/bottom 2.54 cm and left/right 3.17 cm. `R p.8`; confirmed in `W sections 1-18` and `L bnuthesis.cls:414-459`.
- **Mandatory:** Each body chapter begins on a new page. `R p.8`.
- **Mandatory:** Front matter from abstract through the page before introduction uses continuous uppercase Roman numerals; main matter from introduction through the end uses continuous Arabic numerals, centered in footer. `R p.8`.
- **Mandatory:** Start running headers at abstract; header text matches the part title. `R p.8`.
- **Mandatory:** Main Chinese body uses Songti 小四 and English Times New Roman 小四, 2-character first-line indent, fixed 20 pt line spacing. `R p.8`.
- **Mandatory:** Formula display spacing is 1.5 lines. `R p.8`.

## Heading hierarchy

Use few levels. The school permits either a numeric hierarchy or a Chinese ordinal hierarchy; do not mix the two within one hierarchy without an approved discipline reason.

| Level | Numeric form | Chinese form | Mandatory layout (`R p.8`) |
| --- | --- | --- | --- |
| Chapter | `第1章 标题` | `第一章 标题` | Heiti 三号, bold, centered, 24 pt before / 18 pt after. |
| Section | `1.1 标题` | `第一节 标题` | Heiti 小三; numeric left, ordinal centered; 24 pt before / 6 pt after. |
| Item | `1.1.1 标题` | `一、标题` | Heiti 四号; numeric left, ordinal indent 2 characters; 12 pt before / 6 pt after. |
| Clause | `1.1.1.1 标题` | `（一）标题` | Heiti 小四; numeric left, ordinal indent 2 characters; 12 pt before / 6 pt after. |

- Arabic heading numbers use Times New Roman. Numeric chapter number/title has one Chinese-character space; numeric section/item/clause has a half-character space. `R p.8`.
- The rule suggests three levels as sufficient and allows four layout levels; additional levels are not a school requirement and require discipline judgement. `R p.8`.
- Introduction onward appears in contents. Abstract, references, appendix, index, achievements, acknowledgements, and committee list use chapter-level visual styling but are not regular numbered chapters. `R pp.6-9`; verify actual field code or LaTeX starred commands.

## Objects and notes

- **Mandatory:** Body figures and tables use Arabic numbers beginning at 1; continuous numbering before appendices is the printed requirement, though chapter numbering is allowed in the general rule. See conflict `C-01`. Figure caption below; table caption above. `R pp.5,8-9`.
- **Mandatory:** Figure/table captions: Songti 五号, centered, single spacing. Figure 6 pt before / 12 pt after; table 6 pt before / 6 pt after. `R pp.8-9`.
- **Mandatory:** Display equations start on a separate centered line, Arabic number in parentheses at the far right, and may be chapter-numbered if numerous. Break long expressions only at operators. `R p.5`, `R p.9`.
- **Mandatory:** Footnotes use superscript markers at sentence end and per-page circled numbers ①②③; footnote text Songti 小五, single spacing. `R p.9`.
- **Mandatory:** Appendix labels are A, B, C…; each has a title. Appendix figures/tables/equations restart under the appendix identifier (`图A1`, `表A1`, etc.). `R p.6`.
- **Recommended:** Use cross-references rather than typed object numbers. Word template explains captions/fields; LaTeX template uses `\label` and `\ref`. `W paras 223-275`; `L data/appendix.tex:8-58`.
- **Observational:** Three-line tables, data-source notes, significant-digit schemes, and detailed statistical notation are not prescribed by the supplied school rule. Apply the discipline's approved convention and report only consistency, unless a faculty rule is supplied.
