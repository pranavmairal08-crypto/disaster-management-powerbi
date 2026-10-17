# Disaster Management Analytics — Power BI Dashboard

A Power BI report for exploring disaster patterns, geographic distribution, emergency response performance, priority, recovery, and impact.

> **Extraction status:** This repository contains the original `.pbix`, report-definition JSON extracted from the file, and inventories of report pages, visuals, and field/measure references. The embedded model is present in the original PBIX, but this extraction pass did **not** decode the model into CSV tables or recover DAX expressions. Do not describe the dataset or DAX as exported until those are independently extracted and verified.

## Report pages

### Executive Overview
- Canvas: 1920 × 1080
- Visuals: 15
  - cardVisual: Total Aid
  - textbox: SMART DISASTER RESPONSE AND EMERGENCY RESPONSE
  - cardVisual: Total Casualties
  - cardVisual: Total Economic Loss
  - lineChart: date; Total Disasters
  - clusteredBarChart: disaster_type; Total Disasters
  - cardVisual: Average Response Efficiency
  - cardVisual: Total Disasters
  - textbox: Data-driven disaster monitoring , impact assessment and emergency response analytics
  - donutChart: country; Total Disasters
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
### Global Disaster Distribution
- Canvas: 1920 × 1080
- Visuals: 8
  - textbox: Geographic distribution , disaster patterns and severity analysis
  - actionButton: (no text label extracted)
  - textbox: DISASTER INTELLIGENCE
  - actionButton: (no text label extracted)
  - map: disaster_type; severity_index; country; casualties; economic_loss_usd; response_time_hours; response_efficiency_score; longitude; latitude
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
### Emergency Response
- Canvas: 1920 × 1080
- Visuals: 13
  - scatterChart: country; Total Economic Loss; Total Aid
  - cardVisual: Average Response Efficiency
  - actionButton: (no text label extracted)
  - lineChart: date; Average Response Time
  - actionButton: (no text label extracted)
  - cardVisual: Average Recovery Days
  - lineChart: disaster_type; Average Response Time; Average Response Efficiency
  - cardVisual: Average Response Time
  - actionButton: (no text label extracted)
  - cardVisual: Total Aid
  - textbox: EMERGENCY RESPONSE
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
### Smart Priority
- Canvas: 1920 × 1080
- Visuals: 12
  - donutChart: Priority Category; Total Disasters
  - scatterChart: disaster_type; economic_loss_usd; severity_index; casualties
  - lineChart: disaster_type; Average Priority Score; Average Response Efficiency
  - textbox: SMART PRIORITY
  - cardVisual: Average Priority Score
  - cardVisual: Critical Disasters
  - cardVisual: High Priority Disasters
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
### Recovery and Impact
- Canvas: 1920 × 1080
- Visuals: 9
  - lineChart: date; Average Recovery Days
  - lineClusteredColumnComboChart: disaster_type; Total Economic Loss; Average Recovery Days
  - scatterChart: disaster_type; casualties; aid_amount_usd; economic_loss_usd
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
  - actionButton: (no text label extracted)
  - textbox: RECOVERY AND IMPACT

## Technology
- Microsoft Power BI Desktop (`.pbix`)
- Power BI report-definition JSON (visual and page metadata)
- CSV inventories for auditing and documentation

## Repository layout
```text
.
├── powerbi/
│   ├── original/Disaster_Management_Dashboard.pbix
│   └── report-definition/        # extracted page/visual/report JSON
├── metadata/
│   ├── pages.json
│   ├── visual_inventory.csv
│   └── field_inventory.csv
├── documentation/
│   └── EXTRACTION_NOTES.md
├── .gitignore
└── README.md
```

## Open the report
1. Install Power BI Desktop.
2. Open `powerbi/original/Disaster_Management_Dashboard.pbix`.
3. If prompted for credentials or a data source, use the appropriate authorized source settings.
4. Check that visuals refresh and that the model has no missing-source errors.

## Data and model extraction caveat
The PBIX contains an embedded `DataModel` binary. This package does not include a verified flat-file export of the data or DAX source. To finish that part, open the PBIX in Power BI Desktop and use an approved model-inspection/export workflow (for example, DAX Studio or Tabular Editor for model metadata/measures, and Power BI's data export or a controlled query for table data). Check licensing, privacy, and source-data permissions before publishing any rows to a public repository.

## Before publishing publicly
- Verify whether the dataset is synthetic, public, or licensed for redistribution.
- Remove credentials, private paths, personal data, and confidential information.
- Test the PBIX on another machine or clean Power BI Desktop session.
- Add screenshots of each report page if you want the GitHub README to showcase the dashboard.
- Add a license only if you have the right to license all included content. No license is included by default.

## Known model references
Table/entity reference: `Disasters`.

Measure names referenced by visuals: Average Priority Score, Average Recovery Days, Average Response Efficiency, Average Response Time, Critical Disasters, High Priority Disasters, Total Aid, Total Casualties, Total Disasters, Total Economic Loss.

These are references discovered in report visual queries, not a complete verified model schema.
