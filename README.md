**Nezha Telegram Bot - NextGen V1** 是一个基于 Nezha 监控 API，用于监控服务器状态的 Telegram 机器人。通过简单的命令，您可以实时查看服务器的运行状态、资源使用情况、执行计划任务以及监控服务可用性。

## 📋 特性

- **账号绑定**：安全绑定您的 Nezha 账户，确保数据隐私。
- **服务器概览**：查看所有服务器的在线状态、内存使用、交换空间、磁盘使用、网络流量等统计信息。
- **单台服务器状态**：获取单个服务器的详细状态信息，包括负载、CPU 使用率、内存、磁盘、网络流量等。
- **计划任务管理**：查看并执行预设的计划任务，自动化管理服务器。
- **服务可用性监测**：监控服务的可用性和平均延迟，确保服务稳定运行。
- **数据刷新**：实时刷新数据，确保您获取到最新的服务器状态。

## 🚀 快速开始

### 📦 前提条件

在开始之前，请确保您已经具备以下条件：

- 已安装Docker、Docker Compose
- Telegram 账号
- 已安装哪吒监控 Dashboard 并完成配置
- Telegram 机器人 Token（通过 [BotFather](https://t.me/BotFather) 获取）

### 🔧 快速安装

直接使用下方代码一键安装，安装目录在/opt/nezha-telegram-bot（记得替换`{此处填写你的Telegram 机器人 Token}`）
```
mkdir /opt/nezha-telegram-bot && cd /opt/nezha-telegram-bot && curl -L https://github.com/ClassmateShen/Nezha-Telegram-Bot-V1-Docker/raw/main/docker-compose-precompiled.yml -o docker-compose.yml && export TELEGRAM_TOKEN={此处填写你的Telegram 机器人 Token} && docker compose up -d
```

### 🧰 自行编译

直接使用下方代码一键执行自己编译，安装目录在/opt/nezha-telegram-bot（记得替换`{此处填写你的Telegram 机器人 Token}`和`{此处填写你的用户名（可随便填）}`）
```
mkdir /opt/nezha-telegram-bot && cd /opt/nezha-telegram-bot && git clone https://github.com/ClassmateShen/Nezha-Telegram-Bot-V1-Docker.git && export TELEGRAM_TOKEN={此处填写你的Telegram 机器人 Token} && export USERNAME={此处填写你的用户名（可随便填）} && docker compose up -d
```

## 🛠️ 使用指南

### 📌 绑定账号

为了确保您的数据安全，绑定账号仅支持私聊中进行操作。如果在群组中尝试绑定，机器人会提示您需在私聊中执行。

1. **私聊中发送 `/bind` 命令**。

2. **按照提示依次输入**：
   - 用户名
   - 密码
   - Dashboard 地址（例如：https://dashboard.example.com）

3. **绑定成功后**，您可以开始使用机器人的各项功能。

### 📜 可用命令

- `/start` - 启动机器人并显示欢迎信息。
- `/help` - 获取可用命令列表和简要说明。
- `/bind` - 绑定您的 Nezha 账户。
- `/unbind` - 解绑您的 Nezha 账户。
- `/overview` - 查看所有服务器的状态总览。
- `/server` - 查看单台服务器的详细状态。
- `/cron` - 执行计划任务。
- `/services` - 查看服务状态总览。

### 📊 服务器概览

使用 `/overview` 命令，可以查看所有绑定服务器的统计信息，包括在线状态、内存使用、交换空间、磁盘使用、网络流量等。您还可以通过点击“刷新”按钮实时更新数据。

### 🖥️ 单台服务器状态

使用 `/server` 命令，输入服务器名称进行搜索，并选择相应的服务器查看详细状态信息。包括负载、CPU 使用率、内存、磁盘、网络流量等数据。

### ⏰ 计划任务管理

使用 `/cron` 命令，可以查看并执行预设的计划任务。点击相应任务名称进行确认执行或取消操作。

### 🌐 服务可用性监测

使用 `/services` 命令，可以查看服务的可用性信息，包括可用率、当前状态、平均延迟和剩余流量等。


## 🙏 致谢

- [Nezha-Telegram-Bot-V1](https://github.com/nezhahq/Nezha-Telegram-Bot-V1) - Nezha Telegram Bot - NextGen V1 原生版本
- [python-telegram-bot](https://github.com/python-telegram-bot/python-telegram-bot) - 用于 Telegram 机器人的开发。
- [aiohttp](https://github.com/aio-libs/aiohttp) - 异步 HTTP 客户端/服务器框架。
- [aiosqlite](https://github.com/jreese/aiosqlite) - 异步 SQLite 连接库。
- [哪吒监控](https://nezha.wiki) - 哪吒服务器监控。
- [ChatGPT](https://chat.openai.com) - 本项目采用“面向 ChatGPT 编程”的理念，完成了包括本文档在内的 90% 的代码。
---

**免责声明**：使用本机器人时，请确保遵守相关法律法规。开发者不对因使用本机器人导致的任何损失承担责任。