# 维护与写作说明（仅作者本地使用）

把本文件复制为 `AUTHOR.local.md`（已在 `.gitignore` 中忽略），按自己的习惯改。仓库里的 `README.md` 只给读者看，操作约定都写在这里。

## 远程与本地

`drafts/`、`notes/`、`templates/` 已在 `.gitignore` 中：**不会推到远程**。远程主要是「成文」[`posts/`](posts/)、读者索引 [`index/`](index/)、[`README.md`](README.md) 与 [`assets/`](assets/)。

模板底稿在仓库里的 [`templates.example/`](templates.example/)（随仓库同步）。首次在本机可：

```bash
mkdir -p drafts notes templates
cp templates.example/*.md templates/
# 选题池可自行建立 drafts/idea-list.md
```

之后在本地 `drafts/`、`notes/`、`templates/` 里随便写，不影响远程观感。

## 目录在作者视角下怎么用

| 路径 | 用途 |
|------|------|
| `posts/YYYY/` | 已发布成文，对外展示以这里为主 |
| `drafts/`（仅本地） | 草稿、选题池等 |
| `notes/`（仅本地） | 碎片笔记：工具、提示词、工作流等 |
| `templates/`（仅本地） | 从 `templates.example/` 复制后可随手改 |
| `assets/images/YYYY/`、`assets/files/` | 配图与附件，随成文一起提交 |
| `index/timeline.md` | 读者时间线，**每发一篇**补一条链接 |
| `index/tags.md` | 读者标签页，**每发一篇**在对应标签下加链接 |

## 文件与命名

- 文章文件：`YYYY-MM-DD-英文短关键词.md`（例：`2026-04-29-ai-agent-workflow.md`）
- 新文：在本地复制 `templates/post-template.md`（或直接从 `templates.example/` 复制）到 `drafts/` 或直达 `posts/2026/`
- 定稿：移到 `posts/YYYY/`，front matter 里 `status: published`

## 发布自检（最少步骤）

1. 正文与资源路径无误  
2. `index/timeline.md` 增加一行（最新在上）  
3. `index/tags.md` 在对应标签下增加链接；新标签就新开一个小节  

## 常用标签（自拟，与 front matter 一致即可）

| 标签 | 含义 |
|------|------|
| `ai-agent` | Agent、自动化工作流 |
| `prompt` | 提示词与实践 |
| `tooling` | 工具链与效率 |
| `reading` | 读书笔记 |
| `reflection` | 复盘与方法论 |
