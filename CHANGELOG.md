# Changelog

本文件记录 CookieJ 的版本变更。格式参考 [Keep a Changelog](https://keepachangelog.com/)。

## [Unreleased]

### Added
- 项目文档体系：CONTRIBUTING.md、ROADMAP.md、CHANGELOG.md、SECURITY.md
- GitHub Issue 和 PR 模板
- 发布流程文档

### Changed
- README.md 全面更新：结构化重写，增加英文摘要、架构说明、贡献指南引用

## [1.0.5] — 历史版本

已实现的核心功能：

- 微博信息流浏览（首页、发现、消息）
- 用户主页与个人中心
- 图片浏览与视频播放
- 多主题切换
- 微博编辑/发布（部分）
- 本地数据缓存（Hive + SQLite）
- 登录授权（微博 OAuth）

技术特征：
- 基于 Flutter 1.17.1 stable 构建
- Redux 状态管理
- Dio 网络层 + Cookie 管理
- 50+ 数据模型
