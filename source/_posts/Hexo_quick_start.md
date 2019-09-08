title: Hexo快速上手
author: 小宋是呢
tags:
  - hexo
categories: 
  - html
thumbnail: >-
  https://images.unsplash.com/photo-1514761261404-b98b1682cefd?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80
language: zh-CN
toc: true
top: true
date: 2019-09-08 10:46:00
---

Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

<!-- more -->

##### 安装

安装 Hexo 只需几分钟时间，若您在安装过程中遇到问题或无法找到解决方式，请提交问题，我会尽力解决您的问题。

###### 安装前提

安装 Hexo 相当简单。然而在安装前，您必须检查电脑中是否已安装下列应用程序：

* Node.js (Should be at least nodejs 6.9)
* Git

如果您的电脑中已经安装上述必备程序，那么恭喜您！接下来只需要使用 npm 即可完成 Hexo 的安装。

```bash
npm install -g hexo-cli
```

###### 安装 Hexo

所有必备的应用程序安装完成后，即可使用 npm 安装 Hexo。

```bash
npm install -g hexo-cli
```



#### 建站


安装 Hexo 完成后，请执行下列命令，Hexo 将会在指定文件夹中新建所需要的文件。

```bash
hexo init <folder>
cd <folder>
npm install
```

新建完成后，指定文件夹的目录如下：


```bash
├── _config.yml
├── package.json
├── scaffolds
├── source
|   ├── _drafts
|   └── _posts
└── themes
```
##### _config.yml

网站的 配置 信息，您可以在此配置大部分的参数。

##### package.json
应用程序的信息。EJS, Stylus 和 Markdown renderer 已默认安装，您可以自由移除。

```bash
package.json
{
  "name": "hexo-site",
  "version": "0.0.0",
  "private": true,
  "hexo": {
    "version": ""
  },
  "dependencies": {
    "hexo": "^3.8.0",
    "hexo-generator-archive": "^0.1.5",
    "hexo-generator-category": "^0.1.3",
    "hexo-generator-index": "^0.2.1",
    "hexo-generator-tag": "^0.2.0",
    "hexo-renderer-ejs": "^0.3.1",
    "hexo-renderer-stylus": "^0.3.3",
    "hexo-renderer-marked": "^0.3.2",
    "hexo-server": "^0.3.3"
  }
}
```

##### scaffolds

模版 文件夹。当您新建文章时，Hexo 会根据 scaffold 来建立文件。

Hexo的模板是指在新建的文章文件中默认填充的内容。例如，如果您修改scaffold/post.md中的Front-matter内容，那么每次新建一篇文章时都会包含这个修改。

##### source
资源文件夹是存放用户资源的地方。除 _posts 文件夹之外，开头命名为 _ (下划线)的文件 / 文件夹和隐藏的文件将会被忽略。Markdown 和 HTML 文件会被解析并放到 public 文件夹，而其他文件会被拷贝过去。

##### themes

主题 文件夹。Hexo 会根据主题来生成静态页面。

