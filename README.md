# [gitbook](https://xiexieni1992.github.io/gitbook/)
## 1、介绍

​	这是一个基于GitBook + Typora + Git文档托管解决方案！

​	

## 2、使用gitbook

### 2.1 安装并初始化gitbook

```
npm install -g gitbook-cli
gitbook init
```

  执行完后。会有以下两个文件

```
README.md —— 书籍的介绍写在这个文件里
SUMMARY.md —— 书籍的目录结构在这里配置
```

### 2.2 Typora 编写SUMMARY.md

```
* [前言](README.md)
* 正文
  * [段落](src/Todo01/README.md)
  * [段落](src/Todo02/README.md)
  * [段落](src/Todo03/README.md)
  * [段落](src/Todo04/README.md)
* [后记]
```

```
├─docs // github 静态资源文件夹
│  ├─.gitignore
│  ├─gitbook
│  │  ├─fonts
│  │  │  └─fontawesome
│  │  ├─gitbook-plugin-fontsettings
│  │  ├─gitbook-plugin-highlight
│  │  ├─gitbook-plugin-lunr
│  │  ├─gitbook-plugin-search
│  │  ├─gitbook-plugin-sharing
│  │  └─images
│  └─src
│      ├─Todo01
│      ├─Todo02
│      ├─Todo03
│      └─Todo04
├─src
│  ├─Todo01
│  ├─Todo02
│  ├─Todo03
│  └─Todo04
└─_book // 本地服务器文件夹
    ├─.gitignore
    ├─gitbook
    │  ├─fonts
    │  │  └─fontawesome
    │  ├─gitbook-plugin-fontsettings
    │  ├─gitbook-plugin-highlight
    │  ├─gitbook-plugin-livereload
    │  ├─gitbook-plugin-lunr
    │  ├─gitbook-plugin-search
    │  ├─gitbook-plugin-sharing
    │  └─images
    └─src // 源文件夹
        ├─Todo01
        ├─Todo02
        ├─Todo03
        └─Todo04
```



保存后，命令行工具运行以下命令：

```
gitbook init
```

GitBook 会查找 SUMMARY.md 文件中描述的目录和文件，如果没有则会将其创建。

### 2.3 本地运行gitbook

```
gitbook serve --port 8088
```

执行 `gitbook serve` 来预览这本书籍,出现 Serving book on [http://localhost:8088](http://localhost:8088/)，浏览器进行本地访问。

### 2.4 构建gitbook

```
gitbook build ./ docs
```

### 2.5 其它格式

```
gitbook pdf ./ ./xxx.pdf
gitbook epub ./ ./xxx.epub
gitbook mobi ./ ./xxx.mobi
```

## 3、Git托管静态网站

进入github=>Setting=>GitHub Pages=>Source

```
master branch /docs dolder
```

