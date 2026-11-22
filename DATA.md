# Data card: citynet_churn.csv

- Source: CityNet customer records (made-up data for this course)
- Rows: 5000   Columns: 14
- One row is: one customer, measured over the last 90 days
- Target: `churned` = 1 if the customer cancelled in the next month. Share of 1s: 17.9%
- Missing values:  `age` = 411, `payment_method` = 149
- Columns NOT used, and why: - Columns NOT used, and why: `cancel_request_logged` — excluded due to data leakage. Churn rate is 3.3% when the value is 0 and 95.8% when the value is 1.
- Known issues: Imbalanced dataset (82.1% non-churned, 17.9% churned). Missing values in age and payment_method.
