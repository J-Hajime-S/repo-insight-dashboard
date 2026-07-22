# Repo Insight Dashboard

## 目标

用户输入一个 GitHub 仓库名称或链接后，可以快速了解这个仓库的基础信息、热度、技术语言和活跃度。

## 目标用户

- 想快速了解开源项目的求职者
- 想浏览 GitHub 项目的学习者

## 核心用户流程

1. 用户输入 owner/repo，例如 facebook/react。
2. 系统请求 GitHub 公开 API。
3. 页面展示仓库概览：
   - 仓库名称
   - 简介
   - 作者头像与名称
   - Star、Fork、Open Issues
   - 主语言、许可证、最近更新时间
4. 页面展示语言构成。
5. 用户可以收藏仓库。
6. 刷新页面后，收藏的仓库仍然存在。

## 必须处理的状态

- 首次打开页面时的空状态
- 正在加载
- 仓库不存在
- 网络错误
- GitHub API 请求过多/限流
- 仓库没有简介、许可证或主语言

## 不做什么

- 不做登录、注册和用户系统
- 不做 GitHub OAuth
- 不做后端和数据库
- 不提交 GitHub Token 或任何密钥
- 不做创建 Issue、PR 等写操作
- 不做复杂动画和多页面系统

## 技术栈

- React
- TypeScript
- Vite
- Tailwind CSS
- GitHub REST API
- localStorage
- 可选：TanStack Query、Recharts

## 成功标准

- 用户能成功搜索 facebook/react 和 microsoft/vscode。
- 手机宽度和桌面宽度下页面都可正常浏览。
- 加载、错误和空数据都有清楚提示。
- 收藏刷新后仍存在。
- 项目有公开 GitHub 仓库、README 和在线演示链接。
