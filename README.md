# BNU Graduate Thesis Standard Skill

为北京师范大学硕士、博士学位论文提供写作前约束和全文规范审计的通用写作 Skill。

它依据以下材料建立规则库：

- 《北京师范大学研究生学位论文编写规则（2026版）》
- 北京师范大学学位论文 Word 参考模板（一）
- 北京师范大学学位论文 LaTeX 参考模板

本项目不附带上述学校材料。使用者应从学校正式渠道或已获授权的渠道取得最新版本，并确认本单位是否有补充要求。

## 能做什么

本 Skill 有两种明确分开的使用方式：

- `prewrite`：写摘要、方法、结果、参考文献或插入图表之前，只给出当前任务直接相关的学校要求，避免把整套规范塞进写作上下文。
- `audit`：在论文基本完成后，检查结构、标题、页码、图表、公式、参考文献和前后一致性，并按严重程度给出有位置的问题清单。

它会区分：

- 学校明确要求；
- 模板支持但不是硬性要求的建议；
- 仅从模板示例中观察到的惯例；
- 无法可靠自动判断、需要人工确认的事项。

## 适用范围

- 硕士和博士学位论文。
- Word、LaTeX、Markdown 或纯文本论文材料。
- 不同学科和研究方法；学校未规定的学术组织方式仍由学科规范和具体写作任务决定。

## 安装（推荐：让 Agent 用自然语言完成）

优先让你正在使用的 Agent 安装，而不是自己运行 `git clone`。把仓库链接替换进下面这句话即可：

```text
请从 https://github.com/vlots1/graduate-thesis-standard.git 安装 graduate-thesis-standard Skill。请保留完整文件夹结构，安装到你自己的 Skills 目录。完成后检查 SKILL.md、references、workflows 和 examples 是否齐全，并告诉我安装位置。不要改动仓库中的内容。
```

这适用于支持本地 Skill 或自定义指令的 Agent，例如 Codex、Claude Code、WorkBuddy，以及其他类似工具。不同工具的 Skills 目录不同，应由该 Agent 按自己的安装方式选择正确位置。

也可以说得更具体：

- 对 Codex：“请从 <GitHub 仓库链接> 安装这个 Skill，然后帮我写一篇教育学硕士论文摘要。”
- 对 Claude Code：“请安装 <GitHub 仓库链接> 中的 graduate-thesis-standard，并在安装后检查文件是否完整。”
- 对其他 Agent：“请把这个 GitHub 项目作为本地论文规范 Skill 安装；如果你的环境不支持 Skill，请告诉我需要的手动安装位置。”

只有当使用的 Agent 不支持安装时，才手动下载项目并复制完整的 `graduate-thesis-standard` 文件夹。不要只复制 `SKILL.md`，因为详细规则、审计流程和来源索引都在其余文件中。

## 使用（推荐：直接说需求）

日常使用不需要填写参数。直接说明论文类型、学科、当前章节和目标即可。

### 写中文摘要前

```text
请用 graduate-thesis-standard 帮我准备心理学硕士论文的中文摘要写作要求。
```

### 修改结果部分前

```text
我正在修改物理学博士论文的结果部分。请先列出当前必须遵守的学校要求，不要改动任何统计结果。
```

### 审计完整 Word 论文

```text
请审计这篇 Word 格式的硕士论文，检查目录、页码、标题、图表和参考文献；只修复明确的格式问题。
```

### 审计完整 LaTeX 论文

```text
请检查这篇 LaTeX 格式的博士论文是否符合学校规范，并把不能自动判断的问题单独列出。
```

Skill 会从任务中判断论文类型、学科、文件格式和使用方式。局部写作默认采用轻量的写作前约束；明确要求检查完整论文时才采用全文审计。无法判断时，它只使用硬性要求，并说明自己的假设。

## 高级控制（可选）

只有在需要精确限制检查范围、严格程度或自动修改边界时，才补充结构化信息，例如：

```yaml
mode: audit
document_type: master_thesis
source_format: docx
strictness: exhaustive
auto_fix: safe_only
```

## 项目结构

```text
graduate-thesis-standard/
├── SKILL.md                         # 调用入口与规则加载方式
├── references/                      # 可追溯的学校规则和模板映射
├── workflows/                       # 写作前约束、全文审计和安全修改边界
├── checklists/                      # 全文审计检查项
├── examples/                        # 调用示例与验收场景
└── agents/openai.yaml               # Skill 展示信息
```

## 规则来源与处理原则

优先级如下：

1. 学校正式发布的编写规则；
2. 学校 Word 和 LaTeX 参考模板；
3. 模板中反复出现、但没有正式条文支持的排版惯例；
4. 学科和通行学术写作规范。

当材料存在冲突或含义不清时，Skill 会记录来源和原因，并提示人工确认。它不会把模板操作说明、示例目录、示例文献或可选功能当成强制规定。

## 安全边界

Skill 可以提出或执行明确、机械且可回退的格式修改，例如标题样式、段落格式、图表题注样式和页码设置。

它不会自动改动研究问题、理论论证、数据、统计结果、样本量、引用含义、文献事实信息或学术结论。

## 已知限制

- 版式检查需要真实的 Word 或 LaTeX 文件及可查看的输出；只有纯文本时，会明确标记无法检查的项目。
- 中英文摘要是否真正对应、文献事实是否正确、统计数字是否合理，仍需要人工或专门工具核实。
- 学院、学部或培养单位的补充要求可能高于或细化学校通用规则，应作为额外来源加入。

## 更新学校规则

学校规则或模板更新后，优先更新：

- `references/source-index.md`
- `references/components-abstract.md`
- `references/layout-headings-objects.md`
- `references/citations-language-consistency.md`
- `references/conflicts-ambiguities.md`

更新后，请运行 Skill 的基础检查，并用 `examples/test-cases.md` 中的十个场景复核两种模式没有混淆。


