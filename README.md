English | [中文](./README_zh.md)

<p align="center">
  <a href="https://xpertai.cn/en/">
    <img src="docs/images/logo.png" alt="Xpert AI" width="240">
  </a>
</p>

<p align="center">
  <strong>Open-Source AI Platform for Enterprise Data Analysis, Indicator Management & Agent Orchestration</strong>
</p>

<p align="center">
  <a href="https://app.mtda.cloud/">XpertAI Cloud</a> •
  <a href="https://xpertai.cn/en/docs/getting-started/community/">Self-hosting</a> •
  <a href="https://xpertai.cn/en/docs/">Documentation</a> •
  <a href="https://xpertai.cn/en/#connect">Enterprise Inquiry</a>
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

**Xpert AI** is an open-source enterprise AI platform that seamlessly integrates agent orchestration with data analysis capabilities, empowering organizations to build intelligent workflows and derive actionable insights from their data.

## 💡 What's New

### 🚀 Version 3.8 — Agent Sandbox

XpertAI 3.8 introduces the **Agent Sandbox** feature, providing isolated execution and file operation environments for agents. The sandbox plugin's core capability is the **Provider Plugin Mechanism**, enabling integration with various runtime infrastructures:

- **Container Systems**: Docker / Podman
- **Cloud Sandboxes**: [Runloop](https://runloop.ai/), [Modal](https://modal.com/), [Daytona](https://daytona.io/)
- **Custom Infrastructure**: Remote VMs or secure sandbox services

## 🏗️ Agent-Workflow Hybrid Architecture

In today's rapidly evolving AI landscape, enterprises face a critical challenge: **How to balance LLM creativity with workflow stability?**

- **Pure Agent Architectures**: Flexible but difficult to control
- **Traditional Workflows**: Reliable but lack adaptability

Xpert AI's **Agent-Workflow Hybrid Architecture** resolves this conflict by enabling AI to exercise "free will" within "rule-based order."

![Agent-Workflow Hybrid Architecture](https://github.com/user-attachments/assets/b3b432f9-54ab-4ec1-9fc4-7e46fbfb88ba)

📖 [Blog: Agent-Workflow Hybrid Architecture](https://xpertai.cn/en/blog/agent-workflow-hybrid-architecture)

### 🤖 [Agent Orchestration Platform](https://xpertai.cn/en/docs/ai/)

Coordinate multiple intelligent agents to handle complex tasks through collaborative workflows. Xpert integrates diverse AI agent types via efficient management mechanisms, leveraging their combined capabilities to solve multidimensional problems.

![Xpert Agent](https://github.com/user-attachments/assets/e21f8b35-2f72-4b81-a245-f36759df7c27)

### 📊 [Data Analysis Platform](https://xpertai.cn/en/docs/models/)

A cloud-native agile data analysis platform featuring:

- **Multidimensional Modeling** — Build sophisticated data models
- **Metrics Management** — Define and track key performance indicators
- **BI Visualization** — Create interactive dashboards and reports

Connect to various data sources for efficient, flexible analysis and visualization, with intelligent tools to help enterprises uncover business value and make data-driven decisions.

## 🚀 Quick Start

### Prerequisites

| Requirement | Minimum Specification |
|-------------|----------------------|
| CPU | 2+ Cores |
| RAM | 4+ GiB |
| Node.js | 20.x or 22.x (ESM & CommonJS) |

### Installation with Docker Compose

The fastest way to get started is using [Docker Compose](docker/docker-compose.yaml). Ensure [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/install/) are installed:

```bash
git clone https://github.com/xpert-ai/xpert.git
cd xpert/docker
cp .env.example .env
docker compose up -d
```

Once running, access the Xpert dashboard at [http://localhost/onboarding](http://localhost/onboarding) to begin initialization.

📚 For development setup, see our [Wiki - Development](https://github.com/xpert-ai/xpert/wiki/Development).

## 💻 Demo & Production

### 🎮 Live Demo

Try Xpert AI Platform at **<https://app.mtda.cloud>**

> 💡 You can generate sample data from the home dashboard page.

### ☁️ Production (SaaS)

Xpert AI Platform SaaS is available at **<https://app.mtda.cloud>**

> ⚠️ Currently in Alpha / testing mode — use with caution in production environments!

## 🧱 Technology Stack

### Core Technologies

| Category | Technology |
|----------|------------|
| Language | [TypeScript](https://www.typescriptlang.org) |
| Backend | [Node.js](https://nodejs.org) / [NestJS](https://github.com/nestjs/nest) |
| Frontend | [Angular](https://angular.dev) / [RxJS](http://reactivex.io/rxjs) |
| Build | [Nx](https://nx.dev) |
| Database | [TypeORM](https://github.com/typeorm/typeorm) |
| AI/LLM | [LangChain](https://js.langchain.com/) |
| Visualization | [ECharts](https://echarts.apache.org/) |
| OLAP | [Java](https://www.java.com/) / [Mondrian](https://github.com/pentaho/mondrian) |

### Recommended for Production

- **Database**: [PostgreSQL](https://www.postgresql.org)
- **Process Manager**: [PM2](https://github.com/Unitech/pm2)

## 🗺️ Roadmap

### SDK

- [ ] [SDK (TypeScript)](https://github.com/xpert-ai/xpert-sdk-js)
  - [x] Digital Experts
  - [x] Long-term Memory Storage
  - [x] Contextual Files
  - [x] Conversation Management
  - [ ] Knowledge Bases
- [ ] [SDK (Python)](https://github.com/xpert-ai/xpert-sdk-py)

### Plugins

- [x] Plugin System
- [x] Marketplace for Plugin Ecosystem
- [x] Hot-swappable Plugins

### Frontend Components

- [ ] **ChatKit** — Frontend component library for embedding expert chat dialogs
  - [x] JavaScript Version
- [x] **Widgets** — UI widgets for richer LLM response experiences

### Agent Capabilities

- [x] **Agent Middlewares** — Plugin-based middleware system
- [x] **Agent Skills** — Lightweight skills for rapid capability integration
- [x] **Sandbox** — Secure isolated execution environment

### Enterprise Features

- [ ] **Audit, Security, Compliance**
  - [ ] Audit Logs
  - [ ] Role-based Access Control
  - [ ] Data Encryption

### Observability

- [ ] **Trace & Evaluation** — Tools for agent/workflow observability
  - [ ] Trace System
  - [ ] Evaluation Framework
- [ ] **Monitoring & Alerting**
  - [ ] Sentry Integration
  - [ ] Prometheus Integration

## 💌 Contact Us

- **Business Inquiries**: <mailto:service@xpertai.cn>
- **Twitter**: [@xpertai_cloud](https://x.com/xpertai_cloud)

## 🛡️ License

We support the open-source community. This software is available under multiple licenses:

| Edition | License |
|---------|--------|
| Community Edition | [AGPL v3](https://github.com/xpert-ai/xpert/blob/main/LICENSES.md#xpert-ai-platform-community-edition-license) |
| Enterprise Edition | [Commercial License](https://github.com/xpert-ai/xpert/blob/main/LICENSES.md#xpert-ai-platform-small-business-license) |
| Enterprise Pro Edition | [Commercial License](https://github.com/xpert-ai/xpert/blob/main/LICENSES.md#xpert-ai-platform-enterprise-license) |

📄 See [LICENSES.md](LICENSES.md) for detailed licensing information.

## 💪 Contributors

<a href="https://github.com/xpert-ai/xpert/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=xpert-ai/xpert" alt="Contributors" />
</a>

### How to Support

- ⭐ **Star us on GitHub** — It helps the project grow!
- 🐛 **Report Issues** — Submit feature requests or bug reports in [Issues](https://github.com/xpert-ai/xpert/issues)
- 🔧 **Contribute Code** — Pull requests are welcome! Please base PRs against the `develop` branch and follow our [Contributing Guide](.github/CONTRIBUTING.md).
