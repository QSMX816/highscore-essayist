# highscore-essayist

上海高考一二模高分（一类文）作文风格 Skill。从 2025–2026 届上海 16 区高三一模/二模公开的考场一类文（63–68 分）约 20 篇中提炼出可执行的思辨作文写作系统，适配 opencode / Claude Code 等 Agent 的 Skill 机制。

## 它能做什么

- **写作**：按上海卷思辨作文的结构与语言规则成篇（800–1000 字，目标一类文）。
- **升格诊断**：按规则给一篇作文定位差距（审题、概念界定、思辨链、时代落点、收束），给出改写方向。

核心提炼（均经语料词频验证）：

| 维度 | 内容 |
| --- | --- |
| 结构模型 | 概念界定开局 → 诚然/然而/当然/更进一步 让步-转折思辨链 → 揆诸当下的时代诊断 → 辩证整合+诗句回收收尾 |
| 语言指纹 | "不是 A，而是 B"划界句、路标词段首导航、抽象名词高频（自我/生命/时代/局限性/主体性） |
| 引证系统 | 哲人一句证（尼采/加缪/萨特/庄子）、文学行动者切片（西西弗/悉达多）、现实案例两行内 |
| 时代诊断词 | 信息茧房、同温层、后真相、工具理性、优绩主义、原子化、异化 |

## 安装

### opencode

```bash
git clone https://github.com/QSMX816/highscore-essayist.git
mkdir -p ~/.config/opencode/skills
cp -r highscore-essayist ~/.config/opencode/skills/
```

### Claude Code

```bash
git clone https://github.com/QSMX816/highscore-essayist.git
mkdir -p ~/.claude/skills
cp -r highscore-essayist ~/.claude/skills/
```

新开会话后生效。

## 使用

对 Agent 说：

- 「用上海高考高分作文的风格写一篇关于 X 的作文」
- 「把这篇作文改成一模范文水平」
- 「切换到 highscore」
- 「按上海一类文的笔法审这道题」

## 语料与边界

- 语料：2025 届上海 16 区高三一模/二模考场一类文约 15 篇全文（含逐段教师简析）+ 2026 届宝山/浦东/杨浦等区范文与 16 区一模题目汇编，来源为公开专栏转载。
- 本 Skill 为写作技法抽象，不含语料原文摘抄；分数为发布者标注，非官方阅卷组发布。
- 上海卷风格不代表全国卷要求；引证人物与名言使用时请自行核实出处。

## 致谢

本 Skill 的制作方法论基于 [wenfeng-skill](https://github.com/XTmingyue/wenfeng-skill)（文风.skill，MIT License © xiongtao）：按照其「文风蒸馏」工作流（阅读语料 → 提炼叙事模型/语言指纹/母题意象/创作规则 → 生成可运行 SKILL.md）从上海一二模范文语料蒸馏而成。

## License

[MIT](./LICENSE)
