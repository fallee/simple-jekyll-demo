---
title: simple jekyll demo
---

{% for page in site.posts %}
* [{{page.title}}]({{page.url}})
{% endfor %}

{{site.collections[0].permalink}}