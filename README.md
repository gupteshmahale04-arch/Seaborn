
# 🌊 Seaborn Data Visualization 

Welcome to the structured reference guide and notebook repository for **Seaborn**, a high-level Python visualization library built on top of Matplotlib.  
This guide covers relational analysis, categorical comparisons, distribution visualizations, and regression/mixed plots.

---

## 📋 Table of Contents
- [🎨 What is Seaborn?](#-what-is-seaborn)
- [🚀 Installing & Importing Seaborn](#-installing--importing-seaborn)
- [📊 Class 1: Relational Plots](#-class-1-relational-plots)
- [🏷️ Class 2: Categorical Plots](#-class-2-categorical-plots)
- [📈 Class 3: Distribution Plots](#-class-3-distribution-plots)
- [📐 Class 4: Regression & Mixed Plots](#-class-4-regression--mixed-plots)
- [📂 Notebooks Directory](#-notebooks-directory)

---

## 🎨 What is Seaborn?
Seaborn is a **high-level data visualization library** built on top of Matplotlib.  
Key advantages include:
- ✨ Beautiful, modern default styles  
- 📝 Concise syntax requiring less code for complex visual charts  
- 🔗 Seamless integration with Pandas DataFrames  

It offers quick, attractive plots while preserving full customization power through Matplotlib.

---

## 🚀 Installing & Importing Seaborn

Install Seaborn with its dependencies:
```bash
pip install seaborn pandas matplotlib
```

Import in Python:
```python
import seaborn as sns
import matplotlib.pyplot as plt
```

---

## 📊 Class 1: Relational Plots
Relational plots show the relationship between two variables, focusing on how one continuous variable changes with respect to another.

**Key Plot Types**
- `scatterplot()` → Displays individual data points to reveal correlations and patterns  
- `lineplot()` → Shows continuous trends or summary lines  

**Examples**
```python
# Load sample dataset
tips = sns.load_dataset("tips")

# Scatter Plot with hue and style mapping
sns.scatterplot(data=tips, x="total_bill", y="tip", hue="smoker", style="smoker")
plt.show()

# Line Plot for continuous trends
sns.lineplot(data=tips, x="size", y="total_bill")
plt.show()
```

---

## 🏷️ Class 2: Categorical Plots
Categorical plots visualize datasets where at least one variable is categorical (e.g., day of the week, gender, class).

**Plot Type Guide**
| Function    | Best For |
|-------------|----------|
| `barplot()` | Comparing average values across categories |
| `countplot()` | Showing how many items fall into each category |
| `boxplot()` | Viewing median, quartiles, and statistical outliers |
| `violinplot()` | Displaying boxplot stats + distribution density |
| `stripplot()` | Viewing individual observations (small datasets) |
| `swarmplot()` | Individual observations without overlap |

**Examples**
```python
# Bar Plot comparing averages
sns.barplot(data=tips, x="day", y="total_bill", hue="sex")
plt.show()

# Box Plot for distribution and outliers
sns.boxplot(data=tips, x="day", y="total_bill")
plt.show()
```

---

## 📈 Class 3: Distribution Plots
Distribution plots illustrate how data values are spread, skewed, or concentrated.

**Key Plot Types**
- `histplot()` → Modern histogram (supports KDE overlays)  
- `kdeplot()` → Smooth curve depicting kernel density estimates  
- `rugplot()` → Tick marks highlighting raw observations  

⚠️ Note: `distplot()` is deprecated; use `histplot()` or `kdeplot()` instead.

**Examples**
```python
# Histogram with KDE curve
sns.histplot(data=tips, x="total_bill", kde=True, bins=15)
plt.show()

# Smooth density curve by category
sns.kdeplot(data=tips, x="total_bill", hue="time", fill=True)
plt.show()
```

---

## 📐 Class 4: Regression & Mixed Plots
Regression and mixed plots combine scatter relationships with statistical modeling or multiple plot types.

**Key Plot Types**
- `regplot()` / `lmplot()` → Scatter + fitted regression line (`lmplot` supports faceting)  
- `jointplot()` → Bivariate scatter + marginal histograms/KDE curves  
- `pairplot()` → Matrix of scatter plots and distribution curves  

**Examples**
```python
# Regression plot with faceting
sns.lmplot(data=tips, x="total_bill", y="tip", hue="smoker", col="time")
plt.show()

# Pairwise relationships matrix
sns.pairplot(tips, hue="sex")
plt.show()
```

---

## 📂 Notebooks Directory
- **Seaborn_class1.ipynb** → Introduction, dataset loading, `scatterplot()`, `lineplot()`  
- **Seaborn_class2.ipynb** → Categorical analysis: `barplot()`, `countplot()`, `boxplot()`, `stripplot()`, `swarmplot()`  
- **Seaborn_class3.ipynb** → Distribution analysis: `histplot()`, `kdeplot()`, `rugplot()`  
- **Seaborn_class4.ipynb** → Statistical models & multi-variable grids: `regplot()`, `lmplot()`, `jointplot()`, `pairplot()`  

---

📌 This README serves as a quick reference and structured learning path for mastering Seaborn visualizations.
```

Would you like me to also create a **GitHub-style badges section** (e.g., Python version, Seaborn version, license) at the top to make it look more professional?
