# ASE/ICSE/FSE/ISSTA 顶会论文 skill 包使用说明


## 文件夹结构

```text
ase-topconf-paper-skills/
├── se-topconf-paper/
├── se-topconf-introduction/
├── se-topconf-conclusion/
├── se-topconf-redline-review/
└── 使用说明.md
```

## 每个 skill 做什么

### 1. se-topconf-paper

主控 skill，适合整篇论文规划、重构、精修和投稿前检查。

适用请求：

- “帮我把这篇文章改成 ASE/ICSE/FSE/ISSTA 风格”
- “帮我设计顶会论文结构和 RQ”
- “检查 abstract-intro-conclusion 是否一致”
- “帮我规划图表、实验、threats、artifact statement”
- “把中文核心/工程报告式内容迁移成英文顶会论文”

内部引用资料：

- `paper-structure.md`：不同论文类型的章节结构。
- `figures-tables-style.md`：ASE 近年论文常见图表类型与 LaTeX 图表规范。
- `writing-patterns.md`：摘要、引言、结果、贡献、结论常用表达。
- `review-checklist.md`：终稿审阅清单。
- `venue-and-policy-notes.md`：会议模板、匿名、artifact、open science 等政策检查入口。

### 2. se-topconf-introduction

专门写或改 Introduction。

适用请求：

- “帮我写 ASE 风格 Introduction”
- “帮我诊断引言每句话的功能”
- “帮我把 gap、RQ、contribution 串起来”
- “我这个引言像中文工程论文，帮我改成英文顶会风格”

核心方法：

`field importance -> object -> evidence -> gap -> consequence -> this paper -> RQs -> method -> findings -> contributions`

### 3. se-topconf-conclusion

专门写或改 Conclusion。

适用请求：

- “帮我写顶会论文结论”
- “帮我检查结论是否和结果/引言一致”
- “把结论写得更像 ASE/ICSE 风格”
- “给结论做 sentence-role 分析”

核心方法：

`paper object -> evidence -> findings -> reusable contribution -> implications -> boundary/future direction -> grounded takeaway`

### 4. se-topconf-redline-review

终稿红线审阅 skill，适合提交前最后一轮 LaTeX 检查。

适用请求：

- “帮我做最终 pre-submission review”
- “只修关键错误，不要大幅润色”
- “输出 revised.tex、final.tex 和 review.md”
- “检查 Chinglish、逻辑、LaTeX、引用、匿名泄露”

默认输出：

- `*-revised.tex`：保留红线修改。
- `*-final.tex`：干净终稿。
- `review.md`：中文关键问题报告。

## 推荐使用顺序

### 从零搭一篇顶会论文

1. 用 `se-topconf-paper` 定论文类型、主线、RQ/EQ、贡献和图表计划。
2. 用 `se-topconf-introduction` 写 Introduction。
3. 先写 Method/Evaluation/Results，再回头压 Abstract。
4. 用 `se-topconf-conclusion` 写 Conclusion。
5. 用 `se-topconf-redline-review` 做最终错误检查。

### 已有草稿要冲顶会

1. 用 `se-topconf-paper` 做整篇诊断：主线、RQ、证据、贡献、图表、threats。
2. 分别用 `se-topconf-introduction` 和 `se-topconf-conclusion` 修首尾闭环。
3. 用 `se-topconf-paper` 检查图表和投稿政策。
4. 最后用 `se-topconf-redline-review` 做 LaTeX 红线审阅。

### 只改局部

- 只改引言：直接用 `se-topconf-introduction`。
- 只改结论：直接用 `se-topconf-conclusion`。
- 只做终稿审阅：直接用 `se-topconf-redline-review`。
- 不确定用哪个：用 `se-topconf-paper`。

## 安装方式

把下面四个文件夹复制到 Codex 可发现的 skills 目录中：

- `se-topconf-paper`
- `se-topconf-introduction`
- `se-topconf-conclusion`
- `se-topconf-redline-review`

如果你的 `$CODEX_HOME` 已设置，通常放到：

```text
$CODEX_HOME/skills/
```

如果未设置，通常放到：

```text
~/.codex/skills/
```

## 使用时建议给 Codex 的最小信息

为了避免模型乱编，请尽量给：

- 目标会议和年份：例如 ASE 2026、ICSE 2027。
- 论文类型：empirical study、tool paper、benchmark、security/testing paper 等。
- 论文题目或一句话主线。
- RQ/EQ。
- 数据集、模型、项目、实验规模。
- 关键结果和不能改的数据。
- 当前 LaTeX 主文件路径。
- 是否处于匿名提交阶段。

## 注意

如果要正式投稿，必须让 Codex 联网核对目标会议当年的最新 CFP、模板、页数、匿名、artifact 和 AI 使用披露政策。这个 skill 包里保留的是截至 2026-05-06 的调研快照和通用写作经验，不替代官方最新规则。
