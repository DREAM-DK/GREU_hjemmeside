# Brief: GreenREFORM-EU 2.0 website (structure and content)

Copy this file into the **new website workspace**. This documentation folder is the content source, not the site repo. Do not add site files here.

Task for now: information architecture and page copy. Not implementation, not visual design beyond a sitemap and what each page is for.

---

## What you are building

A dedicated public website for **GreenREFORM-EU 2.0**: the model, who it is for, how it works at a high level, and a way into the technical documentation.

The documentation itself says it will live on a dedicated site. The LaTeX document remains the source of truth for mechanisms, equations, and code names. The site is the front door: shorter, navigable, and written for people who will not start at Chapter 1.

**Title of the documentation:** GreenREFORM-EU 2.0 Model Documentation  
**Subtitle:** Theoretical Framework and Architecture  
**Publisher:** DREAM, Danish Research Institute for Economic Analysis and Modelling  
**DREAM site:** https://dreamgruppen.dk/

---

## Audience

Primary: finance ministries, planning bureaus, and emissions agencies of EU Member States (TSI users).

Secondary: DREAM staff, country modelling teams, and technically literate policy analysts.

The site is not a GAMS tutorial and not a replacement for the PDF/LaTeX documentation. It should get a ministry reader to: what the model is, what it can score, what it cannot, and where to read the chapter that matches their question.

TSI 2024 pilot countries named in Chapter 1: Belgium, Finland, Austria, Italy, Poland. GreenREFORM-EU 2.0 is a KR Foundation extension to refine capabilities, generalise the architecture, and produce the documentation.

---

## Naming (use these, do not invent others)

| Use | Do not use as the public name |
|---|---|
| GreenREFORM-EU | GreenREFORM EU (unhyphenated) as the model name |
| GreenREFORM-EU 2.0 for this edition / KR Foundation project | Treat 2.0 as a new model generation unless the documentation says so |
| GreenREFORM for the Danish parent model | Confuse DK and EU |
| MAKRO as DREAM’s Danish MoF macro model | Call MAKRO the EU model |
| **Energy technology model** (code name) | **Abatement model** on the site except once, as a synonym used in DREAM project reports |
| Hard-linked: technology and CGE in one simultaneous system | Soft-linking as something this model does. Soft-linking is the alternative it rejects. A standardised interface to external energy-system models is proposed work, not a property of the documented model |

British English. Short sentences. No “highly complex”. Readable names in prose (“buildings”, “housing services”); code names only where a technical page needs them.

---

## What the site must not promise

These are explicit documentation decisions. Repeating them on a website would be wrong.

**TSI 2026 is parked (10 November 2026).** Until the contract with the Commission is settled, the site does not mention the TSI 2026 project, by name or by implication. The project page and every removed line are in `content/parked/tsi-2026.md`, with steps to restore them. The paragraph below, and the Julia and soft-linking bullets, apply again once it is restored.

**Publication timing (set 3 November 2026).** The site will not go live before the grant agreement with the Commission is signed. Copy may therefore describe the TSI 2026 project (ECONCLIMA2) as real, because it will be real by the time anyone reads it. This assumption covers award status only. It does not clear third-party consent, a licence text, a repository address, or a country list — those are tracked in `content/open-questions.md` and in the flags on each project page. If the launch date is ever brought forward ahead of signature, revisit the TSI 2026 page first.

- **Open source is allowed (changed 3 November 2026).** The model may be described as open source. Name no licence (MIT or other) until DREAM confirms the text, and do not invent a licence page. Statistics Denmark holds rights to the Danish benchmark data, so the claim does not cover that data set. Results of the TSI 2024 project were licensed to the Commission under conditions, and access to those results is limited to non-commercial, non-competitive use. The Rights section of the documentation is still a placeholder.
- **Julia is project work, not a property of the model (changed 3 November 2026).** The TSI 2026 grant was awarded, so the conversion to Julia may be described on the TSI 2026 project page as work the project will do. The model documented here is GreenREFORM-EU 2.0, written in GAMS with Python and gamY. Do not say the documented model is in Julia, and do not point a reader at a Julia code base until one exists and DREAM gives the address.
- **Soft-linking is project work, and the model itself is hard-linked (changed 3 November 2026).** The TSI 2026 grant includes a work package on an interface to external energy-system models. That may be described as project work. It is not a property of the documented model, whose defining feature is that the energy technology model and the CGE core are solved in one simultaneous system. Naming an external model is a separate question: on the core-model pages, name none. Country project pages may name the model a national team actually uses, where the source is public and the partner has cleared it.
- **Do not describe unused features as available:** household housing stock as a household asset, labour–leisure choice, central bank / monetary policy, public optimisation, bequest/demographic matrices that are not in the code.
- **Industry count:** 57 is a property of the **Danish benchmark data set**, not of the model in the abstract. Other country calibrations can have different industry lists.

Housing, if mentioned: there is **no household housing stock**. Households buy housing services (`cHou`). The dwelling stock is building capital (`iB`) of industry `68203` (renting and owner-occupation aggregated; Danish NA also has `68204`). That is ESA 2010 industry accounts, not an omission. Details: Chapter 2 § Housing and Chapter 3 capital goods.

---

## Suggested site map (starting point, not a constraint)

Use the documentation’s own reading path: architecture first, then agents, then markets.

1. **Home** — one screen: what it is, who it is for, hard-linked energy technology + CGE, modularity, links to Documentation / About.
2. **The model** — purpose (climate-neutrality 2050, EU economic governance, carbon prices, technology subsidies, mandates, investment; GDP, employment, wages, trade, fiscal accounts). Distinctive feature: continuous approximation of discrete technology choice; merit-order adoption; simultaneous solve with the macro core.
3. **How it is organised** — agents: households, firms, government (accounting, not an optimiser), rest of the world. Markets close the system. No central bank. Population is the main scale variable.
4. **Documentation** — landing page for the six chapters + appendix + PDF when it exists. Each chapter gets a short page (problem, what is endogenous, what is not, one figure if useful, link to the `.tex` / future PDF).
5. **For country teams** — TSI 2024 countries; that the model is a small-open-economy CGE calibrated to national accounts + energy balances; industry list comes from the data; GAMS + Python.
6. **About / contact** — DREAM, lineage GreenREFORM → MAKRO, KR Foundation 2.0, Commission TSI. Open source; licence text to be confirmed. https://dreamgruppen.dk/

Optional later, not now: download, Git, run instructions, country pages.

Chapters are unfoldable sections on the documentation page, not pages of their
own. Decided 5 November 2026; the reasoning is in `content/pages/documentation.md`.
They follow the documentation TOC:

| Chapter | File (current `_EN` edition) | Sections |
|---|---|---|
| Foreword | `greu_frontmatter_v5_EN.tex` | How to read; Status |
| 1 Introduction | `greu_chapter01_merged_v9_EN.tex` | Background; technical challenge; code and modularity; model economy; chapter–code map |
| 2 Households | `greu_chapter02_merged_v6_EN.tex` | Exogenous savings; Ramsey; consumption tree; energy; housing |
| 3 Firms | `greu_chapter03_merged_v5_EN.tex` | Output and price; production function; factor demand; capital; energy end purposes; energy technology; multi-output; corporate finance |
| 4 Government | `greu_chapter04_merged_v6_EN.tex` | Revenue; expenditure; public production; sector flows; fiscal closure |
| 5 Rest of the world | `greu_chapter05_merged_v4_EN.tex` | Export demand; energy exports; imports; external balance |
| 6 Markets | `greu_chapter06_merged_v4_EN.tex` | Input-output; pricing; labour; energy markets; emissions |
| A CES / indexing | `greu_appendix_merged_v3_EN.tex` | Algebra; smart indexing; calibration notes |
| References | `greu_references_v1_EN.tex` | |

Master (always check this for the live file names): the highest-numbered `greu_master_merged_v*_EN.tex`, currently **v3** (working assumption of 5 November 2026; see `content/open-questions.md` item 12).

Always read the `\GREUchapter{...}` / `\input{...}` lines in the master. Older `v1`–`v8` chapter files exist on disk and are **not** current. Note that `v1`, `v2` and `v3` of the master all compile to 124 pages, so length does not identify the current one.

---

## Local paths (this machine)

Workspace roots already used for the documentation project:

```text
I:\GroenReform\Eksterne projekter\KR-foundation forlængelse af EU-projekt\Dokumentationsnotat\FinalVersion
I:\GroenReform\Eksterne projekter\KR-foundation forlængelse af EU-projekt\Dokumentationsnotat\GREU_model
I:\GroenReform\Eksterne projekter\KR-foundation forlængelse af EU-projekt\Dokumentationsnotat\Background material
```

Add `FinalVersion` as a second (read-only) root of the website workspace. Add `Background material` if you need project PDFs. Add `GREU_model` only if a page must cite code; for structure and content it is usually enough to follow the documentation.

### Documentation (source of truth for wording)

| What | Path |
|---|---|
| Master / live file list | `FinalVersion\greu_master_merged_v3_EN.tex` |
| Title, foreword, how to read, status | `FinalVersion\greu_frontmatter_v5_EN.tex` |
| Shared layout / PDF title | `FinalVersion\preamble.tex` |
| Agent conventions (stale file table; still useful for writing rules) | `FinalVersion\AGENTS.md` |
| Current file set and open issues | `FinalVersion\outstanding_issues.md` |
| What changed, including housing and 2.0 title | `FinalVersion\revision_report.md` (Round 7) |
| Chapter–code map | `greu_chapter01_merged_v9_EN.tex`, Table after `\label{sec:intro-files}` |

The published PDF is `Website\content\Documentation\greu_master_merged_v4_EN.pdf` (10 November 2026). Use it for reading, and as the site's download. Do not hand-edit `.aux`, `.log`, `.toc`.

### Background material (lineage and project narrative, not code)

```text
I:\GroenReform\Eksterne projekter\KR-foundation forlængelse af EU-projekt\Dokumentationsnotat\Background material\
```

| File | Use for |
|---|---|
| `the_greenreform-eu_model.pdf` | Deliverable D4.3 of TSI 101195159; IP/licensing language used in the foreword rewrite |
| `Development_of_the_GreenREFORM_model.pdf` | Danish GreenREFORM parent |
| `Tpl_Application Form (Part B) (TSI)_final_v1.pdf` | TSI 2026 narrative. The grant was awarded; see the note on publication timing under "What the site must not promise" |
| `brancheopdeling_januar2026(2).xlsx` | Danish GreenREFORM industry list; `68203` = housing sector including household dwelling stock |
| `Old_Model_documentation_Joao\` | Superseded. Do not copy structure from here without checking the current `_EN` chapters |

### Model code (facts only, if needed)

```text
I:\GroenReform\Eksterne projekter\KR-foundation forlængelse af EU-projekt\Dokumentationsnotat\GREU_model\
```

Entry points: `run.py`, `model\base_model.gms`, `model\modules\`, `model\sets\`, `GREU_model\AGENTS.md`.

**Known mismatch:** documentation cites modules as `03_production.gms`; the repo files are unprefixed (`production.gms`). Same files. `outstanding_issues.md` item A1. Do not tell users to open the prefixed names unless you also say they are documentation names.

---

## Public / related URLs

- DREAM: https://dreamgruppen.dk/
- Danish GreenREFORM industry classification (same file as in Background material): https://dreamgruppen.dk/Media/639034635331031563/brancheopdeling_januar2026.xlsx
- ESA 2010 (housing services as production): https://ec.europa.eu/eurostat/esa2010/chapter/view/1/
- Statistics Denmark, dwellings in industry accounts (context only): https://www.dst.dk/en/Statistik/dokumentation/documentationofstatistics/national-accounts--fixed-capital-stock/statistical-processing

There is no live GreenREFORM-EU 2.0 site yet. Do not scrape a placeholder.

---

## How to treat the documentation as copy

- Prefer the **foreword** for the homepage and “what is distinctive”.
- Prefer **Chapter 1 § Background** for why ministries need it and for TSI / KR Foundation 2.0.
- Prefer **Chapter 1 § Core technical challenge** for hard-linking vs soft-linking and the energy technology model.
- Prefer **Chapter 1 § Agents** for the one-paragraph description of each agent.
- Prefer **“How to read this document”** for the documentation landing page.
- Do not rewrite chapters into the site. Summarise, then point to the chapter.
- If the `.tex` and older PDFs or LyX/HTM disagree, follow the current `_EN` chapter; if that disagrees with `GREU_model`, follow the code and say so.
- Do not edit the documentation unless asked.

---

## Working method

1. Plan the sitemap (pages, nav, what is on Home vs Documentation).
2. Draft headings and 1–3 short paragraphs per page, with a pointer to the `.tex` section used.
3. List open questions for DREAM (licence, URL, logo, whether the PDF is public, contact).
4. Implementation and visual design come later.

Address the person you are talking to. Several people edit the documentation; there is no assumed named owner.
