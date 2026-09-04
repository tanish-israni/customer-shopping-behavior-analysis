# Customer Shopping Behavior Analysis

> End-to-end data analytics project using **Python, MySQL, and Power BI** to uncover customer, product, promotion, and revenue insights from 3,900 retail purchase records.

## Project at a glance

| Area | What I delivered |
| --- | --- |
| Business problem | Identified patterns in customer spend, subscriptions, discount use, shipping, product ratings, and repeat purchases. |
| Data preparation | Cleaned and standardized fields, created age groups, and engineered purchase-frequency features with Python and Pandas. |
| SQL analysis | Wrote business queries using aggregations, CTEs, `CASE` logic, subqueries, and window functions. |
| Dashboarding | Built an interactive Power BI dashboard to make findings accessible to stakeholders. |
| Communication | Produced a written report and presentation that translate analysis into business insights. |

## Recruiter highlights

This project demonstrates my ability to take a raw public dataset through a complete analytics workflow:

- Clean and transform data with **Python, Pandas, and Jupyter Notebook**.
- Load and query analytical data in **MySQL**.
- Use **CTEs, window functions, aggregations, conditional logic, and subqueries** to answer business questions.
- Build stakeholder-focused reporting in **Power BI**.
- Communicate findings through a formal report and presentation.

## Business questions answered

- Which categories, customer groups, and age segments contribute the most revenue?
- How does spend vary by gender, subscription status, and shipping type?
- Which discounted purchases exceed the overall average purchase value?
- Which products have the highest average ratings and the highest discount-use rates?
- How can customers be classified as new, returning, or loyal based on prior purchases?
- Which products are most frequently purchased within each category?

## Key findings

All results below were calculated from the included dataset.

| Metric | Result | Business interpretation |
| --- | ---: | --- |
| Purchase records analyzed | 3,900 | Sufficient scope for exploratory customer segmentation. |
| Total revenue | $233,081 | Total revenue represented by the dataset. |
| Average purchase value | $59.76 | Benchmark used to identify above-average transactions. |
| Highest-revenue category | Clothing ($104,264) | Largest category revenue opportunity. |
| Discounted transactions | 43.0% | Promotional activity is a material part of the purchase journey. |
| Highest-rated product | Gloves (3.86 / 5) | Potential product to investigate for merchandising and customer satisfaction. |
| Subscriber average spend | $59.49 | Comparable with non-subscribers ($59.87), suggesting subscription value should be assessed beyond average spend alone. |

> The dataset has more male than female purchase records. Revenue comparisons by gender should therefore be assessed alongside customer counts, not in isolation.

## Analytics workflow

```text
Public CSV dataset
        |
        v
Python data cleaning and feature engineering
        |
        v
MySQL exploratory and business analysis
        |
        v
Power BI dashboard
        |
        v
Business report and presentation
```

## Repository contents

| Folder / file | Description |
| --- | --- |
| [`data/raw/`](data/raw/) | Original public customer shopping dataset. |
| [`notebooks/customer_shopping_behavior_analysis.ipynb`](notebooks/customer_shopping_behavior_analysis.ipynb) | Python data-cleaning, feature-engineering, and database-loading workflow. |
| [`sql/customer_shopping_behavior_analysis.sql`](sql/customer_shopping_behavior_analysis.sql) | MySQL queries answering the core business questions. |
| [`powerbi/customer_behaviour_dashboard.pbix`](powerbi/customer_behaviour_dashboard.pbix) | Interactive Power BI dashboard. |
| [`reports/`](reports/) | Written analysis report in PDF and DOCX formats. |
| [`presentation/Customer-Shopping-Behavior-Analysis.pptx`](presentation/Customer-Shopping-Behavior-Analysis.pptx) | Stakeholder presentation deck. |

## Technical skills used

- **Python:** Pandas, Jupyter Notebook, SQLAlchemy
- **SQL / MySQL:** Data aggregation, CTEs, window functions, `CASE` statements, subqueries, segmentation
- **Power BI:** Interactive dashboard development and business reporting
- **Analytics:** Data cleaning, feature engineering, exploratory data analysis, KPI development, customer segmentation
- **Communication:** Insight reporting and presentation design

## How to run the project

### Prerequisites

- Python 3.9+ with `pandas`, `jupyter`, and `sqlalchemy`
- MySQL 8+
- Power BI Desktop

### 1. Run the Python notebook

From the repository root:

```bash
jupyter notebook
```

Open `notebooks/customer_shopping_behavior_analysis.ipynb` and run the cells. The notebook reads `data/raw/customer_shopping_behavior.csv` when launched from the repository root.

### 2. Run the MySQL analysis

The notebook standardizes column names and derives `age_group`. Load the prepared data into a MySQL table named `customer`, then execute:

```sql
SOURCE sql/customer_shopping_behavior_analysis.sql;
```

### 3. Explore the dashboard

Open `powerbi/customer_behaviour_dashboard.pbix` in Power BI Desktop. Update the data-source path if Power BI prompts you to do so.

## Author

**Tanish Israni**

If you are reviewing this project as part of my portfolio, please see the SQL script, Power BI dashboard, report, and presentation for the complete analysis.