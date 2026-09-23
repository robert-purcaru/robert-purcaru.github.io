# robert-purcaru.github.io

Personal website, built with [Jekyll](https://jekyllrb.com/) on the
[academicpages](https://github.com/academicpages/academicpages.github.io)
template (a fork of Minimal Mistakes). Deployed by GitHub Pages from the
default branch.

## Where things live

The site is one scrolling page (`_pages/about.md`). The nav links in
`_data/navigation.yml` jump to its sections by id: `#about`, `#publications`,
`#industry`, `#projects`.

| What | File |
| --- | --- |
| Site title, your name, sidebar links | `_config.yml` |
| Nav bar (links to sections) | `_data/navigation.yml` |
| The page itself and its section order | `_pages/about.md` |
| Education and Industry Experience rows | `_data/experience.yml` (logos in `images/logos/`) |
| Publications | `_publications/` (one file per paper) |
| Projects | `_projects/` (one file per entry; photos in `images/projects/`) |
| Site-specific styles | `_sass/_custom.scss` |
| Education, CV pages (hidden from nav for now) | `_pages/education.md`, `_pages/cv.md` |

## Adding content

**A paper** — copy one of the files in `_publications/`. Papers are listed
newest first by `date`; the body text is the short description shown under the
title, and `paperurl` is where "Full paper" links.

**A project** — copy one of the files in `_projects/` (keep
`section: projects`) and set `order` to place it. Use `images:` for photos on the left (two photos sit side
by side), or `icon:` (a Font Awesome class) when there's no photo. `links:` adds
links under the description.

**A job or degree** — add an entry under `industry:` or `education:` in
`_data/experience.yml`. `details:` (Markdown) is optional text shown under the
row, and entries appear in the order they're listed. Drop a logo in `images/logos/`, or leave `logo` blank and set `initials`
for a text tile.

**Your photo** — `images/profile.jpg`, set by `author.avatar` in `_config.yml`.

**Your CV PDF** — put it at `files/cv.pdf` and uncomment the download link at the
top of `_pages/cv.md`.

## Running it locally

```sh
bundle install
bundle exec jekyll serve -l -H localhost
```

Then open <http://localhost:4000>. `_config.yml` is *not* hot-reloaded — restart
the server after changing it.

## Images

Strip metadata from photos before committing them (EXIF can include GPS
location). Re-saving with Pillow, as below, keeps only the pixels:

```sh
python3 -c "from PIL import Image; import sys; im=Image.open(sys.argv[1]); im.save(sys.argv[1], quality=85)" images/projects/new.jpg
```
