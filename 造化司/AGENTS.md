# AGENTS.md - 造化司入口

> 新媒体蜂群作战中心
> 
> 当用户说"造化司"或需要做内容时，读取此文件
> 
> 上位裁判：`00-行动中枢/Meta/系统文档/大罗天系统总控台.md`

---

## 快速启动

```
用户说"造化司"或进入新媒体执行任务
  → 读取系统总控台确认任务属于内容执行
  → 读取本文件
  → 匹配 skills/
  → 执行对应工作流
  → 过程写入 sessions/
  → 成品写入 output/ 并回链到 10-项目/
```

---

## 造化司是什么

造化司是新媒体操盘手的 AI 作战室，包含：

- **3 个内容 Skill**：追热点、选题口播、内容自动优化
- **4 个社区 Skill**：skill-creator、humanizer-zh、brainstorming、frontend-design
- **7 个规划中 Agent**：coordinator、account-strategy、content-producer、e-commerce、product-selling-points、compliance、data-review（当前 `agents/` 为空，尚未启用）
- **Memory Store**：只做新媒体任务索引和专用缓存，长期知识资产回到 `10-项目/` 或 `40-副脑/`

---

## 用户可能说的话 → 对应 Skill

| 用户说 | 调用 Skill | 说明 |
|-------|-----------|------|
| "追热点"、"蹭热点"、"这个热点能不能追" | hot-spot-content | 热点判断→找角度→写口播稿 |
| "选题"、"写个口播"、"这个选题怎么写" | topic-content | 选题分析→差异化→写口播稿 |
| "优化内容"、"迭代"、"深度打磨" | auto-optimize-content | 三角度迭代→对比合并→终稿 |
| "去AI味"、"润色"、"让内容更自然" | humanizer-zh | 社区skill，中文润色 |
| "头脑风暴"、"想点子"、"创意" | brainstorming | 社区skill，发散思维 |
| "设计"、"前端"、"页面" | frontend-design | 社区skill，前端设计 |

---

## 目录结构

```
造化司/
├── AGENTS.md              ← 你正在看的文件（入口）
├── CHANGELOG.md           ← 变更日志
├── README.md              ← 使用说明
├── 新媒体蜂群架构蓝图.md    ← 整体架构
├── agents/                ← Agent 角色定义（待创建）
├── skills/                ← 工作流
│   ├── auto-optimize-content/
│   ├── hot-spot-content/
│   └── topic-content/
├── memory/                ← 任务索引/专用缓存（不做长期知识副本）
├── sessions/              ← 任务产出
├── templates/             ← 模板
└── output/                ← 最终成品
```

---

## 执行规则

### 必须做
- 每次进入造化司，先读取本文件
- 执行前按系统总控台确认：这是内容生产任务，不是决策分析或知识库整理任务
- 执行前优先调用 `10-项目/示例项目/` 的项目事实和 `40-副脑/` 的通用模型
- 过程文件写入 `sessions/[日期]-[任务名]/`
- 最终成品复制到 `output/`
- 可长期复用的成品必须回链或复制到 `10-项目/示例项目/内容资产/`

### 禁止做
- 不把造化司当作平行知识库
- 不把 `memory/` 当作长期知识资产库
- 不跳过 Skill 流程直接写内容
- 不替代 `50-AI决策系统` 做复杂商业取舍判断

---

## 下一步

1. 用户说需求 → 匹配 Skill → 执行
2. 如果没有匹配的 Skill → 问用户想要什么
3. 如果是新任务 → 创建 sessions/[日期]-[任务名]/ → 开始

---

*本文件是造化司的入口，所有内容操作从这里开始。*
