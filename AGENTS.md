# GreenREFORM-EU 2.0 website — agent primer

This folder is the **website workspace**. The documentation in the sibling
`FinalVersion` folder is the content source. Do not add site files there.

Several people edit. Address the person you are talking to. Do not assume a
named owner.

## What this workspace is for now

Information architecture and page copy. Not a visual design system. Not a
GAMS tutorial. Not a replacement for the PDF/LaTeX documentation.

Implementation of a live site comes later. Optional later, not now: download,
Git, run instructions, country pages.

## Open this as a multi-root workspace

Local `Background material/` in this folder holds the KR proposal (Aug 2025),
the February 2026 project plan, and the March 2026 partner deck. Read
`content/background-notes.md` before using those files as copy. They are
project narrative, not a substitute for the `_EN` chapters.

Use `greenreform-eu-website.code-workspace`. It mounts:

| Root | Role |
| --- | --- |
| Website (this folder) | Write here |
| Documentation (`FinalVersion`) | Read only. Prefer the compiled PDF of the current master when it exists; otherwise the live `_EN` `.tex` named in the master |
| Background material | Read only. Lineage and project PDFs, not code |

Do not add `GREU_model` unless a page must cite code.

Always check live file names in the highest-numbered master. Several masters
exist: `v1`, `v2` and `v3` as of 5 November 2026, and all three compile to 124
pages, so the page count will not tell them apart. Older `v1`–`v8` chapter
files exist on disk and are not current.

## Copy rules

- British English. Short sentences. No “highly complex”.
- Use **GreenREFORM-EU** (hyphen). Use **GreenREFORM-EU 2.0** for this edition.
- Use **GreenREFORM** only for the Danish parent. Do not call MAKRO the EU model.
- Use **energy technology model** in public copy. Mention **abatement model**
  once, as the synonym used in DREAM project reports.
- Hard-linked means technology and CGE in one simultaneous system. Soft-linking
  is the alternative this model rejects. A standardised interface to external
  energy-system models is proposed work, not a property of the documented model.
- Readable names in prose (“buildings”, “housing services”). Code names only
  where a technical page needs them.
- Summarise chapters. Do not rewrite them onto the site.
- If `.tex` and older PDFs disagree, follow the current `_EN` chapter. If that
  disagrees with `GREU_model`, follow the code and say so.
- Do not edit the documentation unless asked.

## Do not promise

- **Open source is allowed.** The model may be described as open source. Do
  not name a licence (MIT or any other) until DREAM confirms the licence text.
  Do not extend the claim to the Danish benchmark data set: Statistics Denmark
  holds its rights. The repository is https://github.com/DREAM-DK/GREU
  (given by DREAM on 10 November 2026). It has no tagged release yet, so do
  not link to "release 2.0" until one exists.
- **TSI 2026 is parked (10 November 2026).** Do not mention the TSI 2026
  project (ECONCLIMA2) on the site, by name or by implication ("version 3.0",
  "successor project", "18 Member States"), until the contract with the
  Commission is settled. The page and every removed line are in
  `content/parked/tsi-2026.md`. That overrides the next bullet until then.
  When asked to restore it, follow "Instructions for the agent" in that file.
- **LaTeX source.** Not published (decided 10 November 2026), neither on the
 site nor in the repository. The documentation is offered as a PDF only.
- **Publication timing.** The site does not go live before the grant agreement
  with the Commission is signed, so TSI 2026 (ECONCLIMA2) may be written about
  as a real project. That covers award status only, not partner consent, the
  licence, the repository address or the country list.
- **Julia** is TSI 2026 project work. The documented model is GAMS with Python
  and gamY. Do not call the documented model Julia, and link to no Julia code
  base until one exists.
- **Soft-linking** is TSI 2026 project work. The documented model is
  hard-linked, and that is its defining feature. Name no external energy model
  on the core-model pages; a country project page may name the one that team
  uses, from a public source and with the partner's clearance.
- Do not describe unused features as available: household housing stock as a
  household asset, labour–leisure choice, central bank / monetary policy,
  public optimisation, bequest/demographic matrices that are not in the code.
- **57 industries** is a property of the Danish benchmark data set, not of the
  model in the abstract.
- Housing: no household housing stock. Households buy housing services
  (`cHou`). The dwelling stock is building capital (`iB`) of industry `68203`.
- Module files in the repo are unprefixed (`production.gms`). Documentation
  cites prefixed names (`03_production.gms`). Same files.

## Where copy should come from

| Site surface | Prefer |
| --- | --- |
| Home, distinctive feature | Foreword (`greu_frontmatter_v5_EN.tex`) |
| Why ministries need it; TSI / KR Foundation 2.0 | Chapter 1 § Background |
| Hard-linking; energy technology model | Chapter 1 § Core technical challenge |
| Agents | Chapter 1 § Agents |
| Documentation landing | “How to read this document” |
| Applications / analyses | Public papers only; TSI paper is the launch example. Not Danish GrønREFORM. |

Master: `greu_master_merged_v3_EN.tex` (working assumption of 5 November 2026;
see `content/open-questions.md` item 12). The published PDF is
`content/Documentation/greu_master_merged_v4_EN.pdf` (10 November 2026). Read
it in preference to the `v3` PDF. Its `.tex` is not in `FinalVersion`.
