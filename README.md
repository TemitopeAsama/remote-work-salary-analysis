# Remote Work & Salary Analysis

---

Analyzing whether remote work status predicts developer salary, using the Stack Overflow Developer Survey.


## Motivation

---

Remote work has become increasingly common in software development, and this analysis aims to explore how work arrangement (remote, hybrid, or in-person) affects compensation. This project explores that question using real survey data from the Stack Overflow Developer Survey, following the CRISP-DM process (Business Understanding, Data Understanding, Data Preparation, Modeling, Evaluation, and Deployment) to investigate whether remote work status can meaningfully predict developer salary.

## Libraries Used

---

- `pandas` — data loading and manipulation
- `numpy` — numerical operations, log transformation
- `matplotlib` / `seaborn` — data visualization
- `scikit-learn` — encoding, train/test splitting, model training, and evaluation

## Files in the Repository

---

- `remote_work_salary_analysis.ipynb` — the full analysis notebook, including exploratory data analysis, data cleaning, model training, evaluation, and a prediction scenario
- `README.md` — this file

## Summary of Results

---

After cleaning the data (removing missing values and filtering statistical outliers in salary), I trained a linear regression model using `RemoteWork` status as the sole predictor of log-transformed salary (`ConvertedCompYearly`). Key findings:

- **In-person workers** show the lowest predicted salary of all groups, notably below every remote/hybrid category.
- **Fully remote workers** show the highest predicted salary, slightly above the baseline hybrid group.
- However, `RemoteWork` status alone explains only about **3.6% of the variation in salary** (R² = 0.036), meaning remote work status has a real but small relationship with compensation — the majority of what drives developer salary lies in other factors (experience, role, education, location, etc.) not captured in this analysis.

Full details on the data cleaning decisions, model coefficients, and evaluation metrics are documented in the notebook.

## Acknowledgments

---

- Data provided by the [Stack Overflow Developer Survey](https://survey.stackoverflow.co/)
- Built as part of the Udacity Data Science Nanodegree Program.