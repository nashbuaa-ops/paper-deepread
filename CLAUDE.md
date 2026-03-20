# paper-deepread — 投研论文精读

## 核心逻辑

**说了啥 → 靠不靠谱 → 影响多大 → 谁受影响 → 要不要动**

## Skill

**触发**: `/paper-deepread <论文链接或PDF路径>`

**输出**: `~/Documents/notes/{YYYYMMDD}-{标题}.md`

**报告结构**:
1. 说了啥 — 一句话核心结论
2. 核心机制 — 人话 + 类比拆解技术原理
3. 靠不靠谱 — 实验故事化 + Claim 分级（Hard/Soft/推测）+ 结果量级
4. 影响多大 — 突破性质 / 旧路线冲击 / 新瓶颈 / 跟进门槛
5. 谁受影响 — 价值链 / 公司映射 / 转化路径 / 跟踪信号
6. 要不要动 — 改变 / 待验证 / 未改变

报告顶部附推荐指数（1-5 星）。

## 项目结构

```
arxiv/
├── .claude-plugin/plugin.json
├── CLAUDE.md
├── README.md
└── skills/
    └── paper-deepread/
        ├── SKILL.md
        └── references/
            └── template.md
```
