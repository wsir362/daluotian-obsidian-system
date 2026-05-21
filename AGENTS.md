# AGENTS.md - 自进化系统入口

> ⚠️ **注意**：本文件已升级为「四层自进化系统」。
> 旧版内容已迁移到 `agent.md`（认知核心）和 `rules/`、`hooks/`、`subagent/`、`memory/` 目录。
> 新 AI 助手进入本项目时，请按以下顺序读取：
>
> 当前唯一工作库：`/Users/wsir/codex/大罗天`
> 旧库 `/Users/wsir/Downloads/大罗天` 仅作为迁移备份，不再写入。

---

## 必读文件顺序

1. **`agent.md`** — 系统宪法（目标/边界/标准/思考顺序）
2. **`00-行动中枢/Meta/系统文档/大罗天当前工作源.md`** — 路径裁判（当前工作库和旧库边界）
3. **`00-行动中枢/Meta/系统文档/大罗天文件边界规则.md`** — 文件裁判（大罗天只存文档型知识文件，不存媒体素材）
4. **`00-行动中枢/Meta/系统文档/大罗天系统总控台.md`** — 调用裁判（任务进哪个系统、调用什么、写回哪里）
5. **`00-行动中枢/Meta/系统文档/大罗天变更控制协议.md`** — 修改裁判（系统级修改如何记录）
6. **`rules/sync-rules.md`** — 同步规则
7. **`rules/classification-rules.md`** — 分类规则
8. **`rules/archive-rules.md`** — 归档规则
9. **`00-行动中枢/Meta/memory/learned-rules.md`** — 已沉淀的习得规则 ⚠️
10. **`00-行动中枢/Meta/memory/corrections.md`**（最近 3 条）— 最近纠正
11. **`00-行动中枢/Meta/memory/observations.md`** — 系统性模式
12. **`subagent/planner.md`** — 规划者角色（复杂任务时）
13. **`subagent/validator.md`** — 验证者角色（批量操作后）
14. **`subagent/archivist.md`** — 归档者角色（docx/旧版处理）
15. **`subagent/executor.md`** — 执行者角色（文件操作）
16. **`hooks/pre-sync.md`** — 同步前钩子
17. **`hooks/post-sync.md`** — 同步后钩子
18. **`hooks/weekly-review.md`** — 每周复盘钩子
19. **`hooks/today-archive.md`** — 今日区归档钩子
20. **`00-行动中枢/Today/README.md`** — 今日区使用说明

---

## 快速启动

```
读取 agent.md → 读取当前工作源 → 读取文件边界规则 → 读取系统总控台 → 读取变更控制协议 → 读取 learned-rules → 判断任务入口 → 调用对应系统/工具 → 按写回裁判落盘 → 更新必要日志
```

## 最高裁判

- **任务调用**：以 `00-行动中枢/Meta/系统文档/大罗天系统总控台.md` 为准。
- **路径读写**：以 `00-行动中枢/Meta/系统文档/大罗天当前工作源.md` 为准。
- **文件边界**：以 `00-行动中枢/Meta/系统文档/大罗天文件边界规则.md` 为准。
- **系统修改**：以 `00-行动中枢/Meta/系统文档/大罗天变更控制协议.md` 为准。
- **具体文件分类**：以 `rules/classification-rules.md` 和 `rules/archive-rules.md` 为准。
- **用户纠错**：写入 `00-行动中枢/Meta/memory/corrections.md`，可复发问题再沉淀到 `learned-rules.md`。

## 目录结构总览

```
大罗天/
├── agent.md              ← 第一层：认知核心
├── rules/                ← 第二层：路径规则
│   ├── sync-rules.md
│   ├── classification-rules.md
│   └── archive-rules.md
├── hooks/                ← 第二层：自动触发
│   ├── pre-sync.md
│   ├── post-sync.md
│   └── weekly-review.md
├── subagent/             ← 第三层：角色分工
│   ├── planner.md
│   ├── validator.md
│   ├── archivist.md
│   └── executor.md
├── 00-行动中枢/
│   └── Meta/       ← 实际路径：00-行动中枢/Meta/
│       └── memory/       ← 第四层：记忆循环
│           ├── corrections.md
│           ├── observations.md
│           ├── learned-rules.md
│           └── evolution-log.md
└── ... (原有目录结构)
```

---

*本文件为入口指引，具体内容请读取上述各文件。*
*系统版本：V1.4（加入全局文件边界裁判）*
