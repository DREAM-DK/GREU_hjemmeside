# GreenREFORM-EU 2.0 website

Public front door for **GreenREFORM-EU 2.0**: the model, who it is for, how it
works at a high level, and a way into the technical documentation.

The LaTeX document remains the source of truth for mechanisms, equations, and
code names. This workspace holds the sitemap and page copy. Implementation and
visual design come later.

Publisher: [DREAM](https://dreamgruppen.dk/), Danish Research Institute for
Economic Analysis and Modelling.

## Open the workspace

Open `greenreform-eu-website.code-workspace` in Cursor (File → Open Workspace
from File). That mounts:

1. **Website** — this folder (write here)
2. **Documentation (FinalVersion)** — live `_EN` chapters. The published PDF,
   `content/Documentation/greu_master_merged_v4_EN.pdf`, is in this folder and
   is preferred for reading
3. **Background material** — project PDFs and lineage, not code

Treat the last two roots as read-only. Do not add site files there.

## Layout

```text
WEBSITE_BRIEF.md          # original brief
AGENTS.md                 # writing and source rules
ACCESSIBILITY.md          # WCAG 2.1 AA audit and what DREAM must decide
DESIGN_PHILOSOPHY.md      # the position: carry information or be removed
DESIGN_PHILOSOPHY_DA.md   # same, in Danish and shorter
DESIGN_RATIONALE.md       # how much graphic the site should carry, with evidence
content/sitemap.md        # pages, nav, Home vs Documentation
content/pages/            # draft copy (1–3 short paragraphs each)
content/open-questions.md # items for DREAM
brand-lab/                # five visual directions; 05 is the one implemented
mockups-graphic/          # clickable pages with the connected-discs graphic
```

## Current task

Information architecture and page copy. Not a live site. Not a GAMS tutorial.

Optional later, not now: download, Git, run instructions, country pages.
