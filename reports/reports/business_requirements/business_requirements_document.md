# Business Requirements Document

## 1. Document Information

| Field          | Details                                                                                  |
| -------------- | ---------------------------------------------------------------------------------------- |
| Project Title  | Customer, Product and Promotion Decision Intelligence System                             |
| Document Type  | Business Requirements Document                                                           |
| Version        | 1.0                                                                                      |
| Status         | Draft                                                                                    |
| Prepared By    | Nenavath Siddhu                                                                          |
| Intended Users | Management, Marketing, Sales, Product, Finance, Customer Experience and Operations teams |
| Tools          | Python, SQL and Power BI                                                                 |

---

## 2. Executive Summary

The retail business collects customer shopping data but lacks a structured analytical system for understanding customer behaviour, product performance, promotional usage and customer satisfaction.

This project will develop an end-to-end decision-support solution using business analysis, Python, SQL, statistical methods and Power BI. The solution will provide governed KPIs, customer and product insights, interpretable customer segments, statistical validation and prioritised business recommendations.

The dataset contains one recorded purchase per customer and does not contain transaction dates, product costs, returns or campaign-response information. Therefore, the project will clearly distinguish measurable KPIs from business metrics that require additional data.

---

## 3. Business Problem

Stakeholders currently lack a consolidated view of:

* Customer groups associated with higher current purchase values
* Product and category performance
* Subscription and discount usage
* Customer satisfaction patterns
* Seasonal, shipping and payment preferences
* High-volume products with comparatively low ratings
* Business recommendations based on analytical evidence

Without a consistent analytical framework, stakeholders may interpret KPIs differently or make decisions based only on descriptive observations.

---

## 4. Business Objectives

The project aims to:

1. Establish consistent and governed KPI definitions.
2. Identify customer groups associated with higher current purchase values.
3. Evaluate category and item performance using value, volume and ratings.
4. Assess discount and subscription patterns.
5. Identify customer-satisfaction issues.
6. validate important differences using statistical methods.
7. Develop interpretable customer segments.
8. Create an interactive Power BI decision-support dashboard.
9. Translate findings into prioritised recommendations.
10. Document unavailable KPIs and future data requirements.

---

## 5. Project Scope

### 5.1 In Scope

* Stakeholder and business-requirement analysis
* Dataset profiling and quality assessment
* Data cleaning and transformation
* Governed KPI calculation
* Customer demographic and behavioural analysis
* Category and product analysis
* Discount and subscription analysis
* Customer-rating analysis
* Seasonal, shipping and payment analysis
* Statistical hypothesis testing
* Interpretable customer segmentation
* Product opportunity matrix
* SQL business analysis
* Four-page Power BI dashboard
* Recommendation prioritisation
* Documentation of limitations and future data needs

### 5.2 Out of Scope

The following are outside the current analytical scope because the required fields are unavailable:

* Monthly or yearly revenue growth
* Customer retention and churn
* Customer lifetime value
* True RFM analysis
* Product profitability and profit margin
* Discount profitability
* Campaign-response analysis
* Product-return analysis
* Conversion-rate analysis
* Demand forecasting

These capabilities may be included in a future project phase if transaction-level data becomes available.

---

## 6. Stakeholders

| Stakeholder              | Business Need                                | Expected Project Output                      |
| ------------------------ | -------------------------------------------- | -------------------------------------------- |
| Senior Management        | Overall performance and opportunities        | Executive dashboard and recommendations      |
| Marketing Manager        | Customer targeting and subscription insights | Customer-segmentation analysis               |
| Sales Manager            | Category, product and seasonal performance   | Sales and product analysis                   |
| Product Manager          | Product performance and satisfaction         | Product opportunity matrix                   |
| Finance Team             | Discount and purchase-value evaluation       | Promotion comparison                         |
| Customer Experience Team | Low-rating drivers and satisfaction patterns | Customer-satisfaction analysis               |
| Operations Team          | Shipping-method usage and ratings            | Operations insights                          |
| Data Analyst             | Reliable analytical requirements             | Cleaned data, SQL queries and validated KPIs |
| Business Analyst         | Traceable business requirements              | BRD, KPI dictionary and traceability matrix  |

---

## 7. Business Questions

### Customer Analysis

1. Which customer groups have the highest average current purchase value?
2. How do age, gender, location and purchase frequency relate to purchasing?
3. How do subscribers and non-subscribers differ?
4. Which customer segments should marketing prioritise?

### Product Analysis

5. Which categories and products generate the highest recorded value and volume?
6. Which products combine high volume with low ratings?
7. Which products are highly rated but purchased less frequently?
8. How do product preferences vary across customer segments and seasons?

### Promotion Analysis

9. Are discounted purchases associated with different purchase values?
10. Which categories and customer groups show greater discount usage?
11. Can subscription and discount effects be evaluated independently?

### Customer Experience

12. Which items, categories or shipping methods receive lower ratings?
13. Are rating differences statistically and practically meaningful?

### Decision Support

14. Which recommendations provide the best balance of expected impact and implementation effort?
15. What additional data should the business collect for future analysis?

---

## 8. Business Requirements

| ID    | Business Requirement                                               | Stakeholder                 | Priority |
| ----- | ------------------------------------------------------------------ | --------------------------- | -------- |
| BR-01 | Provide an executive view of major governed KPIs                   | Senior Management           | Must     |
| BR-02 | Compare purchase performance across customer groups                | Marketing and Sales         | Must     |
| BR-03 | Evaluate category and item performance by value, volume and rating | Sales and Product           | Must     |
| BR-04 | Compare discounted and non-discounted purchases                    | Finance and Marketing       | Must     |
| BR-05 | Compare subscribers and non-subscribers                            | Marketing                   | Must     |
| BR-06 | Identify low-rating products and customer-experience patterns      | Product and CX              | Must     |
| BR-07 | Analyse shipping and payment preferences                           | Operations                  | Should   |
| BR-08 | Identify interpretable customer segments                           | Marketing                   | Must     |
| BR-09 | Create a product opportunity matrix                                | Product Manager             | Must     |
| BR-10 | Statistically validate important group differences                 | Management and Data Analyst | Must     |
| BR-11 | Provide interactive filtering and drill-through                    | All dashboard users         | Should   |
| BR-12 | Prioritise recommendations by impact and effort                    | Senior Management           | Must     |
| BR-13 | Document dataset limitations and unavailable KPIs                  | All stakeholders            | Must     |
| BR-14 | Ensure consistency between Python, SQL and Power BI results        | Data Analyst                | Must     |

### Priority Definition

* **Must:** Essential for project success
* **Should:** Important but not essential for the first release
* **Could:** Valuable if time permits
* **Won’t:** Excluded from the current release

---

## 9. Functional Requirements

| ID    | Functional Requirement                                                                            | Related Business Requirement |
| ----- | ------------------------------------------------------------------------------------------------- | ---------------------------- |
| FR-01 | Calculate total recorded purchase value                                                           | BR-01                        |
| FR-02 | Calculate distinct customer count and average purchase value                                      | BR-01                        |
| FR-03 | Calculate average rating while excluding missing ratings                                          | BR-01, BR-06                 |
| FR-04 | Filter results by gender, age group, location, category, season, subscription and discount status | BR-02, BR-11                 |
| FR-05 | Compare category and item value, count and rating                                                 | BR-03                        |
| FR-06 | Compare discounted and non-discounted purchase averages                                           | BR-04                        |
| FR-07 | Display subscription rate and subscriber performance                                              | BR-05                        |
| FR-08 | Classify products using documented volume and rating thresholds                                   | BR-09                        |
| FR-09 | Create customer segments using selected behavioural features                                      | BR-08                        |
| FR-10 | Report confidence intervals, effect sizes and appropriate statistical tests                       | BR-10                        |
| FR-11 | Support dashboard drill-through and tooltip functionality                                         | BR-11                        |
| FR-12 | Display recommendation owner, priority, evidence and success measure                              | BR-12                        |
| FR-13 | Display important KPI definitions and limitations                                                 | BR-13                        |
| FR-14 | Reconcile key outputs across Python, SQL and Power BI                                             | BR-14                        |

---

## 10. Non-Functional Requirements

| ID     | Requirement      | Acceptance Measure                                                                |
| ------ | ---------------- | --------------------------------------------------------------------------------- |
| NFR-01 | Accuracy         | Major KPI values must match across Python, SQL and Power BI                       |
| NFR-02 | Usability        | Dashboard navigation and filters must be understandable without technical support |
| NFR-03 | Performance      | Dashboard pages should respond to filters without unreasonable delay              |
| NFR-04 | Maintainability  | KPI definitions and transformation rules must be documented                       |
| NFR-05 | Reproducibility  | Analysis must run from documented notebooks and SQL scripts                       |
| NFR-06 | Transparency     | Assumptions, thresholds and analytical limitations must be visible                |
| NFR-07 | Interpretability | Segments and statistical results must have understandable business explanations   |
| NFR-08 | Privacy          | Customer IDs must not be exposed unnecessarily in dashboard views                 |

---

## 11. Business Rules

| Rule ID | Business Rule                                                                                               |
| ------- | ----------------------------------------------------------------------------------------------------------- |
| RULE-01 | Each row represents one customer and one recorded purchase                                                  |
| RULE-02 | Purchase amount represents current recorded purchase value, not lifetime revenue                            |
| RULE-03 | A high current-value purchase is provisionally defined as at least $75                                      |
| RULE-04 | Missing ratings must be excluded from rating averages                                                       |
| RULE-05 | Ratings below 3.0 are classified as low                                                                     |
| RULE-06 | Ratings from 3.0–3.9 are classified as medium                                                               |
| RULE-07 | Ratings from 4.0–5.0 are classified as high                                                                 |
| RULE-08 | `Promo Code Used` must not be treated as independent of `Discount Applied` because the fields are identical |
| RULE-09 | Customer ID must not be used as a predictive-model feature                                                  |
| RULE-10 | Statistical association must not be described as causation                                                  |
| RULE-11 | Product opportunity thresholds must be documented before classification                                     |
| RULE-12 | Segments must not be described as lifetime-value segments                                                   |

---

## 12. Dashboard Requirements

### Page 1: Executive Overview

* Total recorded purchase value
* Total customers
* Average purchase value
* Average review rating
* Subscription rate
* Discount usage rate
* Category contribution
* Seasonal performance
* Summary of major findings

### Page 2: Customer and Segmentation

* Customer demographics
* Purchase-frequency analysis
* Subscriber comparison
* Discount usage by segment
* Customer-segment profiles
* Segment filters and drill-through

### Page 3: Product and Satisfaction

* Category and item performance
* Product opportunity matrix
* High-volume, low-rated products
* Rating distribution
* Ratings by category, item and shipping type

### Page 4: Promotion and Decision Support

* Discounted versus non-discounted comparisons
* Discount usage by category and customer group
* Statistical findings
* Recommendation prioritisation
* Recommendation owner and success measure

---

## 13. Data Requirements

### Available Fields

* Customer ID
* Age
* Gender
* Item Purchased
* Category
* Purchase Amount
* Location
* Size
* Colour
* Season
* Review Rating
* Subscription Status
* Shipping Type
* Discount Applied
* Promo Code Used
* Previous Purchases
* Payment Method
* Frequency of Purchases

### Additional Data Required for Future Analysis

| Required Field          | Future Use                     |
| ----------------------- | ------------------------------ |
| Transaction Date        | Trends, seasonality and growth |
| Order ID                | Transaction-level tracking     |
| Quantity                | Units sold and basket analysis |
| Unit Price              | Pricing analysis               |
| Product Cost            | Profit and margin analysis     |
| Discount Amount         | Discount profitability         |
| Return Status           | Return-rate analysis           |
| Campaign ID             | Campaign-performance analysis  |
| Sales Channel           | Channel comparison             |
| Customer Activity Dates | Retention, churn and recency   |
| Website Visits or Leads | Conversion analysis            |

---

## 14. Assumptions and Constraints

### Assumptions

* Customer ID uniquely identifies each customer.
* Purchase Amount is expressed in US dollars.
* Category and item labels are sufficiently consistent after cleaning.
* Rating values should remain between 1 and 5.
* The dataset is suitable for portfolio analysis but may not represent the entire retail market.

### Constraints

* Only 3,900 records are available.
* Each customer has one current purchase record.
* Transaction dates are unavailable.
* Product costs and profit are unavailable.
* Discount amount is unavailable.
* Return and campaign data are unavailable.
* Subscription and discount effects are confounded because every subscriber received a discount.
* Findings describe dataset associations and may not generalise to other customers.

---

## 15. Acceptance Criteria

The project will be accepted when:

* All mandatory business requirements are addressed.
* Data-quality checks are completed and documented.
* KPI calculations follow the KPI dictionary.
* Major KPI results match across Python, SQL and Power BI.
* Missing ratings are handled correctly.
* Dashboard filters and drill-through features operate correctly.
* Statistical tests include assumptions, effect sizes and business interpretation.
* Customer segments are evaluated and have understandable business profiles.
* The product opportunity matrix uses documented thresholds.
* Recommendations include evidence, priority, owner and success measures.
* Limitations and unavailable KPIs are clearly communicated.
* The GitHub repository contains sufficient documentation to reproduce and explain the project.

---

## 16. Risks and Mitigation

| Risk                                             | Impact                          | Mitigation                                        |
| ------------------------------------------------ | ------------------------------- | ------------------------------------------------- |
| Findings are presented as causal                 | Incorrect decisions             | Use association-based wording                     |
| Missing ratings distort averages                 | Misleading satisfaction results | Exclude missing ratings from rating calculations  |
| Duplicate promotion fields cause double counting | Incorrect promotion reporting   | Use only `Discount Applied`                       |
| Segments are difficult to interpret              | Low business usefulness         | Prefer stable, explainable segment profiles       |
| Small differences are treated as important       | Poor recommendations            | Report effect sizes and business significance     |
| KPI values differ between tools                  | Loss of stakeholder confidence  | Reconcile Python, SQL and Power BI outputs        |
| Dataset cannot answer advanced retail questions  | Overstated conclusions          | Document limitations and future data requirements |

---

## 17. Project Deliverables

* Business case
* Stakeholder analysis
* Business Requirements Document
* KPI dictionary
* Requirements traceability matrix
* Assumptions and constraints document
* Data dictionary
* Cleaned dataset
* Data-quality report
* Python analysis notebooks
* SQL scripts
* Statistical findings report
* Customer-segmentation model card
* Power BI dashboard
* Recommendation-prioritisation matrix
* Executive summary
* Future data requirements document
---

## 18. Related Documents

* [Stakeholder Analysis](stakeholder_analysis.md)
* [KPI Dictionary](kpi_dictionary.md)
* [Requirements Traceability Matrix](requirements_traceability_matrix.md)
* [Assumptions and Constraints](assumptions_and_constraints.md)
* [Future Data Requirements](future_data_requirements.md)
