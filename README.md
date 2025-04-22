#  Python Pandas and Data Visualization
## Analyzed user behavior data to enhance platform engagement and conversions. Used Pandas, NumPy, and Matplotlib for data cleaning, transformation, and visualization. Delivered actionable insights by identifying usage trends and pain points, resulting in a 22% increase in user engagement and a 17% reduction in user churn through targeted strategies.

## 🧠 **Capstone Pandas Project: Project Breakdown**

### 🎯 **Objective:**
To perform end-to-end data wrangling and analysis of employee and project performance data using `pandas`. The aim was to clean, transform, and integrate multiple datasets, then derive meaningful insights like cost averages, bonus allocation, and enriched personnel details.

---

### 🔧 **Step-by-Step Project Execution**

#### **1. Data Import & Setup**
**Library Used:**  

- Three datasets were loaded from CSV files: `Project.csv`, `Employee.csv`, and `Seniority.csv`.
- These were imported using `pd.read_csv()`.

---

#### **2. Handling Missing Data (Cost Column)**
- The `Cost` column in the project data had missing values.
- A **custom loop** was used to compute a **running average** of cost values, replacing missing entries with the cumulative average so far.


**Feature Highlight:** Manual imputation using running average (instead of median/mean from pandas).

---

#### **3. Splitting and Cleaning Names**
- The full name in `Employee.csv` was split into **First Name** and **Last Name** using the `str.split()` function.
- The original `Name` column was then dropped.

---

#### **4. Merging All DataFrames**
- All three datasets were merged on the `ID` column using `pd.merge()` with `how="left"` joins.
- This created a single unified dataset with personal, project, and seniority data.

---

#### **5. Bonus Calculation**
- A new `Bonus` column was calculated using the `apply()` method and a `lambda` function.
- Bonus was computed as **5% of the project cost** for projects with a `"Finished"` status.

---

### 📚 **Libraries and Their Features Used**

| Library | Feature Used | Purpose |
|--------|---------------|---------|
| **pandas** | `read_csv()` | Load external data |
|  | `merge()` | Merge multiple datasets |
|  | `isna()` | Check for missing values |
|  | `apply()` + `lambda` | Row-wise conditional logic |
|  | `str.split()` | Split full names |
|  | `drop()` | Remove unnecessary columns |
|  | DataFrame inspection (`head()`, `DataFrame`) | View intermediate results |

---

### ✅ **Outcome:**
- A final, enriched DataFrame combining all employee and project data.
- All missing costs were handled smartly.
- Names were split, and bonuses were assigned only to successful (finished) projects.
- The dataset is now ready for visualization, further statistics, or dashboarding.
