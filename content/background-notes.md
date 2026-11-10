# Notes from local Background material

Folder: `Website/Background material/` (not the sibling `Dokumentationsnotat` copy).

| File | Date | What it is |
| --- | --- | --- |
| `Project proposal August 2025.pdf` | Aug 2025 | KR Foundation narrative for **GreenREFORM EU Version 2.0**. This is the awarded 2.0 grant, not the TSI 2026 bid. |
| `Project activities and timeline for GreenREFORM EU February 2026.pdf` | 16 Feb 2026 | Project plan v2 (Jens Sand Kirk). Revises the August timeline. |
| `GreenREFORM EU 2.0 Project Meeting March 2026.pptx` | 25 Mar 2026 | Partner meeting. Status of documentation, energy technology work, and the four country teams. |
| `ECONCLIMA2_GAP_meeting_Ignacio_8Oct2026.pptx` | 8 Oct 2026 | DREAM's slides for a grant agreement preparation meeting with SG REFORM. Administrative: two budget corrections, three changes to the Description of the Action, a staff replacement, reallocation between work packages. **Almost nothing in it is site copy.** See the note below. |

Use these for **project narrative** (who funds 2.0, who the partners are, what 2.0 is for). Do not override the live `_EN` documentation for mechanisms. Several proposal sentences are **not** site facts.

---

## What 2.0 is, in these files

TSI 2024 built **GreenREFORM-EU Version 1.0** (Commission). It ran about one year and ended December 2025.

KR Foundation funds **Version 2.0**: one year from January 2026, to keep momentum, support the remaining partners, refine the model, and publish documentation. The March deck states the grant as **EUR 66,500**. KR Foundation also part-funded the original Danish GreenREFORM research project.

Aim in February/March 2026: finish **by October 2026**, not December, to limit overlap with a hoped-for TSI 2026 start in September 2026.

Headline activities: model development (documentation + refinements), capacity building, data and implementation support, plus (from Feb 2026) support to a **UCPH Vietnam** partnership.

---

## Partners (do not copy Chapter 1 blindly)

TSI 2024 started with **five** Member State institutions. Chapter 1 still names Belgium, Finland, Austria, Italy and **Poland**.

The August proposal and later 2.0 files say **four** remain active: Ministries of Finance of **Austria, Finland and Italy**, and the **Federal Planning Bureau of Belgium**. One of the original five withdrew (resources). Poland is not in the 2.0 partner list.

Belgium is described as the furthest along (proposal risk section; March status).

---

## Country status (March 2026)

Useful for a later “for country teams” page. Not properties of the documented core model.

- **Austria:** Scripted, reproducible data pipeline from public data; calibrate this year; internal workshops. Goal: be ready when TSI 2026 starts.
- **Belgium (GreenREFORM-BE):** Baseline CGE calibration done; simple shock run; abatement module with generic Belgian data. Next: technology catalogues for the top six emitting sectors; scenarios. Ambition: industrial green-transformation study. Two approaches named in the deck: top-down linking with **TIMES**, and integrated technology catalogues inside GreenREFORM-BE. A Python script builds catalogues from TIMES processes. **Do not** describe GreenREFORM-EU 2.0 itself as soft-linked to TIMES.
- **Finland (FinReform):** 2019 national dataset, target Q1 2026; then calibration; pilots on environmental taxation and transport fuels.
- **Italy:** Harmonise national accounts and energy balances; exploratory carbon-price (or similar) shocks by Q4 2026.

Capacity building in 2.0: almost nothing planned yet (5 person-days reserved).

---

## Model development named in the 2.0 plan

Budget lines (Feb 2026): documentation, user guide, publish, promote, data and calibration, energy markets, model structure, “abatement model”.

March deck, now: documentation, energy technology model, model structure. Next: data and calibration, energy markets. Later: user guide, publish.

Energy technology model (deck): formerly “abatement”; Excel technology-data module; structure and integration (frontloaded investment). Matches the documentation naming rule.

Modularity: a parallel Faroe Islands project replaces “Green” with “Fiscal” and keeps a common core. Twelve people on model development. Frequent GitHub updates are called hard to follow. **Do not** link to GitHub or a public repo until DREAM gives the address.

Documentation goals in the deck: overview of the whole project; intuition on technical detail; guide to using and adapting the model. Structure in place in March; remaining work on details, data, and how modules connect.

---

## Vietnam (adjacent, not 2.0 deliverable)

Partnership with UCPH Development Economics Research Group. DREAM’s PhD-year finance is **outside** the 2.0 budget.

March deck (UCPH project): *Promoting Green Reforms in a Rapidly Industrializing Country… Viet Nam*. MFA grant, DKK 4.8 million, 1 Jan 2026 – 31 Dec 2027. Vietnamese counterparts: IPSS, NIEF, ISPAE. Custom GreenREFORM for Vietnam (2024 SAM, population, technology catalogues).

Do not present Vietnam as a TSI country or as a 2.0 output.

---

## TSI 2026

August 2025: four partners + DREAM were **preparing** a 2026 TSI bid for country-specific submodels. Not a fact about the current model.

February 2026: that application had support from institutions in **18** Member States and was **pre-qualified** by the Commission; start then expected September 2026.

October 2026: **the grant was awarded.** TSI project 101359253, acronym ECONCLIMA2, in grant agreement preparation through October. From 3 November 2026 the working assumption is that the site does not launch before the grant agreement is signed, so TSI 2026 may be written about as a real project. See `content/parked/tsi-2026/project-tsi-2026.md`.

10 November 2026: **parked** until the contract is settled. The site does not mention the project. See `content/parked/tsi-2026.md`.

That assumption settles award status and nothing else. Still open: whether SG REFORM treats the 18-country list as public and whether each country agrees to be named; the licence for the Julia code; the EU emblem and the funding acknowledgement required by Article 17 and Annex 5.

### `ECONCLIMA2_GAP_meeting_Ignacio_8Oct2026.pptx`

DREAM's own slides for the grant agreement preparation meeting with SG REFORM, 8 October 2026. It is an administrative deck — two budget corrections DREAM describes as its own budgeting errors, three changes to the Description of the Action, a staff replacement, and reallocation between work packages. None of that is site copy.

Two things in it are useful. Slide 6 brings the server user guide (D2.1) forward from month 26 to month 7, which is a deliverable date the TSI 2026 page should match. Slide 3 states that the key deliverable of the 2.0 project is an improved model with documentation and a user guide **published on a dedicated website in time for the launch of ECONCLIMA2** — that is this site, and it is the clearest statement of what it is for.

Two things in it must stay off the site. Slide 7 names a senior economist who has left DREAM; employment of named individuals is not site material. Slide 3 gives candid assessments of how Belgium, Finland, Italy and Austria are progressing, including one team said to be struggling with resource allocation. Country pages report only what each institution agrees to publish.

---

## Do not take these proposal sentences onto the site

| Claim in the PDFs / deck | Why not |
| --- | --- |
| Model will be **open source** | Allowed since 3 November 2026. Name no licence until DREAM confirms the text. Does not cover the Danish benchmark data |
| GreenREFORM-EU is a **simplified** Danish GreenREFORM | Documentation does not use that as the public description; 2.0 is architecture + docs, not “lite DK” |
| **Soft-link / TIMES** as a model feature | Documented model is hard-linked. The TSI 2026 interface is project work. TIMES is Belgian (and Italian) **country** work |
| **Five** TSI countries as current 2.0 partners | 2.0 files name four; Poland withdrew |
| Julia as a property of the **documented** model | Allowed since 3 November 2026 as TSI 2026 project work. The 2.0 model documented here is GAMS with Python and gamY |
| User guide and public Version 2.0 already available | Planned second-half / later; March: not done |
| Public GitHub | Mentioned as a maintenance problem. Do not link to a repository until DREAM gives the address |

---

## Usable for About / Home (if DREAM agrees)

- DREAM: non-profit; core funding from the Danish Ministry of Finance; also client work. About 30 model developers in one office (proposal).
- Lineage: Danish GreenREFORM (KR-supported via the Green GDP project with UCPH and others) → GreenREFORM-EU under TSI 2024 → KR Foundation 2.0.
- Danish GreenREFORM was used by the Expert Group on Green Tax Reform and in the 2024 Green Tripartite debate. That is **DK GreenREFORM**, not the EU model scoring Danish agriculture.
- Coalition of Finance Ministers / Helsinki principle 4 / Green Macroeconomic Modelling Initiative: dissemination context, not a product claim.
- Statistics Denmark: TSI data partner; may subcontract on 2.0.
- 2.0 publication intent: refined model + theoretical documentation. The website is the front door to that documentation.
