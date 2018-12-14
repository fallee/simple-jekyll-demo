---
title: 初始化jekyll环境
---

构建最精简的jekyll环境

## index.md 首页
{% raw %}
``` liquid

---
title: simple jekyll demo
---

{% for page in site.posts %}
* [{{page.title}}]({{page.url}})
{% endfor %}


```
{% endraw %}

## _posts/ post集合目录
目录内的.md 和 .html 文件会被收录到 site.posts 集合
并生成对应的 .html 文件
## _posts/2018-12-14-init-jekyll-context.md 一篇md文章


