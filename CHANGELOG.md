# Changelog

## v3 — 2026-10-05

- **Reading time.** Articles that take four minutes or more show an estimate
  in the dateline, such as "Oct 5, 2026 · 7 min read". Shorter pieces and
  untitled items don't get one.
- **Narrow columns.** On iPhone, iPad Split View, and narrow Mac reading panes:
  tighter side margins, a smaller headline, a tighter line height, and
  ragged-right instead of justified text, to avoid gaps between words.
- **Touch.** On touch screens, the feed name, byline and dateline links have
  larger tap areas. Nothing moves visually.
- **Increase Contrast.** When Increase Contrast is on in macOS or iOS, muted
  text, rules and link underlines are darker in both palettes.
- **More elements styled:** highlighted text (`mark`), keyboard keys (`kbd`),
  definition lists, expandable `details` sections, and audio players now match
  the theme instead of showing browser defaults.
- **Better line breaks:** paragraphs and list items avoid ending on a single
  short word, where the system supports it.
- **Bare URLs** (like the links in hnrss.org items) can now wrap mid-URL, so
  justified lines in front of them no longer stretch into huge gaps.
- **Drop cap** is skipped when the opening paragraph is under 20 words, such
  as the "Article URL: …" line in link-aggregator items.
- Modernized the table selectors (`:matches()` → `:is()`). There is no visual change.

## v2 — 2026-08-21

- Removed the empty source-link pill shown on articles without an external link.
- Enlarged the byline and dateline.
- Added screenshots to the README.

## v1 — 2026-08-20

- First release.
