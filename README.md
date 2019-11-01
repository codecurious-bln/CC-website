# code curious Website Project

This is a community project to build the [code curious website](https://codecurious-bln.github.io/CC-website/). It is using [Jekyll](https://jekyllrb.com).

## Installation

Go to your terminal and run:

    git clone git@github.com:codecurious-bln/CC-website.git
    # or
    git clone https://github.com/codecurious-bln/CC-website.git

    bundle
    bundle exec jekyll serve

…and then go to http://localhost:4000/

## Adding a post

Create a `YYYY-MM-DD-title-to-display.markdown` file inside `{language}/_posts` folder. Have a look at other files for example: `en/_posts/2019-09-21-code-and-cake.markdown`

Inside each post please check the [Front Matter](https://jekyllrb.com/docs/front-matter/) which looks like something below. If you leave the `i18n_key` blank, it will not look for files in other languages, with the same _internationalization_ key. The categories help filter the posts by language and also topic. Current the `en/_posts` and `de/_posts` link to blog posts, but also event posts.
```
---
i18n_key: code_and_cake_2030
categories: de events
title: Haha
---
```

For adding a blog post, as opposed to say an event, it is similar but you would change the categories slightly e.g

```
---
i18n_key: unique_blog_key
categories: es blog
title: Yay a new blog post!
---
```

## Adding a page
Most pages should be sorted into their respective language folder (`en`/`de`), exceptions may include pages like the 404 error page. If you want to link to a different translation of the page, make sure both pages have the same _internationalization_ key as shown below, while allowing different titles and urls automatically. If you need to override a url regardless of their location, you can set it with `permalink: /whatever`

```
# inside `en/about.markdown`
---
title: About
i18n_key: about
---

# inside `de/about.markdown`
---
title: Veranstaltungen
i18n_key: about
---
```

## Add a page to header
Inside each of the page front matters make sure they have a title
```markdown
# en/about.markdown
title: "About"
```
Inside `_config.yml` update
```yaml
header_pages:
  - en/about.markdown
  - en/events.markdown
```

## Code of Conduct
See the code of conduct [here](CODE_OF_CONDUCT.md).

## Social Media

[![@codecurious_bln](https://imgur.com/c8T4FEm.png)](https://twitter.com/codecurious_bln) [@codecurious_bln](https://twitter.com/codecurious_bln)

[![@code.curious](https://imgur.com/z11KUEi.png)](https://www.instagram.com/code.curious/) [@code.curious](https://www.instagram.com/code.curious/)