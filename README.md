# Ping Wang — Academic Website

Personal academic website of Ping Wang, a researcher in computational imaging and machine vision at Westlake University.

**Website:** <https://pwangcs.github.io>

The site is built with [al-folio](https://github.com/alshedivat/al-folio), Jekyll, and GitHub Pages. It includes a research overview, publications, news, and a downloadable public CV.

## Local development

Requirements: Ruby and Bundler, Node.js, and Python.

```bash
bundle install
npm ci
bundle exec jekyll serve
```

Open <http://localhost:4000> to preview the site.

## Updating content

- Biography: `_pages/about.md`
- Research areas: `_pages/research.md`
- Publications: `_bibliography/papers.bib`
- CV details: `_data/cv.yml`
- Public CV PDF: `assets/pdf/Ping_Wang_CV.pdf`
- News: `_pages/news.md` and `_news/`

## Deployment

The GitHub Actions workflow in `.github/workflows/deploy.yml` builds the site on pushes to `main` and publishes the generated `_site` to the `gh-pages` branch. In repository **Settings → Pages**, select **Deploy from a branch**, branch `gh-pages`, folder `/ (root)`. The first successful build creates the branch.

The repository retains the al-folio MIT license and attribution.
