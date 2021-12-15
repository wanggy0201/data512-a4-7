# data-512-a4-7

Hawaii: How COVID-19 Affects Travel

## Introduction
In this project, I will explore the COVID-19 impact in Honolulu, Hawaii in 2 aspects. In the first part (A4 assignment), I will try to answer the question “How did masking policies change the progression of confirmed COVID-19 cases from February 1, 2020 through October 15, 2021?”. Next in the second part (A5&7 Assignments), I will be exploring answers to the question “How did the COVID-19 pandemic affect people travelling to Hawaii?”. The full report can be found here: https://docs.google.com/document/d/1lFPU9p4GzJJm3OYw7-xgqkegWq8RNLv5AjrgNqfpWRs/edit?usp=sharing

## Data source
1. [Link](https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv) - The RAW_us_confirmed_cases.csv file from the Kaggle repository of John Hopkins University COVID-19 data.
2. [Link](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i) - The CDC dataset of masking mandates by county.
3. [Link](https://github.com/nytimes/covid-19-data/tree/master/mask-use) - The New York Times mask compliance survey data.
4. [Link](https://www.hawaiitourismauthority.org/research/monthly-visitor-statistics/) - Monthly Visitor Statistics from Hawaii Travel Authority
5. [Link](https://www.hawaiitourismauthority.org/research/infrastructure-research/) - Air seats and hotel occupancy statistics from Hawaii Travel Authority

## Project structure

### Python notebook (A4.ipynb & A7.ipynb)
These will be the main noteboooks that contains code that performs data acquisition, data processing and analysis.

### Datasets (under `data/`)
This directory contains data files that contains te datasets that are used for the analysis. For the Hawaii travel data `hawaii-data.csv`, it is a cleaned version of the raw data stored under `a7_raw_data`

### Procssed Hawaii travel data (under `data/hawaii-data.csv`)
This is a file that is convered using the raw data collected from the Hawaii Travel Authority. It will follow the following schema:

|                          | Value   | Description                                     |
|--------------------------|---------|-------------------------------------------------|
| Time                     | date    | Monthly timestamp                               |
| Visitor Arrival          | numeric | Total monthly visitor                           |
| Avg. length of stay      | numeric | Average stay of visitors                        |
| Per day spending         | numeric | Average day spent in Hawaii                     |
| Per trip spending        | numeric | Average spending of visitors                    |
| Total flights            | numeric | Total flights scheduled to Hawaii               |
| International flight     | numeric | Total international flights scheduled to Hawaii |
| Hotel Occupancy          | numeric | Hotel occupancy monthly statistics              |
| Hotel rate               | numeric | Monthly average hotel rate                      |
| Hotel revPar             | numeric | Monthly average hotel revPar metric             |
| Hotel supply (thousands) | numeric | Monthly average hotel supply (in thousands)     |
| Hotel Demand             | numeric | Monthly average hotel demand (in thousands)     |

### Analysis results (under `a4_output_figures` and `a7_output_figures`)
This directory contains analysis results, where currently in this project we only have a time series visualization graph.

## How to run the project
Before running the project, you will need to download this file to `data/` - https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i

To run the project, open the notebook `A4.ipynb` or  `A7.ipynb`. Select `Cell -> Run All`. This will generate the analysis results and all intermediate datasets including the raw data and procssed data.
