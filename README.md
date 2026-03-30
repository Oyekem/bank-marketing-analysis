Bank Marketing Prediction Dashboard
📚 Table of Contents
•	Project Data Analytics: Bank Marketing Prediction
o	📚 Table of Contents
o	🎯 Introduction
o	💻 Installation
o	🔄 Project Workflow
o	🗂️ Dataset Overview
o	📈 Dashboard Explanation
________________________________________
🎯 Introduction
This project analyzes the Bank Marketing dataset, which contains information about clients, their demographics, and marketing campaigns conducted by a Portuguese bank. The goal is to predict whether a client will subscribe to a term deposit (y) and extract insights for marketing strategy optimization.
The project leverages Python, Pandas, Plotly, Seaborn, and Streamlit for data analysis, visualization, and dashboard creation.
________________________________________
💻 Installation
Follow these steps to set up the project locally:
1.	Clone the repository
git clone https://github.com/<your-username>/bank-marketing-dashboard.git
2.	Set up a virtual environment (optional but recommended)
python -m venv env
Activate the environment:
•	Windows:
.\env\Scripts\activate
•	MacOS/Linux:
source env/bin/activate
3.	Install the dependencies
pip install -r requirements.txt
4.	Run the dashboard
streamlit run bank_marketing_dashboard.py
The dashboard will open in your default web browser, showing interactive visualizations.
________________________________________
🔄 Project Workflow
1.	Data Wrangling
o	Load the CSV dataset using Pandas
o	Handle missing and duplicate values
o	Detect and treat outliers (IQR capping, winsorization)
o	Check for skewness and optionally log-transform numeric features
2.	Exploratory Data Analysis (EDA)
o	Visualize target distribution
o	Analyze numerical features (age, balance, duration, campaign, previous, pdays)
o	Analyze categorical features (job, marital, education, contact, poutcome)
o	Extract insights to guide marketing strategy
3.	Feature Engineering
o	Encode categorical features for modeling
o	Prepare features for machine learning models (optional step if predicting y)
4.	Dashboard Visualization
o	Build an interactive dashboard using Streamlit
o	Users can filter data by features such as job, education, marital status, contact type, and month
o	Visualizations include bar charts, line charts, and KPIs for customer subscriptions
________________________________________
🗂️ Dataset Overview
•	Source: Kaggle, CSV format
•	Rows: ~45,211
•	Columns / Features: 17
•	Target Variable: y (term deposit subscription: "yes"/"no")
Key Features
Feature	Type	Description	Outlier Handling
age	Numeric	Age of client	Kept (<5% extreme)
job	Categorical	Type of job	–
marital	Categorical	Marital status	–
education	Categorical	Education level	–
default	Binary	Has credit in default?	–
balance	Numeric	Average yearly balance	IQR capping + optional log-transform
housing	Binary	Has housing loan?	–
loan	Binary	Has personal loan?	–
contact	Categorical	Contact type	–
day	Numeric	Last contact day of month	–
month	Categorical	Last contact month	–
duration	Numeric	Last contact duration (seconds)	IQR capping + optional log-transform
campaign	Numeric	Number of contacts during this campaign	IQR capping
pdays	Numeric	Days since last contact (-1 = never)	Kept
previous	Numeric	Number of contacts before this campaign	Kept
poutcome	Categorical	Outcome of previous campaign	–
________________________________________
📈 Dashboard Explanation
How to use the dashboard
1.	Run the Streamlit app
streamlit run bank_marketing_dashboard.py
2.	Explore visualizations
•	Filters: Select job, education, marital status, contact type, or month
•	KPIs: View subscription counts and conversion rates
•	Charts: Compare features like:
o	Job vs Subscription Rate
o	Education vs Subscription Rate
o	Duration vs Subscription Probability
o	Campaign frequency vs Subscription
o	Previous campaign outcome vs Subscription
3.	Insights derived from dashboard
•	Students, retired, and management clients respond best to campaigns
•	Clients with higher education levels are more likely to subscribe
•	Longer call duration correlates with higher subscription probability
•	Previous successful campaigns strongly influence subscription behavior
•	Campaigns should focus on targeted segments for efficiency
________________________________________
print("Thank you for exploring the Bank Marketing Dashboard! 🙏")
Thank you for reading! 🙏

