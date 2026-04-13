---
layout: default
title: Upgrade Summary
---

## Upgrade Summary
- **From:** 1.0.0-beta
- **To:** 1.1.0
- **Date:** 2026-04-13
- **Automated changes:** 28
- **Manual steps:** 1

## Automated Changes Applied

### Configuration (2 files)

- [x] Added collection_mode: false to _config.yml (after telar_language)
- [x] Updated _config.yml: version 1.1.0 (2026-04-13)

### Layouts (2 files)

- [x] Updated _layouts/index.html - Homepage with collection mode branch
- [x] Updated _sass/_layout.scss - Layout styles (collection mode)

### Includes (3 files)

- [x] Updated _includes/panels.html - Panels with data-telar-panel attributes
- [x] Updated _includes/share-panel.html - Share panel with "this view" tab
- [x] Updated _includes/widgets/bibliography.html - Bibliography widget template (new)

### Styles (4 files)

- [x] Updated _sass/_panels.scss - Panel styles (bibliography max-width)
- [x] Updated _sass/_story.scss - Story styles (title cards)
- [x] Updated _sass/_viewer.scss - Viewer styles (Tify background fix)
- [x] Updated _sass/_widgets.scss - Widget styles (bibliography hanging indent)

### Scripts (12 files)

- [x] Updated assets/js/share-panel.js - Share panel (deep link support)
- [x] Updated assets/js/telar-story.js - Bundled story JS
- [x] Updated assets/js/telar-story.js.map - Source map
- [x] Updated assets/js/telar-story/main.js - Story entry point (deep link init)
- [x] Updated assets/js/telar-story/card-pool.js - Card pool (title cards, media deactivation)
- [x] Updated assets/js/telar-story/deep-link.js - Deep linking module (new)
- [x] Updated assets/js/telar-story/navigation.js - Navigation (panel keyboard scroll, hash writes)
- [x] Updated assets/js/telar-story/panels.js - Panels (glossary deep-link numbers, hash writes)
- [x] Updated assets/js/telar-story/scroll-engine.js - Scroll engine (panel fix, hash writes)
- [x] Updated scripts/telar/core.py - Build pipeline (audio manifest generation)
- [x] Updated scripts/telar/widgets.py - Widget parser (bibliography support)
- [x] Updated tests/js/card-pool.test.js - Card pool tests (title cards)

### Documentation (1 file)

- [x] Updated README.md - README (v1.1.0 features, bilingual)

### Other (4 files)

- [x] Updated CHANGELOG.md - CHANGELOG (v1.1.0 release notes)
- [x] Updated tests/unit/test_bibliography_widget.py - Bibliography widget tests (new)
- [x] Updated _data/languages/en.yml - English strings (collection_mode_heading added)
- [x] Updated _data/languages/es.yml - Spanish strings (collection_mode_heading added)

## Manual Steps Required

Please complete these after merging:

1. **New features available after upgrade:**

- **Deep linking**: Your story URLs now update as readers scroll. They can copy and share a URL that points to a specific step, optionally with a panel open. No configuration needed — it works automatically.

- **Title cards**: To add a chapter heading between story steps, leave the object column empty for a step row. The question column becomes the heading text. Title cards work with scroll, keyboard, and button navigation.

- **Collection mode**: To flip your homepage to a collection-first layout, add `collection_mode: true` to `_config.yml` (the upgrade script has already added the flag set to `false`). Objects appear first with large thumbnails; stories appear below with smaller thumbnails.

- **Bibliography styling**: To format references with hanging indent in panel content, wrap them in a `:::bibliography` block in your markdown file.

- **Share panel**: The share panel now includes a "this view" tab that copies the current URL with the reader's exact position. ([guide](https://telar.org/docs))

## Resources

- [Full Documentation](https://telar.org/docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Report Issues](https://github.com/UCSB-AMPLab/telar/issues)
