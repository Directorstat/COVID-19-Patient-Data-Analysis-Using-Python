COVID-19 Patient Data Analysis Using Python

Project Overview

# COVID-19 Patient Data Analysis Using Python

## Project Overview

This project performs exploratory data analysis on COVID-19 patient records. 
The analysis examines trends in new cases, deaths, and vaccination data across multiple countries. 
The project focuses on cleaning raw health data, handling missing values, detecting outliers, and visualizing relationships between infection rates, mortality, and vaccination.

## Objectives

Clean and preprocess the COVID-19 dataset

Handle missing and inconsistent data values

Detect and treat outliers in health indicators

Explore distributions of cases, deaths, and vaccinations

Examine relationships between infections, deaths, and vaccination levels

Visualize trends and correlations using statistical plots

## Techniques Used
Google Colab

Libraries used
pandas, data manipulation and preprocessing; numpy, numerical computation; matplotlib, data visualization; seaborn, statistical visualization; scikit-learn, missing value imputation

## Dataset Description

The dataset contains COVID-19 patient statistics from several countries.

Columns included
DATE, date of record; country, country name; NEW_Cases, number of new COVID-19 cases; NEW_DEATHS, number of new deaths; vaccinated, vaccination count

Additional columns created during analysis
Year, Month, Day and DATE_numeric

These variables support time-based analysis and visualization.

## Data Cleaning Process

### Handling Missing Values

Several columns contained missing values represented as n/a, unknown and ?

These values were converted to NaN during data import.

Missing numeric values were handled using mean imputation.

Technique used

SimpleImputer with mean strategy from scikit-learn.

### Date Conversion

The DATE column was converted to a datetime format to enable time analysis.

New variables were extracted: Year, Month and Day

### Removing Duplicate Records

Duplicate rows were detected and removed to ensure dataset accuracy.

Result

Duplicate rows after cleaning: 0

## Outlier Detection

Outliers were detected using the Interquartile Range method.

Steps used

Calculate first quartile Q1

Calculate third quartile Q3

Compute IQR = Q3 − Q1

Filter values outside the acceptable range

This process reduced extreme values in the NEW_DEATHS variable.

Boxplots were used to visualise the distributions before and after outlier removal.

## Exploratory Data Analysis

### Univariate Analysis

Distribution analysis was conducted for numeric variables using histograms and density curves.

Key observations

NEW_Cases and NEW_DEATHS show roughly symmetrical distributions

Most values fall within moderate ranges

The day variable reflects data across days 1 to 30

### Country Distribution

A frequency bar chart was used to show the representation of countries in the dataset.

Key finding

Brazil, Canada, and China have the most records.

Argentina and Australia have fewer observations.

### Vaccination Disparity Across Countries

The standard deviation of vaccination levels was calculated by country.

Bar charts show variation in vaccination distribution across regions.

## Correlation Analysis

### Cases and Vaccination

Scatter plot and correlation analysis show weak or no correlation between

NEW_Cases and vaccinated

### Deaths and Vaccination

The scatter plot indicates little relationship between

NEW_DEATHS and vaccinated

### Cases and Deaths

A strong positive correlation exists between

NEW_Cases and NEW_DEATHS

Interpretation

As infection numbers increase, death counts also increase.

## Visualization Techniques Used

Several statistical visualizations were applied.

Box plots
Detect outliers in numeric features.

Histogram plots
Understand variable distributions.

Bar charts
Show the frequency of countries.

Scatter plots with regression lines
Analyze relationships between health indicators.

Heatmap
Visualize correlation between numerical variables.

Line plot
Show daily vaccination trends.

## Key Insights

Missing values were successfully handled using mean imputation

Duplicate records were removed to improve dataset quality

NEW_DEATHS contained several outliers that required filtering

Brazil, Canada, and China dominate the dataset representation

A strong positive correlation exists between infection cases and deaths

Vaccination counts show a weak correlation with both cases and deaths

Vaccination distribution remains relatively stable across days in 2024

## How to Run the Project

1. Install Python

2. Install required libraries

pip install pandas numpy matplotlib seaborn scikit-learn

3. Place the dataset file in the project folder

Patient data.csv

4. Run the Python script

python covid_analysis.py

## Learning Outcomes

This project demonstrates practical skills in

Data preprocessing and cleaning

Missing data imputation

Outlier detection using IQR

Exploratory data analysis

Statistical correlation analysis

Data visualisation using Python libraries
