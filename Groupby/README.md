# Pandas Essentials - Groupby

## Groupby Computation
```python
# Get the count of medals for the Edition group
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
```

```python
# Group by edition, the country represented, and the medals
olympics_df.groupby(['Edition', 'NOC', 'Medal']).agg(['count'])
# output
City	Sport	Discipline	Athlete	Gender	Event	Event_gender
Edition	NOC	Medal							
1896	AUS	Gold	2	2	2	2	2	2	2
AUT	Bronze	2	2	2	2	2	2	2
Gold	2	2	2	2	2	2	2
Silver	1	1	1	1	1	1	1
DEN	Bronze	3	3	3	3	3	3	3
...	...	...	...	...	...	...	...	...	...
2008	UZB	Silver	2	2	2	2	2	2	2
VEN	Bronze	1	1	1	1	1	1	1
VIE	Silver	1	1	1	1	1	1	1
ZIM	Gold	1	1	1	1	1	1	1
Silver	3	3	3	3	3	3	3
2356 rows × 7 column


olympics_df.groupby(['Edition', 'NOC', 'Medal']).agg({'Edition' :['min', 'max', 'count']})
# output
Edition
min	max	count
Edition	NOC	Medal			
1896	AUS	Gold	1896	1896	2
AUT	Bronze	1896	1896	2
Gold	1896	1896	2
Silver	1896	1896	1
DEN	Bronze	1896	1896	3
...	...	...	...	...	...
2008	UZB	Silver	2008	2008	2
VEN	Bronze	2008	2008	1
VIE	Silver	2008	2008	1
ZIM	Gold	2008	2008	1
Silver	2008	2008	3
2356 rows × 3 columns


# Find Carl Lewis and then groupby Athlete
olympics_df[olympics_df.Athlete == 'LEWIS, Carl'].groupby(['Medal', 'Athlete']).agg({'Edition' :['min', 'max', 'count']})
# output
Edition
min	max	count
Medal	Athlete			
Gold	LEWIS, Carl	1984	1996	9
Silver	LEWIS, Carl	1988	1988	1
```