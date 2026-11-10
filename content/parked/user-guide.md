# Parked: the user guide page

**Decided 10 November 2026.** The user guide will not be ready when the site
launches. It will be added later. The User guide page stays in the navigation
as a holding page, so no link or menu has to change when the guide arrives.

The full page as it was before is kept in `content/parked/user-guide/user-guide.html`.

## To restore: what to ask

When the guide is ready, ask the agent:

> The user guide is ready: [file or link]. Put it on the website, following
> `content/parked/user-guide.md`.

## Instructions for the agent

1. **Read first.** Read this file and `AGENTS.md`. Live files may have changed
   since 10 November 2026; do not assume they match the **Now** text below.
2. **User guide page (`mockups-graphic/user-guide.html`).** Take the main
   content from the parked copy, but keep the live masthead, navigation,
   sign-up band and footer. Point "Download the guide" at the real file or
   link (it was `href="#"`). Check the six-item "What it covers" list against
   the guide's actual chapters. Change the sign-up heading back to "Get told
   when the guide is updated" if that still fits.
3. **Put back the edits below.** Replace the **Now** text with the **Was**
   text, or the equivalent if a file was edited since.
4. **News.** Add a dated item announcing the guide.
5. **Version 2.0.** If the guide is published as a Version 2.0 output, update
   the "User guide" and "Publication" lines and the Record on both the HTML
   and md pages.
6. **Search** `mockups-graphic/*.html` and `content/pages/*.md` for "will
   follow", "follows later", "holding page" and "Coming later" to catch
   anything missed.
7. **Render** `user-guide.html` and `index.html` with headless Chrome and look.
8. Delete this file and `content/parked/user-guide/` last, and report.

## Edits to live files

| File | Was | Now |
| --- | --- | --- |
| `index.html`, hero | Three buttons, the third `<a class="btn-ghost" href="user-guide.html">User guide</a>` | Two buttons |
| `news.html`, October 2026 item | "The model code, the theoretical documentation and the user guide are now available from the repository." | "The model code is now available from the repository, and the theoretical documentation as a PDF from this website. A user guide will follow." |
| `get-the-model.html`, lead | "The model code, the documentation and the user guide are published openly. You do not need an agreement with DREAM to read, run or adapt them." | "The model code is published openly. You do not need an agreement with DREAM to read, run or adapt it. The documentation is free to download as a PDF, and a user guide will follow." (Since 10 November 2026 the openness claim covers the code only; keep it that way on restore.) |
| `get-the-model.html` | "The theoretical documentation and the user guide are in the same repository, in LaTeX source and as published PDFs." | "The theoretical documentation is published as a PDF on the Documentation page. The user guide will be added when it is published." (The LaTeX source is not published, decided 10 November 2026; do not restore that wording.) |
| `get-the-model.html` | "Start from Chapter 1 of the documentation, then the user guide." | "Start from Chapter 1 of the documentation. A user guide will follow." |
| `applications.html`, Version 2.0 card | "wrote the documentation and the user guide" | "wrote the documentation" |
| `analysis-tsi-paper.html` | "start from the user guide." | "start from the documentation. A user guide with worked runs will follow." |
| `accessibility.html` | "the model documentation, the user guide and the published papers." | "the model documentation and the published papers, and the user guide when it is published." |
| `project-version-2-0.html` | "Being written. It will be published with version 2.0." / "with the documentation and the user guide, together with this website." | "Being written. It will be published after this website goes live." / "with the documentation, together with this website. The user guide follows later." |
| `project-version-2-0.md` | Outputs row with "a user guide"; "Written and published with version 2.0."; Publication "with the documentation and the user guide" | "A user guide follows later."; "Not published at the launch of this website. It will be added later."; Publication without the guide |
| `sitemap.html` | "install, calibrate, run a shock." / `s: 'Install, calibrate, run a shock'` | Adds "A holding page at launch; the guide is added later." / `s: 'Holding page at launch'` |
| `content/sitemap.md` | "Forthcoming until the 2.0 guide exists." | "A holding page at launch (decided 10 November 2026) …" |
| `content/pages/applications.md` | "Point to the user guide for how to" | "Point to the user guide, once it is published, for how to" |
