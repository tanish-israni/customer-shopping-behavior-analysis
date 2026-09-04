# Customer Shopping Behavior Analysis

An end-to-end data analytics project that explores customer shopping behavior with **Python**, **MySQL**, and **Power BI**. The analysis examines spending patterns, discounts, subscriptions, shipping preferences, product ratings, customer segments, and revenue by age group.

## Repository layout

```text
data/raw/       Original customer shopping dataset
notebooks/      Python exploratory analysis
sql/            MySQL analysis queries
powerbi/        Interactive Power BI dashboard (.pbix)
reports/        Written analysis report (PDF and DOCX)
presentation/  Presentation deck
```

## Tools used

- Python (Pandas, Jupyter Notebook)
- MySQL 8+
- Microsoft Power BI

## Dataset

The dataset contains individual customer transactions and attributes including age, gender, item and category purchased, purchase amount, location, review rating, subscription status, shipping type, discounts, prior purchases, payment method, and purchase frequency.

Dataset: `data/raw/customer_shopping_behavior.csv`

## How to reproduce the analysis

1. Open `notebooks/customer_shopping_behavior_analysis.ipynb` in Jupyter and run the cells. It loads the CSV from `data/raw/`.
2. Import the CSV into MySQL as a table named `customer`. Use column names compatible with the queries in `sql/customer_shopping_behavior_analysis.sql` (for example, `purchase_amount`, `item_purchased`, and `review_rating`).
3. Run the SQL script to answer the business questions.
4. Open `powerbi/customer_behaviour_dashboard.pbix` in Power BI Desktop. Refresh its data source if prompted.
5. Review the full findings in `reports/` and `presentation/`.

## Analysis questions

- How does revenue differ by gender and age group?
- Which discounted purchases still exceed average spend?
- Which products have the strongest average review ratings?
- How do subscription, shipping, and repeat-purchase behaviors relate to spending?
- Which products and customer segments offer the strongest commercial signals?

## Project files

The dashboard, reports, and presentation are included as editable/original deliverables. They may require Microsoft Power BI or Microsoft Office-compatible software to view or edit.

