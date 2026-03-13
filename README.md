# CocoaBoard — R Shiny Dashboard

An R/Shiny implementation of the Chocolate Sales Dashboard, ported from the Python visualization project [DSCI-532_2026_8_cocoaboard](https://github.com/UBC-MDS/DSCI-532_2026_8_cocoaboard).


## Features

- **Filters:** Date range, Country (multi-select), Product (multi-select)
- **KPI cards:** Total Revenue, Total Boxes Shipped, Active Sales Reps, Avg Revenue per Transaction, YoY Revenue, MoM Revenue (with loading spinners)
- **Revenue by Product:** Interactive pie chart (responds to all active filters)
- **Leaderboard table:** Rank, Revenue, Transactions, Boxes Shipped, Avg Deal Size, Revenue Share — includes a summary row
- **Revenue trend:** Monthly line chart tracking the top 5 sales reps over time

## Deployed App

- **Stable (main):** https://019ce94c-207a-9c7d-800f-83e5fe970e41.share.connect.posit.cloud

## Dataset

The dashboard uses the **Chocolate Sales** dataset from Kaggle:

- **Source:** [Chocolate Sales | Kaggle](https://www.kaggle.com/datasets/saidaminsaidaxmadov/chocolate-sales)

## Run locally

```r
# Install dependencies (once)
install.packages(c("shiny", "bslib", "ggplot2", "dplyr", "tidyr", "plotly", "DT", "lubridate", "bsicons", "scales", "shinycssloaders"))

# From project root (cocoaboard-visualisation-R/)
shiny::runApp()
```

Or in RStudio: open `cocoaboard.Rproj`, then run the app (e.g. Run App on `app.R`).

## Deploy to Posit Connect Cloud

Connect Cloud needs a **generated** `manifest.json` (from `rsconnect::writeManifest()`)
