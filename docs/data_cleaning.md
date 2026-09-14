# Data Cleaning

Before building the dashboard, I carried out a small set of data-quality checks in Power Query.

## Cleaning steps

1. Imported the three CSV tables and promoted the first row as headers.
2. Set IDs and category fields to Text and date fields to Date.
3. Removed duplicate application records using `application_id`.
4. Standardised inconsistent college names.
5. Replaced blank marketing channels with `Unknown`.
6. Filled missing application countries from the matching marketing lead where possible; otherwise used `Unknown`.
7. Checked application statuses and flagged values outside the expected recruitment stages.
8. Connected applications to marketing leads using `student_id` and checked for unmatched records.
9. Used college and intake fields to connect recruitment targets to the report.
10. Checked totals before creating the dashboard visuals.

## Validation checks

The raw practice data contained:

- 7,525 application rows before duplicate removal;
- 7,500 unique application IDs;
- 25 duplicate application rows;
- 8,700 marketing leads;
- 16 recruitment target rows;
- 300 applications without a matching marketing lead;
- 55 application rows with a missing country;
- 95 marketing leads with a missing marketing channel.

These checks helped me understand why data cleaning should be completed before calculating KPIs or building visuals.