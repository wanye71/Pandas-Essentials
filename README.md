# Python pandas Essentials - Basic Analysins

## Using sort_values()
```python
olympic_df.Athlete.sort_values()

651                 AABYE, Edgar
2849       AALTONEN, Arvo Ossian
2852       AALTONEN, Arvo Ossian
7716    AALTONEN, Paavo Johannes
7730    AALTONEN, Paavo Johannes
                  ...           
603                   ÖSTMO, Ole
608                   ÖSTMO, Ole
621                   ÖSTMO, Ole
596                   ÖSTMO, Ole
8051           ÖSTRAND, Per-Olof
Name: Athlete, Length: 29216, dtype: object
```

```python
# Sort by multiple series
olympic_df.sort_values(by=['Edition', 'Athlete'])

City	Edition	Sport	Discipline	Athlete	NOC	Gender	Event	Event_gender	Medal
7	Athens	1896	Aquatics	Swimming	ANDREOU, Joannis	GRE	Men	1200m freestyle	M	Silver
82	Athens	1896	Gymnastics	Artistic G.	ANDRIAKOPOULOS, Nicolaos	GRE	Men	rope climbing	M	Gold
110	Athens	1896	Gymnastics	Artistic G.	ANDRIAKOPOULOS, Nicolaos	GRE	Men	team, parallel bars	M	Silver
111	Athens	1896	Gymnastics	Artistic G.	ATHANASOPOULOS, Spyros	GRE	Men	team, parallel bars	M	Silver
48	Athens	1896	Cycling	Cycling Road	BATTEL, Edward	GBR	Men	individual road race	M	Bronze
...	...	...	...	...	...	...	...	...	...	...
28095	Beijing	2008	Equestrian	Dressage	ZU-SAYN WITTGENSTEIN, Nathalie	DEN	Women	team	X	Bronze
28819	Beijing	2008	Sailing	Sailing	ZUBARI, Shahar	ISR	Men	RS:X - Windsurfer	M	Bronze
28977	Beijing	2008	Taekwondo	Taekwondo	ZUBCIC, Martina	CRO	Women	49 - 57 kg	W	Bronze
28387	Beijing	2008	Gymnastics	Rhythmic G.	ZUEVA, Natalia	RUS	Women	group competition	W	Gold
29007	Beijing	2008	Tennis	Tennis	ZVONAREVA, Vera	RUS	Women	singles	W	Bronze
29216 rows × 10 columns
```





