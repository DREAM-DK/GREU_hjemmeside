# Parked: the Country teams directory

**Parked 3 November 2026, to bring the launch forward.** Nothing here is
wrong. It was removed because it is the one part of Applications that cannot
go public until four institutions agree to be named and to have their
calibration status described, and waiting for four clearances was holding up
everything else on the site.

This file is the whole record. Nothing was copied to a parallel folder,
because a duplicate of `applications.html` or `site.css` would drift away from
the live file within weeks and nobody would be able to tell which half of the
difference was deliberate. Everything removed is reproduced below, verbatim,
with the place it came from.

**What was *not* parked.** `content/pages/for-country-teams.md` is a different
object with a confusingly similar name: a page addressed *to* a modelling
team, explaining what they are calibrating. It names nobody's status, was
never built as a mockup, and stays in the plan as brief item 5.

---

## Before restoring

1. **Clearance.** Each institution named below must agree to be named and to
   have its calibration status described. The three country *projects* have
   approval requests in `content/approvals/`; this directory needs its own,
   and it covers different institutions — Austria, Finland and Italy are
   ministries, Belgium is the Federal Planning Bureau.
2. **Check the status lines are still true.** They describe calibration
   progress as of the March 2026 partner deck. Any of them could be a year
   stale by the time this comes back, and a wrong status is worse than none.
3. **Confirm the country list.** Chapter 1 names five TSI 2024 countries;
   the 2.0 files name four, after one institution withdrew. See
   `content/open-questions.md` item 7.
4. **Watch the source.** The status wording below is drawn from internal
   project material. `content/background-notes.md` records candid assessments
   of how each team is doing, including one team described as struggling with
   resource allocation. That kind of judgement never goes on the site.

---

## Removed from `mockups-graphic/applications.html`

It sat between the Projects grid and the closing `</div>` of the page wrap,
immediately after the six project cards.

```html
    <h2>Country teams</h2>
    <p class="measure">Each institution calibrates the model to its own accounts and energy balances. Status can be shown before any analysis is public. Internal notes stay off the site.</p>

    <div class="ccards">
      <div class="ccard">
        <img src="assets/mark.svg" alt="" width="44" height="44" />
        <div>
          <div class="nm">Federal Ministry of Finance</div>
          <div class="meta">Scripted data pipeline from public sources; calibration and internal workshops. No public analysis yet.</div>
        </div>
        <span class="pill">Austria</span>
      </div>
      <div class="ccard">
        <img src="assets/mark.svg" alt="" width="44" height="44" />
        <div>
          <div class="nm">Federal Planning Bureau</div>
          <div class="meta">Baseline calibration complete. Technology catalogues for the largest emitting sectors. No public analysis yet.</div>
        </div>
        <span class="pill">Belgium</span>
      </div>
      <div class="ccard">
        <img src="assets/mark.svg" alt="" width="44" height="44" />
        <div>
          <div class="nm">Ministry of Finance</div>
          <div class="meta">National data set and first calibration. Pilots on environmental taxation and transport fuels are planned, not yet listed as analyses.</div>
        </div>
        <span class="pill">Finland</span>
      </div>
      <div class="ccard">
        <img src="assets/mark.svg" alt="" width="44" height="44" />
        <div>
          <div class="nm">Department of Finance</div>
          <div class="meta">Harmonising national accounts with energy balances. Exploratory simulations are not yet public.</div>
        </div>
        <span class="pill">Italy</span>
      </div>
      <div class="ccard">
        <img src="assets/mark.svg" alt="" width="44" height="44" />
        <div>
          <div class="nm">Core model</div>
          <div class="meta">Danish benchmark data from Statistics Denmark. The calibration every country team starts from.</div>
        </div>
        <span class="pill">Reference</span>
      </div>
    </div>
    <p class="caption">The disc is never modified, never re-coloured and never has anything added to it. What a country, a version or a project needs to say is said in type beside it.</p>
```

The caption is worth keeping even if the directory never returns: it states
the rule about the disc, which the brand-lab boards also make. If the
directory does not come back, that sentence should find a home in
`mockups-graphic/README.md` instead.

## Removed from `mockups-graphic/assets/site.css`

It sat between the `.caption` rule and `.signup`.

```css
/* Country teams: the disc is never modified, never re-coloured and never has
   anything added to it. What a country needs to say is said in type beside
   it. Component from brand-lab/boards/05c-dream-heritage-applications.html. */

.ccards { display: grid; gap: 12px; }

.ccard {
  display: flex;
  align-items: center;
  gap: 15px;
  border: 1px solid var(--line);
  background: var(--surface);
  padding: 14px 18px;
}

.ccard img { display: block; flex: none; }
.ccard .nm { font-size: 16px; font-weight: 600; }
.ccard .meta { font-size: 13.5px; color: var(--ink-soft); margin-top: 1px; max-width: 68ch; }

.ccard .pill {
  margin-left: auto;
  background: var(--green-tint);
  color: var(--green);
  border-radius: 20px;
  padding: 4px 14px;
  font-size: 13px;
  font-weight: 600;
  white-space: nowrap;
}
```

And from the 760 px breakpoint, where it was the last pair of rules:

```css
  .ccard { flex-wrap: wrap; }
  .ccard .pill { margin-left: 0; }
```

The component itself is not lost: it is still drawn in
`brand-lab/boards/05c-dream-heritage-applications.html`, under the heading
"Country teams, without touching the mark", with its own copy of the CSS.
That board is a design record and was left alone.

## Removed from the content layer

From `content/pages/applications.md`, the third row of the object table:

```
| **Country team** | Who is calibrating, and how far have they got? | `/applications/countries/…` |
```

and the section:

```
## Country teams

Austria, Belgium, Finland, Italy (2.0 partners). Status of calibration can be
shown before any analysis is public. Public analyses by that institution are
listed on the team page and in the library. No implied results.
```

From `content/sitemap.md`, the row:

```
| Country team | `/applications/countries/…` | Institution and calibration status; public analyses only. |
```

and the line:

```
**Country teams** answer: who is calibrating, and how far have they got.
```

## Wording changed elsewhere

These pages referred to the directory in passing. The phrases were reworded
rather than deleted, so restoring means putting the third object back into a
list of two, not hunting for gaps.

| File | Was |
| --- | --- |
| `mockups-graphic/applications.html` | Page lead: "Projects explain who funded the work. Country teams explain who is calibrating the model." |
| `mockups-graphic/index.html` | "See analyses, projects and country teams →" |
| `mockups-graphic/sitemap.html` | "a hub holding three kinds of object: analyses, projects and country teams"; the Country teams outline item; the notes paragraph; the `Country teams` node in the diagram data; the closing paragraph |
| `mockups-graphic/analysis-tsi-paper.html` | Table row: `<tr><th>Country team</th><td>None. Core-model paper.</td></tr>` |
| `mockups-graphic/project-version-2-0.html` | "Analyses by the country teams are listed under Applications" |
| `content/pages/project-version-2-0.md` | "country teams are listed under Analyses when the institution publishes them" |
| `mockups-graphic/README.md` | The Country teams component note and the green country pill note |

`mockups-graphic/news.html` uses the phrase "a country team" generically, of
any national modelling team bringing in its own technology costs. That is
ordinary English rather than a reference to the directory, so it was left as
it is.
