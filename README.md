# New York Nightside

![New York Nightside in dark and light mode](docs/nyn-split.png)

A theme for [NetNewsWire](https://netnewswire.com) that sets articles like a
broadsheet and finishes them like a Mac app.

Set in Apple's [**New York**](https://developer.apple.com/fonts/) throughout,
with a thick-over-thin press rule at the masthead, the feed name in letterspaced
caps, a drop cap on the opening paragraph, ragged-right body copy with automatic
hyphenation, and a fleuron (❦) in place of the usual horizontal rule. The macOS
half shows up in the details: softly rounded media and code blocks and
system-blue links.

Longer articles get an estimated reading time in the dateline and a reading
map: a hairline in the right margin, like the rule between newspaper columns,
with a dot for each section placed where it falls in the article. Click a dot
to jump to that section, or drag along the rule to scrub through the piece.
Articles without headings get five evenly spaced dots instead. The map stays
out of sight while you read and fades in when you scroll or point at the
margin. It shows in reading panes 440px wide and up (it hides on iPhone), and
the theme respects the system's Increase Contrast setting. Hat tip to Raisul
Chowdhury's [Calm](https://raisul.xyz/projects/calm) theme for the idea.

**New in v6:** the reading map fades out when you stop scrolling, leaving the
margin clean. It shows for a moment when an article opens, comes back as soon
as you scroll, and stays put while the pointer is over it or a dot has
keyboard focus. See [CHANGELOG.md](CHANGELOG.md) for what's new in each
release.

Built dark-first. Both palettes are tuned to sit flush against NetNewsWire's own
window colors, so the reading pane doesn't float on a different shade from the
timeline beside it.

## Install

**iPhone and iPad:** GitHub won't render `netnewswire://` links as clickable, so
copy the full URL below, paste it into Safari's address bar, and confirm that you
want to open NetNewsWire. NetNewsWire then downloads and installs the theme.

```text
netnewswire://theme/add?url=https%3A%2F%2Fgithub.com%2Fchrislockard%2FNewYorkNightside%2Freleases%2Flatest%2Fdownload%2FNewYorkNightside.nnwtheme.zip
```

**macOS:** paste the same URL into Safari, or run it from Terminal:

```sh
open 'netnewswire://theme/add?url=https%3A%2F%2Fgithub.com%2Fchrislockard%2FNewYorkNightside%2Freleases%2Flatest%2Fdownload%2FNewYorkNightside.nnwtheme.zip'
```

**Manually:** download
[NewYorkNightside.nnwtheme.zip](https://github.com/chrislockard/NewYorkNightside/releases/latest/download/NewYorkNightside.nnwtheme.zip)
from the latest release and unzip it, then in NetNewsWire go to **Settings → Open Themes Folder** and drop it in. On iOS, save the bundle somewhere reachable from the Files app, then **Settings → Theme → +**.

Select it under **Settings → General → Article Theme** on macOS, or **Settings → Articles → Theme** on iOS.

## Notes before you install

- **Dark mode is the primary design.** Light mode is fully supported and tuned,
  but the theme was drawn for dark first and looks its best there.
- **Wants a recent macOS.** The rule that hides the empty headline on untitled
  items uses the CSS `:has()` selector, which needs Safari 15.4 or later. On
  older systems, untitled items will show an empty gap where the headline would
  be. Everything else degrades cleanly.
- **Some features need JavaScript.** The reading map, drop cap and reading
  time are added by the theme's script, which only runs when **Enable
  JavaScript** is on in NetNewsWire's General settings (macOS). With it off,
  articles still read normally; those three features just don't appear.
- The drop cap goes on the first real paragraph, wherever the feed puts it.
  Short items (under about 80 words) and posts that open with an image,
  heading or quote don't get one. That's deliberate: a drop cap floating beside
  a photo looks like a mistake. An all-italic editor's note at the top is
  skipped, and the drop cap goes on the paragraph after it.

## Tweaking it

Everything lives in `stylesheet.css`. The colors are CSS custom properties at
the top of the file, split into a light block and a `prefers-color-scheme: dark`
block, so retheming means editing about a dozen lines rather than hunting
through selectors.

Common changes:

| Want | Do this |
| --- | --- |
| Justified instead of ragged-right | Add `text-align: justify;` to `.articleBody p` |
| No reading map | Add `.readingMap { display: none !important; }` at the end |
| Reading map always visible | Add `.readingMap { opacity: 1 !important; }` at the end |
| No drop cap | Delete the `#bodyContainer .dropCap::first-letter` rule |
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

## Feedback

New York Nightside is actively maintained. If an article renders badly or
something looks off, please
[open an issue](https://github.com/chrislockard/NewYorkNightside/issues/new).
Include a link to the feed or article, your NetNewsWire and OS versions, light
or dark mode, and a screenshot if you can. Suggestions are welcome too.

If the same problem shows up in NetNewsWire's built-in themes, it's probably a
NetNewsWire issue. Report it to
[the NetNewsWire project](https://github.com/Ranchero-Software/NetNewsWire/issues) instead.

## License

MIT. See [LICENSE](LICENSE), which also carries attributions for NetNewsWire's
default theme (MIT, Ranchero Software) and the Font Awesome icon used in
`template.html` (CC BY 4.0).
