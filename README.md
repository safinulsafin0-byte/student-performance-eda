# Student Performance — Exploratory Data Analysis

An exploratory data analysis project investigating factors associated with
students' final academic performance using the UCI Student Performance dataset.

## Project Overview

This project analyzes student academic performance and explores relationships
between final grades and different academic, demographic, behavioral, and
family-related factors.

The main target variable is:

- `G3` — Final grade

The analysis focuses on:

- Study time
- Previous failures
- Absences
- Gender
- School
- Internet access
- Parental education
- Alcohol consumption
- Academic grade progression
- Correlations between numerical variables

## Dataset

The project uses the Portuguese student dataset from the
UCI Student Performance dataset.

Dataset file:

`student-por.csv`

The dataset contains 649 student records and 33 attributes.

## Project Structure

```text
student-performance-eda/
│
├── data/
│   ├── raw/
│   │   ├── student-mat.csv
│   │   └── student-por.csv
│   │
│   └── processed/
│
├── notebooks/
│   └── 01_student_performance_eda.ipynb
│
├── figures/
│   ├── g3_distribution.png
│   ├── studytime_vs_g3.png
│   ├── failures_vs_g3.png
│   ├── absences_vs_g3.png
│   ├── gender_vs_g3.png
│   ├── school_vs_g3.png
│   ├── internet_vs_g3.png
│   ├── correlation_matrix.png
│   └── grade_progression.png
│
├── reports/
│   └── eda_summary.md
│
├── README.md
├── requirements.txt
└── .gitignore

Tools & Technologies
Python
Pandas
NumPy
Matplotlib
Seaborn
Jupyter Notebook
Analysis Workflow

The project follows a complete exploratory data analysis workflow:

Data loading
Dataset inspection
Data quality assessment
Missing-value analysis
Duplicate-value analysis
Descriptive statistics
Target variable analysis
Univariate analysis
Bivariate analysis
Correlation analysis
Feature engineering
Key findings
Limitations
Conclusion
Key Findings
Study Time

Students with higher study-time categories generally achieved higher
average final grades.

Previous Failures

Previous failures showed a relatively strong negative association with
final academic performance.

Students with no previous failures had substantially higher average
final grades.

Gender

Female students had a somewhat higher average final grade than male
students in this dataset.

School

Students from GP had a higher average final grade than students from MS.

Internet Access

Students with internet access had a higher average final grade than
students without internet access.

Parental Education

Higher parental education levels were generally associated with higher
average final grades.

Academic Progression

Average grades increased gradually across G1, G2, and G3.

Strongest Correlations

G1 and G2 showed the strongest correlations with G3.

However, these variables represent earlier academic grades, so their use
in predictive modeling depends on the intended prediction timing.

Important Note About Correlation

The relationships identified in this project are observational associations.

Correlation does not imply causation.

For example, a higher average grade among students with internet access
does not mean that internet access directly causes higher academic
performance.

Target Leakage Consideration

G1 and G2 are earlier academic grades and have very strong relationships
with G3.

If a future machine learning model is intended to predict final performance
before G1 and G2 become available, these variables should be excluded.

If prediction occurs after G1 and G2 are available, they may be valid
predictive features depending on the prediction scenario.

Limitations
The dataset represents students from Portuguese schools.
The findings may not generalize to other educational systems.
The analysis identifies associations rather than causal relationships.
Some variables are self-reported.
Several categorical groups contain relatively few observations.
The dataset is relatively small compared with real-world educational
datasets.
Future Work

Possible extensions include:

Statistical hypothesis testing
Regression analysis
Classification models
Final-grade prediction
Feature importance analysis
Model comparison
Cross-validation
Model explainability
Author

Safinul Islam

Computer Science & Engineering Student

License

This project is intended for educational and portfolio purposes.


---

# 2. `reports/eda_summary.md`

এটাও বানাও।

```markdown
# EDA Summary

## Dataset

Portuguese Student Performance Dataset

Rows: 649

Target: G3 (Final Grade)

## Main Findings

- Average final grade (G3): approximately 11.91
- Study time shows a positive association with G3.
- Previous failures show a negative association with G3.
- Female students have a somewhat higher average G3 than male students.
- GP students have a higher average G3 than MS students.
- Internet access is associated with higher average G3.
- Higher parental education is generally associated with higher G3.
- G1 and G2 have the strongest relationships with G3.

## Important Correlations

- G2 → G3: approximately 0.919
- G1 → G3: approximately 0.826
- Failures → G3: approximately -0.393
- Studytime → G3: approximately 0.250
- Dalc → G3: approximately -0.205
- Walc → G3: approximately -0.177

## Conclusion

The EDA identifies several academic, behavioral, demographic, and
family-related factors associated with final student performance.

The results provide a foundation for future statistical analysis and
machine learning experiments.