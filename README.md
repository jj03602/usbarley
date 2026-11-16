# U.S. Barley Export Competitiveness — project website and dashboard

Project website for the University of Idaho study on the global competitiveness of U.S. barley, supported by the
Idaho Barley Commission. It introduces the project, summarizes key findings, and links to the interactive R Shiny
dashboard, which shows how supply-side factors (production and transportation costs) and demand-side factors
(who buys barley and why), along with tariffs, shape U.S. and competitors' barley exports.

- Dashboard: https://jung-keon.shinyapps.io/usbarley/
- Website: https://<your-username>.github.io/<repo>/ (after GitHub Pages is turned on)

## Folder layout
```
index.html                     the website (HTML, CSS and a few lines of JavaScript, no build step)
assets/ibc-logo.png            Idaho Barley Commission logo (footer)
assets/dashboard-overview.png  screenshot of the dashboard Overview page (hero image)
assets/dashboard-outlook.png   screenshot of the Outlook to 2035 page (scenario tools section)
.nojekyll                      tells GitHub Pages to serve the files as they are
README.md                      this file
```

## Dashboard pages
- Overview: the U.S. in the world barley market; who exports barley and where U.S. barley and malt go.
- Supply: cost to grow (U.S. vs. Canada, Australia, the EU, Argentina and Ukraine), who grows and who sells
  (major producers that export little), cost to move (rail and ocean freight), and how exports leave the country.
- Demand: U.S. demand, the large importers and what they use barley for, and beer and malting.
- Outlook to 2035: a scenario builder for income growth, drinking habits, age structure, urban share,
  Mexico's beer exports and barley per tonne of beer; what moves demand; and how reliable the projection is.
- Tariffs: what U.S. barley and malt pay vs. the lowest-tariff main competitor in each market; a tariff scenario
  under a moderate or strong buyer response; and the evidence from China's duties on Australian barley.
- About the data: definitions, sources and the full indicator list.

## Key findings shown on the website
| Topic           | Finding                                                                      |
|-----------------|------------------------------------------------------------------------------|
| Market position | U.S. supplies about 0.5% of world barley grain exports                       |
| Main customer   | 82% of U.S. barley and malt export value goes to Mexico, mostly as malt      |
| Cost to grow    | U.S. operating cost about $129/t (2020-2024), same as Argentina              |
| Outlook to 2035 | World barley for brewing rises from 29.9 to 33.3 Mt                          |
| Tariff risk     | A 10-point Mexican tariff on U.S. malt would cost $17-108M a year            |
| New markets     | Sub-Saharan Africa imports about $626M of malt a year, mostly from Europe    |

To change a number, edit the "Key findings" section of `index.html`.

## Run it locally
Open `index.html` in a browser; nothing needs to be installed.

## Publish it
1. Push the folder's contents to the repository's root (keep the `assets` folder):
   ```
   git init
   git add .
   git commit -m "Project website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo>.git
   git push -u origin main
   ```
2. In the repository, go to Settings > Pages > Build and deployment, choose "Deploy from a branch",
   branch `main`, folder `/ (root)`, and save.
3. After a minute the site is live at `https://<your-username>.github.io/<repo>/`.

## Update it
- Screenshots: replace the PNGs in `assets/` with new ones of the same name (about 1600 px wide).
- Dashboard link: the address appears in `index.html` several times; search for `shinyapps.io` to change it.
- The live dashboard loads on the page only when a visitor clicks "Load the dashboard here", so page views
  do not use shinyapps.io active hours.
- The dashboard itself (R code and data) is maintained separately in `barley_dashboard/` and deployed to
  shinyapps.io with `rsconnect::deployApp("app", appName = "usbarley")`.

## Project team
Xiaoli Etienne, Patrick Hatzenbuehler, Andres Trujillo-Barrera and Jung-Keon Jo,
Department of Agricultural Economics and Rural Sociology, University of Idaho.

## Funding
This project is supported by the Idaho Barley Commission.

## Data sources
USDA (FAS PSD, ERS, AMS), FAOSTAT, UN Comtrade, U.S. Census Bureau, WITS (UNCTAD TRAINS), IMF and World Bank.
