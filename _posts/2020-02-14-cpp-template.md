---
layout: post
title: C++ | C++模板体验
categories: C++
description: 一起来学泛型编程！
keywords: C++,template
---
今天来体验一波泛型。我之前写过一个max函数，大概是这样写的吧：
```cpp
int max(int const &a,int const&b)//常量引用
{
  return a>b?a:b;
}
```
真是不错的语法！我们可以把它优化成内联函数版本：
```cpp
inline int max(int const &a,int const&b)//常量引用
{
  return a>b?a:b;
}
```
可是这玩意为什么只能比较int？如果我想比两个double，恐怕得把它乘以几百倍才能来比。这好解决，c++不是有函数重载吗？来！
```cpp
double max(double const &a,double const&b)//常量引用
{
  return a>b?a:b;
}
```
可是如果要求俩std::size_t的最大值（例如0xffff45和0xffffff)这个早超了int范围了！难道又重载？？？？？？？？？我不玩了！如果没有泛型，我们就丢下C++吧……可惜C++是有的！！！上代码吖！
```cpp
template<typename tp>
tp max(tp const &a,tp const &b)
{
  return a>b?a:b;
}
```
beautiful!这样就可以比较任意可以用>号比较的类型！如果你把一个struct/class重载了>运算符，也是可以的！这个就当做作业吧！你可以把你定义的struct/class发到我邮箱<mailto:northy360@126.com>我们一同进步！<br>
![Load Photo Error](https://gitee.com/momonorthy/github-blog-images-2/raw/master/img/duj.jpg)
