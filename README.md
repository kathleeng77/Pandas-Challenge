# Pandas-Challenge

Analyzing Gaming Data with the Pandas Library in Jupyter Notebook
-----

## Analysis

* Of the active players, the vast majority are male (84%). There also exists, a smaller, but notable proportion of female players (14%).
* Our peak age demographic falls between 20-24 (44.8%) with secondary groups falling between 15-19 (18.6%) and 25-29 (13.4%).
* The age group that spends the most money is the 20-24 age group.
-----

## Breakdown

#### Dependencies and Setup
```python
# Importing Pandas Library
import pandas as pd

# File to Load
file_path = "purchase_data.csv"

# Read Purchasing File and store into pandas data frame
raw_data = pd.read_csv(file_path)
raw_data.head()
```

#### Player Count

* total number of players.

```python
total_players = len(raw_data["SN"].unique())

total_players_df = pd.DataFrame({"Total Players": [total_players]})

total_players_df
```

<div>

<table class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Total Players</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>576</td>
    </tr>
  </tbody>
</table>
</div>

#### Purchasing Analysis

* number of unique items.
* average purchase price.
* total number of purchases.
* total revenue.

```python
unique_items = len(raw_data["Item ID"].unique())
avg_price = sum(raw_data["Price"])/len(raw_data["Price"])
purchases = len(raw_data["Purchase ID"])
revenue = sum(raw_data["Price"])

purchasing_df = pd.DataFrame({"Number of Unique Items": [unique_items], "Average Price": [avg_price],
                              "Number of Purchases":[purchases], "Total Revenue":[revenue]})

purchasing_df["Average Price"] = purchasing_df["Average Price"].map("${:,.2f}".format)
purchasing_df["Total Revenue"] = purchasing_df["Total Revenue"].map("${:,.2f}".format)

purchasing_df
```

Third, I used .groupby(), 'bins', and .sort_values() to perform calculations on certain groups, such as:

* percentage and count of different genders and ages.
```python
```

* purchase count, average purchase price, total purchase value, and average purchase total per person by gender and age groups.
```python
```

* top spenders by screen name.
```python
```

* most popular items.
```python
```

* most profitable items.
```python
```
-----

## Notes

When checking correctness in the final data frame (showing "most profitable items"), I realized that the values weren't sorted in descending values properly. After much research, I decided to delete the row that I felt was causing the main miscalculation while trying to show the first few rows with .head(). However, I want to keep researching to find another way to solve this without altering the data in a destructive way.