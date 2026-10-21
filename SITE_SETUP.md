# Publish Ping Wang's academic website

This repository is configured for the al-folio Jekyll theme and the GitHub Pages address https://pwangcs.github.io.

## Before publishing

1. Review the homepage, publication list, research topics, and CV data.
2. The public CV PDF has been replaced with the phone-number-free version supplied in the workspace as `Ping_CV.pdf`.
   The website uses `assets/pdf/Ping_Wang_CV.pdf` as the public download. The template's automatic RenderCV PDF workflow has been removed so it cannot overwrite that file.
3. Create a GitHub repository named pwangcs.github.io under the GitHub account pwangcs. Leave the new repository empty; do not initialize it with a README or license.

## Push the site

Run these commands in this project directory after the repository has been created:

    git remote add origin https://github.com/pwangcs/pwangcs.github.io.git
    git add .
    git status --short
    git commit -m "Set up personal academic website"
    git branch -M main
    git push -u origin main

The included .github/workflows/deploy.yml builds the Jekyll site and publishes the generated _site directory to the gh-pages branch after a push to main.

## Enable GitHub Pages

In the repository on GitHub, open Settings → Pages and choose Deploy from a branch, then select gh-pages and / (root). Check the Actions tab for the first build. When the deployment succeeds, the site should be available at https://pwangcs.github.io.

## Updating content

- Edit the biography in _pages/about.md.
- Add or update publications in _bibliography/papers.bib.
- Edit research areas in _pages/research.md.
- Edit the structured CV in _data/cv.yml and the downloadable PDF in assets/pdf/Ping_Wang_CV.pdf.
- Add news posts in _news/.

The project is based on https://github.com/alshedivat/al-folio. Local Jekyll build verification requires Ruby and Bundler; these are not installed in the current Windows environment, so the GitHub Actions build will be the first full Jekyll build unless Ruby is installed locally.
