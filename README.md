# Disaster Management Analytics Dashboard | Power BI

An interactive Microsoft Power BI report designed to explore disaster patterns, geographic distribution, emergency-response performance, priority classification, and recovery impact.

> **Repository status:** This repository includes the original Power BI report, extracted report-definition metadata, and inventories of pages, visuals, and field/measure references. The data model is embedded in the `.pbix` file, but a verified flat-file dataset export, complete model schema, relationships, Power Query transformations, and DAX expressions have **not** yet been extracted. The descriptions below are based on the report structure and references found in the file; they should not be treated as independently verified calculations or findings.

## Dashboard pages

The report contains five pages. The report canvas for each page is 1920 × 1080.

### 1. Executive Overview
A high-level summary of disaster activity and impact, with visuals referencing:
- Total disasters over time
- Disaster counts by type and country
- Total casualties and economic loss
- Total aid and average response efficiency

### 2. Global Disaster Distribution
A geographic view for exploring disaster locations and patterns. The map references fields including country, disaster type, severity, casualties, economic loss, response time, response-efficiency score, latitude, and longitude.

### 3. Emergency Response
A view of response performance and aid, with visuals referencing:
- Average response time and response efficiency
- Response-time trends over time and by disaster type
- Average recovery days
- Total aid
- Economic loss and aid comparisons

### 4. Smart Priority
A view of disaster priority categories and severity indicators, with visuals referencing:
- Disaster counts by priority category
- Average priority score
- Critical and high-priority disaster counts
- Relationships among disaster type, severity, casualties, and economic loss

### 5. Recovery and Impact
A view of recovery duration and disaster impact, with visuals referencing:
- Average recovery days over time
- Economic loss and recovery days by disaster type
- Casualties, aid amounts, and economic loss

**Note:** These are descriptions of the report visuals and their referenced fields/measures, not claims about specific results. Values and calculations should be verified in Power BI before presenting conclusions.

## Key report references

The report references a table/entity named `Disasters` and the following fields in its visual definitions:

- **Date and geography:** `date`, `country`, `latitude`, `longitude`
- **Disaster characteristics:** `disaster_type`, `severity_index`, `Priority Category`
- **Impact:** `casualties`, `economic_loss_usd`
- **Response and aid:** `response_time_hours`, `response_efficiency_score`, `aid_amount_usd`

Measure names referenced by visuals include:

- `Total Disasters`
- `Total Casualties`
- `Total Economic Loss`
- `Total Aid`
- `Average Response Efficiency`
- `Average Response Time`
- `Average Recovery Days`
- `Average Priority Score`
- `Critical Disasters`
- `High Priority Disasters`

These names were identified from report definitions. The actual DAX expressions and complete model schema have not yet been recovered, so the calculation logic is not documented here as verified fact.

## Technology and tools

- **Microsoft Power BI Desktop** — report authoring and interactive dashboard
- **Power BI report-definition JSON** — extracted page and visual metadata
- **CSV** — inventories of pages, visuals, fields, and PBIX contents
- **DAX Studio / Tabular Editor** — potential tools for inspecting the semantic model and measure definitions (not required just to view the report)

## Repository structure

```text
.
├── powerbi/
│   ├── original/
│   │   └── Disaster_Management_Dashboard.pbix
│   └── report-definition/
│       ├── report.json
│       └── version.json
├── metadata/
│   ├── pages.json
│   ├── visual_inventory.csv
│   ├── field_inventory.csv
│   └── pbix_contents.csv
├── documentation/
│   └── EXTRACTION_NOTES.md
├── .gitignore
└── README.md
```

## Open the Power BI report

1. Install and open Microsoft Power BI Desktop.
2. Open `powerbi/original/Disaster_Management_Dashboard.pbix`.
3. If Power BI requests data-source credentials or reports a missing source, use the authorized source configuration associated with the report.
4. Review the model and refresh the report, if appropriate and permitted.
5. Check that the visuals load correctly before relying on their values.

The report-definition JSON and CSV inventories are for documentation and inspection; they are not a substitute for the interactive `.pbix` report.

## Current extraction status

| Component | Status |
|---|---|
| Original `.pbix` report | Included |
| Report pages and visual inventory | Extracted |
| Field and measure-name references | Inventoried from report definitions |
| Flat-file dataset export | Not yet extracted and verified |
| Complete table/column schema | Not yet verified |
| DAX expressions | Not yet recovered |
| Model relationships | Not yet recovered |
| Power Query transformations | Not yet recovered |
| Screenshots of dashboard pages | Not currently included |

## Next steps to improve reproducibility

1. Inspect the semantic model and verify table/column definitions, relationships, and DAX expressions.
2. Export the underlying data only if the source-data license and privacy requirements permit it.
3. Document each KPI's actual calculation and validate it against the report.
4. Add screenshots of the five report pages to this repository.
5. Record the data source, refresh process, and any assumptions or limitations.

## Before making the repository public

- Confirm that you have permission to publish the `.pbix` file and any embedded data.
- Do not publish credentials, tokens, private data, or confidential source information.
- Check GitHub's file-size limits before committing the `.pbix` file. GitHub blocks regular Git files larger than 100 MB; Git LFS may be appropriate for larger files.
- Add a license only if you have the right to license all included material. No license is provided by this repository by default.

## Disclaimer

This repository documents a Power BI report and its extracted metadata. It does not independently validate the source data, model calculations, or disaster-response conclusions. Verify the data, measures, and source permissions before using the report for operational, academic, or public claims.
