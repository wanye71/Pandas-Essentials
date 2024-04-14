# Python pandas Essentials - Basic Analysins

## Using value_counts()
```python
# Check to see how many medals were presented each time the Olympics were held
olympic_df.Edition.value_counts()

2008    2042
2000    2015
2004    1998
1996    1859
1992    1705
1988    1546
1984    1459
1980    1387
1976    1305
1920    1298
1972    1185
1968    1031
1964    1010
1952     889
1912     885
1956     885
1924     884
1960     882
1936     875
1948     814
1908     804
1928     710
1932     615
1900     512
1904     470
1896     151
Name: count, dtype: int64
```

```python
# Get how many medals were givin to Men and Women
olympic_df.Gender.value_counts()

Gender
Men      21721
Women     7495
Name: count, dtype: int64
```

```python
# Sort the returned data as assencding
olympic_df.Gender.value_counts(ascending=True)

Gender
Women     7495
Men      21721
Name: count, dtype: int64
```





