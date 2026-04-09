# 饼干微博 (CookieJ) — Flutter 微博客户端

> **A third-party Weibo client built with Flutter.** CookieJ demonstrates how to implement a long-form social media application using Flutter, integrating with the Sina Weibo Open Platform API. It covers feed browsing, user profiles, video playback, theming, and more — serving as both a usable client and a reference project for Flutter developers working with complex content-driven apps.

**Flutter 长图文社区应用的开源实践**

CookieJ 是一个使用 Flutter 开发的第三方微博客户端，接口基于[新浪微博开放平台](https://open.weibo.com/) API。UI 设计参考了 Smooth、Share 和微博国际版，结合个人偏好进行调整。

||||
|-|-|-|
![](screenshot/home.jpg)|![](screenshot/discovery.jpg)|![](screenshot/notice.jpg)
![](screenshot/user1.gif)|![](screenshot/user2.gif)|![](screenshot/video.jpg)
![](screenshot/personal.jpg)|![](screenshot/theme.jpg)|![](screenshot/edit.jpg)

## 功能概览 / Features

- **信息流浏览** — 首页、发现页、消息通知
- **用户主页** — 个人资料、微博列表、关注/粉丝
- **内容展示** — 长文、图片、视频播放
- **主题切换** — 多种主题色可选
- **编辑发布** — 微博撰写（部分功能）
- **本地缓存** — 图片缓存、数据持久化（Hive + SQLite）

> 注：由于新浪开放平台 API 权限限制，部分功能（如点赞、完整评论）尚未完全实现。

## 项目状态 / Project Status

CookieJ 是一个个人维护的开源项目，核心功能已实现并可运行。项目最初基于 Flutter 1.x / Dart 2.x 构建，**尚未迁移到 Flutter 3.x 和 null safety**。依赖升级和现代化迁移是当前最主要的技术待办事项。

欢迎对 Flutter 社区应用开发感兴趣的开发者参与贡献，尤其是在依赖升级、测试补充和代码现代化方面。

## 技术栈 / Tech Stack

| 类别 | 技术 |
|------|------|
| 框架 | Flutter (originally 1.17.1 stable) |
| 语言 | Dart (SDK >=2.7.0 <3.0.0) |
| 状态管理 | Redux (flutter_redux) |
| 网络 | Dio + Cookie 管理 |
| 本地存储 | Hive, SQLite (sqflite), SharedPreferences |
| 媒体 | video_player, audioplayers, cached_network_image |
| WebView | flutter_inappwebview |
| UI 组件 | pull_to_refresh, flutter_swiper, extended_image |

## 快速开始 / Getting Started

### 前置条件

1. 安装 Flutter SDK（项目当前需要 Flutter 1.x 通道，迁移到 Flutter 3.x 正在规划中）
2. 在[微博开放平台](https://open.weibo.com/apps)注册应用，获取 App Key、App Secret 和 Redirect URI

### 配置 API 凭证

获取微博开放平台凭证后，在项目根目录创建 `assets/data/appkey.json`：

```json
{
    "appkey": "你的 App Key",
    "appSecret": "你的 App Secret",
    "redirectUri": "你的回调地址"
}
```

> **注意：** `appkey.json` 已加入 `.gitignore`，请勿将你的凭证提交到版本控制。

### 编译运行

```bash
flutter pub get
flutter run
```

## 项目结构 / Architecture

项目采用 Redux 模式进行状态管理，按职责分层：

```
lib/cookiej/
├── action/        # Redux Actions（access、app、theme、user）
├── reducer/       # Redux Reducers
├── config/        # 样式配置和静态配置
├── db/            # SQLite 数据库封装
├── event/         # EventBus 事件定义
├── model/         # 数据模型（微博 JSON 映射，50+ 模型文件）
│   └── local/     # 本地/Widget 相关模型
├── net/           # API 网络层（按域拆分：weibo、user、comment、search 等）
├── page/          # UI 页面
│   ├── home/      # 首页
│   ├── discovery/ # 发现
│   ├── message/   # 消息
│   ├── login/     # 登录
│   ├── personal_center/  # 个人中心
│   ├── public/    # 公共页面（微博详情、用户主页等）
│   └── widget/    # 复用组件
├── provider/      # 数据控制器（业务逻辑层）
└── utils/         # 工具类
```

## 路线图 / Roadmap

详见 [ROADMAP.md](ROADMAP.md)。当前优先事项：

1. **Flutter 3.x 迁移** — 升级到最新 Flutter stable，启用 null safety
2. **依赖现代化** — 更新过时依赖，替换已废弃的包
3. **测试覆盖** — 补充单元测试和集成测试
4. **代码质量** — 静态分析、lint 规则完善

## 参与贡献 / Contributing

欢迎参与贡献！请阅读 [CONTRIBUTING.md](CONTRIBUTING.md) 了解如何提交 Issue、Pull Request 和参与开发。

## 致谢 / Acknowledgments

- 特别感谢 Smooth 作者 [@06peng](https://weibo.com/llp0524) 的支持
- UI 设计灵感来自 Smooth、Share 和微博国际版

## 许可证 / License

本项目基于 [GPL-3.0](LICENSE) 许可证开源。

---

**联系方式：** 微博 [@竹笋饼干](https://www.weibo.com/p/1005052294516673)
