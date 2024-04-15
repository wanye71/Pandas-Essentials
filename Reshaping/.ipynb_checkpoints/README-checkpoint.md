# Pandas Essentials - Reshaping

## Reshaping Exercise 
```python
import pandas as pd

olympics_df = pd.read_csv('../olympics.csv', skiprows=4)
olympics_df.head()
# # Whic hAthletes are from USA and won Gold medal
gold_medal_df = olympics_df[(olympics_df.NOC == 'USA') & (olympics_df.Medal == 'Gold')]
gold_medal_df

# Athletes across the history of the olympics 
gold_medal_df.groupby(['Edition', 'Gender']).size()

# unstack gender|
gold_medal_df.groupby(['Edition', 'Gender']).size().unstack('Gender', fill_value=0)

gold_medal_df.groupby(['Edition', 'Gender']).size().unstack('Gender', fill_value=0).plot()

# Plt the 5 athletes who have won the most gold medals over the history
# of the Olympics.
# When there is a tie, consider the number of silver medals, then bronze medals

# Grouby 'Athlete' and 'Medal'
olympics_df.groupby(['Athlete', 'Medal']).size()

# Grouby 'Athlete' and 'Medal', unstack it and fill the nans
group_df = olympics_df.groupby(['Athlete', 'Medal']).size().unstack('Medal', fill_value=0)
group_df


group_df.sort_values(['Gold', 'Silver', 'Bronze'])

group_df.sort_values(['Gold', 'Silver', 'Bronze'], ascending=False)

group_df.sort_values(['Gold', 'Silver', 'Bronze'], ascending=False)[['Gold', 'Silver', 'Bronze']]

group_df.sort_values(['Gold', 'Silver', 'Bronze'], ascending=False)[['Gold', 'Silver', 'Bronze']].head()

group_df.sort_values(['Gold', 'Silver', 'Bronze'], ascending=False)[['Gold', 'Silver', 'Bronze']].head().plot(kind='bar', figsize=(12,7))
```