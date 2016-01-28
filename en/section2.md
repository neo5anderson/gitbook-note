## File System

#### Root

+ `book.json`: Configuration file, create it manually
+ `LANGS.md`: Languages description, create it manually
+ `README.md`: Introduction
+ `en/`: English content folder, by manually
+ `zh-hans/`: Simplified Chinese content folder, by manually
+ `_book/`: Build output folder

#### Content

+ `README.md`: Introduction
+ `SUMMARY.md`: Summary Index
+ `GLOSSARY.md`: Glossary list

#### _book

+ `index.html`: Language index page
+ `search_index.json`: search index file
+ `gitbook/`: scripts, resource and style files
+ `en/`: English content pages
+ `zh-hans/`: Simplified Chinese content pages

### Content info.

#### README.md

Content introductions

#### SUMMARY.md

The structure of chapters and subchapters of the book.

```md
# Summary

* [Chapter 1](section1/README.md)
    * [example 1](section1/example1.md)
    * [example 2](section1/example2.md)
* [Chapter 2](section2/README.md)
    * [example 1](section2/example1.md)
```

#### LANGS.md

Multi-Languages supported.

```md
* [中文](zh-hans/)
* [English](en/)
```

#### GLOSSARY.md

```md
# term
Definition for this term
```

#### book.json

+ gitbook: version, a [SEMVER](http://semver.org/) format condition
+ title: use `README.md` first title by default
+ description: use `README.md` first paragraph by default
+ isbn: ISBN
+ language: use `en` by default
+ direction: use `rtl` by default
+ styles: css, can change: website, ebook, pdf, mobi, epub
+ plugins: list of plugins
+ pluginsConfig: plugins specific configurations
+ structure: override files paths
+ variables: defines variables values
+ pdf: specific customization like `headerTemplate`, `footerTemplate`

