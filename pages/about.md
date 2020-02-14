---
layout: page
title: About
description: 你好
keywords: 
comments: true
menu: 关于
permalink: /about/
---

我是Mily。因代码而生，因代码而立。
兴趣：【手帐】 【C++】 【JavaScript】【世界语】
## 联系

号码：18157073593
邮箱：
> [邮箱1](mailto:northy360@126.com)
  [邮箱2](mailto:momonorthy2008@outlook.com)
## Skill Keywords

{% for category in site.data.skills %}
### {{ category.name }}
<div class="btn-inline">
{% for keyword in category.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}
