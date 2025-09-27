# MkDocs Material guide

## 1. 安装

推荐使用 pip 安装：

```bash
pip install mkdocs-material
```

也可用 Docker 或源码安装，详见 [官方文档](https://squidfunk.github.io/mkdocs-material/getting-started/)。

## 2. 新建项目

```bash
mkdocs new my-project
cd my-project
```

## 3. 配置 mkdocs.yml

`mkdocs.yml` 是主配置文件，常见配置如下：

```yaml
site_name: 我的文档站点
site_url: https://your-site.com
theme:
	name: material
	language: zh
	logo: images/logo.png
	favicon: images/favicon.ico
	palette:
    - scheme: default
      primary: indigo
      accent: indigo
      toggle:
        icon: material/weather-night
        name: Switch to dark mode
    - scheme: slate
      primary: indigo
      accent: indigo
      toggle:
        icon: material/weather-sunny
        name: Switch to light mode
nav:
	- 首页: index.md
	- 指南:
			- 快速开始: guide/quickstart.md
			- 配置: guide/config.md
markdown_extensions:
	- admonition
	- codehilite
	- toc:
			permalink: true
	- pymdownx.superfences
	- pymdownx.details
plugins:
	- search
	- tags
	- git-revision-date
extra:
	social:
		- icon: fontawesome/brands/github
			link: https://github.com/yourname/yourrepo
```

### 3.1 主题自定义
- `palette`：自定义配色和暗色模式切换
- `logo`/`favicon`：自定义站点图标
- `language`：站点语言

### 3.2 导航（nav）
支持多级导航和分组，结构清晰。

### 3.3 Markdown 扩展
推荐启用 `admonition`、`codehilite`、`toc`、`pymdownx.*` 等增强文档表现力。

### 3.4 插件（plugins）
常用插件：
- `search`：内置全文搜索
- `tags`：标签支持
- `git-revision-date`：显示文档最后更新时间
更多插件见 [插件列表](https://squidfunk.github.io/mkdocs-material/plugins/)

### 3.5 额外配置（extra）
可添加社交链接、页脚、分析代码等。

## 4. 常用命令

```bash
# 本地预览
mkdocs serve

# 构建静态站点
mkdocs build

# 部署到 GitHub Pages
mkdocs gh-deploy
```

## 5. 部署

### 5.1 本地预览
```bash
mkdocs serve
```
浏览器访问 http://127.0.0.1:8000

### 5.2 构建静态文件
```bash
mkdocs build
```
静态文件生成在 `site/` 目录。

### 5.3 部署到 GitHub Pages
```bash
mkdocs gh-deploy
```
自动推送 `site/` 到 gh-pages 分支。

## 6. 进阶配置与自定义

- [自定义配色](https://squidfunk.github.io/mkdocs-material/setup/changing-the-colors/)
- [自定义字体](https://squidfunk.github.io/mkdocs-material/setup/changing-the-fonts/)
- [自定义 logo 和图标](https://squidfunk.github.io/mkdocs-material/setup/changing-the-logo-and-icons/)
- [多语言支持](https://squidfunk.github.io/mkdocs-material/setup/changing-the-language/)
- [扩展与插件](https://squidfunk.github.io/mkdocs-material/plugins/)
- [Markdown 扩展](https://squidfunk.github.io/mkdocs-material/setup/extensions/)
- [自定义页眉页脚](https://squidfunk.github.io/mkdocs-material/setup/setting-up-the-header/)
- [添加评论系统](https://squidfunk.github.io/mkdocs-material/setup/adding-a-comment-system/)

---

更多详细配置与用法请参考 [MkDocs Material 官方文档](https://squidfunk.github.io/mkdocs-material/)。

