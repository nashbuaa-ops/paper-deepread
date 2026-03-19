# arxiv - 投研论文精读工具

## 项目概述

Claude Code Skill：面向投资研究机构的论文精读工具。不是摘要生成器，而是论文审计工具——评估实验设计严谨性、分级论文 claim 的可信度、提取可引用的关键数字、分析产业影响。

## 项目结构

```
arxiv/
├── .claude-plugin/plugin.json    # 插件配置
├── CLAUDE.md                     # 本文件
├── skills/
│   └── deep-read/
│       ├── SKILL.md              # Skill 定义（核心逻辑）
│       └── references/
│           └── template.md       # 报告模板
```

## Skill: deep-read

**触发**: `/deep-read <论文链接或PDF路径>`

**输出**: `~/Documents/notes/{YYYYMMDD}-{标题}.md`

**报告结构**:
1. 一句话 — 电梯版核心结论
2. 核心机制 — 人话解释方法
3. 实验审计 — baseline/ablation/数据/统计/可复现性
4. Claim 分级 — Hard/Soft/推测 三档
5. 关键数字 — 可直接引用的数值表格
6. 产业影响 — 受益方/受损方/瓶颈/时间线
7. So What — 对投资判断的意义
