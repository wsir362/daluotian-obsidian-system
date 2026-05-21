# Skill: auto-optimize-content

> 内容自动优化工作流：从选题到终稿的全流程
> 
> 适用场景：口播、视频号、小红书等内容创作

---

## 快速启动

```
1. 读取 program.md（最短路径指南）
2. 按 phase-01 → phase-04 顺序执行
3. 每个 phase 完成后，用对应 checklist 验收
4. 最终输出到造化司/output/
```

---

## 严格约束

### 必须做
- 每个 phase 产出物必须写入文件（不能只输出在聊天里）
- 每个 phase 完成后必须用验收清单检查
- 三角度 prompt 必须做一致性检查
- 内层迭代最多 5 轮，超过必须人工介入

### 禁止做
- 不跳过 phase-01 直接写内容
- 不在没有一致性检查的情况下进入内层迭代
- 不输出未经对比合并的终稿

---

## 工作流总览

```
phase-01 选题立项
    ↓ 产出：选题卡、目标用户画像、内容定位
    ↓ 验收：acceptance-checklist.md
phase-02 三角度 Prompt 设计
    ↓ 产出：3 个版本的 prompt（情绪版/数据版/悬念版）
    ↓ 验收：consistency-check.md
phase-03 内层迭代
    ↓ 产出：每个 prompt 版本迭代 2-5 轮
    ↓ 验收：每轮产出质量 ≥ 阈值
phase-04 对比合并 + 终稿
    ↓ 产出：comparison-table.md + 最终文案
    ↓ 验收：终稿验收清单
```

---

## 文件索引

| 文件 | 说明 |
|------|------|
| [program.md](program.md) | 最短路径指南（5分钟上手） |
| [docs/verifiability.md](docs/verifiability.md) | R1-R5 可验证性纪律 |
| [docs/phase-01-spec.md](docs/phase-01-spec.md) | 选题立项详细流程 |
| [docs/phase-02-prompts.md](docs/phase-02-prompts.md) | 三角度 prompt 设计 |
| [docs/phase-03-inner.md](docs/phase-03-inner.md) | 内层迭代规则 |
| [docs/phase-04-output.md](docs/phase-04-output.md) | 对比合并 + 终稿输出 |
| [templates/acceptance-checklist.md](templates/acceptance-checklist.md) | 验收清单 |
| [templates/consistency-check.md](templates/consistency-check.md) | 三角度一致性检查表 |
| [templates/comparison-table.md](templates/comparison-table.md) | 逐模块对比合并表 |

---

## 与蜂群系统的关系

本 skill 是 Coordinator（新媒体总监）的核心调度逻辑之一：

```
Coordinator 收到内容需求
    ↓
调用 auto-optimize-content skill
    ↓
phase-01：调产品卖点 Agent + 起号策略 Agent
phase-02：调内容生产 Agent（3个版本）
phase-03：内层迭代（内容生产 Agent 自迭代）
phase-04：调合规风控 Agent + Coordinator 拍板
    ↓
输出到造化司/output/
```

---

*本 skill 是造化司的核心工作流，所有内容产出都应走这个流程。*
