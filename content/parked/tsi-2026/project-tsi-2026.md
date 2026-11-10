# Project: Economic Analysis for Climate Action 2 (TSI 2026)

**Nav title:** Applications › Projects › TSI 2026  
**Path:** `/applications/projects/tsi-2026`  
**Status:** Draft copy. Not cleared by DREAM or SG REFORM. Written as if the
project had been launched. Source is the grant preparation file of October
2026. See the flags at the end.

## Headline and lead

> Economic Analysis for Climate Action 2: GreenREFORM-EU in 18 Member States

> From October 2026 to January 2029 the European Commission funds DREAM to
> bring GreenREFORM-EU to 18 Member States. The project trains national
> teams, moves the code to the open-source language Julia, automates the
> supply of Eurostat data and builds new sectoral sub-models for the
> sectors the countries ask for.

Two buttons under the lead:

- **Commission project page** → https://reforms-investments.ec.europa.eu/technical-support-instrument-0/revenue-administration-and-public-financial-management/economic-analysis-climate-action_en
- **Model documentation** → `documentation.html`

## Record

| | |
| --- | --- |
| Funder | European Commission, Technical Support Instrument (TSI), through SG REFORM |
| Delivered by | DREAM |
| Period | 1 October 2026 to 31 January 2029. 28 months. |
| Grant | TSI project 101359253, acronym ECONCLIMA2 |
| Model edition | The next after version 2.0, towards version 3.0 |
| Member States | 18, in two tracks |
| Outcome | Trained national teams, an open-source code base, a Eurostat data pipeline, new sub-models |

## Why it was set up

The amended Directive 2011/85/EU on national budgetary frameworks asks
Member States to assess and report the macro-fiscal effects of climate change
and climate policy. Many ministries lack the tools, the data and the staff to
do it. Their work tends to cover single aspects. Climate risk is still rarely
part of forecasts and budget plans.

The TSI 2024 project built GreenREFORM-EU for five institutions. It showed
that collecting data by hand was the main delay for national teams. Eighteen
Member States asked the Commission for further support.

*Source: Commission project page, Context; DoA part B § 1.1 and 1.2.*

## What it is part of

The Commission project is called Economic Analysis for Climate Action. It has
three pillars:

1. The GreenREFORM-EU model and similar models.
2. Analytical tools for macro-fiscal impacts, nature-related risks and the
   costs of climate events.
3. Integrating climate risk into fiscal and budgetary planning.

DREAM's grant covers the first pillar. This page describes that part only.

*Source: Commission project page, Support delivered; DoA part B § 1.3.*

## What it sets out to do

1. Deliver a fully functional, open-source GreenREFORM-EU model in Julia, with
   technical documentation, a user guide and server access.
2. Give national teams a three-day introduction seminar, online training,
   country visits and a final workshop.
3. Build an automated Eurostat data pipeline, and a standard interface for
   countries that run their own energy-system models.
4. Build a benchmark technology data set and guidelines for a common EU
   technology data set.
5. Design, code, calibrate and hand over one or two new sectoral sub-models.

*Source: DoA part B § 1.2.*

## What the project does

- **Code and model.** The code moves from a mix of Python, GAMS and gamY to
  Julia, before the new teams start. A GAMS licence is then no longer needed.
  A solver licence is still needed. DREAM keeps the model, the documentation
  and the user guide up to date during the project.
- **Server.** Designated staff in each Member State get restricted access to
  a Linux server hosted by the Technical University of Denmark. The project
  provides the solver licence.
- **Training.** A joint three-day seminar in Copenhagen. Online training with
  exercises. A two-day visit by DREAM experts to each country in the
  introduction track. A final joint two-day workshop on the new sub-models.
- **Data.** An automated pipeline that imports Eurostat input-output tables,
  sector accounts and emissions and prepares them for the model. DREAM also
  publishes calibration guidelines and a paper that calibrates the model to
  Danish data as a worked example.
- **Technology data.** A benchmark technology data set for Denmark, with
  costs, energy mix, capital intensity and emission-reduction potential. It
  is the blueprint for a common EU technology data set, which an external
  provider builds.
- **Energy-system models.** GreenREFORM-EU solves its energy technology model
  and the macroeconomy together. Some countries also keep their own
  energy-system models. The project designs a standard interface so that
  they can exchange baseline scenarios with GreenREFORM-EU, and tests it with
  one country.
- **New sub-models.** One or two sectoral sub-models. The countries decide the
  scope during the project.
- **Technical report.** A final report on the Danish benchmark calibration,
  with examples from other countries where possible, and with policy
  experiments.

*Source: DoA part A, work packages 2 to 14; DoA part B § 1.5.*

## Timeline

- **October to December 2026.** Preparation. The Julia code base and the first
  documentation.
- **January 2027 to November 2028.** Work with the Member States.
- **December 2028 to January 2029.** Final reports.

*Source: DoA part A, WP1.*

## Who takes part

Eighteen Member States take part. The roles differ:

- **Introduction track, nine countries.** Cyprus, Germany, Estonia, Greece,
  Spain, Latvia, Malta, Portugal and Sweden. They have no working model of
  this kind. They receive a customised model, server access, training and a
  country visit.
- **Implementation track, thirteen countries.** Austria, Belgium, Cyprus,
  Germany, Greece, Spain, Finland, Italy, Latvia, Malta, the Netherlands,
  Portugal and Sweden. They work on national calibration, Eurostat data and
  the link to energy-system models, and on new sub-models.
- **Both tracks.** Cyprus, Germany, Greece, Spain, Latvia, Malta, Portugal and
  Sweden.
- **Advisers.** Austria, Belgium, Finland and Italy took part in TSI 2024.
  They advise the introduction track.
- **Observers.** France, Slovakia and Slovenia.
- **Denmark.** Advisory role.

Country progress is described on the country pages as each institution agrees
to publish it. This page does not report it.

*Source: DoA part B § 1.2.*

## What it delivers

DREAM publishes the public outputs on this website.

- **Code.** An open-source Julia code base, ready in December 2026. The final
  code base follows in November 2028.
- **Documentation and user guides.** First versions in January 2027. Final
  versions in November 2028. A user guide for the server in April 2027.
- **Training.** Seminar and training material, with online presentations.
- **Data pipeline.** A technical note on the Eurostat pipeline, by June 2027.
- **Calibration.** Guidelines and a benchmark calibration paper, by
  December 2027.
- **Technology data.** Guidelines, by September 2027. The benchmark data set
  has restricted access.
- **Energy-system interface.** A concept note and a technical report, by
  December 2027.
- **New sub-models.** Code and documentation, by September 2028. Their
  benchmark data set has restricted access.
- **Final technical report.** By November 2028.

Dates are planned dates from the grant. They can move.

*Source: DoA part A, list of deliverables and milestones.*

## Results

The project has published no results yet. Analyses appear under
[Analyses](../analyses.md) as they are published.

The model it builds on, and the first public analysis, come from the
[TSI 2024 project](project-tsi-2024.md). The refined edition it starts from
comes from [Version 2.0](project-version-2-0.md).

## Read more

- [The Commission's project page](https://reforms-investments.ec.europa.eu/technical-support-instrument-0/revenue-administration-and-public-financial-management/economic-analysis-climate-action_en)
- [Model documentation](../documentation.md)
- [TSI 2024](project-tsi-2024.md) and [Version 2.0](project-version-2-0.md)

---

## Flags for the team

1. **Rules updated, 3 November 2026.** `WEBSITE_BRIEF.md`, `AGENTS.md`,
   `.cursor/rules/copy-and-sources.mdc` and `content/background-notes.md` no
   longer forbid the Julia conversion, the energy-system interface or TSI 2026
   narrative. All four now say the same thing this page does: these are
   project work, not properties of the documented model, which is GAMS with
   Python and gamY and is hard-linked. The page still names no external model.
2. **Launch assumed, and that is now the standing assumption.** The site does
   not go live before the grant agreement is signed, so the present tense is
   safe. If the launch is ever brought forward ahead of signature, this page
   is the first one to revisit.
3. **Julia and the licence.** The plan says the Julia code is public and
   open source. It names no licence. The site names none either. Note that
   Version 2.0, the GAMS model, is the one described in the documentation.
   The Julia version will need its own documentation.
4. **Country list.** The page names the 18 countries and their roles, from the
   grant. The Commission's concept note gives slightly different groups
   (for example, the Netherlands in the introduction group, and France in it
   as a participant). The page follows the grant. Ask SG REFORM whether the
   list is public, and each country whether it agrees to be named.
5. **Other pillars.** The page says DREAM's grant covers the first pillar. The
   Commission's concept note gives pillars 0, 2 and 3 to other contractors.
   The page does not say who. Confirm that SG REFORM is content with the
   framing.
6. **Soft linking.** The grant calls one work package "soft linking to energy
   system models". The page says "interface" and "exchange baseline
   scenarios". The concept note names the TIMES model. The page does not.
7. **Dates.** Delivery dates are the due months of the grant, turned into
   calendar months from October 2026. Check them before publishing, and
   decide whether the site should promise them.
8. **Money and people.** The page leaves out the grant total, the budget, the
   staff list and the subcontractors. The University of Copenhagen and an
   external technology data provider both carry subcontracts.
9. **Visibility.** The grant requires the EU emblem and a funding
   acknowledgement on the project website, under Article 17 and Annex 5. The
   grant says a custom domain will point to a GreenREFORM-EU hub on the DREAM
   portal, which holds all public outputs. That is probably this site. Add the
   emblem and the exact wording from Annex 5 to the footer and to this page.
10. **Version 3.0.** Applications and Documentation say "towards version 3.0".
    The grant does not use a version number. Confirm it.
11. **Project title.** The Commission calls it "Economic Analysis for Climate
    Action". The grant adds "2 – Green Policy Modelling through the
    GreenREFORM-EU model". The page uses the shorter title with "2".
12. **Commission page.** My fetch showed the text but no document list. Check
    for more links.
13. **Version 2.0 overlap.** The 9 October meeting asked for the 2.0
    documentation and this website to be ready for the launch of this
    project. The Version 2.0 page and this page should agree on dates.
