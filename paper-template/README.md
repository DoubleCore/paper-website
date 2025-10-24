## 如何使用此模板 (How to Use This Template)

本仓库提供了一个即用型的学术项目主页模板。您只需按照以下步骤填充您的内容，即可快速生成一个专业的项目网站。

### 1. 全局信息配置

打开 `index.html` 文件，在 `<head>` 部分进行以下配置：

- **Google Analytics**: 将 `G-XXXXXXXXXX` 替换为您自己的 Google Analytics ID，以便追踪网站流量。
- **页面标题**: 将 `<title>` 标签中的 `{{PAPER_TITLE}}` 替换为您的论文标题。
- **页面描述和关键词**: 修改 `<meta name="description">` 和 `<meta name="keywords">` 中的 `content` 属性，以优化搜索引擎收录效果。

### 2. 填充页面内容

在 `index.html` 文件中，通过搜索和替换以下占位符来填充您的研究内容：

- `{{PAPER_TITLE}}`: 您的论文标题。
- `{{AUTHOR_NAME}}`: 作者姓名。您可以根据需要添加或删除作者区块。
- `{{AUTHOR_LINK}}`: 作者的个人主页链接。
- `{{PDF_LINK}}`: 论文PDF文件的链接。
- `{{ARXIV_LINK}}`: 您的ArXiv预印本链接。
- `{{CODE_LINK}}`: 代码仓库的链接。
- `{{CONFERENCE_NAME}}`: 论文发表的会议或期刊名称。
- `{{YEAR}}`: 发表年份。
- `{{TEASER_TEXT}}`: 一段引人注目的核心成果简介。
- `{{ABSTRACT_TEXT}}`: 您的论文摘要。
- `{{METHOD_X_TITLE}}`: 您的方法要点标题 (例如, `{{METHOD_1_TITLE}}`)。
- `{{METHOD_X_DESCRIPTION}}`: 对方法要点的详细描述。
- `{{SOTA_COMPARISON_TEXT}}`: 与当前最先进技术(SOTA)的比较说明。
- `{{ABLATION_STUDY_TEXT}}`: 消融实验的相关描述。

### 3. 替换图片资源

将您的项目图片（如核心成果图、方法概述图等）放入 `images` 文件夹，并更新 `index.html` 中相应的图片路径。建议保持图片文件名与模板中的名称一致，以简化修改过程。

### 4. 更新BibTeX引用

在 `index.html` 文件底部的 `<section id="BibTeX">` 部分，更新为您的论文的BibTeX引用格式。

### 5. 部署到GitHub Pages

完成以上修改后，将您的代码推送到GitHub仓库，并在仓库的设置中启用GitHub Pages。您的项目主页即可通过 `https://your-username.github.io/your-repo-name/` 访问。

## 常见问题

### 为何新增 `github paper` 文件夹后 GitHub Pages 构建失败？
GitHub Pages 默认只会从仓库根目录（或设置为 `docs/` 的目录）读取入口文件。在这个项目里，`index.html`、`main.js` 等网站资源位于仓库根目录。如果为了整理结构，把这些文件全部移动到一个名为 `github paper` 的额外文件夹里，根目录就不再包含入口文件，GitHub Pages 在构建时会提示找不到站点源，从而发布失败。保持网站文件位于仓库根目录，或者将目标目录重命名为 `docs/` 并在仓库设置中将 Pages 的发布源改为 `main /docs`，即可恢复正常部署。
