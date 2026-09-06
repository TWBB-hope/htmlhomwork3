# 课堂作业三 · CSS布局、响应式设计与Bootstrap

课程：软件开发综合实践（2026年秋季学期）第三次课

## 仓库结构

```
├── courses-page/            案例复现：响应式课程展示页
│   ├── index.html           纯CSS版（Flex导航 + Grid卡片墙 + 媒体查询断点）
│   ├── bootstrap.html       Bootstrap版（栅格 + navbar/card/alert组件 + 样式覆盖）
│   ├── css/
│   │   ├── courses.css
│   │   └── bootstrap-override.css
│   └── screenshots/         两版各三档宽度截图
└── topic-page/              自主实践：响应式专题页「拾光书影音」
    ├── index.html           入口文件
    ├── css/style.css        移动优先样式（含三项研究任务）
    └── screenshots/         三档截图、深浅色对比、打印预览
```

## 在线查看

直接用浏览器打开 `topic-page/index.html` 与 `courses-page/index.html`、`courses-page/bootstrap.html` 即可，无需构建。

## 自主实践要求对照

| 要求 | 实现情况 |
| --- | --- |
| 主题与内容完整 | 书影音推荐主题，6张卡片 + hero/数据条/关于/页脚区块 |
| 手机与桌面布局合理无横向滚动 | 375/768/1200 三档实测 `scrollWidth == innerWidth` |
| Flex或Grid复杂布局 | Flex吸顶导航 + Grid卡片墙 `repeat(auto-fit, minmax(280px, 1fr))` |
| 媒体查询断点合理 | 移动优先，768px / 992px 两档 `min-width` 增强 |
| Bootstrap栅格+两类组件 | 自主实践未用Bootstrap；案例复现版含栅格 + navbar/card/alert |
| 三档运行截图 | `topic-page/screenshots/` |
| Git提交与远程推送 | 提交记录见 `git log`，推送至远程仓库 |
| Console无红色报错 | 页面无JavaScript，三档截图时控制台无报错 |

## 研究任务（选做，全部完成）

1. **流式排版**：`h1` 用 `clamp(28px, 3.5vw + 14px, 44px)`，`h2` 用 `clamp(20px, 1.5vw + 12px, 26px)`，替换了原有三档媒体查询里的固定px字号。
2. **深色模式**：颜色全部走CSS变量，`@media (prefers-color-scheme: dark)` 换一组变量值即可整体切换。
3. **打印样式**：`@media print` 隐藏导航页脚、Grid改块级单栏、`break-inside: avoid` 防卡片跨页断裂。

## 环境说明

案例复现的Bootstrap版通过 jsDelivr CDN 引入 Bootstrap 5.3.3，联网时可正常显示。
