# Hax0r Hugo Theme

A minimalistic dark theme for your [Hugo](https://gohugo.io) site.

## Installation

```bash
cd <your_hugo_site>
git submodule add https://git.goatpr0n.de/blog/hugo-theme-hax0r.git themes/hax0r
```

## Usage

The theme supports the configuration of colors through editing `config.{toml,yaml}`.

**TOML**
```toml
[params.style]
backgroundColor = '#04080f'
textColor = '#dae3e5'
borderColor = '#dae3e5'
anchorColor = '#507dbc'
anchorActiveColor = '#bbd1ea'
anchorHoverColor = '#bbd1ea'
preTextColor = '#f8f8f2'
preBackgroundColor = '#272822'
```

**YAML**

```yaml
params:
  style:
    backgroundColor: '#04080f'
    textColor: '#dae3e5'
    borderColor: '#dae3e5'
    anchorColor: '#507dbc'
    anchorActiveColor: '#bbd1ea'
    anchorHoverColor: '#bbd1ea'
    preTextColor: '#f8f8f2'
    preBackgroundColor: '#272822'
```

## Configuration example

```yaml
baseURL: 'https://goatpr0n.farm/'
languageCode: 'en-us'
title: 'A farm without animals'
theme: 'hax0r'

menu:
  main:
    - name: Blog
      pageRef: /
      weight: 10
    - name: Links
      pageRef: /links
      weight: 20
    - name: Tags
      pageRef: /tags
      weight: 90
    - name: Categories
      pageRef: /categories
      weight: 90

params:
  style:
    backgroundColor: '#04080f'

permalinks:
  blog: /:year/:month/:slug/

taxonomies:
  category: categories
  tag: tags

sitemap:
  changefreq: "monthly"
  filename: "sitemap.xml"
  priority: 0.5
```
