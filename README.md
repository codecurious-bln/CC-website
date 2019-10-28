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

## Adding an event

Create a `YYYY-MM-DD-title-to-display.markdown` file inside `_events` folder. Have a look at other files for example: `_events/2019-09-21-code-and-cake.markdown`
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
