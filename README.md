# THE GARDEN BEYOND TIME｜时间之外·思想之境

这是一个可直接部署到 GitHub Pages 的静态网站 V1.0。

## 网站结构
- `/`：Three.js 3D 交互起始页《时间的尽头》
- `/garden/`：数字花园首页
- `/garden/articles.html`：思想与研究、内容搜索与分类
- `/garden/article.html?id=...`：文章详情页
- `/garden/graph.html`：可点击的主题知识图谱
- `/garden/creations.html`：小说与创作
- `/garden/experiments.html`：实验与作品
- `/garden/about.html`：关于

## 上传方式（GitHub Pages）
1. 下载并解压 `digital_garden_site_v1.zip`。
2. 打开 GitHub 仓库 `luyuezhi-master/luyuezhi-master.github.io`。
3. 将压缩包内的所有文件和文件夹上传到仓库根目录。
4. 如果仓库已有 `index.html`，请先备份；本项目的 `index.html` 将作为网站新起始页。
5. 提交（Commit changes）后，等待 GitHub Pages 自动部署。
6. 访问 `https://luyuezhi-master.github.io/`，起始页点击 `ENTER THE GARDEN` 进入数字花园。

也可以使用 Transmit：连接 GitHub Pages 对应的发布目录并上传整个目录结构。注意 GitHub Pages 通常通过 Git 仓库部署，不是直接上传到 InfinityFree 的 `htdocs`；如果你使用的是 GitHub Pages，建议在 GitHub 仓库网页端上传或通过 Git 客户端同步。

## 如何新增文章
编辑 `data/articles.json`，在数组中增加一个对象。示例：

```json
{
  "id": "my-new-note",
  "title": "一条新的思想笔记",
  "date": "2026-11-12",
  "type": "note",
  "category": "哲学与思想",
  "tags": ["意识", "文明"],
  "status": "seedling",
  "summary": "用一两句话概括核心观点。",
  "body": [
    ["问题", "正文段落……"],
    ["进一步思考", "正文段落……"]
  ]
}
```

`type` 可选：`note`、`essay`、`research`、`creation`、`experiment`。
`status` 可选：`seedling`（发芽）、`growing`（生长）、`mature`（成熟）、`evergreen`（常青）。

新增分类主题时，同时维护 `data/topics.json`。知识图谱关系维护在 `data/relations.json`。

## 技术与依赖
- HTML / CSS / 原生 JavaScript
- Three.js 0.161.0，使用 jsDelivr CDN
- Google Fonts 字体 CDN
- 无数据库、无后端、无构建命令
- 建议通过 HTTPS 访问。3D 首页需要浏览器支持 WebGL，并需要能够访问 CDN。

## 版本说明
V1.0 是可部署的基础版本，包含示例内容、分类检索、详情页和初版知识图谱。示例文章是结构演示与已有讨论主题的整理稿，发布前请逐篇审阅、补充来源并确认表述。
