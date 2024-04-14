# Python pandas Essentials - Basic Plotting

## Exercise
```python
import pandas as pd

import matplotlib.pyplot as plt
import seaborn as sns

%matplotlib inline

odf = pd.read_csv('olympics.csv', skiprows=4)
odf.head()

# Identify men and women who participated
mw = odf[ (odf.Edition == 2008) & (odf.NOC == 'CHN')]
mw.head()

# Plot the gender series
mw.Gender.value_counts().plot(kind='bar');

sns.countplot(data=odf, x='Gender');

sns.countplot(data=odf, x='Gender', palette='bwr');

# Plot the number of Gold, Silver and Bronze medals for each gender
sns.countplot(x='Medal', data=mw, hue='Gender');

# How can you give the data more meaning?
# Is there anything else you can change to make it more intuitive?

sns.countplot(x='Medal', data=mw, hue='Gender', palette='bwr');

sns.countplot(x='Medal', data=mw, hue='Gender', palette='bwr', order=['Gold', 'Silver', 'Bronze']);
```