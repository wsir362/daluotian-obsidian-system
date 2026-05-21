# 造化司 · 变更日志

> 记录每次更改，方便回溯

---

## 2026-05-14

### 跑通第一条内容闭环测试

- 创建 `sessions/2026-05-13-示例内容闭环测试/`
- 写入 `README.md`、`调用记录.md`、`终稿.md`
- 将成品暂存到 `output/文案/2026-05-14-示例内容闭环测试-终稿.md`
- 将长期项目资产回链到 `10-项目/示例项目/内容资产/选题库/闭环测试/2026-05-14-示例内容闭环测试-终稿.md`

### 测试结论

- 造化司作为新媒体执行器的路径跑通。
- 过程文件与成品文件已分离。
- 成品没有只留在 `output/`，已回到项目资产。

### 暴露问题

- 示例项目项目内存在多个“示例选题”版本，后续需要建立主稿/旧稿/测试稿的版本命名规则。

---

## 2026-05-13

### 对齐系统总控台
- 修正 `AGENTS.md`：造化司定位为新媒体执行器，不是平行知识库。
- 修正 `README.md`：`memory/` 改为任务索引/专用缓存，长期知识回到 `10-项目/` 或 `40-副脑/`。
- 修正 `新媒体蜂群架构蓝图.md`：标记为历史蓝图/规划稿，并以系统总控台为当前执行边界。
- 明确 `agents/` 当前为空，7 个 Agent 仍处于规划中，尚未启用。
- 明确内容生产过程写入 `sessions/`，成品写入 `output/`，长期资产需回链到 `10-项目/示例项目/内容资产/`。

### 待办
- [ ] 如需启用 Agent，先创建具体 prompt，再更新 README 状态。
- [ ] 为 `memory/` 建立索引模板，而不是复制长期知识。

---

## 2026-05-12

### 创建造化司目录结构
- 创建 `造化司/` 主目录
- 创建子目录：`agents/`、`skills/`、`memory/`、`sessions/`、`templates/`、`output/`
- 创建 `README.md` 使用说明
- 移入 `新媒体蜂群架构蓝图.md`

### 创建内容优化 Skill
- 创建 `skills/auto-optimize-content/`
- 包含：SKILL.md、program.md、5个docs、3个templates
- 功能：内容自动优化工作流（4个phase）

### 创建追热点 Skill
- 创建 `skills/hot-spot-content/`
- 包含：SKILL.md、3个docs、2个templates
- 功能：追热点口播（2小时内出稿）

### 创建选题口播 Skill
- 创建 `skills/topic-content/`
- 包含：SKILL.md、3个docs、2个templates
- 功能：选题口播（深度创作）

### 安装社区 Skill
- ✅ skill-creator（写skill的skill）
- ✅ humanizer-zh（去AI味，中文润色）
- ✅ brainstorming（头脑风暴）
- ✅ frontend-design（前端设计）
- ❌ office-hours（未找到）
- ❌ penpot-uiux-design（网络失败）
- ❌ playwright-cli（网络失败）
- ❌ agent rich（未找到）
- ❌ bb closer（未找到）

### 待办
- [ ] 写 Agent Prompt（6个）
- [ ] 填充 Memory Store（产品手册/爆款文案/平台规则）
- [ ] 跑通第一个 Session

---

*日志格式：日期 → 变更内容 → 待办*
