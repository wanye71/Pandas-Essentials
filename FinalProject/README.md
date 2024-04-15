# Pandas Essentials - Final Project

## Identification of Top-Performing Athletes Representing USA Across Olympic Editions

```python
# Importing necessary libraries
import pandas as pd  # Pandas for data manipulation and analysis
import seaborn as sns  # Seaborn for statistical data visualization
import matplotlib.pyplot as plt  # Matplotlib for basic plotting functionality

from matplotlib.colors import ListedColormap  # ListedColormap for creating custom color maps

# Magic command to display matplotlib plots inline within Jupyter Notebook or JupyterLab
%matplotlib inline
```

```python
# Reading the dataset 'olympics.csv' into a pandas DataFrame
olympics_df = pd.read_csv('../olympics.csv', skiprows=4)
# Displaying the DataFrame to inspect its contents
olympics_df
```

```python
# Filtering the DataFrame to select rows where the 'NOC' column equals 'USA'
group_df = olympics_df[olympics_df.NOC == 'USA']
# Displaying the filtered DataFrame containing data only for the USA
group_df
```

```python
# Grouping the DataFrame 'group_df' by 'Edition', 'Athlete', and 'Medal', 
# and then counting the occurrences of each group
group_df.groupby(['Edition', 'Athlete', 'Medal']).size()
```

```python
# Calculating the total number of medals ('Gold', 'Silver', and 'Bronze') for each row
group_df['Total'] = group_df['Gold'] + group_df['Silver'] + group_df['Bronze']

# Resetting the index of the DataFrame 'group_df' to default and modifying the DataFrame in place
group_df.reset_index(inplace=True)

# Finding the top-performing athlete (highest total medals) for each edition of the Olympics
top_usa = [group.sort_values('Total', ascending=False)[:1] for year, group in group_df.groupby('Edition')]

# Creating an empty DataFrame 'top'
top = pd.DataFrame()

# Appending the top-performing athlete for each edition to the 'top' DataFrame
for i in top_usa:
    top = top._append(i)

# Displaying the DataFrame 'top' containing the top-performing athlete for each edition of the Olympics
top
```