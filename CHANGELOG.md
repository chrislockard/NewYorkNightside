# Changelog

## v6 — 2026-11-20

- **The reading map fades out while you read.** It shows for a couple of
  seconds when an article opens so you know it's there, fades in whenever you
  scroll, and fades out again about a second and a half after you stop. It
  stays visible while the pointer is over it, while you're dragging along it,
  and while a dot has keyboard focus. You can still point at or click the
  margin while it's hidden. To keep it on screen all the time, see the new
  line in the README's tweak table.

## v5 — 2026-11-20

- **Reading map.** Articles two screens or longer get a hairline in the right
  margin with a dot for each section, placed where that section falls in the
  article. The current section's dot is red. Click a dot to jump to it, drag
  along the rule to scrub (the drag snaps to nearby dots), or use the arrow
  keys once a dot has focus. Hovering shows the section's name. Articles with
  fewer than three usable headings get five depth dots, top to end. It works
  in reading panes as narrow as 440px, widening the right margin if needed,
  and hides on iPhone. Inspired by the map in Raisul Chowdhury's
  [Calm](https://raisul.xyz/projects/calm) theme.
- **Ragged-right text everywhere.** Body copy is no longer justified, so there
  are no more wide gaps between words. Hyphenation stays on.
- **No source-link box.** The capsule at the foot of the article is gone; it
  sometimes showed up empty. On link posts (Daring Fireball and the like), the
  linked article now appears as a quiet "Link:" line under the dateline. It's
  hidden when a post has no outside link, even with JavaScript off.

## v4 — 2026-10-05

- **Drop caps show up more consistently.** Whether an article gets one now
  depends on its total length (80 words or more), not on how long its first
  paragraph is. Long posts that open with a short line, like many on Daring
  Fireball and Schneier on Security, get their drop cap back.
- **Drop caps work with more feed formats:** paragraphs nested in wrapper
  `<div>`s (HEY World), and feeds that send plain text with no paragraph tags
  (The Register).
- **Editor's notes are skipped.** If a post opens with an all-italic note
  ("This essay originally appeared in…"), the drop cap goes on the paragraph
  after it.
- **HEY World posts** now get the same justified, hyphenated text as other
  feeds.

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
