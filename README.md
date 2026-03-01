# 2026 Datathon -- Team 59
---

## 1.Overview
This project analyzes financial resilience using a personal finance dataset.
Our main objective is to understand how debt burden relative to income affects financial stability and short-term financial stress.

The key concept of this project is:
Debt-to-Income Ratio (DTI)


---
## 2. Define Financial Resilience

### 🔹 Debt-to-Income Ratio (DTI)

$$
DTI = \frac{Total\ Debt}{Annual\ Income}
$$

### Where:

**Total Debt includes:**
- Mortgage debt (PWDPRMOR)
- Student loan debt (PWDSLOAN)
- Credit card debt (PWDSTCRD)
- Other personal loans (PWDSTLOC)

**Annual Income refers to:**
- After-tax annual income (PEFATINC)

---

### 🔹 Interpretation of DTI

The Debt-to-Income Ratio (DTI) measures how much of an individual’s income is used to pay debt obligations.

- A higher DTI suggests higher financial burden  
- A lower DTI indicates stronger financial stability  

---

### 🔹 Financial Resilience Classification

We classify individuals based on DTI:

- **Thriving:** DTI < 0.2  
- **Coping:** 0.2 ≤ DTI < 0.5  
- **At Risk:** DTI ≥ 0.5  

**Alternative industry benchmark:**

- Low DTI (<30%) → Financially stable  
- High DTI (>40%) → Potential financial stress   

---

## 3. Analytical Direction

We aim to quantify which financial and demographic variables most strongly predict:

- financial resilience (short-term financial stress)

### Potential Predictors:

- Age Group (PAGEMIEG)
- Education Level (PEDUCMIE)
- Family Type (PFMTYPG) 
- Home Ownership (PFTENUR)
- Work Status 2022 (PLFFPTME)
- Number of Earners (PNBEARG)
- Bank Deposits (PWASTDEP)

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

## 8.License

**All rights reserved. No license granted.**

