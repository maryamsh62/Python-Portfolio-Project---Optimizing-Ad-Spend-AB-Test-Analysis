# Optimizing Ad Spend: A/B Testing Analysis



## Executive Summary
**Result:** Successful. The ad campaign significantly outperformed the control group.

This project analyzes the results of an A/B test involving 588,101 users (sourced from [Kaggle](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing?resource=download)) to evaluate the effectiveness of a marketing campaign. By comparing a treatment group (exposed to ads) against a control group (exposed to a Public Service Announcement), I quantified the specific impact of the ad on user conversion rates.

**Key Wins:**
* **43% Lift** in conversion rate (2.55% vs 1.79%).
* **Statistically Significant** result (P-value < 0.05).
* identified **Monday at 4 PM** as the peak time for user engagement.
* Discovered a strong correlation between **ad frequency** and conversion (Retargeting validity).

---

## 📂 Project Structure
* `marketing_AB.csv`: The raw dataset used for analysis.
* `AB_Testing_Analysis.ipynb`: The Jupyter Notebook containing all Python code, data cleaning, and visualizations.
* `README.md`: Project overview and summary.

---

## 🔍 The Business Problem
Marketing campaigns are expensive. Before scaling a campaign, businesses need to know if the ads are actually driving sales or if users would have bought the product anyway.

**Objective:**
1.  Compare the conversion rates of the **Ad Group** vs. the **PSA Group**.
2.  Determine if the difference is statistically significant using a **Chi-Square Test**.
3.  Analyze specific days and times to optimize future ad scheduling.

---

## 🛠 Tools Used
* **Python:** Data cleaning and manipulation.
* **Pandas:** Aggregation and frequency analysis.
* **Matplotlib & Seaborn:** Data visualization (Bar charts, Line graphs).
* **SciPy:** Statistical hypothesis testing (`chi2_contingency`).

---

## 📊 Methodology & Analysis

### 1. Data Cleaning
* Checked for duplicate `user_id`s to ensure the **Independence Assumption** of the A/B test was met.
* Verified no missing values in key columns (`test group`, `converted`, `total ads`).

### 2. Hypothesis Testing
I used a **Chi-Square Test of Independence** to test the null hypothesis ($H_0$) that there is no difference between the Ad and PSA groups.



* **Contingency Table:**
    
   ![Contingency Table](https://github.com/maryamsh62/Python-Portfolio-Project---AB-Test-Analysis/blob/master/Contingency%20Table.png)
   

* **Result:** The test returned a p-value of `1.99e-13`, rejecting the null hypothesis.

### 3. Key Insights

####  Insight 1: The Ad Works (Conversion Lift)
The Ad group achieved a **2.55%** conversion rate compared to the PSA group's **1.79%**. This is a relative lift of **43%**, proving the campaign's effectiveness.

![Conversion Rate]()

####  Insight 2: Peak Times (Day & Hour)
* **Best Day:** Mondays (~3.3% conversion rate).
* **Best Time:** 4 PM (Hour 16).
* **Weakest Day:** Saturdays showed a dip in engagement across both groups.

####  Insight 3: The "Rule of Repetition"
I analyzed the `total ads` column to understand the impact of frequency.
* **Converted Users** saw an average of **83.9 ads**.
* **Non-Converted Users** saw an average of **23.3 ads**.
This suggests a strong positive correlation between impression frequency and the likelihood of conversion, supporting a retargeting strategy.

---

## 💡 Recommendations
Based on the data, I recommend the following actions to the marketing team:

1.  **Scale the Campaign:** The 43% lift justifies rolling out the ad to the full audience.
2.  **Optimize Schedule:** Increase budget allocation for **Mondays** and the **4 PM – 8 PM** window to maximize ROI.
3.  **Implement Retargeting:** Since higher frequency correlates with conversion, implement a retargeting strategy to ensure interested users see the ad multiple times.

---

Author: Maryamsadat Shakeri, [LinkedIn](https://www.linkedin.com/in/maryamsadat-shakeri/) 

