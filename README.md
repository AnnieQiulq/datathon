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
- Number of Earners (Number of Earners)
- Bank Deposits (PWASTDEP)

---

## 5. Methodology Overview

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

---

## 4.Tech Stack

- **Language:** Python 3 （Jupyter Notebook）
- **Architecture:** Notebook-based data analysis pipeline (EDA → feature engineering → linear regression modeling → visualization)
- **Key libraries** pandas, numpy, sklearn, matplotlib, seaborn

---
以上已修改
## 5.Project Structure

```text
SmartCalendar/
├─ core/
│  ├─ src/main/java/
│  │  ├─ entity/
│  │  ├─ use_case/
│  │  ├─ data_access/
│  │  └─ interface_adapter/
│  └─ pom.xml
├─ app-fx/
│  ├─ src/main/java/com/smartcalendar/fx/
│  │  ├─ App.java
│  │  └─ MainController.java (and other controllers)
│  ├─ src/main/resources/com/smartcalendar/fx/
│  │  ├─ MainView.fxml
│  │  ├─ LoginView.fxml
│  │  ├─ SignupView.fxml
│  │  └─ style.css
│  └─ pom.xml
├─ pom.xml          # Parent POM (aggregates modules)
└─ README.md
```

---

## 6.Build & Run

### Prerequisites

- **JDK 21** installed.
- Maven installed or integrated in your IDE (IntelliJ IDEA recommended).
- JavaFX available via the **javafx-maven-plugin** (configured in `app-fx/pom.xml`).

### Clone

```bash
git clone https://github.com/JacobChan182/SmartCalendar.git
cd SmartCalendar
```

### Build

From the project root:

```bash
mvn clean install -DskipTests
```

This builds both `core` and `app-fx`.

### Run (Maven)

From the project root:

```bash
mvn -pl app-fx -am javafx:run
```

- `-pl app-fx` – run only the JavaFX module.
- `-am` – build dependencies (e.g. `core`) automatically.

### Run (IDE)

- Import the project as a **Maven project**.
- Set the run configuration to:
    - Module: `app-fx`
    - Main class: `com.smartcalendar.fx.App`
- Run.

---

## 9.Contribution Guidelines

- Use feature branches (e.g. `feat/edit-event-ui`, `feat/weather-panel`).
- Keep commits focused and descriptive (e.g., `feat: add edit event dialog`).
- Run `mvn test` before opening a pull request.
- For UI changes, include a short description and, if possible, a screenshot.

---

## 10.License

**All rights reserved. No license granted.**

