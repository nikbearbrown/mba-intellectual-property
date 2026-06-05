# CAJAL SVG Generation Log — Introduction to Intellectual Property: with LLMs

## Run: 2026-05-29

Generated static Brutalist-style SVGs from `pantry/*-cajal.md` plans, then converted to 300 DPI PNG (`scripts/svg-to-png.mjs`). Content drawn from chapter prose with correct IP-law terms; the CAJAL Okabe-Ito palette and Illustrae blocks were overridden. Chapter files not modified.

Note: this book had no local node_modules — `sharp`/`glob` resolved via a symlink to the friction book's node_modules.

| Cajal file | Figures | Generated | Skipped |
|---|---|---|---|
| 00-frontmatter-cajal.md | 0 | 0 | 0 |
| 00-introduction-cajal.md | 5 | 5 | 0 |
| 01-patent-basics-cajal.md | 5 | 5 | 0 |
| 02-patent-enforcement-cajal.md | 5 | 5 | 0 |
| 03-copyright-basics-cajal.md | 0 | 0 | 0 |
| 04-trademark-basics-cajal.md | 5 | 5 | 0 |
| 05-trade-secret-basics-cajal.md | 5 | 5 | 0 |
| 99-back-matter-cajal.md | 0 | 0 | 0 |

## Summary
- Total cajal.md files processed: 8
- Files with zero figures: 3 (00-frontmatter, 03-copyright-basics, 99-back-matter)
- Total figures parsed: 25
- Total SVGs generated: 25
- Total skipped: 0
- PNG conversion: run completed — 25 PNGs at 300 DPI

## Verification
- xmllint --noout: all 25 valid
- viewBox 0 0 700 ...: all conform; no width/height on `<svg>`
- No rounded corners, no gradients, no Okabe-Ito leakage, no forbidden fonts
- Visual spot-check: 04-fig-03 (distinctiveness spectrum: Aspirin/Phone generic → Kodak/Exxon fanciful) — legally accurate, on-style.

## Notes
- 03-copyright-basics had 0 planned figures (CAJAL declined) — worth a follow-up CAJAL pass if that chapter should carry figures.
- Enrichment pass (markdown image refs + D3 + Prompts into chapters) NOT done — separate step.
