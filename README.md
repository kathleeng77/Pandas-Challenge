# Pandas-Challenge

Analyzing Gaming Data with Pandas in Jupyter Notebook

# Analysis

First, I opened Jupyter Notebook from git bash, imported dependencies (pandas and numpy), and read in the .csv file.

Second, I calculated the following:
* total number of players.
* number of unique items.
* average purchase price.
* total number of purchases.
* total revenue.

Third, I used .groupby(), 'bins', and .sort_values() to perform calculations on certain groups, such as:
* percentage and count of different genders and ages.
* purchase count, average purchase price, total purchase value, and average purchase total per person by gender and age groups.
* top spenders by screen name.
* most popular items.
* most profitable items.

# Notes

When checking correctness in the final data frame (showing "most profitable items"), I realized that the values weren't sorted in descending values properly. After much research, I decided to delete the row that I felt was causing the main miscalculation while trying to show the first few rows with .head(). However, I want to keep researching to find another way to solve this without altering the data in a destructive way.