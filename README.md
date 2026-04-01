# 🚢 Titanic Dataset Analysis
### Central Tendency: Mean, Median & Mode

<div align="center">

![Python](https://img.shields.io/badge/Python-3.13-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Dataset_&_Viz-4C72B0?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

**Author:** Akmal Raxmatov &nbsp;|&nbsp; **Dataset:** 891 Passengers · 15 Features &nbsp;|&nbsp; **Status:** ✅ Complete

</div>

---

## 🎯 Project Overview

This project explores the **three fundamental measures of central tendency** — Mean, Median, and Mode — using the classic Titanic passenger dataset. By applying these concepts to real historical data, we move beyond theory and into practical statistical interpretation.

> *"The Titanic dataset isn't just a dataset — it's a story told through numbers."*

---

## 📊 Statistical Concepts Covered

| Concept | Formula | Best Used When |
|:---|:---:|:---|
| **Mean** | $\bar{x} = \frac{\sum x_i}{n}$ | Data is symmetric, no extreme outliers |
| **Median** | Middle value in sorted data | Data is skewed (e.g., fare prices) |
| **Mode** | Most frequently occurring value | Categorical or discrete data |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Python 3.13** | Core language |
| **Pandas** | Data loading and manipulation |
| **Seaborn** | Built-in Titanic dataset + visualization |
| **Matplotlib** | Chart customization |
| **Jupyter Notebook** | Interactive analysis environment |

---

## 📁 Project Structure

```
titanic-statistics/
│
├── notebooks/
│   └── o_rtacha_moda_mediana.ipynb    # Main analysis notebook
│
├── visuals/
│   └── titanic_analysis.png           # 4-panel statistical chart
│
├── requirements.txt
└── README.md
```

---

## 🔬 Analysis Results

### Passenger Age

```python
df = sns.load_dataset('titanic')

mean_age   = df['age'].mean()     # → 29.70 years
median_age = df['age'].median()   # → 28.00 years
mode_age   = df['age'].mode()[0]  # → 24.00 years
```

| Metric | Value | Interpretation |
|:---|:---:|:---|
| **Mean** | 29.70 years | Average age across all passengers |
| **Median** | 28.00 years | The "middle" passenger was 28 years old |
| **Mode** | 24.00 years | Most common age on board |

> **Key Insight:** Mean > Median > Mode — this tells us the age distribution is **right-skewed**. A small number of older passengers pull the average upward, while the majority of passengers were in their mid-20s.

---

### Ticket Fare

```python
mean_fare   = df['fare'].mean()     # → $32.20
median_fare = df['fare'].median()   # → $14.45
mode_fare   = df['fare'].mode()[0]  # → $8.05
```

| Metric | Value | Interpretation |
|:---|:---:|:---|
| **Mean** | $32.20 | Pulled up by expensive 1st-class tickets |
| **Median** | $14.45 | Most passengers paid far less than average |
| **Mode** | $8.05 | The single most common ticket price |

> **Key Insight:** The dramatic gap between Mean ($32.20) and Median ($14.45) is a classic sign of **heavy right skew** — a few wealthy 1st-class passengers significantly distort the average. The Median is a far more representative measure here.

---

### Survival by Passenger Class

| Class | Survival Rate |
|---|---|
| 1st Class | **62.9%** |
| 2nd Class | **47.3%** |
| 3rd Class | **24.2%** |

---

## 📈 Visualizations

The notebook generates a 4-panel analysis chart covering:

1. **Age Distribution** — Histogram + KDE with Mean/Median/Mode markers
2. **Fare Distribution** — Right-skewed distribution showing economic inequality
3. **Survival Rate by Class** — Bar chart highlighting class disparities
4. **Age by Gender** — Boxplot comparing male vs. female age distributions

---

## 💡 Key Takeaways

**1. When to use the Median over the Mean:**
For skewed data like income or fare prices, the Median better represents the "typical" value. The Titanic fare data is a perfect real-world example of this principle.

**2. Mean, Median, Mode relationship reveals distribution shape:**

```
Mean ≈ Median ≈ Mode  →  Symmetric (normal) distribution
Mean > Median > Mode  →  Right-skewed  ← Titanic age & fare
Mean < Median < Mode  →  Left-skewed
```

**3. Missing data affects central tendency:**
The age column has 177 missing values (19.9%). All measures are calculated on the available 714 records — an important caveat for any real-world analysis.

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/titanic-statistics.git
cd titanic-statistics

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the notebook
jupyter notebook notebooks/o_rtacha_moda_mediana.ipynb
```

---

## 📦 requirements.txt

```
pandas>=2.0.0
seaborn>=0.12.0
matplotlib>=3.7.0
jupyter>=1.0.0
```

---

## 🔭 Next Steps

- [ ] Add dispersion analysis: Variance, Standard Deviation, IQR
- [ ] Explore fare distribution segmented by passenger class
- [ ] Visualize survival rates by age group
- [ ] Introduce the skewness coefficient ($g_1$)

---

## 👤 Author

**Akmal Raxmatov**
- 📍 Uzbekistan
- 🎓 Prospective student — International Economics (UWED, 2026)
- 📊 Focus: Statistics, Data Analytics, Python

---

## 📄 License

Open-source under the [MIT License](LICENSE).

---

<div align="center">
  <sub>891 passengers · 15 features · 3 measures · infinite stories</sub>
</div>
