# pipo-seminar.github.io

Website of **PIPO: Privacy, Informal Proofs & Open problems** (Monday 7 December 2026, PariSanté Campus).

It is a plain [Jekyll](https://jekyllrb.com) site with no theme, so GitHub Pages builds it on its own.

## What to edit

| To change…                                  | Edit                     |
| ------------------------------------------- | ------------------------ |
| Date, room, address, contact email, title   | `_config.yml`            |
| The program (talks, times, abstracts)       | `_data/schedule.yml`     |
| Organizers (affiliations, links, photos)    | `_data/organizers.yml`   |
| Text of the home page                       | `index.md`               |
| Text around the schedule                    | `program.md`             |
| Colors and layout                           | `assets/css/style.css`   |

You can edit these files straight from github.com (pencil icon). The site rebuilds about a minute after each commit.

### Adding a talk

In `_data/schedule.yml`, fill in an existing `type: talk` entry:

```yaml
- time: "10:10"
  end: "10:50"
  type: talk
  title: "Auditing differentially private training"
  speaker: "Jane Doe"
  speaker_url: "https://example.org/~jane"
  affiliation: "Inria"
  abstract: >-
    One paragraph of abstract. *Markdown* works here.
  slides: /assets/slides/doe.pdf   # optional: put the PDF in assets/slides/
```

Empty fields are not displayed. A talk with no title is shown as "To be announced".

### Organizer photos

Put square images in `assets/img/organizers/` and set e.g. `photo: /assets/img/organizers/valentin.jpg`.

### Adding a page

Create `something.md` with this header, then add it to `nav` in `_config.yml`:

```markdown
---
title: Something
permalink: /something/
---

Your text in Markdown.
```

## Preview locally

Requires Ruby (`brew install ruby` on macOS).

```sh
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>. Restart the server after editing `_config.yml`.

## Publishing

In the repository settings on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`. The site is served at <https://pipo-seminar.github.io>.
