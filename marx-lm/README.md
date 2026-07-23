# Marx LM —— 马列毛主义综合分析技能

[![License: MIT](https://img.shields.io/badge/License-MIT-red.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0-blue.svg)](https://github.com/gith-ub-cell/mel)

> "马克思的整个世界观不是教义，而是方法。它提供的不是现成的教条，而是进一步研究的出发点和供这种研究使用的方法。" —— 恩格斯

## 这是什么

Marx LM 是一个为 Claude Code 设计的**马列毛主义综合分析技能**，涵盖：

| 领域 | 内容 |
|------|------|
| **哲学** | 辩证唯物论、唯物辩证法、认识论、唯物史观 |
| **政治经济学** | 剩余价值理论、资本积累、利润率下降、AI 批判 |
| **科学社会主义** | 国家与革命、无产阶级专政、共产主义 |
| **批判方法论** | 27 种当代思潮的马克思主义批判 |
| **实践诊断工具** | 矛盾分析、阶段判断、项目诊断、阶级分析 |
| **经典文献** | 马恩列斯毛 104 部核心著作提要 |

它不只是讲理论——**它把马克思主义变成可操作的分析工具**，用于诊断项目问题、分析社会现象、进行理论批判。

## 安装

### 方法一：克隆到 Claude Code skills 目录

```bash
# 进入 Claude Code 技能目录
cd ~/.claude/skills

# 克隆本仓库为 marx-lm
git clone https://github.com/gith-ub-cell/mel.git marx-lm
```

### 方法二：直接下载

1. 下载本仓库 ZIP：[mel/archive/refs/heads/master.zip](https://github.com/gith-ub-cell/mel/archive/refs/heads/master.zip)
2. 解压到 `~/.claude/skills/marx-lm/`
3. 重命名文件夹为 `marx-lm`

## 使用

安装后，在 Claude Code 中通过 `/marx-lm` 调用，或直接说"调用 MarxLMskill"。

### 支持的场景

- **矛盾分析**：找主要矛盾、矛盾的主要方面、次要矛盾
- **项目诊断**：项目卡住了？从客观实际出发逐层诊断
- **阶级分析**：对任何社会现象做阶级视角的剖析
- **政治经济学批判**：分析剥削、异化、资本积累、AI 影响
- **思潮批判**：对技术决定论、自由主义、消费主义等做马克思主义批判
- **文艺批评**：用《在延安文艺座谈会上的讲话》评判影视文学作品
- **经典文献查询**：查找马恩列斯毛著作的核心论点

### 示例

```
调用 MarxLMskill，分析 AI 对当前劳动市场的影响

调用 MarxLMskill，用《讲话》评判电影《四渡》

调用 MarxLMskill，诊断当前项目的主要矛盾
```

## 文件结构

```
marx-lm/
├── SKILL.md                            # 主技能文件（行为指令）
├── README.md                           # 本文件
└── references/                         # 知识库（按需读取）
    ├── dialectical-materialism.md       # 辩证唯物论
    ├── epistemology.md                  # 认识论
    ├── historical-materialism.md        # 唯物史观
    ├── political-economy.md             # 政治经济学
    ├── scientific-socialism.md          # 科学社会主义
    ├── critique-methodology.md          # 批判方法论
    ├── practice-playbook.md             # 实践映射手册
    ├── classic-citations.md             # 经典引文汇编
    └── canonical-literature.md          # 经典文献提要（104部）
```

## 许可

MIT License

## 贡献

欢迎提交 Issue 和 PR。

---

*Made with ❤️ for dialectical materialism*
