# Pandas Essentials - Groupby

## The Groupby object
```python
# Groupby Edition
olympics_df.groupby('Edition')

# output
<pandas.core.groupby.generic.DataFrameGroupBy object at 0x0000029BB18E0ED0>
```

```python
# Get what type the Groupby object is
type(olympics_df.groupby('Edition'))

# output
pandas.core.groupby.generic.DataFrameGroupBy
```

```python
# Display Groupby object in a list
list(olympics_df.groupby('Edition'))

# output
[(1896,
         City  Edition          Sport       Discipline  \
  0    Athens     1896       Aquatics         Swimming   
  1    Athens     1896       Aquatics         Swimming   
  2    Athens     1896       Aquatics         Swimming   
  3    Athens     1896       Aquatics         Swimming   
  4    Athens     1896       Aquatics         Swimming   
  ..      ...      ...            ...              ...   
  146  Athens     1896  Weightlifting    Weightlifting   
  147  Athens     1896  Weightlifting    Weightlifting   
  148  Athens     1896      Wrestling  Wrestling Gre-R   
  149  Athens     1896      Wrestling  Wrestling Gre-R   
  150  Athens     1896      Wrestling  Wrestling Gre-R   
  
                        Athlete  NOC Gender                        Event  \
  0               HAJOS, Alfred  HUN    Men               100m freestyle   
  1            HERSCHMANN, Otto  AUT    Men               100m freestyle   
  2           DRIVAS, Dimitrios  GRE    Men   100m freestyle for sailors   
  3          MALOKINIS, Ioannis  GRE    Men   100m freestyle for sailors   
  4          CHASAPIS, Spiridon  GRE    Men   100m freestyle for sailors   
  ..                        ...  ...    ...                          ...   
  146             JENSEN, Viggo  DEN    Men  heavyweight - two hand lift   
  147       ELLIOTT, Launceston  GBR    Men  heavyweight - two hand lift   
  148  CHRISTOPOULOS, Stephanos  GRE    Men                   open event   
  149            SCHUMANN, Carl  GER    Men                   open event   
  150          TSITAS, Georgios  GRE    Men                   open event   
  
      Event_gender   Medal  
  0              M    Gold  
  1              M  Silver  
  2              M  Bronze  
  3              M    Gold  
  4              M  Silver  
  ..           ...     ...  
  146            M    Gold  
  147            M  Silver  
  148            M  Bronze  
  149            M    Gold  
  150            M  Silver  
  
  [151 rows x 10 columns]),
 (1900,
        City  Edition       Sport  Discipline  \
  151  Paris     1900    Aquatics    Swimming   
  152  Paris     1900    Aquatics    Swimming   
  153  Paris     1900    Aquatics    Swimming   
  154  Paris     1900    Aquatics    Swimming   
  155  Paris     1900    Aquatics    Swimming   
  ..     ...      ...         ...         ...   
  658  Paris     1900  Tug of War  Tug of War   
  659  Paris     1900  Tug of War  Tug of War   
  660  Paris     1900  Tug of War  Tug of War   
  661  Paris     1900  Tug of War  Tug of War   
  662  Paris     1900  Tug of War  Tug of War   
  
                                 Athlete  NOC Gender            Event  \
  151                     HALMAY, Zoltan  HUN    Men  1500m freestyle   
  152                JARVIS, John Arthur  GBR    Men  1500m freestyle   
  153                        WAHLE, Otto  AUT    Men  1500m freestyle   
  154                    DROST, Johannes  NED    Men  200m backstroke   
  155                  HOPPENBERG, Ernst  GER    Men  200m backstroke   
  ..                                 ...  ...    ...              ...   
  658                       COLLAS, Jean  FRA    Men       tug of war   
  659                  GONDOUIN, Charles  FRA    Men       tug of war   
  660  HENRIQUEZ DE ZUBIERRA, Constantin  FRA    Men       tug of war   
  661                      ROFFO, Joseph  FRA    Men       tug of war   
  662                     SARRADE, Emile  FRA    Men       tug of war   
  
      Event_gender   Medal  
  151            M  Bronze  
  152            M    Gold  
  153            M  Silver  
  154            M  Bronze  
  155            M    Gold  
  ..           ...     ...  
  658            M  Silver  
  659            M  Silver  
  660            M  Silver  
  661            M  Silver  
  662            M  Silver  
  
  [512 rows x 10 columns]),
  ...
```