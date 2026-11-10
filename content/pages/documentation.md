# Documentation

**Nav title:** Documentation  
**Path:** `/documentation`

## How to read

The document follows the agents of the model and then closes with the markets
that connect them. Chapter 1 sets out the architecture. Chapters 2 to 5 take
the household, the firm, the government and the rest of the world in turn.
Chapter 6 is where the pieces meet. Appendix A collects the CES and CET
algebra and the indexing device used in the GAMS code.

A reader who wants one part of the model should read Chapter 1 first, then
that chapter, then the matching section of Chapter 6. A reader who wants to
work with the code should read Chapter 1 and Appendix A first.

Where the text makes a claim about what the model does, a note gives the
equation, set, dummy or switch in the code that supports it.

*Source: Foreword, How to read this document.*

## Status of this edition

This site summarises GreenREFORM-EU 2.0 as documented in the current `_EN`
LaTeX files. The implementation is GAMS, supported by Python.

**The published PDF is `content/Documentation/greu_master_merged_v4_EN.pdf`**
(supplied 10 November 2026; compiled 4 November 2026; 124 pages, 0.7 MB). The
Download button on `documentation.html` points at it. On the live site, give it
a readable file name, for example `greenreform-eu-2.0-documentation.pdf`.

The `v4` master `.tex` is not in `FinalVersion`, which stops at `v3`. A text
comparison of the two PDFs finds one change of substance: a new paragraph in
Chapter 6.3 saying the model has no unemployment rate, and that the employment
gap is not one. The rest is the date (November rather than October 2026) and
layout. The chapter summaries therefore still rest on the `v3` file list below.
The Markets summary now carries the unemployment point.

*Source: Foreword, Status; `greu_master_merged_v4_EN.pdf`; `WEBSITE_BRIEF.md`.*

## How the documentation is presented

Decided 5 November 2026. The PDF is the document. The site is the map.

- **The compiled PDF is the download.** It is 124 pages. Open question 2 was
  settled on 10 November 2026, when the PDF was supplied for the site.
- **The LaTeX source is not published.** Decided 10 November 2026. It is not
  offered on the site or in the model repository. The second button on the page
  points at Get the model.
- **Each chapter gets a short summary on this page**, in an unfoldable section
  rather than a page of its own.
- **The documentation is not rendered into HTML.**

The reason for the last point is authority, not effort. `AGENTS.md` and the
brief both make the LaTeX document the source of truth for mechanisms,
equations and code names. A full HTML rendering is a second copy of that text,
and the first time it lags a revision there are two documents that disagree
about an equation, with no way for a reader to tell which is current. The
effort is real as well: the live edition carries 110 display equations, about
1,650 pieces of inline maths, 13 TikZ diagrams, 7 figures, 24 tables, 196
endnotes and roughly 1,300 `\file{}` code references, so conversion needs a
LaTeXML or tex4ht pipeline and a separate SVG build for the diagrams. Nobody on
the website side can run LaTeX at present.

What HTML would buy is findability: search indexing, a link to one section,
reading on a phone, and turning those 1,300 code references into links into the
repository. Each of those depends on the repository address and the licence,
which are open questions 1 and 9. Revisit when both are settled.

### Why unfoldable sections, not sub-pages

The Contents list on the page becomes the summaries. Unfolding a chapter shows
the problem it treats, what is endogenous, what is not, and a link into the
PDF.

- It adds no level to the navigation. Seven sub-pages would appear in the
  sitemap, in the footer and in every breadcrumb, for content that is a few
  paragraphs each.
- A reader comparing two chapters can open both without leaving the page.
- `<details>` and `<summary>` are native HTML. No framework, no script, and
  keyboard and screen-reader behaviour comes for free.

Built on 5 November 2026. Three things it needed, all now in place:

1. **Each section carries an `id`**, so `documentation.html#firms` links to one
   chapter. The sections work closed and without script; a few lines at the foot
   of the page open the one named in the address.
2. **Find-in-page.** Chrome expands a closed `<details>` when the browser's
   find lands inside it. Firefox and Safari do not reliably. The visible summary
   line therefore carries the words a reader is likely to search for: it repeats
   the section list of the chapter rather than teasing it.
3. **A size rule.** If a chapter summary needs a figure and more than about 200
   words, it has outgrown an unfoldable section and should become a page. The
   brief allows a figure per chapter, so this is likely to come up. None of the
   eight summaries written so far needs a figure.

Each summary follows the same shape: what the chapter treats, what the model
decides there, what it takes as given, and the list of sections. "Decided here"
and "Taken as given" are the brief's "what is endogenous, what is not" in words
a ministry reader will not have to translate.

Four of the summaries carry a point that corrects a reasonable assumption, and
those are the ones worth keeping if the text is ever cut. Households optimise
over two margins only, so there is no labour–leisure choice. The government is
an accounting framework, not an optimiser. The rest of the world is where the
export elasticity turns a cost shock into a quantity shock, which is what sizes
every result the model produces. And in Chapter 6, only one price in the model
is attached to a market clearing condition, the wage, so higher demand produces
a quantity response first: the loop is a cost loop, not a scarcity loop.

## Chapters

| Page | Live file |
| --- | --- |
Each row is an unfoldable section on `documentation.html`, not a page of its
own. The anchor is what `documentation.html#firms` addresses.

| Section | Anchor | Live file |
| --- | --- | --- |
| Foreword | `#foreword` | `greu_frontmatter_v5_EN.tex` |
| 1 Introduction | `#introduction` | `greu_chapter01_merged_v9_EN.tex` |
| 2 Households | `#households` | `greu_chapter02_merged_v6_EN.tex` |
| 3 Firms | `#firms` | `greu_chapter03_merged_v5_EN.tex` |
| 4 Government | `#government` | `greu_chapter04_merged_v6_EN.tex` |
| 5 Rest of the world | `#rest-of-the-world` | `greu_chapter05_merged_v4_EN.tex` |
| 6 Markets | `#markets` | `greu_chapter06_merged_v4_EN.tex` |
| A CES and indexing | `#ces-and-indexing` | `greu_appendix_merged_v3_EN.tex` |
| References | `#references` | `greu_references_v1_EN.tex` |
