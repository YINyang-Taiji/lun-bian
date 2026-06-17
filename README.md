---
AIGC:
    Label: "1"
    ContentProducer: 001191440300708461136T1XGW3
    ProduceID: 1ef3dd00febd39b403dab3406d83ed08_d9e8a163699711f1a99c5254007bceed
    ReservedCode1: CvzPuBfq5g6TPoecCFvWTJaRWy/KZ7+6itsk8eRVy6iTjoZfA88TlgtILNHeZnb9FA8iVtPyRuHUcgQ0THTAekJ6at0lFE6j4uTKxmGWWzE88KtttH0GlqCN/cZ1kogWgaP7G0LB5Nf+PT0kyuZ/AquP1c+gWsE4Y8uegK9UCNQAjzp/5TOxqBvhYvs=
    ContentPropagator: 001191440300708461136T1XGW3
    PropagateID: 1ef3dd00febd39b403dab3406d83ed08_d9e8a163699711f1a99c5254007bceed
    ReservedCode2: CvzPuBfq5g6TPoecCFvWTJaRWy/KZ7+6itsk8eRVy6iTjoZfA88TlgtILNHeZnb9FA8iVtPyRuHUcgQ0THTAekJ6at0lFE6j4uTKxmGWWzE88KtttH0GlqCN/cZ1kogWgaP7G0LB5Nf+PT0kyuZ/AquP1c+gWsE4Y8uegK9UCNQAjzp/5TOxqBvhYvs=
---



# Skill Forge | 从操作到 Skill——做一遍就学会

> 把你手头的操作变成可复用的 Skill——不用写一行 prompt。行为捕捉理解 + Darwin 自进化 + 鲁班打磨 + 一键多平台封装，一条龙全自动。

---

## 一句话定位

**Skill Forge** 是生成 Skill 的 meta-Skill。支持三种入口——行为流、需求描述、半成品打磨——覆盖从观察到交付的全链路。内置 Darwin 自进化评分循环、鲁班打磨工艺、自动依赖检测安装、多平台封装。

## 三种入口

| 入口 | 场景 | 你会听到 |
|------|------|---------|
| **Phase 1-A 行为捕捉** | 说不清需求，但能手把手做一遍 | "请开始操作，完成后告诉我" |
| **Phase 1-B 需求直译** | 需求明确，一句话就能说清楚 | "明白，这是规格书，你看下" |
| **半成品打磨** | 已有 Skill 需要优化/扩展/发布 | "先验料，看看这料值不值得雕" |

## 六大锻造阶段

```
Phase 0 接活 ──→ Phase 1 识意 ──→ Phase 2 铸胚
                                     │
                                Phase 2.5 试刃 ←── 用户实测反馈循环
                                     │
                                Phase 3 淬火 ←── Darwin 自进化评分循环
                                     │
                                Phase 4 开刃 ←── 鲁班亮活（README + 出师证书）
                                     │
                                Phase 5 封箱 ←── 依赖安装 + 多平台封装
```

## 快速开始

直接在对话中说：

```
"帮我做一个 skill，它能自动整理桌面文件"
"我不知道怎么描述，你看我操作"
"打磨这个 skill"
"把刚才的操作做成 skill 并发布到 ClawHub"
```

Skill Forge 会自动识别入口，走完 0-5 完整锻造流程。

## 触发词

- `帮我做一个 skill` / `创建一个 skill` / `锻造一个 skill`
- `打磨这个 skill` / `优化我的 skill`
- `把操作做成 skill` / `把刚才的步骤变成 skill`
- `skill forge` / `封装这个 skill 发布`

## 锻造戒律（15 条）

1. 用户说不清需求时 → 自动切行为捕捉，不放弃
2. 跳过行为确认 → 禁止，推断可能完全错误
3. 跳过试刃直接进淬火 → 禁止，初版常有偏差
4. 试刃只给一个修正方案 → 禁止，必须 ≥2 个
5. 试刃修正不记录 → 禁止，每轮必须保存 deviation 报告
6. 淬火后不亮活 → 禁止，没有 README 无法传播
7. 亮活后不封箱 → 禁止，用户还得手动整理发布
8. 自评自改 → 禁止，必须独立子 Agent 评分
9. 依赖安装失败静默跳过 → 禁止，展示错误并提供手动方案
10. 为凑分堆冗余 → 禁止，触顶即停
11. 泄露凭据或私有路径 → 禁止，Phase 4/5 强制脱敏检查
12. 把 Runtime 写死 → 禁止，必须跨平台中立
13. 用户说"不对"时只改表面 → 禁止，深入偏差分析
14. 回滚用破坏性方式 → 禁止，必须保留日志
15. 回滚后不告知状态 → 禁止，必须展示当前版本位置

## 强制停手点（11 个）

以下节点必须暂停等用户确认，不可自主推进：

1. Phase 1-A 每轮行为推断后
2. Phase 2 铸胚完成，展示初版所有文件后
3. Phase 2.5 每轮偏差分析报告展示后
4. Phase 2.5 修正方案生成后（等待选择）
5. Phase 2.5 执行修正后（等待确认是否继续循环）
6. Phase 3.1 基线评估评分卡展示后
7. Phase 3.2 每个 skill 优化完成后
8. Phase 3.3 探索性重写提议时
9. Phase 2.5 / Phase 4 执行回滚前
10. Phase 5 封装完成，展示发布包后
11. 任何涉及高风险操作时

## 关键技术细节

- **行为捕捉**：五维度采集（鼠标轨迹/键盘输入/屏幕焦点/操作节奏/结果反馈），通过 `analyze_image` 和 `shell_executor` 实现
- **Darwin 自进化**：9维评分 + 棘轮保留（只有真正变好才保留）+ 每轮 ≤2 轮改进
- **鲁班打磨**：验料 → 过尺 → 慢刨 → 亮活 → 交活，配合三级回滚机制
- **多平台封装**：GitHub + ClawHub + skills.sh + UUmit + 通用 .zip

## 输出物

对于每个被锻造的 Skill，最终产出：

```
[skill-name]/
├── SKILL.md              # Skill 核心定义
├── README.md             # 完整 README + Showcase
├── test-prompts.json     # 测试用例
├── results.tsv           # Darwin 进化历史
├── scripts/              # 安装与打包脚本
├── assets/               # GIF + 截图
└── skill-forge-export.zip
```

## 兼容性

Skill Forge 产出的 Skill 确保 Runtime 中立，可在以下平台运行：
Claude Code / Codex / Cursor / OpenClaw / Hermes / Marvis / Workbuddy / Jiuwenswarm

## 许可证

MIT. 锻造出的 Skill 的许可证由用户自行选择。

---

*"做一遍，它就学会了。"*
*（内容由AI生成，仅供参考）*
*（内容由AI生成，仅供参考）*
