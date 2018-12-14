---
title: 初始化jekyll环境
---

构建最精简的jekyll环境


# 基础配置

## _config.yml
``` yml
baseurl: /simple-jekyll-demo
title: Simple Jekyll Demo
description: Quickly build a simple Jekyll website
```
由于项目定义在子目录中所以需要配置`baseurl`

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
2018/12/2018-12-14-init-jekyll-context.md 
被自动收录的文件名必须符合 YYYY-MM-DD-TITLE 的规则
文件内可以通过yml头进行属性更新
```yml

---
title: 标题
date: yyyy-mm-dd HH:ii:ss +-TTTT
categories: 分类 | [分类列表,]
---

```
由于当前的路径规则为 `/:categories/:year/:month/:day/:title:output_ext`
分类会被体现在路径里
{% raw %}
通过 {{site.collections[0].permalink}} 查看集合路径生成规则
{% endraw %}

## _posts/2018-12-14-simple.md 一篇md文章
``` 

---
# yml 头信息
title: simple blog
---

simple blog desc # 第一行为摘要，可以通过 page.excerpt 获取

simple blog content  # MD格式的正文内容

```



