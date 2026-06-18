# 赛前热身 — 安装部署指南（Setup Guide）

本指南帮助你完成 Dream XI AI 的完整安装和配置，从零到开球。

---

## 目录

- [环境要求](#环境要求)
- [方式一：桌面安装器](#方式一桌面安装器推荐)
- [方式二：源码安装](#方式二源码安装)
- [配置 API Key](#配置-api-key)
- [Redis 配置](#redis-配置)
- [验证安装](#验证安装)
- [常见问题](#常见问题)

---

## 环境要求

| 组件 | 版本要求 | 说明 |
|------|----------|------|
| Node.js | 20+ | JavaScript 运行时 |
| pnpm | 9+ | 包管理器 |
| Git | 2.x+ | 版本控制 |
| Redis | 7+（可选） | 持久化存储，可用 `--memory` 模式跳过 |

### 验证环境

```bash
node --version   # 应输出 v20.x.x 或更高
pnpm --version   # 应输出 9.x.x 或更高
git --version
```

---

## 方式一：桌面安装器（推荐）

如果 [Releases 页面](https://github.com/loulanyue/dream-xi-ai/releases) 有桌面安装包：

### Windows

1. 下载 `.exe` 安装器
2. 运行安装器
3. 从桌面快捷方式或开始菜单启动 Dream XI AI

### macOS

1. 下载 `.dmg` 文件
2. 将应用拖入 Applications（应用程序）
3. 首次打开时，右键点击应用 → 选择"打开"（绕过 Gatekeeper）

### Linux

暂无桌面安装器，请使用源码安装方式。

> 桌面安装器内置了应用运行时、便携 Node.js 和 Redis，普通用户**无需**运行 `pnpm install` 或 `pnpm build`。

---

## 方式二：源码安装

### 1. 克隆仓库

```bash
git clone https://github.com/loulanyue/dream-xi-ai.git
cd dream-xi-ai
```

### 2. 安装依赖

```bash
pnpm install
```

### 3. 构建所有包

```bash
pnpm build
```

> 首次启动前**必须**先构建。

### 4. 配置环境变量

```bash
cp .env.example .env
```

编辑 `.env` 文件配置基础设施参数。API Key 在启动后通过 UI 配置。

### 5. 开球！

```bash
pnpm start
```

### 后台运行（守门员模式）

```bash
pnpm start --daemon     # 后台启动
pnpm start:status       # 查看状态
pnpm stop               # 停止
```

### 一键安装（Linux）

```bash
bash scripts/install.sh
```

选项：`--start`（自动启动）、`--memory`（跳过 Redis）、`--registry=URL`（自定义 npm 镜像）

Windows 用户：使用 `scripts/install.ps1`，然后 `scripts/start-windows.ps1`。

---

## 配置 API Key

启动后打开 `http://localhost:3003`，进入 **更衣室 → 系统设置 → 账号配置**。

### 支持的模型提供商

| 提供商 | 球员 | 配置项 |
|--------|------|--------|
| Anthropic | #10 Leo (Claude) | `ANTHROPIC_API_KEY` |
| OpenAI | #8 André (GPT) | `OPENAI_API_KEY` |
| Google | #9 Flash (Gemini) | `GOOGLE_API_KEY` |
| 第三方（Kimi、GLM、MiniMax 等） | 替补球员 | 在 UI 中配置 |

> [!TIP]
> 至少配置一个 API Key 即可开始使用。不必一次配齐所有球员。

---

## Redis 配置

### 使用 Redis（推荐）

```bash
# macOS
brew install redis
brew services start redis

# Linux
sudo apt install redis-server
sudo systemctl start redis
```

### 不使用 Redis（内存模式）

```bash
pnpm start --memory
```

> [!WARNING]
> 内存模式下，重启后所有比赛记忆将丢失。仅建议用于本地测试。

---

## 验证安装

启动后，验证以下功能：

1. ✅ 打开 `http://localhost:3003` 能看到 Dream XI 界面
2. ✅ 进入更衣室能看到球员状态
3. ✅ 发送一条消息 `@leo 你好` 能收到队长回复
4. ✅ 检查终端日志无报错

---

## 常见问题

### `pnpm: command not found`

```bash
npm install -g pnpm
```

### `EACCES: permission denied`

```bash
# macOS/Linux
sudo chown -R $(whoami) ~/.pnpm-store
```

### 端口被占用

```bash
# 查找占用 3003 端口的进程
lsof -i :3003
# 杀死进程
kill -9 <PID>
```

### Redis 连接失败

确认 Redis 正在运行：
```bash
redis-cli ping   # 应返回 PONG
```

或使用内存模式：`pnpm start --memory`

---

更多问题请参考 [SUPPORT.md](SUPPORT.md)。
