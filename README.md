# hugo-theme-自定义教程
hugo自定义主题教程的demo

从一句话说起   

> everything in Hugo is a Page

这个是hugo的一个主旨, 意思是我们看到的每个静态页面都有一个对应的markdown文件.

hugo通常用来创建个人博客, hugo通过用户编写markdown文件来生成静态网站, 用户想在博客网站上添加什么页面, 只用编写对应的markdown文件就可以了.hugo根据markdown文件的类型寻找对应的页面模板来生成对应的静态页面. 一切就是这么简单. 如果想构建自己的网站主题, 我们只需要搞清楚markdown文件和模板页面的对应关系就可以了. 另外, 用户的markdown文件的目录结构一般就代表最终网站的结构.

## hugo工作目录的结构
``` bash
├── archetypes
│   └── default.md
├── config.toml
├── content
├── data
├── layouts
│   ├── _default
│   │   ├── list.html
│   │   └── single.html
│   └── index.html
├── public
│   ├── categories
│   │   └── index.xml
│   ├── index.xml
│   ├── sitemap.xml
│   └── tags
│       └── index.xml
├── resources
│   └── _gen
│       ├── assets
│       └── images
├── static
└── themes
    └── mytheme
        ├── archetypes
        │   └── default.md
        ├── layouts
        │   ├── 404.html
        │   ├── _default
        │   │   ├── baseof.html
        │   │   ├── list.html
        │   │   └── single.html
        │   ├── index.html
        │   └── partials
        │       ├── footer.html
        │       ├── header.html
        │       └── head.html
        ├── LICENSE
        ├── static
        │   ├── css
        │   └── js
        └── theme.toml
```
上面的目录结构就是hugo的工作目录, 或者叫网站骨架, hugo就是根据这里的东西生成网站的, 结构看上去很多, 但我们主要了解两个目录和一个文件就可以了.

- content目录: 这个目录就是用户存放markdown文件的地方, 他的目录结构就是网站的结构    
- themes目录: 这个目录就是存放页面模板的地方, 所有的markdown文件在这里都有对应的模板页面
- config.toml文件: 这个配置文件主要用来指导hugo如何生成网站的.比如生成网站时使用那个主题

## 创建主题的命令
``` bash
hugo new theme <主题名称>  # 实际使用的时候没有尖括号(<>)
```
hugo会根据命令行中的模板名称, 在themes目录中创建同名的目录, 然后再目录中生成基本的模板文件.

## 文章目录
hugo这种模式的个人博客系统, 在一定程度上燃起了我写博客的积极性, 以前也写, 在一些博客平台上, 因为做技术的总是想搞个自己的博客, 也弄过一些开源的博客系统, 总是觉得很麻烦, 各种配置, 安装, 弄皮肤. 最后反而把写作这事情搞丢了, 真是有点本末倒置. 而hugo却可以让写作时丝般顺滑, 倒腾皮肤时随心所欲. 这个系列的文章就是在倒腾hugo的过程中的一些记忆, 前面有按hugo上的一些技术点写了些文章, 感觉自己都有点看不懂, 这次换了个角度, 从实际需求的角度写, 比如想定义首页的样式, 想定义文章页面的样式, 这样也许更能把思路理清, 也更加实用.

- [x] [自定义hugo主题--概述](https://hugo.aiaide.com/post/%E8%87%AA%E5%AE%9A%E4%B9%89hugo%E4%B8%BB%E9%A2%98-%E6%A6%82%E8%BF%B0/)
- [ ] [自定义hugo主题--从首页开始](https://hugo.aiaide.com/)
- [ ] [自定义hugo主题--内容页](https://hugo.aiaide.com/)
- [ ] [自定义hugo主题--内容列表页](https://hugo.aiaide.com/)
- [ ] [自定义hugo主题--导航菜单](https://hugo.aiaide.com/)
- [ ] [自定义hugo主题--标签和分类](https://hugo.aiaide.com/)
