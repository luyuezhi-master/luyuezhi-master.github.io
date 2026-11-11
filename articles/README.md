# 文章内容目录

当前 V1.0 使用 `data/articles.json` 管理文章数据，文章详情页由 `garden/article.html` 根据 id 自动呈现。

新增内容时，在 `data/articles.json` 的数组中增加一条记录，字段包括：
- `id`：唯一英文标识
- `title`：标题
- `date`：日期，YYYY-MM-DD
- `type`：note / essay / research / creation / experiment
- `category`：所属领域
- `tags`：标签数组
- `status`：seedling / growing / mature / evergreen
- `summary`：摘要
- `body`：正文段落数组，每项为 `[小标题, 正文]`

建议后续内容量增加后，再将文章拆分为独立 Markdown 文件并引入静态站点生成器。
