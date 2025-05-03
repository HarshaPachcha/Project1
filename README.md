# Project1

# LinkedIn Job Trend Analysis_ Understanding Skill Demand Across Cities and Roles

This project scrapes job listings from LinkedIn to analyze skill demand trends across cities and roles, specifically focusing on the **Data Analyst** role. The project processes the scraped data to identify the top skills required and visualizes them using heatmaps. It also generates insights for businesses and job seekers to understand the market demand for various skills across different locations.

## 📌 **Objective**

- Scrape LinkedIn job postings for the role of **Data Analyst** (or other roles) to analyze skill demand trends.
- Clean and parse the job descriptions to extract relevant skills.
- Generate heatmaps to visualize the demand for top skills across various cities.
- Provide a **Skill vs. City Matrix** and **Job Demand Recommendations** based on the analysis.

## 🛠 **Tools & Libraries Used**

- **Python 3.x**
- **Libraries:**
  - `requests` (for sending HTTP requests)
  - `BeautifulSoup` (for scraping job listings from LinkedIn)
  - `pandas` (for data manipulation and analysis)
  - `matplotlib` and `seaborn` (for data visualization)
- **Others:**
  - **Time module** (to add delays between requests and respect LinkedIn's terms)

## 🚀 **Getting Started**

To run this project locally, follow the steps below:

### **1. Clone the Repository**

```bash
git clone https://github.com/your-username/linkedin-job-trend-analysis.git
cd linkedin-job-trend-analysis
```

### **2. Install Dependencies**

Install the required Python libraries:

```bash
pip install -r requirements.txt
```

If you don't have a `requirements.txt` file, install the necessary libraries manually:

```bash
pip install requests beautifulsoup4 pandas matplotlib seaborn
```

### **3. Modify Configuration (Optional)**

You can adjust the `keywords` and `location` in the script to scrape different job roles and locations. For example, to scrape for **Software Engineer** jobs in **California**, change the values as shown below:

```python
keywords = "Data Analyst"
location = ""
```
Location is empty because to scrap information from different locations for the role of data analyst

### **4. Run the Script**

Run the Python script:

```bash
python linkedin_job_analysis.py
```

### **5. Output Files**

The script will generate the following output files:

- **`linkedin_job_data.csv`**: A CSV file containing scraped job data including job titles, companies, cities, descriptions, and associated skills.
- **`skill_vs_city_matrix.csv`**: A CSV file containing a matrix of skill demand by city.

### **6. Visualizations**

- **Heatmap**: The script will generate a heatmap showing the top 10 skills and their demand across different cities.


## 📝 **Project Structure**

```plaintext
linkedin-job-trend-analysis/
│
├── linkedin_job_analysis.py    # Main Python script for scraping and analysis
├── linkedin_job_data.csv       # Output file with scraped job data
├── skill_vs_city_matrix.csv    # Matrix of skill demand across cities
├── requirements.txt            # List of Python dependencies
└── README.md                   # Project README
```


## 📊 **Data Visualization**

The analysis includes a **heatmap** showing the demand for top 10 skills across cities, providing valuable insights for job seekers and businesses.

### **Example Heatmap**

- The x-axis represents the **top 10 skills**.
- The y-axis represents the **cities**.
- The values in the heatmap represent the **demand** for each skill in each city.



## 🧰 **How It Works**

1. **Web Scraping**: The script uses **BeautifulSoup** to scrape job listings from LinkedIn. It extracts job titles, company names, job locations, and descriptions.
2. **Skill Matching**: The job descriptions are scanned for a list of predefined skills (e.g., Python, SQL, Data Visualization). Skills are then matched and stored.
3. **Data Cleaning & Analysis**: The skills data is cleaned, and a **pivot table** is created to analyze the number of job postings requiring each skill in each city.
4. **Visualization**: A heatmap is generated to show the skill demand trends across cities.
5. **Exporting Data**: All the results are saved in CSV files for further analysis.





##Project-2
# 📊 HR Analytics - Predict Employee Attrition

This project combines an interactive Power BI dashboard with a machine learning model to analyze and predict employee attrition. It leverages real-world HR data to visualize trends, identify high-risk segments, and build predictive models to support data-driven HR decisions.

---

## 🔍 Overview

The goal is to help HR departments and leadership teams understand employee turnover using data analysis and machine learning techniques. The project has two main parts:

1. 📈 **Power BI Dashboard** – for data visualization and trend analysis
2. 🤖 **Python ML Model** – for predicting whether an employee is likely to leave

---

## 📁 Dataset

- **File Name**: `Employee Attrition.csv`
- **Records**: ~1,470 employees
- **Features**:
  - Demographics: `Age`, `Gender`, `MaritalStatus`
  - Employment details: `JobRole`, `Department`, `YearsAtCompany`, `MonthlyIncome`
  - Satisfaction metrics: `JobSatisfaction`, `WorkLifeBalance`
  - Target variable: `Attrition`

---

## 📊 Power BI Dashboard Features

### ✅ KPI Cards
- Total Employees
- Employees Left
- Attrition Rate
- Average Monthly Income
- Average Age
- Average Years at Company

### 📊 Visuals
- Age Distribution by Attrition
- Attrition by Department and Job Role
- Waterfall Chart: Department-wise Attrition Contribution
- Job Satisfaction vs. Attrition
- Monthly Income vs. Attrition

### 🎛️ Interactive Filters
- Gender, Job Role, Department, Education Field, Work-Life Balance, Years at Company

---

## 🤖 Machine Learning Model (Python)

A simple ML pipeline built using **Pandas**, **Scikit-learn**, **Seaborn**, and **Matplotlib** to predict employee attrition.

### 🧪 Models Used:
- Decision Tree Classifier (default)
- Logistic Regression (optional)

### 🧰 Process:
1. Label Encoding of categorical variables
2. Train/Test split (80/20)
3. Model training and prediction
4. Evaluation: Accuracy, Confusion Matrix, and Classification Report

### 📌 Sample Output:
```bash
Accuracy: 0.83

Classification Report:
              precision    recall  f1-score   support
           0       0.86      0.92      0.89       252
           1       0.64      0.47      0.54        42

Confusion Matrix:
[[232  20]
 [ 22  20]]



