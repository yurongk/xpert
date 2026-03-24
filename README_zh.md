[English](./README.md) | 中文

<p align="center">
  <a href="https://xpertai.cn/">
    <img src="docs/images/logo.png" alt="Xpert AI" width="240">
  </a>
</p>

<p align="center">
  <strong>开源企业级 AI 平台 — 数据分析、指标管理与智能体编排</strong>
</p>

<p align="center">
  <a href="https://app.mtda.cloud/">XpertAI 云</a> •
  <a href="https://xpertai.cn/docs/getting-started/community/">自托管</a> •
  <a href="https://xpertai.cn/docs/">文档</a> •
  <a href="https://xpertai.cn/#connect">企业咨询</a>
</p>

<p align="center">
  <a href="https://github.com/xpert-ai/xpert/" target="_blank">
    <img src="https://visitor-badge.laobi.icu/badge?page_id=meta-d.ocap" alt="Visitors">
  </a>
  <a href="https://www.npmjs.com/@metad/ocap-core">
    <img src="https://img.shields.io/npm/v/@metad/ocap-core.svg?logo=npm&logoColor=fff&label=NPM+package&color=limegreen" alt="ocap on npm" />
  </a>
  <a href="https://www.gnu.org/licenses/agpl-3.0.html" target="_blank">
    <img src="https://img.shields.io/badge/License-AGPL%20v3-blue.svg" alt="License: AGPL v3">
  </a>
  <a href="https://gitpod.io/#https://github.com/xpert-ai/xpert" target="_blank">
    <img src="https://img.shields.io/badge/Gitpod-Ready--to--Code-blue?logo=gitpod" alt="Gitpod Ready-to-Code">
  </a>
</p>

**Xpert AI** 是一个开源的企业级 AI 平台，无缝融合智能体编排与数据分析能力，助力企业构建智能工作流，从数据中获取可执行的业务洞察。

## 💡 新功能

### 🚀 3.8 版本 — 智能体沙箱

XpertAI 3.8 正式发布**智能体沙箱**功能，为智能体提供隔离的执行与文件操作环境。沙箱插件的核心能力是 **Provider 插件机制**，支持接入多种运行时基础设施：

- **容器系统**：Docker / Podman
- **云端沙箱**：[Runloop](https://runloop.ai/)、[Modal](https://modal.com/)、[Daytona](https://daytona.io/)
- **自定义基础设施**：远程虚拟机或安全沙箱服务

## 🏗️ 智能体与工作流混合架构

在 AI 技术快速落地的今天，企业面临一个关键挑战：**如何平衡 LLM 的创造性与工作流的稳定性？**

- **纯智能体架构**：灵活但难以控制
- **传统工作流**：可靠但缺乏应变能力

Xpert AI 的**智能体与工作流混合架构**解决了这一矛盾，让 AI 在"规则秩序"中行使"自由意志"。

![智能体与工作流混合架构](https://github.com/user-attachments/assets/b3b432f9-54ab-4ec1-9fc4-7e46fbfb88ba)

📖 [博客：智能体与工作流混合架构](https://xpertai.cn/blog/agent-workflow-hybrid-architecture)

### 🤖 [智能体编排平台](https://xpertai.cn/docs/ai/)

通过协调多个智能体的协作，处理复杂任务。Xpert 通过高效的管理机制集成不同类型的 AI 智能体，利用其组合能力解决多维度问题。

![Xpert 智能体](https://github.com/user-attachments/assets/e21f8b35-2f72-4b81-a245-f36759df7c27)

### 📊 [数据分析平台](https://xpertai.cn/docs/models/)

云原生敏捷数据分析平台，核心功能包括：

- **多维建模** — 构建复杂的数据模型
- **指标管理** — 定义和追踪关键绩效指标
- **BI 可视化** — 创建交互式仪表盘和报表

连接多种数据源，实现高效灵活的分析与可视化，配合智能分析工具帮助企业发现业务价值，做出数据驱动的决策。

## 🚀 快速开始

### 环境要求

| 要求 | 最低配置 |
|------|----------|
| CPU | 2 核以上 |
| 内存 | 4 GiB 以上 |
| Node.js | 20.x 或 22.x（支持 ESM 和 CommonJS）|

### 使用 Docker Compose 安装

最快捷的启动方式是使用 [Docker Compose](docker/docker-compose.yaml)。请确保已安装 [Docker](https://docs.docker.com/get-docker/) 和 [Docker Compose](https://docs.docker.com/compose/install/)：

```bash
git clone https://github.com/xpert-ai/xpert.git
cd xpert/docker
cp .env.example .env
docker compose -f docker-compose-cn.yml up -d
```

启动后，访问 [http://localhost/onboarding](http://localhost/onboarding) 开始初始化流程。

📚 开发环境配置请参考 [Wiki - 开发](https://github.com/xpert-ai/xpert/wiki/Development)。

## 💻 演示与生产环境

### 🎮 在线演示

访问 **<https://app.mtda.cloud>** 体验 Xpert AI 平台

> 💡 您可以在首页仪表盘生成示例数据。

### ☁️ 生产环境（SaaS）

Xpert AI 云平台地址：**<https://app.mtda.cloud>**

> ⚠️ 当前处于 Alpha / 测试阶段，生产环境请谨慎使用！

## 🧱 技术栈

### 核心技术

| 类别 | 技术 |
|------|------|
| 编程语言 | [TypeScript](https://www.typescriptlang.org) |
| 后端框架 | [Node.js](https://nodejs.org) / [NestJS](https://github.com/nestjs/nest) |
| 前端框架 | [Angular](https://angular.dev) / [RxJS](http://reactivex.io/rxjs) |
| 构建工具 | [Nx](https://nx.dev) |
| 数据库 | [TypeORM](https://github.com/typeorm/typeorm) |
| AI/LLM | [LangChain](https://js.langchain.com/) |
| 可视化 | [ECharts](https://echarts.apache.org/) |
| OLAP 引擎 | [Java](https://www.java.com/) / [Mondrian](https://github.com/pentaho/mondrian) |

### 生产环境推荐

- **数据库**：[PostgreSQL](https://www.postgresql.org)
- **进程管理**：[PM2](https://github.com/Unitech/pm2)

## 🗺️ 路线图

### SDK

- [ ] [SDK (TypeScript)](https://github.com/xpert-ai/xpert-sdk-js)
  - [x] 数字专家
  - [x] 长期记忆存储
  - [x] 上下文文件
  - [x] 会话管理
  - [ ] 知识库
- [ ] [SDK (Python)](https://github.com/xpert-ai/xpert-sdk-py)

### 插件系统

- [x] 插件系统
- [x] 插件市场
- [x] 热插拔插件

### 前端组件

- [ ] **ChatKit** — 嵌入式智能体聊天对话框前端组件库
  - [x] JavaScript 版本
- [x] **Widgets** — 让大模型响应驱动更丰富界面体验的 UI 组件

### 智能体能力

- [x] **智能体中间件** — 基于插件的中间件系统
- [x] **智能体技能** — 轻量级技能，快速集成定制能力
- [x] **沙箱** — 安全的隔离执行环境

### 企业级功能

- [ ] **审计、安全、合规**
  - [ ] 审计日志
  - [ ] 基于角色的访问控制
  - [ ] 数据加密

### 可观测性

- [ ] **追踪与评估** — 智能体/工作流可观测性工具
  - [ ] 追踪系统
  - [ ] 评估框架
- [ ] **监控与告警**
  - [ ] Sentry 集成
  - [ ] Prometheus 集成

## 💌 联系我们

- **商务合作**：<mailto:service@xpertai.cn>
- **Twitter**：[@xpertai_cloud](https://x.com/xpertai_cloud)
- **微信**：xpertai
- **飞书**：[加入我们](https://www.feishu.cn/invitation/page/add_contact/?token=d31n417e-fa7e-4e88-970c-15e502b6de0a)

## 🛡️ 许可证

我们支持开源社区。本软件提供多种许可方式：

| 版本 | 许可证 |
|------|--------|
| 社区版 | [AGPL v3](https://github.com/xpert-ai/xpert/blob/main/LICENSES.md#xpert-ai-platform-community-edition-license) |
| 企业版 | [商业许可](https://github.com/xpert-ai/xpert/blob/main/LICENSES.md#xpert-ai-platform-small-business-license) |
| 企业专业版 | [商业许可](https://github.com/xpert-ai/xpert/blob/main/LICENSES.md#xpert-ai-platform-enterprise-license) |

📄 详细许可信息请参阅 [LICENSES.md](LICENSES.md)。

## 💪 贡献者

<a href="https://github.com/xpert-ai/xpert/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=xpert-ai/xpert" alt="Contributors" />
</a>

### 如何支持我们

- ⭐ **在 GitHub 上 Star 我们** — 帮助项目成长！
- 🐛 **反馈问题** — 在 [Issues](https://github.com/xpert-ai/xpert/issues) 提交功能请求或 Bug 报告
- 🔧 **贡献代码** — 欢迎提交 Pull Request！请基于 `develop` 分支并遵循[贡献指南](.github/CONTRIBUTING.md)
