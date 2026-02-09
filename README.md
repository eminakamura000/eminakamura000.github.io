# Website Update Guide

This guide explains the basic workflow for updating the website.

## What You Need

- A standard computer with a Terminal or Command Prompt app.
- A code editor ([VS Code](https://code.visualstudio.com/) or similar).
- [Git](https://git-scm.com/) and [Hugo](https://gohugo.io/) installed.
- [GitHub Desktop](https://desktop.github.com/).

## Where Things Live

- Main website text/content: `content/`
  - Bio: `content/home.md`.
  - Research: `content/research.html`.
  - Teaching: `content/teaching.html`.
- PDFs, replication packages, and downloadable files: `static/` (usually `static/papers/`)
- Sidebar settings (name, short bio, profile photo): `config.toml`

Do not manually edit `public/` (it is generated automatically).

## Standard Workflow (Every Update)

1. Navigate to the GitHub folder in your terminal: `/GitHub/eminakamura000.github.io`.
2. Make your content/file edits.
3. Preview locally:
   - Open Terminal
   - Run:
     ```bash
     cd .../GitHub/eminakamura.github.io
     hugo serve
     ```
   - Open the provided localhost link in your browser.
   - Verify that the changes look correct.
4. Stop the preview server with `Control + C` in Terminal.
5. Open GitHub Desktop.
6. (Recommended) Review the changed files.
7. Write a clear commit message (example: `Add working paper on ...`).
8. Click **Commit to main**.
9. Click **Push origin**.

### How To Add a New Paper

1. Add the paper PDF (and any replication `.zip` or data files) to `static/papers/`. If a `.zip` file is larger than 100 mb, you will not be able to push it onto GitHub. In that case, upload the file to Google Drive and add a link to it in the research section. 
2. Open: `content/research.html`
3. Add the paper entry in HTML format (matching the existing formatting and section order).
4. Save the file.
5. Preview with `hugo serve`.
6. If it looks good, commit and push from GitHub Desktop.

### Other Common Edits

- Edit an existing paper: update its entry in `content/research.html`.
- Reorder papers: move entries up/down within `content/research.html`.
- Edit bio/contact text: update `content/home.md` using [markdown syntax](https://www.markdownguide.org/basic-syntax/).
- Update sidebar title/short bio/photo filename: edit `config.toml`.

## Quick Checklist Before Pushing

- Site preview looks correct with `hugo serve`.
- New links open correctly.
- PDF/ZIP paths start with `/papers/...` if stored in `static/papers/`.
- No accidental changes to unrelated files.
