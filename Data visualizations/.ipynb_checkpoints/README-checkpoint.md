# Pandas Essentials - Data Visualizations

## Learning Heatmaps
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
%matplotlib inline

olympics_df = pd.read_csv('../olympics.csv', skiprows=4)
olympics_df


# Using the Olympics dataset, present a summary of the total medals won by participating countries in the 2008 Olympics

olympics_2008 = olympics_df[olympics_df.Edition == 2008]
olympics_2008

olympics_2008.groupby(['NOC', 'Medal']).size()

olympics_2008.groupby(['NOC', 'Medal']).size().unstack('Medal', fill_value=0)

group_df = olympics_2008.groupby(['NOC', 'Medal']).size().unstack('Medal', fill_value=0)[['Gold', 'Silver', 'Bronze']]
group_df = group_df.sort_values(['Gold', 'Silver', 'Bronze'], ascending=False)
group_df

sns.heatmap(group_df);

group_df = group_df.transpose()
group_df

plt.figure(figsize=(18,5))
sns.heatmap(group_df)
```