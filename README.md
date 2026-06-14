# 京沪高铁24站旅客评论分析 · 可分享页面

一个**自包含的单页交互报告**(`index.html`),基于 122,445 条清洗后社交平台评论(抖音 / 快手 / 微博 / 小红书),从铁路管理者视角做情绪分析、24 站逐站旅客映像与改进方向。

- 图表:ECharts(多 CDN 自动回退,优先国内 bootcdn,失败再退 jsdelivr / cdnjs / unpkg)
- 无后端、无构建,直接托管静态文件即可
- `.nojekyll`:让 GitHub Pages 原样输出

## 一、推送到 GitHub 并开启 Pages

在本目录下执行(`<用户名>` / `<仓库名>` 换成实际值):

```bash
cd report-site
git init -b main
git add -A
git commit -m "京沪高铁24站旅客评论分析 可分享页面"
git remote add origin https://github.com/<用户名>/<仓库名>.git
git push -u origin main
```

> HTTPS 推送时"密码"填 GitHub Personal Access Token(Settings → Developer settings,勾 `repo`);或改用 SSH remote。

然后在仓库 **Settings → Pages** 选择 `main` 分支、根目录 `/`,保存。
几分钟后页面地址为 `https://<用户名>.github.io/<仓库名>/`。

## 二、发布到腾讯云 EdgeOne Pages(国内访问更稳)

两种方式任选:

1. **连 GitHub 一键部署**:EdgeOne Pages 控制台 → 新建项目 → 选择上面这个 GitHub 仓库 → 框架选「静态站点 / 无」→ 输出目录填 `/`(根目录)→ 部署。之后每次 push 自动更新。
2. **直接上传**:EdgeOne Pages → 新建项目 → 直接上传 → 把本目录(含 `index.html`)拖上去即可。

用 EdgeOne 分配的默认域名访问**无需备案**;若绑定自有域名并走大陆节点才需要 ICP 备案。

## 文件说明

| 文件 | 说明 |
|------|------|
| `index.html` | 完整交互报告(总览 / 24站对比 / 逐站分析 / 主题 / 三大方向 / 行动建议) |
| `.nojekyll` | GitHub Pages 原样输出标记 |
