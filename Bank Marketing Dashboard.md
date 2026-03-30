# Bank Marketing Dashboard

This dashboard shows insights from the Bank Marketing dataset using Streamlit, Plotly, and Pandas. Filters allow dynamic exploration of customer behavior.


About the Dashboard

The Bank Marketing Dashboard is an interactive data visualization tool that provides insights into customer behavior, campaign performance, and sales trends. The app includes:

- KPIs: Total sales, average rating, and average sales per order.  
- Charts:  
  - Sales by product line (horizontal bar chart)  
  - Daily sales (bar chart)  

- Dynamic Filters:  
  - Job  
  - Education  
  - Marital status  
  - Contact type  
  - Campaign outcome  

These filters allow you to explore different segments of customers and analyze patterns in their responses to marketing campaigns.


Dataset

The dashboard uses the Bank Marketing dataset, which contains customer information collected from direct marketing campaigns of a Portuguese banking institution.  

Key columns include:
- `age` – Customer age  
- `job` – Type of job  
- `marital` – Marital status  
- `education` – Education level  
- `contact` – Communication type  
- `poutcome` – Outcome of the previous marketing campaign  
- `y` – Whether the customer subscribed to a term deposit  


The dataset is stored in 'data/bank-full.csv'. Missing values in key categorical columns are filled with "Unknown".
