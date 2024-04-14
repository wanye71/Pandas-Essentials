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

## Accessing Series
1. Accessing with square-bracket notation

| City | Edition | Sport | Discipline | Athlete | NOC | Gender | Event | Event_gender | Medal |
|------|---------|-------|------------|---------|-----|--------|-------|--------------|-------|

```python
olympics_df['City']

0         Athens
1         Athens
2         Athens
3         Athens
4         Athens
          ...   
29211    Beijing
29212    Beijing
29213    Beijing
29214    Beijing
29215    Beijing
Name: City, Length: 29216, dtype: object
```
2. Accessing with dot-notation

| City | Edition | Sport | Discipline | Athlete | NOC | Gender | Event | Event_gender | Medal |
|------|---------|-------|------------|---------|-----|--------|-------|--------------|-------|

```python
olympics_df.Athlete

0               HAJOS, Alfred
1            HERSCHMANN, Otto
2           DRIVAS, Dimitrios
3          MALOKINIS, Ioannis
4          CHASAPIS, Spiridon
                 ...         
29211          ENGLICH, Mirko
29212    MIZGAITIS, Mindaugas
29213         PATRIKEEV, Yuri
29214           LOPEZ, Mijain
29215          BAROEV, Khasan
Name: Athlete, Length: 29216, dtype: object
```
3. Accessing multiple columns

| City | Edition | Sport | Discipline | Athlete | NOC | Gender | Event | Event_gender | Medal |
|------|---------|-------|------------|---------|-----|--------|-------|--------------|-------|

```python
olympics_df[['City', 'Edition', 'Athlete']]

City	Edition	Athlete
0	Athens	1896	HAJOS, Alfred
1	Athens	1896	HERSCHMANN, Otto
2	Athens	1896	DRIVAS, Dimitrios
3	Athens	1896	MALOKINIS, Ioannis
4	Athens	1896	CHASAPIS, Spiridon
...	...	...	...
29211	Beijing	2008	ENGLICH, Mirko
29212	Beijing	2008	MIZGAITIS, Mindaugas
29213	Beijing	2008	PATRIKEEV, Yuri
29214	Beijing	2008	LOPEZ, Mijain
29215	Beijing	2008	BAROEV, Khasan
```

3. Confirm object (DataFrame or Series)
```python
type(olympics_df)
pandas.core.frame.DataFrame

type(olympics_df.City)
pandas.core.series.Series
```