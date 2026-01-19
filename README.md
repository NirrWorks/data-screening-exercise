# Data Screening Exercise – ICE Detention Facilities

## Overview
This repository contains my submission for the Data Scientist screening
exercise for Relevant Research.

The purpose of this exercise is to demonstrate data cleaning, analysis,
and visualization skills using a real-world, messy administrative dataset.

---

## Dataset Description
The dataset (`messy_ice_detention.csv`) contains information on immigration
detention facilities in the United States, including:

- Facility name
- City and state
- Four population indicators (Level A, Level B, Level C, Level D)
- Last inspection end date

The dataset intentionally includes data quality issues such as:
- Metadata rows before the header
- Missing values
- Malformed numeric fields
- Excel serial date formats
- Inconsistent formatting

---

## Data Cleaning
The following steps were taken to prepare the data for analysis:

1. Removed non-tabular metadata rows and identified the correct header
2. Standardized column names for clarity and consistency
3. Converted Level A–D columns to numeric values
4. Converted Excel serial numbers to calendar dates
5. Preserved missing values rather than imputing them
6. Documented assumptions and limitations explicitly

---

## Analysis
A new variable, **Total Population**, was created by summing the Level A,
Level B, Level C, and Level D columns.

Facilities were then sorted by total population, and the **top 10 largest
detention facilities** were selected for further analysis.

---

## Visualization
A horizontal bar chart was created to visualize the top 10 detention
facilities by total population. The visualization is saved as:

top_10_detention_facilities.png


---

## How to Run the Analysis
1. Clone this repository
2. Ensure Python 3 is installed
3. Install required libraries:
pip install pandas numpy matplotlib

4. Open and run `analysis.ipynb`

---

## Assumptions and Limitations
- The dataset does not define the meaning of Levels A–D; these were treated
as quantitative population indicators without semantic interpretation.
- Excel serial dates were assumed to use the 1899-12-30 origin.
- Missing inspection dates were retained and documented as a limitation.

---

## Methods and Resources
This exercise was completed using Python with the pandas and matplotlib
libraries.

ChatGPT was used as a reference tool to clarify exercise requirements,
structure the data cleaning workflow, and improve documentation.
All code and interpretations were reviewed and adapted to meet the
specific requirements of this exercise.

ChatGPT prompt link:
https://chatgpt.com/share/696e59b1-5cfc-800a-8310-cb7099e5282c