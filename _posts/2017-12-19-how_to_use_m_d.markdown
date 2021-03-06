---
layout: post
title:  "Markdown basics"
description: This section introduces some of the basic grammar of Markdown, so that we can satisfy our most basic article editing requirements.  
date:   2017-12-18 23:17:00 +0800
categories: jekyll update
img: md1.png
categories: [one, two]
color: 9E9D24
author: John
---
本来想直接开更python的内容，但是想到后面更新文章少不了用到markdown的一些语法，所以学习几条md的基础语法，满足更新文章的最基本需求.

#粗体和斜体
粗体和斜体的代码如下，根据顺序可以看到相应的显示效果：

{% highlight ruby %}
*JohnZhang*

**JohnZhang**

***JohnZhang***

~~delete~~ (markdwon pad 2 中预览失败，应该是在WIN10中JS渲染有问题)
{% endhighlight %}

显示效果：
![cuxieti]({{site.baseurl}}/images/zxt1.png)

#分级标题
分级标题代码如下，不过我觉得还是'#'好用一些：

{% highlight ruby %}
JohnZhang
=============

JohnZhang
-------------
{% endhighlight %}

显示效果：
![biaoti]({{site.baseurl}}/images/bt01.png)

#超链接
Markdown支持两种形式的链接语法：行内式、参考式（行内式运用较多,时间有限只提下行内式）
##行内式
语法说明：[]里写链接文字，()里写链接地址, ()中的”“中可以为链接指定title属性，title属性可加可不加。title属性的效果是鼠标悬停在链接上会出现指定的 title文字。[链接文字](链接地址 “链接标题”)’这样的形式。链接地址与链接标题前有一个空格。

{% highlight ruby %}

John's space [lonely](https://johnzhangchina.github.io/lonely/ "lonely")

{% endhighlight %}

显示效果：
![lonely]({{site.baseurl}}/images/jsl1.png)

这三种写简单博客够用了，有些语法等要用到的时候自行查询就可以了，今天有点累写不动了，后面的时间应该会先更python基础吧目标是年前用python写一个网站自动化测试的脚本，可能有点困难，因为自己学还好，更到github上有点麻烦，尽力。

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
