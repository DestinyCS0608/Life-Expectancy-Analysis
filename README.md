# Analysis of Country Status, Alcohol, and Expenditure as Factors of Life Expectancy

## Project Overview

This project explores the relationship between alcohol consumption, government healthcare expenditure, and country status (developed vs developing) on life expectancy. Using data from the World Health Organization and the United Nations, we applied multiple regression models to understand how these factors interact to influence life expectancy across 193 countries (2000–2015).

**Goal:** Identify key predictors of life expectancy and understand how country context modifies the impact of alcohol and healthcare expenditure.

## Key Findings

-   Developed countries have higher life expectancy (≈79 yrs) and healthcare spending (≈7.5% of GDP).

-   Developing countries have lower life expectancy (≈67 yrs) and lower healthcare spending (≈5.5% of GDP).

-   The interaction between alcohol consumption and healthcare expenditure shows that higher investment in healthcare mitigates the negative effects of alcohol on life expectancy.

## Data 

-   Source: WHO Global Health Observatory (GHO), UN database

-   Years Covered: 2000–2015

-   Countries Included: 193 (some missing due to data limitations: e.g., Vanuatu, Tonga)

## Variables Used:

-   life_expectancy – average lifespan in years

-   status – Developed / Developing

-   alcohol – average per capita alcohol consumption (liters)

-   total_expenditure – healthcare expenditure as % of GDP

## Methodology

1.  Data Cleaning: Selected relevant columns, removed missing values, standardized names.
2.  Exploratory Data Analysis (EDA): Visualized relationships between life expectancy, alcohol, and healthcare expenditure by country status.
3.  Statistical Analysis:
    -   Multiple regression: life_expectancy \~ status + alcohol \* total_expenditure

    -   Nested F-test confirmed that including the interaction term improved model fit.
4.  Model Diagnostics: Checked linearity, normality, multicollinearity, and heteroscedasticity; log transformation did not improve assumptions.

## Results

-   Regression Analysis:

    -   Developing countries: \~8.8 years lower life expectancy than developed countries.

    -   Interaction term: alcohol × healthcare expenditure positively influences life expectancy.

-   Visual Insights:

    -   Developed: alcohol slightly decreases life expectancy; expenditure increases it.

    -   Developing: alcohol and expenditure positively correlated with life expectancy.

## Limitations

-   Linearity and normality assumptions were not fully met.

-   Potential bias due to missing data for some countries.

-   Other important predictors (e.g., diet, pollution, lifestyle) not included.

## Skills & Tools Used

-   Programming: R, tidyverse, dplyr, ggplot2

-   Statistical Analysis: Multiple regression, interaction terms, nested F-test, confidence intervals

-   Data Visualization: Scatterplots, interaction plots

-   Data Cleaning & Wrangling: Handling missing data, renaming, filtering

