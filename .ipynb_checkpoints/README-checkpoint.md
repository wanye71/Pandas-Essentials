# Python pandas Essentials - Data Input and Validation

## Read (read.csv)
- Input
  - read_excel()
  - read_json()
  - read_sql_table()
 
```python
# skiprows will skip the first 4 rows of the file
olympic_df = pd.read_csv('olympics.csv', skiprows=4)
olympic_df
```