---
layout: post
title:  'jekyll 主题 dactl 踩坑备忘'
tags:
  - jekyll
  - dactl
  - 踩坑
overlay: purple
published: false
---

# dactl 踩坑备忘

* 行号显示bug

* 中文.md文件名导致博文样式异常

## 行号显示bug

修改`dactl`主题配置文件`_config.yml`

```yaml
span:
      line_numbers: false
    block:
      line_numbers: false
```

## 中文.md文件名导致博文样式异常

不要使用中文名的.md文件作为博客文件，中文名会导致博客列表的样式加载失败。
