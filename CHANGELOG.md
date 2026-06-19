# Changelog

变更记录遵循 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/) 格式，
版本号遵循 [语义化版本](https://semver.org/lang/zh-CN/) 规范。

## 版本策略

- `PATCH`：不破坏兼容性的 Bug 修复、文档更新
- `MINOR`：向后兼容的新功能、新球员接入
- `MAJOR`：破坏性变更，需要用户迁移

---

## [0.2.0-alpha] - 2026-06-19

> 📚 文档增强赛季 — 更完善的战术手册！

### Added

- **FAQ 常见问题（README 中英双语）**：新增面向新用户的常见问题解答区块，涵盖模型选择、Redis 要求、多用户支持等
- **架构说明优化**：补充架构三层原则的"负责/不负责"对比说明，使设计意图更清晰
- **ROADMAP v0.2.0 里程碑**：新增下一赛季详细里程碑计划，包括战术训练场可视化编辑器等
- **TIPS 工作效率提升**：补充高级使用技巧，包括 Antigravity AI 集成建议
- **AGENTS.md 完善**：补充 #1 门将（Quality Gate）的详细职责描述，以及 Antigravity AI 助手角色定位
- **design-system.md 补充**：新增阴影/高程系统规范和语义色值说明

### Changed

- **ROADMAP 进度更新**：将"本地全感知（Qwen）"从规划中更新为进行中，反映最新开发状态
- **双语文档同步**：中英文 README 同步补充 FAQ 区块和架构说明

---

## [0.1.0] - 2026-06-18

> 🏆 首个公开版本 — 球队集结完毕！

### Added

- **完整项目文档结构**：README（中英双语）、CONTRIBUTING、SECURITY、SUPPORT、SETUP、AGENTS、CHANGELOG
- **球员阵容定义**：
  - #10 队长 Leo（Claude）— 组织核心
  - #8 中场 André（GPT/Codex）— 引擎
  - #9 前锋 Flash（Gemini）— 灵感射手
  - #4 后卫 Wall（opencode）— 稳固磐石
- **球队铁律 (Fair Play Rules)**：四条不可违反的安全约定
- **主教练模式 (Head Coach Mode)**：人类作为战术决策者的角色定义
- **五大原则**：面向终场哨声、共创者非木偶、方向大于速度、唯一真相源、验证即完成
- **架构文档**：三层架构（模型层 / Agent CLI 层 / 平台层）
- **docs/ 文档目录**：
  - `docs/VISION.md` — 愿景：我们不缺球星，缺的是一支真正的球队
  - `docs/TIPS.md` — 赛场锦囊
  - `docs/ROADMAP.md` — 赛季计划
  - `docs/SOP.md` — 战术纪律手册
  - `docs/design-system.md` — 球队视觉识别系统
- **XI & You** 品牌理念：梦之队与你，一起征战，一起夺冠

[0.1.0]: https://github.com/loulanyue/dream-xi-ai/releases/tag/v0.1.0
