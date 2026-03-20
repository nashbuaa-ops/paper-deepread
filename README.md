# paper-deepread

投研论文精读 Skill for [Claude Code](https://claude.ai/claude-code)。

不是论文摘要生成器，而是**论文审计工具**——站在投资分析师的视角，评估实验可信度、分析技术格局变化、映射到具体公司和投资判断。

## 核心逻辑链条

**论文说了啥（一句话 + 核心机制） → 靠不靠谱（关键实验 + Claim 分级） → 影响多大（技术格局变化） → 谁受影响（投资映射） → 要不要动（So What）**

1. **说了啥**：这篇论文到底在讲什么？用人话和类比把技术翻译成投资人能理解的语言
2. **靠不靠谱**：实验设计严不严谨？每个结论是硬证据、软证据还是作者猜的？结果的量级够不够改变游戏规则？
3. **影响多大**：这个技术突破动了谁的奶酪？让谁的技术积累贬值？别人多快能追上？打开了什么新机会？
4. **谁受影响**：打到价值链哪一层？具体哪家公司的护城河被加强或削弱？从论文到影响财报最可能死在哪一步？
5. **要不要动**：三选一——改变 / 待验证 / 未改变，一句话说清影响哪些投资判断。

论文里的公式和术语对非专业研究的人不太友好，读起来比较晦涩，我习惯用类比的方式来理解技术逻辑和实验设计——重点讲清楚每个实验在验证什么机制、结果意味着什么，把一些相对生涩的术语转化成大家更好理解一点的语言。

## 安装

```bash
claude install-plugin /path/to/arxiv
```

或者用 GitHub 地址：

```bash
claude install-plugin https://github.com/<your-username>/arxiv
```

## 使用

在 Claude Code 中输入：

```
/paper-deepread https://arxiv.org/abs/2603.15031
```

支持以下输入格式：

| 输入 | 示例 |
|------|------|
| arxiv ID | `2603.15031` |
| arxiv 链接 | `https://arxiv.org/abs/2603.15031` |
| arxiv PDF | `https://arxiv.org/pdf/2603.15031` |
| alphaxiv 链接 | `https://www.alphaxiv.org/abs/2603.15031` |
| 本地 PDF | `/Users/me/Downloads/paper.pdf` |

## 输出示例

生成 Markdown 报告至 `~/Documents/notes/{YYYYMMDD}-{标题}.md`：

```markdown
# Attention Residuals

> **来源**: ... | **作者**: Kimi Team | **日期**: 2026-03-16

**推荐指数**: ⭐⭐⭐⭐ (4/5) | **判断变化**: 待验证

## 说了啥
## 核心机制
## 靠不靠谱
## 影响多大
## 谁受影响
## 要不要动
```

每篇报告顶部有推荐指数（1-5 星）和判断变化标签，方便团队排序和筛选。

## 报告结构

| 章节 | 对应逻辑 | 回答什么 |
|------|---------|---------|
| 说了啥 | 说了啥 | 一句人话概括 |
| 核心机制 | 说了啥 | 用类比拆解技术原理 |
| 靠不靠谱 | 靠不靠谱 | 实验故事 + Claim 分级 + 结果量级 |
| 影响多大 | 影响多大 | 突破性质 / 旧路线冲击 / 新瓶颈 / 跟进门槛 |
| 谁受影响 | 谁受影响 | 价值链 / 公司映射 / 转化路径 / 跟踪信号 |
| 要不要动 | 要不要动 | 改变 / 待验证 / 未改变 |

## 自定义

### 修改输出目录

编辑 `skills/paper-deepread/SKILL.md` 中的 L0 格式约束：

```
- **输出目录**: `~/Documents/notes/`
```

### 修改报告模板

编辑 `skills/paper-deepread/references/template.md`。

## 项目结构

```
arxiv/
├── .claude-plugin/plugin.json
├── CLAUDE.md
├── README.md
├── LICENSE
└── skills/
    └── paper-deepread/
        ├── SKILL.md              # Skill 定义（核心逻辑）
        └── references/
            └── template.md       # 报告模板
```

## License

MIT
