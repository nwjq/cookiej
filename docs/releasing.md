# 发布流程 / Release Process

CookieJ 的版本发布检查清单。

## 发布前检查

### 代码准备
- [ ] 所有目标改动已合并到主分支
- [ ] `flutter analyze` 无严重警告
- [ ] `flutter test` 通过
- [ ] 在目标设备上手动验证核心功能

### 版本号更新
- [ ] 更新 `pubspec.yaml` 中的 `version` 字段
  - 格式：`major.minor.patch+build`（如 `1.1.0+1`）
  - 遵循 [语义化版本](https://semver.org/)
- [ ] 更新 `CHANGELOG.md`：将 `[Unreleased]` 内容移到新版本号下，添加发布日期

### 构建验证
- [ ] `flutter build apk --release`（Android）
- [ ] `flutter build ios --release`（iOS，如适用）

## 发布步骤

1. 完成上述检查
2. 创建 Git tag：`git tag v{版本号}`
3. 推送 tag：`git push origin v{版本号}`
4. 在 GitHub 创建 Release（参考 [release-template.md](release-template.md)）
5. 上传构建产物（APK 等）

## 版本号约定

- **patch**（1.0.x）：Bug 修复、小幅改进
- **minor**（1.x.0）：新功能、非破坏性改动
- **major**（x.0.0）：重大架构变更、破坏性改动（如 Flutter 3.x 迁移）
