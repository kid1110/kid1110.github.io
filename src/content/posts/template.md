---
title: "博客文章模板（复制我，开始写新文章）"
author: kid
pubDatetime: 2026-09-09T12:00:00+08:00
modDatetime: 2026-09-09T12:00:00+08:00
slug: template
featured: true
draft: false
tags:
  - 模板
  - 指南
description: "这是一篇模板文章，完整演示 AstroPaper 的 frontmatter 字段与常见 Markdown 写作语法，方便你复制后填入自己的内容。"
timezone: "Asia/Shanghai"
# 可选字段（需要时取消注释）：
# ogImage: ../../assets/images/你的封面图.png   # 或填写远程图片 URL
# canonicalURL: https://blog.kkid.fun/posts/xxx  # 原创转载时的原始链接
# hideEditPost: true                              # 隐藏「编辑此页」按钮
---

这是一篇**模板文章**。请直接复制本文件（`src/content/posts/template.md`），改好 frontmatter 与正文即可作为新文章发布。下面演示了 AstroPaper 支持的 frontmatter 字段与常见写作语法。

## Table of contents

## 1. Frontmatter 字段说明

每篇文章开头用 `---` 包裹的 YAML 即 frontmatter，本文件用到的字段如下：

```yaml
---
title: "博客文章模板"                        # 必填：文章标题
author: kid                                   # 可选：作者，缺省取 site.author
pubDatetime: 2026-09-09T12:00:00+08:00        # 必填：发布日期
modDatetime: 2026-09-09T12:00:00+08:00        # 可选：最后修改时间
slug: template                                # 可选：URL 路径，缺省由文件名生成
featured: true                                # 是否在首页「精选」展示
draft: false                                  # true 时为草稿，不会发布
tags: ["模板", "指南"]                         # 标签，用于标签页聚合
description: "一句话描述"                      # 必填：摘要与 SEO 描述
timezone: "Asia/Shanghai"                      # 可选：本文时间的展示时区
---
```

## 2. 常用文本语法

### 标题与段落

用 `#` 的个数表示 1~6 级标题；正文用空行分隔段落。

### 强调、行内代码

这是**加粗**、*斜体*、~~删除线~~，以及 `行内代码`。

### 列表

- 无序列表项一
- 无序列表项二
  - 嵌套子项

1. 有序列表项一
2. 有序列表项二

- [x] 已完成的任务
- [ ] 待办任务

### 引用

> 这是一段引用文字，可嵌套：
>
> > 嵌套引用。

### 链接与图片

链接示例：[GitHub](https://github.com)。图片语法：`![alt 描述](图片地址)`。

![一张示例图片](https://images.pexels.com/photos/159618/still-life-school-retro-ink-159618.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)

### 表格

| 功能 | 说明 | 示例 |
| --- | --- | --- |
| 代码高亮 | 代码块自动语法高亮 | `ts` |
| 自动目录 | 由 `## Table of contents` 触发 | 本文顶部 |
| 数学公式 | 需按官方指南自行开启插件 | 默认关闭 |

### 代码块

````md
```ts
interface Post {
  title: string;
  pubDatetime: Date;
  tags: string[];
}

export function hello(name: string): string {
  return `你好，${name}！`;
}
```
````

### 提示框（Callout）

> [!NOTE]
> 普通说明信息。

> [!TIP]
> 实用技巧。

> [!WARNING]
> 需要留意的内容。

> [!CAUTION]
> 谨慎操作。

### 分隔线与脚注

分隔线如下：

---

脚注示例[^1]。

[^1]: 这是脚注的内容。

## 3. 如何写一篇新文章

1. 复制本文件并重命名，例如 `src/content/posts/my-first-post.md`；
2. 修改 frontmatter 中的 `title` / `pubDatetime` / `description` 等；
3. 把正文换成你的内容（可删掉本文演示片段）；
4. 确认无误后删除本模板文件并提交。

> [!WARNING]
> 本页是模板演示。正式写作时请删除本文件，避免「模板」文章出现在你的博客列表中。
