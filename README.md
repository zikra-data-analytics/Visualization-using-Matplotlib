# Visualization-using-Matplotlib
Library - Matplotlib, Seaborn

# 📊 Data Visualization with Python

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?style=flat)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-teal?style=flat)
![Status](https://img.shields.io/badge/Status-In%20Progress-green?style=flat)

A collection of Python data visualization projects using **Matplotlib** and **Seaborn** — covering chart types, customizations, and real-world data storytelling.

---

## 🗂️ Projects Covered

| # | Notebook | Charts Used | Description |
|---|----------|-------------|-------------|
| 1 | `lineplot_practice.ipynb` | Line Plot | Weekly sales trend, multi-city temperature comparison |
| 2 | `barplot_practice.ipynb` | Bar Plot | Student marks comparison, conditional coloring |
| 3 | `scatterplot_practice.ipynb` | Scatter Plot | Relationship between Maths & Science marks |
| 4 | `fruit_sales_comparison.ipynb` | Multi-Line Plot | Weekly sales of Mango, Apple & Guava |

---

## 📈 Charts Covered

- ✅ **Line Plot** — Trends over time, multi-line comparison
- ✅ **Bar Plot** — Category comparison, conditional coloring (pass/fail)
- ✅ **Scatter Plot** — Relationship between two variables
- 🔄 **Histogram** — Distribution of data *(coming soon)*
- 🔄 **Box Plot** — Spread and outliers *(coming soon)*
- 🔄 **Heatmap** — Correlation matrix *(coming soon)*

---

## 🛠️ Tools & Libraries

```python
import matplotlib.pyplot as plt   # Core plotting library
import seaborn as sns              # Statistical visualization
import matplotlib.patches as mpatches  # Custom legends
```

**Environment:** Google Colab / Anaconda + VS Code
**Language:** Python 3.x

---

## 💡 Key Concepts Practiced

- Chart customization — colors, markers, linestyles, labels
- Conditional coloring using list comprehension
- Adding value labels with `plt.bar_label()` and `plt.text()`
- Custom legends using `matplotlib.patches`
- Background styling with `plt.gca().set_facecolor()`
- Axis limits with `plt.xlim()` / `plt.ylim()`
- Multi-chart layout using `plt.subplot()`

---

## 🚀 How to Run

1. Clone this repository
```bash
git clone https://github.com/your-username/data-visualization.git
```

2. Open any `.ipynb` file in Jupyter / VS Code / Google Colab

3. Run all cells — no additional installation needed if using Anaconda or Colab

---

## 📌 Sample Visualizations

### Weekly Sales — Line Plot
```python
days  = ["Mon", "Tue", "Wed", "Thur", "Fri", "Sat", "Sun"]
sales = [20, 92, 320, 186, 75, 89, 65]

plt.plot(days, sales, marker="o", color="black",
         linestyle="dashed", markersize=10,
         markerfacecolor="green", markeredgecolor="yellow")
plt.title("Days vs Sales of a Product")
plt.xlabel("Days")
plt.ylabel("Sales")
plt.grid()
plt.show()
```

### Student Marks — Conditional Bar Plot
```python
# Green = Pass (marks > 50), Red = Fail (marks < 50)
colors = ["green" if m > 50 else "red" for m in marks]
bars = plt.bar(students, marks, color=colors, edgecolor="black")
plt.bar_label(bars)
```

---

## 🙋 About

**Zikra Shaikh** — Aspiring Data Scientist | Python & SQL Enthusiast

📌 [LinkedIn] (www.linkedin.com/in/zikra-shaikh) | 🐙 [GitHub](https://github.com/zikra-data-analytics)

---

*This repository is actively updated as part of my Data Science learning journey.*
