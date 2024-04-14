# Python pandas Essentials - DataFrames

## Series and DataFrames
```python
import pandas as pd
```

```python
olympics_df = pd.read_csv('olympics.csv', skiprows=4)
olympics_df.head()
```

## Accessing the DataFrame
```python
olympics_df
```