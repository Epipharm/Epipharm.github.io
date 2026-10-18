# Epigenetic Pharmacology (EpiPharm) Lab — website

Source of <https://epipharm.github.io>, the homepage of the Epigenetic Pharmacology (EpiPharm)
laboratory (PI: Hyunsoo Rho, College of Pharmacy, Ewha Womans University).
Built with [Jekyll](https://jekyllrb.com/) and the [al-folio](https://github.com/alshedivat/al-folio) starter,
hosted on GitHub Pages.

## How the site is updated

Edit files on the `main` branch (directly on GitHub: open the file → pencil icon → **Commit changes**).
Every commit triggers the **Deploy site** action, which rebuilds the site into the `gh-pages` branch
(do not edit `gh-pages` by hand). The new version is live a few minutes later.

| To change…                      | Edit…                                                                                   |
| ------------------------------- | --------------------------------------------------------------------------------------- |
| Home-page text, address         | `_pages/about.md`                                                                       |
| Profile photo                   | replace `assets/img/prof_pic.jpg`                                                       |
| Publications                    | `_bibliography/papers.bib` (one BibTeX entry per paper; `selected = {true}` → home page) |
| Publication thumbnails          | images in `assets/img/publication_preview/` (file name = the entry's `preview` field)    |
| Accent colour (Ewha Green)      | `$purple-color` in `_sass/_variables.scss`                                              |
| Lab members                     | `_pages/people.md`                                                                      |
| Contact icons (Scholar, ORCID…) | `_data/socials.yml`                                                                     |
| Site title, name, colors, flags | `_config.yml`                                                                           |

Notes

- Author markers in `papers.bib`: `*` after a last name = equal contribution, `†` = co-corresponding author.
  Explain them per entry in the `annotation` field (shown under the author list).
- The PI's name is underlined in publication lists based on `scholar.last_name` / `scholar.first_name` in `_config.yml`.
- Unused template pages (blog, projects, repositories, CV, bookshelf, teaching, news) are hidden via the
  `exclude:` list in `_config.yml` rather than deleted, so the template can be updated later.
- Local copies of theme files (each with one small change, see the comment inside): `_layouts/about.liquid`
  (home-page heading from `heading:` in `_pages/about.md`), `_layouts/bib.liquid` (annotation shown inline),
  `_sass/_variables.scss` (accent colour).

Full documentation of the starter: <https://github.com/alshedivat/al-folio/blob/main/docs/CUSTOMIZE.md>
