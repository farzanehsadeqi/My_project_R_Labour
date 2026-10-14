# What Drives Job Mobility? Employer Changes and Worker Characteristics in R

How often do workers change employers, and which characteristics explain the differences? This project models the number of employer changes as a function of gender, occupation, age, income history and wage level, using OLS regression in R.

## Data

Labour-market data on individual workers (cohort observed from 1986) with the following variables:

- **nchange**: number of employer changes (dependent variable)
- **gender**, **occupation** (blue collar / white collar)
- **age**
- **periods_income**: number of years with positive income
- **median_wage**: median wage category

## Methods

- **Descriptive analysis**: summary statistics and distributions of key variables
- **Model 1**: linear regression on all characteristics, comparing predicted employer changes across gender, occupation and income groups
- **Model 2**: adds a quadratic effect of income periods to capture non-linear effects
- **Model 3**: adds a gender × occupation interaction
- **Model comparison** via adjusted R², and prediction for a specific worker profile
- **Residual diagnostics**: skewness and kurtosis, Jarque–Bera test for normality, Breusch–Pagan test for heteroskedasticity

## Key findings

- Men, blue-collar workers and low-wage workers change employers more often.
- Income periods have a significant non-linear (quadratic) effect on job mobility.
- The gender × occupation interaction is not statistically significant.
- Model 2 performs best by adjusted R².
- Residuals deviate from normality in all three models, so inference should be read with caution.

## Tools

R · `lmtest` · `tseries` · `moments`

## How to run

Open `projectLabour.Rmd` in RStudio, load the dataset as `change`, and knit to HTML.
