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

## How the pieces fit

The theme is one of four parts. On its own it gives the layout, the design tokens and the CSS; everything dynamic comes from the snippets.

| Part | Where | What it brings |
|---|---|---|
| **Eric theme** | This repository | Templates, template parts, theme.json, style.css (Part A base, Part B site), per-block CSS in `assets/styles/`, the mobile-menu submenu fix |
| **Code snippets** | [website-lab/snippets](https://github.com/ericrothdotorg/website-lab/tree/main/snippets) | The shortcodes the templates use, the fixed header bar, Eric Companion CSS, custom post types, quotes, stats and more. Run with [Code Snippets  ↗](https://wordpress.org/plugins/code-snippets/) |
| **Eric Slider** | Standalone: [eric-slider](https://github.com/ericrothdotorg/eric-slider); on the site its files sit in the theme's `assets/eric-slider/` folder, already included in the release zip | Sliders and carousels (loaded by the snippet *Eric Slider & Animate*) |
| **Display Posts** | [Plugin by Bill Erickson  ↗](https://displayposts.com/) | The `[display-posts]` listings in the templates |

Shortcodes in the templates and where they come from:

| Shortcode | Snippet |
|---|---|
| `[er_hero]`, `[er_breadcrumbs]`, `[er_cpt_archive]`, `[er_post_footer]`, `[er_related_posts]`, `[er_socials_support]` | [`snippets/overall/eric-companion.php`](https://github.com/ericrothdotorg/website-lab/blob/main/snippets/overall/eric-companion.php) |
| `[er_cached]` | [`snippets/overall/display-posts-bill-erickson.php`](https://github.com/ericrothdotorg/website-lab/blob/main/snippets/overall/display-posts-bill-erickson.php) |
| `[display-posts]` | Display Posts plugin |

---

## Using it on your own site

This is the theme of one particular site, shared as it is. Use it, take it apart, borrow what you like.

- **Theme only:** Installs and runs, but the shortcodes above show as plain text and much of the look is missing.
- **The full picture:** Add the Display Posts plugin and the snippets, at least *Eric Companion PHP* and *CSS*, *Display Posts – Bill Erickson* and *CPTs & Taxonomies* (the custom post types the archive templates expect).
- **Menu:** The header points to a navigation menu of this site. On yours, pick your own menu for the Navigation block in the Site Editor.

---

## Install

1. Download **eric.zip** from the latest release under [Releases](https://github.com/ericrothdotorg/eric-theme/releases).
2. WordPress: Appearance → Themes → Add New Theme → Upload Theme → choose the zip → Install Now.

Don't use the green **Code → Download ZIP** button for this: it downloads the repository without the Eric Slider files, and the theme would end up in a folder named after the repository instead of `eric`.

**Requires:** WordPress 7.0 or later, PHP 8.0 or later.

---

## License

GPL v3 or later. Parts of the code, CSS and templates are partly derived from [Ollie  ↗](https://olliewp.com) by Mike McAlister (GPL v3 or later). Eric Slider: MIT.
