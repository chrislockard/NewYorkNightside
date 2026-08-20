# New York Nightside

A theme for [NetNewsWire](https://netnewswire.com) that sets articles like a
broadsheet and finishes them like a Mac app.

Set in Apple's **New York** throughout, with a thick-over-thin press rule at the
masthead, the feed name in letterspaced caps, a drop cap on the opening
paragraph, justified body copy with automatic hyphenation, and a fleuron (❦) in
place of the usual horizontal rule. The macOS half shows up in the details:
softly rounded media and code blocks, a pill-shaped source link at the foot, and
system-blue links.

Built dark-first. Both palettes are tuned to sit flush against NetNewsWire's own
window colors, so the reading pane doesn't float on a different shade from the
timeline beside it.

## Install

**One click:** paste this into your browser's address bar.

```
netnewswire://theme/add?url=https://github.com/chrislockard/NewYorkNightside/releases/latest/download/NewYorkNightside.nnwtheme.zip
```

**Manually:** download the `.nnwtheme` bundle, then in NetNewsWire go to **Settings → Open Themes Folder** and drop it in. On iOS, save the bundle somewhere reachable from the Files app, then **Settings → Theme → +**.

Select it under **Settings → General → Article Theme** on macOS, or **Settings → Articles → Theme** on iOS.

## Notes before you install

- **Dark mode is the primary design.** Light mode is fully supported and tuned,
  but the theme was drawn for dark first and looks its best there.
- **Wants a recent macOS.** The rule that hides the empty headline on untitled
  items uses the CSS `:has()` selector, which needs Safari 15.4 or later. On
  older systems, untitled items will show an empty gap where the headline would
  be. Everything else degrades cleanly.
- Feeds that open with an image rather than a paragraph won't get a drop cap.
  That's deliberate — a drop cap floating beside a photo looks like a mistake.

## Tweaking it

Everything lives in `stylesheet.css`. The colors are CSS custom properties at
the top of the file, split into a light block and a `prefers-color-scheme: dark`
block, so retheming means editing about a dozen lines rather than hunting
through selectors.

Common changes:

| Want | Do this |
| --- | --- |
| Ragged-right instead of justified | Delete the `text-align: justify` line in `.articleBody p` (it's commented) |
| No drop cap | Delete the `#bodyContainer > p:first-child::first-letter` rule |
| A different serif | Change `--font-serif` at the top |
| Wider or narrower measure | Change `max-width` on `body` (currently `40em`) |

## Palettes

| | Dark | Light |
| --- | --- | --- |
| Background | `#222222` | `#ffffff` |
| Body text | `#f1ece3` | `#252320` |
| Muted text | `#ada79f` | `#716c62` |
| Rules | `#3e3c37` | `#e1dcd1` |
| Links | `#8ab6ff` | `#0b5edf` |
| Masthead flag | `#e0736a` | `#b1221c` |

Both palettes hold roughly the same text contrast (about 13.5:1 dark, 15.7:1 light), so neither mode reads noticeably heavier than the other.

## Support

This is published as-is and isn't actively maintained — I made it for my own
reading and put it up in case it's useful to someone else. You're welcome to
fork it and make it yours; that'll be faster than waiting on me.

## License

MIT. See [LICENSE](LICENSE), which also carries attributions for NetNewsWire's
default theme (MIT, Ranchero Software) and the Font Awesome icon used in
`template.html` (CC BY 4.0).
