# Design rationale: how much graphic should this site carry?

Written to support a decision between two approaches to the GreenREFORM-EU
site. It sets out what was measured on the live mockup at
[greenreform.gopublic.dk](https://greenreform.gopublic.dk/), which published
standards apply, and where the argument for a quieter site is strong and where
it is weak.

The positive statement of the position is in
[DESIGN_PHILOSOPHY.md](DESIGN_PHILOSOPHY.md). This note is the evidence.

This is a question about fitness for a specific audience, not about taste.
Anyone using this note to argue a position should read the "Where the
objection is weak" section first, because the obvious form of the argument
does not survive contact with the evidence.

## The short version

The live mockup spends **3,470 pixels** of page height to deliver **249
words**. Two of the three screens a visitor scrolls through before reaching
any substance are a photograph of a farmyard and a photograph of a child in a
car in front of wind turbines. Neither photograph is in the accessibility
tree: they are CSS background images, so by the site's own construction they
convey nothing to anyone who cannot see them.

The strongest objection is not that this is ugly. It is that:

1. The decorative colour band **causes a legal compliance failure** that would
   not exist on a plain background.
2. The photographs make an **advocacy claim** that the model itself is
   designed not to make.
3. The intended reader is a modeller in a finance ministry who arrives with a
   task, and the page defers that task by three screens.

## What was measured

Measured on 3 October 2026 against the live site, at a 1,425 px viewport, by
evaluating in the page rather than by inspection.

| Finding | Detail |
| --- | --- |
| Content density | 249 words over 3,470 px of page height |
| Contrast failures | **2**, both WCAG 1.4.3 at level AA |
| Failing elements | The hero buttons "Read the documentation" and "Become a user" |
| The failure | `#DE0D0D` text on `#9DE4AA` background = **3.38:1**, where 4.5:1 is required |
| The same red on white | **5.0:1**, which passes |
| Language of parts | `aria-label="Åben hovednavigationen"` and a footer landmark named `Bund`, both Danish, on a page declaring `lang="en"`, with no `lang="da"`. WCAG 3.1.2 at level AA |
| The photographs | `foto_is_1336690099.jpg` and `foto_jh_ima131364.jpg`, 620×620 each, applied as CSS backgrounds |
| Every `<img>` on the page | `alt=""`, i.e. declared decorative |
| Reflow at 320 px | **Passes.** `scrollWidth` equals `clientWidth`, nothing overflows |
| Landmarks, skip link, headings | Present and correct |

### The contrast failure is the whole argument in miniature

`#DE0D0D` on white reads 5.0:1 and passes. The identical button on the green
band reads 3.38:1 and fails. **The decoration broke it.** Nothing about the
colour, the type size or the component is wrong; the only cause is the
decision to lay a contrasting colour behind the content.

This matters beyond these two buttons. Under the Danish web accessibility act
the site must meet EN 301 549, which for a web page means WCAG 2.1 AA. Every
additional background colour multiplies the number of foreground-background
pairs somebody has to get right, and every one of them is a place the site can
fall out of compliance later, silently, when a colour is reused in a context
nobody tested. A page with one background colour has one set of pairs to
verify. This page has at least five.

The file naming of the photographs is worth noting: the `is` prefix with a
ten-digit identifier is the pattern of a commercial stock library asset. That
should be confirmed, along with the licence terms for a publicly funded site.

## Where the objection is strongest

### 1. The photographs make a claim the model cannot support

This is the argument most likely to land with DREAM, and it has nothing to do
with visual preference.

A smiling child in front of wind turbines is an emotional argument for the
green transition. GreenREFORM-EU is not an argument for anything. It is an
instrument a finance ministry uses to score policies, including policies that
score badly, and including scenarios a minister would rather not publish. Its
value to a ministry rests on being seen as neutral apparatus.

Dressing a neutral analytical tool in campaign imagery undermines the single
property that makes it worth adopting. A sceptical official in a finance
ministry who lands on a page that looks like it is selling them the green
transition will discount the model before reading a word about it. The
documentation workspace already enforces this discipline in the prose, where
claims must be traceable to a chapter and unsupported features may not be
advertised. The pictures should be held to the same standard as the sentences.

### 2. The reader arrives with a task, and the page defers it

The audience named in the brief is finance ministries, planning bureaus and
emissions agencies. These readers are not being persuaded to care about
climate policy; that is their job already. They arrive wanting to find out
what the model does, whether it will run on their data, and where the
documentation is.

The home page answers none of those in the first screen. It offers a slogan,
"Supporting better climate policy decisions", which could sit on any
organisation in the sector. Compare the Netherlands Bureau for Economic Policy
Analysis, [cpb.nl](https://www.cpb.nl/en): it also opens with a photograph,
but four named publications are on screen immediately beside it, and a dated
publication list follows directly. The photograph costs nothing because the
content is not displaced.

That is the sharper version of the complaint. **The problem is not that there
are pictures. It is that there is almost nothing else.**

### 3. Page weight has a cost this project should not ignore

Two 620×620 photographs plus decorative SVG banding is a real payload to send
on every visit, to deliver 249 words. The W3C published
[Web Sustainability Guidelines](https://w3c.github.io/sustainableweb-wsg/) in
2023 covering exactly this. For most sites this is a minor point. For a site
whose entire subject is the carbon cost of economic activity, it is an
awkward one to have to defend, and somebody will eventually raise it in
public.

## Where the objection is weak

Read this before arguing the case, or it will be dismissed in one move.

**DREAM's own site does the same thing.** [dreamgruppen.dk](https://dreamgruppen.dk/)
leads with a full-bleed aerial photograph and a three-line aspirational
slogan, runs the same `#DE0D0D` red, and illustrates news items with stock
photography including a child holding carrots. Jonas has not invented a style.
He has applied the existing house style of the parent institution, which is
defensible and probably what he was asked to do. Any argument of the form
"stock photography is unprofessional" loses immediately.

**The mockup is competently built.** It has a working skip link, named
navigation landmarks, a single correct `h1`, lazy-loaded images, correct empty
`alt` on decorative images, and it reflows cleanly at 320 px with no
horizontal scrolling. Most sites fail that last test. Whoever built the
template knew what they were doing, and the two defects found are narrow and
fixable rather than structural.

**It is on a real platform.** A CMS-backed site can be edited by people who do
not write HTML, and it will still exist in three years. Hand-built mockups
will not. Platform maintainability is a stronger argument than any aesthetic
one, and it currently favours the live mockup.

**A plain-language opening is genuinely good.** Dropping a visitor straight
into "dynamic computable general equilibrium model" serves nobody. Some
framing before the technical substance is right, and the live mockup gets that
part correct.

## The published principles worth citing

Ranked by how much weight each carries in a Danish public-sector discussion.

| Source | Why it applies |
| --- | --- |
| [EN 301 549 / WCAG 2.1 AA](https://digst.dk/tilsyn/webtilgaengelighed/) via the Danish web accessibility act | Not advice. The legal floor, enforced by Digitaliseringsstyrelsen. The contrast failure above is measured against it |
| [Det Fælles Designsystem](https://designsystem.dk/) | The Danish public sector's common design system, from the same agency that enforces the accessibility law. It uses line illustration rather than photography and a restrained palette. It is the closest thing to an official Danish house standard |
| [GOV.UK Government Design Principles](https://www.gov.uk/guidance/government-design-principles) | The most widely cited set in public-sector digital work. Principle 2, "Do less". Principle 4, "Do the hard work to make it simple". Principle 6, "This is for everyone" |
| [Nielsen Norman Group](https://www.nngroup.com/articles/banner-blindness-old-and-new-findings/) on banner blindness and photographs as content | Eyetracking research consistently finds that users look at images carrying information and skip images that read as decoration. Decorative stock photography is not neutral; it is actively filtered out |
| [W3C Web Sustainability Guidelines](https://w3c.github.io/sustainableweb-wsg/) | Page weight as an environmental cost. Pointed, for this subject |
| [Europa Component Library](https://ec.europa.eu/component-library/) | Relevant because the audience is EU Member State institutions and part of the funding is the Commission's Technical Support Instrument |
| Edward Tufte, *The Visual Display of Quantitative Information* | The data-ink ratio. Decoration competes with information for the reader's attention. The argument generalises from charts to pages, and it is a reference this particular audience respects |

## Is it old-fashioned?

Partly, but that is the weakest way to put it and it invites a pointless
argument about taste.

The pattern of alternating full-bleed colour bands, a hero photograph with an
aspirational slogan, and paired photo-and-colour "split boxes" spread through
template marketplaces and CMS vendor themes between roughly 2014 and 2020. It
is still the default in Scandinavian public-sector CMS platforms, so it is
ubiquitous rather than obsolete. Calling it dated is both arguable and beside
the point.

The accurate criticism is about **category, not age**. This is a marketing
vernacular, developed to hold the attention of an uncommitted consumer
audience who did not come looking for anything in particular. GreenREFORM-EU
is a reference product for a specialist audience who arrive with a specific
task already in mind. Borrowing the marketing vernacular is a category error,
and the symptom of the error is measurable: 249 words in 3,470 pixels.

The direction serious technical and research publishers have moved in is
typographic and content-dense, with graphics that carry information. That is
not an absence of design. It is harder to do than applying a template, which
is rather the point of GOV.UK principle 4.

## A test, instead of an argument about taste

Arguing "fewer pictures" against "more pictures" has no resolution, because
both sides are stating preferences. Proposing a shared test does, and it is
also a fairer way to treat a colleague's work, because it applies equally to
both mockups.

The test already written into this workspace, in
[AGENTS.md](AGENTS.md), is:

> Green is never decoration. If something is green it is either the model
> itself or something you can click.

Generalised: **every graphic element must either carry information or be
removed.** Applied honestly:

| Element | Carries information? |
| --- | --- |
| The connected discs in `mockups-graphic/` | Yes. They are DREAM's actual models, and the arrangement states the lineage |
| The inline lineage diagram | Yes. MAKRO to GrønREFORM to GreenREFORM-EU, labelled |
| The squared grid background | No, but it is monochrome CSS, costs no bytes, and fades out. Borderline, and it should be defended or dropped on that basis |
| The farmyard photograph | No. The site's own markup places it outside the accessibility tree |
| The child in front of wind turbines | No, and it additionally asserts something the model does not |
| The coloured band behind the hero buttons | No, and it costs 1.1 contrast points, taking the page below the legal minimum |

This test does not produce a plain site. It produces a site whose graphics are
specific to this model and could not be lifted onto any other organisation's
page, which is a stronger brand position than stock photography, not a weaker
one. A stock photograph of a wind farm is available to every competitor. The
disc diagram of the DREAM model family is not.

## What to do with this

The two defects found should be reported to Jonas regardless of how the wider
question is settled. They are specific, fixable, and one of them is a legal
compliance issue:

1. The hero buttons fail WCAG 1.4.3 at 3.38:1. Either darken the red on the
   green band or drop the band.
2. `Åben hovednavigationen` and the footer landmark `Bund` are Danish strings
   on a page declaring `lang="en"`. Untranslated template defaults.

Minor, and worth confirming rather than asserting: the header and footer link
to `dreamgroup.dk`, where the institute's site is `dreamgruppen.dk`. If that
is not a deliberate English-language alias, it is a broken link in two places.

The wider question is better put to the group as a choice of audience than as
a choice of style. If the site is a shop window for DREAM, the live mockup is
close to right and consistent with the parent site. If it is a working
reference for ministry modellers who will return to it repeatedly, the
density, not the decoration, is the thing to argue about.
