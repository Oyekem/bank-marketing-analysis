# Project Data Analytics: Bank Marketing Dataset EDA



## 📚 Table of Contents
[Project Data Analytics: Bank Marketing Analysis](#-project-data-analytics-bank-marketing-analysis)
- 📚 [Table of Contents](#-table-of-contents)
- 🎯 [Introduction](#-introduction)
- 🎯 [Objectives](#-objectives)
- 💻 [Installation](#-installation)
- 🔄 [Project Workflow](#project-workflow)
- 🗂️ [Dataset Overview](#-dataset-overview)
- 📈 [Dashboard Explanation](#-dashboard-explanation)


## 🎯 Introduction
This project analyzes the Bank Marketing dataset, which contains information about clients, their demographics, and marketing campaigns conducted by a Portuguese bank. The goal is to predict whether a client will subscribe to a term deposit (y) and extract insights for marketing strategy optimization.
The project leverages Python, Pandas, Plotly, Seaborn, and Streamlit for data analysis, visualization, and dashboard creation.


## 🎯 Objectives
- Understand customer behavior and subscription patterns
- Clean and preprocess the dataset for accurate analysis
- Identify key variables influencing marketing campaign success
- Generate actionable insights to support data-driven decision-making


## 💻 Installation
Follow these steps to set up the project locally:
1. Clone the repository
git clone https://github.com/<your-username>/bank-marketing-dashboard.git

2. Set up a virtual environment (optional but recommended)
python -m venv env
Activate the environment:
Windows:
.\env\Scripts\activate
MacOS/Linux:
source env/bin/activate

3. Install the dependencies
pip install -r requirements.txt

4. Run the dashboard
streamlit run bank_marketing_dashboard.py
The dashboard will open in your default web browser, showing interactive visualizations.


## 🔄 Project Workflow
1. Data Wrangling

The first step of the project is to clean and prepare the bank marketing dataset for analysis. The data wrangling process includes:

- Loading the dataset from CSV using Pandas
- Handling missing values and identifying “unknown” entries
- Handling duplicate records (if any)
- Correcting inconsistent data types across features
- Detecting and treating outliers using IQR and winsorization
- Handling skewed numerical features (log transformation where necessary)
- Preserving meaningful encoded values (e.g., pdays = -1, previous = 0)
- Standardizing and cleaning categorical variables for analysis
- Preparing the dataset for exploratory analysis and modeling

2. Exploratory Data Analysis

The second step of the project is to explore the dataset and extract meaningful insights about customer behavior and marketing effectiveness. The exploratory data analysis process includes:

- Target Variable Analysis
  Understanding subscription distribution and class imbalance (~11.7% subscribed)
  
- Numerical Feature Analysis
  Analyzing variables such as age, balance, duration, campaign, pdays, and previous
  
- Categorical Feature Analysis
  Exploring job, marital status, education, contact type, and poutcome
  
- Bivariate Analysis
  Examining relationships between features and subscription outcome (y)

- Campaign Performance Analysis
  Understanding how call duration, frequency, and previous outcomes affect conversion

- Customer Segmentation Analysis
  Identifying high-performing groups (students, retired, management, educated clients)

- Seasonality Analysis
  Evaluating the effect of months on campaign success

3. Data Visualization

The third step of the project is to visualize the data and communicate insights effectively. The data visualization process includes:

- Visualizing subscription distribution (class imbalance)
- Visualizing numerical features using histograms and boxplots
- Visualizing categorical features using count plots and bar charts
- Visualizing relationship between call duration and subscription probability
- Visualizing campaign frequency vs subscription success
- Visualizing previous campaign outcomes vs subscription
- Visualizing customer segments (job, education, marital status) vs conversion rate
- Visualizing contact channel effectiveness (cellular vs telephone)
- Correlation heatmap for numerical features
- Identifying trends and patterns across features

4. Dashboard

The last step of the project is to create an interactive dashboard for insights and decision-making. The dashboard includes:

- Customer subscription KPIs (conversion and non-conversion rates)
- Interactive filters (job, education, marital status, contact type, month)
- Visualization of subscription rates across customer segments
- Analysis of campaign performance (duration, frequency, previous outcomes)
- Comparison of communication channels (cellular vs telephone)
- Insights on seasonality and campaign timing
- Identification of high-value customer segments
- Actionable marketing recommendations based on data insights


## 🗂️ Dataset Overview
Source: Kaggle, CSV format
Rows: ~ 45,211
Columns / Features: 17
Target Variable: y (term deposit subscription: "yes"/"no")
Key Features
Feature
age
job
marital
education
default
balance
housing
loan
contact
day
month
duration
campaign
pdays
previous
poutcome


## 📈 Dashboard Explanation
How to use the dashboard
1. Run the Streamlit app
      streamlit run bank_marketing_dashboard.py

2. Explore visualizations
- Filters: Select job, education, marital status, contact type, or month
- KPIs: View subscription counts and conversion rates
- Charts: Compare features like:
- Job vs Subscription Rate
- Education vs Subscription Rate
- Duration vs Subscription Probability
- Campaign frequency vs Subscription
- Previous campaign outcome vs Subscription

3. Insights derived from dashboard
- Students, retired, and management clients respond best to campaigns
- Clients with higher education levels are more likely to subscribe
- Longer call duration correlates with higher subscription probability
- Previous successful campaigns strongly influence subscription behavior
- Campaigns should focus on targeted segments for efficiency


print("Thank you for exploring the Bank Marketing Dashboard! 🙏")

### Thank you for reading! 🙏




