# Consumer Shopping Behaviour Analysis

## Project Overview

This project analyses consumer shopping data to identify patterns in customer spending, product preferences, discounts, subscriptions, ratings, shipping and purchasing behaviour..

The analysis is designed to support both Data Analyst and Business Analyst responsibilities by combining technical analysis with business requirements, stakeholder needs, KPIs and actionable recommendations.

## Business Problem

The business has customer shopping data but lacks clear evidence about:

- Which customer groups generate higher purchase value
- Which products and categories perform best
- Whether discounted purchases have different values
- How subscribers differ from non-subscribers
- Which seasonal and demographic patterns affect purchasing
- How customer information can support merchandising and marketing decisions

## Main Business Question

How can demographic, product, spending, discount, subscription, satisfaction, shipping and purchase-history information be used to identify valuable customer groups and improve merchandising, promotion and retention strategies?

## Project Objectives

1. Identify high-value customer groups.
2. Evaluate category, product and seasonal performance.
3. Compare discounted and non-discounted purchases.
4. Compare subscribers and non-subscribers.
5. Examine factors associated with purchase value and ratings.
6. Segment customers using available behavioural characteristics.
7. Translate analytical findings into measurable business recommendations.

## Dataset Overview

- Records: 3,900
- Features: 18
- Unique customers: 3,900
- Duplicate records: 0
- Missing review ratings: 37
- Age range: 18–70
- Purchase amount range: $20–$100
- Total recorded purchase value: $233,081

Each row represents one customer's current purchase together with summary information about previous purchasing behaviour.

## Tools and Technologies

- Excel: Initial validation
- SQL: Data-quality checks and business queries
- Python: Cleaning, EDA and statistical analysis
- Power BI: Interactive dashboard
- GitHub: Documentation and portfolio presentation

## Project Workflow

1. Business understanding
2. Data audit
3. Data cleaning
4. Feature engineering
5. Exploratory data analysis
6. Statistical analysis
7. Customer segmentation
8. SQL analysis
9. Power BI dashboard
10. Business recommendations

## Important Data-Quality Findings

- There are 37 missing review ratings.
- `Discount Applied` and `Promo Code Used` contain identical information.
- Every subscriber in the dataset received a discount.
- Customer IDs are ordered by gender and cannot be used as predictive features.
- The dataset does not contain transaction dates, order IDs, cost, profit or sales-channel information.

## Current Status

- [x] Business problem defined
- [x] Dataset audited
- [x] Data limitations identified
- [ ] Data cleaning completed
- [ ] Exploratory analysis completed
- [ ] Statistical testing completed
- [ ] SQL analysis completed
- [ ] Customer segmentation completed
- [ ] Power BI dashboard completed
- [ ] Recommendations finalised

## Repository Structure

```text
consumer-shopping-behaviour-analysis/
├── README.md
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── sql/
├── dashboard/
├── reports/
└── images/
