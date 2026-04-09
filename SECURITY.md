# Security Policy

## 报告安全问题 / Reporting a Vulnerability

如果你发现本项目存在安全问题，请**不要**在公开 Issue 中报告。

请通过以下方式私下联系维护者：

- 微博私信：[@竹笋饼干](https://www.weibo.com/p/1005052294516673)
- 或在 GitHub 上创建 [Private Security Advisory](https://github.com/nwjq/cookiej/security/advisories/new)

我会在确认问题后尽快回应（维护者时间有限，感谢耐心）。

## 安全注意事项

- **API 凭证**：`assets/data/appkey.json` 包含微博开放平台凭证，已在 `.gitignore` 中排除。请确保不要将你的凭证提交到版本控制。
- **第三方依赖**：本项目部分依赖版本较旧，可能包含已知安全问题。依赖升级是 [Roadmap](ROADMAP.md) 中的优先事项。

## 范围

本安全策略适用于本仓库中的代码。对于微博开放平台 API 本身的安全问题，请联系新浪微博官方。
