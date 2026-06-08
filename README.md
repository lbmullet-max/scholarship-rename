# EMU Honors Scholarship Rename Proposal

An interactive, on-brand web version of the proposal to rename the Yoder/Webb Scholarship
as the EMU Honors Scholarship. Built as a single self-contained `index.html` (the EMU logo
and ridge graphic are embedded, so there are no extra image files to manage).

## Publish on GitHub Pages

1. Create a repository (public, or private if you have Pages on your plan) and add `index.html`
   to the root.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose your
   default branch (e.g. `main`) and the `/ (root)` folder, then **Save**.
4. Wait about a minute. Your site goes live at
   `https://<your-username>.github.io/<your-repo>/`.

## Wire up the "Discuss" buttons

The Discuss section links to GitHub so your team can comment in one place.

1. Open `index.html` and find the config block near the bottom of the `<script>`:
   ```js
   const REPO = "your-org/your-repo";
   ```
2. Replace it with your repo, for example `emu-admissions/honors-proposal`, and commit.
3. **Open a discussion** now points to GitHub Discussions (enable it under
   **Settings → General → Features → Discussions**), and **Raise a question** opens a
   prefilled GitHub Issue.

Until you set `REPO`, the buttons show a short reminder instead of going to a broken link.

### Optional: inline threaded comments

If you want comments to appear directly on the page rather than over on GitHub, add
[giscus](https://giscus.app) (it stores comments in your repo's Discussions). Configure it on
giscus.app, then paste the `<script>` snippet into the Discuss section of `index.html`.

## Editing the content

All the text lives directly in `index.html` between the `<main>` tags, in plain HTML
sections (`#ask`, `#today`, `#why`, `#peers`, `#timeline`, `#heritage`, `#discuss`). Edit the
copy in place and commit; Pages redeploys automatically.

## Notes

- This is marked **Draft for internal review**.
- Before the heritage statement publishes anywhere outward-facing, confirm with University
  Archives whether Ada and Peggy Webb were related and the exact wording of Ada's
  "one of the first" distinction.
- The peer-comparison source links point to each institution's current financial-aid page;
  worth a quick re-check before this goes in front of leadership, since aid pages change.
