# Home

**Nav title:** Home  
**Path:** `/`

## Headline and lead

> Score climate policy for emissions and macro-fiscal impact in the same model

> GreenREFORM-EU is a dynamic computable general equilibrium model designed to
> meet the needs of finance ministries, planning bureaus and emissions agencies
> alike. It scores carbon prices, technology subsidies, mandates and green
> investment for their effect on emissions, and for the macro-fiscal
> consequences.

"Designed to meet the needs of ... alike" is a claim about the model, not a
statement of audience. Chapter 1 § Background carries it: the legal
requirements "demand that Ministries of Finance and other institutions move
beyond static or fragmented modelling approaches", and the tools they need
"must be able to simultaneously capture economy-wide feedback on GDP,
employment, wages, trade, and fiscal balance sheets".

The stronger claim — that several institutions share the model as a common
platform — stays off this page. In Denmark that is real and has a decade
behind it, and it belongs on About as history. For GreenREFORM-EU the TSI
partners are one institution per country, so the claim would be an aspiration
written in the present tense.

Scored **for** emissions, not delivering them: a policy can raise emissions as
well as cut them, and the model is neutral on the direction. The construction
is the Foreword's own — a policy "scored for its effect on emissions and on
output, employment, investment and the public finances at the same time".

**Macro-fiscal** means the economy and the public finances taken together. It
is the documentation's own word: Chapter 1 § Background says the transition
"requires Member States to assess the macro-fiscal implications of green
transition policies", and that the project lets policymakers work "within a
unified macro-fiscal environment". It is the Commission's too — DG ECFIN uses
it of climate assessment, and DG REFORM's TSI flagship *Economic Analysis for
Climate Action* is about capacity to assess "the macro-fiscal implications of
climate change and climate policies". The site cites neither: a reader who
wants the provenance can find it.

The lead does not gloss the term. An earlier draft spelled it out — "output,
employment, wages and trade on one side, tax revenue, spending and debt on the
other" — but the next section, "What makes it different", already says a
policy is scored for emissions and for output, employment, investment and the
public finances at once. The gloss was read twice in two hundred words.

The headline frames the model as being about climate policy. The macroeconomic
core also runs without the climate block, which is a point to raise later in
the page rather than in the hero.

*Source: `greu_frontmatter_v5_EN.tex`, Foreword; Chapter 1 § Combining and
overriding modules (`greu_chapter01_merged_v9_EN.tex`).*

## Built for ministry work: the third card

The card used to be "Honest limits / What it does not do", and read as a list
of absences. It is now:

> **Your economy** — What you set
>
> The core carries no country-specific rules. The exchange rate regime,
> whether funding binds, and how wages respond to demand are set for the
> economy you are modelling. The results turn on those choices.

The source is DREAM's own GMMI Paris deck (Jens Sand Kirk, 27 October 2026),
not the `_EN` chapters. Slide 5 labels the Danish setup "this closure is
specific to Denmark": fixed to the euro, capital flowing freely, funding not
rationed. Slide 7 makes three axes govern the result — interest-rate
pressure, wage pressure, exchange rate. Slide 8 closes with "a different
exchange rate, or tighter supply of investment goods, gives a different
answer". Slide 11 describes the EU model as "the same core, with simplified
parameter assumptions and no country-specific rules. A country calibrates it
to its own data."

The card does **not** claim the model solves a floating exchange rate or a
credit-rationing regime. The axes are what differs between economies and what
the user has to settle; whether each is a solved mechanism or an assumption
is a question for the documentation, not the homepage.

The non-features the card used to carry are off the homepage. They briefly sat
in the "In brief" panel and were taken out: the home page is a front door, and
a list of absences is not what a first-time ministry reader needs from it.

They are not dropped from the site. The TSI paper page states them in its
scope note — "No monetary policy. Government is an accounting closure, not an
optimiser" — which is where a reader meets a concrete result and needs to know
what stands behind it. `content/pages/how-it-is-organised.md` carries the full
set for the page that explains the agents. Both are needed, because the
workspace rules forbid describing these features as available, and silence on
a technical page would read as a promise.

Nothing else from that folder is usable here: the TSI 2026 programme and its
country count, the Julia version, the standardised soft-link interfaces, and
the Viet Nam, Faroese, Belgian and Finnish spin-offs are all either barred by
the site rules or marked in the working notes as not cleared to describe.

## What it is

GreenREFORM-EU is a dynamic general equilibrium model for fiscal and
environmental policy analysis. DREAM (Danish Research Institute for Economic
Analysis and Modelling) builds and maintains it. GreenREFORM-EU 2.0 is the
edition documented here.

It is a multi-sectoral computable general equilibrium model of a small open
economy. It integrates the economic national accounts with physical energy
balances and greenhouse gas emissions.

*Source: `greu_frontmatter_v5_EN.tex`, Foreword.*

## Who it is for

The primary readers are finance ministries, planning bureaus and emissions
agencies of EU Member States (TSI users). DREAM staff, country modelling teams
and technically literate policy analysts are the secondary audience.

The site is a front door. It should get a ministry reader to: what the model
is, what it can score, what it cannot, and which chapter matches their
question.

*Source: `WEBSITE_BRIEF.md`; Chapter 1 § Background (`sec:intro-background`).*

## Distinctive feature

Fuel switching, electrification and carbon capture are discrete choices in
reality. GreenREFORM-EU represents them continuously. Capital intensity is
assumed to follow a log-normal distribution across the firms of an industry,
so a representative firm adopts competing technologies along a merit-order
curve as relative prices move.

That energy technology model is hard-linked to the macroeconomic core: the
technology equations enter the same system and are solved with it. A
technology-specific policy can then be scored for emissions and for output,
employment, investment and the public finances at the same time.

In DREAM project reports the same object is sometimes called the abatement
model. The code, and this site, use energy technology model.

*Source: Foreword; Chapter 1 § Core technical challenge (`sec:intro-challenge`);
Status (naming).*

## Modularity

Text and code are built as modules. A module can be understood in partial
equilibrium, combined with others, or assembled into the full general
equilibrium model, as long as it keeps the objects it takes in and the objects
it sends out.

*Source: Foreword, modularity paragraph.*

## Next

- [The model](the-model.md) — purpose and what it can score  
- [Documentation](documentation.md) — chapters and how to read them  
- [About](about.md) — DREAM, lineage, rights
