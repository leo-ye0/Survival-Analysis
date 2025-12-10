# Survival-Analysis
## DSCI564 Survival Analysis
#### Instructor: Mohammad Reza Rajati, PhD
#### Yutao Ye
#### Email: yutaoye@usc.edu
---
### Survival Analysis Description
Survival Analysis is a subfield of statistics that studies time to a specific event (such as
death or malfunction of an equipment) as a random variable. The statistical properties
of the random variable such as mean time to an event are very important in many fields
such as biostatistics and reliability engineering.
In this project, I will perform survival analysis on benchmark data and learn about
statistical tools for survival analysis such as the Kaplan-Meier estimator and the Cox
Proportional Hazards Model.

# Survival Analysis of Primary Biliary Cirrhosis (PBC)

## Project Overview
This project performs a comprehensive survival analysis on the `pbcseq` (Primary Biliary Cirrhosis sequential) dataset. The goal is to identify significant risk factors for mortality and compare traditional statistical methods against modern machine learning techniques.

The analysis includes:
1.  **Data Pre-processing:** Handling sequential data, log-transformations, and missing value imputation.
2.  **Kaplan-Meier Analysis:** Visualizing survival differences by Sex and Treatment.
3.  **Cox Proportional Hazards Model:** Building a time-varying regression model with stepwise variable selection.
4.  **Deep Learning:** Implementing a DeepSurv neural network to capture non-linear risk factors and comparing its performance to the Cox model.

## Dataset
The analysis uses the `pbcseq` dataset from the R `survival` package.
* **Subjects:** 312 patients with Primary Biliary Cirrhosis.
* **Structure:** Longitudinal/Sequential data (multiple visits per patient).
* **Key Variables:**
    * `futime`: Follow-up time (days).
    * `status`: 0=alive, 1=transplanted, 2=death.
    * `trt`: Treatment (D-penicillamine vs Placebo).
    * `sex`: Male/Female.
    * `bili`, `albumin`, `protime`, `age`: Clinical covariates.

## Prerequisites & Installation

### R Packages
This project requires the following R libraries:
```r
install.packages(c("survival", "MASS", "survivalmodels", "reticulate"))