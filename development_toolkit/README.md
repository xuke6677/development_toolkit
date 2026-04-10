# 开发工具箱

基于 Electron 的桌面端开发工具箱，集成多种常用开发工具。

## 功能模块

- JSON格式化 — 格式化、压缩、校验、语法高亮、折叠展开、搜索、内联编辑、转义处理、Java Bean 转换，虚拟滚动支持大数据量
- 时间戳转换 — 当前时间戳显示、时间戳⇄日期时间互转、快捷选择当前日期/时间
- 翻译 — 中英文互译（MyMemory API）、简繁转换
- SQL拼接工具 — 批量值转 SQL IN 格式、去重、SQL格式化
- Cron生成器 — 可视化配置 Cron 表达式、反解析、最近运行时间预览
- 文本处理 — 去空格、去换行、去重、Unicode⇄中文转换

## 技术栈

- Electron 33.x
- 原生 HTML/CSS/JS（无框架依赖）
- electron-builder 打包构建

## 项目结构

```
development_toolkit/
├── main.js          # Electron 主进程
├── index.html       # 页面结构
├── renderer.js      # 渲染进程（JSON解析、虚拟滚动、搜索、编辑）
├── tools.js         # 工具页面逻辑（时间戳、翻译、SQL、Cron、文本处理）
├── styles.css       # 样式
├── package.json     # 项目配置与构建脚本
```

## 快速开始

> Node.js 安装在 `D:\nodejs`，需确保 PATH 包含该路径

### 安装依赖
```bash
set PATH=D:\nodejs;%PATH% && npm install
```

### 开发运行
```bash
set PATH=D:\nodejs;%PATH% && npm start
```

### 构建

```bash
# 构建为目录（免安装版）
set PATH=D:\nodejs;%PATH% && npm run build

# 构建为安装包（NSIS）→ 生成 开发工具箱 Setup x.x.x.exe
set PATH=D:\nodejs;%PATH% && npm run build:exe
```

构建产物在 `dist/` 目录下。

## 许可证

MIT
