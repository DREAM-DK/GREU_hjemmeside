# Layout mockups

Clickable pages for GreenREFORM-EU, using Direction 05 and the **connected
discs** and **squared grid** from the brand lab. This is not the GoBasic theme.

**To view:** double-click `index.html`. The navigation works, so you can click
through the pages in a browser. Nothing is live: buttons, downloads and the
newsletter form do nothing.

## Where the graphic comes from

`brand-lab/backgrounds/05-dream-heritage.svg` and
`brand-lab/generated/dream-heritage-study.png`: DREAM's model discs, each in
its own colour, joined by thin lines on a faint grid, with the international
model as the largest disc. The topology and the colours here are unchanged
from that file.

## Three registers, and they are not interchangeable

This is the part worth arguing about, because the graphic carries a claim.
The coloured discs **are** DREAM's models. Used as wallpaper they would say
"family" on pages that are not about the family.

| Register | File | Means | Used on |
| --- | --- | --- | --- |
| Family | `assets/family.svg` | The DREAM models, GreenREFORM-EU among them | Home hero, About lineage |
| Lineage | inline SVG in `index.html` | MAKRO to Gr&oslash;nREFORM to GreenREFORM-EU, labelled | Home, "Where it comes from" |
| Quiet | `assets/constellation-quiet.svg` | Nothing. Page texture | Interior page heads |
| Grid | `.gridpaper` in CSS | Nothing. Squared paper | Page heads, hero, signup band, sitemap |

The quiet register is the same arrangement of discs drawn entirely in mist. It
introduces no sixth colour and makes no claim about the family.

The grid and the quiet discs fade out towards the bottom of the band they sit
in, and the band has no bottom rule. Because the band keeps the page
background colour, there is nothing left to mark where it ended: the graphic
simply runs out and the page continues. The signup band is the exception. It
has its own colour and its own rules top and bottom, so its edge is deliberate
and the grid stays even across it.

The five colours and the rule that green is never decoration are in
`assets/site.css`. The grid is mist, the quiet discs are mist, and the only
green on a page is still the model or a link.

## What the pages do differently

- **Home** opens with the family constellation beside the headline, and closes
 "Where it comes from" with a labelled lineage diagram. The lineage is the
 honest version of the claim: MAKRO, then Gr&oslash;nREFORM, then this model.
- **Interior pages** have a page head band on squared paper, with the quiet
 constellation fading in from the right.
- **The disc is never modified**, never re-coloured, and never has anything
 added to it. What a country, a version or a project needs to say is said in
 type beside it. The disc-and-type component that showed this on Applications
 went with the Country teams directory, parked on 3 November 2026
 (`../content/parked/country-teams.md`); it is still drawn on sheet
 `brand-lab/boards/05c-dream-heritage-applications.html`.
- **The signup band** and the **sitemap** sit on squared paper.

## Open questions this raises

1. **The green country pill.** Sheet 05c gives country teams a green-tinted
 pill. Sheet 05d says green means the model or a link, and a country name is
 neither. Both are Direction 05. One of them has to give. Not urgent while
 the Country teams directory is parked, but settle it before restoring.
2. **Quoting DREAM's colours.** The family graphic reproduces the DREAM,
 MAKRO, REFORM, SMILE and Gr&oslash;nREFORM disc colours. They now match
 DREAM's own logo files exactly. Showing them on the GreenREFORM-EU site is a
 statement about the relationship between the models and needs DREAM's
 agreement, not just a designer's.
3. **How often the family may appear.** It is used twice here. More than that
 and it stops being a claim and becomes decoration.
4. **The disc at 44 px.** The country cards follow sheet 05c and use the full
 disc at 44 px, below the 56 px floor that sheet 05b sets. Either the floor
 moves or the cards use the initial, as the favicon does.

## Files

```
index.html               The model (home)
documentation.html       Documentation
user-guide.html          User guide
get-the-model.html       Get the model
applications.html        Applications
analysis-tsi-paper.html  One analysis record
project-tsi-2024.html    One project page (TSI 2024)
project-version-2-0.html One project page (Version 2.0)
news.html                News
about.html               About
accessibility.html       Accessibility statement (footer, not nav)
sitemap.html             Sitemap diagram, not a site page
assets/site.css          Direction 05 theme, plus the graphic system
assets/family.svg        The connected discs, in the family colours
assets/constellation-quiet.svg  The same arrangement, in mist
assets/mark.svg          The model disc
assets/favicon.svg       The initial, for sizes below the floor
```

## Screenshots

`screenshots/` holds flat images for slides, email and print. Each is 3720 px
wide: the 1240 px page rendered at three times scale.

**This is a dated snapshot, not a mirror of the pages.** It was last refreshed
on 3 November 2026 and is no longer regenerated as a matter of course. It
covers ten of the seventeen pages. The seven project pages — TSI 2024,
TSI 2026, Version 2.0, Viet Nam, FinReform, Belgium and Faroe Islands — have
no image here at all.
Before pasting one into a deck, check it against the page.

To regenerate, render the file with headless Chrome:

```
chrome --headless=new --disable-gpu --hide-scrollbars --no-first-run ^
  --user-data-dir=%TEMP%\shot-profile --force-device-scale-factor=3 ^
  --window-size=1240,3000 --virtual-time-budget=5000 ^
  --screenshot=%TEMP%\raw.png "<full path to the .html file>"
```

Chrome takes a plain Windows path as the last argument and handles the
non-ASCII folder names, so there is no need to copy the site to a temp folder
first.

Render tall — 3000 is above every page — and crop afterwards rather than
trying to set the exact page height. A fixed height per page is a maintenance
trap: it goes stale the moment any copy changes, and too small crops the
footer while too large adds paper-coloured space below it. To find the real
bottom, scan up from the last row of the raw image for the first row that is
dark at x = 0, w/3, w/2 and w-1; that is the foot of the dark footer. Crop
there. `sitemap.html` is the exception, as it has no dark footer, so give it a
fixed 3726.

Two traps. `--virtual-time-budget` gives the Hind web font time to arrive:
without a network connection Chrome falls back to Segoe UI and the screenshots
stop matching the pages as served. And Chrome writes progress to stderr, which
PowerShell turns into a terminating `NativeCommandError` under
`$ErrorActionPreference = 'Stop'`, so wrap the call in `'Continue'` and pipe
`2>&1` to `Out-Null`.

## Accessibility

Built to WCAG 2.1 AA, as the Danish web accessibility act requires. See
[../ACCESSIBILITY.md](../ACCESSIBILITY.md). The graphic system is covered
there too: the discs and the grid are decorative, so they are hidden from
assistive technology and carry no colour-only meaning.

Type is Hind from Google Fonts, so the renderer needs a network connection or
the screenshots fall back to Segoe UI and stop matching the pages.
