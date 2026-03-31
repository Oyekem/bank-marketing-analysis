# Project Data Analytics: Bank Marketing Dataset EDA



## 📚 Table of Contents
[Project Data Analytics: Bank Marketing Analysis](#-project-data-analytics-bank-marketing-analysis)
- 📚 [Table of Contents](#-table-of-contents)
- 🎯 [Introduction](#-introduction)
- 💻 [Installation](#-installation)
- 🔄 [Project Workflow](#project-workflow)
- 🗂️ [Dataset Overview](#-dataset-overview)
- 📈 [Dashboard Explanation](#-dashboard-explanation)


## 🎯 Introduction
This project analyzes the Bank Marketing dataset, which contains information about clients, their demographics, and marketing campaigns conducted by a Portuguese bank. The goal is to predict whether a client will subscribe to a term deposit (y) and extract insights for marketing strategy optimization.
The project leverages Python, Pandas, Plotly, Seaborn, and Streamlit for data analysis, visualization, and dashboard creation.


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
- Understanding subscription distribution and class imbalance (~11.7% subscribed)
Numerical Feature Analysis
Analyzing variables such as age, balance, duration, campaign, pdays, and previous
Categorical Feature Analysis
Exploring job, marital status, education, contact type, and poutcome
Bivariate Analysis
Examining relationships between features and subscription outcome (y)
Campaign Performance Analysis
Understanding how call duration, frequency, and previous outcomes affect conversion
Customer Segmentation Analysis
Identifying high-performing groups (students, retired, management, educated clients)
Seasonality Analysis
Evaluating the effect of months on campaign success

3. Data Visualization

The third step of the project is to visualize the data and communicate insights effectively. The data visualization process includes:

Visualizing subscription distribution (class imbalance)
Visualizing numerical features using histograms and boxplots
Visualizing categorical features using count plots and bar charts
Visualizing relationship between call duration and subscription probability
Visualizing campaign frequency vs subscription success
Visualizing previous campaign outcomes vs subscription
Visualizing customer segments (job, education, marital status) vs conversion rate
Visualizing contact channel effectiveness (cellular vs telephone)
Correlation heatmap for numerical features
Identifying trends and patterns across features

4. Dashboard

The last step of the project is to create an interactive dashboard for insights and decision-making. The dashboard includes:

Customer subscription KPIs (conversion and non-conversion rates)
Interactive filters (job, education, marital status, contact type, month)
Visualization of subscription rates across customer segments
Analysis of campaign performance (duration, frequency, previous outcomes)
Comparison of communication channels (cellular vs telephone)
Insights on seasonality and campaign timing
Identification of high-value customer segments
Actionable marketing recommendations based on data insights

## 🗂️ Dataset Overview
Source: Kaggle, CSV format
Rows: ~45,211
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


📈 Dashboard Explanation
How to use the dashboard
1. Run the Streamlit app
streamlit run bank_marketing_dashboard.py
2. Explore visualizations
Filters: Select job, education, marital status, contact type, or month
KPIs: View subscription counts and conversion rates
Charts: Compare features like:
Job vs Subscription Rate
Education vs Subscription Rate
Duration vs Subscription Probability
Campaign frequency vs Subscription
Previous campaign outcome vs Subscription
3. Insights derived from dashboard
Students, retired, and management clients respond best to campaigns
Clients with higher education levels are more likely to subscribe
Longer call duration correlates with higher subscription probability
Previous successful campaigns strongly influence subscription behavior
Campaigns should focus on targeted segments for efficiency


print("Thank you for exploring the Bank Marketing Dashboard! 🙏")
Thank you for reading! 🙏









### Numerical Features vs Target (y) Insights
- **Duration:** Longer calls → higher probability of subscription (strong predictor).  
- **Balance:** Moderate balances → higher subscription; extremes have less impact.  
- **Campaign:** Fewer contacts per campaign → higher subscription likelihood.  
- **Previous Contacts:** More previous contacts → higher subscription if prior campaigns were successful.  
- **Pdays:** Recent contacts (lower pdays) → higher subscription probability.  
- **Age:** Most age groups behave similarly; middle-aged clients slightly more likely to subscribe.








1️⃣ Job
Job
Student
Retired
Unemployed
Management
Admin
Self-employed
Unknown
Technician
Services
Housemaid
Entrepreneur
Blue-collar
Insights:
Highest subscription: Students and retired clients. Possibly more time/flexibility or targeted needs for saving.
Lowest subscription: Blue-collar, entrepreneurs, housemaids.
Marketing takeaway: Target campaigns toward high-performing job groups first (student, retired, unemployed).


2️⃣ Marital Status
Status
Single
Divorced
Married
Insights:
Singles have slightly higher subscription rates than married clients.
Divorced clients are in the middle.
Marketing takeaway: Consider demographic segmentation — singles might respond better to offers that emphasize flexibility or short-term benefits.


3️⃣ Contact Type
Contact
Cellular
Telephone
Unknown
Insights:
Cellular contacts convert better than landline/telephone.
Unknown contacts are nearly uninformative.
Marketing takeaway: Prioritize cellular contact campaigns; flag “unknown” contacts as missing data to handle or exclude in modeling.


4️⃣ Education
Education
Tertiary
Unknown
Secondary
Primary
Insights:
Higher education correlates with higher subscription.
“Unknown” education surprisingly performs relatively well (could include mixed education types).
Lower education levels (primary) subscribe less.
Marketing takeaway: Tailor offers for tertiary-educated clients; consider additional support or incentives for lower education groups.


5️⃣ Previous Outcome (poutcome)
Previous Outcome
Success
Other
Failure
Unknown
Insights:
Most predictive feature by far: previous success drastically increases likelihood of subscription.
“Other” and “Failure” outcomes are moderate to low.
Unknowns have the lowest predictive power.
Marketing takeaway: Clients with past success should be prioritized; this is a golden feature for predictive modeling.


✅ General Takeaways
1. Strong Influencers: poutcome, job, education, and contact type.
2. Moderate Influencers: marital status.
3. Marketing Strategy: Focus on clients who are students, retired, tertiary-educated, contacted via cellular, and had previous successful campaigns.
4. Data Handling: Unknowns exist in education, contact, poutcome; treat them carefully (imputation or separate category).
5. Feature Engineering Hint: Features like poutcome can be encoded ordinally or one-hot; high predictive power will help models handle the class imbalance better.










📌 Project Overview

This project performs an Exploratory Data Analysis (EDA) of a bank marketing dataset to uncover patterns and factors influencing customer subscription to term deposits. The dataset contains over 45,000 customer records, including demographic details, financial attributes, and interactions from marketing campaigns.



🎯 Objectives

Understand customer behavior and subscription patterns

Clean and preprocess the dataset for accurate analysis

Identify key variables influencing marketing campaign success

Generate actionable insights to support data-driven decision-making



🛠️ Tools & Technologies

Python

Pandas & NumPy for data manipulation

Matplotlib & Seaborn for data visualization



📂 Dataset Information

Rows: ~45,211

Columns: 17 features

Target Variable: y (Subscription: Yes/No)



🔧 Data Cleaning & Preparation

Handled missing values and removed duplicates

Detected and treated outliers using boxplots and IQR method

Applied Winsorization to reduce extreme values

Reduced skewness in key numerical features:



balance → ~1.09

duration → ~1.04

campaign → ~1.09

Preserved meaningful values:



pdays = -1 (no previous contact)

previous = 0 (no prior campaigns)



📊 Exploratory Data Analysis

Univariate Analysis: Examined numerical and categorical variables

Bivariate Analysis: Studied relationships with subscription outcome

Visualizations:



Histograms

Boxplots

Countplots

Correlation Analysis: Identified relationships among features using a heatmap



🔍 Key Insights

Only ~11.7% of customers subscribed → highly imbalanced dataset

Call duration is the strongest predictor of subscription

Customers with previous successful campaigns show higher conversion rates

Excessive contact attempts reduce conversion → diminishing returns

Cellular communication outperforms telephone

Moderate account balances correlate with higher subscription likelihood

Higher subscription rates observed among:



Management, students, and retired individuals

Customers with higher education levels

Seasonality effect: Certain months show higher campaign success



💡 Business Recommendations

Focus on customers with previous successful interactions

Prioritize quality over quantity in customer calls

Leverage cellular communication channels for better engagement

Avoid excessive repeated contact to reduce customer fatigue

Target high-potential customer segments identified in the analysis

Align campaigns with high-performing months to maximize conversion



⚠️ Challenges

Significant class imbalance in the target variable

Presence of outliers and skewed distributions

Some categorical variables contain “unknown” values



🚀 Future Work

Apply machine learning models for subscription prediction

Handle class imbalance using techniques like SMOTE

Perform feature selection and engineering for improved modeling



📷 Sample Visualizations

(Add 2–3 charts here to visually summarize key findings, e.g., subscription by job type, duration vs. subscription, campaign success by month)






🔗 GitHub Repository

👉 [Add Your GitHub Link Here]
