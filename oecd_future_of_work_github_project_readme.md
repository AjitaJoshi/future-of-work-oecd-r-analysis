# Human Adaptation to Automation and Algorithmic Management in the Digital Economy
## A Comparative OECD Workforce Analytics Study

---

## Repository Description

Comparative workforce analytics project exploring automation, AI adoption, and algorithmic management across OECD countries using labour market and digital economy datasets. Focused on employment transformation, workforce inequality, digital skills, and the future of work through quantitative social science and data-driven research using R.

---

# Project Overview

This project explores how automation, AI adoption, and algorithmic management are reshaping employment, workforce inequality, and organisational systems across OECD countries.

Using publicly available OECD labour market and digital economy datasets, this study analyses workforce transformation, digital skills, automation exposure, and employment resilience within the context of the future of work.

The project combines workforce analytics, quantitative social science, and organisational research perspectives to understand how digital technologies are influencing professional work across industries and countries.

---

# Research Objectives

- Analyse automation impact across industries
- Explore workforce vulnerability to technological disruption
- Compare labour market trends across OECD countries
- Investigate relationships between digital skills and employment resilience
- Examine workforce inequality associated with digital transformation
- Explore implications of algorithmic and organisational management systems

---

# Research Questions

1. Which industries face the highest automation exposure across OECD economies?

2. How does automation affect employment trends and workforce stability?

3. What role do digital skills play in workforce resilience?

4. Are certain demographic groups disproportionately affected by automation?

5. How are AI-driven organisational systems reshaping professional work?

---

# Data Sources

## OECD Data Portal
https://data.oecd.org

Datasets include:
- Employment by industry
- Digital skills indicators
- Labour productivity
- ICT usage
- Gender employment gaps
- Workforce participation trends

---

# Tools Used

- RStudio
- tidyverse
- ggplot2
- dplyr
- readr
- Excel
- Power BI

---

# Analytical Methods

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Comparative Analysis
- Trend Analysis
- Workforce Analytics
- Data Visualisation

---

# Suggested Repository Structure

```text
future-of-work-oecd-r-analysis/
│
├── README.md
├── datasets/
│   ├── oecd_employment_data.csv
│   ├── digital_skills_data.csv
│   └── automation_risk_data.csv
│
├── scripts/
│   ├── data_cleaning.R
│   ├── exploratory_analysis.R
│   ├── visualisation_analysis.R
│   └── workforce_inequality_analysis.R
│
├── visualisations/
│   ├── automation_risk_plot.png
│   ├── employment_trends.png
│   ├── digital_skills_analysis.png
│   └── gender_gap_analysis.png
│
├── findings/
│   ├── key_findings.md
│   └── policy_implications.md
│
└── presentation/
    └── future_of_work_summary.pdf
```

---

# Example R Code

## Data Cleaning

```r
library(tidyverse)

employment_data <- read_csv("datasets/oecd_employment_data.csv")

# View structure
glimpse(employment_data)

# Remove missing values
employment_clean <- employment_data %>%
  drop_na()

# Save cleaned data
write_csv(employment_clean, "datasets/employment_clean.csv")
```

---

## Exploratory Analysis

```r
library(tidyverse)

employment_clean <- read_csv("datasets/employment_clean.csv")

industry_summary <- employment_clean %>%
  group_by(industry) %>%
  summarise(avg_employment = mean(employment_rate))

print(industry_summary)
```

---

## Data Visualisation

```r
library(tidyverse)

employment_clean <- read_csv("datasets/employment_clean.csv")

# Employment trends by industry

ggplot(employment_clean,
       aes(x = industry,
           y = employment_rate)) +
  geom_boxplot() +
  theme_minimal() +
  labs(
    title = "Employment Rate by Industry",
    x = "Industry",
    y = "Employment Rate"
  )
```

---

# Key Themes

- Automation and workforce transformation
- AI and organisational management
- Employment resilience
- Digital inequality
- Skills and employability
- Future of work research

---

# Public Good Contribution

This project contributes to discussions surrounding:
- ethical AI
- workforce wellbeing
- employment sustainability
- labour market inequality
- digital inclusion
- future workforce policy

---

# Future Scope

Potential future developments include:
- Predictive modelling of automation risk
- Machine learning applications for workforce forecasting
- AI governance and ethical workplace analytics
- Comparative analysis between platform and organisational workers
- Longitudinal labour market analysis

---

# Author

Ajita Joshi  
MSc Data Analytics & Human Resource Management  
University of Leeds

Research Interests:
- Future of Work
- AI and Algorithmic Management
- Workforce Analytics
- Organisational Behaviour
- Employment Relations
- Digital Economy Research

