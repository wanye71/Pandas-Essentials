# Python pandas Essentials - Indexing

## Using iloc[]
```python
df.iloc[1700]

Athlete         RABOT, Pierre
index                    1700
City                   London
Edition                  1908
Sport                 Sailing
Discipline            Sailing
NOC                       FRA
Gender                    Men
Event                      6m
Event_gender                X
Medal                  Bronze
Name: 1700, dtype: object
```

```python
df.iloc[[1542, 2390, 6000, 15000]]

| Athlete                  | index | City       | Edition | Sport      | Discipline      | NOC | Gender | Event                                  | Event_gender | Medal  |
|--------------------------|-------|------------|---------|------------|-----------------|-----|--------|----------------------------------------|--------------|--------|
| DUCKETT, Richard Louis  | 1542  | London     | 1908    | Lacrosse   | Lacrosse        | CAN | Men    | lacrosse                               | M            | Gold   |
| SAASTAMOINEN, Eino       | 2390  | Stockholm  | 1912    | Gymnastics | Artistic G.     | FIN | Men    | team, free system                     | M            | Silver |
| AGOSTONI, Carlo          | 6000  | Los Angeles| 1932    | Fencing    | Fencing         | ITA | Men    | épée individual                       | M            | Bronze |
| JENSEN, Poul Richard Hoj | 15000 | Montreal   | 1976    | Sailing    | Sailing         | DEN | Men    | fleet/match race keelboat open (Soling)| X            | Gold   |

```