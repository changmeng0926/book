# README

[http://gitbook.zhangjikai.com/plugins.html]: 官网 '实例'

#### 安装

```bash
npm install gitbook-cli -g
```

#### 初始化

```bash
gitbook init
```

#### 开启服务

```bash
gitbook serve
```

#### 安装插件

```bash
gitbook install
```

#### 打包

```bash
gitbook build
```

### 目录结构

```
.
├── book.json
├── README.md
├── SUMMARY.md
├── chapter-1/
|   ├── README.md
|   └── something.md
└── chapter-2/
    ├── README.md
    └── something.md
```

#### book.json

```bash
存放配置信息
```

#### Summary

概要文件主要存放 GitBook 的文件目录信息，左侧的目录就是根据这个文件来生成的，默认对应的文件是 `SUMMARY.md`，可以在 `book.json` 重新定义该文件的对应值。

```
# Summary
* [Introduction](README.md)
* [Part I](part1/README.md)
    * [Writing is nice](part1/writing.md)
    * [GitBook is nice](part1/gitbook.md)
* [Part II](part2/README.md)
    * [We love feedback](part2/feedback_please.md)
    * [Better tools for authors](part2/better_tools.md)
```

### 配置

```json
"title" : 设置书本的标题
"author" : 作者的相关信息
"description" : 本书的简单描述
"language" : 使用语言
"gitbook" : 指定版本
"root": 指定存放 GitBook 文件（除了 book.json）的根目录
"links" : {	//	在左侧导航栏添加链接信息
    "sidebar" : {
        "Home" : "http://zhangjikai.com"
    }
}
"styles": {	//	自定义页面样式， 默认情况下各generator对应的css文件
    "website": "styles/website.css",
    "ebook": "styles/ebook.css",
}
"plugins": [ //	配置使用的插件	如果要去除自带的插件， 可以在插件名称前面加-
    "-search"
]
"pluginsConfig": { //	配置插件的属性
    "fontsettings": {
        "theme": "sepia",
        "family": "serif",
        "size":  1
    }
}
```
