# Student Recruitment and Applications Dashboard | Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811)
![Status](https://img.shields.io/badge/status-complete-2E8B57)

> A beginner portfolio project exploring student applications, enrolments and recruitment channels.

## Project summary

I worked on this project to practise cleaning data and building a simple Power BI dashboard. It uses fictional student recruitment data, with 7,500 applications and 8,700 enquiries.

The aim was to understand how applications move through the recruitment stages and compare results by college, country and marketing channel. This is a learning project, not a report for a real organisation.

## Business questions

- How many applications led to enrolment?
- Which colleges received the most applications?
- Which marketing channels had the most enrolments?
- How close were enrolments to the target?

## Dashboard

### Recruitment overview

![Recruitment overview](images/recruitment-overview.png)

This page shows the main totals, monthly application trend, recruitment funnel and application statuses.

### Conversion and channels

![Conversion and channels](images/conversion-and-channels.png)

This page compares conversion rates by college and country, and enrolments by marketing channel. The Power BI report has filters for date, college, course, country and intake.

## Tools and skills demonstrated

| Tool | What I practised |
|---|---|
| Power Query | Removing duplicates, fixing data types and handling missing values |
| Power BI | Building charts, KPI cards and filters |
| DAX | Calculating totals and conversion rates |

## Data preparation

- Removed 25 duplicate application rows.
- Standardised college and country names.
- Replaced missing marketing channels with **Unknown**.
- Joined applications to marketing leads using student ID.
- Checked missing countries, invalid statuses and unmatched applications.

## DAX measures

Two simple examples used in the report:

```DAX
Total Applications =
DISTINCTCOUNT(Applications[application_id])

Conversion Rate =
DIVIDE([Total Enrolments], [Total Applications])
```

The conversion rate shows the percentage of applications that resulted in enrolment.

## Key findings

- **2,182 of 7,500 applications resulted in enrolment**, giving a conversion rate of **29.1%**. Enrolments reached **93.0% of the target**.
- **London Pathway College** had the most applications (**1,898**) and the highest college conversion rate (**30.5%**).
- **Education Agent** had the most enrolments (**612**). Paid Social had a slightly higher conversion rate (**30.7%** compared with **29.2%**), showing why it helps to compare both totals and percentages.

## What I learned

I practised turning separate data files into a report that is easy to explore. I also learned to check the data before drawing conclusions and to compare conversion rates alongside the number of applications.

## Limitations

- All data is fictional and is used for learning.
- **Unknown** means missing information, not a real country or channel. Its country conversion rate should not be treated as a useful market comparison.
- Targets are provided by college and intake, not by month.
- Enquiries and applications are separate records, so not every enquiry has a matching application.

## Repository structure

```text
.
├── README.md
└── images/
    ├── recruitment-overview.png
    └── conversion-and-channels.png
```

## Author

**Euan Williams** — Aspiring Junior BI / Data Analyst  
[View my full portfolio](https://github.com/Euanwilliams98)
