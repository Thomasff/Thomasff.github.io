---
title: "Hugo 写作功能速览"
date: 2026-05-22T18:40:00+08:00
draft: true
slug: hugo-writing-cheatsheet
description: 一篇不冗长的示例文章，集中演示分类、标签、图片和常见内容格式。
categories:
  - Hugo
  - Notes
tags:
  - markdown
  - shortcode
  - image
  - table
image: cover.jpg
math: true
license: "CC BY-NC-SA 4.0"
---

这篇文章是“写法清单”，每段都尽量短，方便你直接复用。

## 1) 基本排版

普通段落里可以包含 **粗体**、*斜体*、`行内代码` 和 [外部链接](https://gohugo.io/documentation/)。

> 引用块适合写结论、定义或提醒。

## 2) 列表

无序列表示例：

- 保持小段落
- 一段只讲一件事
- 标题层级不要跳

有序列表示例：

1. 新建文章
2. 本地预览
3. 提交并推送

任务列表：

- [x] 完成主题切换
- [x] 添加分类和标签
- [ ] 持续更新内容

## 3) 代码块

```bash
# create
hugo new content post/my-note.md

# preview
hugo server -D
```

```yaml
title: "My Post"
draft: false
tags: ["hugo", "markdown"]
categories: ["Blog"]
```

## 4) 图片与图集

单图（封面之外的正文图）：

![Gallery One](gallery-1.jpg)

两图并排会被主题自动处理为图集效果（不同主题行为略有差异）：

![Gallery One](gallery-1.jpg)
![Gallery Two](gallery-2.jpg)

## 5) 表格

| 字段 | 用途 | 示例 |
| --- | --- | --- |
| `categories` | 文章分类 | `Hugo` |
| `tags` | 文章标签 | `markdown` |
| `image` | 封面图 | `cover.jpg` |

## 6) 折叠块与分隔线

<details>
<summary>点击展开：发布流程</summary>

1. 写完文章后把 `draft` 设为 `false`
2. `git add . && git commit -m "new post"`
3. `git push`

</details>

---

## 7) 数学公式（可选）

行内公式：$E = mc^2$

块公式：

$$
\int_0^1 x^2 \, dx = \frac{1}{3}
$$

## 8) 最小可复用模板

你后续可以从这个 front matter 开始：

```yaml
---
title: "文章标题"
date: 2026-05-23T20:00:00+08:00
draft: true
description: "一句话摘要"
categories: ["Hugo"]
tags: ["markdown"]
image: "cover.jpg"
---
```
