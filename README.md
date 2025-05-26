# Sale-market-Data-
A beginner-friendly data analysis project exploring sales trends.
import pandas as pd
import matplotlib.pyplot as plt

# Load data
data = pd.read_csv("sales_data.csv")

# Show top 5 rows
print(data.head())

# Basic analysis: Total sales by region
sales_by_region = data.groupby('Region')['Sales'].sum().sort_values(ascending=False)
print(sales_by_region)

# Simple visualization
sales_by_region.plot(kind='bar', title='Total Sales by Region')
plt.show()
