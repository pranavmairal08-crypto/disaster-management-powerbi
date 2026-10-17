# Extraction Notes

## Extracted successfully
- Original PBIX copied unchanged into `powerbi/original/`.
- Report definition JSON files copied from the PBIX.
- Five page names and canvas dimensions recorded in `metadata/pages.json`.
- Visual inventory and report-referenced fields/measures recorded as CSV files.

## Not extracted in this pass
- Data rows into CSV/Excel.
- Complete semantic model schema and relationships.
- DAX expressions for measures/calculated columns.
- Power Query M expressions and source connection details.

The PBIX `DataModel` is a binary model payload; simply unzipping the PBIX does not turn it into a readable table export. Any values/formulas should be extracted with a compatible Power BI model tool and then checked against the actual report.
