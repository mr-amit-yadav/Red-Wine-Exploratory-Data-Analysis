# 🍷 Red Wine Exploratory Data Analysis

A comprehensive Exploratory Data Analysis (EDA) of the **Portuguese "Vinho Verde" Red Wine** dataset, examining physicochemical properties and their relationship to wine quality.

---

## 📌 Project Overview

This project performs an end-to-end EDA on the red wine quality dataset. The goal is to understand the distribution of features, identify correlations between physicochemical properties, and gain visual insights into what influences wine quality scores.

> The dataset is related to the red variant of the Portuguese "Vinho Verde" wine. Due to privacy and logistical reasons, only physicochemical (input) and sensory (output) variables are included — no data about grape types, wine brand, or selling price is available.

---

## 📂 Dataset

- **File:** `winequality-red.csv`
- **Source:** UCI Machine Learning Repository - [Wine Quality Dataset](https://archive.ics.uci.edu/ml/datasets/wine+quality)
- **Records:** 1,599 entries (before deduplication)
- **Type:** Can be treated as a classification or regression task

### Input Variables (Physicochemical Tests)
| # | Feature |
|---|---------|
| 1 | Fixed Acidity |
| 2 | Volatile Acidity |
| 3 | Citric Acid |
| 4 | Residual Sugar |
| 5 | Chlorides |
| 6 | Free Sulfur Dioxide |
| 7 | Total Sulfur Dioxide |
| 8 | Density |
| 9 | pH |
| 10 | Sulphates |
| 11 | Alcohol |

### Output Variable
| # | Feature |
|---|---------|
| 12 | Quality (score between 0 and 10) |

---

## 🔍 Analysis Performed

### 1. Data Loading & Inspection
- Loaded the dataset using `pandas`
- Inspected shape, column names, data types, and sample rows

### 2. Data Cleaning
- Checked for **missing values** — none found
- Identified and **removed duplicate records** using `drop_duplicates()`

### 3. Descriptive Statistics
- Generated summary statistics (`describe()`) for all features
- Examined unique quality score values

### 4. Correlation Analysis
- Computed pairwise feature correlations
- Visualized correlations using a **Seaborn heatmap**

### 5. Visualizations
- **Bar chart** - Distribution of wine quality scores (imbalanced dataset)
- **Histograms with KDE** - Distribution of each feature
- **Pairplot** - Multivariate relationships across all features
- **Box plot** - Alcohol content across quality categories
- **Scatter plot** - Alcohol vs. pH, colored by quality

---

## 🧰 Tech Stack

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading, cleaning, and analysis |
| `matplotlib` | Plotting and visualization |
| `seaborn` | Statistical data visualization |

---

## ⚠️ Key Observations

- The dataset is **imbalanced** — most wines are rated 5 or 6, with very few rated 3, 4, or 8.
- **Alcohol** shows a positive correlation with wine quality.
- **Volatile acidity** has a negative correlation with quality.
- Outlier detection algorithms could be used to identify exceptional or poor wines.
- Not all input variables may be relevant — feature selection methods are worth exploring.

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas matplotlib seaborn
```

### Run the Notebook
1. Clone the repository:
   ```bash
   git clone https://github.com/mr-amit-yadav/Red-Wine-Exploratory-Data-Analysis.git
   cd Red-Wine-Exploratory-Data-Analysis
   ```
2. Open the notebook:
   ```bash
   jupyter notebook Red_Wine.ipynb
   ```
3. Place `winequality-red.csv` in the same directory as the notebook.

---

## 📁 Repository Structure

```
Red-Wine-Exploratory-Data-Analysis/
│
├── Red_Wine.ipynb          # Main analysis notebook
├── winequality-red.csv     # Dataset (download separately)
├── README.md               # Project documentation
└── LICENSE                 # MIT License
```

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Amit Yadav**  
GitHub: [@mr-amit-yadav](https://github.com/mr-amit-yadav)
