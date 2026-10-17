# dorsafsallami.github.io

Personal academic website of Dorsaf Sallami, published at <https://dorsafsallami.github.io/>.

The site is built with [Hugo](https://gohugo.io/) (extended, v0.115.4) using the small set of
templates in `layouts/` and the stylesheet in `assets/css/main.css`; no external theme is used.

## Updating content

| What | Where |
| --- | --- |
| About text, role line, Veracity box | `content/_index.md` |
| News | `data/news.yaml` (newest shown on the homepage, all on `/news/`) |
| Publications | `data/publications.yaml` (`selected: true` puts an entry on the homepage) |
| Talks | `data/talks.yaml` |
| Media & public writing | `data/media.yaml` |
| Teaching & mentorship | `content/teaching/_index.md` |
| Service | `content/services/_index.md` |
| Navigation, contact links, email | `config.yml` |
| CV, portrait, slides, posters | `static/` (use lowercase file names) |

Each data file starts with a comment describing its fields. Keep lists newest-first.

## Previewing locally

Install Hugo extended (e.g. `winget install Hugo.Hugo.Extended` or `brew install hugo`), then:

```sh
hugo server
```

and open <http://localhost:1313/>. `hugo --gc --minify` builds the site into `public/` (ignored by git).

## Publishing

Pushing to the `main` branch triggers `.github/workflows/hugo.yml`, which builds the site and
deploys it to GitHub Pages (repository **Settings → Pages → Source: GitHub Actions**).
