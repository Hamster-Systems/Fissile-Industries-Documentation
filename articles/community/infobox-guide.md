<!-- fissile-infoboxes: off -->
# Reusable infoboxes

Infoboxes are compact information panels designed for Fissile Industries item, element, material and machine articles.

You can insert an infobox from the website editor using **Element infobox**, or paste the Markdown below directly into a GitHub documentation page. Every box starts with `:::infobox Title` and finishes with `:::`. You can add **multiple** infoboxes to one page, with regular article text between them.

## Example: two infoboxes in one article

```markdown
# Boron

:::infobox Boron
image: /media/docs/media/elements/boron.png
alt: Boron item sprite
caption: Boron
layout: inline
collapsible: true
collapsed: false
visible: true

[Properties]
Type: Element
Exists in reality: Yes
Atomic number: 5

[Reactivity | collapsed]
Neutron absorption: Add verified information
:::

:::infobox Boron-10
layout: inline
collapsible: true
collapsed: true

[Properties]
Type: Isotope
Atomic number: 5

[Chemistry]
Notes: Add verified information
:::
```

The first card opens normally and has a collapsible **Reactivity** section. The second card is collapsed until a reader opens it. Both are independent.

## Page-wide infobox switch

The website editor offers **Show infoboxes on this page**. Unchecking it hides every infobox on that article while keeping the Markdown safely stored, so you can re-enable all the infoboxes later.

For editors using GitHub directly, the equivalent article-wide setting is:

```markdown
```

Place that metadata line near the top of the page to disable all infoboxes on it. Remove it or change it to `on` to turn infobox rendering back on. This setting does not hide the rest of the article and is not displayed to visitors.

## Infobox settings

| Option | Usage |
| --- | --- |
| `image: URL` | Shows a pixel-art image (use an approved HTTPS or wiki media URL) |
| `alt: Description` | Accessible alternative text for the image |
| `caption: Text` | Optional caption underneath the image |
| `layout: side` | Float a small card on the right (default) |
| `layout: inline` | Place multiple cards beside each other when space allows |
| `layout: wide` | Fill the article width |
| `collapsible: true` | Allow visitors to expand/collapse the entire infobox |
| `collapsed: true` | Start the entire box closed |
| `visible: false` | Hide that particular box without deleting its Markdown |
| `[Properties]` | Starts a named property group |
| `[Reactivity \| collapsed]` | Starts an expandable, initially closed group |

Each property is written as `Label: Value`. Groups can be called **Properties**, **Reactivity**, **Chemistry**, **Safety**, **Electrical**, **Radioactivity**, or anything suitable. Another way to declare a group is `## Chemistry`, but brackets are preferred to keep infobox headings out of the document outline. Supported inline Markdown, such as links and bold text, works inside property values.

## Images

Upload a screenshot/item texture to the website media library, or commit a PNG/WebP image in the documentation repository under `media/`.

Example image path: `/media/docs/media/elements/boron.png`.

This is only an example path; **upload the image first** or omit the `image:` line. Any image that exists in the wiki can be used in multiple boxes. For Minecraft textures, infobox artwork uses pixelated scaling to keep pixels sharp.

## Notes

- No database migrations are necessary: the boxes are stored directly in Markdown article files.
- GitHub commit history automatically records edits to each article.
- Infoboxes are only rendered in wiki articles and in the administrator's documentation preview, not in forum posts.
- Text, URLs and configuration values are validated and safely rendered; scripts and executable HTML are unsupported.