<div align="center">

# highscore-essayist

**从考场一类文里，提炼可复用的高分写法。**

<p>
  <a href="LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg"></a>
  <a href="https://agentskills.io"><img alt="Agent Skills" src="https://img.shields.io/badge/Agent%20Skills-Compatible-green"></a>
  <a href="#安装"><img alt="Skills" src="https://img.shields.io/badge/Skills-Portable-blue"></a>
</p>

<p>
  <strong>highscore-essayist 是上海高考思辨作文的风格快照。</strong>
</p>

<p>
  它从 2025–2026 届上海 16 区高三一模/二模公开的考场一类文（63–68 分）约 20 篇中，提炼结构模型、语言指纹、引证系统和创作边界，生成一个可直接调用的写作 <code>SKILL</code>。
</p>

<p>
  <a href="#它解决什么问题">它解决什么问题</a> ·
  <a href="#它蒸馏什么">它蒸馏什么</a> ·
  <a href="#安装">安装</a> ·
  <a href="#边界">边界</a>
</p>

</div>

---

## 它解决什么问题

一篇作文卡在二类文，常常能感觉"差点意思"，却很难说清楚：

- 立意有了，为什么就是不像一类文那么"思辨"？
- 素材背了一堆，为什么堆上去反而降分？
- 让步、转折、层进，到底该在哪个位置出现？
- 高分作文是句子像，还是骨架像？
- 能不能把这种写法变成一个可复用的写作 Skill？

**highscore-essayist 要做的，就是把这些模糊感觉变成可执行规则。**

它不摘抄范文，不复述考场原文，也不把一类文压缩成"万能模板"。

它只提炼一类文背后的 HOW：这些文章是怎么拿到 63 分以上的。

---

## 它蒸馏什么

highscore-essayist 不只提取表层"好词好句"。它把一类文语料拆成六层可执行规则：

| 层次 | 提取内容 | 目的 |
|---|---|---|
| 结构模型 | 概念界定开局、让步—转折思辨链、时代诊断、辩证收束 | 让新文章按同一套引擎运转 |
| 语言指纹 | 划界句式、路标词导航、抽象名词光谱、四字语密度 | 让文本气质稳定 |
| 引证系统 | 哲人一句证、文学行动者切片、现实案例两行化 | 让引用为论点作证 |
| 母题意象 | 两元关系、技术时代处境、有限与无限 | 让文章有内在精神轴线 |
| 论证推进 | 开篇、节奏、冲突、设问链、转场、收束 | 让规则能落到段落 |
| 风格边界 | 不可写、诚实边界、语料范围 | 防止套路化、空喊和误引 |

一个规则要进入最终 `SKILL.md`，至少要满足：

1. **复现性**：在多篇一类文中反复出现，并经词频统计验证。
2. **生成力**：能指导面对新题目时怎么写。
3. **排他性**：不是所有议论文都会用的普通建议。

---

## 安装

### 方式一：让 agent 安装

告诉你正在使用的 agent：

```text
帮我安装这个 skill：https://github.com/QSMX816/highscore-essayist
```

### 方式二：CLI 安装

```bash
npx skills add QSMX816/highscore-essayist
```

### 方式三：手动安装

把仓库 clone 到你使用的运行环境的 skills 目录：

```bash
mkdir -p <skills-dir>
git clone https://github.com/QSMX816/highscore-essayist <skills-dir>/highscore-essayist
```

opencode 用户默认目录为 `~/.config/opencode/skills/`，Claude Code 用户为 `~/.claude/skills/`。

### 方式四：直接粘贴

如果你的工具暂不支持自动加载 Skill，也可以把 `SKILL.md` 内容直接粘贴进对话。它本质是一份带 YAML frontmatter 的 Markdown 指令。

---

## 使用

### 按一类文风格成篇

```text
/highscore-essayist 用上海高考高分作文的风格，写一道关于"获取信息越多是否越聪明"的思辨作文
```

### 给作文升格诊断

```text
/highscore-essayist 把我这篇二类文改成一模范文水平，指出思辨链断在哪里
```

---

## 工作原理

### 1. 确认语料

只取公开的考场一类文与教师范文，标注届别、区县与分数，非官方语料一律注明。

### 2. 通读与抽样

全文通读约 20 篇，覆盖 2025/2026 届、一模与二模、十余个区县；辅以 30 余道真题还原题旨分布。

### 3. 提炼技法

从结构、语言、引证、母题、推进、边界六个维度提取规则。

### 4. 词频验证

对路标词、哲学引证、时代诊断词做定量统计，只保留高频复现的指纹。

### 5. 生成 Skill

输出一个可安装、可调用、可继续写作的目标 `SKILL.md`。

---

## 边界

本仓库只提供写作技法，不包含任何受版权保护的范文原文。

语料为公开专栏转载的考场作文与解析，分数为发布者标注，非官方阅卷组发布；2026 届公开全文范文较少，归纳以 2025 届为主。

highscore-essayist 不是阅卷标准，也不保证复现阅卷现场；上海卷风格不代表全国卷要求，引证人物与名言使用时请自行核实出处。

它生成的是基于一二模范文的风格快照。

---

## 灵感来源

本项目使用 [XTmingyue/wenfeng-skill](https://github.com/XTmingyue/wenfeng-skill)（文风.skill，MIT © xiongtao）的蒸馏工作流生成，页面版式亦参考该项目。

---

## License

MIT
