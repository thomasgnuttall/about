# Thomas Nuttall

Deployment here - https://thomasgnuttall.github.io/about/

The site is built with [Jekyll](https://jekyllrb.com/). GitHub Pages rebuilds it on every push to `gh-pages`, so content changes only need an edit to a data file and a push.

## Adding content

| To add | Edit | Notes |
| --- | --- | --- |
| A paper or talk | `_data/publications.yml` | Add it under the right heading, newest first. Punctuation is added for you. |
| A performance | `_data/performances.yml` | Sorted by date automatically. |
| A song or album | `_data/music.yml` | Use a `youtube` or `spotify_album` ID. |
| A design | `_data/design.yml` | Put the image in `assets/images/design/` first, about 1400px wide. |
| A "Recent Content" video | `_data/recent.yml` | |
| A footer link | `_data/contact.yml` | |
| The about text | `_includes/sections/about.html` | |
| A new tab | `_data/sections.yml` | Also create `_includes/sections/<id>.html`. |

The site title and description are in `_config.yml`. Each data file has a comment at the top describing its format.

## Layout

```
_config.yml      site title, description and build settings
_data/           the content
_includes/       page parts: head, header, footer, citation format, embeds
  sections/      one template per tab
_layouts/        the page shell
assets/          CSS, JavaScript and images
index.html       renders each tab listed in _data/sections.yml
```

## Previewing locally

This needs Ruby 3 or later, and only the first command has to be run once:

```
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000. The built site goes to `_site/`, which is ignored by git.
