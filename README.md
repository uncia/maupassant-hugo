# maupassant-hugo
Maupassant theme, ported to Hugo.

[中文文档](README_zh.md)

# Configuration

A simple sample:

```toml
baseURL = "https://blog.mynook.info"
languageCode = "zh-CN"
title = "My Nook"
hasCJKLanguage = true
theme = "maupassant-hugo"
enableRobotsTXT = true
PaginatePath = "page"

[params]
    description = "What else did you expect me to say?"

[[params.links]]
    name = "比尔盖子 博客"
    url = "https://tomli.blog/"
    title = "代码如诗，人生无限。"

[author]
    name = "Joker Qyou"
    homepage = "https://mynook.info"
```

The above configuration was excerpted from my blog.

## Basics

`baseURL` sets the base URL for your whole block, every permanent link is based on it.
`theme = "maupassant-hugo"` is required to enable this theme.
`title` sets the title of your blog.
The `description` parameter in `[params]` block specifies a short message to be displayed under your blog name. In some other themes it is referenced as `subtitle`.

## Links

You can add as many links as you like by adding `[[params.links]]` blocks. In which:

- `name` is displayed as link text;
- `url` sets the link URL;
- `title` is used for, well, link title: short text that shows upon mouse hover;

## Author

The `[author]` block is for fallback use only. If a post has `author: "My Name"` in its front matter, the value `My Name` will be used as author name. Otherwise the `[author]` block in site config will be used.

# Analytics

As a reader / user of the Internet I hate tracking, because we deserve privacy. But as a blogger I was always trying out for new and more accurate tracking / analytics product.

At last I decided to let go. I want my readers to have privacy. Other Hugo themes (or Hugo itself) might have Google Analytics or other analytics product integrated. But I decided not to use them by default. That's why this theme **by default** does not track you.
