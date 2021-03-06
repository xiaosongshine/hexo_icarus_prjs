title: Icarus简单配置
thumbnail: >-
  https://images.unsplash.com/photo-1468476396571-4d6f2a427ee7?ixlib=rb-1.2.1&auto=format&fit=crop&w=2044&q=32
author: 小宋是呢
abstract: Icarus的配置包括两部分：主题配置和后台配置。
password: 1234567890
message: 测试加密，密码 1-0
tags:
  - Icarus
categories:
  - theme
language: zh-CN
toc: true
top: false
date: 2019-09-07 20:54:00
---

####介绍

Icarus的配置包括两部分：主题配置和后台配置。

##### 主题配置

Icarus使用_config.yml文件进行全局页面布局，插件和窗口小部件设置。它将检查并验证配置文件，指出任何配置错误，并在不存在的情况下为您生成一个配置文件。您可以随时从*.spec.js文件themes/icarus/includes/specs夹中的文件检查规格。

<!-- more -->

默认主题配置包含以下部分：

* 网站首选项和页面元数据
* 顶部导航栏链接
* 页脚链接
* 文章显示设置
* 评论，分享和搜索插件设置
* 边栏小部件设置
* 其他显示和分析插件
* CDN设置

大多数设置都记录在_config.yml文件中。有关配置插件的更多详细信息，请参阅联机文档。


##### 后台配置

除了全局主题配置，您还可以在任何帖子中进行自定义。也就是说，您可以从帖子覆盖主题配置。假设您要在帖子中显示不同的导航栏菜单。要做到这一点，你只需要将navbar设置放在帖子的前面：

```bash
navbar:
    menu:
        Home: /
        Special!: /special
```

您在此处设置的配置仅适用于此帖子。此功能对于向特定受众显示自定义/优化页面非常有用。例如，您可以根据页面查看器的国家/地区和语言启用更快的CDN或本地化评论服务。