# openclaw-ocm

一个基于菜单的 OpenClaw 一键管理脚本（安装 / 配置 / 启停 / 日志 / 通道 / 大模型），主打“开箱即用、一气呵成”。

A menu-driven one-click manager script for OpenClaw (install / configure / start/stop / logs / channels / models), designed to be quick and practical.

---

## 快速开始 / Quick start (one-liner)

```bash
wget -O ocm.sh https://raw.githubusercontent.com/ttbb1211/openclaw-ocm/main/ocm.sh && bash ocm.sh
功能简介 / What it does

• 安装 OpenClaw（通过 npm -g openclaw@latest）
• 创建/更新配置：~/.openclaw/openclaw.json
• 启动/停止/重启 OpenClaw Gateway（优先走 systemd user service）
• 快捷添加/管理大模型 Provider（预设 + 自定义 BaseURL）
• 管理 Channel（Telegram Bot 等）
• 常用运维工具：健康检查、查看日志、设备配对/批准等

───

安全提示 / Security notes

• 不要在截图/日志里泄露任何密钥：API Key、Bot Token、Gateway Token、Clawhub Token 等。
• “查询 Gateway Token”界面默认打码显示（可交互选择是否显示完整 token）。
• 建议保持网关绑定 loopback (127.0.0.1)，除非你明确理解暴露到公网/LAN 的风险。

───

环境要求 / Requirements

• Linux + bash
• curl、jq（脚本会尝试自动安装）
• node + npm（用于安装 OpenClaw）

───

仓库文件 / Repo layout

• ocm.sh — 主脚本 / main script

───

免责声明 / Disclaimer

请先阅读脚本内容再运行，尤其是在生产环境或公网服务器上。

Review the script before running, especially on production/public servers.
