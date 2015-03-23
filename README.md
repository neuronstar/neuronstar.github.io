# 写科学写故事


1. 去 [prose.io](http://prose.io) 写作。由于 [prose.io](http://prose.io) 偶尔不稳定，最好在本地写好粘贴上去。
2. 在  [prose.io](http://prose.io)  上上传图片的时候，在 Image URl 里面填写这个地址 `images/posts/xxx.png` 其中 `xxx.png` 是图片的文件名。这样的好处是所有的图片都在 `images/posts` 文件夹中。
2. 语法是  kramdown。参考[这个页面](http://kramdown.gettalong.org/)。除了常用的语法，可能 `quote` 和 `footnote` 也比较常用。
3. 作者：OctoMiao，ErbB4，neuronstar


关于  metadata：每个文章需要包含（prose 中不需要上面和下面的横杠）。

```
layout: article
title: "文章题目"
modified: 2014-10-18
author: OctoMiao
toc: false
comments: true
categories: stories
summary: 显示在首页的一个简介
```

categories 目前包括 science, stories, til


-----

[skinny-bones](https://github.com/mmistakes/skinny-bones-jekyll) 修改的主题，沿用原作者的 MIT License. 

GitHub + [prose.io](http://prose.io) 可以像普通的带有数据库的博客（如 Wordpress）等一样实现在线编辑在线发布。

-----

# 写作


## workflow

登录 prose.io，链接 GitHub 账号，开始写吧，就这么简单。prose.io 专门为基于 jekyll 的写作做了优化，例如在编辑区域不会看到 meta data，而是需要在右侧的边栏有个 meta data 的按钮，就像正常的博客使用一样。




-----

# 简要文档

## GitHub 上的设置

改为自己的站点，只需要 Fork 这个 repository，然后将 repository 名称改为自己想要的名称。

> 一般而言，对于个人，想要使用 `username.github.io` 作为网站名称的，需要将 repository 改名为 `username.github.io` 并且将所有的文件放在 `master` 分支。GitHub 会自动将 `master` 分支中的 jekyll 内容编译为 html. 同样的道理，对于项目页面，jekyll 的源文件放在 `gh-pages` 分支中，GitHub 也会自动编译为 html 页面。

然后需要做以下修改：

- [ ] 按照上面的要求修改 repository 名称，并且将内容放在正确的分支中。
- [ ] 修改 `_config.yml` 中的内容，包括站点名称等等。其中 duoshuo 代码是需要去 http://duoshuo.com 注册一个账号并且创建一个网站的评论框，获取代号。
- [ ] 请替换现有的根目录下面的 favicon.ico, images 目录下的 logo-120x120.png，front-cover.jpg（显示在首页的背景图片） 等文件。`images/authors` 目录下的图像是用于作者头像，将头像放在这里，然后在下一步中更改配置文件。`images/mars` 目录中的文件是在示例 post 中用到的，可以删除。
- [ ] 在 `_data/authors.yml` 中修改作者列表（格式请参照文件中的例子 example）；在 `_data/footer.yml` 中修改网站底部的几个链接（可以添加，但是添加太多了就要换行了，不好看）；在 `_data/navigation.yml` 文件中修改站点顶部的链接（同时影响右侧边栏的滑出导航）。
- [ ] 其他的设置和自定义请阅读 jekyll 的官方文档。


> 如果你不了解 jekyll，简略说来：
> 
> 1. 所有的文章都在 `_posts` 目录下面。posts 的命名按照 jekyll 的要求，需要以日期格式开头。如果不这样命名，不会自动索引，但是依然会自动生成 html 页面，这时候需要手动索引。**我在目录中保留了几篇样稿，这样可以模仿格式，请在正式发布站点时删除。**
> 
> 2. `science`，`til`，`stories`，`history`，`club`，`about`，这些都是可以删除或者更改的文件目录。这些文件夹的名称是 post 的 category 名称，里面的 index.md 是索引页面，可以自己更改，我个人习惯在根目录建立这样的文件夹。也可以参考其他用法。
> 
> 3. `_posts` 目录中 posts 中的作者的代码需要与 `_data/authors.yml` 中的一致。例如在 `_posts` 目录中写了一篇名为 `2014-10-18-martian-sunset-phobos.md` 的新文章，其中 meta data 中设定作者为 `author: example` ，那么在 `_data/authors.yml` 中需要有 `example` 这个作者。
> 
> 4. 另外，所有的 html 文件会默认全部原封不动进入到 GitHub 生成的站点中。







-----

# Skinny Bones Jekyll Starter

Just a little something I'm using to jump start a site refresh. I like to think of it as a starter for building your own Jekyll site. I purposely keep the styling minimal and bare to make it easier to add your own flare and markup.

I'm currently using a variation of it on my personal website [Made Mistakes](http://mademistakes.com) with some modifications. To learn more about how to use the theme and install it check out the [Skinny Bones demo](http://mmistakes.github.io/skinny-bones-jekyll/) (*work in progress*).

![screenshot of Skinny Bones](http://mmistakes.github.io/skinny-bones-jekyll/images/skinny-bones-theme-feature.jpg)

---

## Notable Features

* Stylesheet built using Sass. *Requires Jekyll 2.x*
* Data files for easier customization of the site navigation/footer and for supporting multiple authors.
* Optional Disqus comments, table of contents, social sharing links, and Google AdSense ads.
* And more.