# Python pandas Essentials - Data Input and Validation

## Using head and tail
```python
# Return the first 5 rows with head()
olympic_df.head()

    City	Edition	Sport	Discipline	Athlete	NOC	Gender	Event	Event_gender	Medal
0	Athens	1896	Aquatics	Swimming	HAJOS, Alfred	HUN	Men	100m freestyle	M	Gold
1	Athens	1896	Aquatics	Swimming	HERSCHMANN, Otto	AUT	Men	100m freestyle	M	Silver
2	Athens	1896	Aquatics	Swimming	DRIVAS, Dimitrios	GRE	Men	100m freestyle for sailors	M	Bronze
3	Athens	1896	Aquatics	Swimming	MALOKINIS, Ioannis	GRE	Men	100m freestyle for sailors	M	Gold
4	Athens	1896	Aquatics	Swimming	CHASAPIS, Spiridon	GRE	Men	100m freestyle for sailors	M	Silver
```

```python
# Get the last 5 rows with tail()
olympic_df.tail()

City	Edition	Sport	Discipline	Athlete	NOC	Gender	Event	Event_gender	Medal
29211	Beijing	2008	Wrestling	Wrestling Gre-R	ENGLICH, Mirko	GER	Men	84 - 96kg	M	Silver
29212	Beijing	2008	Wrestling	Wrestling Gre-R	MIZGAITIS, Mindaugas	LTU	Men	96 - 120kg	M	Bronze
29213	Beijing	2008	Wrestling	Wrestling Gre-R	PATRIKEEV, Yuri	ARM	Men	96 - 120kg	M	Bronze
29214	Beijing	2008	Wrestling	Wrestling Gre-R	LOPEZ, Mijain	CUB	Men	96 - 120kg	M	Gold
29215	Beijing	2008	Wrestling	Wrestling Gre-R	BAROEV, Khasan	RUS	Men	96 - 120kg	M	Silver
```

```python
# Display specific number of rows from the beginning
olympic_df.head(3)

# Display specific number of rows from the end
olympic_df.tail(3)
```