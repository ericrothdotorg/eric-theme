# Eric Theme

**Contributors:** [ericrothdotorg](https://github.com/ericrothdotorg)

A lean, build-free WordPress block theme (FSE), the one running [ericroth.org](https://ericroth.org/). No page builder, no framework, no webfonts: Templates, theme.json and plain CSS that loads only what a page actually uses.

**Tags:** eric-theme, wordpress, block-theme, fse, eric-snippets, eric-slider, website-lab

---

**What makes it genuinely stand out**

Most block themes are either polished demo themes built to sell or empty starter kits. This one is the production theme of a live site (this one!), shared as it is, so every rule exists because a real page needed it. The theme owns layout, design tokens and CSS, while everything dynamic lives in separate, documented code snippets. Performance comes from structure, not plugins: Per-block stylesheets load only on pages that use that block, and system fonts mean zero font requests. The CSS is readable, with a reset base layer and a site layer with a table of contents and stated conventions. There’s no build step: Upload the zip and it runs.

**Who would actually reach for it**

WordPress developers who want to see how a real block theme is put together, without a bundler, a page builder or a pile of unused patterns. It installs and runs on its own; add the companion snippets and the Display Posts plugin for the full look. As a readable, honest reference to learn from, borrow from or take apart, it fills a gap that polished commercial themes don’t.

---

## How the pieces fit

The theme is one of four parts. On its own it gives the layout, the design tokens and the CSS; everything dynamic comes from the snippets.

| Part | Where | What it brings |
|---|---|---|
| **Eric Theme** | This repository | Templates, template parts, theme.json, style.css (Part A base, Part B site), per-block CSS in `assets/styles/`, the mobile-menu submenu fix |
| **Eric Snippets** | [eric-snippets](https://github.com/ericrothdotorg/eric-snippets) | The shortcodes the templates use, the fixed header bar, Eric Companion CSS, custom post types, quotes, stats and more |
| **Eric Slider** | Standalone: [eric-slider](https://github.com/ericrothdotorg/eric-slider); on the site its files sit in the theme's `assets/eric-slider/` folder, already included in the release zip | Sliders and carousels (loaded by `eric-slider-animate.php` from the eric-slider repo) |
| **Display Posts** | [Plugin by Bill Erickson  ↗](https://displayposts.com/) | The `[display-posts]` listings in the templates |

### Required shortcodes

The templates and template parts use these shortcodes. If the snippet or plugin that provides one isn't active, its raw shortcode text shows on the page instead.

| Shortcode | Source |
|---|---|
| `[er_hero]`, `[er_breadcrumbs]`, `[er_cpt_archive]`, `[er_post_footer]`, `[er_related_posts]`, `[er_socials_support]` | [`snippets/overall/eric-companion.php`](https://github.com/ericrothdotorg/eric-snippets/blob/main/snippets/overall/eric-companion.php) |
| `[er_cached]` | [`snippets/overall/display-posts-bill-erickson.php`](https://github.com/ericrothdotorg/eric-snippets/blob/main/snippets/overall/display-posts-bill-erickson.php) |
| `[post_stats]`, `[total_post]`, `[total_my_interests]`, `[reusable]`, `[merged_tag_cloud]` | [`snippets/overall/site-essentials-cookies.php`](https://github.com/ericrothdotorg/eric-snippets/blob/main/snippets/overall/site-essentials-cookies.php) |
| `[display-posts]` | [Display Posts  ↗](https://displayposts.com/) plugin |

---

## Using it on your own site

This is the theme of one particular site, shared as it is. Use it, take it apart, borrow what you like.

- **Start with the theme:** Upload it and it runs. Layout, design tokens and CSS are all there, ready to explore or build on. Shortcodes from the snippets show as plain text until you add them. Footer and sidebar still carry this site's links and images, so swap in your own.
- **Get the full picture:** Add the [Display Posts  ↗](https://displayposts.com/) plugin and a few [snippets](https://github.com/ericrothdotorg/eric-snippets): *"Eric Companion PHP"*, *"Eric Companion CSS"*, *"Display Posts - Bill Erickson"*, *"Site Essentials & Cookies"* and *"CPTs & Taxonomies"*. That brings in the heroes, archives, related posts and the custom post types.
- **Make it yours:** Pick your own menu for the Navigation block in the Site Editor and set a static front page under Settings → Reading.

---

## Install

1. Download **eric.zip** from the latest release under [Releases](https://github.com/ericrothdotorg/eric-theme/releases). It's the complete theme, [eric-slider](https://github.com/ericrothdotorg/eric-slider) included.
2. WordPress: Appearance → Themes → Add New Theme → Upload Theme → choose the zip → Install Now.

Prefer the code straight from the repo (green **Code** button → **Download ZIP**)? Add the files from [eric-slider](https://github.com/ericrothdotorg/eric-slider) to `assets/eric-slider/`.

**Requires:** WordPress 7.0 or later, PHP 8.0 or later.

---

## License

GPL v3 or later. Parts of the code, CSS and templates are derived from [Ollie ↗](https://olliewp.com) by Mike McAlister (GPL v3 or later). Bundled: [animate.css ↗](https://animate.style) by Daniel Eden (MIT). [eric-slider](https://github.com/ericrothdotorg/eric-slider): MIT.
