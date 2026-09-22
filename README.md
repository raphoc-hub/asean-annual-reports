# ASEAN + US Annual Reports

A searchable filing index built during my investment-research internship at MBG Investment Management. The public site connects company search and market-level browsing to original filing documents.

[Current site](https://asean-filings.surge.sh/) · [Portfolio](https://raphoc-hub.github.io/#work)

## What is here

- Company search by name or ticker.
- Market pages for Indonesia, Malaysia, the Philippines, Singapore, Thailand, Vietnam and the United States.
- Company filing lists with source links, including annual reports, Form 10-K and Form 20-F records.
- A static HTML/CSS/JavaScript interface backed by JSON files; no application server or build step.

| File | Purpose |
| --- | --- |
| `index.html` | Search, market coverage and recent filings |
| `country.html` | Companies in a selected market |
| `company.html` | Filings for a selected company |
| `data/summary.json` | Snapshot totals and coverage metadata |
| `data/search.json` | Company search index |
| `data/country_*.json`, `data/reports_*.json` | Market and filing records |

## Preview locally

Requires Git and Python 3.

```sh
git clone https://github.com/raphoc-hub/asean-annual-reports.git
cd asean-annual-reports
python3 -m http.server 8000 --bind 127.0.0.1
```

Open <http://127.0.0.1:8000/>. Use HTTP rather than opening the HTML file directly: the interface fetches local JSON files. Stop the server with `Ctrl+C`.

## Status and provenance

This repository is a **July 2026 public snapshot**, not a mirror of the current deployment. Its [committed summary](data/summary.json) differs from the [current site's summary](https://asean-filings.surge.sh/data/summary.json); do not apply the current site's counts to this checkout.

The repository contains the frontend and exported index, not the upstream collection pipeline or internal research materials. Coverage varies by market, records can become stale, and external document links can change. Confirm a filing against its original source before relying on it. This is a research navigation tool, not investment advice.
