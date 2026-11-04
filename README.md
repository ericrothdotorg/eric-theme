# Eric Theme

**Contributors:** [ericrothdotorg](https://github.com/ericrothdotorg)

A lean, build-free WordPress block theme (FSE), the one running ericroth.org. No page builder, no framework, no webfonts: Templates, theme.json and plain CSS that loads only what a page actually uses.

**Tags:** wordpress, block-theme, fse, website-lab, eric-slider

---

**What makes it genuinely stand out**

Most block themes are either polished demo themes built to sell or empty starter kits. This one is the production theme of a live site (this one!), shared as it is, so every rule exists because a real page needed it. The theme owns layout, design tokens and CSS, while everything dynamic lives in separate, documented code snippets. Performance comes from structure, not plugins: Per-block stylesheets load only on pages that use that block, and system fonts mean zero font requests. The CSS is readable, with a reset base layer and a site layer with a table of contents and stated conventions. There’s no build step: Upload the zip and it runs.

**Who would actually reach for it**

WordPress developers who want to see how a real block theme is put together, without a bundler, a page builder or a pile of unused patterns. It’s not a drop-in, do-everything theme. On its own it installs and runs, but the full look needs the companion snippets and the Display Posts plugin. As a readable, honest reference to learn from, borrow from or take apart, it fills a gap that polished commercial themes don’t.

---

## Get it here

[Eric Theme](https://github.com/ericrothdotorg/website-lab/tree/main/eric-theme)

---

## Using it on your own site

This is the theme of one particular site, shared as it is. Use it, take it apart, borrow what you like.

- **Theme only:** Installs and runs, but the shortcodes above show as plain text and much of the look is missing.
- **The full picture:** Add the Display Posts plugin and the snippets, at least *Eric Companion PHP* and *CSS*, *Display Posts – Bill Erickson* and *CPTs & Taxonomies* (the custom post types the archive templates expect).
- **Menu:** The header points to a navigation menu of this site. On yours, pick your own menu for the Navigation block in the Site Editor.

---

## License

GPL v3 or later. Parts of the code, CSS and templates are derived from [Ollie  ↗](https://olliewp.com) by Mike McAlister (GPL v3 or later). Eric Slider: MIT.
