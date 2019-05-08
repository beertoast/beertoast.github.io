---
layout: post
title:  "如何使用`Github Pages` 快速搭建博客？"
date:   2019-05-06
categories: github
tags: jekyll github-pages
mathjax: true
---

* content
{:toc}
### 理解
1. 你得有一个项目，然后在项目的`Settings>GitHub Pages>Source`中选择你的`Github Pages`来源。![]({{site.url}}/images/github-pages-setting.png)
2. `Github Pages`是支持`jekyll`的，在上一步中，如果你选择的是`master`分支，确保你的项目文件结构和`jekyll`项目保持一致；如果你选择的是`docs\`,确保该文件夹结构与`jekyll`一致。
3. 完成上面两步，每次你`commit`你的代码。`Github Pages`会自动生成/更新静态页面。

### 具体步骤
所以，我们只要`clone` or `download`别的`Github Pages`项目，修改样式，变成我们自己的项目就好了。当然，有兴趣，有时间，你也可以自己安装`jekyll`,从头开始。
1. 从[Supported themes](https://pages.github.com/themes/)或者[jekyll-theme](https://github.com/topics/jekyll-theme)选择一个主题，然后`fork`或者`clone`或者`downlod`。(ps:本站使用的是[gaohaoyang.github.io](https://github.com/Gaohaoyang/gaohaoyang.github.io))
2. 本地开发。
    - 安装[jekyll](https://jekyllrb.com/docs/installation/)环境。
    - 在你的项目根目录，编辑`Gemfile`文件，内容如下
    ````
    source 'https://rubygems.org'
    gem 'github-pages', group: :jekyll_plugins
    ````
    - 安装依赖。
    ````bash
    $ bundle install
    > Fetching gem metadata from https://rubygems.org/............
    > Fetching version metadata from https://rubygems.org/...
    > Fetching dependency metadata from https://rubygems.org/..
    > Resolving dependencies...
    ````
    - 运行如下命令，在浏览器访问`http://127.0.0.1:4000`。
    ````bash
    $ bundle exec jekyll serve
    ...
    Server address: http://127.0.0.1:4000/
    Server running... 
    press ctrl-c to stop.
    ````
3. 使用`SublmeText3`编辑markdown文件，安装[MarkdownEditing](https://github.com/SublimeText-Markdown/MarkdownEditing)插件。
4. 到了这里，你就照葫芦画瓢发布文章就行了，然后`commit`。`_posts`文章的目录。

