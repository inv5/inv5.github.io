---
layout: page
title: About
description: 你好
keywords: 
comments: true
menu: 关于
permalink: /about/
---

我是马壮，码而生，码而立。

仰慕「优雅编码的艺术」。

坚信熟能生巧，努力改变人生。

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
