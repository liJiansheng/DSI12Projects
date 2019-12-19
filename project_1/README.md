# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Testing, Statistical Summaries and Inference

### Project 1 Overview

This project aims to recommend ways to improve SAT participation based on 2017 and 2018 SAT and ACT data.

### Data Cleaning

With the given raw data, the data is cleaned using pandas and Python. The data is merged and stored in a final file in data/final.csv.

### Data Dictionary

**SAT 2017**

| Feature                 | Type   | Dataset  | Description                                  |
| ----------------------- | ------ | -------- | -------------------------------------------- |
| state                   | object | SAT 2017 | States participating in SAT                  |
| sat_participation       | float  | SAT 2017 | participation Percentage of SAT              |
| sat_evidence_read_write | int    | SAT 2017 | Score for SAT Evidence Read Write            |
| sat_math                | int    | SAT 2017 | Score for SAT Math                           |
| total                   | int    | SAT 2017 | Total Score for Evidence Read Write and Math |

**ACT 2017**

| Feature           | Type   | Dataset  | Description                     |
| ----------------- | ------ | -------- | ------------------------------- |
| state             | object | ACT 2017 | States participating in SAT     |
| act_participation | float  | ACT 2017 | participation Percentage of SAT |
| act_english       | int    | ACT 2017 | Score for ACT English           |
| act_math          | float  | ACT 2017 | Score for ACT Math              |
| act_reading       | float  | ACT 2017 | Score for ACT Reading           |
| act_science       | float  | ACT 2017 | Score for ACT Science           |
| composite         | float  | ACT 2017 | Composite Score for ACT         |

### Exploratory Data Analysis

With final.csv as the data source, some custom functions were created. To further spot trends, filtering and masking of the data was used.

### Data Visualisation

Making use of numpy, matplotlib and seaborn, the different aspects of the data was masked and filtered to provide a better analysis. There were many plots but not all were used in the final analysis
