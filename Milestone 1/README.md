# Milestone 1 — Data Preprocessing & Exploratory Data Analysis

A concise summary of the steps taken to preprocess student performance data and perform exploratory data analysis (EDA). This milestone prepares the data for later modeling and recommender-system work.

---

## Table of contents
- [Objective](#objective)
- [Tools & environment](#tools--environment)
- [Dataset](#dataset)
- [Methodology](#methodology)
  - [1. Data merge](#1-data-merge)
  - [2. Data preprocessing](#2-data-preprocessing)
  - [3. Descriptive analysis](#3-descriptive-analysis)
  - [4. Exploratory data analysis (EDA)](#4-exploratory-data-analysis-eda)
- [Key insights](#key-insights)
- [Visualizations produced](#visualizations-produced)

---

## Objective
Preprocess student performance data and perform Exploratory Data Analysis (EDA) to:
- understand the dataset,
- detect patterns and outliers,
- prepare clean, encoded and scaled data for subsequent machine learning tasks (prediction, recommendations).

---

## Tools & environment
- Python 3.x
- Google Colaboratory (used for analysis)
- Libraries:
  - pandas, numpy
  - matplotlib, seaborn
  - scikit-learn

---

## Dataset
Source: Kaggle — [Student Performance for Recommender Systems](https://www.kaggle.com/datasets/rodrigotertulino/student-performance-for-recommender-systems)

The dataset was split into two CSV tables for this milestone:
- `Table1.csv`
- `Table2.csv` 

Join key: `student_id`

---

## Methodology

### 1. Data merge
- Imported `Table1.csv` and `Table2.csv` using pandas.
- Performed an inner merge on `student_id` to obtain a consolidated dataset.

### 2. Data preprocessing
- Missing values:
  - Numeric columns: imputed with column mean.
  - Categorical columns: imputed with column mode.
- Removed duplicate rows.
- Fixed data types:
  - Numeric columns → `int`/`float`
  - Categorical columns → `category`
  - IDs → `string`
- Encoded categorical variables using label encoding or one-hot encoding as appropriate.
- Normalized numeric columns using `StandardScaler` for comparability.

### 3. Descriptive analysis
- Generated summary statistics: mean, median, standard deviation.
- Computed correlation matrix for numeric features to identify relationships.
- Detected outliers using the IQR (Interquartile Range) method.
- Checked categorical distributions to detect class imbalance in gender, program, and performance labels.

### 4. Exploratory data analysis (EDA)
- Value distributions : histograms for numeric features and countplots for categorical features.
- Relationship plots :  barplots to investigate feature interactions.
- Correlation heatmap to visualize numeric correlations.
- Pattern analysis : relationship between engagement metrics (e.g., `total_logins`) and performance (`final_exam_score`).

---

## Key insights
1. The target `performance_label` distribution is imbalanced; most students are in category 0.
2. `quiz_scores_avg` shows a strong positive correlation with `final_exam_score`.
3. Outliers are present in `avg_session_duration` and `total_logins` (IQR-detected).
4. Gender and program distributions are slightly imbalanced but generally not extreme.
5. Higher engagement (more logins, longer session durations) tends to correlate with better exam performance.

---

## Visualizations produced
- Histograms (value distributions for numeric features)
- Barplots 
- Correlation heatmap
- Engagement vs performance plots (e.g., `total_logins` vs `final_exam_score`)

(Visualization files or notebook cells with the plots should be located in the Milestone 1 folder or the analysis notebook.)


