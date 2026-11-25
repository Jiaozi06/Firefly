---
title: Asteria
published: 2026-11-25
draft: false
order: 100
description: 复刻 DeepSeek 安卓端界面与对话体验、通过 API 接入模型的原生 Android AI 客户端，支持本地对话管理和多渠道模型服务。
image: ""
status: published
tags: [Android, Java, AI, DeepSeek]
link:
  - label: GitHub
    icon: fa7-brands:github
    value: https://github.com/Jiaozi06/Asteria
  - label: APK 下载
    icon: material-symbols:download
    value: https://github.com/Jiaozi06/Asteria/releases
lang: zh_CN
---

## 项目简介

Asteria 是一款原生 Android AI 聊天客户端。项目从复刻 DeepSeek 安卓端界面与对话体验开始，通过 API 调用模型，不使用 DeepSeek 账号登录；随后扩展为可连接多种模型服务的本地优先应用。它不是 DeepSeek 官方应用。

## 主要功能

- **多模型和多协议：** 支持 DeepSeek、OpenAI、Anthropic、Gemini、Ollama 与自定义提供商，可分别保存接口地址、模型与协议。
- **流式聊天：** 支持 Markdown、代码高亮、表格、思考过程展示，以及编辑后重新发送消息。
- **上下文管理：** 按模型设置上下文窗口，支持自动压缩较早历史；遇到接口上下文超限时可缩减历史重试。
- **对话管理和导入：** 支持全文搜索、重命名、置顶、批量删除，以及导入 DeepSeek 导出链接或 ZIP 文件。
- **移动端能力：** 按接口能力提供图片与文件附件、联网搜索、语音转写和朗读；DeepSeek 官方接口还支持余额查询。
- **本地数据保护：** 聊天记录保存在应用私有目录，API Key 与代理凭据使用 Android Keystore 加密保存。

发送对话时，内容会发往用户设置的模型服务。使用 DeepSeek 的搜索、附件或语音转写功能时，相关内容也会发送到 DeepSeek；删除本地会话不会自动删除已上传到开放平台的附件。

## 安装和许可证

支持 Android 8.0 及以上版本。APK 与源码可从上方链接获取。当前仓库采用 PolyForm Noncommercial 1.0.0 许可证；商业用途需另行授权。此前以 MIT 发布的版本仍按各自版本附带的许可证执行。
