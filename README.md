![](/assets/images/readme/1.png)
[![Github Pages](https://github.com/vanhiupun/Vanhiupun.github.io/actions/workflows/jekyll.yml/badge.svg?style=flat-square&logo=github&logoColor=ffffff&color=f3a306)](https://github.com/vanhiupun/Vanhiupun.github.io/actions/workflows/jekyll.yml)
[![ GitHub ](https://img.shields.io/badge/Github%20Repository-222222?style=flat-square&logo=github&logoColor=ffffff)](https://github.com/vanhiupun)
[![ Blog ](https://img.shields.io/badge/Github%20Page-222222?style=flat-square&logo=github&logoColor=ffffff)](https://vanhiupun.github.io)
[![ Gmail ](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=Gmail&logoColor=ffffff)](mailto:fanxiaobin422@gmail.com)
[![ MIT ](https://img.shields.io/badge/License%20MIT-EC9430?style=flat-square&logo=Mitsubishi&logoColor=ffffff)](https://github.com/vanhiupun/Vanhiupun.github.io/blob/c0c037532393ee2718892f87b200a0bbe33e7eb9/License)


#### 详细说明
[制作和我一样的Jekyll博客](https://vanhiupun.github.io/jekyll/2021/11/20/制作和我一样的Jekyll博客.html)

#### 安装

```git
git clone git@github.com:vanhiupun/Vanhiupun.github.io.git
```

#### 设置环境

```git
cd Vanhiupun.github.io
bundle install
bundle exec jekyll serve
```

要设置您的环境来开发此主题，请运行`bundle install`.

您的主题设置就像一个普通的`Jekyll`站点一样！要测试您的主题，请运行`bundle exec jekyll serve`并打开您的浏览器[http://localhost:4000](http://localhost:4000)。这将使用您的主题启动 Jekyll 服务器。像往常一样添加页面、文档、数据等来测试您的主题内容。当您对主题和内容进行修改时，您的站点将重新生成，刷新后您应该会看到浏览器中的更改，就像往常一样。

当你的主题被释放，只有在文件中`_data`，`_layouts`，`_includes`，`_sass`和`assets`使用 Git 跟踪将被捆绑在一起。要将自定义目录添加到您的主题宝石，请相应地编辑正则表达式`jekyll-theme-yat.gemspec`。

#### 开始

你可以通用修改`_config.yml`文件来轻松的开始搭建自己的博客:

```bash
title: Vanhiupun blog  # 你的博客网站标题

email: fanxiaobin422@gamil.com # 你的邮箱

author: Vanhiupun # 你的名字

baseurl: "" # 网站的子路径，例如 /blog

url: "" # 站点的基本主机名和协议，例如 e.g. http://example.com

favicon: "./favicon.png" # 网站的图标

# 分页设置
paginate: 5 #在主页显示5篇文章

# 摘录大小设置
excerpt_size: 250 #主页文章字数显示为250字

```

#### 撰写博文

要发表的文章一般以 Markdown 的格式放在这里`_posts/`，你只要看看这篇模板里的文章你就立刻明白该如何设置。

```bash
---
layout: post #布局
title: 科学上网指南（二）：线路的区别与选择 #标题
categories: 科学上网 #分类
banner:
  image: https://vanhiupun.github.io/assets/images/banners/jichang.jpeg #图片地址 也可以使用 ./assets/images/banners/jichang.jpeg
  opacity: 0.618 #不透明度
  background: "#000" #背景颜色
  height: "50vh" #高度
  min_height: "50vh" #宽度
  heading_style: "font-size: 4.25em; font-weight: bold; " #标题样式
  subheading_style: "color: gold" #副标题样式
tags: [机场指南] #标签
---
```

#### Header Image

博客每页的标题底图是可以自己选的，看看几篇示例 post 你就知道如何设置了。

标题底图的选取完全是看个人的审美了。每一篇文章可以有不同的底图，你想放什么就放什么，最后宽度要够，大小不要太大，否则加载慢啊。

> 上传的图片最好先压缩，这里推荐 imageOptim 图片压缩软件，让你的博客起飞。

但是需要注意的是本模板的标题是**白色**的，所以背景色要设置为**灰色**或者**黑色**，总之深色系就对了。当然你还可以自定义修改字体颜色，总之，用 github pages 就是可以完全的个性定制自己的博客。

#### Customization

如果你喜欢折腾，你可以去自定义这个模板的 Code。

**如果你可以理解 `_include/ `和 `_layouts/`文件夹下的代码（这里是整个界面布局的地方），你就可以使用 `Jekyll` 使用的模版引擎 `Liquid`的语法直接修改/添加代码，来进行更有创意的自定义界面啦！**

#### Disqus 评论

国际比较流行，界面也很大气、简洁，如果有人评论，还能实时通知，直接回复通知的邮件就行了
需要去注册一个[Disqus 帐号](https://disqus.com/)。将我的账号替换成你的就可以

```bash
# Disqus 评论
disqus:
  shortname: "vanhiupun" #在disqus注册一个账号 并将此处换成你自己的账号
```

#### Analytics

网站分析，现在支持[Google Analytics](https://analytics.google.com/analytics/web/)。需要去官方网站注册一下，然后将返回的 code 贴在下面：

```bash
# Google Analytics
google_analytics: "UA-212989441-1"    # 你用Google账号去注册一个就会给你一个这样的id 将此处替换即可
enableDNT: true
```

#### 贡献

非常感谢问题和拉取请求。如果您在我非常乐意向您介绍如何创建拉取请求之前从未为开源项目做出过贡献。

您可以首先[打开一个问题](https://github.com/vanhiupun/Vanhiupun.github.io/issues/new)，描述您要解决的问题，我们将从那里开始。

#### 致谢

这个模板是从 [jeffreytse](https://github.com/jeffreytse/jekyll-theme-yat) Fork 的, 感谢这个作者。

#### License

遵循 MIT 许可证。有关详细,请参阅 [LICENSE](./License)。

#### 赞助
<img src="./assets/images/img/zz.png">