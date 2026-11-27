# TODAY Tech 官网

TODAY Tech 官方组织网站首版，使用原生 HTML、共享 CSS 和少量 JavaScript 构建，适合直接通过 GitHub Pages 托管。

## 本地预览

仓库没有运行时依赖。使用 Python 启动静态文件服务器：

```bash
python3 -m http.server 8000
```

然后访问 <http://localhost:8000/>。三个页面都使用目录式入口，可直接刷新访问：

- `/` — TODAY Tech 组织首页
- `/projects/today-infrastructure/` — TODAY Infrastructure 框架介绍
- `/products/today-infra-assistant/` — TODAY Infra Assistant 插件介绍

## 目录结构

```text
.
├── index.html
├── robots.txt
├── sitemap.xml
├── logo.svg
├── assets/
│   ├── css/site.css       # 全站设计与响应式样式
│   └── js/site.js         # 移动端导航、页脚年份
├── projects/
│   └── today-infrastructure/index.html
└── products/
    └── today-infra-assistant/index.html
```

页面已包含 canonical、Open Graph 基础元信息和首页 Organization 结构化数据。`robots.txt` 与 `sitemap.xml` 使用正式域名 `today-tech.cn`；自定义域名启用后，可将 `https://today-tech.cn/sitemap.xml` 提交到 Google Search Console 等站长工具。

## 已核实的公开入口

- [TODAY Tech GitHub 组织](https://github.com/today-tech)
- [TODAY Infrastructure 源码](https://github.com/TAKETODAY/today-infrastructure)
- [TODAY Infrastructure 文档](https://docs.today-tech.cn/today-infrastructure/)
- [TODAY Infra Assistant Marketplace](https://plugins.jetbrains.com/plugin/36523-today-infra-assistant)

当前框架公开仓库仍在 `TAKETODAY/today-infrastructure`，README 使用 `cn.taketoday` 坐标，开发版本为 `5.0-Draft.10-SNAPSHOT`。`cn.today-tech` 和 `1.0.0` 出现在项目 ADR 的未来规划中，官网没有将它们描述为已发布事实。插件页面可访问，但尚未发现正式的支持、许可或隐私资料，因此插件页只链接 Marketplace。

## GitHub Pages 部署

将仓库发布源设置为包含 `index.html` 的分支根目录即可。自定义域名 `today-tech.cn`、DNS 和 GitHub Pages 设置需在仓库外部配置，本首版没有修改这些设置，也没有提交或推送代码。
