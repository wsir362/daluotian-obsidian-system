# Hook: Weekly Review · 每周复盘

> 触发条件：每周五（或用户主动要求"复盘"时）
> 作用：定期回顾 corrections 和 observations，提炼为 learned-rules

---

## 复盘流程

### Step 1：回顾本周纠正
- 读取 `00-行动中枢/Meta/memory/corrections.md` 本周新增条目
- 统计：本周纠正次数、主要问题类型分布

### Step 2：模式验证
- 读取 `00-行动中枢/Meta/memory/observations.md`
- 检查已有模式是否仍在重复发生
- 如果某模式连续 2 周未出现，标记为"已收敛"

### Step 3：规则提炼
- 从本周纠正中提炼可执行的规则
- 判断规则是否通用 enough（适用 ≥3 个场景）
- 写入 `00-行动中枢/Meta/memory/learned-rules.md`

### Step 4：系统健康度评估
- 纠正频率趋势（目标：逐周下降）
- learned-rules 触发次数（目标：逐周上升）
- 重复错误复发率（目标：=0）

### Step 5：更新 evolution-log
- 记录本周系统变化
- 评估是否需要版本升级

## 复盘输出模板

```markdown
## 2026-WXX 周复盘

**纠正统计**：本周新增 X 条纠正（上周 Y 条）→ 趋势：↑/↓/→
**主要问题类型**：
- 类型A：Z 次（根因：xxx）
- 类型B：W 次（根因：yyy）

**新提炼规则**：
- 规则 N：xxx（来源：correction #XX）

**已收敛模式**：
- 模式 X：连续 2 周未出现，标记为已解决

**系统健康度**：🟢/🟡/🔴
**下周重点**：xxx
```

## 自动化提醒

建议在 `00-行动中枢/Meta/用户上下文/本周聚焦.md` 中设置每周五提醒：
> 「周五 17:00 触发 weekly-review hook」
