# 支持 — 场边医疗站（Support）

## 如何获取帮助

本项目使用 GitHub Issues 追踪 Bug 和功能请求。在提交新 Issue 之前，请先搜索现有 Issues 避免重复。

### 快速自助参考

| 你的问题 | 推荐文档 |
|----------|----------|
| 首次安装和入门 | [SETUP.md](./SETUP.md) |
| 使用技巧 | [docs/TIPS.md](./docs/TIPS.md) |
| 战术纪律与工作流 | [docs/SOP.md](./docs/SOP.md) |
| 球队愿景 | [docs/VISION.md](./docs/VISION.md) |
| 贡献代码（加入球队） | [CONTRIBUTING.md](./CONTRIBUTING.md) |
| 安全漏洞报告 | [SECURITY.md](./SECURITY.md) |
| 赛季路线图 | [docs/ROADMAP.md](./docs/ROADMAP.md) |
| 球员角色说明 | [AGENTS.md](./AGENTS.md) |

---

## 提交 Bug 报告（伤病报告）

提交 Bug 时，请通过 [GitHub Issue](https://github.com/loulanyue/dream-xi-ai/issues/new) 提交，并尽量包含：

1. **环境信息（球场条件）**：
   ```bash
   node --version      # Node.js 版本
   pnpm --version      # pnpm 版本
   uname -a            # 操作系统
   redis-cli --version # Redis 版本（如使用）
   ```

2. **复现步骤（比赛回放）**：能触发问题的最小操作步骤

3. **期望行为（应该进的球）**：你认为应该发生什么

4. **实际行为（实际发生的犯规）**：实际发生了什么，包含完整的错误信息和日志

5. **临时解决方案（场上急救）**：如果你找到了 workaround，请一并描述

---

## 提交功能请求（转会申请）

欢迎新战术建议！请通过 [GitHub Issue](https://github.com/loulanyue/dream-xi-ai/issues/new) 提交，并描述：

- 该功能要解决的问题或使用场景
- 你设想的解决方案或接口设计
- 你考虑过的替代方案
- 对现有球队的影响（向后兼容性）

> [!NOTE]
> 重大功能（如新增球员位置、修改核心阵型）建议先通过 Issue 讨论达成共识，再提交 Pull Request。

---

## 项目维护状态

**Dream XI AI** 处于积极开发状态，由社区协作维护。

**响应时效参考（VAR 回放速度）**：

| 类型 | 目标响应时间 |
|------|-------------|
| 安全漏洞（红牌犯规） | 3 个工作日内确认 |
| Bug 报告（伤病报告） | 5 个工作日内初步回复 |
| 功能请求（转会申请） | 尽力而为，无固定 SLA |
| Pull Request（入队审批） | 7 个工作日内初步审查 |

---

## 贡献代码

如果你想直接加入球队贡献力量，请先阅读 [CONTRIBUTING.md](./CONTRIBUTING.md) 了解训练流程和球衣规范。
