# eadame.ovh

Personal site built with [Zola](https://www.getzola.org/) (single binary, no Ruby/Node).
English is the default language (`/`), Brazilian Portuguese lives under `/pt-br/`.

## Run locally

Install Zola (https://www.getzola.org/documentation/getting-started/installation/), then:

```sh
zola serve      # http://127.0.0.1:1111, live reload
zola build      # static output in public/
```

## Deploy

Push to `master`. `.github/workflows/deploy.yml` builds with Zola and publishes `public/` to the `gh-pages` branch
(Settings → Pages → "Deploy from a branch" → `gh-pages`, as before). `static/CNAME` keeps the custom domain.

## Where things live

| To change…                        | Edit                                                      |
| --------------------------------- | --------------------------------------------------------- |
| About text                        | `content/_index.md`, `content/_index.pt-br.md`            |
| News                              | `data/news.toml` (add a `[[news]]` block, both languages) |
| Publications                      | `data/papers.bib` (`selected={true}` shows on home)       |
| Teaching                          | `data/courses.toml`                                       |
| Outreach (posters/talks/courses)  | `data/outreach.toml` (`/presentations/` redirects here)   |
| Repos                             | `data/repos.toml`                                         |
| CV                                | replace `static/assets/pdf/cv.pdf`                        |
| Menu / UI strings, both languages | `config.toml` (`[translations]`, `[languages.pt-br.translations]`) |
| Look                              | `static/style.css` (a few lines) and `templates/`         |
