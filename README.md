# Student Recruitment and Applications Dashboard | Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811)
![Status](https://img.shields.io/badge/status-complete-2E8B57)

> A beginner portfolio project exploring student applications, enrolments and recruitment channels.

## Project summary

I worked on this project to practise cleaning data and building a simple Power BI dashboard. It uses fictional student recruitment data, with **7,500 applications** and **8,700 enquiries**.

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

This page compares conversion rates by college and country, and enrolments by marketing channel. The report also includes filters for date, college, course, country and intake.

## Tools and skills demonstrated

| Tool | What I practised |
|---|---|
| Power Query | Removing duplicates, fixing data types and handling missing values |
| Power BI | Building charts, KPI cards and filters |
| DAX | Calculating totals and conversion rates |
| Data modelling | Connecting applications, marketing leads and recruitment targets |

## Data preparation

- Removed **25 duplicate application rows**.
- Standardised inconsistent college names.
- Replaced missing marketing channels with **Unknown**.
- Filled missing country information where a matching marketing record was available.
- Connected applications to marketing leads using student ID.
- Checked missing countries, invalid statuses and unmatched applications.

More detail is available in [Data Cleaning](docs/data_cleaning.md) and the [Data Dictionary](docs/data_dictionary.md).

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

- **2,182 of 7,500 applications resulted in enrolment**, giving an overall conversion rate of **29.1%**. Enrolments reached **93.0% of the target**.
- **London Pathway College** had the most applications (**1,898**) and the highest college conversion rate (**30.5%**).
- **Education Agent** generated the most enrolments (**612**). Paid Social had a slightly higher conversion rate (**30.7%** compared with **29.2%**), showing why both volume and conversion rate are useful when comparing channels.

## What I learned

I practised turning separate data files into a report that is easy to explore. I also improved my understanding of Power Query cleaning, simple DAX measures, report filters and comparing conversion rates alongside application volumes.

I also learned that unusual results need checking before they are presented as a finding. For example, the dashboard shows a **100% conversion rate for the Unknown country category**. Because Unknown represents missing information, I would investigate those records rather than treating it as a high-performing country.

## Limitations

- All data is fictional and is used for learning.
- **Unknown** means missing information, not a real country or marketing channel.
- Targets are provided by college and intake, not by month.
- Enquiries and applications are separate records, so not every enquiry has a matching application.

## Repository structure

```text
.
├── README.md
├── docs/
│   ├── data_cleaning.md
│   └── data_dictionary.md
└── images/
    ├── recruitment-overview.png
    └── conversion-and-channels.png
```

## Author

**Euan Williams** — Aspiring Junior BI / Data Analyst  
[View my full portfolio](https://github.com/Euanwilliams98)
