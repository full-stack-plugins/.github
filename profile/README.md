# Full-Stack-Plugins

<p align="center">
  <strong>面向 AI Coding Agent 的研发过程插件生态 —— AI 设计工具 · 图表绘制 · 代码质量 · 服务器运维，Codex / ZCode / Kimi 三平台独立安装</strong>
</p>

<p align="center">
  <a href="https://github.com/full-stack-plugins"><img alt="Repos" src="https://img.shields.io/badge/Repos-6-blue?style=flat-square"></a>
  <a href="https://github.com/full-stack-plugins/full-stack-plugins"><img alt="Plugins" src="https://img.shields.io/badge/Plugins-4-green?style=flat-square"></a>
  <a href="https://github.com/full-stack-plugins/full-stack-plugins"><img alt="Hosts" src="https://img.shields.io/badge/Hosts-Codex%20·%20ZCode%20·%20Kimi-blue?style=flat-square"></a>
  <a href="https://github.com/full-stack-plugins/.github/blob/main/LICENSE"><img alt="License" src="https://img.shields.io/badge/License-Apache_2.0-orange?style=flat-square"></a>
</p>

---

## 🧭 关于本组织

**Full-Stack-Plugins** 是一个面向研发过程的插件生态，覆盖 **AI 设计工具、图表绘制、代码质量、服务器运维**，面向 **Codex、ZCode、Kimi Code** 三个宿主平台。

每个插件以独立仓库交付，内置三平台适配层（`.codex-plugin` / `.zcode-plugin` / `kimi.plugin.json`）与渐进式披露的 Agent Skills，提供从 **MCP 工具**到**门禁流水线**到**自动化运维**的可执行能力。

与姊妹组织 [Full-Stack-Skills](https://github.com/full-stack-skills) 对位：技能侧沉淀「怎么想」的领域知识，本组织提供「能做到」的插件能力——Stitch 对应技能侧的 stitch-skills，ProcessOn 对应 processon-skills，按同一套领域划分共建同一个生态。

### 核心理念

> **插件标准化封装（三平台 Manifest） · MCP 工具 · 渐进式披露技能**

---

## 📦 插件仓库

### 插件

| 插件 | 仓库 | 版本 | 说明 |
|------|------|:----:|------|
| 🎨 **Google Stitch 设计** | [stitch-design-plugin](https://github.com/full-stack-plugins/stitch-design-plugin) | 0.7.9 | 基于 Google Stitch 的设计与前端搭建 |
| 📊 **ProcessOn 图表** | [processon-design-plugin](https://github.com/full-stack-plugins/processon-design-plugin) | 0.2.2 | 生成可编辑的 ProcessOn 精美图表（流程图 / 架构图 / 思维导图） |
| 🔍 **代码规范守卫** | [codeguard-plugin](https://github.com/full-stack-plugins/codeguard-plugin) | 0.3.4 | 让 AI 写的代码一次通过 lint 门禁（多语言规则集） |
| 🛡️ **宝塔 Linux 面板** | [bt-linux-panel-plugin](https://github.com/full-stack-plugins/bt-linux-panel-plugin) | 1.0.2 | 通过 MCP 运维宝塔 Linux 面板 |

### 基础设施

| 仓库 | 说明 |
|------|------|
| [full-stack-plugins](https://github.com/full-stack-plugins/full-stack-plugins) | 插件市场仓：catalog 单一事实源 + 三平台清单 + 发版工具 |

---

## 🚀 快速开始

插件市场清单由 [full-stack-plugins/full-stack-plugins](https://github.com/full-stack-plugins/full-stack-plugins) 统一发布：

```bash
# Codex
codex plugin marketplace add full-stack-plugins/full-stack-plugins
codex plugin add codeguard@full-stack-plugins   # 其余插件同理
```

```text
# Kimi Code CLI
/plugins marketplace https://raw.githubusercontent.com/full-stack-plugins/full-stack-plugins/main/kimi-marketplace.json
```

> ZCode：设置 → 插件 → 添加插件市场，输入 `full-stack-plugins/full-stack-plugins`。

---

## 📁 插件结构规范

```
<plugin-repo>/
├── .codex-plugin/plugin.json     # Codex 适配
├── .zcode-plugin/plugin.json     # ZCode 适配
├── kimi.plugin.json              # Kimi 适配
├── skills/<skill>/SKILL.md       # 渐进式披露技能
└── assets/                       # Logo 与资源
```

---

## 🤝 贡献指南

1. **Fork** 对应插件仓库
2. 任何代码改动都要 bump + 发版（市场端靠版本号感知更新）
3. 提交 **Pull Request**，由市场仓统一重生成三平台清单

> 新插件提案请在 [Discussions](https://github.com/orgs/full-stack-plugins/discussions) 中发起。

---

## 📄 许可协议

本组织下所有项目均采用 [Apache 2.0](LICENSE) 开源许可协议。

---

<p align="center">
  <sub>Made with ❤️ by PartMe AI Team</sub>
</p>
