# 🚁 UAV Propeller Performance Analysis

This capstone project aims to improve the performance prediction of propellers used in small UAVs (Unmanned Aerial Vehicles). By applying data-driven techniques and machine learning models, we investigate how blade geometry and operational parameters influence thrust, power, and efficiency.

---

## 📌 Business Problem

The increasing demand for UAVs in both civilian and military domains requires optimization of propulsion systems. Propeller performance must balance size, weight, and aerodynamic efficiency. This project uses experimental and geometric data to build predictive models that can support design optimization.

---

## 🎯 Objectives

- Merge and preprocess multi-source propeller data.
- Compute important engineering parameters like solidity, blade area, disc area, etc.
- Visualize key performance variables and detect correlations.
- Build machine learning models to predict:
  - Thrust Coefficient
  - Power Coefficient
  - Efficiency

---

## 📂 Dataset Overview

### 1. Experiment Data
Files: `Experiment_vol1.xlsx`, `Experiment_vol2.xlsx`, `Experiment_vol3.xlsx`  
**Features**:
- Propeller name, brand, diameter, pitch
- Advanced ratio, RPM
- Thrust coefficient, power coefficient, efficiency

### 2. Geometry Data
Files: `Geom_vol1.xlsx`, `Geom_vol2.xlsx`, `Geom_vol3.xlsx`  
**Features**:
- Blade name, chord-radius distribution (c/R)
- Beta angle (blade angle relative to rotation)
- Propeller pitch and diameter

---

## ✅ Tasks Completed

### 📊 Data Preprocessing
- Combined and cleaned experimental + geometry datasets
- Renamed columns to follow Python conventions
- Generated:
  - Chord and radius distributions
  - Blade area (via trapezoidal integration)
  - Disc area and solidity ratio
- Merged computed solidity back with experimental data

### 📉 Exploratory Analysis
- Checked for missing values and outliers
- Created:
  - Bivariate analysis plots
  - Heatmap of correlation matrix
- Compared performance across brands, blades, and configurations

### 🤖 Machine Learning
- Built Gradient Boosting Regressors for each performance metric
- Compared 3 model variants:
  1. Without missing value imputation
  2. With imputation
  3. Without using solidity as a feature
- Evaluated using RMSE and visual plots
- Models trained specifically on **2-blade propellers**, then tested on others

### 🧾 SQL Analysis
- Filtered high-performing propellers (>12% thrust coefficient)
- Ranked propellers by efficiency
- Identified worst-performing 100 based on power coefficient
- Counted zero/negative-efficiency cases in combined dataset

### 📊 Tableau Dashboard
- Developed a multi-chart dashboard showing:
  - Performance comparisons across propeller brands
  - Efficiency vs Solidity trade-offs
  - Outliers and risky designs
- Focused on data storytelling

---

## 📁 Repository Structure

```

📁 data/
Experiment\_vol\*.xlsx
Geom\_vol\*.xlsx

📁 notebooks/
Data\_Cleaning.ipynb
Feature\_Engineering.ipynb
Modeling.ipynb
SQL\_Tasks.sql
Tableau\_Snapshots/

📄 README.md
📄 requirements.txt

```

---

## 🔧 Tech Stack

- **Python** (Pandas, NumPy, Seaborn, Matplotlib, Scikit-Learn)
- **SQL** (SQLite or Pandasql for querying)
- **Tableau** for storytelling dashboards
- **Jupyter Notebooks** for iterative development

---

## 👤 Author

**Faizan Malik**  
- 📧 [faizanmalikmmm@gmail.com](mailto:faizanmalikmmm@gmail.com)  
- [GitHub](https://github.com/faizanmal) | [LinkedIn](https://www.linkedin.com/in/faizanmalikdelhi)

---

## 🎓 Note

This project was completed as part of the Post Graduate Certificate in Data Science from IIT Kanpur.
