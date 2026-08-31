# bpholden.github.io

Personal site. Plain HTML and CSS — no build step, no Jekyll, no dependencies.

```
index.html      the whole page
style.css       all styling
images/         portrait + figures (SVG placeholders, replace with your own)
```

## Deploy

From a clone of the repo:

```bash
git clone https://github.com/bpholden/bpholden.github.io
cd bpholden.github.io
# copy index.html, style.css and images/ in here, replacing the old index.html
git add -A
git commit -m "New site"
git push origin main
```

Live at https://bpholden.github.io within a minute or two. Hard-refresh
(Cmd/Ctrl-Shift-R) if you see the old page — GitHub Pages caches aggressively.

To preview locally before pushing:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Things to edit

Every spot that needs your input is marked `<!-- EDIT -->` in `index.html`.
The short list:

1. **Affiliation line** and the one-sentence lede in the hero. The lede is the
   single most important sentence on the page — it's what a program committee
   or a prospective student reads first.
2. **Contact links** — email, ORCID, and the ADS search URL. The ADS link
   currently searches for `Holden, Bradford`; replace it with a link to your
   ADS library if you keep one, which will be cleaner.
3. **The three "What I work on" cards.** I wrote these from what your public
   repos suggest. Rewrite them in your own words.
4. **Images.** Drop three JPEGs or PNGs into `images/` and update the `src`
   attributes. Anything around 1200px wide is plenty; keep files under ~400 KB
   each so the page stays fast. Write real captions — a figure with a good
   caption does more than three paragraphs of prose.
5. **Repo descriptions.** Several of your repos have no description on GitHub;
   I guessed at those and marked them. Fixing them on GitHub itself is worth
   doing anyway — the description shows up in search.

## Adding a page

For a CV, teaching, or a full publication list, copy `index.html` to
`cv.html`, strip the body down, and link it from the hero nav. The stylesheet
already covers headings, links, and lists.
