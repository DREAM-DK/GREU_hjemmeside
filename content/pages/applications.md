# Applications

**Nav title:** Applications  
**Path:** `/applications`

Two objects on one hub. Do not collapse them.

| Object | Answers | Lives under |
| --- | --- | --- |
| **Analysis** | Has anyone scored a question like mine? | `/applications/analyses/…` |
| **Project** | Who funded this generation of the model? | `/applications/projects/…` |

A researcher or official starts with analyses. Projects are the map around
them. An analysis names its project. It does not live only on that page.

A third object, **Country team**, was parked on 3 November 2026 to bring the
launch forward: see `content/parked/country-teams.md`. It is the only part of
this hub that needs four institutions to clear being named.

The TSI 2026 project was parked on 10 November 2026, until the contract with
the Commission is settled: see `content/parked/tsi-2026.md`.

## Analyses

Public experiments, papers and notes that use GreenREFORM-EU. Country studies
appear when the institution publishes them.

**No filter at launch** (decided 10 November 2026). With one analysis there is
nothing to filter, so the filter buttons were taken off `applications.html`.
Add them back when there are enough analyses to filter. The planned filter is
by policy question (carbon tax / ETS, technology subsidy, transport fuels,
industrial transition, with versus without the energy technology model), then
by model version and country. The removed markup was:

```html
<div class="chips" role="group" aria-label="Filter analyses by policy question">
  <button type="button" class="chip" aria-pressed="true">All</button>
  <button type="button" class="chip" aria-pressed="false">Carbon tax / ETS</button>
  <button type="button" class="chip" aria-pressed="false">Technology subsidy</button>
  <button type="button" class="chip" aria-pressed="false">Transport fuels</button>
  <button type="button" class="chip" aria-pressed="false">Industrial transition</button>
  <button type="button" class="chip" aria-pressed="false">With vs without the technology model</button>
</div>
```

It sat directly after the intro paragraph under "Analyses", which also said
"Filter by the policy question." The `.chips` styles are still in `site.css`.

Each record: title, date, authors and institution, three sentences on what
was scored, model version, technology block on/off/compared, data set, what
the run could not do, link to the PDF. Point to the user guide, once it is published, for how to
reproduce a shock. Do not rewrite the paper onto the site.

Launch item:

- *The GreenREFORM EU model*, final paper of the TSI 2024 project (25 February 2026, DREAM). Carbon tax with
  revenue recycling, with and without the energy technology model. Version
  1.0, Danish benchmark data, TSI 2024. Not a country-team paper. The PDF
  currently sits on dreamgruppen.dk; republish or copy onto this site so the
  international reader is not sent into the Danish catalogue as the only path.

Empty state is allowed. Internal country notes stay off the list.

News announces a paper. Analyses keeps it.

## Projects

Each project page lists the analyses that came out of it. Do not treat a
project card as a substitute for the analysis record.

Two kinds of project sit on this hub, and the distinction matters. The first
two are generations of the model itself, funded to build it. The last four
are other people's projects that use it. A reader who cannot tell them apart
will credit DREAM with work it did not do, and will read a Belgian or Finnish
result as a property of GreenREFORM-EU.

All six sit in **one group under one heading**, in the order above: the two
generations first, then the four adopters. The distinction is carried by the
introduction, not by headings.

Until November 2026 the introduction read "funding vehicles and generations of
the model". That was written when the hub held three projects and all three were
generations. Four adopter projects were added one at a time, and none of them is
a funding vehicle for GreenREFORM-EU or a generation of it, so the sentence
quietly stopped being true. The fix broadens the definition rather than dividing
the grid.

Headings for the two kinds were tried and rejected. At six projects, two
headings over groups of two and four make a structural claim that the content
does not need, and the Faroe Islands project sits awkwardly on either side of
it. Revisit this when there are enough adopter projects that a reader has to
scan for the one they want. At that point grouping earns its keep, and the
grouping may not be build-versus-use: it could be by country, by question, or by
model version.

| Project | What it is | DREAM's role |
| --- | --- | --- |
| [TSI 2024](project-tsi-2024.md) | Built version 1.0 for five institutions | Delivered it |
| [Version 2.0](project-version-2-0.md) | KR Foundation year of refinement and documentation | Delivered it |
| [Viet Nam](project-viet-nam.md) | UCPH with three Vietnamese institutes, MFA funded | Collaborates on the modelling |
| [FinReform](project-finreform.md) | Finnish national project, TAH Foundation funded | None |
| [Belgium: CEEP-IT](project-belgium.md) | VITO/EnergyVille, FPB and ICEDD, Energy Transition Fund | None |
| [Faroe Islands](project-faroe-islands.md) | Fiscal sustainability model for the Faroese Economic Council | Builds it |

The Faroe Islands project does not fit the two-way split cleanly. DREAM builds
the model, as in the first two, but it is commissioned by someone else for
their own use, as in the last four. It is also the only one outside the EU and
the only one whose subject is not climate policy. It sits in the second group
because the funding and the purpose are the partner's. The introduction
therefore says DREAM works on two of them, rather than letting the contrast
with "all delivered by DREAM" imply that DREAM is absent from every adaptation.
That clause is the one piece of the introduction that cannot be cut: without
it, the sentence about the generations quietly makes a false claim about the
Faroe Islands.

Clearance status, which is what gates publication:

| Page | Status |
| --- | --- |
| Viet Nam | **Approved** by UCPH, 5 November 2026 |
| FinReform | **Approved** by Luke, 4 November 2026, with changes |
| Belgium | **Approved** by VITO/EnergyVille and FPB, 9 November 2026, with changes |
| Faroe Islands | No request sent yet |

Every page ends with numbered flags recording what is still unverified.

*Sources: Chapter 1 background; `content/background-notes.md`; TSI paper
(February 2026).*
