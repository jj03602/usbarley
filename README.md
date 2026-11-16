# U.S. Barley Competitiveness — project website

Landing page for the University of Idaho project on the global competitiveness of U.S. barley, supported by the Idaho Barley Commission. It introduces the project, lists key findings, describes the dashboard pages, and loads the live R Shiny dashboard (https://jung-keon.shinyapps.io/usbarley/) on request.

## Files

```
index.html                    the whole page (HTML, CSS and a few lines of JavaScript)
assets/ibc-logo.png           Idaho Barley Commission logo (footer)
assets/dashboard-overview.png screenshot of the dashboard Overview page
assets/dashboard-outlook.png  screenshot of the Outlook to 2035 page
.nojekyll                     tells GitHub Pages to serve the files as they are
```

## Publish with GitHub Pages

1. Create a repository on GitHub, e.g. `usbarley`.
2. Upload the contents of this folder to the repository's root (keep the `assets` folder). From a terminal:
   ```
   git init
   git add .
   git commit -m "Project website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/usbarley.git
   git push -u origin main
   ```
3. In the repository, go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. After a minute the site is live at `https://<your-username>.github.io/usbarley/`.

## Updating

- Text and findings: edit `index.html` (the numbers are in the "Key findings" section).
- Screenshots: replace the PNGs in `assets/` with new ones of the same name (about 1600 px wide).
- The live dashboard loads only when a visitor clicks "Load the dashboard here", so page views don't use shinyapps.io active hours.
