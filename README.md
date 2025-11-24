# Titanic-Dataset-Analysis
🛳️ Titanic Dataset — Exploratory Data Analysis (EDA)

This repository contains a complete exploratory data analysis of the Titanic dataset using Python.
The goal of the project is to understand the data, build helpful features, and visualize key patterns that influenced passenger survival.
This project is part of my personal learning and portfolio in data analytics.

📌 Project Overview

This analysis covers the full EDA workflow, including:
Inspecting the dataset
Cleaning and preparing data
Creating new features (AgeGroup, FamilySize)
Exploring relationships between features and survival
Building clear and informative visualizations
Summarizing insights in a structured report
The full written analysis (PDF) is also included in the repository.


_**📚 Libraries Used**_
pandas
numpy
matplotlib
seaborn

**🧹 Data Preparation**
The following steps were taken before analysis:

**1. Loading the dataset**
data_df = pd.read_csv("titanic.csv")

**2. Checking missing values**
data_df.isna().sum()

* Age: many missing
* Embarked: few missing
* Cabin: mostly missing

**3. Creating new features**
_**AgeGroup**_
bins = [0, 12, 17, 30, 50, 80]
labels = ['Child', 'Teen', 'Young Adult', 'Adult', 'Senior']
data_df['AgeGroup'] = pd.cut(data_df['Age'], bins=bins, labels=labels)


_**FamilySize**_
data_df['FamilySize'] = data_df['SibSp'] + data_df['Parch'] + 1

📊 Visualizations
**Survival by Sex**
Reveals strong survival advantage for females.
**Survival by Passenger Class**
First-class passengers survived more; third-class the least.
**Embarked vs Survival**
Cherbourg passengers have the highest survival rates.
**AgeGroup vs Survival**
Children survive more; seniors the least.
**Pclass × AgeGroup × Survival (Stacked Chart)**
Shows how age and class interact together.
**Correlation Heatmap**
Highlights Fare–Pclass relationship; other correlations are weak.
**Family Size Analysis**
Family sizes of 2–4 have the highest survival rates; solo travelers and large families have lower survival.

**🧠 Key Insights**
- Gender is the strongest predictor of survival.
- Higher passenger class means higher survival.
- Age groups show clear differences — children favored, seniors most vulnerable.
- Fare reflects socioeconomic status and survival chances.
- Embarkation port ties back to class distribution.
- Family size has a non-linear relationship with survival.

📄 Report

A detailed 2-page written report is included in the repository (report.pdf) summarizing all findings.

🎯 Future Improvements

Build a simple logistic regression survival prediction model

Add SHAP/LIME explanations

Create interactive dashboards (Streamlit, Plotly)

Implement advanced feature engineering

✨ About This Project

This EDA project is part of my personal data analytics learning journey.
It is designed to show clear, structured thinking, clean code, and effective visualization.
