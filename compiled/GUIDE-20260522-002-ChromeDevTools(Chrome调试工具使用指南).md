---
id: GUIDE-20260522-002
title: Chrome DevTools for Coding Agents
title_zh: Chrome DevTools for 编程助手使用指南
category: GUIDE
tags: [tool, frontend, testing, debugging, reference, opencode]
status: published
created: 2026-05-22
updated: 2026-05-22
summary: Official Chrome DevTools MCP server — lets AI agents control, inspect, and debug a live Chrome browser
source: https://developer.chrome.com/docs/devtools/agents/get-started
difficulty: intermediate
---

# Chrome DevTools for Coding Agents (Chrome DevTools 使用指南)

> 官方文档: https://developer.chrome.com/docs/devtools/agents/get-started
> 安装方式: `~/.config/opencode/opencode.jsonc` 中配置的 `chrome-devtools` MCP

## 简介

Chrome DevTools for agents 是 Google Chrome 官方推出的 MCP 服务器，让 AI 编程助手能**直接控制、检查、调试**一个真实的 Chrome 浏览器。

## 使用前提

需要 Chrome 以远程调试模式启动：

```powershell
# 先完全关闭所有 Chrome 窗口，然后运行：
"D:\Software\RunningCheeseChrome\App\chrome.exe" --remote-debugging-port=9222
```

> 端口 `9222` 已在你机器上配置好，每次使用前确保 Chrome 以调试模式运行即可。

## 核心能力

| 能力 | 说明 | 调用示例 |
|------|------|---------|
| Console 检查 | 查看页面 Console 日志和错误 | "看看这个页面有什么报错" |
| Network 检查 | 查看网络请求和响应 | "检查这个请求为什么失败" |
| Elements 审查 | 审查 DOM 元素和 CSS 样式 | "审查这个按钮的样式" |
| 截图 | 截取页面截图 | "截个图给我看看" |
| 页面导航 | 打开任意 URL | "打开 linux.do" |

## 对比 Playwright MCP

| 对比项 | Chrome DevTools MCP | Playwright MCP |
|--------|-------------------|----------------|
| 浏览器 | 你正在使用的 Chrome（真实环境） | 独立无头浏览器 |
| 登录态 | ✅ 直接用你的登录状态 | ❌ 需要额外导入 Cookie |
| 调试能力 | ✅ Console/Network/Elements | ❌ 只做操作交互 |
| 适用场景 | 调试线上 bug、复现问题 | 自动化测试、截图 |

## 使用方法

重启 opencode 后，直接对 AI 说：

```text
"帮我看看这个页面 Console 有什么报错"
"检查这个 Network 请求为什么失败"
"审查一下这个元素的 CSS 样式"
"打开 linux.do"
```
