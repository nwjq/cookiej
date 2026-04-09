# 参与贡献 / Contributing

感谢你对 CookieJ 的关注！这是一个个人维护的开源项目，维护者时间有限，但非常欢迎社区贡献。

Thank you for your interest in contributing to CookieJ! This is a personally maintained project — contributions are welcome, though response times may vary.

## 如何贡献

### 报告 Bug

1. 先搜索 [已有 Issues](https://github.com/nwjq/cookiej/issues) 确认是否已报告
2. 使用 [Bug Report 模板](https://github.com/nwjq/cookiej/issues/new?template=bug_report.md) 创建 Issue
3. 尽量提供：Flutter 版本、设备信息、复现步骤、截图

### 提出功能建议

1. 使用 [Feature Request 模板](https://github.com/nwjq/cookiej/issues/new?template=feature_request.md) 创建 Issue
2. 说明你期望的行为和使用场景

### 提交 Pull Request

1. Fork 仓库并创建你的分支 (`git checkout -b feature/your-feature`)
2. 进行修改
3. 确保代码可以正常编译 (`flutter build apk --debug`)
4. 提交 PR，描述清楚改动内容和原因

### 当前最需要的贡献

以下方向特别欢迎贡献者参与：

- **Flutter 3.x / null safety 迁移** — 这是当前最高优先级的技术改进
- **依赖升级** — 将过时的包更新到最新兼容版本
- **测试补充** — 添加单元测试和 widget 测试
- **文档完善** — 代码注释、API 文档

## 开发环境

- Flutter SDK（项目当前基于 1.17.1 stable，迁移工作进行中）
- Dart SDK >=2.7.0 <3.0.0
- 微博开放平台 App Key（参见 [README](README.md#配置-api-凭证)）

## 代码风格

- 遵循 [Dart 官方风格指南](https://dart.dev/effective-dart/style)
- 提交信息建议使用：`type: 简要描述`（如 `fix: 修复首页刷新崩溃`）

## 行为准则

请保持友善和尊重。技术讨论欢迎不同观点，但请对事不对人。
