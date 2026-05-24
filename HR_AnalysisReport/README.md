# 📊 HR Employee Attrition & Salary Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Plotting-11557c)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📌 Project Overview

This project performs an exploratory data analysis (EDA) and visualization study on an HR employee dataset of **14,999 records**. The goal is to uncover patterns behind employee attrition, salary distribution, and workplace factors — insights that can help organizations reduce employee turnover and improve workforce planning.

---

## 🗂️ Dataset

| Property | Details |
|---|---|
| **Source** | HR Employee Dataset (CSV) |
| **Rows** | 14,999 employees |
| **Columns** | 10 features |
| **Missing Values** | None |
| **Duplicates** | Detected and removed |

### 📋 Column Description

| Column | Type | Description |
|---|---|---|
| `satisfactoryLevel` | float | Employee satisfaction score (0–1) |
| `Performance` | float | Last performance evaluation score (0–1) |
| `numberOfProjects` | int | Number of projects handled |
| `avgMonthlyHours` | int | Average monthly working hours |
| `timeSpent.company` | int | Years spent at the company |
| `workAccident` | int | Whether employee had a work accident (0/1) |
| `left` | int | Whether employee left the company (0/1) |
| `promotionInLast5years` | int | Whether employee was promoted in last 5 years (0/1) |
| `dept` | object | Department name |
| `salary` | object | Salary level — low / medium / high |

---

## 🎯 Objectives

- Understand the distribution of employees across departments and salary bands
- Identify which factors are most strongly associated with employees leaving
- Analyze the relationship between workload, satisfaction, and attrition
- Derive actionable business insights from visual patterns

---

## 🔍 Key Analyses Performed

### 1. 📦 Data Cleaning & EDA
- Shape, dtypes, null check, duplicate removal
- Column rename: `lastEvaluation` → `Performance`
- Value counts for salary and department

### 2. 📁 Projects vs Attrition
- Employees with **2 projects** had a high leaving rate
- Employees with **3–4 projects** showed the most stability
- Employees handling **7 projects** almost entirely left — indicating severe overload

### 3. 🏢 Department vs Salary
- `Management` and `RandD` have the highest proportion of high-salary employees
- `Sales` and `Support` — despite being the largest departments — are heavily skewed toward low salary
- Nearly **49% of the entire workforce** earns low salary; only **8.2%** earn high salary

### 4. 🚪 Department vs Attrition
- Department alone is **not a strong predictor** of attrition
- Leaving rates are distributed fairly evenly across all departments
- Sales has the highest absolute number of leavers due to its large size

### 5. 💰 Salary vs Attrition
- Low-salary employees leave the most — a clear and strong signal
- High-salary employees show significantly lower attrition

### 6. 🏅 Promotion vs Attrition
- Employees who were **not promoted** in the last 5 years leave at a much higher rate
- Promotion (or lack thereof) is a key driver of attrition

### 7. 😊 Satisfaction Level vs Attrition
- Employees who left show a notably **lower satisfaction score**
- Two distinct groups of leavers: very dissatisfied AND overworked-but-once-satisfied employees

### 8. ⚠️ Work Accident vs Attrition
- Employees who experienced work accidents tend to **stay** — possibly due to dependency or ongoing recovery

### 9. ⏱️ Monthly Hours vs Satisfaction
- Employees working **250+ hours/month** with low satisfaction are the highest-risk group for leaving
- This scatter plot reveals the most powerful combined insight in the dataset

---

## 📈 Visualizations Used

| Chart Type | Purpose |
|---|---|
| `sns.countplot()` | Compare categorical distributions |
| `sns.barplot()` | Department vs salary comparison |
| `sns.heatmap()` | Salary % heatmap by department |
| `sns.histplot()` | Satisfaction level distribution |
| `sns.scatterplot()` | Hours vs satisfaction (colored by attrition) |
| `plt.pie()` | Proportional breakdowns |
| `plt.subplots()` | Side-by-side comparison charts |
| `pd.crosstab()` | Normalized % tables |

---

## 💡 Key Findings & Conclusions

> **Top 3 drivers of employee attrition:**
> 1. **Low salary** — the single strongest predictor
> 2. **No promotion in 5 years** — employees feel stagnant
> 3. **Overwork + low satisfaction** — working 250+ hours/month with low morale

> **Department is NOT a major factor** in attrition — the distribution of leavers is relatively uniform across departments.

> **Management earns the best** — highest proportion of high-salary employees despite being the smallest department.

---

## 🛠️ Tech Stack

```
Python 3.x
├── pandas       — data loading, cleaning, EDA
├── numpy        — numerical operations
├── matplotlib   — base plotting
└── seaborn      — statistical visualizations
```

---

## 🚀 How to Run

1. **Clone the repository**
```bash
git clone https://github.com/zikra-data-analytics/hr-analysis-visualization.git
cd hr-analysis-visualization
```

2. **Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. **Launch the notebook**
```bash
jupyter notebook HR_Analysis.ipynb
```

4. **Update the file path** in Cell 2 to point to your local CSV file:
```python
df = pd.read_csv(r"your\path\to\people.csv")
```

---

## 📁 Project Structure

```
hr-analysis-visualization/
│
├── HR_Analysis.ipynb          # Main analysis notebook
├── people.csv                 # Dataset (not included — see note below)
└── README.md                  # Project documentation
```

> ⚠️ **Note:** The dataset file is not included in this repository. You can use any HR employee dataset with the same column structure.

---

## 🙋‍♀️ About

This project is part of my **Data Science & Analytics portfolio**, built while transitioning into the field. I am actively learning Python, data visualization, and machine learning — and documenting the journey publicly.

🔗 **GitHub:** [zikra-data-analytics](https://github.com/zikra-data-analytics)

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).
