# Olist Delivery Performance Analysis

This SQL project analyzes how often Olist orders arrived after their
estimated delivery date and how late delivery rates varied by customer state.

[View the analysis notebook](olist_delivery_analysis.ipynb)

## Key Findings

- **Overall:** 6,534 of 96,470 eligible orders arrived late (6.77%).
- **Highest late delivery rate:** Alagoas (21.41%, or 85 of 397 orders).
- **Most late deliveries:** São Paulo (1,820 late orders, 4.49%).
- **Investigation priority:** Rio de Janeiro had 1,495 late deliveries
  and a 12.11% late delivery rate, above the overall rate of 6.77%.

## Method

I used SQLite to join the orders and customers tables on `customer_id`.
I compared actual and estimated calendar dates for delivered orders
with both dates available. Eight delivered orders were excluded because
at least one date was missing.

## How to Run

1. Download the [Olist dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).
2. Download the notebook from this repository and open it in Google Colab.
3. Upload `olist_orders_dataset.csv` and `olist_customers_dataset.csv`
   to the Colab session.
4. Run the notebook from top to bottom.

## Tools

SQLite, Python (pandas), and Google Colab.
