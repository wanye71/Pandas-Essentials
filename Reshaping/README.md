# Pandas Essentials - Reshaping

## stack() and unstack()
```python
import pandas as pd

olympics_df = pd.read_csv('../olympics.csv', skiprows=4)
olympics_df.head()

# Athletes winnind medals in Beijing Olympics 100m or 200m track event
gender_df = olympics_df[(olympics_df.Edition == 2008) & ((olympics_df.Event == '100m') | (olympics_df.Event == '200m'))]
gender_df

group = gender_df.groupby(['NOC', 'Gender', 'Discipline', 'Event']).size()
group

group_df = group.unstack(['Discipline', 'Event'])
group_df