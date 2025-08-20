# Credit Card Customer Segmentation & Analytics 💳

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Tools](https://img.shields.io/badge/Tools-MySQL%20%7C%20Power%20BI-yellow.svg)
![Libraries](https://img.shields.io/badge/Libraries-Pandas%20%7C%20Scikit--learn%20%7C%20Seaborn-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📄 Overview

This project provides a comprehensive analysis of a credit card dataset, featuring both **unsupervised machine learning** for customer segmentation and a **Power BI dashboard** for interactive business intelligence reporting.

The analysis is broken into two main parts:
1.  **Customer Segmentation (Python):** Utilizes K-Means Clustering and PCA in Jupyter Notebooks to identify distinct customer archetypes based on their spending habits.
2.  **BI Reporting (Power BI & MySQL):** Features an interactive dashboard for visualizing key business metrics like revenue trends and transaction analysis, powered by a MySQL database.

The ultimate goal is to provide actionable insights for targeted marketing, risk assessment, and strategic decision-making.

---

## 📋 Table of Contents

- [Problem Statement](#-problem-statement)
- [Dataset](#-dataset)
- [Project Workflow](#-project-workflow)
- [Key Findings & Cluster Profiles](#-key-findings--cluster-profiles)
- [Technologies Used](#-technologies-used)
- [How to Use](#-how-to-use)

---

## 🎯 Problem Statement

A credit card company wants to better understand its customer base to tailor its marketing campaigns more effectively. By grouping customers into distinct segments and visualizing key performance indicators, the company can create personalized offers, improve customer retention, and identify high-value or at-risk customers.

---

## 💾 Dataset

The dataset contains transactional data for approximately 9,000 active credit card holders over a 6-month period. It includes 18 behavioral variables.

**Key Features:**
- `BALANCE`: The outstanding balance on the credit card.
- `PURCHASES`: The total amount of purchases made.
- `CREDIT_LIMIT`: The credit limit for the account.
- `PAYMENTS`: The total amount of payments made by the user.
- `TENURE`: The duration of the credit card service in months.

---

## ⚙️ Project Workflow

The project follows a structured data science and business intelligence workflow:

1.  **Data Storage:** CSV files are loaded into a **MySQL database** to serve as a single source of truth.
2.  **Data Cleaning & Preprocessing (Python):** Missing values are handled, and data is scaled using `StandardScaler` for the ML model.
3.  **Exploratory Data Analysis (EDA):** Feature distributions and correlations are analyzed to understand data patterns.
4.  **Dimensionality Reduction (PCA):** PCA is used to reduce features for effective clustering and visualization.
5.  **K-Means Clustering:** The **Elbow Method** is used to find the optimal number of clusters, and a K-Means model is trained to segment customers.
6.  **BI Dashboarding (Power BI):** A Power BI report is connected to the MySQL database to create interactive visualizations of business metrics.

---

## 📈 Key Findings & Cluster Profiles

The Python analysis identified four distinct customer segments:

* **Cluster 0: The Transactors (High Spenders, Low Balance)**
    * **Characteristics:** High purchase frequency, high one-off purchases, and they consistently pay off their balance.
    * **Marketing Strategy:** Target with premium rewards, cashback offers, and loyalty programs.

* **Cluster 1: The Revolvers (High Balance, High Credit Limit)**
    * **Characteristics:** Maintain a high balance, make frequent use of installments, and have a high credit limit.
    * **Marketing Strategy:** Offer balance transfer options and low-interest installment plans.

* **Cluster 2: The Cautious Spenders**
    * **Characteristics:** Low balance, low purchase frequency, and low credit limit.
    * **Marketing Strategy:** Encourage usage through small, targeted offers and bonus points.

* **Cluster 3: The Low-Activity Customers**
    * **Characteristics:** Very low activity across all metrics; at risk of churning.
    * **Marketing Strategy:** Launch re-engagement campaigns and "welcome back" bonuses.

---

## 🛠️ Technologies Used

- **Data Analysis & ML:** Python, Jupyter Notebook, NumPy, Pandas, Scikit-learn
- **Data Visualization:** Matplotlib, Seaborn
- **Database:** MySQL
- **Business Intelligence:** Power BI

---

## 🚀 How to Use

This project has two main components: the Python analysis and the Power BI dashboard.

### Part 1: Python Analysis (Jupyter Notebooks)

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Aditya7615/Credit_Card_Data_Report.git](https://github.com/Aditya7615/Credit_Card_Data_Report.git)
    cd Credit_Card_Data_Report
    ```
2.  **Install the required libraries:**
    ```bash
    pip install numpy pandas matplotlib seaborn scikit-learn jupyter
    ```
3.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
4.  **Open and run the notebooks** to see the full analysis, from data cleaning to cluster interpretation.

### Part 2: Power BI Dashboard (MySQL + Power BI)

This part visualizes the data stored in a MySQL database.

#### ⚡ Quickstart Steps

1.  **Load Data into MySQL**
    - Import these CSV files into your MySQL database:
      - `credit_card.csv`
      - `customer.csv`
      - `cc_add.csv`
      - `cust_add.csv`
    - Use the `LOAD DATA LOCAL INFILE` command or your favorite database tool.
    - Ensure you create the tables: `cc_detail` and `customer_detail`.

2.  **Connect Power BI to MySQL**
    - Open Power BI Desktop.
    - Go to **Get Data** → **MySQL Database** → Enter your server and database connection details.
    - Choose **Import** or **DirectQuery** to load the `cc_detail` and `customer_detail` tables.

3.  **Build or Open the Dashboard**
    - Open the provided Power BI report file (`.pbix`).
    - Make sure table relationships are correctly set (e.g., using `Customer ID` to link the tables).
    - **Refresh** the dashboard to pull the latest data from your MySQL database.

#### 🎯 Dashboard Features
- Quarterly Revenue and Transaction Trends.
- Revenue breakdown by Expenditure, Card Type, Education, Salary, State, and Gender.
- Dynamic updates when the underlying MySQL data is refreshed!

