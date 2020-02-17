---
layout: post
title: 为你自己的Jekyll增加Gitalk评论
categories: 前端
---
我可是一个前端小白。对于gitalk，扒了好几百张贴子才会，今天分享给大家。<br>
先打开<https://github.com/settings/applications/new>,按照下图进行创建。<br>
![Error When Load Photo.](https://raw.githubusercontent.com/m3-soft/m3-soft.github.io/master/images/blog/2020-02-15.png)<br>
然后点确定，获得1*ID和1*Secret。打开博客的_includes/comments.html，加入以下代码::<br>
```html
{% if page.comments != false %}



<div id="gitalk-container"></div>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/gitalk@1/dist/gitalk.css">

<script src="https://cdn.jsdelivr.net/npm/gitalk@1/dist/gitalk.min.js"></script>

<script src="https://raw.githubusercontent.com/m3-soft/JavaScript-MD5/master/js/md5.min.js"></script>

<script>

var gitalk = new Gitalk({

  clientID: '<YOURID>',

  clientSecret: '<YOURSECRET>',

  repo: 'cmet',

  owner: 'USERNAME',

  admin: ['USERNAME'],

  id: '{{ page.url | truncate: 50, '' }}',      

  distractionFreeMode: false  // 专注模式

})

gitalk.render('gitalk-container')

</script>



{% endif %}
```
(把原有内容删的干干净净以后)<br>
然后去创建一个叫cmet的repo,就可有评论了！！！
<br>![Load Photo Error](https://gitee.com/momonorthy/github-blog-images-2/raw/master/img/duj.jp
