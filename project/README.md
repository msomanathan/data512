# Project
The goal of this project is to answer the research question: How did masking policies change the progression of confirmed COVID-19 cases from February 1, 2020 through October 1, 2021?

## Data source
The following 3 datasets were downloaded to acquire the raw data for COVID-19 confirmed cases in the US for all counties:
- `confirmed_cases.csv`: https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university. This dataset has the cumulative confirmed COVID-19 cases for each US county from Feb 2020 to Oct 2021.
- `mask_mandates.csv`: https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i. This dataset tells whether mask mandate was in effect for any given day for each US county from Feb 2020 to Oct 2021. There are days where this data was missing, and these were assumed to be no mask mandate in effect.
- `mask_usage.csv`: https://github.com/nytimes/covid-19-data/tree/master/mask-use. This dataset provides the percentage of the population that complied with mask mandate policies for every US county.

## Code
The code is provided in the notebook `project.ipynb`.

## Visualization
The visualization of the COVID-19 case data is found in:
- `visualization.png`, which plots a time series of both the infection rate, and the actual infections on any given date. Furthermore, the plot highlights the time period where mask mandate was in effect.
