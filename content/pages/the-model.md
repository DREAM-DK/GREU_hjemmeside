# The model

**Nav title:** The model  
**Path:** `/the-model`

## Purpose

Member States need to assess the macro-fiscal implications of the transition
to climate neutrality by 2050. That requirement is now part of EU economic
governance, including the revised national budgetary frameworks.

GreenREFORM-EU is a standardised dynamic CGE framework for those assessments.
It is meant to score real climate policies — carbon prices, technology
subsidies, renewable energy mandates, capital investment — and to return
economy-wide feedback on GDP, employment, wages, trade and fiscal accounts.

*Source: Chapter 1 § Background (`sec:intro-background`).*

## What is distinctive

Bottom-up energy models usually make discrete technology choices. Top-down CGE
models usually substitute inside a production function. The two do not readily
align.

The common workaround is soft-linking: solve the models apart and pass results
until they agree. GreenREFORM-EU rejects that for this model. The energy
technology model uses a continuous approximation of discrete choice and solves
in the same system as the macro core. Soft-linking is the alternative, not a
feature. A standardised interface to external energy-system models is proposed
work for a later project, not a property of GreenREFORM-EU 2.0.

Agents are forward-looking. Firms and households can anticipate future carbon
taxes and technology costs, including anticipatory investment in abatement
capital.

*Source: Chapter 1 § Core technical challenge (`sec:intro-challenge`);
foreword (feature 4 of TSI 2026 is not claimed).*

## What this page does not claim

The model is not a GAMS tutorial. Industry detail comes from the data set a
country calibrates to; 57 industries is the Danish benchmark, not a universal
count. Housing on the household side is a purchase of housing services, not a
household dwelling stock.

*Source: Chapter 1 § The model economy; Chapter 2 § Housing.*
