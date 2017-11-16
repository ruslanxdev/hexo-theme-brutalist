# Brutalist

A minimalistic and brutal [Hexo](http://hexo.io) theme for a personal website, inspired [Cactus Dark](https://probberechts.github.io/cactus-dark/) theme, [Brutalist Websites](http://brutalistwebsites.com/) and [GitHub Styleguide](https://github.com/styleguide).

<!-- [Demo](https://ruslankhh.com/hexo-theme-brutalist/) -->

## Summary

- [General](#general)
- [Features](#features)
- [Install](#install)
- [Configuration](#configuration)
- [License](#license)

## General

- **Version** : 0.1.0
- **Compatibility** : Hexo 3 or later

## Features

- Fully responsive
- Disqus
- Googe analytics
- Font Awesome icons
- Pick your own code highlighting scheme
- Configurable navigation menu
- Projects list
- Simplicity

## Install

1. In the `root` directory:

  ```bash
  $ git clone https://github.com/ruslankhh/hexo-theme-brutalist.git themes/brutalist
  $ npm install hexo-pagination --save
  ```

2. Change the `theme` property in the `config.yml` file.

  ```yml
  theme: brutalist
  ```

3. Run: `hexo generate` and `hexo server`

## Configuration

### Navigation

Setup the navigation menu in the theme's `_config.yml`:

```yml
memu:
  Home: /
  Archives: /archives/
  About: /about/
  <link_name>: <link_url>
```

### Blog posts list on home page

You have two options for the list of blog posts on the home page:

- Show only the 5 most recent posts (default)

```yml
customize:
  show_all_posts: false
  post_count: 5
```

- Show all posts

```yml
customize:
  show_all_posts: true
```

### Projects list

Create a projects file `source/_data/projects.json`.

```json
[
  {
    "name": "Hexo",
    "url": "https://hexo.io/",
    "desc": "A fast, simple & powerful blog framework"
  },
  {
    "name": "Font Awesome",
    "url": "http://fontawesome.io/",
    "desc": "The iconic font and CSS toolkit"
  }
]
```

### Social media links

Brutalist can automatically add links to your social media accounts. Therefore, update the theme's `_config.yml`:

```
customize:
  social_links:
    github: <your_github_url>
    twitter: <your_twitter_url>
    <name>: <your_name_url>
```

where `<name>` is the name of a [Font Awesome icon](http://fontawesome.io/icons/#brand).

### RSS

Set the `rss` field in the theme's `_config.yml` to one of the following values:

1. `rss: false` will totally disable rss (default).
2. `rss: atom.xml` sets a specific feed link.
3. `rss:`leave empty to use the [hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed) plugin.

### Analytics

Add you Google Analytics `tracking_id` to the theme's `_config.yml`.

```yml
plugins:
  gooogle_analytics: 'UA-49627206-1' # Format: UA-xxxxxx-xx
```

### Comments

First, create a site on Disqus: [https://disqus.com/admin/create/](http://disqus.com/admin/create/).

Next, update the theme's `_config.yml` file:

```yml
plugins:
  disqus_shortname: SITENAME
```

where `SITENAME` is the name you gave your site on Disqus.

### Code Highlighting

Pick one of [the available colorschemes](https://github.com/probberechts/cactus-dark/tree/master/source/css/_highlight) and add it to the theme's `_config.yml`:

```yml
customize:
  highlight: <theme>
```

## Author

[Ruslan Khusnetdinov](https://github.com/ruslankhh)

## License
MIT
