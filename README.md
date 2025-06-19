<div align="center">
  <img src="https://avatars.githubusercontent.com/u/210800337?u=9a7fedf901126afbc0338b728e5a4838127019f9&v=4" alt="PalyNext Logo" width="200"/>
</div>

<br/>

# PalyNext Platform

A modular, plugin-based project management and collaboration platform — designed to be extensible, scalable, and modern. Inspired by tools like Mattermost, Slack, and modern VCS-integrated systems.

## ✨ Features

- 🧩 Plugin-based architecture (Go + gRPC + Fiber)
- ⚡️ Dynamic webapp federation (Vite + React)
- 🔌 Runtime plugin discovery and loading
- 📦 Modular microservice deployment
- 💬 Chat, task management, API extensibility
- 🔍 Hot reload and live plugin development

## 🏗 Tech Stack

| Layer       | Technology                           |
|-------------|---------------------------------------|
| Backend     | Go, gRPC, Fiber, Hashicorp go-plugin |
| Frontend    | Vite, React, Module Federation, TailwindCSS, ShadCN UI |
| DevOps      | Makefile, Docker (optional), Node     |
| Plugins     | Hot-reloadable Go + React modules     |

## 🚀 Getting Started

### 1. Clone & Setup
```bash
git clone https://github.com/palynext/platform.git
cd platform
```

### 2. Build Plugins (Go + Web)
```bash
make build-plugin
```

### 3. Run Main Server
```bash
go run main.go
```

### 4. Run Web Host
```bash
cd webapp
npm install
npm run dev
```

## 📁 Project Structure

```
platform/
├── main.go                    # Main entrypoint for host server
├── plugins/                  # All plugin folders
│   └── pluginA/
│       ├── server/           # Go plugin
│       └── webapp/           # React plugin
├── webapp/                   # Host UI
└── internal/                 # Shared utilities and plugin interfaces
```

## 📦 Plugin Development

- Each plugin should implement:
  - `Init()` with metadata
  - gRPC interface (defined in `plugin.proto`)
  - Optional: `PluginEntry.tsx` if it has a frontend

## 🧠 Authors & Credits

- Developed by the PalyNext Team
- Inspired by open-source tools like Mattermost, Coolify, Gitea

## 📄 Licenses

This project uses multiple components with the following licenses:

- **PalyNext Platform Core**: MIT License
- **ShadCN UI**: MIT License
- **TailwindCSS**: MIT License
- **Hashicorp go-plugin**: MPL 2.0
- **Fiber**: MIT License
- **Vite**: MIT License
- **React**: MIT License
- **Docker** (if used): Apache 2.0

Please review individual libraries for their detailed license information.

## 🛣️ Roadmap

### Q3 2025
- [x] Plugin system for Go + gRPC
- [x] Dynamic React module federation
- [x] Plugin CLI: create, build, run
- [x] Middleware hook support (before/after)
- [x] Lifecycle events for plugins
- [ ] Centralized plugin marketplace UI

### Q4 2025
- [ ] Role-based access control
- [ ] Real-time chat + notification module
- [ ] Project/task management system
- [ ] External OAuth integration
- [ ] Embedded database support for plugins

### 2026 and beyond
- [ ] Cloud-native deployment templates
- [ ] Plugin dependency resolution
- [ ] Enterprise SSO and audit logging
- [ ] AI-assisted task flow & auto-tagging
