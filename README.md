# Python pandas Essentials - Basic Plotting

## Seaborn Basic Plotting
```python
# How many medals have been won by men and women in the history of the Olypics. How many gold, silver and bronze medals were won for each gender?

sns.countplot(x='Medal', data=odf, hue='Gender');
```