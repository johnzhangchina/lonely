---
layout: post
title:  "How to biuld the space on Github-step 1"
description: This section is to introduce how we can build the space belongs to you at GitHub, it includes how to sign up, create project and edit at local PC and upload.
date:   2017-12-17 16:00:00 +0800
categories: jekyll update
img: step1_01.jpg
categories: [one, two]
color: 7E57C2
author: John
---

#注册账号
访问：http://www.github.com/，注册你的username和邮箱，邮箱十分重要，GitHub上很多通知都是通过邮箱的。比如你的主页上传并构建成功会通过邮箱通知，更重要的是，如果构建失败的话也会在邮件中说明原因。

#创建项目仓库
在创建博客之前，还需要用已有的帐号创建一个项目，上面那个链接的projectName将是这里即将创建的项目名称。在Git中，项目被称为仓库(Repository)，仓库顾名思义，当然可以包含代码或者非代码。将来我们的网页或者模板实际上都是保存在这个仓库中的。
登录后，访问https://github.com/new，创建仓库如下图（图片来源于网络，自己懒得截图了）：
![create project]({{site.baseurl}}/images/cp1.png)

#本地编辑及上传
网上很多教程都用的是git工具，对于常年用Windows这种傻瓜式操作系统的人来讲一般觉得很麻烦（后面如果必须要用到再用），所以本人用的是Github Desktop这个工具，可以将github上的内容clone到本地或者将本地的仓库同步到GitHub上（clone到本地我就不记录操作了，懂一点英语的挨个试一下就知道了）。
![upload project]({{site.baseurl}}/images/ul1.png)

#搭建基本框架并同步到GitHub
在该目录下手动创建如下文件和文件夹，最终形成这样的结构：
![structure]({{site.baseurl}}/images/st1.png)

'_includes：默认的在模板中可以引用的文件的位置，后面会提到'
'_layouts：默认的公共页面的位置，后面会提到'
'_posts：博客文章默认的存放位置'
'.gitignore：git将忽略这个文件中列出的匹配的文件或文件夹，不将这些纳入源码管理'
'_config.yml：关于jekyll模板引擎的配置文件'
'index.html：默认的主页'

在_layouts目录下创建一个default.html，在其中输入如下内容，特别注意：文件本身要以UTF-8 without BOM的格式保存，以防止各种编码问题，建议使用notepad++或sublime编辑
{% highlight ruby %}
<!DOCTYPE html>
	<html>
	<head>
	　<meta http-equiv="content-type" content="text/html; charset=utf-8" />
	　<title>一步步在GitHub上创建博客主页(2)</title>
	</head>
	<body>
	　{{content }}
	</body>
	</html>
编辑index.html
---
layout: default
title: test title
---
<p>Hello world!</p>
编辑_config.yml
encoding: utf-8
{% endhighlight %}
[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
