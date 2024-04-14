# Python pandas Essentials - Data Input and Validation

## Using shape
Shape will return a tuple that's rows and columns. Confirms the dimensions of your dataset
```python
# Get rows and columns
olympic_df.shape
(29216, 10)

# Get rows only
olympic_df.shape[0]
(29216)

# Get columns only
olympic_df.shape[1]
(10)
```