# Python pandas Essentials - Basic Plotting

## Basic plotting
```python
# Line plot
first_olympics.Sport.value_counts().plot(kind='line');

# Bar plot
first_olympics.Sport.value_counts().plot(kind='bar');

# Horizontal Bar plot
first_olympics.Sport.value_counts().plot(kind='barh');

# Pie plot
first_olympics.Sport.value_counts().plot(kind='pie');
```