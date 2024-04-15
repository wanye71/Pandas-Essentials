# Pandas Essentials - Groupby

## Groupby Exercise
```python
# Groupby 'Edition' and get the size object to determine the medals count for each group
olympics_df.groupby('Edition').size()

# output
Edition
1896     151
1900     512
1904     470
1908     804
1912     885
1920    1298
1924     884
1928     710
1932     615
1936     875
1948     814
1952     889
1956     885
1960     882
1964    1010
1968    1031
1972    1185
1976    1305
1980    1387
1984    1459
1988    1546
1992    1705
1996    1859
2000    2015
2004    1998
2008    2042
dtype: int64


# Now plot it!
olympics_df.groupby('Edition').size().plot()
```

```python
# Groupby 'NOC'  and let's use the basic aggregate function first. 
# So, we need the count and note that because 
# it's asking for the first and the most recent medal win,
# what we want to use is the min and the max information that is
olympics_df.groupby('NOC').agg(['count', 'min', 'max'])

# output
| City | Edition | Sport | Discipline | Gender | Event | Event_gender | Medal |
|------|---------|-------|------------|--------|-------|--------------|-------|
| AFG  | Beijing | Beijing | Taekwondo | Men    | - 58 kg | M | Bronze |
| AHO  | Seoul | Seoul | Sailing | Men    | board (division II) | M | Silver |
| ALG  | Atlanta | Sydney | Athletics | Women    | high jump | W | Silver |
| ANZ  | London | Stockholm | Aquatics | Women    | singles indoor | W | Silver |
| ARG  | Amsterdam | Tokyo | Aquatics | Women    | volleyball | X | Silver |
| ...  | ... | ... | ... | ...    | ... | ... | ... |
| VIE  | Beijing | Sydney | Taekwondo | Women    | 49 - 57 kg | W | Silver |
| YUG  | Amsterdam | Tokyo | Aquatics | Women    | water polo | W | Silver |
| ZAM  | Atlanta | Los Angeles | Athletics | Men    | 400m hurdles | M | Silver |
| ZIM  | Athens | Moscow | Aquatics | Women    | hockey | W | Silver |
| ZZX  | Athens | St Louis | Athletics | Women    | tug of war | X | Silver |


# Using agg dict
olympics_df.groupby('NOC').agg({'Edition' :['count', 'min', 'max']})
# output
| Edition | count | min | max |
|---------|-------|-----|-----|
| AFG     | 1     | 2008| 2008|
| AHO     | 1     | 1988| 1988|
| ALG     | 14    | 1984| 2008|
| ANZ     | 29    | 1908| 1912|
| ARG     | 239   | 1924| 2008|
| ...     | ...   | ... | ... |
| VIE     | 2     | 2000| 2008|
| YUG     | 435   | 1924| 2000|
| ZAM     | 2     | 1984| 1996|
| ZIM     | 23    | 1980| 2008|
| ZZX     | 48    | 1896| 1904|

```