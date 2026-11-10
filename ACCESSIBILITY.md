# Web accessibility

The mockup in `mockups-graphic/` is built to meet the Danish web accessibility
act. This note records which rules apply, what was changed to meet them, what
was tested, and what cannot be settled without a decision from DREAM.

Source: [digst.dk/tilsyn/webtilgaengelighed](https://digst.dk/tilsyn/webtilgaengelighed/).

## What the law asks for

The act (`lov om webtilg&aelig;ngelighed`) applies to public authorities and
bodies governed by public law. It requires two separate things, and the second
is the one most often missed.

1. **The site must meet the standard.** The harmonised European standard is
   **EN 301 549**. Chapter 9 covers web pages and amounts to **WCAG 2.1 at
   level A and AA**. Chapter 10 covers documents that are not web pages, which
   for this site means the model documentation, the user guide and the papers.
2. **The site must publish an accessibility statement.** A statement is only
   valid if it is produced in Digitaliseringsstyrelsen's **WAS-Tool** and
   published at the standardised address `was.digst.dk/<domain>`. It must be
   reviewed at least once a year. The recommended pattern is a short address on
   the site's own domain, `<domain>/was`, redirecting to the standardised one.

Digitaliseringsstyrelsen supervises compliance and runs a monitoring programme
that samples sites each year.

## What was changed

All of this applies to `mockups-graphic/`.

### Structure and navigation

| Change | Criterion |
| --- | --- |
| A visible-on-focus **skip link** as the first item on every page | 2.4.1 Bypass blocks |
| `<main id="main">` moved so it contains the `h1`, including the home hero and the graphic page heads | 1.3.1, 2.4.1 |
| `aria-label="Primary"` on the navigation landmark, `aria-label="Newsletter"` on the signup landmark | 1.3.1, 4.1.2 |
| Heading levels made continuous. `get-the-model` and `news` jumped `h1` to `h3`; both gained the missing `h2` | 1.3.1 |
| `aria-current="page"` already marked the active navigation item | 4.1.2 |

### Forms

| Change | Criterion |
| --- | --- |
| The newsletter field now has a real `<label for>` instead of a placeholder doing the work | 1.3.1, 3.3.2, 4.1.2 |
| `name="email"` and `autocomplete="email"` added | **1.3.5 Identify input purpose** |
| The visually hidden label uses the clip technique, not `left:-9999px`, which can misplace the focus ring | 2.4.7 |
| The Applications filter chips were `<span>`s. They are now `<button type="button">` with `aria-pressed` | 2.1.1 Keyboard, 4.1.2 |

### Colour and contrast

Two real failures were found by calculation, not by eye.

| Item | Was | Now | Criterion |
| --- | --- | --- | --- |
| Newsletter placeholder | `#7C8A80`, **3.6:1** | `#5E6B62`, **5.6:1**, `opacity: 1` | 1.4.3 |
| Borders of inputs and filter chips | `#D9E0D9`, **1.3:1** | `--line-ui: #79837B`, **3.9:1** | **1.4.11 Non-text contrast** |

Ratios are against white, which is the surface those controls sit on.

`--line-firm` is kept at its old value for decorative rules, card edges and
table borders. 1.4.11 applies to the boundary of a user interface component,
not to every line on the page, so those do not need 3:1.

The focus ring is clay `#A04A26`, **5.6:1** on paper. It is the one place clay
is not a content signal, and it now also covers `<summary>` and anything with
a `tabindex`.

### Non-text content

| Change | Criterion |
| --- | --- |
| The model disc is decorative beside the site name, so `alt=""` | 1.1.1 |
| `family.svg` carries a description of what the discs mean, not "logo" | 1.1.1 |
| The sitemap diagram, which a script draws, gained `role="img"`, a `<title>` and a `<desc>` | 1.1.1, 4.1.2 |
| The same sitemap is now written out as a nested list in a `<details>` below the diagram. That list is also the only version available with scripting off | 1.1.1 |
| The grid and the quiet discs are CSS backgrounds, so they are already absent from the accessibility tree. `constellation-quiet.svg` is additionally `role="presentation"` | 1.1.1 |

Nothing on the site uses colour as the only carrier of meaning. Both places
that once risked it are gone as of 3 November 2026.

The clay "new" tag did repeat its meaning in words while the tag read `NEW`.
When the project tags were standardised onto a period-and-funder pattern, the
TSI 2026 tag became "2026 – 2029 · European Commission" but kept the clay
class, so for a short time the colour was the only thing saying "new". That is
a 1.4.1 failure, and it is the kind that appears through drift rather than
through a decision. The project tags are now uniformly grey, and `site.css`
carries the rule that clay may only return if the tag text says NEW.

The green "country" pill went with the Country teams directory, parked the
same day: see `content/parked/country-teams.md`. If that directory is
restored, the pill has to repeat the country name in words, which it did.

### Unfoldable chapters on the documentation page

The seven chapter summaries are `<details>` and `<summary>`, decided on
5 November 2026. Native elements were chosen over a scripted accordion so that
the expanded state is announced, the keyboard behaviour is the browser's, and
the sections still open without script.

Two consequences are worth writing down, because they shape the copy rather
than the markup.

Chrome expands a closed `<details>` when find-in-page lands inside it. Firefox
and Safari do not reliably. A reader searching the page for a word that only
appears in a closed body may therefore conclude the page does not mention it.
The summary line of each chapter has to carry the words a reader would search
for, which is why the closed state repeats the section list rather than teasing
it.

The chevron is marked `aria-hidden` and is decorative. It is not the carrier of
the open or closed state; the `<summary>` element is. This is the same rule as
the one about colour below: nothing may depend on a visual cue alone.

### Reflow

A breakpoint at 520 px was added: the vertical rule in the masthead is dropped,
buttons go full width, the two-column metadata table stacks, and page padding
tightens. `.mono` gained `overflow-wrap: anywhere`, because file names have no
spaces to break at and would otherwise push the page wider than the viewport.

## What was tested, and how

An audit harness loads each page in an iframe at a fixed width and measures
every element: its box against the viewport, and its computed text colour
against its computed background, with the WCAG relative-luminance formula.

Results at both **320 px** and **1240 px**, on `applications`,
`accessibility`, `documentation`, `index` and `about`:

- `scrollWidth` equals `clientWidth` at 320 px. Nothing scrolls sideways,
  which satisfies **1.4.10 Reflow** and the equivalent 400% zoom case.
- **Zero contrast failures.** The only element reported outside the viewport is
  the skip link parked off-screen until focused, which is intended.

Checked by inspection across all ten pages: one `h1` each, no duplicate `id`s,
`lang` and `<title>` present everywhere, no heading-level jumps, every `<img>`
carries an `alt`.

Not yet tested, because it needs a person rather than a script: screen-reader
output, and tab order through a page from end to end.

## What DREAM has to decide

These are blocking, in the sense that the statement cannot be published without
the first one.

1. **Is DREAM covered by the act?** It applies to public authorities and bodies
   governed by public law. Whether an independent institute funded this way
   counts is a legal question. It also decides which tool may be used: WAS-Tool
   is only for bodies covered by the act, and private actors are expressly not
   allowed to publish statements through it. If DREAM is not covered, the
   accessibility work still stands on its merits, but the statement page should
   be rewritten as a voluntary commitment rather than a legal declaration.
2. **A telephone contact.** The act requires both a written and a telephone
   route for reporting barriers. The site publishes an email address and no
   number.
3. **The documents.** This is the largest open item. A PDF produced from LaTeX
   is not tagged for accessibility by default: reading order, alternative text
   on figures, table headers and document language all have to be added
   deliberately. EN 301 549 chapter 10 covers them, and the documentation is
   the main thing this site exists to deliver. Someone has to own this, and it
   has to be decided whether it happens before or after launch.
4. **Language of the statement.** It is addressed to citizens and must be
   understandable without technical knowledge. This site is in English; the
   statement is normally expected in Danish. It may need both.
5. **Who signs it off.** Self-assessment or an external audit.

## A caveat about the real build

These are static mockups with one hand-written stylesheet. The real site is
expected to be built on Ber&uacute;'s GoBasic subsite framework. None of the
markup here survives that move, so treat this as a specification of what the
built site has to do, not as the implementation. The contrast values and the
palette decisions do carry over, because they are properties of the colours.
