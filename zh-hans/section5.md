## 奇技淫巧

### 变量

在 `book.json` 定义变量：

```json
{
    "variables": {
        "host": "jill.org",
        "authors": [
            { "name": "Samy" },
            { "name": "Aaron" }
        ]
    }
}
```

在 Markdown 文件中使用：

```md
当前主机为 {{ book.host }}

当前文件为 {{ file.path }}，修改时间 {{ file.mtime }}
GitBook 构建版本号 {{ gitbook.version }}

{% for author in book.authors %}
    * {{ author.name }}
{% endfor %}

{% if book.host == "jill.org" %}

{% else %}

{% endif %}
```

### 转义大括号

```md
{% raw %}
    这里不会有 {{ 任何输出 }}
{% endraw %}
```

### 模板

```md
{% block header %}
# 默认开头...
{% endblock %}

{% block content %}
# 默认内容...
{% endblock %}

{% block footer %}
# 默认结尾
{% endblock %}
```

使用

```md
{% extends "template/content.md" %}

{% block content %}
重写的内容
{% endblock %}
```

### 内容引用

```md
{% include "./test.inc.md" %}
{% include "git+https://github.com/bala/bala#1.0.1" %}
{% include book.var_of_doc %}
```

### 指定版本

```shell
git clone https://github.com/GitbookIO/gitbook.git
cd gitbook && npm install && cd ..
gitbook versions:link gitbook
```

取消

```shell
gitbook versions:uninstall latest
```

