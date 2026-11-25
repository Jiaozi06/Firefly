---
title: 从 DeepSeek 安卓端体验到 Asteria：我的原生 AI 聊天客户端
published: 2026-11-25
description: 介绍 Asteria 的设计起点、多模型接入、对话管理，以及本地数据与密钥保护方式。
tags: [Asteria, Android, AI, DeepSeek]
category: 项目记录
author: 饺子
slug: asteria-android-ai-client
comment: true
---

# 从 DeepSeek 安卓端体验到 Asteria

Asteria 是我做的一款原生 Android AI 聊天客户端。项目从复刻 DeepSeek 安卓端的界面与对话体验出发，重点是通过 API 连接模型，而不是使用 DeepSeek 账号登录。它不是 DeepSeek 官方应用；DeepSeek 是 Asteria 支持的模型服务之一。随着开发推进，我也加入了多模型接入、本地对话管理和更灵活的上下文设置。

## 一个界面，连接不同模型

Asteria 支持 DeepSeek、OpenAI、Anthropic、Gemini、Ollama 和自定义提供商。不同服务可以分别保存接口地址、模型和调用协议，也可以手动切换协议。聊天采用流式回复，支持 Markdown、代码高亮、表格和可展开的思考过程。

## 把对话管理做在手机上

聊天记录保存在应用本地。侧栏支持按日期浏览、全文搜索、重命名、置顶和批量删除；已有 DeepSeek 对话可以从导出链接或 ZIP 文件导入。每个模型还可以单独设置上下文窗口，自动压缩较早的历史并保留最近的对话内容。

根据模型和接口能力，Asteria 还支持图片与文件附件、联网搜索、网页来源、语音转写和朗读。使用 DeepSeek 官方接口时，可以查看账户余额；也可以为提供商设置 SOCKS5 代理。

## 本地保存，也要知道数据会发往哪里

聊天历史保存在手机的应用私有目录，API Key 使用 Android Keystore 加密保存。发送消息时，当前对话内容仍会发往你所配置的模型服务以生成回复；使用 DeepSeek 的搜索、附件或语音转写等功能时，相关内容也会发送到 DeepSeek。删除本机对话不会自动删除已上传至开放平台的附件。

## 下载和源码

Asteria 支持 Android 8.0 及以上版本。当前发布版本为 **v2.19.1**，可以在 [GitHub Releases](https://github.com/Jiaozi06/Asteria/releases) 下载 APK，也可以查看 [源码仓库](https://github.com/Jiaozi06/Asteria)。项目使用 Java 和 Android SDK 构建。

当前仓库版本采用 PolyForm Noncommercial 1.0.0 许可证；商业用途需要另行获得授权。此前按 MIT 发布的旧版本仍遵循各自版本附带的许可证。

这是我持续迭代中的 Android 项目，欢迎到 GitHub 查看代码和更新。
