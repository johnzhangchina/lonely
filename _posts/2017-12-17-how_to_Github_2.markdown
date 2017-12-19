---
layout: post
title:  "How to biuld the space on Github-step 2"
description: This section is to introduce after we builed space, how can we use the template then edit it to make the space looks more prety and personalized.
date:   2017-12-17 18:00:00 +0800
categories: jekyll update
img: ste2.png
categories: [one, two]
color: BF360C
author: John
---
#捷径-使用别人的模板
在step 1 中大体上了解了在GitHub上搭建博客的基本结构，但是对于没有HTML和CSS以及JS基础的人来讲自己搭建一个界面美妙、使用起来方便的博客短期内是比较困难的，所以最简单、直接的方式是copy一份别人的，自己在上面进行修改。
copy别人的模板有两种途径：1. 百度一下（关键字： GitHub博客模板）2. 从GitHbu直接copy 这里直接介绍第二种：
![download template]({{site.baseurl}}/images/dt1.png)
这样直接就把前辈的博客整个copy下来了，然后运用 step 1 中GitHub Desktop工具将自己修改好的版本push到自己的GitHub master分支中就可以了。

#个性化修改
Step 1中介绍的GitHub结构内容部分在这里就起作用了（这样你可以知道在哪去修改内容），copy下来的模板如下：
![download template]({{site.baseurl}}/images/edit.png)

{% highlight ruby %}
_includes：默认的在模板中可以引用的文件的位置，后面会提到
_layouts：默认的公共页面的位置，后面会提到
_posts：博客文章默认的存放位置
.gitignore：git将忽略这个文件中列出的匹配的文件或文件夹，不将这些纳入源码管理
_config.yml：关于jekyll模板引擎的配置文件
index.html：默认的主页
{% endhighlight %}
这里主要是修改_config.yml和_layouts中的内容，其它的可以后面再仔细研究下，对于_config.yml中，主要是修改baseurl，将url改成自己的地址，这样模板才会起作用，否则相关的CSS等不会生效，_layouts中主要修改一些标题，这样看起来才像自己的东西。
_config.yml修改：
要将自己博客的相对路径写进去，这里要注意两个问题 1. github page 的话要是username.github.io 就为空 2. 要是username.github.io/reponame 就得写reponame，以我自己的为例，我的是第二种就如下图配置：
![configure]({{site.baseurl}}/images/conf1.png)
对于title那些修改就不记录了，能想到用GitHub写博客的一看就懂怎么改。

#写博客
后面需要做的就是用markdown写博客，然后将其放到_posts文件中，相关的图片放到images文件夹中并在markdown文件中引用。
![link art]({{site.baseurl}}/images/mdlink.png)
然后展示下我根据别人修改出来的博客界面：
![link art]({{site.baseurl}}/images/mygithub.png)

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
