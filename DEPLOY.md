# Deploying the Bookfania site to GitHub Pages

1. Unzip `readigo-site.zip` into the root of the Readigo repo. It adds `site/` and `.github/workflows/pages.yml` (existing `checks.yml` is untouched).
2. Commit and push to `main`:
   ```sh
   git add site .github/workflows/pages.yml
   git commit -m "Add Bookfania landing page"
   git push origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
4. The "Deploy site to GitHub Pages" workflow runs on pushes to `main` that touch `site/` (or run it manually from the Actions tab). Site URL:
   **https://elysiahuang.github.io/Readigo/**

Alternative: instead of Actions, push the *contents* of `site/` to a `gh-pages` branch and set Source to "Deploy from a branch → gh-pages / (root)".

Before publishing to stores: replace the "Coming soon" buttons (TODO comments in `site/index.html`) and the placeholder `site/privacy.html`. If the repo or owner name changes, update the absolute `og:image`/`og:url` meta tags.
