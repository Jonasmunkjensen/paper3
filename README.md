# Utilization of Municipal Health Services Among People with Type 2 Diabetes

## Overview

This repository contains the analysis code and documentation for a cross-sectional, register-linked study investigating the utilization of municipality-based health services among people living with type 2 diabetes (T2D) in the Central Denmark Region.

The study is part of the **LIVING project** and uses data from the **Health in Central Denmark (HICD) Cohort**, linking regional survey data with nationwide register-based demographic, socioeconomic, and clinical information.

The study aims to describe who uses municipal health services, who does not, and whether current services reach population groups with the greatest apparent need for support.

## Research questions

The study consists of four complementary components:

1. **Mapping of municipal health service utilization**

   How many people with T2D report contact with different municipality-based health services?

2. **Attrition and representativeness**

   How representative are the survey respondents of the broader population of people with T2D in the Central Denmark Region?

3. **Users vs. non-users**

   Which demographic, socioeconomic, clinical, behavioral, and psychosocial characteristics are associated with utilization of municipal health services?

4. **Illustrative patient profiles**

   How do combinations of individual characteristics translate into differences in the predicted probability of using municipal health services?

## Municipal health services

The study examines five types of municipality-based support:

* Referral from a general practitioner
* Diet counseling
* Physical activity and/or exercise programs
* Diabetes self-management programs
* Mental health support related to living with diabetes

For the main analyses, each service is treated as a binary outcome distinguishing **users** from **non-users**.

## Study population

The HICD cohort includes adults aged 18–75 years with diabetes in the Central Denmark Region.

For the present study:

| Population                               |      N |
| ---------------------------------------- | -----: |
| People with T2D in HICD                  | 72,343 |
| Respondents to the primary questionnaire | 20,830 |
| Consented to supplementary questionnaire | 13,328 |
| Completed supplementary questionnaire    |  4,704 |

The primary analysis is based on the **4,704 respondents** who completed the supplementary questionnaire.

A response-weighted analysis will additionally be used to represent the 13,328 individuals who consented to receive the supplementary questionnaire.

## Data sources

The study combines:

### Survey data

Data from the HICD primary and supplementary questionnaires, including measures of:

* Health literacy
* Diabetes distress
* Well-being
* Quality of life
* Physical activity
* BMI
* Smoking
* Perceived disease burden
* Personality traits
* Diabetes duration

### Register data

Nationwide register-based information including:

* Age
* Sex
* Country of origin
* Educational attainment
* Equivalized disposable household income
* Cohabitation/marital status
* Diabetes duration
* HbA1c
* Total cholesterol
* Comorbidity

## Analysis

All analyses are performed in **R**.

The main statistical approaches include:

* Descriptive statistics
* Response weighting using stabilized inverse probability weights
* Attrition analyses
* Logistic regression
* Restricted cubic splines for assessment of non-linear associations
* Predicted probabilities for illustrative patient profiles

The analysis is explicitly **descriptive and associational**. The study does not aim to estimate causal effects of municipal health service utilization.

The detailed statistical analysis plan is available in the project documentation and will be uploaded to **Open Science Framework (OSF)** for timestamping before the analyses are initiated.

## Repository structure

The repository is organized to separate data preparation, analysis, and reporting:

```text
.
├── README.md
├── protocol/
│   └── protocol.qmd
│   └── references.bib
│   └── litteratur/
│
├── R/
│   ├── 01_import.R
│   ├── 02_data_cleaning.R
│   ├── 03_create_variables.R
│   ├── 04_response_weights.R
│   ├── 05_mapping.R
│   ├── 06_attrition.R
│   ├── 07_users_vs_nonusers.R
│   └── 08_patient_profiles.R
│
├── output/
│   ├── tables/
│   └── figures/
│
└── manuscript/
    ├── manuscript.qmd
    └── references.bib
```

> **Note:** data are not included in this repository due to data protection and research governance requirements.

## Reproducibility

The analyses are developed using **R** and **Quarto**.

Packages and dependencies should be documented in the project files. Where possible, analyses should be run through the numbered scripts in the `R/` directory in sequence.

The repository is intended to provide a transparent record of the analytical workflow while ensuring that individual-level confidential data are not exposed.

## Study status

**Study period:** 2026–2027

**Current status:** Analysis plan under development.

Before analysis, the statistical analysis plan will be timestamped through OSF. The analysis plan is currently being refined, including the final participant flow numbers, variable definitions, and statistical procedures.

## Related project

This study is part of the **LIVING project**, which investigates the effectiveness of different diabetes self-management program configurations, including programs incorporating supervised high-intensity interval training (HIIT).

## Citation

A citation for the study will be added once the manuscript has been published.

## Contact

**Jonas Munk Jensen**
Aarhus University / Steno Diabetes Center Aarhus / Aarhus University
