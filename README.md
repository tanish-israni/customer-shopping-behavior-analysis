# Customer Shopping Behavior Analysis

End-to-end customer analytics project built with **Python, MySQL, and Power BI**. It turns 3,900 retail purchase records into a repeatable workflow for data preparation, SQL analysis, interactive reporting, and business-facing communication.

## Business objective

Understand the customer, product, and promotion patterns that influence revenue and retention. The project answers questions such as:

- Which customer groups and product categories generate the most revenue?
- Do discounts, subscriptions, and shipping choices relate to customer spend?
- Which products earn the best ratings and receive discounts most often?
- How can customers be segmented by purchase history?

## Dashboard and deliverables

| Deliverable | Location |
| --- | --- |
| Interactive Power BI dashboard | [`powerbi/customer_behaviour_dashboard.pbix`](powerbi/customer_behaviour_dashboard.pbix) |
| MySQL business queries | [`sql/customer_shopping_behavior_analysis.sql`](sql/customer_shopping_behavior_analysis.sql) |
| Python preparation notebook | [`notebooks/customer_shopping_behavior_analysis.ipynb`](notebooks/customer_shopping_behavior_analysis.ipynb) |
| Written report | [`reports/Customer Shopping Behavior Analysis.pdf`](reports/Customer%20Shopping%20Behavior%20Analysis.pdf) |
| Presentation deck | [`presentation/Customer-Shopping-Behavior-Analysis.pptx`](presentation/Customer-Shopping-Behavior-Analysis.pptx) |

## Key findings

The figures below are calculated from the included dataset.

| Metric | Result | Takeaway |
| --- | ---: | --- |
| Customers / purchase records | 3,900 | Broad base for exploratory segmentation |
| Total revenue | $233,081 | Overall revenue represented in the dataset |
| Average purchase value | $59.76 | Useful benchmark for customer-level comparisons |
| Highest-revenue category | Clothing ($104,264) | Primary category for commercial focus |
| Discounted transactions | 43.0% | Promotions are used frequently |
| Top-rated product | Gloves (3.86 / 5) | A strong product candidate for merchandising analysis |
| Subscriber average spend | $59.49 | Similar to non-subscribers ($59.87); subscription value should be evaluated beyond spend alone |

> **Note:** This dataset contains more male than female purchase records, so gender-level revenue totals should be interpreted alongside record counts rather than as a direct spending comparison.

## Workflow

```text
Raw CSV → Python data preparation → MySQL business queries → Power BI dashboard → Report & presentation
```

1. **Python / Pandas** standardizes column names, creates age groups and purchase-frequency fields, and prepares the data for analysis.
2. **MySQL** answers ten focused business questions, including revenue comparisons, customer segmentation, top products by rating, and discount behavior.
3. **Power BI** presents the results in an interactive dashboard for stakeholder exploration.
4. **Report and presentation** communicate the findings and recommendations in business-friendly formats.

## Repository structure

```text
.
├── data/raw/        Source dataset
├── notebooks/       Python / Jupyter data-preparation workflow
├── sql/             MySQL analysis queries
├── powerbi/         Power BI dashboard (.pbix)
├── reports/         Analysis report (PDF and DOCX)
└── presentation/    Presentation deck
```

## Dataset

Source file: [`data/raw/customer_shopping_behavior.csv`](data/raw/customer_shopping_behavior.csv)

- **Granularity:** one customer purchase record
- **Size:** 3,900 records and 18 source columns
- **Fields include:** customer ID, age, gender, item and category, purchase amount, location, review rating, subscription status, shipping type, discount and promotion use, previous purchases, payment method, and purchase frequency.

## Run the project

### Prerequisites

- Python 3.9+ with `pandas`, `jupyter`, and `sqlalchemy`
- MySQL 8+
- Power BI Desktop (to open or refresh the dashboard)

### 1. Explore and prepare the data

From the repository root, launch Jupyter:

```bash
jupyter notebook
```

Open `notebooks/customer_shopping_behavior_analysis.ipynb`. Update the CSV path to `data/raw/customer_shopping_behavior.csv` if your Jupyter working directory is the repository root.

### 2. Load and analyze in MySQL

The notebook standardizes source-column names (for example, `Purchase Amount (USD)` becomes `purchase_amount`) and derives `age_group`. Load that prepared dataset into a MySQL table named `customer`, then run:

```sql
SOURCE sql/customer_shopping_behavior_analysis.sql;
```

The SQL script creates/uses the `customer_behavior` database and contains the analysis queries.

### 3. Explore the dashboard

Open `powerbi/customer_behaviour_dashboard.pbix` in Power BI Desktop. If prompted, update the data-source path to the local CSV or prepared dataset.

## Tools

- **Python:** Pandas, Jupyter Notebook, SQLAlchemy
- **Database:** MySQL
- **Visualization:** Microsoft Power BI
- **Documentation:** Microsoft Word and PowerPoint

## Author

Tanish Israni