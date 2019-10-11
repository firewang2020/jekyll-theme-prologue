# Prologue - Jekyll Theme

[![Gem Version](https://badge.fury.io/rb/jekyll-theme-prologue.svg)](https://badge.fury.io/rb/jekyll-theme-prologue)

![Prologue Theme](assets/images/screenshot.png "Prologue Theme Screenshot")

本模板由 [Chris Bobbe](https://chrisbobbe.github.io) 从单站点响应式页面 [HTML5 UP](https://html5up.net/prologue) 改版而成，使其支持多页面，并增加了固定导航栏。在此基础上，我们还增加了站点统计，font-awesome icon的外部支持，gitalk评论，mathjax显示数学公式。

**Demo**: https://chrisbobbe.github.io/jekyll-theme-prologue/

**New Demo:**  https://firewang.github.io/jekyll-theme-prologue/

# 配置项

1. 直接 Fork 或者 clone the [GitHub repository]
2. 修改仓库名称为你想要设置的站点名称
3. 配置 `_config.yml` 
   1.  `url` and `base_url` 你的网站的信息
   2. 头像 `avatar: path/to/your/avatar.jpg`  ，目前路径`avatar: assets/images/avatar.jpg` (48x48 pixels 最佳)
   3. Gitalk生成你自己仓库的clientID 和clientSecret

# 生成主页面

1. **Your `_config.yml` file must include the following line or your homepage won't work**: `collections: [sections]`. This tells Jekyll to look in the _sections folder (which you will create) for your content and render it all on one page.

2. **Create a `_sections` folder** in your project's root directory and start adding content to your homepage. Set a cover photo in any of the sections by adding `cover-photo: path/to/photo.jpg` and `cover-photo-alt: your alt text here` to the section's frontmatter. Sample content is provided in the [GitHub repository](https://github.com/chrisbobbe/jekyll-theme-prologue/tree/master/_sections).

主页面下的分页面需要将html或者markdown文件放置于 `_sections` 目录下. 其他配置项参考 [frontmatter](https://jekyllrb.com/docs/frontmatter/):
- `title`：页面名称（必填）
- `order`：页面排序（必填）
- `cover-photo` (optional; 背景图片. Example: `assets/images/banner.jpg`)
- `cover-photo-alt` (required if using a cover photo. Describes the photo for screen readers and SEO; e.g. "Dome of Light art installation, Kaohsiung, Taiwan")
- `icon` (optional; see [Font Awesome](https://fontawesome.com/icons) for icon codes. Example: `fa-github`)
- `icon-style` (optional; "solid" is default, "regular" for outline style icons, or "brands" for logos)
- `auto-header` (optional; "use-title" is default, "none" for no header, or custom header text)
- `hide` (optional; if `true`, the section won't appear)

# 记录博客

在`_posts` 下的markdown文件都会被解析为文档页面（ [this Jekyll Docs page](https://jekyllrb.com/docs/posts/) ），可以自行选择使用哪个页面模板进行解析，blog或者post，一般选择post 。博客文章内容的主页面在`主站地址/blog.html` 下:

```
---
layout: blog
title: My Blog
author: yourname
mathjax: false
---
```



# 增加页面

在根目录增加 .html 或者 .md 文件，即会在左侧导航栏生成一个新主页面. 在文件内标示layout为page即可:

```
---
title: My New Page
layout: page
---
```

对页面的配置项：
- `subtitle` ：副标题
- `order` ：排序，如果还有其他页面，这里控制所有页面的显示顺序，（填1，2，3…）
- `icon` : 选择你喜欢的icon [Font Awesome](https://fontawesome.com/icons),  Example: `fa-github`，可不填
- `icon-style`：icon样式 (可选; "solid" is default, "regular" for outline style icons, or "brands" for logos)
- `hide`：是否显示页面link (可选; if `true`, 在导航栏不会显示link)

其他的SEO, this theme also lets you add `permalink` (see [Jekyll Docs](https://jekyllrb.com/docs/permalinks/#where-to-configure-permalinks)), `robots` (string, e.g. "noindex, nofollow"), and `canonical` (boolean; true is default) to any page or post.

# Contributing

Please feel free to submit issues and feature requests!

# Credits

Original README from HTML5 UP:

```
Prologue by HTML5 UP
html5up.net | @ajlkn
Free for personal and commercial use under the CCA 3.0 license (html5up.net/license)


This is Prologue, a simple, single page responsive site template. It features a
clean, minimalistic design and a sticky sidebar with navigation-linked scrolling.

Demo content images* are courtesy of the ridiculously talented Felicia Simion. Check out
more of her amazing work over at deviantART:

http://ineedchemicalx.deviantart.com/

(* = Not included! Only meant for use with my own on-site demo, so please do NOT download
and/or use any of Felicia's work without her explicit permission!)

Demo banner images* courtesy of Unsplash, a radtastic collection of CC0 (public domain)
images you can use for pretty much whatever.

(* = Not included)

AJ
aj@lkn.io | @ajlkn

PS: Not sure how to get that contact form working? Give formspree.io a try (it's awesome).


Credits:

	Demo Images:
		Felicia Simion (ineedchemicalx.deviantart.com)
		Unsplash (unsplash.com)

	Icons:
		Font Awesome (fortawesome.github.com/Font-Awesome)

	Other
		jQuery (jquery.com)
		html5shiv.js (@afarkas @jdalton @jon_neal @rem)
		CSS3 Pie (css3pie.com)
		background-size polyfill (github.com/louisremi)
		Respond.js (j.mp/respondjs)
		jquery.scrolly (@ajlkn)
		jquery.scrollzer (@ajlkn)
		Skel (skel.io)
```
