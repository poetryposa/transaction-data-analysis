📑 SQL Query Summary

Live Dashboard
You can explore the interactive dashboard here:  
[Customer Transaction & Card Usage Dashboard]([https://lookerstudio.google.com/xxxxxx](https://lookerstudio.google.com/reporting/72dfa2eb-40d6-41d8-ba38-6d010eefa960))

1. Data Quality Checks
- Check uniqueness of IDs across tables (users_data, cards_data, transaction_data).
- Validate whether all client_id in transactions exist in users_data.
- Validate date field with SAFE_CAST to ensure proper format and range.
  
2. View Creation
- v_users → cleaned user profile (id, age, gender, income, debt, credit score).
- v_cards → standardized card data (brand, type, limit, open date).
- v_transactions → standardized transaction data (date, client, card, amount, chip usage, merchant info).
- Result Sets (rs_*) → saved views for reusable analytics, e.g. monthly trend, top MCC.

3. User Profile Analysis
- Average income, debt, credit score by gender.
- Distribution of users by credit band.

4. Card Analysis
- Card brand × type distribution with average credit limit.
- Proportion of cards flagged as present in the dark web.

5. Transaction Analysis
- Monthly transaction trends (count, total, average).
- Top MCC categories (total spend, average spend).
- Chip vs non-chip usage patterns.
- Spending by credit band (joining users + transactions).
- Spending by card brand/type (joining cards + transactions).

6. Client-Level Analysis
- Top 10 clients by total spending, with profile summary (income, credit band, number of cards).
- Transactions made with dark web–flagged cards.
- Potential anomalies: transactions greater than card credit limit.


## Notes on Dataset
For this project, I used a **sample of 3,000 rows** extracted from the original dataset (~1GB).  
Due to the reduced sample size, some visualizations such as **monthly or long-term transaction trends** may appear limited.  
The purpose of this dashboard is to **demonstrate analytical skills, data visualization, and storytelling**, rather than to fully represent the complete dataset.

