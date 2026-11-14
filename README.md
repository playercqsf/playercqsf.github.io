# Player传奇发布网（静态站）

纯静态多栏目网站，可直接部署到 GitHub Pages（playercqsf.github.io）。

## 目录结构（全部文件与 index.html 同级，扁平结构）

```
index.html      首页
mr.html         栏目：每日新开传奇
bb.html         栏目：传奇版本大全
gg.html         栏目：开服表公告
gl.html         栏目：传奇游戏攻略
zx.html         栏目：传奇资讯中心
about.html      关于本站
404.html        404 页
mr1.html …  mr30.html    每日新开 30 篇
bb1.html …  bb30.html    版本大全 30 篇
gg1.html …  gg30.html    开服公告 30 篇
gl1.html …  gl30.html    攻略 30 篇
zx1.html …  zx30.html    资讯 30 篇
1.jpg … 30.jpg  126×126 区服图标（替换成你自己的图）
style.css       全站样式
favicon.svg     站点图标
robots.txt      搜索引擎抓取规则
sitemap.xml     站点地图（含全部 157 个页面）
.nojekyll       关闭 GitHub Pages 的 Jekyll 处理
```

## 部署到 playercqsf.github.io

1. 新建仓库，仓库名必须是 `playercqsf.github.io`（用户名 playercqsf 的用户站点仓库）。
2. 把本压缩包内的**全部文件**（不要多套一层文件夹）上传到仓库根目录。
3. Settings → Pages → Source 选择 `Deploy from a branch`，分支 `main`，目录 `/ (root)`，保存。
4. 等待 1～3 分钟，访问 https://playercqsf.github.io/ 。

## 替换 126×126 图片

首页 6 张（1.jpg–6.jpg）+ 五个栏目页各 4 张（7.jpg–26.jpg）+ 关于页示例 4 张（27.jpg–30.jpg），共 30 张。
直接用同名文件覆盖即可，尺寸保持 126×126（正方形，jpg/png 均可，扩展名为 .jpg）。
图片按 126×126 的方形裁切显示，首页为紧凑卡位、栏目页推荐位与关于页示例位均按原比例缩放，不会拉伸变形。

## 内容替换

- 文章正文在构建源文件中按 `@TITLE / @TAG / @DATE / @KW / @DESC / @LEAD / @H2` 分段，可重新生成。
- 开服表数据集中在 `SERVERS` 列表，改一处首页表格与侧栏同步更新。
- 站内区服名称、开区时间、爆率参数均为示例数据，上线前请替换为真实信息。

## 版式与标题

- 首页、五个栏目页、全部文章页均为紧凑版式，桌面端页面高度约 1600–1900px，控制在两屏内。
- 全站 `<title>` 不再带站名后缀，只保留页面自身主题词；站点名保留在 logo、og:site_name 与 JSON-LD 中。

## SEO 已配置项

- 每页独立 title / keywords / description，标题控制在 30 字内，描述约 75 字。
- canonical 指向 playercqsf.github.io 绝对地址。
- 全站语义化标签：header / nav / main / article / section / h1-h3 / breadcrumb。
- 结构化数据：WebSite、CollectionPage、Article、BreadcrumbList、FAQPage。
- 内链体系：栏目 ↔ 文章 ↔ 相关阅读 ↔ 上一篇/下一篇 ↔ 标签聚合。
- sitemap.xml + robots.txt，纯静态无 JS 依赖，移动端自适应。
