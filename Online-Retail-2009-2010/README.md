# Online Retail EDA (2009-2010)

This is my first EDA project using the Online Retail II dataset. I worked through the data step by step and used Pandas, Matplotlib and Seaborn.

## What I did

- Checked the dataset size, columns and data types.
- Checked missing values and exact duplicates.
- Converted `InvoiceDate` to datetime.
- Looked at negative quantities and rows with zero prices.
- Made a working copy without exact duplicate rows.
- Used positive-quantity and positive-price rows for the sales analysis.
- Calculated `LineValue` as `Quantity * Price`.
- Analysed monthly transaction value, top products by quantity, and top countries and products by transaction value.
- Made line and bar charts to see the results.

## What I found

- The original dataset had 525,461 rows and 8 columns.
- `Description` had 2,928 missing values (0.56%). All of those rows had a price of zero.
- `Customer ID` had 107,927 missing values (20.54%). I kept these rows for overall sales analysis because a missing ID does not necessarily mean the transaction is unusable.
- There were 6,865 exact duplicate rows. After removing them from the working copy, 518,596 rows remained.
- There were 12,302 negative-quantity rows after removing duplicates. Of these, 10,181 had invoice numbers starting with `C`; the other 2,121 had zero prices.
- There were 3,681 zero-price rows in total, including 1,560 rows with positive quantities.
- The United Kingdom had the highest filtered transaction value, about £8.81 million.
- `WHITE HANGING HEART T-LIGHT HOLDER` had the highest positive quantity, with 58,691 units.
- `Manual` had the highest transaction value among descriptions, about £262,963, but it may not be a normal physical product.
- November 2010 had the highest monthly transaction value, about £1.46 million. December was about £437,631, but the data ends on 9 December, so it is not a full month.

## Run the notebook

Keep the `Online_Retail_EDA.ipynb` notebook and the `data` folder together. The notebook loads the data from `data/Year_2009-2010.csv` using a relative path.

Before running the notebook, add `Year_2009-2010.csv` to the `data` folder. The CSV is from the UCI dataset linked below.

## Note

The sales analysis keeps rows where `Quantity > 0` and `Price > 0`, then calculates `LineValue = Quantity * Price`. These values are useful for this analysis, but they are not finalized net revenue.

## Dataset source

[UCI Machine Learning Repository — Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
