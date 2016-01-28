## Tricks

### Variables

In `book.json`:

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

In markdown files:

```md
Host is {{ book.host }}

File is {{ file.path }}, modify time: {{ file.mtime }}
GitBook version: {{ gitbook.version }}

{% for author in book.authors %}
    * {{ author.name }}
{% endfor %}

{% if book.host == "jill.org" %}

{% else %}

{% endif %}
```

### Escaping

```md
{% raw %}
    this will {{ no be processed }}
{% endraw %}
```

### Inheritance

```md
{% block header %}
# Default Header ...
{% endblock %}

{% block content %}
# Default Content ...
{% endblock %}

{% block footer %}
# Default Footer ...
{% endblock %}
```

Usage:

```md
{% extends "template/content.md" %}

{% block content %}
Overrided content
{% endblock %}
```

### Content References

```md
{% include "./test.inc.md" %}
{% include "git+https://github.com/bala/bala#1.0.1" %}
{% include book.var_of_doc %}
```

### Latest Version

```shell
git clone https://github.com/GitbookIO/gitbook.git
cd gitbook && npm install && cd ..
gitbook versions:link gitbook
```

uninstall

```shell
gitbook versions:uninstall latest
```

