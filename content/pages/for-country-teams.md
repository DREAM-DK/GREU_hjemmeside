# For country teams

**Nav title:** For country teams  
**Path:** `/for-country-teams`

## What you are calibrating

GreenREFORM-EU is a small-open-economy CGE. A country application is
calibrated to that country’s national accounts and energy balances. How a
demand or production tree branches is written in the code. Which goods sit at
the bottom of the tree is settled by the data set.

The Danish benchmark data set has 57 industries. Other country calibrations
can have different industry lists. Do not treat 57 as a property of the model
in the abstract.

*Source: Chapter 1 § The partition of the data (`sec:intro-economy`);
foreword.*

## TSI 2024

The Commission’s TSI 2024 project started deployment in five Member States.
Chapter 1 names Belgium, Finland, Austria, Italy and Poland. The KR Foundation
2.0 files name four remaining partners: Austria, Finland, Italy (ministries of
finance) and Belgium (Federal Planning Bureau). One of the original five
institutions withdrew.

GreenREFORM-EU 2.0 is the KR Foundation year after TSI 2024: refine the model,
support those four teams, and produce the documentation.

Whether the public site lists five, four, or neither is still for DREAM.

*Source: Chapter 1 § Background (`sec:intro-background`).*

## Implementation

The documented implementation is GAMS, supported by Python. This page is not
a run guide. Download, Git and run instructions are out of scope for this
round.

Documentation cites module files with chapter prefixes
(`03_production.gms`). In the repository the same files are unprefixed
(`production.gms`). Until the names are aligned, use the unprefixed files in
the code and treat the prefixes as documentation names.

*Source: Foreword, Status; Chapter 1 § Code structure (`sec:intro-code`);
`outstanding_issues.md` A1.*
