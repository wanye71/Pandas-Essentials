# Python pandas Essentials - Basic Plotting

## Figsize()
```python
# Adjust the plot size to span 10 inches by 3 inches
first_olympics.Sport.value_counts().plot(figsize=(10,3));
```

## Colormaps
```python
first_olympics.Sport.value_counts().plot(kind='pie', colormap='Pastel1')
```