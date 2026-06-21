# 术语表（Glossary）

Dream XI AI 使用足球隐喻来描述技术概念。本文档提供足球术语与技术术语的双向对照。

---

## 足球术语 → 技术术语

| 足球术语 | 技术含义 | 说明 |
|----------|----------|------|
| **球队 (Squad)** | AI Agent 集合 | 多个协同工作的 AI Agent 组成的团队 |
| **主教练 (Head Coach)** | 人类用户 | Dream XI 的核心决策者，提供愿景和最终判断 |
| **球员 (Player)** | AI Agent | 具有独立身份、职责和个性的单个 AI Agent |
| **阵型 (Formation)** | 路由配置 | 定义任务如何分发给不同球员的配置方案 |
| **比赛 / 场次 (Match)** | 会话 / 线程 | 一个独立的工作上下文，包含完整的对话历史 |
| **战术板 (Tactical Board)** | 线程 (Thread) | 隔离的上下文空间，每个功能一个战术板 |
| **传球 (Pass)** | A2A 消息传递 | Agent 之间的消息路由和任务交接 |
| **@mention 点名** | 定向路由 | 将消息路由给特定 Agent 的机制 |
| **更衣室 (Dugout)** | 控制面板 UI | 查看球员状态、战术、费用的管理界面 |
| **替补席 (Bench)** | 未激活 Agent | 因缺少 API Key 或暂时未使用的球员 |
| **热身 (Warmup)** | 设计阶段 | 功能开发前的技术方案制定阶段 |
| **进攻 (In-Play)** | 实现阶段 | 实际编码、执行的阶段 |
| **审查 (Review)** | 代码审查 | 跨 Agent 的代码质量检查阶段 |
| **进球 (Goal!)** | 功能完成 | 通过所有门禁检查、合并到主分支 |
| **门将 (Goalkeeper)** | 质量门禁 | 自动化最后防线，执行 `pnpm gate` |
| **门禁 (Gate)** | CI 质量检查 | 合并前的自动化检查（测试、Lint、类型检查等） |
| **红牌 (Red Card)** | P1 阻断问题 | 必须修复才能继续的严重问题 |
| **黄牌 (Yellow Card)** | P2 应修复问题 | 应该修复但不阻断合并的问题 |
| **角球 (Corner Kick)** | P3 建议 | 可选的改进建议，不影响合并 |
| **赛后复盘 (Post-Match)** | 回顾总结 | 功能完成后的经验沉淀和流程改进 |
| **VAR 回放** | 安全漏洞审查 | 对安全问题的仔细回溯分析 |
| **球队铁律 (Fair Play)** | 安全约束 | 不可违反的 AI Agent 行为边界 |
| **比赛记录 (Match Log)** | 持久化记忆 | 跨会话保存的上下文和决策历史 |
| **战术手册 (Playbook)** | Skills 框架 | 按需加载的专项能力模块（TDD、审查等）|
| **球衣规范 (Kit Rules)** | 代码风格规范 | TypeScript 严格模式、Biome lint、命名约定 |
| **转会市场 (Transfer Market)** | 集成/插件 | 接入新的 Agent CLI 或外部工具 |
| **青训营 (Academy)** | 自定义 Agent | 导入自有模型训练成球队成员 |
| **联赛模式 (League)** | 多项目管理 | 同时管理多个项目的统一视图 |
| **终场哨声 (Final Whistle)** | 发布/上线 | 功能最终交付给真实用户 |

---

## 技术术语 → 足球术语

| 技术术语 | 足球类比 |
|----------|----------|
| Multi-Agent Orchestration | 阵型与传球体系 |
| Agent-to-Agent (A2A) | 队员间传球 |
| Persistent Identity | 球员号码与角色 |
| Context Compression | 上下文压缩 = 球员失忆风险 |
| MCP (Model Context Protocol) | 统一球场通信频道 |
| Redis | 比赛记录数据库（数据圣殿） |
| Thread Isolation | 战术板隔离（一线程一比赛） |
| Cross-Model Review | 跨位置审查制度 |
| SOP Guardian | 球队纪律委员会 |
| Self-Evolution | 球队训练后的能力成长 |
| Head Coach Mode | 人类主教练模式 |
| Tactics Framework | 专项技能战术库 |

---

## 球员编号对照

| 编号 | 球员名 | 技术实体 | 核心职责 |
|------|--------|----------|----------|
| **#10** | Leo（里奥） | Claude (Opus/Sonnet/Haiku) | 架构设计、复杂推理、战术规划 |
| **#8** | André（安德） | GPT / Codex | 代码审查、安全分析、测试覆盖 |
| **#9** | Flash（弗拉什） | Gemini | 创意设计、快速原型、灵感突破 |
| **#4** | Wall（沃尔） | opencode（多模型） | 基础设施、兜底执行、多位置适配 |
| **#1** | 门将（Quality Gate） | CI 自动化 | 质量门禁、合并检查、最后防线 |

---

*「一支好球队，每个人都知道自己的位置——也知道每个术语背后的含义。」*
