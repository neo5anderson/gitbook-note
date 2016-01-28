## 文件系统

#### 根

+ `book.json`: 配置文件，需手动生成
+ `LANGS.md`: 语言描述文件，需手动生成
+ `README.md`: 简介描述文件
+ `en/`: 英文内容目录，需手动生成
+ `zh-hans/`: 简体中文内容目录，需手动生成
+ `_book/`: 组建后输出路径

#### 语言内容目录

+ `README.md`: 内容介绍
+ `SUMMARY.md`: 目录索引描述文件
+ `GLOSSARY.md`: 术语列表

#### _book

+ `index.html`: 语言索引页面
+ `search_index.json`: 搜索索引描述
+ `gitbook/`: 页面脚本、资源以及样式表
+ `en/`: 英文内容页面
+ `zh-hans/`: 简体中文内容页面

### 描述文件说明

#### README.md

内容介绍，会自动添加至输出的目录中

#### SUMMARY.md

定义内容结构，包含每个章节的列表和链接，比如：

```md
# 概述

这本书的目录

* [第一章](section1/README.md)
    * [实例 1](section1/example1.md)
    * [实例 2](section1/example2.md)
* [第二章](section2/README.md)
    * [实例 1](section2/example1.md)
```

#### LANGS.md

多语言描述文件，实例：

```md
* [中文](zh-hans/)
* [English](en/)
```

#### GLOSSARY.md

```md
# 术语
术语的解释或定义
```

#### book.json

+ gitbook: 版本号，格式为 [SEMVER](http://semver.org/)
+ title: 标题，默认使用 `README.md` 的第一个标题
+ description: 描述，默认使用 `README.md` 的第一段
+ isbn: ISBN
+ language: 文字语言，默认是 `en`
+ direction: 文字方向，默认是 `rtl`
+ styles: 样式表，可选 website, ebook, pdf, mobi, epub
+ plugins: 插件列表
+ pluginsConfig: 配置所有插件
+ structure: 重写文件结构路径
+ variables: 通过模板定义变量
+ pdf: 定制头尾模板，`headerTemplate`, `footerTemplate`

