# 2026 Datathon -- Team 59
---

## 1.Overview

Financial resilience is structurally driven by housing exposure and life-cycle debt patterns.

Using a Debt-to-Income (DTI) framework, we identify the key drivers of financial vulnerability and quantify the impact of housing cost shocks.

Our findings highlight the disproportionate burden faced by mortgage-exposed and working-age households.


---
## 2. Define Financial Resilience
We measure financial resilience using：

### 🔹 Debt-to-Income Ratio (DTI)

$$
DTI = \frac{Total\ Debt}{Annual\ Income}
$$

### Where:

**Total Debt includes:**
- Mortgage debt 
- Student loan debt 
- Credit card debt 
- Other personal loans 

**Annual Income refers to:**
- After-tax annual income 

### 🔹 Interpretation of DTI

The Debt-to-Income Ratio (DTI) measures how much of an individual’s income is used to pay debt obligations.

- A higher DTI suggests higher financial burden  
- A lower DTI indicates stronger financial stability  
 
---

## 3. Analytical Direction

We aim to quantify which financial and demographic variables most strongly predict:

- financial resilience (short-term financial stress)

### Potential Predictors:

- Age Group 
- Education Level 
- Family Type 
- Home Ownership 
- Work Status 2022 
- Number of Earners
- Bank Deposits 

---

## 4. Methodology Overview

### Step 1: Data Cleaning
- Remove negative DTI values  
- Remove infinite DTI values  
- Check missing values  

### Step 2: Feature Engineering
- Calculate Total Debt  
- Compute DTI  
- Create Financial Resilience categories  

### Step 3: Exploratory Data Analysis
- DTI distribution  
- Compare stress vs non-stress groups  
- Correlation analysis  

### Step 4: Modeling
- Linear regression  
- Feature importance analysis

### Step 5: Visualization
- Bar charts of key variables vs resilience categories
- Boxplots for top 2 influential variables
- DTI distribution histogram
- Shock simulation comparison plots

---

### Key Findings

- 1️⃣ Housing Tenure is the Strongest Predictor
Mortgage-exposed households exhibit significantly higher DTI levels and are more sensitive to financial shocks.

- 2️⃣ Working-Age Households Carry Higher Debt Burdens
Individuals aged 25–54 show elevated financial vulnerability relative to older households.

- 3️⃣ Risk Compounds Across Multiple Factors
Financial stress emerges from layered risk exposure rather than single-variable effects

## Shock Simulation

We simulate a 10% rent increase to evaluate resilience sensitivity.

Results show a measurable increase in the proportion of at-risk households, highlighting structural housing cost exposure.

---

## Policy Recommendations

### Target Mortgage-Exposed Households
- Temporary mortgage deferrals during income shocks
- Structured refinancing for high-DTI borrowers

### Strengthen Financial Buffers for Working-Age Households
- Automatic emergency savings programs
- Matched savings incentives

### Implement Multi-Factor Risk Screening
- Combine DTI, housing tenure, age, and debt composition
- Enable proactive intervention before financial distress escalates


## Conclusion

Financial resilience is structurally driven.  
Targeted, data-informed interventions can significantly reduce systemic financial vulnerability

---

## 5.Tech Stack

- **Language:** Python 3 （Jupyter Notebook）
- **Architecture:** Notebook-based data analysis pipeline (EDA → feature engineering → linear regression modeling → visualization)
- **Key libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn

---

## 6.Project Structure

```text
datathon/
│
├── main.ipynb                         # Main analysis notebook
├── Personal Finance Case.pdf          # Case description
├── personal_finance_dataset(origin).xlsx         # Case data with description
├── personal_finance_dataset(without...).xlsx     # Pure case data
└── README.md
```

---

## 7.Run

### Prerequisites

- python 3.x
- Jupyter Notebook
- You may use Anaconda or pip

### Clone

```bash
git clone https://github.com/AnnieQiulq/datathon.git
cd datathon
```

### Instal

Before running the notebook, install the required packages
- Option 1: Using pip
  ```bash
  pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
  ```
- Option 2: Using Anaconda
  ```bash
  conda install pandas numpy matplotlib seaborn scikit-learn openpyxl
  ```

### Run

From the project root:

```bash
jupyter notebook
```
- Open main.ipynb, then select Restart & Run All to reproduce the full analysis.

---

## 8.AI Tool Usage

We used ChatGPT for code assistance and debugging.

---

## 9.License

**All rights reserved. No license granted.**

