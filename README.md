# Calculator Frontend

前后端分离计算器的独立前端仓库。使用原生 HTML、CSS、JavaScript 和 Fetch API。浏览器只负责输入、显示结果及操作历史；所有计算由后端完成。

## 目录

```text
index.html      页面结构
css/style.css   响应式布局与浅色/深色主题
js/app.js       API 请求、计算器按键和历史交互
codestyle.md    前端代码约定
```

## 功能

数字、四则运算、小数、括号、一元正负号输入；Enter 计算、Backspace 退格、Escape 清空；历史查询、搜索、删除单条和清空；错误提示与深色模式。历史只从后端 API 获取，`localStorage` 只保存主题。

## 本地运行与后端 API

在本目录运行 `python -m http.server 5500`，打开 `http://127.0.0.1:5500` 可查看页面。`js/app.js` 顶部的 `API_BASE` 默认为 `/api`；完整计算功能要求前端和 FastAPI 通过同一域名提供服务，并将 `/api/*` 路由到后端。课程作业的独立后端源码位于 [calculator-backend](https://github.com/lyweee859-arch/calculator-backend)；完整的同域本地运行及 Vercel 部署配置位于 [calculator-vercel](https://github.com/lyweee859-arch/calculator-vercel)。

如果单独部署本前端，需在托管平台配置 `/api/*` 反向代理到后端，或为单独的后端地址调整 `API_BASE` 和后端 CORS。纯静态服务器自身不执行计算。

**Deployment URL:** To be added after deployment.
