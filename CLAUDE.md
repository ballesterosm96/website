# mariaballesteros.com

Personal academic website for María Ballesteros. Single-page static site, no build step, no dependencies.

## Structure
- `index.html` — the entire site (content + CSS in one file). Sections: hero, #latest, #research, #teaching, #contact.
- `files/` — public PDFs. Currently only `Ballesteros_CV.pdf`.
- `CNAME` — custom domain for GitHub Pages (mariaballesteros.com). Do not delete.
- `.nojekyll` — tells GitHub Pages to serve files as-is.

## Rules
- NEVER copy or link Maria's Dropbox/local paper files here without her explicit approval. Working papers say "Draft available upon request" (mailto link). Published work links to the official online version (SSRN, journal site).
- Dissertation papers 1 and 2 (Displacement as State-Building; Ripe for Entry) are request-only. Paper 3 (Territorial Control in Civil Wars) links to SSRN: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4912415
- No em dashes in site copy (Maria's writing style rule).
- Keep the design system: warm paper background, Fraunces display font, Source Serif 4 body, terracotta accent (#8C3B2E). Status badges: pub (green), rr (amber), wp (purple), prog (gray).

## Common updates
- New paper: copy an `<article class="paper">` block inside the right `.theme` div in #research.
- News item: edit the three `.card` blocks in #latest (keep newest first, drop the oldest).
- New CV: overwrite `files/Ballesteros_CV.pdf` with the latest NO-REFERENCES export from
  `~/Dropbox/Harvard/Job Market Materials/Ballesteros_CV_Jul2026_NoReferences.pdf` (or successor).
  The website always uses the no-references version.

## Deploy
Hosted on GitHub Pages from this repo (branch: main, root). After any change:
```
git add -A && git commit -m "update" && git push
```
The site rebuilds automatically in about a minute. DNS for mariaballesteros.com is managed in Squarespace (A records to GitHub Pages IPs, www CNAME to the GitHub Pages hostname).

## Preview locally
Open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit http://localhost:8000.
