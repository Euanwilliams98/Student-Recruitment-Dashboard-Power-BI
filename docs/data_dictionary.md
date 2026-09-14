# Data Dictionary

This project uses three fictional recruitment tables.

## Student applications

| Field | Meaning |
|---|---|
| application_id | Unique application identifier |
| student_id | Key used to connect applications to marketing leads |
| application_date | Date the application was submitted |
| intake | Planned student intake |
| college | Fictional pathway college |
| course | Subject area applied for |
| country | Applicant country |
| application_status | Latest recruitment stage |
| offer_date | Date an offer was issued, where applicable |
| acceptance_date | Date an offer was accepted, where applicable |
| enrolment_date | Date the student enrolled, where applicable |

## Marketing leads

| Field | Meaning |
|---|---|
| lead_id | Unique enquiry/lead identifier |
| student_id | Key used to connect leads to applications |
| enquiry_date | Initial enquiry date |
| marketing_channel | Source of the enquiry |
| campaign_name | Marketing campaign linked to the lead |
| country | Country recorded at enquiry stage |

## Recruitment targets

| Field | Meaning |
|---|---|
| intake | Student intake period |
| college | Fictional pathway college |
| application_target | Target number of applications |
| enrolment_target | Target number of enrolments |

The source data intentionally contains some duplicates, blanks and inconsistent values so I could practise basic data cleaning in Power Query.