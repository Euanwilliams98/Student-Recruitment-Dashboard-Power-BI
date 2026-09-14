# Student Recruitment and Applications Dashboard | Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811)
![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Cleaning-217346)
![DAX](https://img.shields.io/badge/DAX-Measures-0078D4)
![Status](https://img.shields.io/badge/status-complete-2E8B57)

> An entry-level Power BI portfolio project exploring student applications, enrolments and recruitment channels using fictional practice data.

## Project summary

I created this project to practise cleaning data, building a simple data model and creating an interactive Power BI dashboard. The dataset contains **8,700 enquiries** and **7,500 applications**.

The aim was to understand how applications move through the recruitment stages and compare performance by college, country and marketing channel. This is a learning project and does not represent a real organisation or real students.

## Business questions

- How many applications led to enrolment?
- Which colleges received the most applications?
- Which marketing channels generated the most enrolments?
- How close were enrolments to the target?

## Dashboard

### Recruitment overview

<img width="1660" alt="Power BI recruitment overview dashboard" src="https://github.com/user-attachments/assets/75e0bea4-f303-4c98-b142-fd89bc459174" />

This page shows the main totals, monthly application trend, recruitment funnel and current application statuses.

### Conversion and channels

<img width="1659" alt="Power BI conversion and recruitment channels dashboard" src="https://github.com/user-attachments/assets/159896e9-832b-41ac-978b-1cddc49e5461" />

This page compares enrolment conversion by college and country and shows enrolments by marketing channel. The report includes filters for date, college, course, country and intake.

## Tools and skills demonstrated

| Tool | What I practised |
|---|---|
| Power Query | Removing duplicates, fixing data types and handling missing values |
| Power BI | Building KPI cards, charts, filters and a two-page interactive report |
| DAX | Creating totals and conversion-rate measures |
| Data modelling | Connecting applications, marketing leads and recruitment targets |
| Data analysis | Comparing volumes, conversion rates and recruitment performance |

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

The conversion-rate measure shows the percentage of applications that resulted in enrolment.

## Key findings

- **2,182 of 7,500 applications resulted in enrolment**, giving an overall application-to-enrolment conversion rate of **29.1%**. Enrolments reached **93.0% of the target**.
- **London Pathway College** received the most applications (**1,898**) and also had the highest college conversion rate (**30.5%**).
- **Education Agent** generated the most enrolments (**612**). Paid Social had a slightly higher conversion rate (**30.7% versus 29.2%**), showing why both volume and conversion rate are useful when comparing channels.

## What I learned

This project helped me practise turning separate data files into a report that is easy to explore. I improved my understanding of Power Query cleaning, basic data modelling, DAX measures, report filters and comparing conversion rates alongside application volumes.

I also learned that unusual results should be checked before being treated as a genuine finding. For example, the dashboard shows a **100% conversion rate for the Unknown country category**. Because Unknown represents missing information, I would investigate those records rather than treating it as a high-performing country.

## Limitations

- All data is fictional and used for learning and portfolio purposes.
- **Unknown** represents missing information, not a real country or marketing channel.
- Targets are provided by college and intake rather than by month.
- Enquiries and applications are separate records, so not every enquiry has a matching application.

## Repository structure

```text
.
├── README.md
└── docs/
    ├── data_cleaning.md
    └── data_dictionary.md
```

## Author

**Euan Williams** — Aspiring Junior BI / Data Analyst  
[View my full portfolio](https://github.com/Euanwilliams98)
