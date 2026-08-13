# robert-purcaru.github.io

Personal website, built with [Jekyll](https://jekyllrb.com/) on the
[academicpages](https://github.com/academicpages/academicpages.github.io)
template (a fork of Minimal Mistakes). Deployed by GitHub Pages from the
default branch.

## Where things live

| What | File |
| --- | --- |
| Site title, your name, sidebar links, collections | `_config.yml` |
| Top nav bar | `_data/navigation.yml` |
| About (the homepage) | `_pages/about.md` |
| Projects list page | `_pages/projects.html` |
| Publications list page | `_pages/publications.html` |
| Education | `_pages/education.md` |
| CV | `_pages/cv.md` |
| One file per publication | `_publications/` |
| One file per project | `_projects/` |
| Images (photo, screenshots, favicon) | `images/` |
| Downloadables (CV PDF, papers) | `files/` |

## Adding content

**A publication** — copy `_publications/2026-01-01-example-publication.md` to a
new file named `YYYY-MM-DD-short-slug.md`. The date in the filename controls the
ordering. Set `category` to `books`, `manuscripts`, or `conferences`; those
headings come from `publication_category` in `_config.yml`.

**A project** — copy `_projects/example-project.md`. The `excerpt` field is what
shows on the Projects list; the body shows on the project's own page.

**Your photo** — put it in `images/` and point `author.avatar` in `_config.yml`
at the filename.

**Your CV PDF** — put it at `files/cv.pdf` and uncomment the download link at the
top of `_pages/cv.md`.

## Running it locally

```sh
bundle install
bundle exec jekyll serve -l -H localhost
```

Then open <http://localhost:4000>. `_config.yml` is *not* hot-reloaded — restart
the server after changing it.

## Housekeeping

`_to_delete/` holds the template's sample content (demo posts, talks, teaching,
portfolio items, the markdown guide). Nothing references it and Jekyll ignores
underscore-prefixed directories, so it is safe to delete the whole folder:

```sh
git rm -r _to_delete
```
