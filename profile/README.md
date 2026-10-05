<div align="center">

# Full-Stack-Plugins

</div>


<p align="center">
  <strong>面向 AI Coding Agent 的研发过程插件生态 —— AI 设计工具 · 图表绘制 · 代码质量 · 服务器运维，Codex / ZCode / Kimi 三平台独立安装</strong>
</p>

<p align="center">
  <a href="https://github.com/partme-ai/full-stack-plugins"><img alt="Plugins" src="https://img.shields.io/badge/Plugins-9-green?style=flat-square"></a>
  <a href="https://github.com/partme-ai/full-stack-plugins"><img alt="Hosts" src="https://img.shields.io/badge/Hosts-Codex%20·%20ZCode%20·%20Kimi-blue?style=flat-square"></a>
  <a href="https://github.com/full-stack-plugins/.github/blob/main/LICENSE"><img alt="License" src="https://img.shields.io/badge/License-Apache_2.0-orange?style=flat-square"></a>
</p>

---

<!-- ecosystem-navigation:start -->

## 生态导航

按当前任务选择入口：技能提供可复用的知识与操作指引，插件连接工具与工作流。各项目可以独立使用，按需安装即可。

| 方向 | 适用任务 | 目录与安装 | 组织 |
| --- | --- | --- | --- |
| Full Stack Skills | 软件开发、架构设计、测试与运维 | [PartMe.AI / full-stack-skills](https://github.com/partme-ai/full-stack-skills) | [full-stack-skills](https://github.com/full-stack-skills) |
| Full AIGC Skills | 图像、视频、音频等内容创作 | [PartMe.AI / full-aigc-skills](https://github.com/partme-ai/full-aigc-skills) | [full-aigc-skills](https://github.com/full-aigc-skills) |
| Full Stack Plugins | 研发与运维的工具集成和工作流 | [PartMe.AI / full-stack-plugins](https://github.com/partme-ai/full-stack-plugins) | [full-stack-plugins](https://github.com/full-stack-plugins) |
| Full AIGC Plugins | 内容制作的工具集成和生成工作流 | [PartMe.AI / full-aigc-plugins](https://github.com/partme-ai/full-aigc-plugins) | [full-aigc-plugins](https://github.com/full-aigc-plugins) |

<!-- ecosystem-navigation:end -->

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
| --- | --- | --- | --- |
| 1Panel | [1panel-plugin](https://github.com/full-stack-plugins/1panel-plugin) | 0.1.1 | 通过官方 MCP 检查与管理 1Panel |
| BaoTa Linux Panel | [bt-linux-panel-plugin](https://github.com/full-stack-plugins/bt-linux-panel-plugin) | 1.0.6 | 通过 MCP 管理宝塔 Linux 面板 |
| CodeGraph | [codegraph-plugin](https://github.com/full-stack-plugins/codegraph-plugin) | 0.1.6 | 代码关系检索、影响分析与官方 CLI 工作流 |
| CodeGuard | [codeguard-plugin](https://github.com/full-stack-plugins/codeguard-plugin) | 0.18.3 | 代码规范检查与 Java 改动影响分析 |
| CodeReview | [codereview-plugin](https://github.com/full-stack-plugins/codereview-plugin) | 0.3.0 | 经用户授权审查待提交代码 |
| FlowGuard | [flowguard-plugin](https://github.com/full-stack-plugins/flowguard-plugin) | 0.4.2 | 智能体 SDD 治理：原生规格、证据与提交门禁 |
| Google Stitch Design | [stitch-design-plugin](https://github.com/full-stack-plugins/stitch-design-plugin) | 0.9.0 | 使用 Google Stitch 设计界面与构建前端 |
| ProcessOn Design | [processon-design-plugin](https://github.com/full-stack-plugins/processon-design-plugin) | 0.2.12 | 生成可编辑的 ProcessOn 流程图、架构图与思维导图 |
| UI Design | [ui-design-plugin](https://github.com/full-stack-plugins/ui-design-plugin) | 0.1.1 | 前端界面设计与图像素材生成 |

### 基础设施

| 仓库 | 说明 |
|------|------|
| [full-stack-plugins](https://github.com/partme-ai/full-stack-plugins) | 插件市场仓：catalog 单一事实源 + 三平台清单 + 发版工具 |

---

## 🚀 快速开始

插件市场清单由 [partme-ai/full-stack-plugins](https://github.com/partme-ai/full-stack-plugins) 统一发布：

Codex 用户请按[市场安装说明](https://github.com/partme-ai/full-stack-plugins#安装)在插件页面添加市场，并选择所需插件。

```text
# Kimi Code CLI
/plugins marketplace https://raw.githubusercontent.com/partme-ai/full-stack-plugins/main/kimi-marketplace.json
```

> ZCode：设置 → 插件 → 添加插件市场，输入 `partme-ai/full-stack-plugins`。

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

本组织下所有项目均采用 [Apache 2.0](../LICENSE) 开源许可协议。

---

<p align="center">
  <sub>Made with ❤️ by PartMe AI Team</sub>
</p>