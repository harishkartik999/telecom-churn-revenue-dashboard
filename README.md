# Telecom Customer Churn & Revenue Dashboard

An interactive 4-page Power BI dashboard analyzing 7,043 telecom customers to identify churn drivers, quantify revenue at risk, and surface a targetable high-risk customer segment.

## Overview

This dashboard was built using the Maven Analytics / IBM Telecom Customer Churn dataset. It goes beyond surface-level churn reporting by using rate-based analysis (instead of raw counts) to avoid misleading conclusions, and by engineering a composite risk segment that isolates the customers most likely to leave.

## Key Findings

- **Overall churn rate: 26.54%**, resulting in **$3.68M** in lost revenue out of $21.37M total revenue.
- **Fiber Optic customers** generate 58% of total revenue ($12.41M) but churn at **40.7%** — nearly double every other internet type.
- A composite **high-risk segment** (high monthly charge + tenure under 12 months + month-to-month contract) contains just **410 customers**, yet churns at **77.3%** — over 3x the company average.
- Customers with **no dependents** churn at **32.6%**, compared to just **6.5%** for those with 1 or more dependents — a 5x gap suggesting family/bundle plans significantly improve retention.
- **Offer E**, a promotional plan, has the highest churn rate of any offer at **52.9%** — nearly double the no-offer baseline — suggesting its terms attract price-sensitive, low-loyalty customers.
- Payment method matters: customers paying by **Mailed Check** churn at **36.9%**, the highest of any payment method, despite not having the highest raw count of churned customers.

## Dashboard Pages

1. **Business Overview** — executive snapshot: total customers, churn rate, revenue, and high-level churn breakdowns by contract, tenure, and category.
2. **Churned Analysis** — root-cause analysis using rate-based metrics (not raw counts) across offer, internet service, payment method, and age group.
3. **Revenue & Risk Analysis** — connects revenue concentration with churn risk, and introduces the engineered high-risk customer segment.
4. **Key Findings & Recommendations** — a one-page executive summary designed so any viewer understands the story in under a minute.

## Screenshots

*(Add screenshots here — see instructions below)*

## Tools & Techniques

- **Power BI** — data modeling, report design, bookmarks for interactive filtering
- **DAX** — custom measures (`Churn Rate %`, `Avg Revenue per Customer`, `High Risk Churn Rate`) and a calculated column to engineer the composite high-risk segment
- **Rate-based analysis** — deliberately favored churn *rate* over raw churned-customer *count* to avoid the bias of larger segments appearing "riskier" simply due to size (e.g. Offer E has a low churned count but the highest churn rate of any offer)

## Dataset

Source: [Maven Analytics / IBM Telecom Customer Churn](https://www.mavenanalytics.io/) — 7,043 customer records with demographic, service, billing, and churn-status fields.

## Files

- `telecom_customer_churn_dashboard.pbix` — the full Power BI file
- `screenshots/` — page-by-page exports of the dashboard

---

*Built as a portfolio project to demonstrate data modeling, DAX, and business-focused dashboard design in Power BI.*
