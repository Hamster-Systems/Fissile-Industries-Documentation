# Fissile Industries Documentation

Official documentation source for **Fissile Industries**.

The [Fissile Industries Wiki](https://github.com/Hamster-Systems/fissile-industries-wikipedia) reads Markdown pages from `articles/` on the `main` branch. The public wiki URLs mirror the paths below `articles/`.

| Repository file | Wiki route |
| --- | --- |
| `articles/index.md` | `/wiki/index` |
| `articles/getting-started/overview.md` | `/wiki/getting-started/overview` |
| `articles/reference/glossary.md` | `/wiki/reference/glossary` |
| `articles/materials/index.md` | `/wiki/materials/index` |
| `articles/materials/ores.md` | `/wiki/materials/ores` |
| `articles/materials/ingots.md` | `/wiki/materials/ingots` |

## Creating and editing pages

Administrators can create and edit articles through the website after configuring a server-side GitHub token with **Contents: Read and write** permission for this repository. Every save creates a Git commit in this repository. You can also edit Markdown directly on GitHub.

Markdown is supported, including headings, lists, fenced code, linked images, GitHub alerts and wiki-specific infoboxes. The website supports a **limited, sanitised subset of HTML** (such as `<table>`, `<details>`, `<strong>`, `<em>` and `<br>`); scripts, inline event handlers and unsafe URLs are not allowed.

Do not commit credentials or private information. Each page must have a unique lower-case, URL-safe name in `articles/`.

## Materials & Resources

The `articles/materials/` folder contains **Ores** and **Ingots** sections, each with eight starter material articles: Uranium, Magnesium, Thorium, Tungsten, Lead, Copper, Titanium and Aluminium. Every page has a placeholder infobox; official item icons and validated gameplay information will be added later.

**Category integration:** The website also needs a `materials` row in its MySQL `wiki_categories` table to show “Materials & Resources” as an editable category with its own category page. A companion website PR seeds this entry using an additive `INSERT IGNORE`. Existing site operators can instead create the category manually in Admin → Wiki categories & pages with slug `materials` (do not create duplicates). Nested `/materials/ores` and `/materials/ingots` article paths appear in the sidebar automatically.
