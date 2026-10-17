# Exploratory Data Analysis Projects

This repository is for my EDA projects using Python. I will add datasets, notebooks, charts and findings as I work through different types of data.

## Projects

### 1. Online Retail (2009-2010)

I used the first year of the Online Retail II dataset to practise data cleaning and EDA with Pandas, Matplotlib and Seaborn.

- Notebook: [Online_Retail_EDA.ipynb](Online-Retail-2009-2010/Online_Retail_EDA.ipynb)
- Dataset: [Year_2009-2010.csv](Online-Retail-2009-2010/data/Year_2009-2010.csv)
- Project notes: [README](Online-Retail-2009-2010/README.md)

### What I found

- The original data had 525,461 rows and 8 columns.
- `Description` had 2,928 missing values (0.56%) and `Customer ID` had 107,927 missing values (20.54%).
- I found 6,865 exact duplicate rows. The working copy had 518,596 rows after removing them.
- The United Kingdom had the highest filtered transaction value, about £8.81 million.
- `WHITE HANGING HEART T-LIGHT HOLDER` had the highest total positive quantity, with 58,691 units.
- November 2010 had the highest monthly transaction value, about £1.46 million.
- December's recorded value was lower, but the dataset ends on 9 December 2010, so December is incomplete.

The notebook uses positive quantities and positive prices for its sales analysis. The values are filtered transaction values, not final net revenue.

## Dataset source

The data is from the [UCI Machine Learning Repository — Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii). This project uses the 2009-2010 sheet only.
